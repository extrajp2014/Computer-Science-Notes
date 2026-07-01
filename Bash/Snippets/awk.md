# EXAMPLES
```bash
# awk - Search and Trim Text Lines according to keyword criterion 

## COMMON
# extract all python functions from .py files
find "." -type f -name "*.py" -print0 | xargs -0 awk '/^def / {print; in_block = 1; next} in_block && /^    / {print; next} {in_block = 0}'
# print line 6
awk '{print $6}'
awk 'NR==6'
# print line 6 to end
awk '{ for(i=6; i<NF; i++) printf "%s",$i OFS; if(NF) printf "%s",$NF; printf ORS}'
# print column 3, 4
awk '{print $3 "\t" $4}'
# print line with more than 18 chars
awk 'length($0) > 18'
# change specific word (DEBUG, ERROR, INFO) to another color
awk '{gsub(/INFO/, "\033[0;32m&\033[0m"); gsub(/DEBUG/, "\033[0;33m&\033[0m"); gsub(/ERROR/, "\033[0;31m&\033[0m")} 1' your_file.log

# cut out url only
text='<DT><A HREF="https://www.gtdb.to/home.php" ADD_DATE="1639408617" ICON="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAAByElEQVQ4jZ2TT0iTYRzHP+/rNofbqM0h6LaUJWU20S0CDx2MWpHhoFM3LyERFAQdOgjdhOgSdOoPBF4TuknkIRnoZXnIoloujFdwNEabI3qd77v3eTq8KRm+K/ten+fz4csPvsrc3TN3QJlUwMM+IsEAOaX+DwxgM8qk+q/wga5+OhPncLX6dklcfwN94W760tcJHhpCCsFbQ6e8srDz3lQQTWU4cvoqllnnc/YpxXcvMX5Udv3ZW6Ao9KVvEE2OUS4s8uHFfczNml36j+wpOHb+JpHBUbTcDIX5J4R6UvQMX+Zg5DilfJb3s/ecBdHkGJHBUdaWnlOYf0zsxCWOnr2GFAJhNfD4250beHwhekcm+Lb6mpVXj3B5A/SOXOHrxyyrC9PET42DEM6CWCqDtEy7ohSIxhaLD8d3DtfqD/+6hYOgPX4SLTeDoW8AIBoGhlUl1J0kmsoQjA2gV4vOArc3QP17GUVR8XfECR8epjORpi3YZQtFg3qt5CyorC2TuHib/gu3UFvcCMukor1Byz2jqi2jb6yDlM6CT3MPqHxZwu0NoFfXqRXzWOYmzeKSYGzvQVgmpXy2KfB7JBgqyCl7mvvL9px/Agqlq8D/LqvkAAAAAElFTkSuQmCC">'
echo "$text" | awk -F'"' '/HREF=/{print $2}'
# Extract the URL using parameter expansion
url="${text#*HREF=\"}"
url="${url%%\"*}"
echo $url

# ADVANCE
awk '
{
    x=reverse($0) (x?"\n":"") x
}

END{
    print x
}

function reverse(s,    p)
{
    for(i=length(s);i>0;i--)
        p=p substr(s,i,1)
    return p
}'


# print line 6 to end
awk '{ for(i=6; i<NF; i++) printf "%s",$i OFS; if(NF) printf "%s",$NF; printf ORS}'
awk -v f="wantedText" '$0 ~ f && $0 !~ /google/ && $0 !~ /twitter/ && $0 !~ /feed/ && $0 !~ /disqus/ {print $2}' | sort | uniq
x=$(youtube-dl --list-formats $1 | tail -1 | awk '{print $1}')

# store variables
awk 'BEGIN { 
   for (i = 0; i < ARGC - 1; ++i) { 
      printf "ARGV[%d] = %s\n", i, ARGV[i] 
   } 
}' one two three four
#result
# ARGV[0] = awk
# ARGV[1] = one
# ARGV[2] = two
# ARGV[3] = three

# NOTE - An example to matching lines starting with FOO1, or FOO2, or ... FOO9
awk '/^FOO[1-9]*/'

# NOTE - Below shows range based filtering power of awk
# NOTE - It prints the **lines** between the patterns,
# inclusive of the pattern matching lines
cat ls.txt
# CUnitAutomated-Listing.xml
# CUnitAutomated-Results.xml
# cunit-to-junit.pl
# Desktop
# Documents
# Downloads

cat ls.txt | awk '/D/,/s/'
# Desktop
# Documents
# Downloads

# NOTE - Below shows the way to exclude the patterns while printing
cat ls.txt
# Hi Hello
# Bye Bye

# NOTE - excludes the starting match
cat ls.txt | awk '/Hi/,/Bye/ {if (!/Hi/) print}'
# Bye Bye

# NOTE - excludes both the starting & ending match
# NOTE - Since there are no lines within the matching lines, nothing is printed
cat ls.txt | awk '/Hi/,/Bye/ {if (!/Hi/&&!/Bye/) print}'
#

# NOTE - Below shows the terse power of awk in doing the above stuff
# NOTE - Below prints the lines within the matching ranges; matched lines excluded
somecmd | awk '/endpattern/{p=0};p;/beginpattern{p=1}'

# NOTE - Prints the lines within the matching ranges; excluding the endpattern
somecmd | awk '/beginpattern/{p=1} /endpattern/{p=0} p'

# NOTE - Prints the lines within the matching ranges; excluding the beginpattern
somecmd | awk 'p; /endpattern/{p=0} /beginpattern/{p=1}'

awk -v f="wantedText" '$0 ~ f && $0 !~ /google/ && $0 !~ /twitter/ && $0 !~ /feed/ && $0 !~ /disqus/ {print $2}' | sort | uniq

# get mac address into a table view
 sudo nmap -sn "192.168.1.0/24" | awk '/Nmap scan report/{ip=$NF;getline;getline;print ip, $3}' | column -t

# REFERENCE
# https://www.howtogeek.com/562941/how-to-use-the-awk-command-on-linux/
# https://www.geeksforgeeks.org/awk-command-unixlinux-examples/
```
# EXAMPLES
```bash
# EXAMPLES

# COMMON
sed 's/find/replace/' file
# this remove _480_resolution from text
new_filename=$(echo "$new_filename" | sed 's/_480_resolution//')

# this extract https:* from text:
# <A HREF="https://www.example.com/Black-Silver-Wire-Mesh-Pencil-Holders/p327376/index.pro"
sed -n 's/.*HREF="\([^"]*\)".*/\1/p'

# Extract the word between "secure" and "for" using sed
sentence="GitHub is a trusted and secure platform for developers to collaborate, code, build"
extracted_word=$(echo "$sentence" | sed 's/.*secure //;s/ for.*//')
echo "Extracted word: $extracted_word"

# Extract line 1
sed '1d;q'
sed '1!d'

# Replace text
cat text.log | awk '{print $8}' | sed 's/https:\/\/yahoo.com\///' | sed 's/https:\/\/www.google.com\///' | sed 's/.$//' | sort | uniq

# remove data-count=" and anything before it
echo "$text_cut2" | sed 's/.*data-date=\"//' | sed 's/\".*//'

# ADVANCE SED
# for -> while -> wget -> grep -> cut -> awk
pagenum=2
pagenum_to_url=$(for num in $(seq 1 "$pagenum"); do echo "$keyword&p=$num"; done )
echo "$pagenum_to_url" | while read line; do wget -O temp.out "$line"; cat temp.out | grep "funny" | cut -b 7- | rev | cut -b 7- | rev | awk '{  printf("https://www.google.com%s\n", $1); }' >> test.out ; done

# remove whitespace from the BEGINNING of the line and remove BLANK LINES
| sed -e 's/^\s*//' -e '/^$/d'
# remove ALL whitespace
| sed 's: ::g'

for fname in $( ls | grep -v 'a.sh' ); do
    dt=$( echo ${fname} | sed -E 's/([0-9]{4}-[0-9]{2}-[0-9]{2})-.*/\1/' )
    sdt=$( echo ${dt} | sed -E 's/-/\//g')
    title=$( echo ${fname} | sed -E "s/${dt}-//" )
    newurl="/post/${fname%%.md}/"
    oldurl="/${sdt}/${title%%.md}.html"
    cat <<-EOF
aliases:
  - ${newurl}
  - ${oldurl}
EOF
done

# Using a single Awk:
# That is, using as field separator either / or :, the username is always in field 5.
... | awk -F '[/:]' '{print $5}'

# To store it in a variable:
username=$(... | awk -F '[/:]' '{print $5}')

# A more flexible implementation with sed that doesn't require username to be field 5:
... | sed -e s/:.*// -e s?.*/??

```

## REFERENCE
http://www.theunixschool.com/2014/08/sed-examples-remove-delete-chars-from-line-file.html
https://stackoverflow.com/questions/19482123/extract-part-of-a-string-using-bash-cut-split
https://www.linode.com/docs/tools-reference/tools/manipulate-text-from-the-command-line-with-sed/

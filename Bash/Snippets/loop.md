# For Loop Example
```bash
# Counter
for i in $(seq 0 20); do
    echo "$i"
done

# Get word from file into loop (parse based on space)
filename=~/Log/scheduleJob.log
filelines=`cat $filename`
echo Start
for line in $filelines ; do
    echo $line
done

# Get word from file into loop (parse based on space)
list=($(cat ~/Log/scheduleJob.log))

for i in ${list[*]}; do
    echo "$i"
done

```

# While Loop Example
```bash
# Read line from file into While loop (parse based on line)
# This skips the last line if running with another .sh
while read p; do
  echo "$p"
done <~/Log/scheduleJob.log

# Read line from Multiple Files into While loop (parse based on line)
while read -u 3 -r line1 && read -u 4 -r line2; do
  # process the lines
  # note that the loop will end when we reach EOF on either of the files, because of the `&&`
done 3< input1.txt 4< input2.txt

# Read line from file into While loop (parse based on line)
fileName=~/Log/scheduleJob.log
cat $fileName | while read line
do
   # do something with $line here
   echo $line
done

# Read line from file into While loop (parse based on line)
filename=~/Log/scheduleJob.log
exec 4<$filename
echo Start
while read -u4 p ; do
    echo $p

# Read line into arrays
while read -r line || [[ $line ]]; do
    my_array+=("$line")
done < my_file
```
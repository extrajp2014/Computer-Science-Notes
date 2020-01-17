# EXAMPLES
```bash
# Routines
sed 's/find/replace/' file

# Extract line 1
sed '1d;q'
sed '1!d'

# Examples
cat text.log | awk '{print $8}' | sed 's/https:\/\/yahoo.com\///' | sed 's/https:\/\/www.google.com\///' | sed 's/.$//' | sort | uniq
```

# REFERENCE
http://www.theunixschool.com/2014/08/sed-examples-remove-delete-chars-from-line-file.html

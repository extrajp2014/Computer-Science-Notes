# EXAMPLES
```bash
# print line 6
awk '{print $6}'
awk 'NR==6'

# print line 6 to end
awk '{ for(i=6; i<NF; i++) printf "%s",$i OFS; if(NF) printf "%s",$NF; printf ORS}'
```
 ### Arrays and similar in Bash
 
 good examples variables in Bash : https://linuxhint.com/variables-bash-programming/
 I copy here the last one:
 ```
 #!/bin/bash
 
myarr=(HTML JavaScript PHP jQuery AngularJS CodeIgniter)
 
#Count total number of elements of the array
total=${#myarr[*]}
echo "Total elements: $total"
 
#Print each element value of the array
echo "Array values :"
for val in ${myarr[*]}
do
printf "   %s\n" $val
done
 
#Print each element value of the array with key
 
echo "Array values with key:"
for key in ${!myarr[*]}
do
printf "%4d: %s\n" $key ${myarr[$key]}
done
```

Another tip: to do `ls` using different patterns of files :
```
s2_4=$(ls {2_*,4_*})
for i in ${s2_4}; do
	echo $i
done
```
that will print 
2_ddstabplots.R
4_fgsea_fromDEGs.R





# bash function

```bash
function trans { 
	vocabulary_file="/Users/batur/vocabulary.md";
	DATE=`date +%Y-%m-%d`;
	if grep -q "$1" $vocabulary_file
	    then ts "$1";
	else
		if grep -q $DATE $vocabulary_file
			then echo "- $1" >> $vocabulary_file && ts "$1" ;
		else
			echo "$DATE"  >> $vocabulary_file && ts "$1"  && 
			echo "- $1" >> $vocabulary_file ;
		fi
	fi
}
```

/Users/batur

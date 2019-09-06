## Dictionaries in bash
I was looking for a way to set the commandline parameters of C executable based on one of the parameters. One way would have been to use a `python` script to run the executable and have a `dict` to get the mappings. But this involves using `subprocess` and checking its output. `bash` somehow seems a more "native" way of running executables. Turns out from version 4, `bash` does support dictionaries, although it calls it "associative arrays". They are declared like this:

```bash
declare -A chardict=(['A']=1 ['B']=2 ['C']=3)
```


The way to access the value it is pretty convenient as well:
```bash
echo ${chardict['A']}
``` 

A little cumbersome to iterate through the keys but it is similar to the way to iterate through arrays
```bash
for alpha in "${!chardict[@]}";
do
	echo ${chardict[${alpha}]}
done
```

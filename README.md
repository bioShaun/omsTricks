# omsTricks

Simple solutions for some frequently met bioinformatics & programming problems.

-----

## Contents

- [Bioinformatics](#bioinformatics)
- [Programming](#programming)


## Bioinformatics 
[[back to top](#contents)]

### Data Format

> Methods for convertion between common bioinformatics data format.

#### gtf -> GenePred

Download [gtfToGenePred](http://hgdownload.cse.ucsc.edu/admin/exe/linux.x86_64/gtfToGenePred) from UCSC

```bash

gtfToGenePred \
    -genePredExt \
    -ignoreGroupsWithoutExons \
    your.gtf \
    /dev/stdout | \
    awk 'BEGIN { OFS="\t"} {print $12, $1, $2, $3, $4, $5, $6, $7, $8, $9, $10}' > your.GenePred


```


## Programming
[[back to top](#contents)]

### Python

#### Get beijing time when your server timezone is UTC

```python

import maya

time_now = maya.now().datetime(to_timezone='Asia/Shanghai')

```

#### Convert string representation of list to list in Python

```python

import ast
x = u'[ "A","B","C" , " D"]'
x = ast.literal_eval(x)

```

### Bash

#### Split string to list

```bash

#!/bin/bash
  
str="hello,world,i,like,you,babalala" 
arr=(${str//,/ }) 
for i in ${arr[@]} 
do 
    echo $i 
done

```

# omsTricks

Simple solutions for some frequently met bioinformatics problems.

-----

## Data Format

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

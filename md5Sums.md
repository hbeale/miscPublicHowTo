## Generate an MD5 sum

 md5sum TCGA_pancancer_somatic_mutation_broad.maf.txt
 
 output: 4ae1b6902bed73d7faaaa2e8ab5809f9  TCGA_pancancer_somatic_mutation_broad.maf.txt



## Confirm MD5 sum:

on FTP server:
md5sum bcbioWgsGRCh37ref.tgz

output: 0164fae369a1349f6502a92f88dcf791  bcbioWgsGRCh37ref.tgz



on server i downloaded from:

echo "0164fae369a1349f6502a92f88dcf791  bcbioWgsGRCh37ref.tgz" > /tmp/sourceMd5.txt

cd /tmp

 md5sum -c sourceMd5.txt

output: bcbioWgsGRCh37ref.tgz: OK


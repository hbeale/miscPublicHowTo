
MD5 sum confirmation:

on FTP server:
md5sum bcbioWgsGRCh37ref.tgz

output: 0164fae369a1349f6502a92f88dcf791  bcbioWgsGRCh37ref.tgz



on server i downloaded from:

echo "0164fae369a1349f6502a92f88dcf791  bcbioWgsGRCh37ref.tgz" > /tmp/sourceMd5.txt

cd /tmp

 md5sum -c sourceMd5.txt

output: bcbioWgsGRCh37ref.tgz: OK


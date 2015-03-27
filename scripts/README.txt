(*) Adding the Apache license to generated proto buf files.

cat apache-license.txt | perl -0 -i -pe 'BEGIN {$h = <STDIN>}; print $h' <files>

For many files, this can be done with
Thanks to http://stackoverflow.com/questions/6141088/append-a-text-on-the-top-of-the-file

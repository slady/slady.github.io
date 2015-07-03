If you have multiple files compressed using the gzip tool
and you want to unzip all the files in a directory using a shell
(this is the Linux command line script),
run the following line:

    for x in *.gz ; do gzip -d $x ; done

Warning! This command will delete the original zipped files!

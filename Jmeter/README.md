To run Jmeter from container:  
docker run --detach --rm --volume `pwd`:/file jmeter --nongui --testfile mytest.jmx --logfile result.jtl -e -o file

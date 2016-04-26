# QuickX

[Quicksort](https://en.wikipedia.org/wiki/Quicksort) encounters stack-overflow if a pivot is chosen from fixed position in a array.
This project exhibits a sample of stack-overflow with a pivot scheme known as pseudomedian of nine. 

    $ cd /tmp
    $ wget http://introcs.cs.princeton.edu/java/stdlib/stdlib.jar
    $ wget http://algs4.cs.princeton.edu/23quicksort/QuickX.java
    $ wget https://github.com/leorge/qmisort/raw/master/KillQuickX.pl
    $ chmod +x KillQuickX.pl
    $ javac -cp .:stdlib.jar QuickX.java
    $ ./KillQuickX.pl 40000 | java -cp .:stdlib.jar QuickX 2>&1 | head

Files in this project are downloaded by wget commands above.

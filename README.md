# QuickX

[Quicksort](http://algs4.cs.princeton.edu/23quicksort)
encounters stack-overflow if a pivot is chosen from fixed position in a array.
This project exhibits a sample of stack-overflow by QuickX.java
which chooses the pseudomedian of nine as a pivot.

    $ cd /tmp
    $ wget http://introcs.cs.princeton.edu/java/stdlib/stdlib.jar
    $ wget http://algs4.cs.princeton.edu/23quicksort/QuickX.java
    $ wget https://github.com/leorge/qmisort/raw/master/KillQuickX.pl
    $ chmod +x KillQuickX.pl
    $ javac -cp .:stdlib.jar QuickX.java
    $ ./KillQuickX.pl 40000 | java -cp .:stdlib.jar QuickX 2>&1 | head
    Exception in thread "main" java.lang.StackOverflowError 
	at QuickX.sort(QuickX.java:60) 
	at QuickX.sort(QuickX.java:94) 
	at QuickX.sort(QuickX.java:94) 
	at QuickX.sort(QuickX.java:94) 
	at QuickX.sort(QuickX.java:94) 
	at QuickX.sort(QuickX.java:94) 
	at QuickX.sort(QuickX.java:94) 
	at QuickX.sort(QuickX.java:94) 
	at QuickX.sort(QuickX.java:94) 

Files in this project are downloaded by wget commands above.

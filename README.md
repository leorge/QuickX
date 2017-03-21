# QuickX

The [pseudomedian of nine](https://en.wikipedia.org/wiki/Quicksort#History)
encounters stack-overflow as below.  
**QuickX.java** and **stdlib.jar** were downloaded by the wget commands below.


    $ cd /tmp
    $ wget http://introcs.cs.princeton.edu/java/stdlib/stdlib.jar
    $ wget http://algs4.cs.princeton.edu/23quicksort/QuickX.java
    $ wget https://github.com/leorge/QuickX/raw/master/KillQuickX.pl
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

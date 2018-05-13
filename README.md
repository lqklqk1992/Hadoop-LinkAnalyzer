# Hadoop-LinkAnalyzer

Description:
This is a MapReduce program to calculate the frequency of every link in all input files from
the attached input directory, and sort the result by their frequency in descending order. You need to:
1. Use MapReduce to calculate the frequency of every links in all files, just like the "WordCount" of the
links. (To simplify this work, you can use getAllStartTags("a") and then use getAttributeValue("href")
in the htmlparser package to get the content of the links.)
2. After frequency calculation, sort the result by their frequency in descending order.
3. The links occurred less than six ( 5) times should be ignored.
4. Output each links followed by their frequency in each line (see the sample output).

Command:
1.Compile LinkAnalyzer.java
export CLASSPATH=$($HADOOP_HOME/bin/hadoop classpath):$CLASSPATH
javac LinkAnalyzer.java

2.Put all .class into LinkAnalyzer.jar
jar cf LinkAnalyzer.jar *.class net/htmlparser/jericho/*

3.Run the program LinkAnalyzer.jar
hadoop jar LinkAnalyzer.jar LinkAnalyzer input output

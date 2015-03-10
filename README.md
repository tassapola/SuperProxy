SuperProxy
==========

Java source code, hadoop config and documentation of SuperProxy project

The project is to implement scalable web proxy with HDFS as cache filesystem. 
It consists of mainly 2 parts: configuring HDFS and writing Java Servlet code.
Once deployed, a user can go to SuperProxy on the web and enters target URL. SuperProxy will fetch contents from target 
URL, do URL rewriting and save contents into HDFS. Next time any user wants to access contents from the same URL, 
SuperProxy sends small request to see if there is any updates based on HTTP Header Modified-by. If there is no updates, 
SuperProxy will return cached contents. The purpose is to optimize network traffic needed and to improve response time.

The project is originally located at https://code.google.com/p/cse124tassapol2/

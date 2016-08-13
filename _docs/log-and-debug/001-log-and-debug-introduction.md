---
title: "Log and Debug Introduction"
date: 2016-06-29 01:29:06 UTC
parent: "Log and Debug"
---

You can use the Drill logs in conjunction with query profiles to troubleshoot issues that you encounter. Drill uses Logback as its default logging system. Logback behavior is defined by configurations set in `<drill_installation_directory>/conf/logback.xml`. 

You can configure Logback to enable specific loggers for particular components. You can also enable Logback to output log messages to Lilith, a desktop application that you can use for socket logging. By default, Drill outputs log files to `$DRILL_HOME/logs`. You can edit the `DRILL_LOG_DIR` variable in `drill-env.sh` to change the location of the log directory, if needed.

Drill outputs two standard log files:  

* `drillbit.out`
* `drill.log`

Drill provides a special file, `drillbit_queries.json`, on each Drill node. This log provides the QueryID and profile for every query run on a Drillbit. The Profile view in the Drill Web Console lists the last one-hundred queries that Drill ran. To see information for queries beyond the last one-hundred, you can view the `drillbit_queries.json` file on each Drill node.

Drill provides [audit logging]({{site.baseurl}}/docs/query-audit-logging/) of queries executed by various drillbits in the cluster. 

As of Drill 1.7, you can access the log files generated by the Drillbit process running on a particular node from the Logs page in the Drill Web Console. Currently, you can only see the logs for the Drillbit process running on the node used to access the Web Console.

In a web browser, navigate to the Drill Web Console at `http://<host_ip_address>:8047` and click on **Logs** to access the Logs page. The Logs page provides a list of links that correlate with the log files stored in `$DRILL_HOME/logs`.  

![Drill Web Console Logs page](http://i.imgur.com/HsZ7p1H.png)
 



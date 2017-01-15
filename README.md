# Report Info

A view with some information from Surefire, PMD, Findbugs and Checkstyle reports.

![screen](https://github.com/gcolin/report-info/raw/master/screen.png)

## How it works

This plugins adds a view that extends ListView. When the view is displayed, the plugin looks for XML supported files for building information in the top of the view. For efficiency, the collected data are cached in an XML file. Thus the RAM memory is not affected and the reloading is fast.

## What report are supported

* The **Surefire** report with name *TEST-.&#42;\.xml*
* The **PMD** XML report with name *pmd.xml*, *build/reports/pmd/main.xml* and *build/reports/pmd/test.xml*
* The **FindBugs** XML report with name *findbugs.xml*, *build/reports/findbugs/main.xml* and *build/reports/findbugs/test.xml*
* The **Checkstyle** XML report with name *checkstyle-result.xml*, *build/reports/findbugs/main.xml* and *build/reports/findbugs/test.xml*

## Known issues

FindBugs report generated by the *findbugs-maven-plugin* are not read.

## How to build

Install maven and execute:

```
    mvn install
```

The file **reportinfo.hpi** can be imported into Jenkins (*pluginManager/advanced* -> Upload Plugin). 

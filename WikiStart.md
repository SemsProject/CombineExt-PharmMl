PharmML Extension for /CombineExt 
==================================
This is an extension for the [CombineExt library](combine-ext:wiki) to support [PharmML](http://pharmml.org/).

Ingredients of this Repository 
-------------------------------
* [source:src/main/java/de/unirostock/sems/cbext/pharmml//PharmMlRecognizer.java /PharmMlRecognizer.java] a recognizer for PharmML files. It extends the [FormatRecognizer class](http://sems.uni-rostock.de/trac/combine-ext/wiki//src/main/java/de/unirostock/sems/cbext//FormatRecognizer.java​), see [Extend/CombineFormatizer](http://sems.uni-rostock.de/trac/combine-ext/wiki///ExtendCombineFormatizer) and [CombineFormatizer](http://sems.uni-rostock.de/trac/combine-ext/wiki///CombineFormatizer)

* [source:src/main/java/de/unirostock/sems/cbext/pharmml//PharmMlIcon.java /PharmMlIcon.java] a icon collection providing the PharmML icon. It extends the [IconCollection class](http://sems.uni-rostock.de/trac/combine-ext/wiki//src/main/java/de/unirostock/sems/cbext//IconCollection.java​), see [Extend/CombineIconizer](http://sems.uni-rostock.de/trac/combine-ext/wiki///ExtendCombineIconizer) and [CombineIconizer](http://sems.uni-rostock.de/trac/combine-ext/wiki///CombineIconizer). it delivers the following icon: ![None](source:src/main/resources/icons/Green-pharmml.png)

* [source:src/main/java/de/unirostock/sems/cbext/pharmml/Demo.java Demo.java] demonstrating how to use this library



Download and Use 
-----------------
* Binaries are available from our binary repository, or see /BuildCombineExtPharmMl
* include the project via Maven: ([find latest version id](http://mvn.sems.uni-rostock.de/releases/de/unirostock/sems///CombineExtPharmML), import the [SEMS Maven repository](https://sems.uni-rostock.de/2013/10/maven-repository/))
```
#!xml
<dependency>
    <groupId>de.unirostock.sems</groupId>
    <artifactId>CombineExtPharmML</artifactId>
    <version>$VERSION</version>
</dependency>
```
* see above (parts of this project) to learn how to use this package

DEV 
----
* /src/main/java/de/unirostock/sems/cbext/pharmml
* [JavaDoc](http://jdoc.sems.uni-rostock.de///CombineExtPharmML/)
* /BuildCombinePharmMl
* find open bugs/issues and requests: {1}
* file an issue or feature request: [None](/newticket)



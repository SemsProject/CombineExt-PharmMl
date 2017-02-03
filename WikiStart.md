PharmML Extension for CombineExt 
==================================

This is an extension for the [CombineExt library](http://sems.uni-rostock.de/trac/combine-ext/wiki) to support [PharmML](http://pharmml.org/).

Ingredients of this Repository 
-------------------------------

* [PharmMlRecognizer.java](https://github.com/SemsProject/CombineExt-PharmMl/blob/master/src/main/java/de/unirostock/sems/cbext/pharmml/PharmMlRecognizer.java) a recognizer for PharmML files. It extends the [FormatRecognizer](http://sems.uni-rostock.de/trac/combine-ext/wiki/CombineFormatizer), see [Extend CombineFormatizer](http://sems.uni-rostock.de/trac/combine-ext/wiki/ExtendCombineFormatizer).
* [PharmlIcon.java](https://github.com/SemsProject/CombineExt-PharmMl/blob/master/src/main/java/de/unirostock/sems/cbext/pharmml/PharmMlIcon.java) a icon collection providing the PharmML icon. It extends the [IconCollection](http://sems.uni-rostock.de/trac/combine-ext/wiki/CombineIconizer), see [Extend CombineIconizer](http://sems.uni-rostock.de/trac/combine-ext/wiki/ExtendCombineIconizer).
* [Demo.java](https://github.com/SemsProject/CombineExt-PharmMl/blob/master/src/main/java/de/unirostock/sems/cbext/pharmml/Demo.java) demonstrating how to use this library


Download and Use 
-----------------

* Binaries are available from our binary repository, or see [build instructions](BuildCombineExtPharmMl)
* include the project via Maven: ([find latest version id](https://github.com/SemsProject/maven-repository/tree/releases/de/unirostock/sems/CombineExtPharmMl), import the [SEMS Maven repository](https://sems.uni-rostock.de/2013/10/maven-repository/))

```xml
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
* [JavaDoc](http://jdoc.sems.uni-rostock.de/CombineExtPharmML/)
* [BuildCombinePharmMl](BuildCombinePharmMl)
* find open bugs/issues and requests at [GitHub](https://github.com/SemsProject/CombineExt-PharmMl/issues)


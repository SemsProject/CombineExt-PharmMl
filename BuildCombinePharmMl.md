Build CombineExt-PharmML
========================

When you've cloned the source code:

```sh
git clone git@github.com:SemsProject/CombineExt-PharmMl.git
```

There are two supported options to build this project:

* [Build with Maven](#build-with-maven)
* [Build with Ant](#build-with-ant)


Build with Maven 
-----------------

[Maven](https://maven.apache.org/) is a build automation tool. We ship a `pom.xml` together with the sources which tells maven about versions and dependencies. Thus, maven is able to resolve everything on its own and, in order to create the library, all you need to call is `mvn package`:

```sh
usr@srv $ mvn package

[INFO] Scanning for projects...
[INFO]                                                                         
[INFO] ------------------------------------------------------------------------
[INFO] Building CombineExtPharmML 1.2
[INFO] ------------------------------------------------------------------------
[WARNING] The POM for xom:xom:jar:1.2.1 is missing, no dependency information available
[INFO] 
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ CombineExtPharmML ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] Copying 1 resource
[INFO] 
[INFO] --- maven-compiler-plugin:3.2:compile (default-compile) @ CombineExtPharmML ---
[INFO] Nothing to compile - all classes are up to date
[INFO] 
[INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ CombineExtPharmML ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] skip non existing resourceDirectory /users/stud00/mp487/mig-git/combine-ext-pharmml/src/test/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.2:testCompile (default-testCompile) @ CombineExtPharmML ---
[INFO] Nothing to compile - all classes are up to date
[INFO] 
[INFO] --- maven-surefire-plugin:2.17:test (default-test) @ CombineExtPharmML ---
[INFO] Surefire report directory: /users/stud00/mp487/mig-git/combine-ext-pharmml/target/surefire-reports

-------------------------------------------------------
 T E S T S
-------------------------------------------------------
Running de.unirostock.sems.cbext.pharmml.PharmMlTest
 WARN (XMLNodeReader.java:262) - The type of String '' on the element constraint (Constraint) is unknown! Some data might be lost.
 WARN (AbstractReaderWriter.java:97) - processAttribute: The attribute 'schemaLocation' on the element PharmML is not part of the SBML specifications (XMLNode).
the format of file test/vancauter_v1.xml is recognized as http://purl.org/NET/mediatypes/application/xml
adding this extension to recognize PharmML
the format of file test/vancauter_v1.xml is recognized as http://identifiers.org/combine.specifications/pharmml
icon name for pharmml filesw/o this extension: Blue-unknown.png
adding this extension to provide an icon for PharmML
icon name for pharmml files w/ this extension: Green-pharmml.png
extracted icon to /tmp/pharmml6618543932702109493.png
 WARN (XMLNodeReader.java:262) - The type of String '' on the element constraint (Constraint) is unknown! Some data might be lost.
 WARN (AbstractReaderWriter.java:97) - processAttribute: The attribute 'schemaLocation' on the element PharmML is not part of the SBML specifications (XMLNode).
 WARN (XMLNodeReader.java:262) - The type of String '' on the element constraint (Constraint) is unknown! Some data might be lost.
 WARN (AbstractReaderWriter.java:97) - processAttribute: The attribute 'schemaLocation' on the element darmML is not part of the SBML specifications (XMLNode).
 WARN (XMLNodeReader.java:262) - The type of String '' on the element constraint (Constraint) is unknown! Some data might be lost.
 WARN (AbstractReaderWriter.java:97) - processAttribute: The attribute 'schemaLocation' on the element darmML is not part of the SBML specifications (XMLNode).
Tests run: 5, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 6.553 sec - in de.unirostock.sems.cbext.pharmml.PharmMlTest

Results :

Tests run: 5, Failures: 0, Errors: 0, Skipped: 0

[INFO] 
[INFO] --- maven-jar-plugin:2.4:jar (default-jar) @ CombineExtPharmML ---
[INFO] 
[INFO] --- maven-assembly-plugin:2.2.1:single (make-assembly) @ CombineExtPharmML ---

[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 16.704 s
[INFO] Finished at: 2017-02-14T13:15:42+01:00
[INFO] Final Memory: 26M/661M
[INFO] ------------------------------------------------------------------------
```

That done, you'll find the binaries in the `target` directory.

Build with Ant 
---------------

[Ant](https://ant.apache.org/) is an Apache tool for automating software build processes. There is a `build.xml` file included in the source code that tells ant what to do. Since ant is not able to resolve the dependencies you need to create a directory `lib` containing the following libraries:

* [Combine-Ext](https://semsproject.github.io/CombineExt/)
* [libPharmML](http://sourceforge.net/projects/libpharmml.ddmore.p/)
* [libPharmML-SO](http://sourceforge.net/projects/libpharmml.ddmore.p/)

We defined multiple targets in the `build.xml`. They can be displayed by calling `ant -p`:

```sh
usr@srv $ ant -p
Buildfile: /users/stud00/mp487/mig-git/combine-ext-pharmml/build.xml

        PharmML Extension for CombineExt

Main targets:

 clean    clean up
 compile  compile the source
 dist     generate the distribution
 init     initialize workspace
 sign     sign a dist
Default target: dist
```

* `clean` will delete all compiled files and produced libraries
* `compile` compiles the source code
* `dist` bundles all compiled binaries into a `jar` package

For example, to create the `jar` library just run `ant dist`:

```sh
usr@srv $ ant dist
Buildfile: /users/stud00/mp487/mig-git/combine-ext-pharmml/build.xml

init:
    [mkdir] Created dir: /users/stud00/mp487/mig-git/combine-ext-pharmml/build
    [mkdir] Created dir: /users/stud00/mp487/mig-git/combine-ext-pharmml/dist

compile:
    [javac] Compiling 3 source files to /users/stud00/mp487/mig-git/combine-ext-pharmml/build
    [javac] warning: Supported source version 'RELEASE_6' from annotation processor 'org.mangosdk.spi.processor.SpiProcessor' less than -source '1.8'
    [javac] 1 warning

dist:
      [jar] Building jar: /users/stud00/mp487/mig-git/combine-ext-pharmml/dist/CombineExtPharmMl-1.2.jar
      [jar] Building jar: /users/stud00/mp487/mig-git/combine-ext-pharmml/dist/CombineExtPharmMl-1.2-fat.jar

BUILD SUCCESSFUL
Total time: 5 seconds
ant dist  10.32s user 0.63s system 176% cpu 6.198 total
```

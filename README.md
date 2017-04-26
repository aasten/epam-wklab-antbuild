# Apache Ant build script task

Create a project with following structure:
* ant
* build.xml
* pom.xml

Apache Maven should be responsible for project packaging. 
Project artifact should be represented as zip package, containing 
* build.xml
Hint : use assembly maven plugin and assembly descriptor.
Ant build script should:
* create in, out, temp folders
* copy files with zip, xml, html, xhtml extensions from in to temp folder
* zip packages should be unpacked without folder structure (only files should be extracted). Zip package should contain xml, html, xhtml, png files.
* after extraction source zip files should be removed from temp folder
* list of xml, html, xhtml files in temp folder should be packed to zip package which should be copied to out folder. 
* clean target should be invoked before each build and should clean temp folder
* logging should be configured
* every target should print current time at the beginning and in the end of target execution.

Attach sample input files along with project sources.

# Solution
Artifact can be got by invoking maven with `assembly:single` goal.

Use `build.xml` within obtained zipped artifact.

Use provided `sample-in` folder to populate required by task `in` folder with sample files.

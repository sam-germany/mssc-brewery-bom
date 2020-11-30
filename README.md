# MSSC Brewery POM


-) Difference between <dependencyManagement> and <dependencies>


<dependencyManagement>

when we define  <dependencyManagement> in the parent POM then,
 we  need to define them in the child POM to show that you are using them. 
 They are not actually included in the child projects just because they are in 
 <dependencyManagement> in the parent POM. Enclosing dependencies in <dependencyManagement>
  centralizes management of the version, scope, and exclusions for each dependency, 
  if and when you decide to use it.

The <dependencyManagement>  is just  useful by helping you centralize the version of your dependencies.
  It is like a kind of helper feature
  
  
<dependencies>
all the dependencies defined in the <dependencies> section in your 
    parent- POM are inherited by all the child-projects automatically
---------------------------------------------------------------------------------------

-) Snapshot vs Version

In case of Version, if Maven once downloaded the mentioned version, say data-service:1.0,
 it will never try to download a newer 1.0 available in repository. To download the updated code,
  data-service version is be upgraded to 1.1.

In case of SNAPSHOT, Maven will automatically fetch the latest SNAPSHOT (data-service:1.0-SNAPSHOT)
 every time app-ui team build their project.

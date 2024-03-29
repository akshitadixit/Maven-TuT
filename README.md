<img src="https://maven.apache.org/images/maven-logo-black-on-white.png" align="center"> 

# Maven Tutorial
All applications, no matter how small or large, must undergo a specific process. These processes can be configured manually, but this becomes a burden. 

To solve this issue, we have Maven, which automates the entire process. This tutorial will help give you a clearer picture of what Maven is, the advantages of using it and setting it up.

<img src="https://img.shields.io/maven-central/v/org.apache.maven/apache-maven?style=plastic" align="center">

## Industry picture
Even though now Gradle, another build tool written in groovy, is capturing some ground of Maven, it is still the most popular build tool for Java projects. Gradle will take its time because it has a little bit of learning curve in terms of the Groovy and domain-specific language you use to write the build script but given Maven uses XML, anybody can understand the build process and build dependencies.<br/>
Some of the largest corporations that use Maven include:

* Accenture
* JPMorgan Chase & Co
* Via Varejo 
* craft base
* Red Hat 
* Mitratech Holdings, Inc.
* KRG TECHNOLOGIES
* Radio - Canada

This <a href="https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/Learn-Maven-and-master-the-build-tools-fundamental-concepts">article</a> talks about why learning Maven could be important for DevOps and beyond just building simple local projects.

## All about it
<details>
  <summary>What is Maven?</summary>
  A tool that can now be used for building and managing any Java-based project. It is a standard way to build the projects, a clear definition of what the project consists of, an easy way to publish project information, and a way to share JARs across several projects.
</details>
<details>
  <summary>How it helps?</summary>
  <ul><li> Your project becomes IDE independent and platform independent</li>
  <li> We can add jars and other dependencies of the project easily using the help of maven. One has to just write the dependency code in pom file.</li>
  <li>Model-based builds − Maven is able to build any number of projects into predefined output types such as jar, war, metadata, etc. without doing any scripting</li>
  <li> Using maven we can easily integrate our project with source control system (such as Subversion or Git)</li>
  <li> Maven provides project information (log document, dependency list, unit test reports etc.)</li></ul>
</details>
<details>
  <summary>Features of Maven</summary>
  <ul><li>A large and growing <a href="https://mvnrepository.com/">repository</a> of libraries.</li>
  <li>Extensible, with the ability to easily write plugins in Java or scripting languages.</li>
  <li>Instant access to new features with little or no extra configuration.</li>
  <li>Coherent site of project information − Using the same metadata as per the build process, maven is able to generate a website and a PDF including complete documentation.</li>
  <li>Release management and distribution publication − Without additional configuration, maven will integrate with your source control system such as CVS and manages the release of a project.</li>
  <li>Backward Compatibility − You can easily port the multiple modules of a project into Maven 3 from older versions of Maven. It can support the older versions also.</li>
  <li>Automatic parent versioning − No need to specify the parent in the sub module for maintenance.</li>
  <li>Parallel builds − It analyzes the project dependency graph and enables you to build schedule modules in parallel. Using this, you can achieve the performance improvements of 20-50%.</li>
  <li>Better Error and Integrity Reporting − Maven improved error reporting, and it provides you with a link to the Maven wiki page where you will get full description of the error.</li></ul>
</details>

## Understanding Archetypes
  Archetype is a Maven project templating toolkit. An archetype is defined as an original pattern or model from which all other things of the same kind are made. Archetype will help authors create Maven project templates for users, and provides users with the means to generate parameterized versions of those project templates.
  <table border="1">
<tr class="a">
<th align="left">Archetype ArtifactIds</th>
<th align="left">Description</th></tr>
<tr class="b">
<td align="left">maven-archetype-archetype</td>
<td align="left">An archetype to generate a sample archetype project.</td></tr>
<tr class="a">
<td align="left">maven-archetype-j2ee-simple</td>
<td align="left">An archetype to generate a simplifed sample J2EE application.</td></tr>
<tr class="b">
<td align="left">maven-archetype-mojo</td>
<td align="left">An archetype to generate a sample a sample Maven plugin.</td></tr>
<tr class="a">
<td align="left">maven-archetype-plugin</td>
<td align="left">An archetype to generate a sample Maven plugin.</td></tr>
<tr class="b">
<td align="left">maven-archetype-plugin-site</td>
<td align="left">An archetype to generate a sample Maven plugin site.</td></tr>
<tr class="a">
<td align="left">maven-archetype-portlet</td>
<td align="left">An archetype to generate a sample JSR-268 Portlet.</td></tr>
<tr class="b">
<td align="left">maven-archetype-quickstart</td>
<td align="left">An archetype to generate a sample Maven project.</td></tr>
<tr class="a">
<td align="left">maven-archetype-simple</td>
<td align="left">An archetype to generate a simple Maven project.</td></tr>
<tr class="b">
<td align="left">maven-archetype-site</td>
<td align="left">An archetype to generate a sample Maven site which demonstrates some of the supported document types like APT, XDoc, and FML and demonstrates how to i18n your site.</td></tr>
<tr class="a">
<td align="left">maven-archetype-site-simple</td>
<td align="left">An archetype to generate a sample Maven site.</td></tr>
<tr class="b">
<td align="left">maven-archetype-webapp</td>
<td align="left">An archetype to generate a sample Maven Webapp project.</td></tr></table>

## How to begin?
  <h4>Install JDK</h4>
  Visit this <a href="https://www.oracle.com/technetwork/java/javase/downloads/index.html">link</a> to download JDK compatible for your machine. Next, set the JAVA_HOME environment variable to point to the base directory location where Java is installed on your machine. Kindly look for proper ways to set this variable according to your OS. Then append Java compiler location to System Path. Test if it has been successfully installed and setup.<br/>
  For windows, open CMD: <code>c:\> java -version</code><br/>
  For linux, open terminal: <code>$ java -version</code><br/>
  For mac, open terminal: <code>machine:~ user$ java -version</code><br/>
  Verify the output similar to:<br/>
  <code>java version "1.7.0_60"</code><br/>
  <code>Java(TM) SE Runtime Environment (build 1.7.0_60-b19)</code><br/>
  <code>Java HotSpot(TM) 64-Bit Server VM (build 24.60-b09, mixed mode)</code><br/>
  <h4>Install Maven</h4>
  First, download <a href="https://maven.apache.org/download.html">Maven</a> and follow the installation instructions. The installation of Apache Maven is a simple process of extracting the archive and adding the `bin` folder with the `mvn` command to the `PATH`.
  <ul><li>Extract the archive in any directory</li>
  <li>Add the `bin` directory of the created directory apache-maven-3.8.1 to the `PATH` environment variable.</li>
  <li>After that, type the following in a terminal or in a command prompt: <code>mvn --version</code> and the result should look similar to:<br/>
  <code>Apache Maven 3.6.3 (cecedd343002696d0abb50b32b541b8a6ba2883f)</code><br/>
  <code>Maven home: D:\apache-maven-3.6.3\apache-maven\bin\..</code><br/>
  <code>Java version: 1.8.0_232, vendor: AdoptOpenJDK, runtime: C:\Program Files\AdoptOpenJDK\jdk-8.0.232.09-hotspot\jre</code><br/>
  <code>Default locale: en_US, platform encoding: Cp1250</code><br/>
  <code>OS name: "windows 10", version: "10.0", arch: "amd64", family: "windows"</code></li></ul>
  
## Creating your first Maven Project
If you have just installed Maven, it may take a while on the first run. This is because Maven is downloading the most recent artifacts (plugin jars and other files) into your local repository. You may also need to execute the command a couple of times before it succeeds. This is because the remote server may time out before your downloads are complete. However, there are ways to fix that, you will just need to stackoverflow.

You will need somewhere for your project to reside, create a directory somewhere and start a shell in that directory.

Run the following command in shell:<br/><code>mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false</code><br/>
You will notice that the command created a directory with the same name given as the artifactId, cd into that directory and you will notice this project structure:<br/>
<pre>
my-app
|-- pom.xml
`-- src
    |-- main
    |   `-- java
    |       `-- com
    |           `-- mycompany
    |               `-- app
    |                   `-- App.java
    `-- test
        `-- java
            `-- com
                `-- mycompany
                    `-- app
                        `-- AppTest.java
</pre>
The <code>src/main/java</code> directory contains the project source code, the <code>src/test/java</code> directory contains the test source, and the <code>pom.xml</code> file is the project's Project Object Model, or POM.<br/>
We just executed the Maven goal `archetype:generate`, and passed in various parameters to that goal. The prefix `archetype` is the plugin that provides the goal. This `archetype:generate` goal created a simple project based upon a `maven-archetype-quickstart` archetype. <br/>
A plugin is a collection of goals with a general common purpose, and that will be all we need to know for now. Another thing that we need not know in detail about is the `POM.xml` file. This is the core of a project's configuration in Maven. It is a single configuration file that contains the majority of information required to build a project in just the way you want. The POM is huge and can be daunting in its complexity, but it is not necessary to understand all of the intricacies just yet to use it effectively.<br/>

## Build and Run

Run `mvn package` to build the packages. You may test the newly compiled and packaged JAR with the following command:<br/>
<pre>java -cp target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App</pre>
Which will print the following:
<pre>Hello World!</pre>

**Note: The build and run will vary for various archetypes, this one is for demo purposes only**

## Maven Tools

When you get even more familiar with Maven, you might begin to use some or all of these tools gradually, here's a list and what they do:
| Tool | Use |
|------|--------|
| validate|  validate the project is correct and all necessary information is available |
| compile|  compile the source code of the project |
| test|  test the compiled source code using a suitable unit testing framework. These tests should not require the code be packaged or deployed |
| package|  take the compiled code and package it in its distributable format, such as a JAR. |
| integration-test|  process and deploy the package if necessary into an environment where integration tests can be run |
| verify|  run any checks to verify the package is valid and meets quality criteria |
| install|  install the package into the local repository, for use as a dependency in other projects locally |
| deploy|  done in an integration or release environment, copies the final package to the remote repository for sharing with other developers and projects.
| clean|  cleans up artifacts created by prior builds |
| site|  generates site documentation for this project |

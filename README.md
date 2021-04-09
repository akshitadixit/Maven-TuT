# Maven Tutorial
A tutorial to get started with Maven in Java

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
<details>
  <summary>How to begin?</summary>
  <h4>Install JDK</h4>
  Visit this <a href="https://www.oracle.com/technetwork/java/javase/downloads/index.html">link</a> to download JDK compatible for your machine. Then test if it has been successfully installed and setup.<br/>
  For windows, open CMD: <code>c:\> java -version</code><br/>
  For linux, open terminal: <code>$ java -version</code><br/>
  For mac, open terminal: <code>machine:~ user$ java -version</code><br/>
  Verify the output similar to:<br/>
  <code>java version "1.7.0_60"</code><br/>
  <code>Java(TM) SE Runtime Environment (build 1.7.0_60-b19)</code><br/>
  <code>Java HotSpot(TM) 64-Bit Server VM (build 24.60-b09, mixed mode)</code><br/>
</details>
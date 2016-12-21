# Expert Areas

Given below are some areas that have overlaps with internal projects.
Picking these will have the advantage that your work in the internal projects can increase your expertise in the 
chosen areas (i.e. your work in CS3282 can help you earn more credit in CS3281).

## Languages

Here are the main languages used in the three projects (`PL` : PowerPointLabs, `SE` : SE-EDU, `TM` : TEAMMATES). 

Language   | Projects
-----------|-----
Java       | `SE`, `TM`
HTML       | `TM`
CSS        | `TM`
JavaScript | `TM`
C#         | `PL`


## Tools, Tech Topics

The aspects, tools, topics given below can help you to pick an aspect and a topic to study.

### Code Quality

* Static analysis 
  * Checkstyle `TM` `SE`
  * Codacy `SE`
  * FindBugs `TM` `SE` 
  * PMD `TM` `SE`
  * ESLint `TM`
  * Stylelint `TM`

## Dev Ops

* Build 
  * Gradle `TM` `SE`
  * npm `TM`

* CI
  * AppVeyor `SE` `PL`
  * Travis `TM` `SE`

* Process 
  * Workflow `TM` `SE` `PL`
  * Dev community management `TM` `SE` `PL`
  * Release management `TM` `SE` `PL`


### Desktop

* GUI
  * JavaFx, ControlsFx `SE`

* Installers `SE` `PL`

* Portability `SE` (ensuring the apps can run an all major OS'es)

### Documentation

Generating and maintaining user/developer docs require good writing skills as well and various tools.

* UML `TM` `SE` `PL`
* Document generation `TM` `SE` `PL` 
  * Jekyll `PL`

### Fault Tolerance

This is especially important to `TM` because Web apps are vulnerable to all sorts of intermittent faults. 
For example, one problem it faces is called 'eventual consistency' where new data requires some time to 
propagate through all nodes of the distributed database during which time the app has to deal with data
in an inconsistent state.

* Logging `TM` `SE` `PL`
* Error reporting `TM` `SE` `PL`
* Backup and restore `TM`

### Performance and scalability

This affects all three projects:
* `PL` : Users don't like their PowerPoint to slow down due to our plugin
* `SE` : We want the app to be very fast and to be able to handle lot of data (especially when connected to 
  third party backends such as Google calendar) 
* `TM` : 1. It has to deal with spikes in load. 2. Every CPU cycle or byte of data transfer costs us money.

Sub areas: 
* Multi-threading `TM` `SE`  
* Profiling `TM` `SE` `PL` : To find performance bottlenecks
* Scalability testing `TM` `SE`

### Security

* Vulnerabilities `TM`: SQL injection, cross site scripting
* Access control `TM`

### Testing

* Code coverage 
  * Blanket.js `TM`
  * EclEmma `TM` `SE`
  * JaCoCo `TM`
  * Coveralls `TM` `SE`

* Testing frameworks
  * JUnit `SE`
  * TestNG `TM`
  * QUnit `TM`

* UI testing
  * Selenium `TM`
  * TestFx `SE`
  
* Mocking
  * Mockito, PowerMock `SE`

### UIX

* Usability `TM` `SE` `PL`
* Accessibility `TM` : Some students who access `TM` may have accessibility needs
* Responsiveness `TM` : The app can be accessed using a variety of devices

### Web (Frontend)

* Front End frameworks: 
  * Bootstrap `TM`
  * JQuery `TM`

* Dynamic page generation
  * JSP `TM`
  * JSTL `TM`

### Web (Backend)

* Google App Engine `TM`
* Servlets `TM`
* Persistence
  * JDO, JPA, GAE DataStore `TM` : 
  * SQLite `SE` : We might use SQLite in higher level address books

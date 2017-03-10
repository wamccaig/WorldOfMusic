# WorldOfMusic
A music repository Application that parses XML files containing information on music.

- To run the executable .jar file, use the following command:

java -jar "WorldOfMusic-1.0-SNAPSHOT-jar-with-dependencies" -c worldofmusic.xml -o output.xml
 
 - "-c" is the input filename*
 - "-o" is the output filename

Notes: 
- A .zip and pom.xml(for maven framework) file have been provided for easy browsing of the source files and integration to an IDE.
- The worldofmusic.xml must be placed in the directory with WorldOfMusic.class according to the application's classpath settings.
- Future iterations could pass in the filter constrains (releaseDate and trackListing >10) as objects.

Time Tracking:

This application took somewhere around 20 hours to complete. Around 4 in requirements gathering and design, 10 in development, and the remining in configuration of deliverables, testing, and revisions.

Upcoming Features:

For a new Xml data in a different structure, we will need a few changes. I chose to implement JAXB library in my application in order to handle the XML parsing. This library is open source, simple to use, and is faster than DOM parsing. The new implementation will at least need a different class or a rework of Records.java to handle the model of the target object because I used annotations/JAXB to link it to the xml structure. If there is a web service that hosts the new XML structure and possibly schema(that would be nice) of the data, we can handle that pretty simply by switching out the model object classes, maybe the XmlReader class and leaving most of the rest of the application as is. The use of interfaces and the Google Guice dependency injection framework I chose to implement go a long way in providing maintainability through future iterations of the application.

For the second feature of redoing the filter constraints, we must then change the FilterView.class to meet the new requirements. This could be as simple as change the findAllTargetObjects method, which I would like to rework anyway. This class could be redone with the filtering constraints (at least 2 compact discs) being passed in as objects to evaluate. This new feature would also possible entail reworking the Release object in order to write the new information to the output.xml file correctly, as again, I use annotations and the JAXB library.


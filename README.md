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

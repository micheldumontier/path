# path
Create a summary of the structure and content of an xml file.

can be run using saxon xslt provided by atomgraph

    docker run -it --rm -v c:/code/xml-path-summary:/xml atomgraph/saxon  -s:/xml/in.xml -xsl:/xml/stylesheet.xsl  -o:/xml/out.xml
    
 run out of heap space? pass in the args
 
    -e JAVA_OPTS='-Xmx4000m'
    
 just make sure your java engine is configured to support that much
 
 alternatively, get the saxon jar from http://saxon.sourceforge.net/
 
     java -jar -Xmx10000m /software/saxon/saxon-he-10.0.jar -s:in.xml -xsl:stylesheet.xsl -o:out.xml
 
 you should also be able to process a folder of xml files

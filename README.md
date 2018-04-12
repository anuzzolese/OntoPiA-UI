# OntoPiA-UI
This projects provides the following facilities for enhancing user experience with the ontologies and the controlled vocabularies of OntoPiA:
 - Virtuoso as SPARQL enpoint;
 - LODE for visualising ontologies as HTML;
 - LodView for browsing ontology entities as well as controlloed vocabularies entities.

### Build and run
The project relies on Docker.
To build the containers type the following command in the terminal having the root of the project as base folder:
```
$> docker-compose build
```
To run the containers type the following command in the terminal having the root of the project as base folder:
```
$> docker-compose up
```

### Usage
Once the containers are up and assuming that `localhost` is the reference host, users can access:
 - the SPARQL endpoint at http://localhost:8890/sparql;
 - LODE at http://localhost:9090/lode;
 - LODE at http://localhost:8080/lodview.

### Examples
The following is an example of SPARQL SELECT query that returns all the classes defined in the ontology network of OntoPiA.
```
PREFIX owl: <http://www.w3.org/2002/07/owl#>
SELECT DISTINCT ?class 
WHERE {
  ?class a owl:Class
}
```

The resource http://localhost:8080/lodview/onto/CPV/Person can be used to visualise the HTML representation of the class Person for the CPV (core person) ontology.

The resource http://localhost:9090/lode/https://w3id.org/italia/onto/CPV can be used to visualise the CPV (core person) ontology as HTML.

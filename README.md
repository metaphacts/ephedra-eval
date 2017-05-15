# Ephedra validation queries
Evaluation queries to validate the Ephedra federation engine

This project stores the queries which we used to validate the Ephedra hybrid query federation architecture.
The query set contains 4 queries from the cultural heritage domain and 3 queries from the pharmaceutics domain.

## I. Cultural heritage domain.

The setup involves the following 4 federation members:
1. Wikidata RDF store: serves as the default repository.
2. British Museum collection: accessed as a SPARQL endpoint <http://public.researchspace.org/sparql>
3. Wikidata text search API: an entity lookup REST API hosted by Wikidata (https://www.wikidata.org/w/api.php). Accessible as an Ephedra extension service, referenced with the URI <http://www.metaphacts.com/ontologies/platform/repository/federation#wikidata-text>
4. word2vec vector space model API: returns a list of Wikidata entities similar to a given entity or a set of given entities.
Accessible both as Ephedra extension service and aggregation service under the URI <http://www.metaphacts.com/ontologies/platform/repository/federation#word2vec>

Queries are denoted as Q1_CH...Q4_CH


## II. Pharmaceutics domain.
The setup includes 4 federation members:
1. Wikidata RDF store: serves as the default repository.
2. Instance of the Nextprot RDF store: accessed as a SPARQL endpoint
3. Wikidata text search API: accessed as Ephedra extension service, referenced under the URI <http://www.metaphacts.com/ontologies/platform/repository/federation#wikidata-text>.
4. BLAST sequence similarity API: returns a list of genome sequences similar to the given one. Wraps around the NCBI-BLAST Common URL API (https://ncbi.github.io/blast-cloud/dev/api.html). Accessible as an Ephedra extension service, referenced with the URI <http://www.metaphacts.com/ontologies/platform/repository/federation#BLAST>.

Queries are denoted as Q1_PH...Q3_PH

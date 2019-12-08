
_**This project is under active development as part of semantic data research with
[UW BIME](http://bime.uw.edu/).**_

# BioModels-ETL

Biomodels-ETL is a customizable ETL pipeline and DAG engine for visualizing SBML 
[BioModels](https://www.ebi.ac.uk/biomodels/) (mathematical models for biological systems). 
It generates NetworkX DAGs that can be exported to multiple file formats 
(e.g. JSON, YAML, GraphML, etc.) and visualized as semantic data networks.

Example network (visualized with Cytoscape):


![](BioModelsETL/docs/images/derived_model_graph.png)
<sub><sup>
Network showing parent-child relationships between BioModels from various providers.
PubMed models are displayed in red, EBI models in green.
</sup></sub>

The pipeline:
- Extracts SBML data from SBML BioModels
- Parses data with user-implemented parsers/classifiers to retrieve semantic data as 
ordered triples (similar to RDF)
- Processes and loads ordered triples into a NetworkX DAG

The DAG can then be exported and drawn, and is compatible with most
network visualization tools (e.g. Cytoscape).

The following flowchart illustrates this process:

![](BioModelsETL/docs/images/etl-flowchart.png)

Completed example networks are available [here](BioModelsETL/graphs).

## Dependencies

[NetworkX](https://networkx.github.io/), [BeautifulSoup](https://pypi.org/project/beautifulsoup4/), 
[dateutil](https://github.com/dateutil/dateutil), [lxml](https://github.com/lxml/lxml),
[libSBML](https://github.com/opencor/libsbml)

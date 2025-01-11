[OQuaRE](../README.md)

# GitHub Actions: Ontology Quality Evaluation

This module leverages the **OQuaRE framework** to automatically evaluate and generate quality metrics for ontology files. For ontologies with multiple versions, the metrics reflect changes over time, representing the evolution of the ontology. It produces visual reports that highlight the quality of each ontology, providing clear insights into their strengths and weaknesses, as shown in Figures 1, 2, and 3. Figure 1 and Figure 2 represent quality characteristics and metrics for a specific ontology, while Figure 3 specifically illustrates the values for the subcharacteristic functional adequacy across four versions of the ontology, represented on the X-axis. The module extends these capabilities to ontology **repositories hosted on GitHub**, enabling the evaluation of ontologies through a standardized system seamlessly integrated into GitHub workflows. This approach offers ontology developers and researchers an efficient way to assess and improve ontology quality. The GitHub Actions repository can be found at:
https://github.com/tecnomod-um/oquare-metrics



<img src="images_software_resources/obi_characteristics_example.png" width="300">
<img src="images_software_resources/obi_metrics example.png" width="300">

<img src="images_software_resources/obi_functionalAdequacy_subcharacteristics_evolutionExample.png" width="400">

## OQuaRE Metrics for an Ontology Corpus

The [Ontology Metrics Evaluation](https://semantics.inf.um.es/ontology-metrics/) page contains detailed information about the ontology quality assessment process, including the preparation and submission of ontology corpora in supported formats. The evaluation process 
involves two primary steps:

1. **Metrics Calculation**: Explains the process of extracting metric values from the ontology corpus and calculating 19 quality metrics using the OQuaRE framework.
 
2. **Metrics Analysis**: Interpreting and analyzing the calculated metrics for stability, correlations, and classification quality.

The page provides visualizations  The page also includes sample corpora and result files, as well as guidance on interpreting the outcomes of the evaluation, offering a complete overview of the methodology and its applications.


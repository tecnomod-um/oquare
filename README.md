# OQuaRE Repository

Ontology Quality Requirement and Evaluation Framework (OQuaRE). This repository contains the OQuaRE framework, including definitions of ontology quality characteristics, subcharacteristics, and metrics. 

# OQuaRE Framework

## Table of Contents  
1. [Ontology Quality Evaluation Framework (OQuaRE)](README.md)  
2. [OQuaRE Quality Model Division](quality_model.md)  
3. [OQuaRE Quality Metrics Division](quality_metrics.md)
4. [OQuaRE Quality Evaluation Division](quality_evaluation.md)    

---

## Ontology Quality Evaluation Framework (OQuaRE)
  
OQuaRE is a systematic framework designed to evaluate the quality of ontologies by adapting the **ISO/IEC 25000:2005 SQuaRE** standard, for Software Product Quality Requirements and Evaluation (SQuaRE). :contentReference[oaicite:0]{index=0} [2]

The **Quality Framework** is divided into five main divisions which can be identified in the figure. The **OQuaRE Requirements Division** focuses on assisting in specifying quality requirements. The **OQuaRE Quality Model Division** addresses the internal and external quality of the software product by defining key characteristics and sub-characteristics. The **OQuaRE Quality Metrics Division** establishes base and derived measures to evaluate quality. The **OQuaRE Quality Evaluation Division** defines the processes required for quality evaluation. Lastly, the **OQuaRE Quality Management Division** focuses on overseeing and managing quality-related activities to ensure continuous improvement and compliance with established standards.

<div align="center">
  <img src="oquare.png" alt="OQuaRE" width="600">
</div>

## OQuaRE Quality Model Division

Is composed of multiple **characteristics** and **subcharacteristics** relevant to ontologies, including **structural features**, **functional adequacy**, **compatibility**, **transferability**, **maintainability**, and **operability** [1][2][3]. :contentReference[oaicite:1]{index=1} OQuaRE introduces a **structural characteristic** to account for ontology-specific aspects, not covered by SQuaRE, such as **formalization**, **redundancy**, **consistency**, and **tangledness** [4]. The Quality Model section provide more detail 
- [Quality Model](quality_model.md)

## QOuaRE Quality Metric Division

 Is composed of base and derived measurements. Base measurements correspond to metrics that can be measured directly on the ontology, such as the number of classes, the number of relations, etc., whereas derived ones combine some base measurements.
 
 The Quality Model section provide more detail 
- [Quality Metrics](quality_metrics.md)

## OQuaRE Quality Evaluation Division 

OQuaRE serves as a critical tool for researchers and developers by systematically identifying the **strengths** and **weaknesses** of ontologies. This enables improvements in their design, fosters reusability, and enhances interoperability within semantic web applications and domain-specific knowledge systems [1][5]. :contentReference[oaicite:2]{index=2}

Evaluating an ontology requires to measure the **quality characteristics** and  **quality subcharacteristic** in OQuaRE is evaluated using a series of **quality metrics**, which provide both qualitative and quantitative insights into the ontology’s design, implementation, and usability. 

The values of the metrics are transformed into **quality scores** by applying **scaling functions**. The current version of OQuaRE uses quality scores in the range **[1, 5]**:
- **1** – “Not Acceptable”  
- **2** – “Not Acceptable - Improvement Required”  
- **3** – “Minimally Acceptable”  
- **4** – “Acceptable”  
- **5** – “Exceeds Requirements”  
---

The following sections explain the **Quality Model** and **Quality Metrics** and **scalign functions** in detail, providing a comprehensive understanding of how these elements are applied in the OQuaRE framework.
1. [Quality Model](quality_model.md)
2. [Quality Metrics](quality_metrics.md)
3. [Quality Evaluation](quality_evaluation.md)
---

## References

[1] Duque-Ramos, A., Fernández-Breis, J.T., Stevens, R., & Aussenac-Gilles, N. (2011). *OQuaRE: A SQuaRE-based approach for evaluating the quality of ontologies*. Journal of Research and Practice in Information Technology, 43, 159-173.  

[2] ISO/IEC 25000:2005. *Software engineering — Software product Quality Requirements and Evaluation (SQuaRE)*. Geneva, Switzerland: International Organization for Standardization.

[3] Stevens, R., & Lord, P. (2009). *Application of ontologies in bioinformatics*. In Handbook on Ontologies (pp. 557–578). Springer Berlin Heidelberg.

[4] Fernández-Breis, J., Egaña, M., & Stevens, R. (2009). *A quality evaluation framework for bio-ontologies*. ICBO International Conference on Biomedical Ontology.

[5] Gangemi, A., Catenacci, C., Ciaramita, M., & Lehmann, J. (2006). *Modelling ontology evaluation and validation*. Semantic Web: Research and Applications, Proceedings, 4011: 140–154.


## Publications

1. **Astrid Duque-Ramos**, Quesada-Martínez, M., Iniesta-Moreno, M., Fernández-Breis, J.T., Stevens, R.  
   *Supporting the analysis of ontology evolution processes through the combination of static and dynamic scaling functions in OQuaRE.*  
   *Journal of Biomedical Semantics*, Volume **7**, Nº 63, 2016.  
   DOI: [10.1186/s13326-016-0091-z](https://doi.org/10.1186/s13326-016-0091-z)

2. **Astrid Duque-Ramos**, Martin Boeker, Ludger Jansen, Stefan Schulz, Miguela Iniesta-Moreno, Jesualdo Tomás Fernández-Breis.  
   *Evaluating the Good Ontology Design guideline (GoodOD) with the Ontology Quality Requirement and Evaluation method and metrics (OQuaRE).*  
   *PLOS One*, Volume **9**, Nº 8, 2014, Pages E104463-1 - E104463-14.  
   DOI: [10.1371/journal.pone.0104463](https://doi.org/10.1371/journal.pone.0104463)

3. **Astrid Duque-Ramos**, Jesualdo Tomás Fernández-Breis, Miguela Iniesta, Michel Dumontier, Mikel Egaña Aranguren, Stefan Schulz, Nathalie Aussenac-Gilles, Robert Stevens.  
   *Evaluation of the OQuaRE framework for ontology quality.*  
   *Expert Systems with Applications*, Volume **40**, Issue 7, 1 June 2013, Pages 2696–2703.  
   DOI: [10.1016/j.eswa.2012.11.004](https://doi.org/10.1016/j.eswa.2012.11.004)

4. **A. Duque-Ramos**, J. T. Fernández-Breis, R. Stevens, N. Aussenac-Gilles.  
   *OQuaRE: a SQuaRE-based approach for evaluating the quality of ontologies.*  
   *Journal of Research and Practice in Information Technology*, Volume **43**, 2011, Pages 159–173.  
   DOI: [10.1.1.363.7967](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.363.7967)


[OQuaRE](../README.md)


### Ontology Quality Evaluation Framework (OQuaRE)

OQuaRE is a systematic framework designed to evaluate the quality of ontologies by adapting the **ISO/IEC 25000:2005 SQuaRE** standard, for Software Product Quality Requirements and Evaluation (SQuaRE). [2]

<div align="center">
  <img src="images_oquare_docs/oquare.png" alt="OQuaRE" width="600">
</div>

The defined

## OQuaRE Quality Model Division

Is composed of multiple **characteristics** and **subcharacteristics** relevant to ontologies, including **structural features**, **functional adequacy**, **compatibility**, **transferability**, **maintainability**, and **operability** [1][2][3]. OQuaRE introduces a **structural characteristic** to account for ontology-specific aspects, not covered by SQuaRE, such as **formalization**, **redundancy**, **consistency**, and **tangledness** [4]. The Quality Model section provide more detail 
- [Quality Model](oquare_docs/quality_model.md)

## QOuaRE Quality Metric Division

 Is composed of base and derived measurements. Base measurements correspond to metrics that can be measured directly on the ontology, such as the number of classes, the number of relations, etc., whereas derived ones combine some base measurements.
 
 The Quality Model section provide more detail 
- [Quality Metrics](oquare_docs/quality_metrics.md)

## OQuaRE Quality Evaluation Division 

OQuaRE serves as a critical tool for researchers and developers by systematically identifying the **strengths** and **weaknesses** of ontologies. This enables improvements in their design, fosters reusability, and enhances interoperability within semantic web applications and domain-specific knowledge systems [1][5]. 

Evaluating an ontology requires to measure the **quality characteristics** and  **quality subcharacteristic** in OQuaRE is evaluated using a series of **quality metrics**, which provide both qualitative and quantitative insights into the ontology’s design, implementation, and usability. 

The values of the metrics are transformed into **quality scores** by applying **scaling functions**. The current version of OQuaRE uses quality scores in the range **[1, 5]**:
- **1** – “Not Acceptable”  
- **2** – “Not Acceptable - Improvement Required”  
- **3** – “Minimally Acceptable”  
- **4** – “Acceptable”  
- **5** – “Exceeds Requirements”  
---

## References

[1] Duque-Ramos, A., Fernández-Breis, J.T., Stevens, R., & Aussenac-Gilles, N. (2011). *OQuaRE: A SQuaRE-based approach for evaluating the quality of ontologies*. Journal of Research and Practice in Information Technology, 43, 159-173.  

[2] ISO/IEC 25000:2005. *Software engineering — Software product Quality Requirements and Evaluation (SQuaRE)*. Geneva, Switzerland: International Organization for Standardization.

[3] Stevens, R., & Lord, P. (2009). *Application of ontologies in bioinformatics*. In Handbook on Ontologies (pp. 557–578). Springer Berlin Heidelberg.

[4] Fernández-Breis, J., Egaña, M., & Stevens, R. (2009). *A quality evaluation framework for bio-ontologies*. ICBO International Conference on Biomedical Ontology.

[5] Gangemi, A., Catenacci, C., Ciaramita, M., & Lehmann, J. (2006). *Modelling ontology evaluation and validation*. Semantic Web: Research and Applications, Proceedings, 4011: 140–154.

# OQuaRE Repository

Ontology Quality Requirement and Evaluation Framework (OQuaRE). This repository contains the OQuaRE framework, including definitions of ontology quality characteristics, subcharacteristics, and metrics. Find links to related papers, applications for OQuaRE, and access to QASAR, the platform for evaluating Semantic Resources, through the usage of OQuaRE and three more ontology quality-related frameworks, namely, OntoEnrich [2], HURON [3] and Evaluome [4].

# OQuaRE Framework

## Table of Contents  
1. [The Ontology Quality Evaluation Framework (OQuaRE)](#the-ontology-quality-evaluation-framework-oquare)  
2. [The Quality Model Division](#the-oquare-quality-model-division)  
3. [The Quality Metrics Division](#the-quality-metrics-division)
4. [The Quality Evaluation Division](#the-quality-evaluation-division)    
   - [Structural](#structural)  
   - [Functional Adequacy](#functional-adequacy)  
   - [Compatibility](#compatibility)  
   - [Transferability](#transferability)  
   - [Operability](#operability)  
   - [Maintainability](#maintainability)  

---

## The Ontology Quality Evaluation Framework (OQuaRE)
  
A systematic framework designed to evaluate the quality of ontologies by adapting the **ISO/IEC 25000:2005 SQuaRE** standard, for Software Product Quality Requirements and Evaluation (SQuaRE). :contentReference[oaicite:0]{index=0} [2]

The **Quality Framework** is divided into five main divisions which can be identified in the figure. The **Quality Requirements Division** focuses on assisting in specifying quality requirements. The **Quality Model Division** addresses the internal and external quality of the software product by defining key characteristics and sub-characteristics. The **Quality Metrics Division** establishes base and derived measures to evaluate quality. The **Quality Evaluation Division** defines the processes required for quality evaluation. Lastly, the **Quality Management Division** focuses on overseeing and managing quality-related activities to ensure continuous improvement and compliance with established standards.

![alt text](oquare.png)

## The Quality Model Division

Is composed of multiple **characteristics** and **subcharacteristics** relevant to ontologies, including **structural features**, **functional adequacy**, **compatibility**, **transferability**, **maintainability**, and **operability** [1][2][3]. :contentReference[oaicite:1]{index=1} OQuaRE introduces a **structural characteristic** to account for ontology-specific aspects, not covered by SQuaRE, such as **formalization**, **redundancy**, **consistency**, and **tangledness** [4]. The Quality Model section provide more detail 
- [Quality Model](quality_model.md)

## The Quality Metric Division

 The Quality Model section provide more detail 
- [Quality Metrics](quality_metrics.md)

## The Quality Evaluation Division 

OQuaRE serves as a critical tool for researchers and developers by systematically identifying the **strengths** and **weaknesses** of ontologies. This enables improvements in their design, fosters reusability, and enhances interoperability within semantic web applications and domain-specific knowledge systems [1][5]. :contentReference[oaicite:2]{index=2}

Each **quality subcharacteristic** in OQuaRE is evaluated using a series of **metrics**, which provide both qualitative and quantitative insights into the ontology’s design, implementation, and usability. The Quality Model section provide more detail
 [The Quality Evaluation Division](quality_evaluation.md) provide more detail 

In OQuaRE, the values of the metrics are transformed into **quality scores** by applying **scaling functions**. The current version of OQuaRE uses quality scores in the range **[1, 5]**:
- **1** – “Not Acceptable”  
- **2** – “Not Acceptable - Improvement Required”  
- **3** – “Minimally Acceptable”  
- **4** – “Acceptable”  
- **5** – “Exceeds Requirements”  

OQuaRE offers two types of **scaling functions** [2], which differ in how the metric values are transformed into quality scores, providing complementary information:

1. **Static Scaling Function**:  
   - Based on recommendations and best practices from the Software Engineering and Ontology Engineering communities.  
   - Uses a predefined transformation function, ensuring that the value of a given metric is always transformed into the same quality score.

2. **Dynamic Scaling Function**:  
   - Based on the observed values of the quality metrics from a **corpus** defined by a set of ontologies.  
   - The transformation function depends on the corpus used, so the value of a metric is transformed into quality scores that vary depending on the corpus of ontologies.
---

The following sections explain the **Quality Model** and **Quality Metrics** in detail, providing a comprehensive understanding of how these elements are applied in the OQuaRE framework.
1. [Quality Model](quality_model.md)
2. [Quality Metrics](quality_metrics.md)
3. [Scaling Functions](scaling_functions.md)

---

## References

[1] Duque-Ramos, A., Fernández-Breis, J.T., Stevens, R., & Aussenac-Gilles, N. (2011). *OQuaRE: A SQuaRE-based approach for evaluating the quality of ontologies*. Journal of Research and Practice in Information Technology, 43, 159-173.  

[2] ISO/IEC 25000:2005. *Software engineering — Software product Quality Requirements and Evaluation (SQuaRE)*. Geneva, Switzerland: International Organization for Standardization.

[3] Stevens, R., & Lord, P. (2009). *Application of ontologies in bioinformatics*. In Handbook on Ontologies (pp. 557–578). Springer Berlin Heidelberg.

[4] Fernández-Breis, J., Egaña, M., & Stevens, R. (2009). *A quality evaluation framework for bio-ontologies*. ICBO International Conference on Biomedical Ontology.

[5] Gangemi, A., Catenacci, C., Ciaramita, M., & Lehmann, J. (2006). *Modelling ontology evaluation and validation*. Semantic Web: Research and Applications, Proceedings, 4011: 140–154.

---

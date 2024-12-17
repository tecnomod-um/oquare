# OQuaRE
Ontology Quality Requirement and Evaluation Framework (OQuaRE)  This repository contains the OQuaRE framework, including definitions of ontology quality characteristics, subcharacteristics, and metrics. Find links to related papers, applications for OQuaRE, and access to QASAR, an app for evaluating ontology quality based on OQuaRE standard
# OQuaRE Wiki

## Table of Contents  
1. [Welcome to OQuaRE Wiki](#welcome-to-oquare-wiki)  
2. [The Ontology Quality Evaluation Framework (OQuaRE)](#the-ontology-quality-evaluation-framework-oquare)  
3. [The OQuaRE Quality Model](#the-oquare-quality-model)  
4. [The Quality Metrics of OQuaRE](#the-quality-metrics-of-oquare)  
   - [Structural](#structural)  
   - [Functional Adequacy](#functional-adequacy)  
   - [Compatibility](#compatibility)  
   - [Transferability](#transferability)  
   - [Operability](#operability)  
   - [Maintainability](#maintainability)    

---

## Welcome to OQuaRE Wiki

This Wiki is for discussing the characteristics and subcharacteristics of the ontology evaluation method called **OQuaRE** [1]. OQuaRE is a framework for evaluating ontology quality based on the standard **ISO/IEC 25000:2005** for Software Product Quality Requirements and Evaluation (SQuaRE) [2].  
Recent efforts have investigated how such software quality standards can be adapted to measure ontology quality, including approaches based on ISO 9126 [3].

---

## The Ontology Quality Evaluation Framework (OQuaRE)

SQuaRE covers two main processes:
1. Software quality requirements specifications.  
2. Software quality evaluation.

SQuaRE defines components like quality models, metrics, requirements, and evaluations. OQuaRE adapts this for ontologies by defining:
- **Evaluation support**  
- **Evaluation process**  
- **Metrics**  

The current version focuses on the **quality model** and **quality metrics** as essential elements for evaluating ontology quality.

---

## The OQuaRE Quality Model

The OQuaRE model adapts the following SQuaRE characteristics to ontologies:
- Functional adequacy  
- Reliability  
- Operability  
- Maintainability  
- Compatibility  
- Transferability  

Additionally, **structural features** are introduced to evaluate aspects not covered by SQuaRE, such as consistency, formalization, redundancy, or tangledness.

---

## The Quality Metrics of OQuaRE

### Structural

| Subcharacteristic      | Definition                                   | Description                                                                                                                                                     | Metrics    |
|------------------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **Formalisation**      | Capability to support reasoning             | Ontology expressed in a formal language (e.g., OWL, RDF/XML).                                                                                                  | -          |
| **Formal relations**   | Representation of non-taxonomic relations   | Types of formal relations beyond part-of relations.                                                                                                            | RROnto     |
| **Redundancy**         | Capability to be informative                | Avoid inferred duplication of classes, properties, or instances.                                                                                               | ANOnto     |
| **Structural accuracy**| Correctness of ontology terms               | Correct taxonomic links, upper-level disjoint categories, appropriate domain/range restrictions.                                                               | -          |
| **Consistency**        | Degree of consistency                       | Logical and naming conventions, structural consistency.                                                                                                        | -          |
| **Tangledness**        | Multiple inheritance issues                 | Distribution of multiple parent categories.                                                                                                                   | TMOnto     |
| **Cohesion**           | Relatedness of ontology classes             | Strong connections between classes.                                                                                                                           | LCOMOnto   |
| **Domain coverage**    | Coverage of a specific domain               | Evaluated by domain experts.                                                                                                                                  | -          |

---

### Functional Adequacy

| Subcharacteristic            | Definition                                  | Description                                                                                          | Metrics                |
|------------------------------|--------------------------------------------|------------------------------------------------------------------------------------------------------|------------------------|
| **Reference ontology**       | Degree of usability as reference           | Better machine exploitation through explicit structures.                                             | -                      |
| **Controlled vocabulary**    | Avoid heterogeneity of terms               | Unified terms with non-redundant definitions.                                                       | ANOnto                 |
| **Schema/value reconciliation**| Common data model for integration        | Facilitates ontology reconciliation and integration.                                                | RROnto, AROnto         |
| **Consistent search/query**  | Improved querying and search methods       | Better data evaluation and retrieval.                                                               | INROnto, Formal degree |
| **Knowledge acquisition**    | Representation of acquired knowledge       | Storage and encoding of domain-specific knowledge.                                                  | ANOnto, NOMOnto        |

---

### Compatibility

| Subcharacteristic      | Definition                                  | Description                                                                 | Metrics                |
|------------------------|---------------------------------------------|-----------------------------------------------------------------------------|------------------------|
| **Replaceability**     | Replace ontology in similar environments   | Ontology can replace another in the same environment.                       | WMCOnto, NOMOnto       |
| **Interoperability**   | Combine ontology with other ontologies      | Degree to which ontologies integrate cooperatively.                         | -                      |

---

### Transferability

| Subcharacteristic      | Definition                                  | Description                                                                 | Metrics                |
|------------------------|---------------------------------------------|-----------------------------------------------------------------------------|------------------------|
| **Portability**        | Transfer ontology between environments      | Translation of ontology between formal languages.                          | -                      |
| **Adaptability**       | Adapt ontology for new environments         | Ontology adaptability without significant changes.                         | WMCOnto, DITOnto       |

---

### Operability

| Subcharacteristic      | Definition                                  | Description                                                                 | Metrics                |
|------------------------|---------------------------------------------|-----------------------------------------------------------------------------|------------------------|
| **Learnability**       | Ease of learning ontology                  | Quality of manuals, guides, and documentation.                             | WMCOnto, NOMOnto       |
| **Helpfulness**        | Assistance for users                       | Availability of effective error messages and help resources.               | -                      |

---

### Maintainability

| Subcharacteristic      | Definition                                  | Description                                                                 | Metrics                |
|------------------------|---------------------------------------------|-----------------------------------------------------------------------------|------------------------|
| **Modularity**         | Discrete components for minimal changes     | Changes in components do not impact others.                                | WMCOnto, CBOnto        |
| **Reusability**        | Ontology reuse in other contexts            | Reuse ontology parts or assets across domains.                             | CBOnto, NOMOnto        |

---

## References

1. Duque-Ramos, A., et al. *OQuaRE: A SQuaRE-Based Approach for Evaluating Ontology Quality*. JRPIT 43 (2011).  
2. ISO/IEC 25000:2005. *Software Product Quality Requirements and Evaluation*. Geneva, Switzerland.  
3. Fernández-Breis, J., et al. (2009). *A Quality Evaluation Framework for Bio-Ontologies*. ICBO Proceedings.  
4. Gangemi, A., et al. (2006). *Modelling Ontology Evaluation*. Semantic Web Research and Applications.  
5. Stevens, R., Lord, P. (2009). *Application of Ontologies in Bioinformatics*. Handbook on Ontologies.  

---



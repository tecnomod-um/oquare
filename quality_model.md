## The OQuaRE Quality Model

The current OQuaRE version includes 8 characteristics and 29 subcharacteristics, the characateriscts are: 
- Functional adequacy  
- Reliability  
- Operability  
- Maintainability  
- Compatibility  
- Transferability  
- Performance efficiency  

Additionally, **structural features** are introduced to evaluate aspects not covered by SQuaRE, such as consistency, formalization, redundancy, or tangledness.

---

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
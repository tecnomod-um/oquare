# Quality Metrics in OQuaRE

OQuaRE permits the definition of the quality model in terms of **quality characteristics**. This standard suggests a series of quality characteristics to measure quality. Each quality characteristic has associated **subcharacteristics**, and each subcharacteristic has a set of **primitive measures** (metrics).  

### **Metric Notation**  
### Metric Notation  
- **C<sub>1</sub>, C<sub>2</sub>, …, C<sub>n</sub>**: Classes of the ontology.  
- **RC<sub>1</sub>, RC<sub>2</sub>, …, RC<sub>k</sub>**: Relationships of class C<sub>i</sub>.  
- **PC<sub>1</sub>, PC<sub>2</sub>, …, PC<sub>z</sub>**: Properties of class C<sub>i</sub>.  
- **IC<sub>1</sub>, IC<sub>2</sub>, …, IC<sub>m</sub>**: Individuals of class C<sub>i</sub>.  
- **SupC<sub>1</sub>, SupC<sub>2</sub>, …, SupC<sub>m</sub>**: Direct superclasses of a given class C.  
- **Thing**: Root class of the ontology.  
     
Some of the metrics such as **Coupling Between Objects (CBO)**, **Depth of Inheritance Tree (DIT)**, **Number Of Children (NOC)**, **Response For a Class (RFC)**, and **Weighted Method Count (WMC)** were selected from **Software Engineering** and particularly **Object-Oriented Programming (OOP)** [1][2]. These were adapted to ontologies due to shared concepts such as **classes, individuals**, and **properties**. Additionally, metrics developed by the **ontology engineering community** were reused, especially those addressing **structural properties** [3][4][5].

---

## Metrics and Formulas  

### **LCOMOnto - Lack of Cohesion in Methods**  
Measures the semantic and conceptual relatedness of classes.  
\[
\text{LCOMOnto} = \frac{\sum \text{Length(path(|C(leaf)i|))}}{m}
\]  
- **Where**: Length(path|C(leaf)i|) is the length of the path from the leaf class *i* to **Thing**, and *m* is the total number of paths.  

| Metric/Score | 1   | 2       | 3       | 4       | 5      |
|--------------|------|---------|---------|---------|--------|
| LCOMOnto     | >8   | (6-8]   | (4-6]   | (2-4]   | <=2    |

---

### **DITOnto - Depth of Subsumption Hierarchy**  
Length of the largest path from **Thing** to a leaf class.  
\[
\text{DITOnto} = \text{Max} \left( \sum D|C_i| \right)
\]  
- **Where**: D|C_i| is the length of the path from the *i*-th leaf class to **Thing**.

| Metric/Score | 1   | 2       | 3       | 4       | 5      |
|--------------|------|---------|---------|---------|--------|
| DITOnto      | >8   | (6-8]   | (4-6]   | (2-4]   | [1-2]  |

---

### **NACOnto - Number of Ancestor Classes**  
Mean number of ancestor classes per leaf class.  
\[
\text{NACOnto} = \frac{\sum |SupC(Leaf)_i|}{\sum |C(leaf)_i|}
\]  

| Metric/Score | 1   | 2       | 3       | 4       | 5      |
|--------------|------|---------|---------|---------|--------|
| NACOnto      | >8   | (6-8]   | (4-6]   | (2-4]   | [1-2]  |

---

### **NOCOnto - Number of Children Classes**  
Number of direct subclasses divided by the number of classes minus the number of leaf classes.  
\[
\text{NOCOnto} = \frac{\sum |RC_i|}{\left( \sum |C_i| - \sum |C(leaf)_i| \right)}
\]  

| Metric/Score | 1   | 2       | 3       | 4       | 5      |
|--------------|------|---------|---------|---------|--------|
| NOCOnto      | >8   | (6-8]   | (4-6]   | (2-4]   | [1-2]  |

---

### **CBOOnto - Coupling Between Objects**  
Number of related classes.  
\[
\text{CBOOnto} = \frac{\sum |SupC_i|}{\left( \sum |C_i| - |R_{\text{Thing}}| \right)}
\]  

| Metric/Score | 1    | 2        | 3        | 4        | 5       |
|--------------|-------|----------|----------|----------|---------|
| CBOOnto      | >12   | (8-12]   | (6-8]    | (3-6]    | [1-3]   |

---

### **RFCOnto - Response for a Class**  
Number of properties directly accessible from a class, including data and object properties.  

\[
\text{RFCOnto} = \frac{\sum |PC<sub>i</sub>| + \sum |SupC<sub>i</sub>|}{\sum |C<sub>i</sub>|}
\]  

| Metric/Score | 1    | 2        | 3        | 4        | 5       |
|--------------|-------|----------|----------|----------|---------|
| RFCOnto      | >12   | (8-12]   | (6-8]    | (3-6]    | [1-3]   |

---

### **NOMOnto - Number of Properties**  
Mean number of properties (object and data) per class.  

\[
\text{NOMOnto} = \frac{\sum |PC<sub>i</sub>|}{\sum |C<sub>i</sub>|}
\]  

| Metric/Score | 1   | 2       | 3       | 4       | 5      |
|--------------|------|---------|---------|---------|--------|
| NOMOnto      | >8   | (6-8]   | (4-6]   | (2-4]   | <=2    |

---
### **PROnto - Properties Richness**  
Measures the ratio of object and data property usages to the total number of subclass relationships and properties.

PROnto = ∑|PCᵢ| / (∑|RCᵢ| + ∑|PCᵢ|)  

| Metric/Score | 1       | 2          | 3          | 4          | 5        |
|--------------|---------|------------|------------|------------|----------|
| PROnto       | [0-20]% | (20-40]%   | (40-60]%   | (60-80]%   | >80%     |

---

### **INROnto - Relationships per Class**  
Mean number of relationships (subclasses) per class.  

INROnto = ∑|RCᵢ| / ∑|Cᵢ|  

| Metric/Score | 1       | 2          | 3          | 4          | 5        |
|--------------|---------|------------|------------|------------|----------|
| INROnto      | [0-20]% | (20-40]%   | (40-60]%   | (60-80]%   | >80%     |

---

### **POnto - Ancestors per Class**  
Mean number of direct ancestors per class.

POnto = ∑|SupCᵢ| / ∑|Cᵢ|  

| Metric/Score | 1       | 2          | 3          | 4          | 5        |
|--------------|---------|------------|------------|------------|----------|
| POnto        | [0-20]% | (20-40]%   | (40-60]%   | (60-80]%   | >80%     |

---

### **CROnto - Class Richness**  
Mean number of individuals per class.

CROnto = ∑|ICᵢ| / ∑|Cᵢ|  

| Metric/Score | 1       | 2          | 3          | 4          | 5        |
|--------------|---------|------------|------------|------------|----------|
| CROnto       | [0-20]% | (20-40]%   | (40-60]%   | (60-80]%   | >80%     |

---

### **AROnto - Attribute Richness**  
Measures the number of restrictions (attributes) of the ontology per class.  

AROnto = ∑|AttCᵢ| / ∑|Cᵢ|  

| Metric/Score | 1       | 2          | 3          | 4          | 5        |
|--------------|---------|------------|------------|------------|----------|
| AROnto       | [0-20]% | (20-40]%   | (40-60]%   | (60-80]%   | >80%     |

---

### **ANOnto - Annotation Richness**  
Mean number of annotation properties per class.  

ANOnto = ∑|ACᵢ| / ∑|Cᵢ|  

| Metric/Score | 1       | 2          | 3          | 4          | 5        |
|--------------|---------|------------|------------|------------|----------|
| ANOnto       | [0-20]% | (20-40]%   | (40-60]%   | (60-80]%   | >80%     |

---

### **TMOnto - Tangledness**  
Measures the mean number of classes with more than one direct ancestor.  

TMOnto = ∑|C(DP)ᵢ| / (∑|Cᵢ| - 1)  

- **Where**:  
  - **C(DP)ᵢ**: Classes with more than one direct parent.  
  - **Cᵢ**: Total number of classes.  

| Metric/Score | 1     | 2        | 3        | 4        | 5        |
|--------------|-------|----------|----------|----------|----------|
| TMOnto       | >8    | (6-8]    | (4-6]    | (2-4]    | (1-2]    |

---

### **TMOnto2 - Tangledness2**  
Measures the mean number of direct ancestors for classes with more than one direct ancestor.  

TMOnto2 = ∑|Sup(CDP)ᵢ| / ∑|CDPᵢ|  

- **Where**:  
  - **Sup(CDP)ᵢ**: Superclasses of classes with more than one direct parent.  
  - **CDPᵢ**: Classes with more than one direct parent.  

| Metric/Score | 1     | 2        | 3        | 4        | 5        |
|--------------|-------|----------|----------|----------|----------|
| TMOnto2      | >8    | (6-8]    | (4-6]    | (2-4]    | (1-2]    |

---

### **WMCOnto - Weighted Method per Class**  
Measures the mean length of the path from **Thing** to a leaf class.  

WMCOnto = ∑ Length(path(|C(leaf)ᵢ|)) / ∑|C(leaf)ᵢ|  

- **Where**:  
  - **Length(path(|C(leaf)ᵢ|))**: Length of the path from the *i*-th leaf class to **Thing**.  
  - **C(leaf)ᵢ**: Leaf classes in the ontology.  

| Metric/Score | 1     | 2        | 3        | 4        | 5        |
|--------------|-------|----------|----------|----------|----------|
| WMCOnto      | >8    | (6-8]    | (4-6]    | (2-4]    | [1-2]    |

---

### **WMCOnto2 - Weighted Method per Class 2**  
Measures the mean number of paths from **Thing** to a leaf class per leaf class.  

WMCOnto2 = ∑ path(|C(leaf)ᵢ|) / ∑|C(leaf)ᵢ|  

- **Where**:  
  - **path(|C(leaf)ᵢ|)**: Number of paths from the *i*-th leaf class to **Thing**.  
  - **C(leaf)ᵢ**: Leaf classes in the ontology.  

| Metric/Score | 1     | 2        | 3        | 4        | 5        |
|--------------|-------|----------|----------|----------|----------|
| WMCOnto2     | >8    | (6-8]    | (4-6]    | (2-4]    | [1-2]    |

---

## References

[1] Chidamber, S.R., and Kemerer, C.F. (1994). *A metric suite for object-oriented design*. IEEE Transactions on Software Engineering, 467–493.  

[2] Li, W., and Henry, S. (1993). *Object-oriented metrics that predict maintainability*. Journal of Systems and Software, 23:111–122.  

[3] Yao, H., Orme, A., and Etzkorn, L. (2005). *Cohesion metrics for ontology design and application*. Journal of Computer Science, 1.  

[4] Tartir, S., and Arpinar, I.B. (2007). *Ontology evaluation and ranking using OntoQA*. ICSC 2007: International Conference on Semantic Computing, Proceedings, 185–192.  

[5] Gangemi, A., Catenacci, C., Ciaramita, M., and Lehmann, J. (2006). *Modelling ontology evaluation and validation*. Semantic Web: Research and Applications, Proceedings, 4011: 140–154.

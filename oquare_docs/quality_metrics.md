[OQuaRE](../README.md)

# OQuaRE Quality Metrics

OQuaRE permits the definition of the quality model in terms of **quality characteristics**. This standard suggests a series of quality characteristics to measure quality. Each quality characteristic has associated **subcharacteristics**, and each subcharacteristic has a set of **Quality Metrics**

 **Quality Metrics** are composed of base and derived measurements. Base measurements correspond to metrics that can be measured directly on the ontology, such as the number of classes, the number of relations, etc., whereas derived ones combine some base measurements.

For the the definition of the base metrics, the following notation has been adopted:  

### Metric Notation  
- $C_1, C_2, ... C_n$ are the Classes of the ontology.  
- $C_1, RC_2, …, RC_k$ are the Relationships of class C_i.  
- $PC_1, PC_2, …, PC_z$ are the Properties of class C_i. 
- $UPC_1, UPC_2, …, UPC_y$ are the Usage of Properties (Object and data) for the property PC_i.  
- $IC_1, IC_2, …, IC_m$ are the Individuals of class C_i.  
- $SupC_1, SupC_2, …, SupC_m$ are the Direct superclasses of a given class C.  
- $Thing$ is the Root class of the ontology.  

## Derived metrics ##
 A set of 19 derived metrics is defined in OQuaRE; some of them have been reused and adapted from both the ontology and software engineering communities. **Coupling Between Objects (CBO)**, **Depth of Inheritance Tree (DIT)**, **Number Of Children (NOC)**, **Response For a Class (RFC)**, and **Weighted Method Count (WMC)** were adapted to ontologies from **Software Engineering** and, in particular, **Object-Oriented Programming (OOP)** (Chidamber and Kemerer, 1994)[1] and Number Of local Methods (NOM) by (Li and Henry, 1993)[2]. Some metrics, especially those addressing **structural properties**, such as those proposed by Yao, Orme, and Etzkorn (2005)[3]; Tartir and Arpinar (2007)[4]; and Gangemi, Catenacci, Ciaramita, and Lehmann [5], were reused from the **ontology engineering community**.
 
## Derived Metrics and Formulas  

### **LCOMOnto - Lack of Cohesion in Methods** 
Mean lenght of all paht from leaf classes to **Thing**..  
$$LCOMOnto = \frac{\sum {Length(path(|C({leaf})_i|))}}{{\sum {path(|C({leaf})_i|)}}}$$

- **Where**:  
  - ${Length(path(|C({leaf})_i|))}$ is the length of the path from the leaf class *i* to **Thing**.  
  - *m* is the total number of paths. 

| Metric/Score | 1   | 2       | 3       | 4       | 5      |
|--------------|------|---------|---------|---------|--------|
| LCOMOnto     | >8   | (6-8]   | (4-6]   | (2-4]   | <=2    |

---

### **DITOnto - Depth of Subsumption Hierarchy**

The length of the largest path from **Thing** to a leaf class.

$${DITOnto} = {Max} \left( \sum D|C_i| \right)$$

- **Where**:  
  - $D|C_i|$ is the length of the path from the *i*-th leaf class to **Thing**.

| Metric/Score | 1   | 2       | 3       | 4       | 5      |
|--------------|------|---------|---------|---------|--------|
| DITOnto      | >8   | (6-8]   | (4-6]   | (2-4]   | [1-2]  |

---

### **NACOnto - Number of Ancestor Classes**  
Mean number of ancestor classes per leaf class.  

$${NACOnto} = \frac{\sum |SupC(Leaf)_i|}{\sum |C(leaf)_i|}$$  

| Metric/Score | 1   | 2       | 3       | 4       | 5      |
|--------------|------|---------|---------|---------|--------|
| NACOnto      | >8   | (6-8]   | (4-6]   | (2-4]   | [1-2]  |

---

### **NOCOnto - Number of Children Classes**  
Number of direct subclasses divided by the number of classes minus the number of leaf classes.  

$${NOCOnto} = \frac{\sum |RC_i|}{\left( \sum |C_i| - \sum |C(leaf)_i| \right)}$$  

| Metric/Score | 1   | 2       | 3       | 4       | 5      |
|--------------|------|---------|---------|---------|--------|
| NOCOnto      | >8   | (6-8]   | (4-6]   | (2-4]   | [1-2]  |

---

### **CBOOnto - Coupling Between Objects**  
Number of related classes.  
$${CBOOnto} = \frac{\sum |SupC_i|}{\left( \sum |C_i| - |R_{{Thing}}| \right)}$$  

| Metric/Score | 1    | 2        | 3        | 4        | 5       |
|--------------|-------|----------|----------|----------|---------|
| CBOOnto      | >12   | (8-12]   | (6-8]    | (3-6]    | [1-3]   |

---
### **CBOOnto2 - Coupling Between Objects**  
Number of related classes.  

$${CBOOnto2} = \frac{\sum |SupC_i|}{\sum |C_i|}$$  

| Metric/Score | 1    | 2        | 3        | 4        | 5       |
|--------------|-------|----------|----------|----------|---------|
| CBOOnto2      | >12   | (8-12]   | (6-8]    | (3-6]    | [1-3]   |

### **RFCOnto - Response for a Class**  
Number of properties directly accessible from a class, including data and object properties.  

$${RFCOnto} = \frac{\sum |PC_i| + \sum |SupC_i|}{\sum |C_i|}$$  

| Metric/Score | 1    | 2        | 3        | 4        | 5       |
|--------------|-------|----------|----------|----------|---------|
| RFCOnto      | >12   | (8-12]   | (6-8]    | (3-6]    | [1-3]   |

---

### **NOMOnto - Number of Usage of Properties**  
Mean number of usage  of properties per class.  

$${NOMOnto} = \frac{\sum |UPC_i|}{\sum |C_i|}$$  

| Metric/Score | 1   | 2       | 3       | 4       | 5      |
|--------------|------|---------|---------|---------|--------|
| NOMOnto      | >8   | (6-8]   | (4-6]   | (2-4]   | <=2    |

---
### **PROnto - Properties Richness**  
Measures the number of relationships defined in the ontology divided by the the number of relationships and usage of properties 

$$PROnto = \sum|RC_i| / (\sum|RC_i| + \sum|UPC_i|)$$  

| Metric/Score | 1       | 2          | 3          | 4          | 5        |
|--------------|---------|------------|------------|------------|----------|
| PROnto       | [0-20]% | (20-40]%   | (40-60]%   | (60-80]%   | >80%     |

---

### **INROnto - Relationships per Class**  
Mean number of relationships (subclasses) per class.  

$$INROnto = \sum|RC_i| / \sum|C_i|$$  

| Metric/Score | 1       | 2          | 3          | 4          | 5        |
|--------------|---------|------------|------------|------------|----------|
| INROnto      | [0-20]% | (20-40]%   | (40-60]%   | (60-80]%   | >80%     |

---

### **POnto - Ancestors per Class**  
Mean number of direct ancestors per class.

$$POnto = \sum|SupC_i| / \sum|C_i|$$  

| Metric/Score | 1       | 2          | 3          | 4          | 5        |
|--------------|---------|------------|------------|------------|----------|
| POnto        | [0-20]% | (20-40]%   | (40-60]%   | (60-80]%   | >80%     |

---

### **CROnto - Class Richness**  
Mean number of individuals per class.

$$CROnto = \sum|IC_i| / \sum|C_i|$$  

| Metric/Score | 1       | 2          | 3          | 4          | 5        |
|--------------|---------|------------|------------|------------|----------|
| CROnto       | [0-20]% | (20-40]%   | (40-60]%   | (60-80]%   | >80%     |

---

### **AROnto - Attribute Richness**  
Measures the number of attributes of the ontology per class.  

$$AROnto = \sum|AttC_i| / \sum|C_i|$$  

- **Where**:  
  - $AttC_i$ is the object property that applies to a class *i* defined in the object property domain and its subclasses

| Metric/Score | 1       | 2          | 3          | 4          | 5        |
|--------------|---------|------------|------------|------------|----------|
| AROnto       | [0-20]% | (20-40]%   | (40-60]%   | (60-80]%   | >80%     |

---

### **ANOnto - Annotation Richness**  
Mean number of annotation properties (label and comments) per class .  

$$ANOnto = \sum|AC_i| / \sum|C_i|$$  

| Metric/Score | 1       | 2          | 3          | 4          | 5        |
|--------------|---------|------------|------------|------------|----------|
| ANOnto       | [0-20]% | (20-40]%   | (40-60]%   | (60-80]%   | >80%     |

---

### **TMOnto - Tangledness**  
Measures the mean number of classes with more than one direct ancestor.  

$$TMOnto = \sum|C(DP)ᵢ| / (\sum|C_i| - 1)$$  

- **Where**:  
  - **C(DP)ᵢ**: Classes with more than one direct parent.  
  - **C_i**: Total number of classes.  

| Metric/Score | 1     | 2        | 3        | 4        | 5        |
|--------------|-------|----------|----------|----------|----------|
| TMOnto       | >8    | (6-8]    | (4-6]    | (2-4]    | (1-2]    |

---

### **TMOnto2 - Tangledness2**  
Measures the mean number of direct ancestors for classes with more than one direct ancestor.  

$$TMOnto2 = \sum|Sup(CDP)ᵢ| / \sum|CDPᵢ|$$  

- **Where**:  
  - **Sup(CDP)ᵢ**: Superclasses of classes with more than one direct parent.  
  - **CDPᵢ**: Classes with more than one direct parent.  

| Metric/Score | 1     | 2        | 3        | 4        | 5        |
|--------------|-------|----------|----------|----------|----------|
| TMOnto2      | >8    | (6-8]    | (4-6]    | (2-4]    | (1-2]    |

---

### **WMCOnto - Weighted Method per Class**  
Measures the mean length of paths from a leaf class to the **Thing**.   

$$WMCOnto = \sum Length(path(|C(leaf)ᵢ|)) / \sum|C(leaf)ᵢ|$$  

- **Where**:  
  - $Length(path(|C(leaf)ᵢ|))$ is the length of the path from the *i*-th leaf class to **Thing**.  
  - **C(leaf)ᵢ** is the leaf classes in the ontology.  

| Metric/Score | 1     | 2        | 3        | 4        | 5        |
|--------------|-------|----------|----------|----------|----------|
| WMCOnto      | >8    | (6-8]    | (4-6]    | (2-4]    | [1-2]    |

---

### **WMCOnto2 - Weighted Method per Class 2**  
Measures the mean number of paths from a leaf class to the class **Thing**. 
$$WMCOnto2 = \sum path(|C(leaf)ᵢ|) / \sum|C(leaf)ᵢ|$$  

- **Where**:  
  - $path(|C(leaf)ᵢ|)$ is the number of paths from the *i*-th leaf class to **Thing**.  
  - **C(leaf)ᵢ** is the leaf classes in the ontology.  

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



[OQuaRE](../README.md)

# The Quality Evaluation Division

 OQuaRE offers two types of **scaling functions** [2], which differ in how the metric values are transformed into quality scores, providing complementary information:

1. **Static Scaling Function**:  
   - Based on recommendations and best practices from the Software Engineering and Ontology Engineering communities.  
   - Uses a predefined transformation function, ensuring that the value of a given metric is always transformed into the same quality score.

2. **Dynamic Scaling Function**:  
   - Based on the observed values of the quality metrics from a **corpus** defined by a set of ontologies.  
   - The transformation function depends on the corpus used, so the value of a metric is transformed into quality scores that vary depending on the corpus of ontologies.


## Static Scaling Function 

There are two types of static scale
- The scale based on percentage score, where each score correspond to an interval starting in 0% until more than 80%, such as the table.

| Metric/Score | 1       | 2          | 3          | 4          | 5        |
|--------------|---------|------------|------------|------------|----------|
| ANOnto       | [0-20]% | (20-40]%   | (40-60]%   | (60-80]%   | >80%     |


- The scale based on interval numbers, where each interval correspond to integer value according to best practices, such as the showed in table 2

| Metric/Score | 1     | 2        | 3        | 4        | 5        |
|--------------|-------|----------|----------|----------|----------|
| TMOnto       | >8    | (6-8]    | (4-6]    | (2-4]    | (1-2]    |


## Dynamic scaling Functions

For defining a Dynamic scale, each ontology in such a corpus is processed with OQuaRE, so calculating the raw values of the quality metrics. These original values are used for generating a scale in k categories determined by k-means clustering [1], which groups similar values into the same category by minimising the intra-class variance and emphasises the differences among categories maximising the interclass variance. the number of categories is defined by the k value.  In the use case defined in [1], the k = 5 because the OQuaRE scale is [1,5].

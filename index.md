---
layout: page
title: Common Hierarchical Abstract Knowledge Representation of Anything
--- 

An upper ontology for for capturing complex multiple-hierarchcial systems of entities. A JSON-LD encoding can be found [here](https://n-harley.github.io/chakra-ontology/json-ld-encoding.json). A Jupyter notebook exploring the ontology can be found [here](https://nbviewer.jupyter.org/github/n-harley/chakra-ontology/blob/main/explorer.ipynb). The classes and properties of the ontology are described below.

|Prefix | Namespace | 
| ---: | :--- |
| `chakra` | <https://n-harley.github.io/chakra-ontology/> |
| `rdf` | <http://www.w3.org/1999/02/22-rdf-syntax-ns#> |
| `rdfs` | <http://www.w3.org/2000/01/rdf-schema#> |
| `owl` | <http://www.w3.org/2002/07/owl#> |



## Classes

### Constituent

#### <https://n-harley.github.io/chakra-ontology/#Constituent>

An instance of [chakra:Constituent](https://n-harley.github.io/chakra-ontology/#Constituent) represents an entity.

```json
{
  "@id": "chakra:Constituent",
  "@type": "owl:Class"
}
```

### Association

#### <https://n-harley.github.io/chakra-ontology/#Association>

An instance of an [chakra:Association](https://n-harley.github.io/chakra-ontology/#Association) represents a directed relationship between instances of [chakra:Constituent](#Constituent). 

```json
{
  "@id": "chakra:Association",
  "@type": "owl:Class"
}
```

### Attribute

#### <https://n-harley.github.io/chakra-ontology/#Attribute>

An instance of [chakra:Attribute](https://n-harley.github.io/chakra-ontology/#Attribute) represents a named element (value) of a conceptual space. 

```json
{
  "@id": "chakra:Attribute",
  "@type": "owl:Class"
}
```

### Property

#### <https://n-harley.github.io/chakra-ontology/#Property>

An instance of [chakra:Property](https://n-harley.github.io/chakra-ontology/#Property) represents a predicate on instances of [chakra:Constituent](https://n-harley.github.io/chakra-ontology/#Constituent).


```json
{
  "@id": "chakra:Property",
  "@type": "owl:Class"
}
```

## Object Properties

### hasAttribute

#### <https://n-harley.github.io/chakra-ontology/#hasAttribute>

An instance of [chakra:hasAttribute](https://n-harley.github.io/chakra-ontology/#hasAttribute) links an instance of [chakra:Constituent](https://n-harley.github.io/chakra-ontology/#Constituent) with an instance of [chakra:Attribute](https://n-harley.github.io/chakra-ontology/#Attribtue).


```json
{
  "@id": "chakra:hasAttribute",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": {"owl:unionOf": {"@list": ["chakra:Constituent","chakra:Association"]},
  "rdfs:range" : "chakra:Attribute"
}
```

### hasProperty

#### <https://n-harley.github.io/chakra-ontology/#hasProperty>

An instance of [chakra:hasProperty](https://n-harley.github.io/chakra-ontology/#hasProperty) links an instance of [chakra:Constituent](https://n-harley.github.io/chakra-ontology/#Constituent) with an instance of [chakra:Property](https://n-harley.github.io/chakra-ontology/#Property).

```json
{
  "@id": "chakra:hasProperty",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": {"owl:unionOf": {"@list": ["chakra:Constituent","chakra:Association"]},
  "rdfs:range": "chakra:Property"
}
```

### hasPart

#### <https://n-harley.github.io/chakra-ontology/#hasPart>

An instance of [chakra:hasPart](https://n-harley.github.io/chakra-ontology/#hasPart) links an instance of [chakra:Constituent](https://n-harley.github.io/chakra-ontology/#Constituent) other instances of [chakra:Constituent](https://n-harley.github.io/chakra-ontology/#Constituent).

```json
{
  "@id": "chakra:hasPart",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": "chakra:Constituent",
  "rdfs:range": "chakra:Constituent"
}
```

### isPartOf

#### <https://n-harley.github.io/chakra-ontology/#isPartOf>

An instance of [chakra:isPartOf](https://n-harley.github.io/chakra-ontology/#isPartOf) links an instance of [chakra:Constituent](https://n-harley.github.io/chakra-ontology/#Constituent) with an instance of [chakra:Constituent](https://n-harley.github.io/chakra-ontology/#Constituent).
```json
{
  "@id": "chakra:isPartOf",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": "chakra:Constituent",
  "rdfs:range": "chakra:Constituent"
}
```

### hasSource

#### <https://n-harley.github.io/chakra-ontology/#hasSource>

An instance of [chakra:hasSource](https://n-harley.github.io/chakra-ontology/#hasSource) links an instance of [chakra:Association](https://n-harley.github.io/chakra-ontology/#Association) with the instance of [chakra:Constituent](https://n-harley.github.io/chakra-ontology/#Constituent) which is the source.

```json
{
  "@id": "chakra:hasSource",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": "chakra:Association",
  "rdfs:range": "chakra:Constituent"
}
```

### hasTarget

#### <https://n-harley.github.io/chakra-ontology/#hasTarget>

An instance of [chakra:hasTarget](https://n-harley.github.io/chakra-ontology/#hasTarget) links an instance of [chakra:Association](https://n-harley.github.io/chakra-ontology/#Association) with the instance of [chakra:Constituent](#Constituent) which is the target.

```json
{
  "@id": "chakra:hasTarget",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": "chakra:Association",
  "rdfs:range": "chakra:Constituent"
}
```

# The Chakra Ontology

An upper ontology for for capturing complex multiple-hierarchcial systems of entities. A JSON-LD encoding can be found [here](https://nick-harley.github.io/chakra-ontology/jsonld.json). A Jupyter notebook exploring the ontology can be found [here](https://nbviewer.jupyter.org/github/nick-harley/chakra-ontology/blob/main/explorer.ipynb). The classes and properties of the ontology are described below.

|Prefix | Namespace | 
| ---: | :--- |
| `chakra` | <https://nick-harley.github.io/chakra-ontology#> |
| `rdf` | <http://www.w3.org/1999/02/22-rdf-syntax-ns#> |
| `rdfs` | <http://www.w3.org/2000/01/rdf-schema#> |
| `owl` | <http://www.w3.org/2002/07/owl#> |



## Classes

### Structure

#### <https://nick-harley.github.io/chakra-ontology#Structure>

```json
{
  "@id": "chakra:Structure",
  "@type": "owl:Class"
}
```

### Constituent

#### <https://nick-harley.github.io/chakra-ontology#Constituent>

```json
{
  "@id": "chakra:Constituent",
  "@type": "owl:Class"
}
```

### Attribute

#### <https://nick-harley.github.io/chakra-ontology#Attribute>

```json
{
  "@id": "chakra:Attribute",
  "@type": "owl:Class"
}
```

### Property

#### <https://nick-harley.github.io/chakra-ontology#Property>

```json
{
  "@id": "chakra:Property",
  "@type": "owl:Class"
}
```

## Object Properties

### hasAttribute

#### <https://nick-harley.github.io/chakra-ontology#hasAttribute>

```json
{
  "@id": "chakra:hasAttribute",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": {
    "owl:unionOf": {
	  "@list": ["chakra:Constituent","chakra:Association"]
	}
  },
  "rdfs:range" : "chakra:Attribute"
}
```

### hasProperty

#### <https://nick-harley.github.io/chakra-ontology#hasProperty>

```json
{
  "@id": "chakra:hasProperty",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": {
    "owl:unionOf": {
	  "@list": ["chakra:Constituent","chakra:Association"]
    },
  }
  "rdfs:range": "chakra:Property"
}
```

### constituents

#### <https://nick-harley.github.io/chakra-ontology#constituents>

```json
{
  "@id": "chakra:constituents",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": "chakra:Structure",
  "rdfs:range": "rdf:List"
}
```

### particles

#### <https://nick-harley.github.io/chakra-ontology#particles>

```json
{
  "@id": "chakra:particles",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": "chakra:Constituent",
  "rdfs:range": "rdf:List"
}
```

### hasPart

#### <https://nick-harley.github.io/chakra-ontology#hasPart>

```json
{
  "@id": "chakra:hasPart",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": "chakra:Constituent",
  "rdfs:range": "chakra:Constituent"
}
```

### isPartOf(isPartOf)

#### <https://nick-harley.github.io/chakra-ontology#isPartOf>

```json
{
  "@id": "chakra:isPartOf",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": "chakra:Constituent",
  "rdfs:range": "chakra:Constituent"
}
```

# The CHAKRA Ontology

#### Common Hierarchical Abstract Knowledge Representation of Anything

## Details

|Prefix | Namespace | 
| ---: | :--- |
| `chakra` | <https://n-harley.github.io/chakra-ontology/> |
| `rdf` | <http://www.w3.org/1999/02/22-rdf-syntax-ns#> |
| `rdfs` | <http://www.w3.org/2000/01/rdf-schema#> |
| `owl` | <http://www.w3.org/2002/07/owl#> |

json-ld encoding: <https://n-harley.github.io/chakra-ontology/json-ld-encoding.json> |

## Classes

#### Constituent

##### [chakra:Constituent](https://n-harley.github.io/chakra-ontology/#Constituent)

```json
{
  "@id": "https://n-harley.github.io/chakra-ontology/#Constituent",
  "@type": "owl:Class"
}
```

#### Association

##### [chakra:Association](https://n-harley.github.io/chakra-ontology/#Association)

```json
{
  "@id": "https://n-harley.github.io/chakra-ontology/#Association",
  "@type": "owl:Class"
}
```

#### Attribute

##### [chakra:Attribute](https://n-harley.github.io/chakra-ontology/#Attribute)

```json
{
  "@id": "https://n-harley.github.io/chakra-ontology/#Attribute",
  "@type": "owl:Class"
}
```

#### Property

[chakra:Property](https://n-harley.github.io/chakra-ontology/#Property)

## Object Properties

#### hasAttribute

[chakra:hasAttribute](https://n-harley.github.io/chakra-ontology/#hasAttribute)

#### hasProperty

[chakra:hasProperty](https://n-harley.github.io/chakra-ontology/#hasProperty)

#### hasPart

[chakra:hasPart](https://n-harley.github.io/chakra-ontology/#hasPart)

#### isPartOf

[chakra:isPartOf](https://n-harley.github.io/chakra-ontology/#isPartOf)

#### hasSource

[chakra:hasSource](https://n-harley.github.io/chakra-ontology/#hasSource)

#### hasTarget

[chakra:hasTarget](https://n-harley.github.io/chakra-ontology/#hasTarget)


```json
{
@context: {
chakra: "https://n-harley.github.io/chakra-ontology/",
rdf: "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
rdfs: "http://www.w3.org/2000/01/rdf-schema#",
owl: "http://www.w3.org/2002/07/owl#",
defines: {
@reverse: "rdfs:isDefinedBy"
},
rdfs:domain: {
@type: "@id"
},
rdfs:range: {
@type: "@id"
},
subClassOf: {
@id: "rdfs:subClassOf",
@type: "@id"
}
},
@id: "chakra:",
@type: "owl:Ontology",
defines: [
{
@id: "chakra:Constituent",
@type: "owl:Class"
},
{
@id: "chakra:Association",
@type: "owl:Class"
},
{
@id: "chakra:Attribute",
@type: "owl:Class"
},
{
@id: "chakra:Property",
@type: "owl:Class"
},
{
@id: "chakra:hasPart",
@type: "owl:ObjectProperty",
rdfs:domain: "chakra:Constituent",
range: "chakra:Constituent"
},
{
@id: "chakra:isPartOf",
@type: "owl:ObjectProperty",
rdfs:domain: "chakra:Constituent",
range: "chakra:Constituent",
owl:inverseOf: "chakra:hasPart"
},
{
@id: "chakra:hasSource",
@type: "owl:ObjectProperty",
rdfs:domain: "chakra:Association",
range: "chakra:Constituent"
},
{
@id: "chakra:hasTarget",
@type: "owl:ObjectProperty",
rdfs:domain: "chakra:Association",
range: "chakra:Constituent"
},
{
@id: "chakra:hasAttribute",
@type: "owl:ObjectProperty",
rdfs:domain: {
owl:unionOf: {
@list: [
"chakra:Constituent",
"chakra:Association"
]
}
},
range: "chakra:Attribute"
},
{
@id: "chakra:hasProperty",
@type: "owl:ObjectProperty",
rdfs:domain: {
owl:unionOf: {
@list: [
"chakra:Constituent",
"chakra:Association"
]
}
},
rdfs:range: "chakra:Property"
}
]
}
```



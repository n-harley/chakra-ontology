# The CHAKRA Ontology

#### Common Hierarchical Abstract Knowledge Representation of Anything

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
  "@id": "chakra:Constituent",
  "@type": "owl:Class"
}
```

#### Association

##### [chakra:Association](https://n-harley.github.io/chakra-ontology/#Association)

```json
{
  "@id": "chakra:Association",
  "@type": "owl:Class"
}
```

#### Attribute

##### [chakra:Attribute](https://n-harley.github.io/chakra-ontology/#Attribute)

```json
{
  "@id": "chakra:Attribute",
  "@type": "owl:Class"
}
```

#### Property

[chakra:Property](https://n-harley.github.io/chakra-ontology/#Property)

```json
{
  "@id": "chakra:Property",
  "@type": "owl:Class"
}
```

## Object Properties

#### hasAttribute

[chakra:hasAttribute](https://n-harley.github.io/chakra-ontology/#hasAttribute)

```json
{
  @id: "chakra:hasAttribute",
  @type: "owl:ObjectProperty",
  rdfs:domain: {owl:unionOf: {@list: ["chakra:Constituent","chakra:Association"]},
  rdfs:range: "chakra:Attribute"
}
```

#### hasProperty

[chakra:hasProperty](https://n-harley.github.io/chakra-ontology/#hasProperty)

```json
{
  @id: "chakra:hasProperty",
  @type: "owl:ObjectProperty",
  rdfs:domain: {owl:unionOf: {@list: ["chakra:Constituent","chakra:Association"]},
  rdfs:range: "chakra:Property"
}
```

#### hasPart

[chakra:hasPart](https://n-harley.github.io/chakra-ontology/#hasPart)

```json
{
  @id: "chakra:hasPart",
  @type: "owl:ObjectProperty",
  rdfs:domain: "chakra:Constituent",
  range: "chakra:Constituent"
}
```

#### isPartOf

[chakra:isPartOf](https://n-harley.github.io/chakra-ontology/#isPartOf)

```json
{
  @id: "chakra:isPartOf",
  @type: "owl:ObjectProperty",
  rdfs:domain: "chakra:Constituent",
  range: "chakra:Constituent"
}
```

#### hasSource

[chakra:hasSource](https://n-harley.github.io/chakra-ontology/#hasSource)

```json
{
  @id: "chakra:hasSource",
  @type: "owl:ObjectProperty",
  rdfs:domain: "chakra:Association",
  range: "chakra:Constituent"
}
```

#### hasTarget

[chakra:hasTarget](https://n-harley.github.io/chakra-ontology/#hasTarget)

```json
{
  @id: "chakra:hasTarget",
  @type: "owl:ObjectProperty",
  rdfs:domain: "chakra:Association",
  range: "chakra:Constituent"
}
```



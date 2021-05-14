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

a representation of an entity.

##### [chakra:Constituent](https://n-harley.github.io/chakra-ontology/#Constituent)

```json
{
  "@id": "chakra:Constituent",
  "@type": "owl:Class"
}
```

#### Association

represents a directed relationship between entities. 

##### [chakra:Association](https://n-harley.github.io/chakra-ontology/#Association)

```json
{
  "@id": "chakra:Association",
  "@type": "owl:Class"
}
```

#### Attribute

represents a named element (value) of a conceptual space. 

##### [chakra:Attribute](https://n-harley.github.io/chakra-ontology/#Attribute)

```json
{
  "@id": "chakra:Attribute",
  "@type": "owl:Class"
}
```

#### Property

represents a predicate on constituents.

##### [chakra:Property](https://n-harley.github.io/chakra-ontology/#Property)

```json
{
  "@id": "chakra:Property",
  "@type": "owl:Class"
}
```

## Object Properties

#### hasAttribute

identifies a constituent with an attribute.

##### [chakra:hasAttribute](https://n-harley.github.io/chakra-ontology/#hasAttribute)

```json
{
  "@id": "chakra:hasAttribute",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": {"owl:unionOf": {"@list": ["chakra:Constituent","chakra:Association"]},
  "rdfs:range" : "chakra:Attribute"
}
```

#### hasProperty

identifies a consituent with a property.

##### [chakra:hasProperty](https://n-harley.github.io/chakra-ontology/#hasProperty)

```json
{
  "@id": "chakra:hasProperty",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": {"owl:unionOf": {"@list": ["chakra:Constituent","chakra:Association"]},
  "rdfs:range": "chakra:Property"
}
```

#### hasPart

connects a constituent to its set of parts.

##### [chakra:hasPart](https://n-harley.github.io/chakra-ontology/#hasPart)

```json
{
  "@id": "chakra:hasPart",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": "chakra:Constituent",
  "rdfs:range": "chakra:Constituent"
}
```

#### isPartOf

inverso of [chakra:hasPart](https://n-harley.github.io/chakra-ontology/#hasPart)

##### [chakra:isPartOf](https://n-harley.github.io/chakra-ontology/#isPartOf)

```json
{
  "@id": "chakra:isPartOf",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": "chakra:Constituent",
  "rdfs:range": "chakra:Constituent"
}
```

#### hasSource

identifies an association with its source constituent.

##### [chakra:hasSource](https://n-harley.github.io/chakra-ontology/#hasSource)

```json
{
  "@id": "chakra:hasSource",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": "chakra:Association",
  "rdfs:range": "chakra:Constituent"
}
```

#### hasTarget

identifies an association with its target constituent.

##### [chakra:hasTarget](https://n-harley.github.io/chakra-ontology/#hasTarget)

```json
{
  "@id": "chakra:hasTarget",
  "@type": "owl:ObjectProperty",
  "rdfs:domain": "chakra:Association",
  "rdfs:range": "chakra:Constituent"
}
```

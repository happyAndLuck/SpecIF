# Tutorial 1: 'Hello World'

At first, we would like to present the shortest SpecIF data-set ever. It contains only items minimally required by the SpecIF schema.

```json
{
    "specifVersion": "1.0",
    "id": "P-Test-Hello-World",
    "title": "Project 'Hello World'",
    "resourceClasses": [{
        "id": "RC-94e50023b1a8015d57",
        "title": "SpecIF:Paragraph",
        "changedAt": "2020-03-01T07:59:00+01:00"
    }],
    "statementClasses": [],
    "resources": [{
        "id": "R-d5b994e50023",
        "title": "Hello World!",
        "class": "RC-94e50023b1a8015d57",
        "changedAt": "2020-03-01T07:59:00+01:00"
    }],
    "statements": [],
    "hierarchies": [{
        "id": "N-78cf736b265",
        "resource": "R-d5b994e50023",
        "changedAt": "2020-03-01T07:59:00+01:00"
    }]
}
```

Some explanations may help to understand the principles:
- The first item indicates the SpecIF version used, so that the respective schema can be applied.
- Of course, a data-set must have an identifier. ASCII alphanumeric characters a-z, A-Z and 0-9 can be used as well as \'_\', \'-\' and \'.\'. An \'id\' must begin with a letter or underscore \'_\', though.
- The \'title\' applies to the whole data-set or project.
- The actual content is provided in the list \'resources\'. Again, every resource has a unique identifier, a title and an indication, when it has been changed.
- Every resource has a class to specify it's semantics and a definition of the applicable data elements, which will be introduced in a subsequent tutorial. Here it is a mere paragraph, but a \'resourceClass\' could equally well define a requirement or model-element. Note the use of a vocabulary term \'SpecIF:Paragraph\'; it is not required, but helps to convey an unambiguous meaning.
- \'statementClasses\' and \'statements\' are used to specify semantic relationships between resources and will be introduced in a subsequent tutorial.
- A hierarchy finally defines a view on the resources. For example, it can be a document outline giving a selection and ordering to resources for reading or it can be a \"Bill of Materials\". A SpecIF data-set can have multiple hierarchies for different audiences or purposes, where a given resource may be referenced once, multiple times or not at all.
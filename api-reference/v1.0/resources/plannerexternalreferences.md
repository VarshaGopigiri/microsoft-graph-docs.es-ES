# <a name="plannerexternalreferences-resource-type"></a>Tipo de recurso plannerExternalReferences

El recurso **plannerExternalReferences** representa la colección de referencias de una tarea. Este es un tipo abierto. Forma parte del objeto [task details](plannertaskdetails.md). El valor del par propiedad-valor es el objeto [externalReference](plannerexternalreference.md).


## <a name="properties"></a>Propiedades
El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar **direcciones URL válidas** a partir de protocolos **HTTP/HTTPS** como propiedades y sus valores deben ser los objetos [externalReference](plannerexternalreference.md). De acuerdo con OData, los nombres de propiedad de los tipos abiertos no pueden contener los caracteres siguientes: `.`, `:` y `%`. Por este motivo, deberán codificarse. A continuación se muestra un ejemplo. Para quitar una referencia, establezca el valor de la propiedad en `null`.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [ "String-value" ],
  "@odata.type": "microsoft.graph.plannerExternalReferences"
}-->


```json
{
  "String-value":
  {
    "alias": "String-value",
    "lastModifiedBy": "String-value",
    "lastModifiedDateTime": "String(timestamp)",
    "previewPriority": "String-value",
    "type": "String-value"
  }
}
```

// Ejemplo

```json
{
  "https%3A//contoso%2Esharepoint%2Ecom/teams/agile/documents/AnnualReport%2Epptx":
  {
    "@odata.type": "microsoft.graph.externalReference", // required in PATCH requests to edit the references on a task
    "alias": "Agile Team Annual Report",
    "lastModifiedBy": {
      "user": {
        "id": "ebf3b108-5234-4e22-b93d-656d7dae5874"
      }
    },
    "lastModifiedDateTime": "2015-09-21T17:45:12.039Z",
    "previewPriority": "0009005756397228702",
    "type": "PowerPoint"
  }
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerExternalReferences resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
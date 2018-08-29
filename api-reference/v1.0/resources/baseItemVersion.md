# <a name="baseitemversion-resource-type"></a>Tipo de recurso BaseItemVersion

El recurso **baseItemVersion** representa una versión anterior de un elemento o una entidad.


## <a name="json-representation"></a>Representación JSON

<!--{
  "blockType": "resource",
  "abstract": true,
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.baseItemVersion",
  "@type.aka": "oneDrive.baseItemVersion"
}-->

```json
{
  "id": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "2016-01-01T15:20:01.125Z",
  "publication": { "@odata.type": "microsoft.graph.publicationFacet" }
}
```

## <a name="properties"></a>Propiedades

|      Nombre de propiedad       |                         Tipo                         |                               Descripción                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| **id**                   | cadena                                               | El identificador de la versión. Solo lectura.                                       |
| **lastModifiedBy**       | [IdentitySet](../resources/identitySet.md)           | Identidad del usuario que modificó por última vez la versión. Solo lectura.        |
| **lastModifiedDateTime** | [DateTimeOffset](../resources/timestamp.md)          | Fecha y hora de la última modificación de la versión. Solo lectura.                 |
| **publication**          | [PublicationFacet](../resources/publicationfacet.md) | Indica el estado de publicación de esta versión concreta. Solo lectura. |


<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->

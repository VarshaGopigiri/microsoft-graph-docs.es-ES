# <a name="list-contracts"></a>Enumerar contratos

Recupere una lista de objetos [contract](../resources/contract.md) asociados a un inquilino de partner.

### <a name="prerequisites"></a>Requisitos previos

Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All*, *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*

### <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->

```http
GET /contracts
```

### <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta. 

> El filtrado es compatible con customerId, defaultDomainName y displayName.

### <a name="request-headers"></a>Encabezados de solicitud

| Nombre      |Descripción|
|:----------|:----------|
| Authorization  | {token} de portador. Necesario. |

### <a name="request-body"></a>Cuerpo de solicitud

No proporcione un cuerpo de solicitud para este método.

### <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Contract](../resources/contract.md) en el cuerpo de la respuesta.

### <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "get_contract"
}-->
```http
GET https://graph.microsoft.com/v1.0/contracts
```

##### <a name="response"></a>Respuesta

Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.Contract",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
    {
      "contractType": "contractType-value",
      "customerId": "customerId-value",
      "defaultDomainName": "defaultDomainName-value",
      "displayName": "displayName-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get Contract",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
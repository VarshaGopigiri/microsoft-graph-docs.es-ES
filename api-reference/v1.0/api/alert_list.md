# <a name="list-alerts"></a>Alertas de lista

Recuperar una lista de objetos de [alerta](../resources/alert.md).

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) |  SecurityEvents.Read.All, SecurityEvents.ReadWrite.All  |
|Delegado (cuenta personal de Microsoft) |  No admitida.  |
|Aplicación | SecurityEvents.Read.All, SecurityEvents.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET /security/alerts
GET /security/alerts?$top=1
GET /security/alerts?$filter={property} eq '{property-value}'
GET /security/alerts?$filter={property} eq '{property-value}'&$top=5
GET /security/alerts?$filter={property} eq '{property-value}'&{property} eq '{property-value}'
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método admite los siguientes [parámetros de consulta de OData](../../../concepts/query_parameters.md) a modo de ayuda para personalizar la respuesta:

- `$count`
- `$filter`
- `$orderby`
- `$select`
- `$skip`
- `$top` devolverá los primeros resultados agregados para cada proveedor API de seguridad.  

Para usar un conjunto de propiedades alternativo, utilice el parámetro de consulta`$select` para especificar el conjunto de propiedades de **alerta** que quiere.  Por ejemplo, para devolver las propiedades **assignedTo**, **category**, y **severity** añada lo siguiente a su consulta: `$select=assignedTo,category,severity`.

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre      |Descripción|
|:----------|:----------|
| Autorización  | {código} del portador. Necesario.|

## <a name="request-body"></a>Cuerpo de la solicitud

No proporcione un cuerpo de solicitud para este método. Se pasará por alto el cuerpo de la solicitud.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos **alerta** en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "get_alerts"
}-->

```http
GET https://graph.microsoft.com/v1.0/security/alerts
```

### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta.

>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.alert",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "activityGroupName": "activityGroupName-value",
      "assignedTo": "assignedTo-value",
      "azureSubscriptionId": "azureSubscriptionId-value",
      "azureTenantId": "azureTenantId-value",
      "category": "category-value",
      "closedDateTime": "datetime-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List alerts",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

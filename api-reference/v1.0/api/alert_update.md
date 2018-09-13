# <a name="update-alert"></a>Actualizar alerta

Actualizar una propiedad modificable **alert** editable dentro de cualquier solución integrada para mantener sincronizados el estado de la alerta y las asignaciones entre las soluciones. Este método actualiza cualquier solución que tiene un registro del Id. de alerta referenciado.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) |   SecurityEvents.ReadWrite.All  |
|Delegado (cuenta personal de Microsoft) |  No admitida.  |
|Aplicación | SecurityEvents.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

> **Nota:** Debe incluir el Id. de **alerta** como un parámetro y vendorInformation que contiene el `provider` y `vendor` con este método.
<!-- { "blockType": "ignored" } -->

```http
PATCH /security/alerts/{alert_id}
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre       | Descripción|
|:-----------|:-----------|
| Authorization  | {código} del portador. Necesario.|
|Prefer | return=representation |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. El cuerpo **debe** contener la propiedad `vendorInformation` con los campos `provider` y `vendor` válidos. En la siguiente tabla se enumeran los campos que se pueden actualizar para una alerta. Los valores para las propiedades existentes que no se incluyen en el cuerpo de la solicitud no cambiarán. Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.

| Propiedad   | Tipo |Descripción|
|:---------------|:--------|:----------|
|assignedTo|Cadena|Nombre del analista al que se asigna la alerta para la evaluación de errores, investigación o corrección.|
|closedDateTime|DateTimeOffset|Hora a la que se ha cerrado la alerta. El tipo de marca de hora representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|comments|Colección String|Comentarios de los analistas de la alerta (para la administración de alertas del cliente).|
|feedback|alertFeedback|Comentarios del analista sobre la alerta. Los valores posibles son: `unknown`, `truePositive`, `falsePositive` y `benignPositive`.|
|status|alertStatus|Estado del ciclo de vida de la alerta (fase). Los valores posibles son: `unknown`, `newAlert`, `inProgress` y `resolved`.|
|tags|Colección String|Etiquetas definidas por el usuario que se pueden aplicar a una alerta y pueden servir como condiciones de filtro (por ejemplo, "HVA", "SAW").|
|vendorInformation *|[securityVendorInformation](../resources/securityvendorinformation.md)|Tipo complejo que contiene detalles sobre el proveedor del producto o servicio de seguridad, el proveedor y el subproveedor (por ejemplo, vendor=Microsoft; provider=Windows Defender ATP; subProvider=AppLocker). **Los campos de proveedor son obligatorios.**|
(\* Indica un campo obligatorio.)

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.

Si se utiliza el encabezado de solicitud opcional, el método devuelve un código de respuesta `200 OK` y el objeto [alert](../resources/alert.md) actualizado en el cuerpo de la respuesta.

## <a name="example-1"></a>Ejemplo 1

### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "update_alert"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/security/alerts/{alert_id}
Content-type: application/json

{
  "assignedTo": "String",
  "closedDateTime": "String (timestamp)",
  "comments": ["String"],
  "feedback": "@odata.type: microsoft.graph.alertFeedback",
  "status": "@odata.type: microsoft.graph.alertStatus",
  "tags": ["String"],
  "vendorInformation":
    {
      "provider": "String",
      "vendor": "String"
    }
}
```

### <a name="response"></a>Respuesta

Este es un ejemplo de respuesta correcta.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.alert"
} -->

```http
HTTP/1.1 204 No Content
```

## <a name="example-2"></a>Ejemplo 2

### <a name="request"></a>Solicitud

En el ejemplo siguiente se muestra una solicitud que incluye el encabezado de solicitud `Prefer`.

<!-- {
  "blockType": "request",
  "name": "update_alert"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/security/alerts/{alert_id}
Content-type: application/json
Prefer: return=representation

{
  "assignedTo": "String",
  "closedDateTime": "String (timestamp)",
  "comments": ["String"],
  "feedback": "@odata.type: microsoft.graph.alertFeedback",
  "status": "@odata.type: microsoft.graph.alertStatus",
  "tags": ["String"],
  "vendorInformation":
    {
      "provider": "String",
      "vendor": "String"
    }
}
```

### <a name="response"></a>Respuesta

Este es un ejemplo de la respuesta cuando se utiliza el encabezado de solicitud opcional `Prefer: return=representation`.

>**Nota:** Es posible que se haya acortado el objeto de respuesta que se muestra aquí para mejorar la legibilidad. En una llamada real se devolverán todas las propiedades.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.alert"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "activityGroupName": "activityGroupName-value",
  "assignedTo": "assignedTo-value",
  "azureSubscriptionId": "azureSubscriptionId-value",
  "azureTenantId": "azureTenantId-value",
  "category": "category-value",
  "closedDateTime": "datetime-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update alert",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

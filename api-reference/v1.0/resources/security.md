# <a name="security-resource-type"></a>Tipo de recurso de seguridad

El recurso de seguridad es el punto de entrada para el modelo de objetos de seguridad. Devuelve un recurso de seguridad singleton. No contiene todas las propiedades utilizables.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto | Descripción |
|:-------------|:------------|:------------|
| [Alertas de lista](../api/alert_list.md) | Colección de [alerta](alert.md) | Obtiene una colección de objetos de alerta. |
| [obtener alertas](../api/alert_get.md) | Colección de [alerta](alert.md) | Obtener un objeto de alerta. |
| [Actualización de alertas](../api/alert_update.md) | Colección de [alerta](alert.md) | Obtener un objeto de alerta. |

## <a name="properties"></a>Propiedades
Ninguno

## <a name="relationships"></a>Relaciones
| Relación | Tipo        | Descripción |
|:-------------|:------------|:------------|
|alertas|Colección de [alerta](alert.md)| Solo lectura. Admite valores NULL.|


## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.security"
}-->

```json
{
}
```

## <a name="example"></a>Ejemplo

El recurso **security** está disponible en la raíz del gráfico.

<!--{
  "blockType": "request"
}-->
```http
GET https://graph.microsoft.com/v1.0/security
```

<!--{
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.security"
}-->
```json
HTTP/1.1 200 OK
Content-type: application/json

{
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "security resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
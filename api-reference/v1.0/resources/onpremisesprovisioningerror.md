# <a name="onpremisesprovisioningerror-resource-type"></a>tipo de recurso onPremisesProvisioningError

Representa los errores de sincronización de directorio de las entidades [user](user.md) y [group](group.md) cuando se sincronizan los directorios locales a Azure Active Directory.

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
|categoría|Cadena| Categoría del error de aprovisionamiento. Nota: Actualmente, hay un único valor posible. Valor posible: *PropertyConflict* (indica que un valor de propiedad no es único). Otros objetos contienen el mismo valor de la propiedad. |
|occurredDateTime|DateTimeOffset| Fecha y hora en que ocurrió el error. |
|propertyCausingError|Cadena| Nombre de la propiedad del directorio que provoca el error. Valores posibles actuales: *UserPrincipalName* o *ProxyAddress* |
|value|Cadena| Valor de la propiedad que provoca el error. |

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onPremisesProvisioningError"
}-->

```json
{
  "category": "String",
  "occurredDateTime": "String (timestamp)",
  "propertyCausingError": "String",
  "value": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onPremisesProvisioningError resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
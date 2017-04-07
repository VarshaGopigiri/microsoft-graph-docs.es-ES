# <a name="shared-resource-type"></a>Tipo de recurso Shared

El recurso **Shared** indica que se ha compartido un objeto DriveItem con otros usuarios. El recurso incluye información sobre cómo se comparte el elemento.

Si un objeto [**DriveItem**](driveitem.md) tiene una faceta **shared** que no es null, el elemento se ha compartido.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.shared"
}-->
```json
{
  "owner": {"@odata.type": "microsoft.graph.identitySet"},
  "scope": "public | organization | users"
}
```

## <a name="properties"></a>Propiedades

| Propiedad | Tipo                          | Descripción                                                                                        |
|:---------|:------------------------------|:---------------------------------------------------------------------------------------------------|
| owner    | [IdentitySet](identityset.md) | La identidad del propietario del elemento compartido. Solo lectura.                                           |
| scope    | String                        | Indica el ámbito sobre cómo se comparte el elemento: `anonymous`, `organization` o `users`. Solo lectura. |

## <a name="scope-values"></a>Valores del ámbito

| Valor        | Descripción                                                                           |
|:-------------|:--------------------------------------------------------------------------------------|
| public       | El elemento se comparte mediante un vínculo que le funciona a cualquier usuario con el vínculo.               |
| organization | El elemento se comparte mediante un vínculo que le funciona a cualquier usuario de la organización del propietario. |
| users        | El elemento se comparte solo con usuarios específicos.                                          |

## <a name="remarks"></a>Comentarios 

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "shared resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

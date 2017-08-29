# <a name="sharinglink-resource-type"></a>Tipo de recurso SharingLink

El recurso **SharingLink** agrupa en una sola estructura los elementos de datos relacionados con vínculos.

Si un recurso [**Permission**](permission.md) tiene una faceta **sharingLink** que no es NULL, el permiso representa un vínculo para compartir (a diferencia de los permisos concedidos a una persona o un grupo).

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "application", "scope" ],
  "@odata.type": "microsoft.graph.sharingLink"
}-->

```json
{
  "application": {"@odata.type": "microsoft.graph.identity"},
  "type": "view | edit",
  "scope": "anonymous | organization",
  "webUrl": "url"
}
```

## <a name="properties"></a>Propiedades

| Propiedad    | Tipo                    | Descripción                                                                                                                                                                                             |
|:------------|:------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| application | [identity](identity.md) | La aplicación con la que está asociada el vínculo.                                                                                                                                                                    |
| type        | String                  | El tipo del vínculo creado.                                                                                                                                                                           |
| scope       | String                  | El ámbito del vínculo representado por este permiso. El valor `anonymous` indica que cualquier usuario puede usar el vínculo, `organization` indica que solo pueden usar el vínculo los usuarios que han iniciado sesión en el mismo inquilino. |
| webUrl      | String                  | Una dirección URL que abre el elemento en el explorador en el sitio web de OneDrive.                                                                                                                                       |

## <a name="type-enumeration"></a>Enumeración de tipos

Esta tabla define los valores posibles de la propiedad **type**:

| Valor   | Rol    | Descripción                                                                     |
|:--------|:--------|:--------------------------------------------------------------------------------|
| `view`  | `read`  | Un vínculo para compartir de solo vista, que permite el acceso de solo lectura.                            |
| `edit`  | `write` | Un vínculo para compartir de edición, que permite el acceso de lectura y escritura.                               |

## <a name="scope-enumeration"></a>Enumeración del ámbito

| Valor          | Descripción                                                                                                                 |
|:---------------|:----------------------------------------------------------------------------------------------------------------------------|
| `anonymous`    | El vínculo para compartir está disponible para que lo use cualquier usuario.                                                                            |
| `organization` | El vínculo para compartir está disponible para que lo use cualquier usuario de la misma organización (inquilino). No está disponible para OneDrive Personal. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sharingLink resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

# <a name="sharinginvitation-resource-type"></a>Tipo de recurso SharingInvitation

El recurso **SharingInvitation** agrupa en una sola estructura los elementos de datos relacionados con invitaciones.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.sharingInvitation"
}-->

```json
{
  "email": "string",
  "invitedBy": {"@odata.type": "microsoft.graph.identitySet" },
  "signInRequired": true
}

```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad  | Tipo                          | Descripción                                                                                                                   |
|:---------------|:------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| email          | String                        | Dirección de correo proporcionada para el destinatario de la invitación para compartir. Solo lectura.                                          |
| invitedBy      | [identitySet](identityset.md) | Proporciona información sobre quién envió la invitación que creó este permiso, si esa información está disponible. Solo lectura. |
| signInRequired | Booleano                       | Si `true` el destinatario de la invitación necesita iniciar sesión para obtener acceso al elemento compartido. Solo lectura.                     |

## <a name="remarks"></a>Comentarios 

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sharingInvitation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

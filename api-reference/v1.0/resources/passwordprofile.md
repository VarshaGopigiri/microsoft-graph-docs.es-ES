# <a name="passwordprofile-resource-type"></a>Tipo de recurso passwordProfile

Contiene el perfil de contraseña asociado al usuario. La propiedad **passwordProfile** de la entidad [user](user.md) es un objeto **passwordProfile**.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|forceChangePasswordNextSignIn|Boolean| **true** si el usuario debe cambiar su contraseña en el próximo inicio de sesión; en caso contrario **false**. |
|password|String|Contraseña del usuario. Esta propiedad es necesaria cuando se crea un usuario. Se puede actualizar, pero el usuario deberá cambiar la contraseña en el próximo inicio de sesión. La contraseña debe cumplir los requisitos mínimos especificados por la propiedad **passwordPolicies** del usuario. De manera predeterminada, se requiere una contraseña segura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.passwordProfile"
}-->

```json
{
  "forceChangePasswordNextSignIn": true,
  "password": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "passwordProfile resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
# <a name="update-grouplifecyclepolicy"></a>Actualizar groupLifecyclePolicy

Actualiza las propiedades de un objeto groupLifecyclePolicy[tipo de recurso groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).
 
|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Directory.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /groupLifecyclePolicies/{id}
```
## <a name="optional-request-headers"></a>Encabezados de solicitud opcionales
| Nombre | Descripción |
|:-----------|:-----------|
| Authorization | {token} de portador. Obligatorio. |
| Content-Type  | application/json  |

## <a name="request-body"></a>Cuerpo de solicitud

En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantienen los valores anteriores o se recalculan según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado.

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
|alternateNotificationEmails|String| Lista de direcciones de correo electrónico para enviar notificaciones para grupos sin propietarios. Se pueden definir varias direcciones de correo electrónico separando una de la otra con un punto y coma. |
|groupLifetimeInDays|Int32| Número de días que faltan para que un grupo expire y necesite renovarse. Una vez renovado, la expiración del grupo se amplía por el número de días definidos. |
|managedGroupTypes|String| El tipo de grupo al que se aplica la directiva de expiración. Los valores posibles son **Todos**, **Seleccionados** o **Ninguno**. |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) actualizado en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "update_grouplifecyclepolicy"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/groupLifecyclePolicies/{id}
Content-type: application/json
Content-length: 125

{
  "groupLifetimeInDays": 180,
  "managedGroupTypes": "Selected",
  "alternateNotificationEmails": "admin@contoso.com"
}
```
##### <a name="response"></a>Respuesta
Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupLifecyclePolicy"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 146

{
  "id": "id-value",
  "groupLifetimeInDays": 180,
  "managedGroupTypes": "Selected",
  "alternateNotificationEmails": "admin@contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update groupLifecyclePolicy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
# <a name="create-rule"></a>Crear regla


Crear un objeto [messageRule](../resources/messagerule.md) especificando un conjunto de condiciones y acciones. 

Outlook lleva a cabo esas acciones si un mensaje entrante en la Bandeja de entrada del usuario cumple las condiciones especificadas.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | MailboxSettings.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | MailboxSettings.ReadWrite    |
|Aplicación | MailboxSettings.ReadWrite |


## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /me/mailFolders/inbox/messagerules
POST /users/{id | userPrincipalName}/mailFolders/inbox/messagerules
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Authorization  | {token} de portador. Obligatorio. |


## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione los parámetros que se aplican a la regla. Estos son los parámetros de cuerpo que suelen usarse al crear reglas. Puede especificar cualquier otra propiedad **messageRule** modificable que corresponda en el cuerpo de la solicitud.

### <a name="request-parameters"></a>Parámetros de la solicitud
| Nombre       | Tipo|Descripción|
|:--------|:-------|:----------|
|actions|[messageRuleActions](../resources/messageruleactions.md)|Acciones que se van a realizar en un mensaje cuando las condiciones correspondientes, si las hubiera, se cumplan. Necesario.|
|conditions|[messageRulePredicates](../resources/messagerulepredicates.md)|Condiciones que, cuando se cumplan, activarán las acciones correspondientes a esa regla. Opcional.|
|displayName| String  | Nombre para mostrar de la regla. Necesario.|
|exceptions| [messageRulePredicates](../resources/messagerulepredicates.md)| Representa las condiciones de excepción de la regla. Opcional. |
|isEnabled | Boolean | Indica si la regla está habilitada para que se aplique a los mensajes. Opcional. |
|sequence| Int32 | Indica el orden en que se ejecuta la regla entre otras reglas. Necesario.|

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto **messageRule** en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "create_messagerule_from_mailfolder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messagerules
Content-type: application/json

{      
    "displayName": "From partner",      
    "sequence": 2,      
    "isEnabled": true,          
    "conditions": {
        "senderContains": [
          "adele"       
        ]
     },
     "actions": {
        "forwardTo": [
          {
             "emailAddress": {
                "name": "Alex Wilbur",
                "address": "AlexW@contoso.onmicrosoft.com"
              }
           }
        ],
        "stopProcessingRules": true
     }    
}

```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.messageRule"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "id":"AQAAAJ5dZqA=",
  "displayName":"From partner",
  "sequence":2,
  "isEnabled":true,
  "hasError":false,
  "isReadOnly":false,
  "conditions":{
    "senderContains":[
      "ADELE"
    ]
  },
  "actions":{
      "stopProcessingRules":true,
      "forwardTo":[
        {
          "emailAddress":{
            "name":"Alex Wilbur",
            "address":"AlexW@contoso.onmicrosoft.com"
          }
        }
      ]
  }
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create rule",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
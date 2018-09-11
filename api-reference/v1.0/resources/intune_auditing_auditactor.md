# <a name="auditactor-resource-type"></a>Tipo de recurso auditActor

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una clase que contiene las propiedades del actor de auditoría.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|type|cadena|Tipo de actor.|
|userPermissions|Colección de cadenas|Lista de los permisos de usuario cuando se ha realizado la auditoría.|
|applicationId|cadena|Id. de aplicación de AAD|
|applicationDisplayName|cadena|Nombre de la aplicación.|
|userPrincipalName|cadena|Nombre principal de usuario (UPN).|
|servicePrincipalName|cadena|Nombre de entidad de seguridad de servicio (SPN).|
|ipAddress|cadena|Dirección IP.|
|userId|cadena|Id. de usuario.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.auditActor"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.auditActor",
  "type": "String",
  "userPermissions": [
    "String"
  ],
  "applicationId": "String",
  "applicationDisplayName": "String",
  "userPrincipalName": "String",
  "servicePrincipalName": "String",
  "ipAddress": "String",
  "userId": "String"
}
```









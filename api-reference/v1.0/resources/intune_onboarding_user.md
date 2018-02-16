# <a name="user-resource-type"></a>Tipo de recurso del usuario

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar usuarios](../api/intune_onboarding_user_list.md)|Colección [user](../resources/intune_onboarding_user.md)|Enumere las propiedades y las relaciones de los objetos [user](../resources/intune_onboarding_user.md).|
|[Obtener user](../api/intune_onboarding_user_get.md)|[user](../resources/intune_onboarding_user.md)|Lea las propiedades y las relaciones del objeto [user](../resources/intune_onboarding_user.md).|
|[Crear user](../api/intune_onboarding_user_create.md)|[user](../resources/intune_onboarding_user.md)|Cree un objeto [user](../resources/intune_onboarding_user.md).|
|[Eliminar user](../api/intune_onboarding_user_delete.md)|Ninguna|Elimina un [user](../resources/intune_onboarding_user.md).|
|[Actualizar user](../api/intune_onboarding_user_update.md)|[user](../resources/intune_onboarding_user.md)|Actualice las propiedades de un objeto [user](../resources/intune_onboarding_user.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Identificador único del usuario.|
|deviceEnrollmentLimit|Int32|El límite del número máximo de dispositivos que el usuario puede inscribir. Los valores permitidos son 5 o 1000.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.user"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.user",
  "id": "String (identifier)",
  "deviceEnrollmentLimit": 1024
}
```




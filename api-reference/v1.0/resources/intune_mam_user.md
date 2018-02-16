# <a name="user-resource-type"></a>Tipo de recurso del usuario

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa un objeto de usuario de Azure Active Directory.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar usuarios](../api/intune_mam_user_list.md)|Colección [user](../resources/intune_mam_user.md)|Enumere las propiedades y las relaciones de los objetos [user](../resources/intune_mam_user.md).|
|[Obtener user](../api/intune_mam_user_get.md)|[user](../resources/intune_mam_user.md)|Lea las propiedades y las relaciones del objeto [user](../resources/intune_mam_user.md).|
|[Crear user](../api/intune_mam_user_create.md)|[user](../resources/intune_mam_user.md)|Cree un objeto [user](../resources/intune_mam_user.md).|
|[Eliminar user](../api/intune_mam_user_delete.md)|Ninguna|Elimina un [user](../resources/intune_mam_user.md).|
|[Actualizar user](../api/intune_mam_user_update.md)|[user](../resources/intune_mam_user.md)|Actualice las propiedades de un objeto [user](../resources/intune_mam_user.md).|
|[Función getManagedAppDiagnosticStatuses](../api/intune_mam_user_getmanagedappdiagnosticstatuses.md)|Colección [getManagedAppDiagnosticStatus](../resources/intune_mam_managedappdiagnosticstatus.md)|Obtiene estados de validación de diagnósticos de un usuario determinado.|
|[Función getManagedAppPolicies](../api/intune_mam_user_getmanagedapppolicies.md)|Colección [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|Obtiene las restricciones de aplicaciones de un usuario determinado.|
|[Acción wipeManagedAppRegistrationsByDeviceTag](../api/intune_mam_user_wipemanagedappregistrationsbydevicetag.md)|Ninguna|Emite una operación de borrado en un registro de la aplicación con la etiqueta del dispositivo especificado.|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|El identificador de usuario.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|managedAppRegistrations|Colección [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|Cero o más registros de administración de aplicaciones administradas que pertenecen al usuario.|

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
  "id": "String (identifier)"
}
```




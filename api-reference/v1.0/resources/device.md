# <a name="device-resource-type"></a>Tipo de recurso device

Representa un dispositivo registrado en la organización. Los dispositivos también se pueden crear en la nube con el servicio de registro de dispositivos o Intune. Las directivas de acceso condicional los usan para la autenticación multifactor. Estos dispositivos pueden ir desde equipos portátiles y de escritorio hasta teléfonos y tabletas. Se hereda de [directoryObject](directoryobject.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Crear dispositivo](../api/device_post_devices.md) | [device](device.md) |Cree un nuevo dispositivo registrado en el directorio.|
|[Obtener dispositivo](../api/device_get.md) | [device](device.md) |Lea las propiedades y relaciones de un objeto device.|
|[Enumerar dispositivos](../api/device_list.md) | Colección [device](device.md)| Recupere una lista de dispositivos registrados en el directorio. |
|[Actualizar dispositivo](../api/device_update.md) | [device](device.md) |Actualice las propiedades de un objeto device. |
|[Eliminar dispositivo](../api/device_delete.md) | Ninguno |Elimine un objeto device. |
|[Crear registeredOwner](../api/device_post_registeredowners.md) |[directoryObject](directoryobject.md)| Agregue un usuario como nuevo propietario del dispositivo; para ello, publique la propiedad de navegación registeredOwners.|
|[Enumerar registeredOwners](../api/device_list_registeredowners.md) |Colección [directoryObject](directoryobject.md)| Obtenga los usuarios que son propietarios registrados del dispositivo de la propiedad de navegación registeredOwners.|
|[Crear registeredUser](../api/device_post_registeredusers.md) |[directoryObject](directoryobject.md)| Agregue un usuario registrado para el dispositivo; para ello, publique la propiedad de navegación registeredUsers.|
|[Enumerar registeredUsers](../api/device_list_registeredusers.md) |Colección [directoryObject](directoryobject.md)| Obtenga los usuarios registrados del dispositivo de la propiedad de navegación registeredUsers.|

## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|accountEnabled|Boolean| **true** si la cuenta está habilitada; en caso contrario, **false**. Necesario.|
|alternativeSecurityIds|Colección [alternativeSecurityId](alternativesecurityid.md)| El operador **any** es necesario para las expresiones de filtro en las propiedades de varios valores. No admite valores NULL. Necesario. |
|approximateLastSignInDateTime|DateTimeOffset| El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|deviceId|Guid| GUID especificado de cliente único para representar el dispositivo. Necesario. |
|deviceMetadata|String|    |
|deviceVersion|Int32|            |
|displayName|String|El nombre para mostrar del dispositivo. Necesario. |
|id|String|El identificador único del dispositivo. Hereda de [directoryObject](directoryobject.md). Clave, no admite valores NULL. Solo lectura.|
|isCompliant|Boolean|**true** si el dispositivo cumple con las directivas de administración de dispositivos móviles (MDM); en caso contrario, **false**.|
|isManaged|Boolean|**true** si una aplicación de administración de dispositivos móviles (MDM) como Intune administra el dispositivo; en caso contrario, **false**.|
|onPremisesLastSyncDateTime|DateTimeOffset|La última hora en que se ha sincronizado el objeto con el directorio local. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|onPremisesSyncEnabled|Booleano|**true** si este objeto está sincronizado desde un directorio local; **false** si este objeto se ha sincronizado originalmente desde un directorio local, pero ya no está sincronizado; **null** si este objeto no se ha sincronizado nunca desde un directorio local (valor predeterminado).|
|operatingSystem|String|El tipo de sistema operativo del dispositivo. Necesario. |
|operatingSystemVersion|String|La versión del sistema operativo del dispositivo. Necesario. |
|physicalIds|Colección String| No admite valores NULL.            |
|trustType|String|    ||

## <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|registeredOwners|Colección [directoryObject](directoryobject.md)|Usuarios que son propietarios registrados del dispositivo. Solo lectura. Admite valores NULL.|
|registeredUsers|Colección [directoryObject](directoryobject.md)|Usuarios que son usuarios registrados del dispositivo. Solo lectura. Admite valores NULL.|



## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "registeredOwners",
    "registeredUsers"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.device"
}-->

```json
{
  "accountEnabled": true,
  "alternativeSecurityIds": [{"@odata.type": "microsoft.graph.alternativeSecurityId"}],
  "approximateLastSignInDateTime": "String (timestamp)",
  "deviceId": "string",
  "deviceMetadata": "string",
  "deviceVersion": 1024,
  "displayName": "string",
  "id": "string (identifier)",
  "isCompliant": true,
  "isManaged": true,
  "onPremisesLastSyncDateTime": "String (timestamp)",
  "onPremisesSyncEnabled": true,
  "operatingSystem": "string",
  "operatingSystemVersion": "string",
  "physicalIds": ["string"],
  "trustType": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "device resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

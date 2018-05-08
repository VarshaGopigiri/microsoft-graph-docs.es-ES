# <a name="update-iosmanagedappregistration"></a>Actualizar iosManagedAppRegistration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualice las propiedades de un objeto [iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md).
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementApps.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md).

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|createdDateTime|DateTimeOffset|Fecha y hora de creación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|lastSyncDateTime|DateTimeOffset|Fecha y hora de la última sincronización de la aplicación con el servicio de administración. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md).|
|applicationVersion|String|Versión de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|managementSdkVersion|String|Versión del SDK de administración de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|platformVersion|String|Versión del sistema operativo. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|deviceType|String|Tipo de dispositivo host. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|deviceTag|String|Etiqueta generada por el SDK de administración de la aplicación, que ayuda a relacionar las aplicaciones que se hospedan en el mismo dispositivo. No garantiza que las aplicaciones se relacionen en todas las condiciones. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md).|
|deviceName|String|Nombre del dispositivo host. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|flaggedReasons|Colección string|Cero o más razones por las que se ha marcado el registro de una aplicación. E.g. Aplicación que se ejecuta en un dispositivo con rooting. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md). Los valores posibles son: `none` y `rootedDevice`.|
|userId|String|Identificador de usuario al que pertenece este registro de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md).|
|appIdentifier|[mobileAppIdentifier](../resources/intune_mam_mobileappidentifier.md)|Identificador del paquete de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)|
|id|String|Clave de la entidad. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md).|
|version|String|Versión de la entidad. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md).|



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}
Content-type: application/json
Content-length: 571

{
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "applicationVersion": "Application Version value",
  "managementSdkVersion": "Management Sdk Version value",
  "platformVersion": "Platform Version value",
  "deviceType": "Device Type value",
  "deviceTag": "Device Tag value",
  "deviceName": "Device Name value",
  "flaggedReasons": [
    "rootedDevice"
  ],
  "userId": "User Id value",
  "appIdentifier": {
    "@odata.type": "microsoft.graph.iosMobileAppIdentifier",
    "bundleId": "Bundle Id value"
  },
  "version": "Version value"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 743

{
  "@odata.type": "#microsoft.graph.iosManagedAppRegistration",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "applicationVersion": "Application Version value",
  "managementSdkVersion": "Management Sdk Version value",
  "platformVersion": "Platform Version value",
  "deviceType": "Device Type value",
  "deviceTag": "Device Tag value",
  "deviceName": "Device Name value",
  "flaggedReasons": [
    "rootedDevice"
  ],
  "userId": "User Id value",
  "appIdentifier": {
    "@odata.type": "microsoft.graph.iosMobileAppIdentifier",
    "bundleId": "Bundle Id value"
  },
  "id": "47632c19-2c19-4763-192c-6347192c6347",
  "version": "Version value"
}
```




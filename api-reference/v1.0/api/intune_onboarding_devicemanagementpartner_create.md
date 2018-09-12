# <a name="create-devicemanagementpartner"></a>Crear deviceManagementPartner

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Cree un objeto [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md).
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementServiceConfig.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceManagementPartners
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Authorization|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceManagementPartner.

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceManagementPartner.

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Todavía no documentado|
|lastHeartbeatDateTime|DateTimeOffset|Marca de tiempo del último latido después de habilitar la opción de administrador Conectarse a los partners de administración de dispositivos|
|partnerState|[deviceManagementPartnerTenantState](../resources/intune_onboarding_devicemanagementpartnertenantstate.md)|Estado de partner de este espacio empresarial. Los valores posibles son: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected` y `unresponsive`.|
|partnerAppType|[deviceManagementPartnerAppType](../resources/intune_onboarding_devicemanagementpartnerapptype.md)|Tipo de aplicación de partner. Los valores posibles son: `unknown`, `singleTenantApp` y `multiTenantApp`.|
|singleTenantAppId|Cadena|Identificador de aplicación de espacio empresarial único de partner|
|displayName|Cadena|Nombre para mostrar del partner|
|isConfigured|Booleano|Si el partner de administración de dispositivos está configurado o no|
|whenPartnerDevicesWillBeRemovedDateTime|DateTimeOffset|Fecha y hora en UTC de cuándo se quitará PartnerDevices|
|whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime|DateTimeOffset|Fecha y hora en UTC de cuándo PartnerDevices se marcará como no compatible|



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceManagementPartners
Content-type: application/json
Content-length: 502

{
  "@odata.type": "#microsoft.graph.deviceManagementPartner",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "unavailable",
  "partnerAppType": "singleTenantApp",
  "singleTenantAppId": "Single Tenant App Id value",
  "displayName": "Display Name value",
  "isConfigured": true,
  "whenPartnerDevicesWillBeRemovedDateTime": "2016-12-31T23:56:38.2655023-08:00",
  "whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime": "2016-12-31T23:58:42.2131231-08:00"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 551

{
  "@odata.type": "#microsoft.graph.deviceManagementPartner",
  "id": "d21e377a-377a-d21e-7a37-1ed27a371ed2",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "unavailable",
  "partnerAppType": "singleTenantApp",
  "singleTenantAppId": "Single Tenant App Id value",
  "displayName": "Display Name value",
  "isConfigured": true,
  "whenPartnerDevicesWillBeRemovedDateTime": "2016-12-31T23:56:38.2655023-08:00",
  "whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime": "2016-12-31T23:58:42.2131231-08:00"
}
```









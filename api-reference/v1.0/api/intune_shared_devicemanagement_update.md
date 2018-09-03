# <a name="update-devicemanagement"></a>Actualizar deviceManagement

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualice las propiedades de un objeto [deviceManagement](../resources/intune_shared_devicemanagement.md).
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

| Tipo de&nbsp;permiso&nbsp;(por&nbsp;flujo de trabajo) | Permisos (de más a menos privilegiados) |
|:---|:---|
| Delegado (cuenta profesional o educativa) |
| &nbsp; &nbsp; Auditoría | DeviceManagementApps.ReadWrite.All |
| &nbsp; &nbsp; Condiciones de la compañía | DeviceManagementServiceConfig.ReadWrite.All |
| &nbsp; &nbsp; Inscripción corporativa | DeviceManagementServiceConfig.ReadWrite.All|
| &nbsp; &nbsp; Configuración de dispositivos | DeviceManagementConfiguration.ReadWrite.All |
| &nbsp; &nbsp; Administración de dispositivos | DeviceManagementManagedDevices.ReadWrite.All |
| &nbsp; &nbsp; Protección de extremo | DeviceManagementManagedDevices.ReadWrite.All |
| &nbsp; &nbsp; Inscripción | DeviceManagementServiceConfig.ReadWrite.All |
| &nbsp; &nbsp; Notificación | DeviceManagementServiceConfig.ReadWrite.All |
| &nbsp; &nbsp; Incorporación | DeviceManagementServiceConfig.ReadWrite.All |
| &nbsp; &nbsp; RBAC | DeviceManagementRBAC.ReadWrite.All |
| &nbsp; &nbsp; Asistencia remota | DeviceManagementServiceConfig.ReadWrite.All |
| &nbsp; &nbsp; Gestión de gastos de telecomunicaciones | DeviceManagementServiceConfig.ReadWrite.All |
| &nbsp; &nbsp; Solución de problemas | DeviceManagementManagedDevices.ReadWrite.All |
| &nbsp; &nbsp; Protección de la información de Windows | DeviceManagementApps.ReadWrite.All |
| Delegado (cuenta personal de Microsoft) | No admitida.|
| Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Authorization|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagement](../resources/intune_shared_devicemanagement.md).

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagement](../resources/intune_shared_devicemanagement.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único del dispositivo|
|**Configuración de dispositivos**|
|settings|[deviceManagementSettings](../resources/intune_deviceconfig_devicemanagementsettings.md)|Configuración de niveles de cuenta.|
|**Administración de dispositivos**|
|subscriptionState|[deviceManagementSubscriptionState](../resources/intune_devices_devicemanagementsubscriptionstate.md)|Estado de suscripción de administración de dispositivos móviles del espacio empresarial. Los valores posibles son: `pending`, `active`, `warning`, `disabled`, `deleted`, `blocked` y `lockedOut`.|
|**Incorporación**|
|intuneBrand|[intuneBrand](../resources/intune_onboarding_intunebrand.md)|intuneBrand contiene datos que se usan para personalizar las aplicaciones del Portal de empresa, así como el portal web del usuario final.|

La compatibilidad con las propiedades de cuerpo de solicitud varía según el flujo de trabajo.

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagement](../resources/intune_shared_devicemanagement.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement
Content-type: application/json
Content-length: 751

{
  "subscriptionState": "active",
  "subscriptions": "intune",
  "adminConsent": {
    "@odata.type": "microsoft.graph.adminConsent",
    "shareAPNSData": "granted"
  },
  "deviceProtectionOverview": {
    "@odata.type": "microsoft.graph.deviceProtectionOverview",
    "totalReportedDeviceCount": 8,
    "inactiveThreatAgentDeviceCount": 14,
    "unknownStateThreatAgentDeviceCount": 2,
    "pendingSignatureUpdateDeviceCount": 1,
    "cleanDeviceCount": 0,
    "pendingFullScanDeviceCount": 10,
    "pendingRestartDeviceCount": 9,
    "pendingManualStepsDeviceCount": 13,
    "pendingOfflineScanDeviceCount": 13,
    "criticalFailuresDeviceCount": 11
  },
  "accountMoveCompletionDateTime": "2017-01-01T00:01:17.9006709-08:00"
}
```

### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Las propiedades devueltas varían según el flujo de trabajo y el contexto.

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 855

{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "0b283420-3420-0b28-2034-280b2034280b",
  "subscriptionState": "active",
  "subscriptions": "intune",
  "adminConsent": {
    "@odata.type": "microsoft.graph.adminConsent",
    "shareAPNSData": "granted"
  },
  "deviceProtectionOverview": {
    "@odata.type": "microsoft.graph.deviceProtectionOverview",
    "totalReportedDeviceCount": 8,
    "inactiveThreatAgentDeviceCount": 14,
    "unknownStateThreatAgentDeviceCount": 2,
    "pendingSignatureUpdateDeviceCount": 1,
    "cleanDeviceCount": 0,
    "pendingFullScanDeviceCount": 10,
    "pendingRestartDeviceCount": 9,
    "pendingManualStepsDeviceCount": 13,
    "pendingOfflineScanDeviceCount": 13,
    "criticalFailuresDeviceCount": 11
  },
  "accountMoveCompletionDateTime": "2017-01-01T00:01:17.9006709-08:00"
}
```



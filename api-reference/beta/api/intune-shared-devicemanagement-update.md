---
title: Actualizar deviceManagement
description: Actualice las propiedades de un objeto deviceManagement.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4d8465ee45a2a6c23dedc4fe049ef1f73bb25218
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924695"
---
# <a name="update-devicemanagement"></a>Actualizar deviceManagement

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualice las propiedades de un objeto [deviceManagement](../resources/intune-shared-devicemanagement.md).

## <a name="prerequisites"></a>Requisitos previos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

Tenga en cuenta que el permiso varía según el flujo de trabajo.

| Permisos&nbsp;tipo&nbsp;(por&nbsp;flujo de trabajo) | Permisos (de más a menos privilegiados) |
|:---|:---|
| Delegado (cuenta profesional o educativa) ||
| &nbsp;&nbsp; **Android para el trabajo** | DeviceManagementConfiguration.ReadWrite.All  |
| &nbsp; &nbsp; **Auditoría** | DeviceManagementApps.ReadWrite.All |
| &nbsp;&nbsp; **Los términos de la compañía** | DeviceManagementServiceConfig.ReadWrite.All |
| &nbsp; &nbsp; **Configuración de dispositivos** | DeviceManagementConfiguration.ReadWrite.All |
| &nbsp; &nbsp; **Administración de dispositivos** | DeviceManagementManagedDevices.ReadWrite.All |
| &nbsp;&nbsp; **SIM electrónica** | DeviceManagementConfiguration.ReadWrite.All |
| &nbsp; &nbsp; **Inscripción** | DeviceManagementServiceConfig.ReadWrite.All |
| &nbsp;&nbsp; **De barrera** | DeviceManagementConfiguration.ReadWrite.All |
| &nbsp;&nbsp; **Notificación** | DeviceManagementServiceConfig.ReadWrite.All |
| &nbsp;&nbsp; **Incorporación** | DeviceManagementServiceConfig.ReadWrite.All |
| &nbsp;&nbsp; **Control de acceso basado en roles (RBAC)** | DeviceManagementRBAC.ReadWrite.All |
| &nbsp;&nbsp; **El acceso remoto** | DeviceManagementConfiguration.Read.All |
| &nbsp;&nbsp; **Asistencia remota** | DeviceManagementServiceConfig.ReadWrite.All |
| &nbsp;&nbsp; **Gestión de gastos de telecomunicaciones** | DeviceManagementServiceConfig.ReadWrite.All |
| &nbsp;&nbsp; **Esta sección** | DeviceManagementManagedDevices.ReadWrite.All |
| &nbsp;&nbsp; **Protección de la información de Windows** | DeviceManagementApps.ReadWrite.All |
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
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagement](../resources/intune-shared-devicemanagement.md).

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagement](../resources/intune-shared-devicemanagement.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único para el dispositivo.|
|**Configuración de dispositivos**|
|intuneAccountId|GUID|Identificador de cuenta Intune para dado inquilino|
|legacyPcManangementEnabled|Booleano|La propiedad para habilitar no MDM administrados heredado administración de PC para esta cuenta. Esta propiedad es de sólo lectura.|
|maximumDepTokens|Int32|Número máximo de tokens DEP permitido por inquilino.|
|configuración|[deviceManagementSettings](../resources/intune-deviceconfig-devicemanagementsettings.md)|Configuración de niveles de cuenta.|
|**Administración de dispositivos**|
|accountMoveCompletionDateTime|DateTimeOffset|La fecha y la hora cuando mueven los datos de inquilinos entre scaleunits.|
|adminConsent|[adminConsent](../resources/intune-devices-adminconsent.md)|Información de consentimiento de administración.|
|deviceProtectionOverview|[deviceProtectionOverview](../resources/intune-devices-deviceprotectionoverview.md)|Información general de protección de dispositivos.|
|managedDeviceCleanupSettings|[managedDeviceCleanupSettings](../resources/intune-devices-manageddevicecleanupsettings.md)|Regla para dispositivos de limpieza|
|subscriptionState|[deviceManagementSubscriptionState](../resources/intune-devices-devicemanagementsubscriptionstate.md)|Estado de suscripción de administración de dispositivos móviles del espacio empresarial. Los valores posibles son: `pending`, `active`, `warning`, `disabled`, `deleted`, `blocked` y `lockedOut`.|
|suscripciones|[deviceManagementSubscriptions](../resources/intune-devices-devicemanagementsubscriptions.md)|Suscripción del inquilino. Los valores posibles son: `none`, `intune`, `office365`, `intunePremium`, `intune_EDU`, `intune_SMB`.|
|windowsMalwareOverview|[windowsMalwareOverview](../resources/intune-devices-windowsmalwareoverview.md)|Información general de malware para los dispositivos de windows.|
|**Incorporación de redes**|
|intuneBrand|[intuneBrand](../resources/intune-onboarding-intunebrand.md)|intuneBrand contiene datos que se usan para personalizar las aplicaciones del Portal de empresa, así como el portal web del usuario final.|

Compatibilidad con propiedades de cuerpo de solicitud varía según el flujo de trabajo.

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagement](../resources/intune-shared-devicemanagement.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud

Este es un ejemplo de una solicitud sigue el flujo de trabajo de administración de dispositivos:

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

Aquí tiene un ejemplo de la respuesta. 

Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Propiedades devueltas varían según el flujo de trabajo y el contexto.

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




---
title: Obtener windowsKioskConfiguration
description: Leer las propiedades y las relaciones del objeto windowsKioskConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3bc5644bfb31717e1c2629fdd92b3937c31c3e72
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939402"
---
# <a name="get-windowskioskconfiguration"></a>Obtener windowsKioskConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Leer las propiedades y las relaciones del objeto [windowsKioskConfiguration](../resources/intune-deviceconfig-windowskioskconfiguration.md) .
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.
## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` objeto de código y [windowsKioskConfiguration](../resources/intune-deviceconfig-windowskioskconfiguration.md) de respuesta en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1889

{
  "value": {
    "@odata.type": "#microsoft.graph.windowsKioskConfiguration",
    "id": "146a990b-990b-146a-0b99-6a140b996a14",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "roleScopeTagIds": [
      "Role Scope Tag Ids value"
    ],
    "supportsScopeTags": true,
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "kioskProfiles": [
      {
        "@odata.type": "microsoft.graph.windowsKioskProfile",
        "profileId": "Profile Id value",
        "profileName": "Profile Name value",
        "appConfiguration": {
          "@odata.type": "microsoft.graph.windowsKioskMultipleApps",
          "apps": [
            {
              "@odata.type": "microsoft.graph.windowsKioskUWPApp",
              "startLayoutTileSize": "small",
              "name": "Name value",
              "appUserModelId": "App User Model Id value",
              "appId": "App Id value",
              "containedAppId": "Contained App Id value"
            }
          ],
          "showTaskBar": true,
          "disallowDesktopApps": true,
          "startMenuLayoutXml": "c3RhcnRNZW51TGF5b3V0WG1s"
        },
        "userAccountsConfiguration": [
          {
            "@odata.type": "microsoft.graph.windowsKioskVisitor"
          }
        ]
      }
    ],
    "kioskBrowserDefaultUrl": "https://example.com/kioskBrowserDefaultUrl/",
    "kioskBrowserEnableHomeButton": true,
    "kioskBrowserEnableNavigationButtons": true,
    "kioskBrowserEnableEndSessionButton": true,
    "kioskBrowserRestartOnIdleTimeInMinutes": 6,
    "kioskBrowserBlockedURLs": [
      "Kiosk Browser Blocked URLs value"
    ],
    "kioskBrowserBlockedUrlExceptions": [
      "Kiosk Browser Blocked Url Exceptions value"
    ]
  }
}
```






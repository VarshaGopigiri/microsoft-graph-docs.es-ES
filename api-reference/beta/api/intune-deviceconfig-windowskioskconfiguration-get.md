---
title: Obtener windowsKioskConfiguration
description: Leer las propiedades y las relaciones del objeto windowsKioskConfiguration.
ms.openlocfilehash: 717f4a0ce9c785450a4694f3409c8c021d26a024
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086035"
---
# <a name="get-windowskioskconfiguration"></a><span data-ttu-id="51525-103">Obtener windowsKioskConfiguration</span><span class="sxs-lookup"><span data-stu-id="51525-103">Get windowsKioskConfiguration</span></span>

> <span data-ttu-id="51525-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="51525-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="51525-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="51525-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="51525-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="51525-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="51525-107">Leer las propiedades y las relaciones del objeto [windowsKioskConfiguration](../resources/intune-deviceconfig-windowskioskconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="51525-107">Read properties and relationships of the [windowsKioskConfiguration](../resources/intune-deviceconfig-windowskioskconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="51525-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="51525-108">Prerequisites</span></span>
<span data-ttu-id="51525-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="51525-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="51525-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="51525-111">Permission type</span></span>|<span data-ttu-id="51525-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="51525-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="51525-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="51525-113">Delegated (work or school account)</span></span>|<span data-ttu-id="51525-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="51525-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="51525-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="51525-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="51525-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51525-116">Not supported.</span></span>|
|<span data-ttu-id="51525-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="51525-117">Application</span></span>|<span data-ttu-id="51525-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51525-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="51525-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="51525-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="51525-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="51525-120">Optional query parameters</span></span>
<span data-ttu-id="51525-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="51525-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="51525-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="51525-122">Request headers</span></span>
|<span data-ttu-id="51525-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51525-123">Header</span></span>|<span data-ttu-id="51525-124">Valor</span><span class="sxs-lookup"><span data-stu-id="51525-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="51525-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="51525-125">Authorization</span></span>|<span data-ttu-id="51525-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="51525-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="51525-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="51525-127">Accept</span></span>|<span data-ttu-id="51525-128">application/json</span><span class="sxs-lookup"><span data-stu-id="51525-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="51525-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="51525-129">Request body</span></span>
<span data-ttu-id="51525-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="51525-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="51525-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51525-131">Response</span></span>
<span data-ttu-id="51525-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [windowsKioskConfiguration](../resources/intune-deviceconfig-windowskioskconfiguration.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="51525-132">If successful, this method returns a `200 OK` response code and [windowsKioskConfiguration](../resources/intune-deviceconfig-windowskioskconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="51525-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="51525-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="51525-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="51525-134">Request</span></span>
<span data-ttu-id="51525-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="51525-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="51525-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51525-136">Response</span></span>
<span data-ttu-id="51525-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="51525-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






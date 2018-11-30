---
title: Enumerar iosDeviceFeaturesConfigurations
description: Enumere las propiedades y las relaciones de los objetos iosDeviceFeaturesConfiguration.
ms.openlocfilehash: dffe7300f243f1c374889b56f9e17aa4c31ba6d0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083277"
---
# <a name="list-iosdevicefeaturesconfigurations"></a><span data-ttu-id="1595d-103">Enumerar iosDeviceFeaturesConfigurations</span><span class="sxs-lookup"><span data-stu-id="1595d-103">List iosDeviceFeaturesConfigurations</span></span>

> <span data-ttu-id="1595d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1595d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1595d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1595d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1595d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1595d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1595d-107">Enumere las propiedades y las relaciones de los objetos [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="1595d-107">List properties and relationships of the [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1595d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1595d-108">Prerequisites</span></span>
<span data-ttu-id="1595d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1595d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1595d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1595d-111">Permission type</span></span>|<span data-ttu-id="1595d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1595d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1595d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1595d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1595d-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="1595d-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="1595d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1595d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1595d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1595d-116">Not supported.</span></span>|
|<span data-ttu-id="1595d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1595d-117">Application</span></span>|<span data-ttu-id="1595d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1595d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1595d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1595d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="1595d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1595d-120">Request headers</span></span>
|<span data-ttu-id="1595d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1595d-121">Header</span></span>|<span data-ttu-id="1595d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1595d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1595d-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="1595d-123">Authorization</span></span>|<span data-ttu-id="1595d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1595d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1595d-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1595d-125">Accept</span></span>|<span data-ttu-id="1595d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1595d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1595d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1595d-127">Request body</span></span>
<span data-ttu-id="1595d-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1595d-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1595d-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1595d-129">Response</span></span>
<span data-ttu-id="1595d-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1595d-130">If successful, this method returns a `200 OK` response code and a collection of [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1595d-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1595d-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="1595d-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1595d-132">Request</span></span>
<span data-ttu-id="1595d-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1595d-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="1595d-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1595d-134">Response</span></span>
<span data-ttu-id="1595d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1595d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 4152

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.iosDeviceFeaturesConfiguration",
      "id": "651e0ab3-0ab3-651e-b30a-1e65b30a1e65",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
      "supportsScopeTags": true,
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "airPrintDestinations": [
        {
          "@odata.type": "microsoft.graph.airPrintDestination",
          "ipAddress": "Ip Address value",
          "resourcePath": "Resource Path value",
          "port": 4,
          "forceTls": true
        }
      ],
      "assetTagTemplate": "Asset Tag Template value",
      "contentFilterSettings": {
        "@odata.type": "microsoft.graph.iosWebContentFilterSpecificWebsitesAccess",
        "specificWebsitesOnly": [
          {
            "@odata.type": "microsoft.graph.iosBookmark",
            "url": "Url value",
            "bookmarkFolder": "Bookmark Folder value",
            "displayName": "Display Name value"
          }
        ],
        "websiteList": [
          {
            "@odata.type": "microsoft.graph.iosBookmark",
            "url": "Url value",
            "bookmarkFolder": "Bookmark Folder value",
            "displayName": "Display Name value"
          }
        ]
      },
      "lockScreenFootnote": "Lock Screen Footnote value",
      "homeScreenDockIcons": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolder",
          "displayName": "Display Name value",
          "pages": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
              "displayName": "Display Name value",
              "apps": [
                {
                  "@odata.type": "microsoft.graph.iosHomeScreenApp",
                  "displayName": "Display Name value",
                  "bundleID": "Bundle ID value"
                }
              ]
            }
          ]
        }
      ],
      "homeScreenPages": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenPage",
          "displayName": "Display Name value",
          "icons": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenFolder",
              "displayName": "Display Name value",
              "pages": [
                {
                  "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
                  "displayName": "Display Name value",
                  "apps": [
                    {
                      "@odata.type": "microsoft.graph.iosHomeScreenApp",
                      "displayName": "Display Name value",
                      "bundleID": "Bundle ID value"
                    }
                  ]
                }
              ]
            }
          ]
        }
      ],
      "notificationSettings": [
        {
          "@odata.type": "microsoft.graph.iosNotificationSettings",
          "bundleID": "Bundle ID value",
          "appName": "App Name value",
          "publisher": "Publisher value",
          "enabled": true,
          "showInNotificationCenter": true,
          "showOnLockScreen": true,
          "alertType": "banner",
          "badgesEnabled": true,
          "soundsEnabled": true
        }
      ],
      "singleSignOnSettings": {
        "@odata.type": "microsoft.graph.iosSingleSignOnSettings",
        "allowedAppsList": [
          {
            "@odata.type": "microsoft.graph.appListItem",
            "name": "Name value",
            "publisher": "Publisher value",
            "appStoreUrl": "https://example.com/appStoreUrl/",
            "appId": "App Id value"
          }
        ],
        "allowedUrls": [
          "Allowed Urls value"
        ],
        "displayName": "Display Name value",
        "kerberosPrincipalName": "Kerberos Principal Name value",
        "kerberosRealm": "Kerberos Realm value"
      }
    }
  ]
}
```






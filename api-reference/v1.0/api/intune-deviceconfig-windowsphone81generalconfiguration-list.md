---
title: Enumerar windowsPhone81GeneralConfigurations
description: Enumere las propiedades y las relaciones de los objetos windowsPhone81GeneralConfiguration.
ms.openlocfilehash: a75593ebc64c08db5f73fd758c5187c4397cc0d2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030028"
---
# <a name="list-windowsphone81generalconfigurations"></a><span data-ttu-id="418b1-103">Enumerar windowsPhone81GeneralConfigurations</span><span class="sxs-lookup"><span data-stu-id="418b1-103">List windowsPhone81GeneralConfigurations</span></span>

> <span data-ttu-id="418b1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="418b1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="418b1-105">Enumere las propiedades y las relaciones de los objetos [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="418b1-105">List properties and relationships of the [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="418b1-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="418b1-106">Prerequisites</span></span>
<span data-ttu-id="418b1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="418b1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="418b1-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="418b1-109">Permission type</span></span>|<span data-ttu-id="418b1-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="418b1-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="418b1-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="418b1-111">Delegated (work or school account)</span></span>|<span data-ttu-id="418b1-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="418b1-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="418b1-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="418b1-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="418b1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="418b1-114">Not supported.</span></span>|
|<span data-ttu-id="418b1-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="418b1-115">Application</span></span>|<span data-ttu-id="418b1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="418b1-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="418b1-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="418b1-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="418b1-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="418b1-118">Request headers</span></span>
|<span data-ttu-id="418b1-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="418b1-119">Header</span></span>|<span data-ttu-id="418b1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="418b1-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="418b1-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="418b1-121">Authorization</span></span>|<span data-ttu-id="418b1-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="418b1-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="418b1-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="418b1-123">Accept</span></span>|<span data-ttu-id="418b1-124">application/json</span><span class="sxs-lookup"><span data-stu-id="418b1-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="418b1-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="418b1-125">Request body</span></span>
<span data-ttu-id="418b1-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="418b1-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="418b1-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="418b1-127">Response</span></span>
<span data-ttu-id="418b1-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="418b1-128">If successful, this method returns a `200 OK` response code and a collection of [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="418b1-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="418b1-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="418b1-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="418b1-130">Request</span></span>
<span data-ttu-id="418b1-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="418b1-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="418b1-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="418b1-132">Response</span></span>
<span data-ttu-id="418b1-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="418b1-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1842

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsPhone81GeneralConfiguration",
      "id": "f5e0e34d-e34d-f5e0-4de3-e0f54de3e0f5",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "applyOnlyToWindowsPhone81": true,
      "appsBlockCopyPaste": true,
      "bluetoothBlocked": true,
      "cameraBlocked": true,
      "cellularBlockWifiTethering": true,
      "compliantAppsList": [
        {
          "@odata.type": "microsoft.graph.appListItem",
          "name": "Name value",
          "publisher": "Publisher value",
          "appStoreUrl": "https://example.com/appStoreUrl/",
          "appId": "App Id value"
        }
      ],
      "compliantAppListType": "appsInListCompliant",
      "diagnosticDataBlockSubmission": true,
      "emailBlockAddingAccounts": true,
      "locationServicesBlocked": true,
      "microsoftAccountBlocked": true,
      "nfcBlocked": true,
      "passwordBlockSimple": true,
      "passwordExpirationDays": 6,
      "passwordMinimumLength": 5,
      "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
      "passwordMinimumCharacterSetCount": 0,
      "passwordPreviousPasswordBlockCount": 2,
      "passwordSignInFailureCountBeforeFactoryReset": 12,
      "passwordRequiredType": "alphanumeric",
      "passwordRequired": true,
      "screenCaptureBlocked": true,
      "storageBlockRemovableStorage": true,
      "storageRequireEncryption": true,
      "webBrowserBlocked": true,
      "wifiBlocked": true,
      "wifiBlockAutomaticConnectHotspots": true,
      "wifiBlockHotspotReporting": true,
      "windowsStoreBlocked": true
    }
  ]
}
```




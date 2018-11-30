---
title: Enumerar windowsUniversalAppXs
description: Enumere las propiedades y las relaciones de los objetos windowsUniversalAppX.
ms.openlocfilehash: 5ce848af62591d300fcd8b40f416df1dd5ad9450
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088272"
---
# <a name="list-windowsuniversalappxs"></a><span data-ttu-id="7a495-103">Enumerar windowsUniversalAppXs</span><span class="sxs-lookup"><span data-stu-id="7a495-103">List windowsUniversalAppXs</span></span>

> <span data-ttu-id="7a495-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7a495-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7a495-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7a495-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7a495-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7a495-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7a495-107">Enumere las propiedades y las relaciones de los objetos [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md).</span><span class="sxs-lookup"><span data-stu-id="7a495-107">List properties and relationships of the [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7a495-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7a495-108">Prerequisites</span></span>
<span data-ttu-id="7a495-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7a495-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7a495-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7a495-111">Permission type</span></span>|<span data-ttu-id="7a495-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7a495-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7a495-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7a495-113">Delegated (work or school account)</span></span>|<span data-ttu-id="7a495-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="7a495-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="7a495-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7a495-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7a495-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7a495-116">Not supported.</span></span>|
|<span data-ttu-id="7a495-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7a495-117">Application</span></span>|<span data-ttu-id="7a495-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7a495-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7a495-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7a495-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="7a495-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7a495-120">Request headers</span></span>
|<span data-ttu-id="7a495-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7a495-121">Header</span></span>|<span data-ttu-id="7a495-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7a495-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7a495-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="7a495-123">Authorization</span></span>|<span data-ttu-id="7a495-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7a495-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7a495-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7a495-125">Accept</span></span>|<span data-ttu-id="7a495-126">application/json</span><span class="sxs-lookup"><span data-stu-id="7a495-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7a495-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7a495-127">Request body</span></span>
<span data-ttu-id="7a495-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7a495-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7a495-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7a495-129">Response</span></span>
<span data-ttu-id="7a495-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7a495-130">If successful, this method returns a `200 OK` response code and a collection of [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7a495-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7a495-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="7a495-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7a495-132">Request</span></span>
<span data-ttu-id="7a495-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7a495-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="7a495-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7a495-134">Response</span></span>
<span data-ttu-id="7a495-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7a495-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1668

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsUniversalAppX",
      "id": "4bc47eba-7eba-4bc4-ba7e-c44bba7ec44b",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisher": "Publisher value",
      "largeIcon": {
        "@odata.type": "microsoft.graph.mimeContent",
        "type": "Type value",
        "value": "dmFsdWU="
      },
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "isFeatured": true,
      "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
      "informationUrl": "https://example.com/informationUrl/",
      "owner": "Owner value",
      "developer": "Developer value",
      "notes": "Notes value",
      "uploadState": 11,
      "publishingState": "processing",
      "committedContentVersion": "Committed Content Version value",
      "fileName": "File Name value",
      "size": 4,
      "applicableArchitectures": "x86",
      "applicableDeviceTypes": "desktop",
      "identityName": "Identity Name value",
      "identityPublisherHash": "Identity Publisher Hash value",
      "identityResourceIdentifier": "Identity Resource Identifier value",
      "isBundle": true,
      "minimumSupportedOperatingSystem": {
        "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
        "v8_0": true,
        "v8_1": true,
        "v10_0": true,
        "v10_1607": true,
        "v10_1703": true,
        "v10_1709": true,
        "v10_1803": true
      },
      "identityVersion": "Identity Version value"
    }
  ]
}
```






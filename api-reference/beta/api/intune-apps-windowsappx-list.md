---
title: Lista windowsAppXs
description: Propiedades de la lista y relaciones de los objetos windowsAppX.
ms.openlocfilehash: 11e4844c22585dca6f7ddbaa9655b154852a56d9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089300"
---
# <a name="list-windowsappxs"></a><span data-ttu-id="a55ae-103">Lista windowsAppXs</span><span class="sxs-lookup"><span data-stu-id="a55ae-103">List windowsAppXs</span></span>

> <span data-ttu-id="a55ae-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a55ae-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a55ae-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a55ae-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a55ae-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a55ae-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a55ae-107">Propiedades de la lista y relaciones de los objetos [windowsAppX](../resources/intune-apps-windowsappx.md) .</span><span class="sxs-lookup"><span data-stu-id="a55ae-107">List properties and relationships of the [windowsAppX](../resources/intune-apps-windowsappx.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a55ae-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a55ae-108">Prerequisites</span></span>
<span data-ttu-id="a55ae-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a55ae-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a55ae-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a55ae-111">Permission type</span></span>|<span data-ttu-id="a55ae-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a55ae-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a55ae-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a55ae-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a55ae-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="a55ae-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="a55ae-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a55ae-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a55ae-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a55ae-116">Not supported.</span></span>|
|<span data-ttu-id="a55ae-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a55ae-117">Application</span></span>|<span data-ttu-id="a55ae-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a55ae-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a55ae-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a55ae-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="a55ae-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a55ae-120">Request headers</span></span>
|<span data-ttu-id="a55ae-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a55ae-121">Header</span></span>|<span data-ttu-id="a55ae-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a55ae-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a55ae-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="a55ae-123">Authorization</span></span>|<span data-ttu-id="a55ae-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a55ae-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a55ae-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a55ae-125">Accept</span></span>|<span data-ttu-id="a55ae-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a55ae-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a55ae-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a55ae-127">Request body</span></span>
<span data-ttu-id="a55ae-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a55ae-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a55ae-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a55ae-129">Response</span></span>
<span data-ttu-id="a55ae-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [windowsAppX](../resources/intune-apps-windowsappx.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a55ae-130">If successful, this method returns a `200 OK` response code and a collection of [windowsAppX](../resources/intune-apps-windowsappx.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a55ae-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a55ae-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="a55ae-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a55ae-132">Request</span></span>
<span data-ttu-id="a55ae-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a55ae-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="a55ae-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a55ae-134">Response</span></span>
<span data-ttu-id="a55ae-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a55ae-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1616

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsAppX",
      "id": "b5179a93-9a93-b517-939a-17b5939a17b5",
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





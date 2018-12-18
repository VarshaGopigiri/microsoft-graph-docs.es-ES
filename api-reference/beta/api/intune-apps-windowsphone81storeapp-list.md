---
title: Lista windowsPhone81StoreApps
description: Propiedades de la lista y relaciones de los objetos windowsPhone81StoreApp.
author: tfitzmac
ms.openlocfilehash: 39fb1b2f9c7fe766bd294ebc05295f6e1b374034
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27313387"
---
# <a name="list-windowsphone81storeapps"></a><span data-ttu-id="67f1b-103">Lista windowsPhone81StoreApps</span><span class="sxs-lookup"><span data-stu-id="67f1b-103">List windowsPhone81StoreApps</span></span>

> <span data-ttu-id="67f1b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="67f1b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="67f1b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="67f1b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="67f1b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="67f1b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="67f1b-107">Propiedades de la lista y relaciones de los objetos [windowsPhone81StoreApp](../resources/intune-apps-windowsphone81storeapp.md) .</span><span class="sxs-lookup"><span data-stu-id="67f1b-107">List properties and relationships of the [windowsPhone81StoreApp](../resources/intune-apps-windowsphone81storeapp.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="67f1b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="67f1b-108">Prerequisites</span></span>
<span data-ttu-id="67f1b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="67f1b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="67f1b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="67f1b-111">Permission type</span></span>|<span data-ttu-id="67f1b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="67f1b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="67f1b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="67f1b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="67f1b-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="67f1b-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="67f1b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="67f1b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="67f1b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="67f1b-116">Not supported.</span></span>|
|<span data-ttu-id="67f1b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="67f1b-117">Application</span></span>|<span data-ttu-id="67f1b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="67f1b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="67f1b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="67f1b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="67f1b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="67f1b-120">Request headers</span></span>
|<span data-ttu-id="67f1b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67f1b-121">Header</span></span>|<span data-ttu-id="67f1b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="67f1b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="67f1b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="67f1b-123">Authorization</span></span>|<span data-ttu-id="67f1b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="67f1b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="67f1b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="67f1b-125">Accept</span></span>|<span data-ttu-id="67f1b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="67f1b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="67f1b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="67f1b-127">Request body</span></span>
<span data-ttu-id="67f1b-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="67f1b-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="67f1b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="67f1b-129">Response</span></span>
<span data-ttu-id="67f1b-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [windowsPhone81StoreApp](../resources/intune-apps-windowsphone81storeapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="67f1b-130">If successful, this method returns a `200 OK` response code and a collection of [windowsPhone81StoreApp](../resources/intune-apps-windowsphone81storeapp.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="67f1b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="67f1b-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="67f1b-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="67f1b-132">Request</span></span>
<span data-ttu-id="67f1b-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="67f1b-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="67f1b-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="67f1b-134">Response</span></span>
<span data-ttu-id="67f1b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="67f1b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 952

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsPhone81StoreApp",
      "id": "f68ce6a1-e6a1-f68c-a1e6-8cf6a1e68cf6",
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
      "appStoreUrl": "https://example.com/appStoreUrl/"
    }
  ]
}
```






---
title: Enumerar mobileLobApps
description: Enumere las propiedades y las relaciones de los objetos mobileLobApp.
author: tfitzmac
ms.openlocfilehash: 2ae7bed1cc876db5df19b620cd9f7aa45b0008b3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331783"
---
# <a name="list-mobilelobapps"></a><span data-ttu-id="d449d-103">Enumerar mobileLobApps</span><span class="sxs-lookup"><span data-stu-id="d449d-103">List mobileLobApps</span></span>

> <span data-ttu-id="d449d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d449d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d449d-105">Enumere las propiedades y las relaciones de los objetos [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="d449d-105">List properties and relationships of the [mobileLobApp](../resources/intune-apps-mobilelobapp.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d449d-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d449d-106">Prerequisites</span></span>
<span data-ttu-id="d449d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d449d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d449d-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d449d-109">Permission type</span></span>|<span data-ttu-id="d449d-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d449d-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d449d-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d449d-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d449d-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="d449d-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="d449d-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d449d-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d449d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d449d-114">Not supported.</span></span>|
|<span data-ttu-id="d449d-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d449d-115">Application</span></span>|<span data-ttu-id="d449d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d449d-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d449d-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d449d-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="d449d-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d449d-118">Request headers</span></span>
|<span data-ttu-id="d449d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d449d-119">Header</span></span>|<span data-ttu-id="d449d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d449d-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d449d-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="d449d-121">Authorization</span></span>|<span data-ttu-id="d449d-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d449d-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d449d-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d449d-123">Accept</span></span>|<span data-ttu-id="d449d-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d449d-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d449d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d449d-125">Request body</span></span>
<span data-ttu-id="d449d-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d449d-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d449d-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d449d-127">Response</span></span>
<span data-ttu-id="d449d-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [mobileLobApp](../resources/intune-apps-mobilelobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d449d-128">If successful, this method returns a `200 OK` response code and a collection of [mobileLobApp](../resources/intune-apps-mobilelobapp.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d449d-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d449d-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="d449d-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d449d-130">Request</span></span>
<span data-ttu-id="d449d-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d449d-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="d449d-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d449d-132">Response</span></span>
<span data-ttu-id="d449d-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d449d-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 983

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.mobileLobApp",
      "id": "2fc11935-1935-2fc1-3519-c12f3519c12f",
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
      "publishingState": "processing",
      "committedContentVersion": "Committed Content Version value",
      "fileName": "File Name value",
      "size": 4
    }
  ]
}
```




---
title: Enumerar managedMobileLobApps
description: Enumere las propiedades y las relaciones de los objetos managedMobileLobApp.
ms.openlocfilehash: 940fd9afb75aec1faffe300b75aa8ef5f0efa4db
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028895"
---
# <a name="list-managedmobilelobapps"></a><span data-ttu-id="53b89-103">Enumerar managedMobileLobApps</span><span class="sxs-lookup"><span data-stu-id="53b89-103">List managedMobileLobApps</span></span>

> <span data-ttu-id="53b89-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="53b89-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="53b89-105">Enumere las propiedades y las relaciones de los objetos [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="53b89-105">List properties and relationships of the [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="53b89-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="53b89-106">Prerequisites</span></span>
<span data-ttu-id="53b89-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="53b89-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="53b89-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="53b89-109">Permission type</span></span>|<span data-ttu-id="53b89-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="53b89-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="53b89-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="53b89-111">Delegated (work or school account)</span></span>|<span data-ttu-id="53b89-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="53b89-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="53b89-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="53b89-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="53b89-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="53b89-114">Not supported.</span></span>|
|<span data-ttu-id="53b89-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="53b89-115">Application</span></span>|<span data-ttu-id="53b89-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="53b89-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="53b89-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="53b89-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="53b89-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="53b89-118">Request headers</span></span>
|<span data-ttu-id="53b89-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53b89-119">Header</span></span>|<span data-ttu-id="53b89-120">Valor</span><span class="sxs-lookup"><span data-stu-id="53b89-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="53b89-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="53b89-121">Authorization</span></span>|<span data-ttu-id="53b89-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="53b89-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="53b89-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="53b89-123">Accept</span></span>|<span data-ttu-id="53b89-124">application/json</span><span class="sxs-lookup"><span data-stu-id="53b89-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="53b89-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="53b89-125">Request body</span></span>
<span data-ttu-id="53b89-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="53b89-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="53b89-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53b89-127">Response</span></span>
<span data-ttu-id="53b89-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="53b89-128">If successful, this method returns a `200 OK` response code and a collection of [managedMobileLobApp](../resources/intune-apps-managedmobilelobapp.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="53b89-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53b89-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="53b89-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="53b89-130">Request</span></span>
<span data-ttu-id="53b89-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="53b89-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="53b89-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53b89-132">Response</span></span>
<span data-ttu-id="53b89-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="53b89-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1069

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedMobileLobApp",
      "id": "cded7cc4-7cc4-cded-c47c-edcdc47cedcd",
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
      "appAvailability": "lineOfBusiness",
      "version": "Version value",
      "committedContentVersion": "Committed Content Version value",
      "fileName": "File Name value",
      "size": 4
    }
  ]
}
```




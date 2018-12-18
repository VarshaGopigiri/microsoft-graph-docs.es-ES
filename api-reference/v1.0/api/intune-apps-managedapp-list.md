---
title: Enumerar managedApps
description: Enumere las propiedades y las relaciones de los objetos managedApp.
author: tfitzmac
ms.openlocfilehash: 86062047c11a44fa6586f1c0582dce78445291ba
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27362121"
---
# <a name="list-managedapps"></a><span data-ttu-id="e7af9-103">Enumerar managedApps</span><span class="sxs-lookup"><span data-stu-id="e7af9-103">List managedApps</span></span>

> <span data-ttu-id="e7af9-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e7af9-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e7af9-105">Enumere las propiedades y las relaciones de los objetos [managedApp](../resources/intune-apps-managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="e7af9-105">List properties and relationships of the [managedApp](../resources/intune-apps-managedapp.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e7af9-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e7af9-106">Prerequisites</span></span>
<span data-ttu-id="e7af9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e7af9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e7af9-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e7af9-109">Permission type</span></span>|<span data-ttu-id="e7af9-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e7af9-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e7af9-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e7af9-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e7af9-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="e7af9-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="e7af9-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e7af9-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e7af9-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e7af9-114">Not supported.</span></span>|
|<span data-ttu-id="e7af9-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e7af9-115">Application</span></span>|<span data-ttu-id="e7af9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e7af9-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e7af9-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e7af9-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="e7af9-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e7af9-118">Request headers</span></span>
|<span data-ttu-id="e7af9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7af9-119">Header</span></span>|<span data-ttu-id="e7af9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e7af9-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e7af9-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="e7af9-121">Authorization</span></span>|<span data-ttu-id="e7af9-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e7af9-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e7af9-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e7af9-123">Accept</span></span>|<span data-ttu-id="e7af9-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e7af9-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e7af9-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e7af9-125">Request body</span></span>
<span data-ttu-id="e7af9-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e7af9-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e7af9-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7af9-127">Response</span></span>
<span data-ttu-id="e7af9-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [managedApp](../resources/intune-apps-managedapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e7af9-128">If successful, this method returns a `200 OK` response code and a collection of [managedApp](../resources/intune-apps-managedapp.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e7af9-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e7af9-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="e7af9-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e7af9-130">Request</span></span>
<span data-ttu-id="e7af9-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e7af9-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="e7af9-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7af9-132">Response</span></span>
<span data-ttu-id="e7af9-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e7af9-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 935

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedApp",
      "id": "f687dd85-dd85-f687-85dd-87f685dd87f6",
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
      "version": "Version value"
    }
  ]
}
```




---
title: Enumerar userInstallStateSummaries
description: Enumere las propiedades y las relaciones de los objetos userInstallStateSummary.
ms.openlocfilehash: 9c28b1b8ab7fd4b3d9b009bc4e436c8de9f64c54
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032306"
---
# <a name="list-userinstallstatesummaries"></a><span data-ttu-id="f85e4-103">Enumerar userInstallStateSummaries</span><span class="sxs-lookup"><span data-stu-id="f85e4-103">List userInstallStateSummaries</span></span>

> <span data-ttu-id="f85e4-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f85e4-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f85e4-105">Enumere las propiedades y las relaciones de los objetos [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="f85e4-105">List properties and relationships of the [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f85e4-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f85e4-106">Prerequisites</span></span>
<span data-ttu-id="f85e4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f85e4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f85e4-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f85e4-109">Permission type</span></span>|<span data-ttu-id="f85e4-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f85e4-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f85e4-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f85e4-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f85e4-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="f85e4-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="f85e4-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f85e4-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f85e4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f85e4-114">Not supported.</span></span>|
|<span data-ttu-id="f85e4-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f85e4-115">Application</span></span>|<span data-ttu-id="f85e4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f85e4-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f85e4-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f85e4-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary
```

## <a name="request-headers"></a><span data-ttu-id="f85e4-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f85e4-118">Request headers</span></span>
|<span data-ttu-id="f85e4-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f85e4-119">Header</span></span>|<span data-ttu-id="f85e4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f85e4-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f85e4-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="f85e4-121">Authorization</span></span>|<span data-ttu-id="f85e4-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f85e4-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f85e4-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f85e4-123">Accept</span></span>|<span data-ttu-id="f85e4-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f85e4-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f85e4-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f85e4-125">Request body</span></span>
<span data-ttu-id="f85e4-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f85e4-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f85e4-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f85e4-127">Response</span></span>
<span data-ttu-id="f85e4-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f85e4-128">If successful, this method returns a `200 OK` response code and a collection of [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f85e4-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f85e4-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="f85e4-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f85e4-130">Request</span></span>
<span data-ttu-id="f85e4-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f85e4-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary
```

### <a name="response"></a><span data-ttu-id="f85e4-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f85e4-132">Response</span></span>
<span data-ttu-id="f85e4-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f85e4-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 295

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.userInstallStateSummary",
      "id": "1e5b41ba-41ba-1e5b-ba41-5b1eba415b1e",
      "userName": "User Name value",
      "installedDeviceCount": 4,
      "failedDeviceCount": 1,
      "notInstalledDeviceCount": 7
    }
  ]
}
```




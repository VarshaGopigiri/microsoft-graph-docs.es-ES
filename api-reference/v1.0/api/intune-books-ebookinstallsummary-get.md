---
title: Obtener eBookInstallSummary
description: Lea las propiedades y las relaciones del objeto eBookInstallSummary.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: d60ea9c491d931f022ae83dda6285d36c6855f89
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933641"
---
# <a name="get-ebookinstallsummary"></a><span data-ttu-id="fd674-103">Obtener eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="fd674-103">Get eBookInstallSummary</span></span>

> <span data-ttu-id="fd674-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fd674-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fd674-105">Lea las propiedades y las relaciones del objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="fd674-105">Read properties and relationships of the [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fd674-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fd674-106">Prerequisites</span></span>
<span data-ttu-id="fd674-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fd674-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fd674-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fd674-109">Permission type</span></span>|<span data-ttu-id="fd674-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fd674-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fd674-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fd674-111">Delegated (work or school account)</span></span>|<span data-ttu-id="fd674-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="fd674-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="fd674-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fd674-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fd674-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fd674-114">Not supported.</span></span>|
|<span data-ttu-id="fd674-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fd674-115">Application</span></span>|<span data-ttu-id="fd674-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fd674-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fd674-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fd674-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedEBooks/{managedEBookId}/installSummary
```

## <a name="optional-query-parameters"></a><span data-ttu-id="fd674-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="fd674-118">Optional query parameters</span></span>
<span data-ttu-id="fd674-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fd674-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="fd674-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fd674-120">Request headers</span></span>
|<span data-ttu-id="fd674-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd674-121">Header</span></span>|<span data-ttu-id="fd674-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fd674-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fd674-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="fd674-123">Authorization</span></span>|<span data-ttu-id="fd674-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fd674-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fd674-125">Accept</span><span class="sxs-lookup"><span data-stu-id="fd674-125">Accept</span></span>|<span data-ttu-id="fd674-126">application/json</span><span class="sxs-lookup"><span data-stu-id="fd674-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fd674-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fd674-127">Request body</span></span>
<span data-ttu-id="fd674-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fd674-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fd674-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fd674-129">Response</span></span>
<span data-ttu-id="fd674-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fd674-130">If successful, this method returns a `200 OK` response code and [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fd674-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fd674-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="fd674-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fd674-132">Request</span></span>
<span data-ttu-id="fd674-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fd674-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/installSummary
```

### <a name="response"></a><span data-ttu-id="fd674-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fd674-134">Response</span></span>
<span data-ttu-id="fd674-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fd674-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 320

{
  "value": {
    "@odata.type": "#microsoft.graph.eBookInstallSummary",
    "id": "9708ad78-ad78-9708-78ad-089778ad0897",
    "installedDeviceCount": 4,
    "failedDeviceCount": 1,
    "notInstalledDeviceCount": 7,
    "installedUserCount": 2,
    "failedUserCount": 15,
    "notInstalledUserCount": 5
  }
}
```




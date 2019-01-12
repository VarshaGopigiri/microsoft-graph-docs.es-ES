---
title: Enumerar enrollmentTroubleshootingEvents
description: Enumere las propiedades y las relaciones de los objetos enrollmentTroubleshootingEvent.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ba4ed35851d5cd13e60099826e5f35f60466ee6d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917359"
---
# <a name="list-enrollmenttroubleshootingevents"></a><span data-ttu-id="41c0f-103">Enumerar enrollmentTroubleshootingEvents</span><span class="sxs-lookup"><span data-stu-id="41c0f-103">List enrollmentTroubleshootingEvents</span></span>

> <span data-ttu-id="41c0f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="41c0f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="41c0f-105">Enumere las propiedades y las relaciones de los objetos [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="41c0f-105">List properties and relationships of the [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="41c0f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="41c0f-106">Prerequisites</span></span>
<span data-ttu-id="41c0f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="41c0f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="41c0f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="41c0f-109">Permission type</span></span>|<span data-ttu-id="41c0f-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="41c0f-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="41c0f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="41c0f-111">Delegated (work or school account)</span></span>|<span data-ttu-id="41c0f-112">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="41c0f-112">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="41c0f-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="41c0f-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="41c0f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41c0f-114">Not supported.</span></span>|
|<span data-ttu-id="41c0f-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="41c0f-115">Application</span></span>|<span data-ttu-id="41c0f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41c0f-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="41c0f-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="41c0f-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/troubleshootingEvents
```

## <a name="request-headers"></a><span data-ttu-id="41c0f-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="41c0f-118">Request headers</span></span>
|<span data-ttu-id="41c0f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41c0f-119">Header</span></span>|<span data-ttu-id="41c0f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="41c0f-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="41c0f-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="41c0f-121">Authorization</span></span>|<span data-ttu-id="41c0f-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="41c0f-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="41c0f-123">Accept</span><span class="sxs-lookup"><span data-stu-id="41c0f-123">Accept</span></span>|<span data-ttu-id="41c0f-124">application/json</span><span class="sxs-lookup"><span data-stu-id="41c0f-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="41c0f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="41c0f-125">Request body</span></span>
<span data-ttu-id="41c0f-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="41c0f-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="41c0f-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41c0f-127">Response</span></span>
<span data-ttu-id="41c0f-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="41c0f-128">If successful, this method returns a `200 OK` response code and a collection of [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="41c0f-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="41c0f-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="41c0f-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="41c0f-130">Request</span></span>
<span data-ttu-id="41c0f-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="41c0f-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/troubleshootingEvents
```

### <a name="response"></a><span data-ttu-id="41c0f-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41c0f-132">Response</span></span>
<span data-ttu-id="41c0f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="41c0f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 639

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.enrollmentTroubleshootingEvent",
      "id": "c4a623f5-23f5-c4a6-f523-a6c4f523a6c4",
      "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
      "correlationId": "Correlation Id value",
      "managedDeviceIdentifier": "Managed Device Identifier value",
      "operatingSystem": "Operating System value",
      "osVersion": "Os Version value",
      "userId": "User Id value",
      "deviceId": "Device Id value",
      "enrollmentType": "userEnrollment",
      "failureCategory": "authentication",
      "failureReason": "Failure Reason value"
    }
  ]
}
```




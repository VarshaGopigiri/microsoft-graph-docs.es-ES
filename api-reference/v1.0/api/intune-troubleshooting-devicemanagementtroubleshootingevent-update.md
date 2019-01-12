---
title: Actualizar deviceManagementTroubleshootingEvent
description: Actualice las propiedades de un objeto deviceManagementTroubleshootingEvent.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: bbbf0689c6e25b19c96dc491d77ddb3cc74251bd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970832"
---
# <a name="update-devicemanagementtroubleshootingevent"></a><span data-ttu-id="05bd9-103">Actualizar deviceManagementTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="05bd9-103">Update deviceManagementTroubleshootingEvent</span></span>

> <span data-ttu-id="05bd9-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="05bd9-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="05bd9-105">Actualice las propiedades de un objeto [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="05bd9-105">Update the properties of a [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="05bd9-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="05bd9-106">Prerequisites</span></span>
<span data-ttu-id="05bd9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="05bd9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="05bd9-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="05bd9-109">Permission type</span></span>|<span data-ttu-id="05bd9-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="05bd9-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="05bd9-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="05bd9-111">Delegated (work or school account)</span></span>|<span data-ttu-id="05bd9-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="05bd9-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="05bd9-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="05bd9-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="05bd9-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="05bd9-114">Not supported.</span></span>|
|<span data-ttu-id="05bd9-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="05bd9-115">Application</span></span>|<span data-ttu-id="05bd9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="05bd9-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="05bd9-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="05bd9-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
```

## <a name="request-headers"></a><span data-ttu-id="05bd9-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="05bd9-118">Request headers</span></span>
|<span data-ttu-id="05bd9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05bd9-119">Header</span></span>|<span data-ttu-id="05bd9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="05bd9-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="05bd9-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="05bd9-121">Authorization</span></span>|<span data-ttu-id="05bd9-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="05bd9-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="05bd9-123">Accept</span><span class="sxs-lookup"><span data-stu-id="05bd9-123">Accept</span></span>|<span data-ttu-id="05bd9-124">application/json</span><span class="sxs-lookup"><span data-stu-id="05bd9-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="05bd9-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="05bd9-125">Request body</span></span>
<span data-ttu-id="05bd9-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="05bd9-126">In the request body, supply a JSON representation for the [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md) object.</span></span>

<span data-ttu-id="05bd9-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="05bd9-127">The following table shows the properties that are required when you create the [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md).</span></span>

|<span data-ttu-id="05bd9-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="05bd9-128">Property</span></span>|<span data-ttu-id="05bd9-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="05bd9-129">Type</span></span>|<span data-ttu-id="05bd9-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="05bd9-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="05bd9-131">id</span><span class="sxs-lookup"><span data-stu-id="05bd9-131">id</span></span>|<span data-ttu-id="05bd9-132">String</span><span class="sxs-lookup"><span data-stu-id="05bd9-132">String</span></span>|<span data-ttu-id="05bd9-133">UUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="05bd9-133">UUID for the object</span></span>|
|<span data-ttu-id="05bd9-134">eventDateTime</span><span class="sxs-lookup"><span data-stu-id="05bd9-134">eventDateTime</span></span>|<span data-ttu-id="05bd9-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="05bd9-135">DateTimeOffset</span></span>|<span data-ttu-id="05bd9-136">Hora en que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="05bd9-136">Time when the event occurred .</span></span>|
|<span data-ttu-id="05bd9-137">correlationId</span><span class="sxs-lookup"><span data-stu-id="05bd9-137">correlationId</span></span>|<span data-ttu-id="05bd9-138">String</span><span class="sxs-lookup"><span data-stu-id="05bd9-138">String</span></span>|<span data-ttu-id="05bd9-139">Id. utilizado para rastrear el error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="05bd9-139">Id used for tracing the failure in the service.</span></span>|



## <a name="response"></a><span data-ttu-id="05bd9-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05bd9-140">Response</span></span>
<span data-ttu-id="05bd9-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="05bd9-141">If successful, this method returns a `200 OK` response code and an updated [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="05bd9-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="05bd9-142">Example</span></span>
### <a name="request"></a><span data-ttu-id="05bd9-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="05bd9-143">Request</span></span>
<span data-ttu-id="05bd9-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="05bd9-144">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
Content-type: application/json
Content-length: 104

{
  "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
  "correlationId": "Correlation Id value"
}
```

### <a name="response"></a><span data-ttu-id="05bd9-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05bd9-145">Response</span></span>
<span data-ttu-id="05bd9-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="05bd9-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 228

{
  "@odata.type": "#microsoft.graph.deviceManagementTroubleshootingEvent",
  "id": "fb26dcee-dcee-fb26-eedc-26fbeedc26fb",
  "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
  "correlationId": "Correlation Id value"
}
```




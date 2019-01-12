---
title: Crear deviceManagementTroubleshootingEvent
description: Cree un objeto deviceManagementTroubleshootingEvent.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: c0fd0e5ddceec3e3aa4ffae3507635286d664df8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922602"
---
# <a name="create-devicemanagementtroubleshootingevent"></a><span data-ttu-id="50d2c-103">Crear deviceManagementTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="50d2c-103">Create deviceManagementTroubleshootingEvent</span></span>

> <span data-ttu-id="50d2c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="50d2c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="50d2c-105">Cree un objeto [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="50d2c-105">Create a new [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="50d2c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="50d2c-106">Prerequisites</span></span>
<span data-ttu-id="50d2c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="50d2c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="50d2c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="50d2c-109">Permission type</span></span>|<span data-ttu-id="50d2c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="50d2c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="50d2c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="50d2c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="50d2c-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="50d2c-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="50d2c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="50d2c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="50d2c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="50d2c-114">Not supported.</span></span>|
|<span data-ttu-id="50d2c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="50d2c-115">Application</span></span>|<span data-ttu-id="50d2c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="50d2c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="50d2c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="50d2c-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/troubleshootingEvents
```

## <a name="request-headers"></a><span data-ttu-id="50d2c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="50d2c-118">Request headers</span></span>
|<span data-ttu-id="50d2c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50d2c-119">Header</span></span>|<span data-ttu-id="50d2c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="50d2c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="50d2c-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="50d2c-121">Authorization</span></span>|<span data-ttu-id="50d2c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="50d2c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="50d2c-123">Accept</span><span class="sxs-lookup"><span data-stu-id="50d2c-123">Accept</span></span>|<span data-ttu-id="50d2c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="50d2c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="50d2c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="50d2c-125">Request body</span></span>
<span data-ttu-id="50d2c-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceManagementTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="50d2c-126">In the request body, supply a JSON representation for the deviceManagementTroubleshootingEvent object.</span></span>

<span data-ttu-id="50d2c-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceManagementTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="50d2c-127">The following table shows the properties that are required when you create the deviceManagementTroubleshootingEvent.</span></span>

|<span data-ttu-id="50d2c-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="50d2c-128">Property</span></span>|<span data-ttu-id="50d2c-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="50d2c-129">Type</span></span>|<span data-ttu-id="50d2c-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="50d2c-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="50d2c-131">id</span><span class="sxs-lookup"><span data-stu-id="50d2c-131">id</span></span>|<span data-ttu-id="50d2c-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="50d2c-132">String</span></span>|<span data-ttu-id="50d2c-133">UUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="50d2c-133">UUID for the object</span></span>|
|<span data-ttu-id="50d2c-134">eventDateTime</span><span class="sxs-lookup"><span data-stu-id="50d2c-134">eventDateTime</span></span>|<span data-ttu-id="50d2c-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="50d2c-135">DateTimeOffset</span></span>|<span data-ttu-id="50d2c-136">Hora en que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="50d2c-136">Time when the event occurred .</span></span>|
|<span data-ttu-id="50d2c-137">correlationId</span><span class="sxs-lookup"><span data-stu-id="50d2c-137">correlationId</span></span>|<span data-ttu-id="50d2c-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="50d2c-138">String</span></span>|<span data-ttu-id="50d2c-139">Id. utilizado para rastrear el error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="50d2c-139">Id used for tracing the failure in the service.</span></span>|



## <a name="response"></a><span data-ttu-id="50d2c-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50d2c-140">Response</span></span>
<span data-ttu-id="50d2c-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="50d2c-141">If successful, this method returns a `201 Created` response code and a [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="50d2c-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="50d2c-142">Example</span></span>
### <a name="request"></a><span data-ttu-id="50d2c-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="50d2c-143">Request</span></span>
<span data-ttu-id="50d2c-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="50d2c-144">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/troubleshootingEvents
Content-type: application/json
Content-length: 179

{
  "@odata.type": "#microsoft.graph.deviceManagementTroubleshootingEvent",
  "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
  "correlationId": "Correlation Id value"
}
```

### <a name="response"></a><span data-ttu-id="50d2c-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50d2c-145">Response</span></span>
<span data-ttu-id="50d2c-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="50d2c-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 228

{
  "@odata.type": "#microsoft.graph.deviceManagementTroubleshootingEvent",
  "id": "fb26dcee-dcee-fb26-eedc-26fbeedc26fb",
  "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
  "correlationId": "Correlation Id value"
}
```




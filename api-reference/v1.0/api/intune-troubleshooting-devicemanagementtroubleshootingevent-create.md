---
title: Crear deviceManagementTroubleshootingEvent
description: Cree un objeto deviceManagementTroubleshootingEvent.
ms.openlocfilehash: b6af29c77037c4da49d1593341718a8e798805c2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030775"
---
# <a name="create-devicemanagementtroubleshootingevent"></a><span data-ttu-id="a1539-103">Crear deviceManagementTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="a1539-103">Create deviceManagementTroubleshootingEvent</span></span>

> <span data-ttu-id="a1539-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a1539-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a1539-105">Cree un objeto [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="a1539-105">Create a new [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a1539-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a1539-106">Prerequisites</span></span>
<span data-ttu-id="a1539-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a1539-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a1539-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a1539-109">Permission type</span></span>|<span data-ttu-id="a1539-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a1539-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a1539-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a1539-111">Delegated (work or school account)</span></span>|<span data-ttu-id="a1539-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a1539-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="a1539-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a1539-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a1539-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a1539-114">Not supported.</span></span>|
|<span data-ttu-id="a1539-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a1539-115">Application</span></span>|<span data-ttu-id="a1539-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a1539-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a1539-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a1539-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/troubleshootingEvents
```

## <a name="request-headers"></a><span data-ttu-id="a1539-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a1539-118">Request headers</span></span>
|<span data-ttu-id="a1539-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1539-119">Header</span></span>|<span data-ttu-id="a1539-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a1539-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a1539-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="a1539-121">Authorization</span></span>|<span data-ttu-id="a1539-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a1539-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a1539-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a1539-123">Accept</span></span>|<span data-ttu-id="a1539-124">application/json</span><span class="sxs-lookup"><span data-stu-id="a1539-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a1539-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a1539-125">Request body</span></span>
<span data-ttu-id="a1539-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceManagementTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="a1539-126">In the request body, supply a JSON representation for the deviceManagementTroubleshootingEvent object.</span></span>

<span data-ttu-id="a1539-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceManagementTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="a1539-127">The following table shows the properties that are required when you create the deviceManagementTroubleshootingEvent.</span></span>

|<span data-ttu-id="a1539-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a1539-128">Property</span></span>|<span data-ttu-id="a1539-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1539-129">Type</span></span>|<span data-ttu-id="a1539-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1539-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a1539-131">id</span><span class="sxs-lookup"><span data-stu-id="a1539-131">id</span></span>|<span data-ttu-id="a1539-132">String</span><span class="sxs-lookup"><span data-stu-id="a1539-132">String</span></span>|<span data-ttu-id="a1539-133">UUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="a1539-133">UUID for the object</span></span>|
|<span data-ttu-id="a1539-134">eventDateTime</span><span class="sxs-lookup"><span data-stu-id="a1539-134">eventDateTime</span></span>|<span data-ttu-id="a1539-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a1539-135">DateTimeOffset</span></span>|<span data-ttu-id="a1539-136">Hora en que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="a1539-136">Time when the event occurred .</span></span>|
|<span data-ttu-id="a1539-137">correlationId</span><span class="sxs-lookup"><span data-stu-id="a1539-137">correlationId</span></span>|<span data-ttu-id="a1539-138">String</span><span class="sxs-lookup"><span data-stu-id="a1539-138">String</span></span>|<span data-ttu-id="a1539-139">Id. utilizado para rastrear el error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="a1539-139">Id used for tracing the failure in the service.</span></span>|



## <a name="response"></a><span data-ttu-id="a1539-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1539-140">Response</span></span>
<span data-ttu-id="a1539-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a1539-141">If successful, this method returns a `201 Created` response code and a [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a1539-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a1539-142">Example</span></span>
### <a name="request"></a><span data-ttu-id="a1539-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a1539-143">Request</span></span>
<span data-ttu-id="a1539-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a1539-144">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="a1539-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1539-145">Response</span></span>
<span data-ttu-id="a1539-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a1539-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




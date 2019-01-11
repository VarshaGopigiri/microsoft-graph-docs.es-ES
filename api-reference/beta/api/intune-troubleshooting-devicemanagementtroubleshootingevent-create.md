---
title: Crear deviceManagementTroubleshootingEvent
description: Cree un objeto deviceManagementTroubleshootingEvent.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 25253b9851c675417801b41692ffaa90a1fe1039
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851782"
---
# <a name="create-devicemanagementtroubleshootingevent"></a><span data-ttu-id="03c2c-103">Crear deviceManagementTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="03c2c-103">Create deviceManagementTroubleshootingEvent</span></span>

> <span data-ttu-id="03c2c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="03c2c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="03c2c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="03c2c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="03c2c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="03c2c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="03c2c-107">Cree un objeto [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="03c2c-107">Create a new [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="03c2c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="03c2c-108">Prerequisites</span></span>
<span data-ttu-id="03c2c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="03c2c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="03c2c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="03c2c-111">Permission type</span></span>|<span data-ttu-id="03c2c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="03c2c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="03c2c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="03c2c-113">Delegated (work or school account)</span></span>|<span data-ttu-id="03c2c-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="03c2c-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="03c2c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="03c2c-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="03c2c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="03c2c-116">Not supported.</span></span>|
|<span data-ttu-id="03c2c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="03c2c-117">Application</span></span>|<span data-ttu-id="03c2c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="03c2c-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="03c2c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="03c2c-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/troubleshootingEvents
```

## <a name="request-headers"></a><span data-ttu-id="03c2c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="03c2c-120">Request headers</span></span>
|<span data-ttu-id="03c2c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03c2c-121">Header</span></span>|<span data-ttu-id="03c2c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="03c2c-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="03c2c-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="03c2c-123">Authorization</span></span>|<span data-ttu-id="03c2c-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="03c2c-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="03c2c-125">Accept</span><span class="sxs-lookup"><span data-stu-id="03c2c-125">Accept</span></span>|<span data-ttu-id="03c2c-126">application/json</span><span class="sxs-lookup"><span data-stu-id="03c2c-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="03c2c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="03c2c-127">Request body</span></span>
<span data-ttu-id="03c2c-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceManagementTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="03c2c-128">In the request body, supply a JSON representation for the deviceManagementTroubleshootingEvent object.</span></span>

<span data-ttu-id="03c2c-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceManagementTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="03c2c-129">The following table shows the properties that are required when you create the deviceManagementTroubleshootingEvent.</span></span>

|<span data-ttu-id="03c2c-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="03c2c-130">Property</span></span>|<span data-ttu-id="03c2c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="03c2c-131">Type</span></span>|<span data-ttu-id="03c2c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="03c2c-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="03c2c-133">id</span><span class="sxs-lookup"><span data-stu-id="03c2c-133">id</span></span>|<span data-ttu-id="03c2c-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="03c2c-134">String</span></span>|<span data-ttu-id="03c2c-135">UUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="03c2c-135">UUID for the object</span></span>|
|<span data-ttu-id="03c2c-136">eventDateTime</span><span class="sxs-lookup"><span data-stu-id="03c2c-136">eventDateTime</span></span>|<span data-ttu-id="03c2c-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="03c2c-137">DateTimeOffset</span></span>|<span data-ttu-id="03c2c-138">Hora en que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="03c2c-138">Time when the event occurred .</span></span>|
|<span data-ttu-id="03c2c-139">correlationId</span><span class="sxs-lookup"><span data-stu-id="03c2c-139">correlationId</span></span>|<span data-ttu-id="03c2c-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="03c2c-140">String</span></span>|<span data-ttu-id="03c2c-141">Id. utilizado para rastrear el error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="03c2c-141">Id used for tracing the failure in the service.</span></span>|



## <a name="response"></a><span data-ttu-id="03c2c-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03c2c-142">Response</span></span>
<span data-ttu-id="03c2c-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03c2c-143">If successful, this method returns a `201 Created` response code and a [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="03c2c-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="03c2c-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="03c2c-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="03c2c-145">Request</span></span>
<span data-ttu-id="03c2c-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="03c2c-146">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/troubleshootingEvents
Content-type: application/json
Content-length: 179

{
  "@odata.type": "#microsoft.graph.deviceManagementTroubleshootingEvent",
  "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
  "correlationId": "Correlation Id value"
}
```

### <a name="response"></a><span data-ttu-id="03c2c-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03c2c-147">Response</span></span>
<span data-ttu-id="03c2c-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="03c2c-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






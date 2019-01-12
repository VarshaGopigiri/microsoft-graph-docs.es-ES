---
title: Crear mobileAppTroubleshootingEvent
description: Crear un nuevo objeto mobileAppTroubleshootingEvent.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 59eea166285f55de32df2728f9bbc834e0eecac8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27978147"
---
# <a name="create-mobileapptroubleshootingevent"></a><span data-ttu-id="aa895-103">Crear mobileAppTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="aa895-103">Create mobileAppTroubleshootingEvent</span></span>

> <span data-ttu-id="aa895-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="aa895-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="aa895-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="aa895-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="aa895-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="aa895-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="aa895-107">Crear un nuevo objeto [mobileAppTroubleshootingEvent](../resources/intune-troubleshooting-mobileapptroubleshootingevent.md) .</span><span class="sxs-lookup"><span data-stu-id="aa895-107">Create a new [mobileAppTroubleshootingEvent](../resources/intune-troubleshooting-mobileapptroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="aa895-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="aa895-108">Prerequisites</span></span>
<span data-ttu-id="aa895-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="aa895-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="aa895-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="aa895-111">Permission type</span></span>|<span data-ttu-id="aa895-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="aa895-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="aa895-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="aa895-113">Delegated (work or school account)</span></span>|<span data-ttu-id="aa895-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="aa895-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="aa895-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="aa895-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="aa895-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aa895-116">Not supported.</span></span>|
|<span data-ttu-id="aa895-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="aa895-117">Application</span></span>|<span data-ttu-id="aa895-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aa895-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="aa895-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aa895-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/mobileAppTroubleshootingEvents
```

## <a name="request-headers"></a><span data-ttu-id="aa895-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="aa895-120">Request headers</span></span>
|<span data-ttu-id="aa895-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa895-121">Header</span></span>|<span data-ttu-id="aa895-122">Valor</span><span class="sxs-lookup"><span data-stu-id="aa895-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="aa895-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="aa895-123">Authorization</span></span>|<span data-ttu-id="aa895-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="aa895-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="aa895-125">Accept</span><span class="sxs-lookup"><span data-stu-id="aa895-125">Accept</span></span>|<span data-ttu-id="aa895-126">application/json</span><span class="sxs-lookup"><span data-stu-id="aa895-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="aa895-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="aa895-127">Request body</span></span>
<span data-ttu-id="aa895-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto mobileAppTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="aa895-128">In the request body, supply a JSON representation for the mobileAppTroubleshootingEvent object.</span></span>

<span data-ttu-id="aa895-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el mobileAppTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="aa895-129">The following table shows the properties that are required when you create the mobileAppTroubleshootingEvent.</span></span>

|<span data-ttu-id="aa895-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aa895-130">Property</span></span>|<span data-ttu-id="aa895-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa895-131">Type</span></span>|<span data-ttu-id="aa895-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa895-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="aa895-133">id</span><span class="sxs-lookup"><span data-stu-id="aa895-133">id</span></span>|<span data-ttu-id="aa895-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="aa895-134">String</span></span>|<span data-ttu-id="aa895-135">UUID del objeto. Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="aa895-135">UUID for the object Inherited from [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="aa895-136">eventDateTime</span><span class="sxs-lookup"><span data-stu-id="aa895-136">eventDateTime</span></span>|<span data-ttu-id="aa895-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="aa895-137">DateTimeOffset</span></span>|<span data-ttu-id="aa895-138">Hora en que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="aa895-138">Time when the event occurred .</span></span> <span data-ttu-id="aa895-139">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="aa895-139">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="aa895-140">correlationId</span><span class="sxs-lookup"><span data-stu-id="aa895-140">correlationId</span></span>|<span data-ttu-id="aa895-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="aa895-141">String</span></span>|<span data-ttu-id="aa895-142">Id. utilizado para rastrear el error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="aa895-142">Id used for tracing the failure in the service.</span></span> <span data-ttu-id="aa895-143">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="aa895-143">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="aa895-144">managedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="aa895-144">managedDeviceIdentifier</span></span>|<span data-ttu-id="aa895-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="aa895-145">String</span></span>|<span data-ttu-id="aa895-146">Identificador del dispositivo creado o recopilado por Intune.</span><span class="sxs-lookup"><span data-stu-id="aa895-146">Device identifier created or collected by Intune.</span></span>|
|<span data-ttu-id="aa895-147">userId</span><span class="sxs-lookup"><span data-stu-id="aa895-147">userId</span></span>|<span data-ttu-id="aa895-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="aa895-148">String</span></span>|<span data-ttu-id="aa895-149">Identificador del usuario que intentó inscribir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa895-149">Identifier for the user that tried to enroll the device.</span></span>|
|<span data-ttu-id="aa895-150">applicationId</span><span class="sxs-lookup"><span data-stu-id="aa895-150">applicationId</span></span>|<span data-ttu-id="aa895-151">cadena</span><span class="sxs-lookup"><span data-stu-id="aa895-151">String</span></span>|<span data-ttu-id="aa895-152">Identificador de la aplicación Intune.</span><span class="sxs-lookup"><span data-stu-id="aa895-152">Intune application identifier.</span></span>|
|<span data-ttu-id="aa895-153">historial de</span><span class="sxs-lookup"><span data-stu-id="aa895-153">history</span></span>|<span data-ttu-id="aa895-154">colección de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="aa895-154">[mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md) collection</span></span>|<span data-ttu-id="aa895-155">Solución de problemas de elemento de historial de aplicación de Mobile Intune</span><span class="sxs-lookup"><span data-stu-id="aa895-155">Intune Mobile Application Troubleshooting History Item</span></span>|



## <a name="response"></a><span data-ttu-id="aa895-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa895-156">Response</span></span>
<span data-ttu-id="aa895-157">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [mobileAppTroubleshootingEvent](../resources/intune-troubleshooting-mobileapptroubleshootingevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aa895-157">If successful, this method returns a `201 Created` response code and a [mobileAppTroubleshootingEvent](../resources/intune-troubleshooting-mobileapptroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="aa895-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa895-158">Example</span></span>
### <a name="request"></a><span data-ttu-id="aa895-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aa895-159">Request</span></span>
<span data-ttu-id="aa895-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="aa895-160">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/users/{usersId}/mobileAppTroubleshootingEvents
Content-type: application/json
Content-length: 489

{
  "@odata.type": "#microsoft.graph.mobileAppTroubleshootingEvent",
  "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
  "correlationId": "Correlation Id value",
  "managedDeviceIdentifier": "Managed Device Identifier value",
  "userId": "User Id value",
  "applicationId": "Application Id value",
  "history": [
    {
      "@odata.type": "microsoft.graph.mobileAppTroubleshootingHistoryItem",
      "occurrenceDateTime": "2017-01-01T00:03:20.8380798-08:00"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="aa895-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa895-161">Response</span></span>
<span data-ttu-id="aa895-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aa895-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 538

{
  "@odata.type": "#microsoft.graph.mobileAppTroubleshootingEvent",
  "id": "77943c10-3c10-7794-103c-9477103c9477",
  "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
  "correlationId": "Correlation Id value",
  "managedDeviceIdentifier": "Managed Device Identifier value",
  "userId": "User Id value",
  "applicationId": "Application Id value",
  "history": [
    {
      "@odata.type": "microsoft.graph.mobileAppTroubleshootingHistoryItem",
      "occurrenceDateTime": "2017-01-01T00:03:20.8380798-08:00"
    }
  ]
}
```






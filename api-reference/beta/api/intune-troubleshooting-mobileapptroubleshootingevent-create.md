---
title: Crear mobileAppTroubleshootingEvent
description: Crear un nuevo objeto mobileAppTroubleshootingEvent.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: bb29e9de5bcebf0d40421280e779f12275ab7274
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27886348"
---
# <a name="create-mobileapptroubleshootingevent"></a><span data-ttu-id="66e65-103">Crear mobileAppTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="66e65-103">Create mobileAppTroubleshootingEvent</span></span>

> <span data-ttu-id="66e65-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="66e65-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="66e65-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="66e65-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="66e65-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="66e65-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="66e65-107">Crear un nuevo objeto [mobileAppTroubleshootingEvent](../resources/intune-troubleshooting-mobileapptroubleshootingevent.md) .</span><span class="sxs-lookup"><span data-stu-id="66e65-107">Create a new [mobileAppTroubleshootingEvent](../resources/intune-troubleshooting-mobileapptroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="66e65-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="66e65-108">Prerequisites</span></span>
<span data-ttu-id="66e65-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="66e65-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="66e65-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="66e65-111">Permission type</span></span>|<span data-ttu-id="66e65-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="66e65-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="66e65-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="66e65-113">Delegated (work or school account)</span></span>|<span data-ttu-id="66e65-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="66e65-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="66e65-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="66e65-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="66e65-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="66e65-116">Not supported.</span></span>|
|<span data-ttu-id="66e65-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="66e65-117">Application</span></span>|<span data-ttu-id="66e65-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="66e65-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="66e65-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="66e65-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/mobileAppTroubleshootingEvents
```

## <a name="request-headers"></a><span data-ttu-id="66e65-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="66e65-120">Request headers</span></span>
|<span data-ttu-id="66e65-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66e65-121">Header</span></span>|<span data-ttu-id="66e65-122">Valor</span><span class="sxs-lookup"><span data-stu-id="66e65-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="66e65-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="66e65-123">Authorization</span></span>|<span data-ttu-id="66e65-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="66e65-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="66e65-125">Accept</span><span class="sxs-lookup"><span data-stu-id="66e65-125">Accept</span></span>|<span data-ttu-id="66e65-126">application/json</span><span class="sxs-lookup"><span data-stu-id="66e65-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="66e65-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="66e65-127">Request body</span></span>
<span data-ttu-id="66e65-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto mobileAppTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="66e65-128">In the request body, supply a JSON representation for the mobileAppTroubleshootingEvent object.</span></span>

<span data-ttu-id="66e65-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el mobileAppTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="66e65-129">The following table shows the properties that are required when you create the mobileAppTroubleshootingEvent.</span></span>

|<span data-ttu-id="66e65-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66e65-130">Property</span></span>|<span data-ttu-id="66e65-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="66e65-131">Type</span></span>|<span data-ttu-id="66e65-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="66e65-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="66e65-133">id</span><span class="sxs-lookup"><span data-stu-id="66e65-133">id</span></span>|<span data-ttu-id="66e65-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="66e65-134">String</span></span>|<span data-ttu-id="66e65-135">UUID del objeto. Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="66e65-135">UUID for the object Inherited from [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="66e65-136">eventDateTime</span><span class="sxs-lookup"><span data-stu-id="66e65-136">eventDateTime</span></span>|<span data-ttu-id="66e65-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="66e65-137">DateTimeOffset</span></span>|<span data-ttu-id="66e65-138">Hora en que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="66e65-138">Time when the event occurred .</span></span> <span data-ttu-id="66e65-139">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="66e65-139">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="66e65-140">correlationId</span><span class="sxs-lookup"><span data-stu-id="66e65-140">correlationId</span></span>|<span data-ttu-id="66e65-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="66e65-141">String</span></span>|<span data-ttu-id="66e65-142">Id. utilizado para rastrear el error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="66e65-142">Id used for tracing the failure in the service.</span></span> <span data-ttu-id="66e65-143">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="66e65-143">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="66e65-144">managedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="66e65-144">managedDeviceIdentifier</span></span>|<span data-ttu-id="66e65-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="66e65-145">String</span></span>|<span data-ttu-id="66e65-146">Identificador del dispositivo creado o recopilado por Intune.</span><span class="sxs-lookup"><span data-stu-id="66e65-146">Device identifier created or collected by Intune.</span></span>|
|<span data-ttu-id="66e65-147">userId</span><span class="sxs-lookup"><span data-stu-id="66e65-147">userId</span></span>|<span data-ttu-id="66e65-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="66e65-148">String</span></span>|<span data-ttu-id="66e65-149">Identificador del usuario que intentó inscribir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66e65-149">Identifier for the user that tried to enroll the device.</span></span>|
|<span data-ttu-id="66e65-150">applicationId</span><span class="sxs-lookup"><span data-stu-id="66e65-150">applicationId</span></span>|<span data-ttu-id="66e65-151">cadena</span><span class="sxs-lookup"><span data-stu-id="66e65-151">String</span></span>|<span data-ttu-id="66e65-152">Identificador de la aplicación Intune.</span><span class="sxs-lookup"><span data-stu-id="66e65-152">Intune application identifier.</span></span>|
|<span data-ttu-id="66e65-153">historial de</span><span class="sxs-lookup"><span data-stu-id="66e65-153">history</span></span>|<span data-ttu-id="66e65-154">colección de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)</span><span class="sxs-lookup"><span data-stu-id="66e65-154">[mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md) collection</span></span>|<span data-ttu-id="66e65-155">Solución de problemas de elemento de historial de aplicación de Mobile Intune</span><span class="sxs-lookup"><span data-stu-id="66e65-155">Intune Mobile Application Troubleshooting History Item</span></span>|



## <a name="response"></a><span data-ttu-id="66e65-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66e65-156">Response</span></span>
<span data-ttu-id="66e65-157">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [mobileAppTroubleshootingEvent](../resources/intune-troubleshooting-mobileapptroubleshootingevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66e65-157">If successful, this method returns a `201 Created` response code and a [mobileAppTroubleshootingEvent](../resources/intune-troubleshooting-mobileapptroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="66e65-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="66e65-158">Example</span></span>
### <a name="request"></a><span data-ttu-id="66e65-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="66e65-159">Request</span></span>
<span data-ttu-id="66e65-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="66e65-160">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="66e65-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66e65-161">Response</span></span>
<span data-ttu-id="66e65-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="66e65-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






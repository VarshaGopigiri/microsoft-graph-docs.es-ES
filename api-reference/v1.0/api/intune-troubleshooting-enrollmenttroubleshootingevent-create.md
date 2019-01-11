---
title: Crear enrollmentTroubleshootingEvent
description: Cree un objeto enrollmentTroubleshootingEvent.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 633e16f1d21808e55dd3b5d8fe677a8b6bec37d2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27869499"
---
# <a name="create-enrollmenttroubleshootingevent"></a><span data-ttu-id="6a5f8-103">Crear enrollmentTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="6a5f8-103">Create enrollmentTroubleshootingEvent</span></span>

> <span data-ttu-id="6a5f8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6a5f8-105">Cree un objeto [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="6a5f8-105">Create a new [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6a5f8-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6a5f8-106">Prerequisites</span></span>
<span data-ttu-id="6a5f8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6a5f8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6a5f8-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6a5f8-109">Permission type</span></span>|<span data-ttu-id="6a5f8-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6a5f8-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6a5f8-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6a5f8-111">Delegated (work or school account)</span></span>|<span data-ttu-id="6a5f8-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6a5f8-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="6a5f8-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6a5f8-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6a5f8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-114">Not supported.</span></span>|
|<span data-ttu-id="6a5f8-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6a5f8-115">Application</span></span>|<span data-ttu-id="6a5f8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6a5f8-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6a5f8-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/troubleshootingEvents
```

## <a name="request-headers"></a><span data-ttu-id="6a5f8-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6a5f8-118">Request headers</span></span>
|<span data-ttu-id="6a5f8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a5f8-119">Header</span></span>|<span data-ttu-id="6a5f8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6a5f8-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6a5f8-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="6a5f8-121">Authorization</span></span>|<span data-ttu-id="6a5f8-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6a5f8-123">Accept</span><span class="sxs-lookup"><span data-stu-id="6a5f8-123">Accept</span></span>|<span data-ttu-id="6a5f8-124">application/json</span><span class="sxs-lookup"><span data-stu-id="6a5f8-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6a5f8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6a5f8-125">Request body</span></span>
<span data-ttu-id="6a5f8-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto enrollmentTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-126">In the request body, supply a JSON representation for the enrollmentTroubleshootingEvent object.</span></span>

<span data-ttu-id="6a5f8-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto enrollmentTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-127">The following table shows the properties that are required when you create the enrollmentTroubleshootingEvent.</span></span>

|<span data-ttu-id="6a5f8-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6a5f8-128">Property</span></span>|<span data-ttu-id="6a5f8-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a5f8-129">Type</span></span>|<span data-ttu-id="6a5f8-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a5f8-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6a5f8-131">id</span><span class="sxs-lookup"><span data-stu-id="6a5f8-131">id</span></span>|<span data-ttu-id="6a5f8-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="6a5f8-132">String</span></span>|<span data-ttu-id="6a5f8-133">UUID del objeto. Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="6a5f8-133">UUID for the object Inherited from [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="6a5f8-134">eventDateTime</span><span class="sxs-lookup"><span data-stu-id="6a5f8-134">eventDateTime</span></span>|<span data-ttu-id="6a5f8-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6a5f8-135">DateTimeOffset</span></span>|<span data-ttu-id="6a5f8-136">Hora en que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-136">Time when the event occurred .</span></span> <span data-ttu-id="6a5f8-137">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="6a5f8-137">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="6a5f8-138">correlationId</span><span class="sxs-lookup"><span data-stu-id="6a5f8-138">correlationId</span></span>|<span data-ttu-id="6a5f8-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="6a5f8-139">String</span></span>|<span data-ttu-id="6a5f8-140">Id. utilizado para rastrear el error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-140">Id used for tracing the failure in the service.</span></span> <span data-ttu-id="6a5f8-141">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="6a5f8-141">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="6a5f8-142">managedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="6a5f8-142">managedDeviceIdentifier</span></span>|<span data-ttu-id="6a5f8-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="6a5f8-143">String</span></span>|<span data-ttu-id="6a5f8-144">Identificador del dispositivo creado o recopilado por Intune.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-144">Device identifier created or collected by Intune.</span></span>|
|<span data-ttu-id="6a5f8-145">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="6a5f8-145">operatingSystem</span></span>|<span data-ttu-id="6a5f8-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="6a5f8-146">String</span></span>|<span data-ttu-id="6a5f8-147">Sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-147">Operating System.</span></span>|
|<span data-ttu-id="6a5f8-148">osVersion</span><span class="sxs-lookup"><span data-stu-id="6a5f8-148">osVersion</span></span>|<span data-ttu-id="6a5f8-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="6a5f8-149">String</span></span>|<span data-ttu-id="6a5f8-150">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-150">OS Version.</span></span>|
|<span data-ttu-id="6a5f8-151">userId</span><span class="sxs-lookup"><span data-stu-id="6a5f8-151">userId</span></span>|<span data-ttu-id="6a5f8-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="6a5f8-152">String</span></span>|<span data-ttu-id="6a5f8-153">Identificador del usuario que intentó inscribir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-153">Identifier for the user that tried to enroll the device.</span></span>|
|<span data-ttu-id="6a5f8-154">deviceId</span><span class="sxs-lookup"><span data-stu-id="6a5f8-154">deviceId</span></span>|<span data-ttu-id="6a5f8-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="6a5f8-155">String</span></span>|<span data-ttu-id="6a5f8-156">Identificador de dispositivo de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-156">Azure AD device identifier.</span></span>|
|<span data-ttu-id="6a5f8-157">enrollmentType</span><span class="sxs-lookup"><span data-stu-id="6a5f8-157">enrollmentType</span></span>|[<span data-ttu-id="6a5f8-158">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="6a5f8-158">deviceEnrollmentType</span></span>](../resources/intune-shared-deviceenrollmenttype.md)|<span data-ttu-id="6a5f8-159">Tipo de la inscripción.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-159">Type of the enrollment.</span></span> <span data-ttu-id="6a5f8-160">Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-160">Possible values are: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`.</span></span>|
|<span data-ttu-id="6a5f8-161">failureCategory</span><span class="sxs-lookup"><span data-stu-id="6a5f8-161">failureCategory</span></span>|[<span data-ttu-id="6a5f8-162">deviceEnrollmentFailureReason</span><span class="sxs-lookup"><span data-stu-id="6a5f8-162">deviceEnrollmentFailureReason</span></span>](../resources/intune-troubleshooting-deviceenrollmentfailurereason.md)|<span data-ttu-id="6a5f8-163">Categoría general del error.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-163">Highlevel failure category.</span></span> <span data-ttu-id="6a5f8-164">Los valores posibles son: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced`, `clientDisconnected` y `userAbandonment`.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-164">Possible values are: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced`, `clientDisconnected`, `userAbandonment`.</span></span>|
|<span data-ttu-id="6a5f8-165">failureReason</span><span class="sxs-lookup"><span data-stu-id="6a5f8-165">failureReason</span></span>|<span data-ttu-id="6a5f8-166">Cadena</span><span class="sxs-lookup"><span data-stu-id="6a5f8-166">String</span></span>|<span data-ttu-id="6a5f8-167">Motivo del error detallado.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-167">Detailed failure reason.</span></span>|



## <a name="response"></a><span data-ttu-id="6a5f8-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6a5f8-168">Response</span></span>
<span data-ttu-id="6a5f8-169">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-169">If successful, this method returns a `201 Created` response code and a [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6a5f8-170">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6a5f8-170">Example</span></span>
### <a name="request"></a><span data-ttu-id="6a5f8-171">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6a5f8-171">Request</span></span>
<span data-ttu-id="6a5f8-172">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-172">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/troubleshootingEvents
Content-type: application/json
Content-length: 509

{
  "@odata.type": "#microsoft.graph.enrollmentTroubleshootingEvent",
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
```

### <a name="response"></a><span data-ttu-id="6a5f8-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6a5f8-173">Response</span></span>
<span data-ttu-id="6a5f8-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6a5f8-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 558

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
```




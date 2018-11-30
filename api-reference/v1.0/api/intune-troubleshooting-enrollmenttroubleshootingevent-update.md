---
title: Actualizar enrollmentTroubleshootingEvent
description: Actualice las propiedades de un objeto enrollmentTroubleshootingEvent.
ms.openlocfilehash: 3479c939e9dca2027a2a296c24b7ae8d00d1c597
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029054"
---
# <a name="update-enrollmenttroubleshootingevent"></a><span data-ttu-id="2faa7-103">Actualizar enrollmentTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="2faa7-103">Update enrollmentTroubleshootingEvent</span></span>

> <span data-ttu-id="2faa7-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2faa7-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2faa7-105">Actualice las propiedades de un objeto [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="2faa7-105">Update the properties of a [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2faa7-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2faa7-106">Prerequisites</span></span>
<span data-ttu-id="2faa7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2faa7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2faa7-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2faa7-109">Permission type</span></span>|<span data-ttu-id="2faa7-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2faa7-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2faa7-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2faa7-111">Delegated (work or school account)</span></span>|<span data-ttu-id="2faa7-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2faa7-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="2faa7-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2faa7-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2faa7-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2faa7-114">Not supported.</span></span>|
|<span data-ttu-id="2faa7-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2faa7-115">Application</span></span>|<span data-ttu-id="2faa7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2faa7-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2faa7-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2faa7-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
```

## <a name="request-headers"></a><span data-ttu-id="2faa7-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2faa7-118">Request headers</span></span>
|<span data-ttu-id="2faa7-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2faa7-119">Header</span></span>|<span data-ttu-id="2faa7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2faa7-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2faa7-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="2faa7-121">Authorization</span></span>|<span data-ttu-id="2faa7-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2faa7-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2faa7-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2faa7-123">Accept</span></span>|<span data-ttu-id="2faa7-124">application/json</span><span class="sxs-lookup"><span data-stu-id="2faa7-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2faa7-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2faa7-125">Request body</span></span>
<span data-ttu-id="2faa7-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="2faa7-126">In the request body, supply a JSON representation for the [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md) object.</span></span>

<span data-ttu-id="2faa7-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="2faa7-127">The following table shows the properties that are required when you create the [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md).</span></span>

|<span data-ttu-id="2faa7-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2faa7-128">Property</span></span>|<span data-ttu-id="2faa7-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="2faa7-129">Type</span></span>|<span data-ttu-id="2faa7-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="2faa7-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2faa7-131">id</span><span class="sxs-lookup"><span data-stu-id="2faa7-131">id</span></span>|<span data-ttu-id="2faa7-132">String</span><span class="sxs-lookup"><span data-stu-id="2faa7-132">String</span></span>|<span data-ttu-id="2faa7-133">UUID del objeto. Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="2faa7-133">UUID for the object Inherited from [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="2faa7-134">eventDateTime</span><span class="sxs-lookup"><span data-stu-id="2faa7-134">eventDateTime</span></span>|<span data-ttu-id="2faa7-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2faa7-135">DateTimeOffset</span></span>|<span data-ttu-id="2faa7-136">Hora en que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="2faa7-136">Time when the event occurred .</span></span> <span data-ttu-id="2faa7-137">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="2faa7-137">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="2faa7-138">correlationId</span><span class="sxs-lookup"><span data-stu-id="2faa7-138">correlationId</span></span>|<span data-ttu-id="2faa7-139">String</span><span class="sxs-lookup"><span data-stu-id="2faa7-139">String</span></span>|<span data-ttu-id="2faa7-140">Id. utilizado para rastrear el error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="2faa7-140">Id used for tracing the failure in the service.</span></span> <span data-ttu-id="2faa7-141">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="2faa7-141">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="2faa7-142">managedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="2faa7-142">managedDeviceIdentifier</span></span>|<span data-ttu-id="2faa7-143">String</span><span class="sxs-lookup"><span data-stu-id="2faa7-143">String</span></span>|<span data-ttu-id="2faa7-144">Identificador del dispositivo creado o recopilado por Intune.</span><span class="sxs-lookup"><span data-stu-id="2faa7-144">Device identifier created or collected by Intune.</span></span>|
|<span data-ttu-id="2faa7-145">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="2faa7-145">operatingSystem</span></span>|<span data-ttu-id="2faa7-146">String</span><span class="sxs-lookup"><span data-stu-id="2faa7-146">String</span></span>|<span data-ttu-id="2faa7-147">Sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2faa7-147">Operating System.</span></span>|
|<span data-ttu-id="2faa7-148">osVersion</span><span class="sxs-lookup"><span data-stu-id="2faa7-148">osVersion</span></span>|<span data-ttu-id="2faa7-149">String</span><span class="sxs-lookup"><span data-stu-id="2faa7-149">String</span></span>|<span data-ttu-id="2faa7-150">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2faa7-150">OS Version.</span></span>|
|<span data-ttu-id="2faa7-151">userId</span><span class="sxs-lookup"><span data-stu-id="2faa7-151">userId</span></span>|<span data-ttu-id="2faa7-152">String</span><span class="sxs-lookup"><span data-stu-id="2faa7-152">String</span></span>|<span data-ttu-id="2faa7-153">Identificador del usuario que intentó inscribir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2faa7-153">Identifier for the user that tried to enroll the device.</span></span>|
|<span data-ttu-id="2faa7-154">deviceId</span><span class="sxs-lookup"><span data-stu-id="2faa7-154">deviceId</span></span>|<span data-ttu-id="2faa7-155">String</span><span class="sxs-lookup"><span data-stu-id="2faa7-155">String</span></span>|<span data-ttu-id="2faa7-156">Identificador de dispositivo de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2faa7-156">Azure AD device identifier.</span></span>|
|<span data-ttu-id="2faa7-157">enrollmentType</span><span class="sxs-lookup"><span data-stu-id="2faa7-157">enrollmentType</span></span>|[<span data-ttu-id="2faa7-158">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="2faa7-158">deviceEnrollmentType</span></span>](../resources/intune-shared-deviceenrollmenttype.md)|<span data-ttu-id="2faa7-159">Tipo de la inscripción.</span><span class="sxs-lookup"><span data-stu-id="2faa7-159">Type of the enrollment.</span></span> <span data-ttu-id="2faa7-160">Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.</span><span class="sxs-lookup"><span data-stu-id="2faa7-160">Possible values are: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`.</span></span>|
|<span data-ttu-id="2faa7-161">failureCategory</span><span class="sxs-lookup"><span data-stu-id="2faa7-161">failureCategory</span></span>|[<span data-ttu-id="2faa7-162">deviceEnrollmentFailureReason</span><span class="sxs-lookup"><span data-stu-id="2faa7-162">deviceEnrollmentFailureReason</span></span>](../resources/intune-troubleshooting-deviceenrollmentfailurereason.md)|<span data-ttu-id="2faa7-163">Categoría general del error.</span><span class="sxs-lookup"><span data-stu-id="2faa7-163">Highlevel failure category.</span></span> <span data-ttu-id="2faa7-164">Los valores posibles son: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced`, `clientDisconnected` y `userAbandonment`.</span><span class="sxs-lookup"><span data-stu-id="2faa7-164">Possible values are: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced`, `clientDisconnected`, `userAbandonment`.</span></span>|
|<span data-ttu-id="2faa7-165">failureReason</span><span class="sxs-lookup"><span data-stu-id="2faa7-165">failureReason</span></span>|<span data-ttu-id="2faa7-166">String</span><span class="sxs-lookup"><span data-stu-id="2faa7-166">String</span></span>|<span data-ttu-id="2faa7-167">Motivo del error detallado.</span><span class="sxs-lookup"><span data-stu-id="2faa7-167">Detailed failure reason.</span></span>|



## <a name="response"></a><span data-ttu-id="2faa7-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2faa7-168">Response</span></span>
<span data-ttu-id="2faa7-169">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2faa7-169">If successful, this method returns a `200 OK` response code and an updated [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2faa7-170">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2faa7-170">Example</span></span>
### <a name="request"></a><span data-ttu-id="2faa7-171">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2faa7-171">Request</span></span>
<span data-ttu-id="2faa7-172">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2faa7-172">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
Content-type: application/json
Content-length: 440

{
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

### <a name="response"></a><span data-ttu-id="2faa7-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2faa7-173">Response</span></span>
<span data-ttu-id="2faa7-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2faa7-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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




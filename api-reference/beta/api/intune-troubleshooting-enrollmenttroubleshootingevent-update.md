---
title: Actualizar enrollmentTroubleshootingEvent
description: Actualice las propiedades de un objeto enrollmentTroubleshootingEvent.
ms.openlocfilehash: 1020b3605a80c0bca995efab4cb173dfa12856cb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090860"
---
# <a name="update-enrollmenttroubleshootingevent"></a><span data-ttu-id="8b7bd-103">Actualizar enrollmentTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="8b7bd-103">Update enrollmentTroubleshootingEvent</span></span>

> <span data-ttu-id="8b7bd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8b7bd-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8b7bd-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8b7bd-107">Actualice las propiedades de un objeto [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="8b7bd-107">Update the properties of a [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8b7bd-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8b7bd-108">Prerequisites</span></span>
<span data-ttu-id="8b7bd-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8b7bd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8b7bd-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8b7bd-111">Permission type</span></span>|<span data-ttu-id="8b7bd-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8b7bd-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8b7bd-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8b7bd-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8b7bd-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8b7bd-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="8b7bd-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8b7bd-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8b7bd-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-116">Not supported.</span></span>|
|<span data-ttu-id="8b7bd-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8b7bd-117">Application</span></span>|<span data-ttu-id="8b7bd-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8b7bd-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8b7bd-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
```

## <a name="request-headers"></a><span data-ttu-id="8b7bd-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8b7bd-120">Request headers</span></span>
|<span data-ttu-id="8b7bd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b7bd-121">Header</span></span>|<span data-ttu-id="8b7bd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8b7bd-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8b7bd-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="8b7bd-123">Authorization</span></span>|<span data-ttu-id="8b7bd-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8b7bd-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8b7bd-125">Accept</span></span>|<span data-ttu-id="8b7bd-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8b7bd-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8b7bd-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8b7bd-127">Request body</span></span>
<span data-ttu-id="8b7bd-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="8b7bd-128">In the request body, supply a JSON representation for the [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md) object.</span></span>

<span data-ttu-id="8b7bd-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="8b7bd-129">The following table shows the properties that are required when you create the [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md).</span></span>

|<span data-ttu-id="8b7bd-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8b7bd-130">Property</span></span>|<span data-ttu-id="8b7bd-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8b7bd-131">Type</span></span>|<span data-ttu-id="8b7bd-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b7bd-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8b7bd-133">id</span><span class="sxs-lookup"><span data-stu-id="8b7bd-133">id</span></span>|<span data-ttu-id="8b7bd-134">String</span><span class="sxs-lookup"><span data-stu-id="8b7bd-134">String</span></span>|<span data-ttu-id="8b7bd-135">UUID del objeto. Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="8b7bd-135">UUID for the object Inherited from [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="8b7bd-136">eventDateTime</span><span class="sxs-lookup"><span data-stu-id="8b7bd-136">eventDateTime</span></span>|<span data-ttu-id="8b7bd-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8b7bd-137">DateTimeOffset</span></span>|<span data-ttu-id="8b7bd-138">Hora en que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-138">Time when the event occurred .</span></span> <span data-ttu-id="8b7bd-139">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="8b7bd-139">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="8b7bd-140">correlationId</span><span class="sxs-lookup"><span data-stu-id="8b7bd-140">correlationId</span></span>|<span data-ttu-id="8b7bd-141">String</span><span class="sxs-lookup"><span data-stu-id="8b7bd-141">String</span></span>|<span data-ttu-id="8b7bd-142">Id. utilizado para rastrear el error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-142">Id used for tracing the failure in the service.</span></span> <span data-ttu-id="8b7bd-143">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="8b7bd-143">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="8b7bd-144">managedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="8b7bd-144">managedDeviceIdentifier</span></span>|<span data-ttu-id="8b7bd-145">String</span><span class="sxs-lookup"><span data-stu-id="8b7bd-145">String</span></span>|<span data-ttu-id="8b7bd-146">Identificador del dispositivo creado o recopilado por Intune.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-146">Device identifier created or collected by Intune.</span></span>|
|<span data-ttu-id="8b7bd-147">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="8b7bd-147">operatingSystem</span></span>|<span data-ttu-id="8b7bd-148">String</span><span class="sxs-lookup"><span data-stu-id="8b7bd-148">String</span></span>|<span data-ttu-id="8b7bd-149">Sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-149">Operating System.</span></span>|
|<span data-ttu-id="8b7bd-150">osVersion</span><span class="sxs-lookup"><span data-stu-id="8b7bd-150">osVersion</span></span>|<span data-ttu-id="8b7bd-151">String</span><span class="sxs-lookup"><span data-stu-id="8b7bd-151">String</span></span>|<span data-ttu-id="8b7bd-152">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-152">OS Version.</span></span>|
|<span data-ttu-id="8b7bd-153">userId</span><span class="sxs-lookup"><span data-stu-id="8b7bd-153">userId</span></span>|<span data-ttu-id="8b7bd-154">String</span><span class="sxs-lookup"><span data-stu-id="8b7bd-154">String</span></span>|<span data-ttu-id="8b7bd-155">Identificador del usuario que intentó inscribir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-155">Identifier for the user that tried to enroll the device.</span></span>|
|<span data-ttu-id="8b7bd-156">deviceId</span><span class="sxs-lookup"><span data-stu-id="8b7bd-156">deviceId</span></span>|<span data-ttu-id="8b7bd-157">String</span><span class="sxs-lookup"><span data-stu-id="8b7bd-157">String</span></span>|<span data-ttu-id="8b7bd-158">Identificador de dispositivo de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-158">Azure AD device identifier.</span></span>|
|<span data-ttu-id="8b7bd-159">enrollmentType</span><span class="sxs-lookup"><span data-stu-id="8b7bd-159">enrollmentType</span></span>|[<span data-ttu-id="8b7bd-160">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="8b7bd-160">deviceEnrollmentType</span></span>](../resources/intune-shared-deviceenrollmenttype.md)|<span data-ttu-id="8b7bd-161">Tipo de la inscripción.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-161">Type of the enrollment.</span></span> <span data-ttu-id="8b7bd-162">Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-162">Possible values are: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`.</span></span>|
|<span data-ttu-id="8b7bd-163">failureCategory</span><span class="sxs-lookup"><span data-stu-id="8b7bd-163">failureCategory</span></span>|[<span data-ttu-id="8b7bd-164">deviceEnrollmentFailureReason</span><span class="sxs-lookup"><span data-stu-id="8b7bd-164">deviceEnrollmentFailureReason</span></span>](../resources/intune-troubleshooting-deviceenrollmentfailurereason.md)|<span data-ttu-id="8b7bd-165">Categoría general del error.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-165">Highlevel failure category.</span></span> <span data-ttu-id="8b7bd-166">Los valores posibles son: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced`, `clientDisconnected` y `userAbandonment`.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-166">Possible values are: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced`, `clientDisconnected`, `userAbandonment`.</span></span>|
|<span data-ttu-id="8b7bd-167">failureReason</span><span class="sxs-lookup"><span data-stu-id="8b7bd-167">failureReason</span></span>|<span data-ttu-id="8b7bd-168">String</span><span class="sxs-lookup"><span data-stu-id="8b7bd-168">String</span></span>|<span data-ttu-id="8b7bd-169">Motivo del error detallado.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-169">Detailed failure reason.</span></span>|



## <a name="response"></a><span data-ttu-id="8b7bd-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8b7bd-170">Response</span></span>
<span data-ttu-id="8b7bd-171">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-171">If successful, this method returns a `200 OK` response code and an updated [enrollmentTroubleshootingEvent](../resources/intune-troubleshooting-enrollmenttroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8b7bd-172">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8b7bd-172">Example</span></span>
### <a name="request"></a><span data-ttu-id="8b7bd-173">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8b7bd-173">Request</span></span>
<span data-ttu-id="8b7bd-174">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-174">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
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

### <a name="response"></a><span data-ttu-id="8b7bd-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8b7bd-175">Response</span></span>
<span data-ttu-id="8b7bd-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





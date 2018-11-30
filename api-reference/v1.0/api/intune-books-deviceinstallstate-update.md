---
title: Actualizar deviceInstallState
description: Actualice las propiedades de un objeto deviceInstallState.
ms.openlocfilehash: aa826b8db510d174d6b1a1ff2f092498a4d1fe7c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029189"
---
# <a name="update-deviceinstallstate"></a><span data-ttu-id="e23ce-103">Actualizar deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="e23ce-103">Update deviceInstallState</span></span>

> <span data-ttu-id="e23ce-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e23ce-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e23ce-105">Actualice las propiedades de un objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="e23ce-105">Update the properties of a [deviceInstallState](../resources/intune-books-deviceinstallstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e23ce-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e23ce-106">Prerequisites</span></span>
<span data-ttu-id="e23ce-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e23ce-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e23ce-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e23ce-109">Permission type</span></span>|<span data-ttu-id="e23ce-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e23ce-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e23ce-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e23ce-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e23ce-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e23ce-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="e23ce-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e23ce-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e23ce-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e23ce-114">Not supported.</span></span>|
|<span data-ttu-id="e23ce-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e23ce-115">Application</span></span>|<span data-ttu-id="e23ce-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e23ce-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e23ce-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e23ce-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates/{deviceInstallStateId}
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary/{userInstallStateSummaryId}/deviceStates/{deviceInstallStateId}
```

## <a name="request-headers"></a><span data-ttu-id="e23ce-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e23ce-118">Request headers</span></span>
|<span data-ttu-id="e23ce-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e23ce-119">Header</span></span>|<span data-ttu-id="e23ce-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e23ce-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e23ce-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="e23ce-121">Authorization</span></span>|<span data-ttu-id="e23ce-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e23ce-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e23ce-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e23ce-123">Accept</span></span>|<span data-ttu-id="e23ce-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e23ce-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e23ce-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e23ce-125">Request body</span></span>
<span data-ttu-id="e23ce-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="e23ce-126">In the request body, supply a JSON representation for the [deviceInstallState](../resources/intune-books-deviceinstallstate.md) object.</span></span>

<span data-ttu-id="e23ce-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="e23ce-127">The following table shows the properties that are required when you create the [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span></span>

|<span data-ttu-id="e23ce-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e23ce-128">Property</span></span>|<span data-ttu-id="e23ce-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="e23ce-129">Type</span></span>|<span data-ttu-id="e23ce-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="e23ce-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e23ce-131">id</span><span class="sxs-lookup"><span data-stu-id="e23ce-131">id</span></span>|<span data-ttu-id="e23ce-132">String</span><span class="sxs-lookup"><span data-stu-id="e23ce-132">String</span></span>|<span data-ttu-id="e23ce-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e23ce-133">Key of the entity.</span></span>|
|<span data-ttu-id="e23ce-134">deviceName</span><span class="sxs-lookup"><span data-stu-id="e23ce-134">deviceName</span></span>|<span data-ttu-id="e23ce-135">String</span><span class="sxs-lookup"><span data-stu-id="e23ce-135">String</span></span>|<span data-ttu-id="e23ce-136">Nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e23ce-136">Device name.</span></span>|
|<span data-ttu-id="e23ce-137">deviceId</span><span class="sxs-lookup"><span data-stu-id="e23ce-137">deviceId</span></span>|<span data-ttu-id="e23ce-138">String</span><span class="sxs-lookup"><span data-stu-id="e23ce-138">String</span></span>|<span data-ttu-id="e23ce-139">Id. del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e23ce-139">Device Id.</span></span>|
|<span data-ttu-id="e23ce-140">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="e23ce-140">lastSyncDateTime</span></span>|<span data-ttu-id="e23ce-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e23ce-141">DateTimeOffset</span></span>|<span data-ttu-id="e23ce-142">Fecha y hora de la última sincronización.</span><span class="sxs-lookup"><span data-stu-id="e23ce-142">Last sync date and time.</span></span>|
|<span data-ttu-id="e23ce-143">installState</span><span class="sxs-lookup"><span data-stu-id="e23ce-143">installState</span></span>|[<span data-ttu-id="e23ce-144">installState</span><span class="sxs-lookup"><span data-stu-id="e23ce-144">installState</span></span>](../resources/intune-books-installstate.md)|<span data-ttu-id="e23ce-145">El estado de instalación del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="e23ce-145">The install state of the eBook.</span></span> <span data-ttu-id="e23ce-146">Los valores posibles son: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed` y `unknown`.</span><span class="sxs-lookup"><span data-stu-id="e23ce-146">Possible values are: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed`, `unknown`.</span></span>|
|<span data-ttu-id="e23ce-147">errorCode</span><span class="sxs-lookup"><span data-stu-id="e23ce-147">errorCode</span></span>|<span data-ttu-id="e23ce-148">String</span><span class="sxs-lookup"><span data-stu-id="e23ce-148">String</span></span>|<span data-ttu-id="e23ce-149">El código de error si hay errores de instalación.</span><span class="sxs-lookup"><span data-stu-id="e23ce-149">The error code for install failures.</span></span>|
|<span data-ttu-id="e23ce-150">osVersion</span><span class="sxs-lookup"><span data-stu-id="e23ce-150">osVersion</span></span>|<span data-ttu-id="e23ce-151">String</span><span class="sxs-lookup"><span data-stu-id="e23ce-151">String</span></span>|<span data-ttu-id="e23ce-152">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e23ce-152">OS Version.</span></span>|
|<span data-ttu-id="e23ce-153">osDescription</span><span class="sxs-lookup"><span data-stu-id="e23ce-153">osDescription</span></span>|<span data-ttu-id="e23ce-154">String</span><span class="sxs-lookup"><span data-stu-id="e23ce-154">String</span></span>|<span data-ttu-id="e23ce-155">Descripción del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e23ce-155">OS Description.</span></span>|
|<span data-ttu-id="e23ce-156">userName</span><span class="sxs-lookup"><span data-stu-id="e23ce-156">userName</span></span>|<span data-ttu-id="e23ce-157">String</span><span class="sxs-lookup"><span data-stu-id="e23ce-157">String</span></span>|<span data-ttu-id="e23ce-158">Nombre de usuario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e23ce-158">Device User Name.</span></span>|



## <a name="response"></a><span data-ttu-id="e23ce-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e23ce-159">Response</span></span>
<span data-ttu-id="e23ce-160">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e23ce-160">If successful, this method returns a `200 OK` response code and an updated [deviceInstallState](../resources/intune-books-deviceinstallstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e23ce-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e23ce-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="e23ce-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e23ce-162">Request</span></span>
<span data-ttu-id="e23ce-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e23ce-163">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates/{deviceInstallStateId}
Content-type: application/json
Content-length: 374

{
  "@odata.type": "#microsoft.graph.deviceInstallState",
  "deviceName": "Device Name value",
  "deviceId": "Device Id value",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "installState": "installed",
  "errorCode": "Error Code value",
  "osVersion": "Os Version value",
  "osDescription": "Os Description value",
  "userName": "User Name value"
}
```

### <a name="response"></a><span data-ttu-id="e23ce-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e23ce-164">Response</span></span>
<span data-ttu-id="e23ce-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e23ce-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 423

{
  "@odata.type": "#microsoft.graph.deviceInstallState",
  "id": "b9feb68f-b68f-b9fe-8fb6-feb98fb6feb9",
  "deviceName": "Device Name value",
  "deviceId": "Device Id value",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "installState": "installed",
  "errorCode": "Error Code value",
  "osVersion": "Os Version value",
  "osDescription": "Os Description value",
  "userName": "User Name value"
}
```




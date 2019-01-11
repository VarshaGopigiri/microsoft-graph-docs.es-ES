---
title: Crear deviceInstallState
description: Cree un objeto deviceInstallState.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 49979b883ffef895124d8bb57837d5c5103a0d67
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825483"
---
# <a name="create-deviceinstallstate"></a><span data-ttu-id="cbea8-103">Crear deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="cbea8-103">Create deviceInstallState</span></span>

> <span data-ttu-id="cbea8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cbea8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cbea8-105">Cree un objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="cbea8-105">Create a new [deviceInstallState](../resources/intune-books-deviceinstallstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cbea8-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cbea8-106">Prerequisites</span></span>
<span data-ttu-id="cbea8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cbea8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cbea8-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cbea8-109">Permission type</span></span>|<span data-ttu-id="cbea8-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cbea8-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cbea8-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cbea8-111">Delegated (work or school account)</span></span>|<span data-ttu-id="cbea8-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cbea8-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="cbea8-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cbea8-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cbea8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cbea8-114">Not supported.</span></span>|
|<span data-ttu-id="cbea8-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cbea8-115">Application</span></span>|<span data-ttu-id="cbea8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cbea8-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cbea8-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cbea8-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates
POST /deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary/{userInstallStateSummaryId}/deviceStates
```

## <a name="request-headers"></a><span data-ttu-id="cbea8-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cbea8-118">Request headers</span></span>
|<span data-ttu-id="cbea8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cbea8-119">Header</span></span>|<span data-ttu-id="cbea8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cbea8-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cbea8-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="cbea8-121">Authorization</span></span>|<span data-ttu-id="cbea8-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cbea8-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cbea8-123">Accept</span><span class="sxs-lookup"><span data-stu-id="cbea8-123">Accept</span></span>|<span data-ttu-id="cbea8-124">application/json</span><span class="sxs-lookup"><span data-stu-id="cbea8-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cbea8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cbea8-125">Request body</span></span>
<span data-ttu-id="cbea8-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceInstallState.</span><span class="sxs-lookup"><span data-stu-id="cbea8-126">In the request body, supply a JSON representation for the deviceInstallState object.</span></span>

<span data-ttu-id="cbea8-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceInstallState.</span><span class="sxs-lookup"><span data-stu-id="cbea8-127">The following table shows the properties that are required when you create the deviceInstallState.</span></span>

|<span data-ttu-id="cbea8-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cbea8-128">Property</span></span>|<span data-ttu-id="cbea8-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbea8-129">Type</span></span>|<span data-ttu-id="cbea8-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbea8-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cbea8-131">id</span><span class="sxs-lookup"><span data-stu-id="cbea8-131">id</span></span>|<span data-ttu-id="cbea8-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="cbea8-132">String</span></span>|<span data-ttu-id="cbea8-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="cbea8-133">Key of the entity.</span></span>|
|<span data-ttu-id="cbea8-134">deviceName</span><span class="sxs-lookup"><span data-stu-id="cbea8-134">deviceName</span></span>|<span data-ttu-id="cbea8-135">String</span><span class="sxs-lookup"><span data-stu-id="cbea8-135">String</span></span>|<span data-ttu-id="cbea8-136">Nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cbea8-136">Device name.</span></span>|
|<span data-ttu-id="cbea8-137">deviceId</span><span class="sxs-lookup"><span data-stu-id="cbea8-137">deviceId</span></span>|<span data-ttu-id="cbea8-138">String</span><span class="sxs-lookup"><span data-stu-id="cbea8-138">String</span></span>|<span data-ttu-id="cbea8-139">Id. del dispositivo</span><span class="sxs-lookup"><span data-stu-id="cbea8-139">Device Id.</span></span>|
|<span data-ttu-id="cbea8-140">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="cbea8-140">lastSyncDateTime</span></span>|<span data-ttu-id="cbea8-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cbea8-141">DateTimeOffset</span></span>|<span data-ttu-id="cbea8-142">Fecha y hora de la última sincronización.</span><span class="sxs-lookup"><span data-stu-id="cbea8-142">Last sync date and time.</span></span>|
|<span data-ttu-id="cbea8-143">installState</span><span class="sxs-lookup"><span data-stu-id="cbea8-143">installState</span></span>|[<span data-ttu-id="cbea8-144">installState</span><span class="sxs-lookup"><span data-stu-id="cbea8-144">installState</span></span>](../resources/intune-books-installstate.md)|<span data-ttu-id="cbea8-145">El estado de instalación del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="cbea8-145">The install state of the eBook.</span></span> <span data-ttu-id="cbea8-146">Los valores posibles son: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed` y `unknown`.</span><span class="sxs-lookup"><span data-stu-id="cbea8-146">Possible values are: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed`, `unknown`.</span></span>|
|<span data-ttu-id="cbea8-147">errorCode</span><span class="sxs-lookup"><span data-stu-id="cbea8-147">errorCode</span></span>|<span data-ttu-id="cbea8-148">String</span><span class="sxs-lookup"><span data-stu-id="cbea8-148">String</span></span>|<span data-ttu-id="cbea8-149">El código de error si hay errores de instalación.</span><span class="sxs-lookup"><span data-stu-id="cbea8-149">The error code for install failures.</span></span>|
|<span data-ttu-id="cbea8-150">osVersion</span><span class="sxs-lookup"><span data-stu-id="cbea8-150">osVersion</span></span>|<span data-ttu-id="cbea8-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="cbea8-151">String</span></span>|<span data-ttu-id="cbea8-152">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cbea8-152">OS Version.</span></span>|
|<span data-ttu-id="cbea8-153">osDescription</span><span class="sxs-lookup"><span data-stu-id="cbea8-153">osDescription</span></span>|<span data-ttu-id="cbea8-154">String</span><span class="sxs-lookup"><span data-stu-id="cbea8-154">String</span></span>|<span data-ttu-id="cbea8-155">Descripción del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cbea8-155">OS Description.</span></span>|
|<span data-ttu-id="cbea8-156">userName</span><span class="sxs-lookup"><span data-stu-id="cbea8-156">userName</span></span>|<span data-ttu-id="cbea8-157">String</span><span class="sxs-lookup"><span data-stu-id="cbea8-157">String</span></span>|<span data-ttu-id="cbea8-158">Nombre de usuario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cbea8-158">Device User Name.</span></span>|



## <a name="response"></a><span data-ttu-id="cbea8-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cbea8-159">Response</span></span>
<span data-ttu-id="cbea8-160">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cbea8-160">If successful, this method returns a `201 Created` response code and a [deviceInstallState](../resources/intune-books-deviceinstallstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cbea8-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cbea8-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="cbea8-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cbea8-162">Request</span></span>
<span data-ttu-id="cbea8-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cbea8-163">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates
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

### <a name="response"></a><span data-ttu-id="cbea8-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cbea8-164">Response</span></span>
<span data-ttu-id="cbea8-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cbea8-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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




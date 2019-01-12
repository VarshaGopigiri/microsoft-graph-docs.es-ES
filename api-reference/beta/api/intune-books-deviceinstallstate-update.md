---
title: Actualizar deviceInstallState
description: Actualice las propiedades de un objeto deviceInstallState.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 65569fbe609b8404d7e55ad6de452e30d3bd1cbf
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939703"
---
# <a name="update-deviceinstallstate"></a><span data-ttu-id="d2efb-103">Actualizar deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="d2efb-103">Update deviceInstallState</span></span>

> <span data-ttu-id="d2efb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d2efb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d2efb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d2efb-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d2efb-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d2efb-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d2efb-107">Actualice las propiedades de un objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="d2efb-107">Update the properties of a [deviceInstallState](../resources/intune-books-deviceinstallstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d2efb-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d2efb-108">Prerequisites</span></span>
<span data-ttu-id="d2efb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d2efb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d2efb-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2efb-111">Permission type</span></span>|<span data-ttu-id="d2efb-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2efb-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d2efb-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2efb-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d2efb-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d2efb-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="d2efb-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2efb-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d2efb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2efb-116">Not supported.</span></span>|
|<span data-ttu-id="d2efb-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2efb-117">Application</span></span>|<span data-ttu-id="d2efb-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2efb-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d2efb-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2efb-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates/{deviceInstallStateId}
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary/{userInstallStateSummaryId}/deviceStates/{deviceInstallStateId}
```

## <a name="request-headers"></a><span data-ttu-id="d2efb-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2efb-120">Request headers</span></span>
|<span data-ttu-id="d2efb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2efb-121">Header</span></span>|<span data-ttu-id="d2efb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d2efb-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d2efb-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="d2efb-123">Authorization</span></span>|<span data-ttu-id="d2efb-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d2efb-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d2efb-125">Accept</span><span class="sxs-lookup"><span data-stu-id="d2efb-125">Accept</span></span>|<span data-ttu-id="d2efb-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d2efb-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d2efb-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2efb-127">Request body</span></span>
<span data-ttu-id="d2efb-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="d2efb-128">In the request body, supply a JSON representation for the [deviceInstallState](../resources/intune-books-deviceinstallstate.md) object.</span></span>

<span data-ttu-id="d2efb-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="d2efb-129">The following table shows the properties that are required when you create the [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span></span>

|<span data-ttu-id="d2efb-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2efb-130">Property</span></span>|<span data-ttu-id="d2efb-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2efb-131">Type</span></span>|<span data-ttu-id="d2efb-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2efb-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d2efb-133">id</span><span class="sxs-lookup"><span data-stu-id="d2efb-133">id</span></span>|<span data-ttu-id="d2efb-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2efb-134">String</span></span>|<span data-ttu-id="d2efb-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d2efb-135">Key of the entity.</span></span>|
|<span data-ttu-id="d2efb-136">deviceName</span><span class="sxs-lookup"><span data-stu-id="d2efb-136">deviceName</span></span>|<span data-ttu-id="d2efb-137">String</span><span class="sxs-lookup"><span data-stu-id="d2efb-137">String</span></span>|<span data-ttu-id="d2efb-138">Nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2efb-138">Device name.</span></span>|
|<span data-ttu-id="d2efb-139">deviceId</span><span class="sxs-lookup"><span data-stu-id="d2efb-139">deviceId</span></span>|<span data-ttu-id="d2efb-140">String</span><span class="sxs-lookup"><span data-stu-id="d2efb-140">String</span></span>|<span data-ttu-id="d2efb-141">Id. del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d2efb-141">Device Id.</span></span>|
|<span data-ttu-id="d2efb-142">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="d2efb-142">lastSyncDateTime</span></span>|<span data-ttu-id="d2efb-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d2efb-143">DateTimeOffset</span></span>|<span data-ttu-id="d2efb-144">Fecha y hora de la última sincronización.</span><span class="sxs-lookup"><span data-stu-id="d2efb-144">Last sync date and time.</span></span>|
|<span data-ttu-id="d2efb-145">installState</span><span class="sxs-lookup"><span data-stu-id="d2efb-145">installState</span></span>|[<span data-ttu-id="d2efb-146">installState</span><span class="sxs-lookup"><span data-stu-id="d2efb-146">installState</span></span>](../resources/intune-books-installstate.md)|<span data-ttu-id="d2efb-147">El estado de instalación del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="d2efb-147">The install state of the eBook.</span></span> <span data-ttu-id="d2efb-148">Los valores posibles son: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed` y `unknown`.</span><span class="sxs-lookup"><span data-stu-id="d2efb-148">Possible values are: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed`, `unknown`.</span></span>|
|<span data-ttu-id="d2efb-149">errorCode</span><span class="sxs-lookup"><span data-stu-id="d2efb-149">errorCode</span></span>|<span data-ttu-id="d2efb-150">String</span><span class="sxs-lookup"><span data-stu-id="d2efb-150">String</span></span>|<span data-ttu-id="d2efb-151">El código de error si hay errores de instalación.</span><span class="sxs-lookup"><span data-stu-id="d2efb-151">The error code for install failures.</span></span>|
|<span data-ttu-id="d2efb-152">osVersion</span><span class="sxs-lookup"><span data-stu-id="d2efb-152">osVersion</span></span>|<span data-ttu-id="d2efb-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2efb-153">String</span></span>|<span data-ttu-id="d2efb-154">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d2efb-154">OS Version.</span></span>|
|<span data-ttu-id="d2efb-155">osDescription</span><span class="sxs-lookup"><span data-stu-id="d2efb-155">osDescription</span></span>|<span data-ttu-id="d2efb-156">String</span><span class="sxs-lookup"><span data-stu-id="d2efb-156">String</span></span>|<span data-ttu-id="d2efb-157">Descripción del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d2efb-157">OS Description.</span></span>|
|<span data-ttu-id="d2efb-158">userName</span><span class="sxs-lookup"><span data-stu-id="d2efb-158">userName</span></span>|<span data-ttu-id="d2efb-159">String</span><span class="sxs-lookup"><span data-stu-id="d2efb-159">String</span></span>|<span data-ttu-id="d2efb-160">Nombre de usuario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2efb-160">Device User Name.</span></span>|



## <a name="response"></a><span data-ttu-id="d2efb-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2efb-161">Response</span></span>
<span data-ttu-id="d2efb-162">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2efb-162">If successful, this method returns a `200 OK` response code and an updated [deviceInstallState](../resources/intune-books-deviceinstallstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d2efb-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2efb-163">Example</span></span>
### <a name="request"></a><span data-ttu-id="d2efb-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2efb-164">Request</span></span>
<span data-ttu-id="d2efb-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2efb-165">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates/{deviceInstallStateId}
Content-type: application/json
Content-length: 317

{
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

### <a name="response"></a><span data-ttu-id="d2efb-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2efb-166">Response</span></span>
<span data-ttu-id="d2efb-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2efb-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






---
title: Crear deviceInstallState
description: Cree un objeto deviceInstallState.
ms.openlocfilehash: b210ca932ee6132bd4b5c09988fae3c0bae9ca25
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088414"
---
# <a name="create-deviceinstallstate"></a><span data-ttu-id="9b26e-103">Crear deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="9b26e-103">Create deviceInstallState</span></span>

> <span data-ttu-id="9b26e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9b26e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9b26e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9b26e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9b26e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9b26e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9b26e-107">Cree un objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="9b26e-107">Create a new [deviceInstallState](../resources/intune-books-deviceinstallstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9b26e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9b26e-108">Prerequisites</span></span>
<span data-ttu-id="9b26e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9b26e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9b26e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b26e-111">Permission type</span></span>|<span data-ttu-id="9b26e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b26e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9b26e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b26e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9b26e-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9b26e-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="9b26e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b26e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9b26e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b26e-116">Not supported.</span></span>|
|<span data-ttu-id="9b26e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b26e-117">Application</span></span>|<span data-ttu-id="9b26e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b26e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9b26e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b26e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates
POST /deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary/{userInstallStateSummaryId}/deviceStates
```

## <a name="request-headers"></a><span data-ttu-id="9b26e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b26e-120">Request headers</span></span>
|<span data-ttu-id="9b26e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b26e-121">Header</span></span>|<span data-ttu-id="9b26e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9b26e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9b26e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="9b26e-123">Authorization</span></span>|<span data-ttu-id="9b26e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9b26e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9b26e-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9b26e-125">Accept</span></span>|<span data-ttu-id="9b26e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9b26e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9b26e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b26e-127">Request body</span></span>
<span data-ttu-id="9b26e-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceInstallState.</span><span class="sxs-lookup"><span data-stu-id="9b26e-128">In the request body, supply a JSON representation for the deviceInstallState object.</span></span>

<span data-ttu-id="9b26e-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceInstallState.</span><span class="sxs-lookup"><span data-stu-id="9b26e-129">The following table shows the properties that are required when you create the deviceInstallState.</span></span>

|<span data-ttu-id="9b26e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9b26e-130">Property</span></span>|<span data-ttu-id="9b26e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b26e-131">Type</span></span>|<span data-ttu-id="9b26e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b26e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9b26e-133">id</span><span class="sxs-lookup"><span data-stu-id="9b26e-133">id</span></span>|<span data-ttu-id="9b26e-134">String</span><span class="sxs-lookup"><span data-stu-id="9b26e-134">String</span></span>|<span data-ttu-id="9b26e-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9b26e-135">Key of the entity.</span></span>|
|<span data-ttu-id="9b26e-136">deviceName</span><span class="sxs-lookup"><span data-stu-id="9b26e-136">deviceName</span></span>|<span data-ttu-id="9b26e-137">String</span><span class="sxs-lookup"><span data-stu-id="9b26e-137">String</span></span>|<span data-ttu-id="9b26e-138">Nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b26e-138">Device name.</span></span>|
|<span data-ttu-id="9b26e-139">deviceId</span><span class="sxs-lookup"><span data-stu-id="9b26e-139">deviceId</span></span>|<span data-ttu-id="9b26e-140">String</span><span class="sxs-lookup"><span data-stu-id="9b26e-140">String</span></span>|<span data-ttu-id="9b26e-141">Id. del dispositivo</span><span class="sxs-lookup"><span data-stu-id="9b26e-141">Device Id.</span></span>|
|<span data-ttu-id="9b26e-142">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="9b26e-142">lastSyncDateTime</span></span>|<span data-ttu-id="9b26e-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9b26e-143">DateTimeOffset</span></span>|<span data-ttu-id="9b26e-144">Fecha y hora de la última sincronización.</span><span class="sxs-lookup"><span data-stu-id="9b26e-144">Last sync date and time.</span></span>|
|<span data-ttu-id="9b26e-145">installState</span><span class="sxs-lookup"><span data-stu-id="9b26e-145">installState</span></span>|[<span data-ttu-id="9b26e-146">installState</span><span class="sxs-lookup"><span data-stu-id="9b26e-146">installState</span></span>](../resources/intune-books-installstate.md)|<span data-ttu-id="9b26e-147">El estado de instalación del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="9b26e-147">The install state of the eBook.</span></span> <span data-ttu-id="9b26e-148">Los valores posibles son: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed` y `unknown`.</span><span class="sxs-lookup"><span data-stu-id="9b26e-148">Possible values are: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed`, `unknown`.</span></span>|
|<span data-ttu-id="9b26e-149">errorCode</span><span class="sxs-lookup"><span data-stu-id="9b26e-149">errorCode</span></span>|<span data-ttu-id="9b26e-150">String</span><span class="sxs-lookup"><span data-stu-id="9b26e-150">String</span></span>|<span data-ttu-id="9b26e-151">El código de error si hay errores de instalación.</span><span class="sxs-lookup"><span data-stu-id="9b26e-151">The error code for install failures.</span></span>|
|<span data-ttu-id="9b26e-152">osVersion</span><span class="sxs-lookup"><span data-stu-id="9b26e-152">osVersion</span></span>|<span data-ttu-id="9b26e-153">String</span><span class="sxs-lookup"><span data-stu-id="9b26e-153">String</span></span>|<span data-ttu-id="9b26e-154">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9b26e-154">OS Version.</span></span>|
|<span data-ttu-id="9b26e-155">osDescription</span><span class="sxs-lookup"><span data-stu-id="9b26e-155">osDescription</span></span>|<span data-ttu-id="9b26e-156">String</span><span class="sxs-lookup"><span data-stu-id="9b26e-156">String</span></span>|<span data-ttu-id="9b26e-157">Descripción del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9b26e-157">OS Description.</span></span>|
|<span data-ttu-id="9b26e-158">userName</span><span class="sxs-lookup"><span data-stu-id="9b26e-158">userName</span></span>|<span data-ttu-id="9b26e-159">String</span><span class="sxs-lookup"><span data-stu-id="9b26e-159">String</span></span>|<span data-ttu-id="9b26e-160">Nombre de usuario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b26e-160">Device User Name.</span></span>|



## <a name="response"></a><span data-ttu-id="9b26e-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b26e-161">Response</span></span>
<span data-ttu-id="9b26e-162">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b26e-162">If successful, this method returns a `201 Created` response code and a [deviceInstallState](../resources/intune-books-deviceinstallstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9b26e-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b26e-163">Example</span></span>
### <a name="request"></a><span data-ttu-id="9b26e-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b26e-164">Request</span></span>
<span data-ttu-id="9b26e-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b26e-165">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates
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

### <a name="response"></a><span data-ttu-id="9b26e-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b26e-166">Response</span></span>
<span data-ttu-id="9b26e-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9b26e-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






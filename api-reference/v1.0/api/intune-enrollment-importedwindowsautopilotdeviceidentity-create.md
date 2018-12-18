---
title: Crear importedWindowsAutopilotDeviceIdentity
description: Crea un objeto importedWindowsAutopilotDeviceIdentity nuevo.
author: tfitzmac
ms.openlocfilehash: 10dbaed9d10a0b37df9e229d501bb6e469847ea5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334296"
---
# <a name="create-importedwindowsautopilotdeviceidentity"></a><span data-ttu-id="f76e9-103">Crear importedWindowsAutopilotDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="f76e9-103">Create importedWindowsAutopilotDeviceIdentity</span></span>

> <span data-ttu-id="f76e9-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f76e9-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f76e9-105">Crea un objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) nuevo.</span><span class="sxs-lookup"><span data-stu-id="f76e9-105">Create a new [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f76e9-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f76e9-106">Prerequisites</span></span>
<span data-ttu-id="f76e9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f76e9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f76e9-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f76e9-109">Permission type</span></span>|<span data-ttu-id="f76e9-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f76e9-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f76e9-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f76e9-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f76e9-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f76e9-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="f76e9-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f76e9-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f76e9-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f76e9-114">Not supported.</span></span>|
|<span data-ttu-id="f76e9-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f76e9-115">Application</span></span>|<span data-ttu-id="f76e9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f76e9-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f76e9-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f76e9-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/importedWindowsAutopilotDeviceIdentities
POST /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads/{importedWindowsAutopilotDeviceIdentityUploadId}/deviceIdentities
```

## <a name="request-headers"></a><span data-ttu-id="f76e9-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f76e9-118">Request headers</span></span>
|<span data-ttu-id="f76e9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f76e9-119">Header</span></span>|<span data-ttu-id="f76e9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f76e9-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f76e9-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="f76e9-121">Authorization</span></span>|<span data-ttu-id="f76e9-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f76e9-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f76e9-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f76e9-123">Accept</span></span>|<span data-ttu-id="f76e9-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f76e9-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f76e9-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f76e9-125">Request body</span></span>
<span data-ttu-id="f76e9-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto importedWindowsAutopilotDeviceIdentity.</span><span class="sxs-lookup"><span data-stu-id="f76e9-126">In the request body, supply a JSON representation for the importedWindowsAutopilotDeviceIdentity object.</span></span>

<span data-ttu-id="f76e9-127">En la tabla siguiente se muestran las propiedades necesarias para crear importedWindowsAutopilotDeviceIdentity.</span><span class="sxs-lookup"><span data-stu-id="f76e9-127">The following table shows the properties that are required when you create the importedWindowsAutopilotDeviceIdentity.</span></span>

|<span data-ttu-id="f76e9-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f76e9-128">Property</span></span>|<span data-ttu-id="f76e9-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f76e9-129">Type</span></span>|<span data-ttu-id="f76e9-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f76e9-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f76e9-131">id</span><span class="sxs-lookup"><span data-stu-id="f76e9-131">id</span></span>|<span data-ttu-id="f76e9-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="f76e9-132">String</span></span>|<span data-ttu-id="f76e9-133">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="f76e9-133">The GUID for the object</span></span>|
|<span data-ttu-id="f76e9-134">orderIdentifier</span><span class="sxs-lookup"><span data-stu-id="f76e9-134">orderIdentifier</span></span>|<span data-ttu-id="f76e9-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="f76e9-135">String</span></span>|<span data-ttu-id="f76e9-136">Id. de pedido del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="f76e9-136">Order Id of the Windows autopilot device.</span></span>|
|<span data-ttu-id="f76e9-137">serialNumber</span><span class="sxs-lookup"><span data-stu-id="f76e9-137">serialNumber</span></span>|<span data-ttu-id="f76e9-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="f76e9-138">String</span></span>|<span data-ttu-id="f76e9-139">Número de serie del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="f76e9-139">Serial number of the Windows autopilot device.</span></span>|
|<span data-ttu-id="f76e9-140">productKey</span><span class="sxs-lookup"><span data-stu-id="f76e9-140">productKey</span></span>|<span data-ttu-id="f76e9-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="f76e9-141">String</span></span>|<span data-ttu-id="f76e9-142">Clave de producto del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="f76e9-142">Product Key of the Windows autopilot device.</span></span>|
|<span data-ttu-id="f76e9-143">hardwareIdentifier</span><span class="sxs-lookup"><span data-stu-id="f76e9-143">hardwareIdentifier</span></span>|<span data-ttu-id="f76e9-144">Binario</span><span class="sxs-lookup"><span data-stu-id="f76e9-144">Binary</span></span>|<span data-ttu-id="f76e9-145">Blob de hardware del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="f76e9-145">Hardware Blob of the Windows autopilot device.</span></span>|
|<span data-ttu-id="f76e9-146">estado</span><span class="sxs-lookup"><span data-stu-id="f76e9-146">state</span></span>|[<span data-ttu-id="f76e9-147">importedWindowsAutopilotDeviceIdentityState</span><span class="sxs-lookup"><span data-stu-id="f76e9-147">importedWindowsAutopilotDeviceIdentityState</span></span>](../resources/intune-enrollment-importedwindowsautopilotdeviceidentitystate.md)|<span data-ttu-id="f76e9-148">Estado actual del dispositivo importado.</span><span class="sxs-lookup"><span data-stu-id="f76e9-148">Current state of the imported device.</span></span>|



## <a name="response"></a><span data-ttu-id="f76e9-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f76e9-149">Response</span></span>
<span data-ttu-id="f76e9-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f76e9-150">If successful, this method returns a `201 Created` response code and a [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f76e9-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f76e9-151">Example</span></span>
### <a name="request"></a><span data-ttu-id="f76e9-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f76e9-152">Request</span></span>
<span data-ttu-id="f76e9-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f76e9-153">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/importedWindowsAutopilotDeviceIdentities
Content-type: application/json
Content-length: 541

{
  "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentity",
  "orderIdentifier": "Order Identifier value",
  "serialNumber": "Serial Number value",
  "productKey": "Product Key value",
  "hardwareIdentifier": "aGFyZHdhcmVJZGVudGlmaWVy",
  "state": {
    "@odata.type": "microsoft.graph.importedWindowsAutopilotDeviceIdentityState",
    "deviceImportStatus": "pending",
    "deviceRegistrationId": "Device Registration Id value",
    "deviceErrorCode": 15,
    "deviceErrorName": "Device Error Name value"
  }
}
```

### <a name="response"></a><span data-ttu-id="f76e9-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f76e9-154">Response</span></span>
<span data-ttu-id="f76e9-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f76e9-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 590

{
  "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentity",
  "id": "985b4f49-4f49-985b-494f-5b98494f5b98",
  "orderIdentifier": "Order Identifier value",
  "serialNumber": "Serial Number value",
  "productKey": "Product Key value",
  "hardwareIdentifier": "aGFyZHdhcmVJZGVudGlmaWVy",
  "state": {
    "@odata.type": "microsoft.graph.importedWindowsAutopilotDeviceIdentityState",
    "deviceImportStatus": "pending",
    "deviceRegistrationId": "Device Registration Id value",
    "deviceErrorCode": 15,
    "deviceErrorName": "Device Error Name value"
  }
}
```




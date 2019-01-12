---
title: Actualizar importedWindowsAutopilotDeviceIdentity
description: Actualiza las propiedades de un objeto importedWindowsAutopilotDeviceIdentity.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: eea4d28fd097e316a569a4969d1ee4376cb189b4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956839"
---
# <a name="update-importedwindowsautopilotdeviceidentity"></a><span data-ttu-id="0c28b-103">Actualizar importedWindowsAutopilotDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="0c28b-103">Update importedWindowsAutopilotDeviceIdentity</span></span>

> <span data-ttu-id="0c28b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0c28b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0c28b-105">Actualiza las propiedades de un objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="0c28b-105">Update the properties of a [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0c28b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0c28b-106">Prerequisites</span></span>
<span data-ttu-id="0c28b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0c28b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0c28b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0c28b-109">Permission type</span></span>|<span data-ttu-id="0c28b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0c28b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0c28b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0c28b-111">Delegated (work or school account)</span></span>|<span data-ttu-id="0c28b-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0c28b-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="0c28b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0c28b-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0c28b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0c28b-114">Not supported.</span></span>|
|<span data-ttu-id="0c28b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0c28b-115">Application</span></span>|<span data-ttu-id="0c28b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0c28b-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0c28b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0c28b-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/importedWindowsAutopilotDeviceIdentities/{importedWindowsAutopilotDeviceIdentityId}
PATCH /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads/{importedWindowsAutopilotDeviceIdentityUploadId}/deviceIdentities/{importedWindowsAutopilotDeviceIdentityId}
```

## <a name="request-headers"></a><span data-ttu-id="0c28b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0c28b-118">Request headers</span></span>
|<span data-ttu-id="0c28b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c28b-119">Header</span></span>|<span data-ttu-id="0c28b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0c28b-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0c28b-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="0c28b-121">Authorization</span></span>|<span data-ttu-id="0c28b-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0c28b-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0c28b-123">Accept</span><span class="sxs-lookup"><span data-stu-id="0c28b-123">Accept</span></span>|<span data-ttu-id="0c28b-124">application/json</span><span class="sxs-lookup"><span data-stu-id="0c28b-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0c28b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0c28b-125">Request body</span></span>
<span data-ttu-id="0c28b-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="0c28b-126">In the request body, supply a JSON representation for the [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) object.</span></span>

<span data-ttu-id="0c28b-127">En la tabla siguiente se muestran las propiedades necesarias para crear [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="0c28b-127">The following table shows the properties that are required when you create the [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md).</span></span>

|<span data-ttu-id="0c28b-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0c28b-128">Property</span></span>|<span data-ttu-id="0c28b-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="0c28b-129">Type</span></span>|<span data-ttu-id="0c28b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c28b-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0c28b-131">id</span><span class="sxs-lookup"><span data-stu-id="0c28b-131">id</span></span>|<span data-ttu-id="0c28b-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="0c28b-132">String</span></span>|<span data-ttu-id="0c28b-133">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="0c28b-133">The GUID for the object</span></span>|
|<span data-ttu-id="0c28b-134">orderIdentifier</span><span class="sxs-lookup"><span data-stu-id="0c28b-134">orderIdentifier</span></span>|<span data-ttu-id="0c28b-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="0c28b-135">String</span></span>|<span data-ttu-id="0c28b-136">Id. de pedido del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="0c28b-136">Order Id of the Windows autopilot device.</span></span>|
|<span data-ttu-id="0c28b-137">serialNumber</span><span class="sxs-lookup"><span data-stu-id="0c28b-137">serialNumber</span></span>|<span data-ttu-id="0c28b-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="0c28b-138">String</span></span>|<span data-ttu-id="0c28b-139">Número de serie del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="0c28b-139">Serial number of the Windows autopilot device.</span></span>|
|<span data-ttu-id="0c28b-140">productKey</span><span class="sxs-lookup"><span data-stu-id="0c28b-140">productKey</span></span>|<span data-ttu-id="0c28b-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="0c28b-141">String</span></span>|<span data-ttu-id="0c28b-142">Clave de producto del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="0c28b-142">Product Key of the Windows autopilot device.</span></span>|
|<span data-ttu-id="0c28b-143">hardwareIdentifier</span><span class="sxs-lookup"><span data-stu-id="0c28b-143">hardwareIdentifier</span></span>|<span data-ttu-id="0c28b-144">Binario</span><span class="sxs-lookup"><span data-stu-id="0c28b-144">Binary</span></span>|<span data-ttu-id="0c28b-145">Blob de hardware del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="0c28b-145">Hardware Blob of the Windows autopilot device.</span></span>|
|<span data-ttu-id="0c28b-146">estado</span><span class="sxs-lookup"><span data-stu-id="0c28b-146">state</span></span>|[<span data-ttu-id="0c28b-147">importedWindowsAutopilotDeviceIdentityState</span><span class="sxs-lookup"><span data-stu-id="0c28b-147">importedWindowsAutopilotDeviceIdentityState</span></span>](../resources/intune-enrollment-importedwindowsautopilotdeviceidentitystate.md)|<span data-ttu-id="0c28b-148">Estado actual del dispositivo importado.</span><span class="sxs-lookup"><span data-stu-id="0c28b-148">Current state of the imported device.</span></span>|



## <a name="response"></a><span data-ttu-id="0c28b-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0c28b-149">Response</span></span>
<span data-ttu-id="0c28b-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0c28b-150">If successful, this method returns a `200 OK` response code and an updated [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0c28b-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0c28b-151">Example</span></span>
### <a name="request"></a><span data-ttu-id="0c28b-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0c28b-152">Request</span></span>
<span data-ttu-id="0c28b-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0c28b-153">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/importedWindowsAutopilotDeviceIdentities/{importedWindowsAutopilotDeviceIdentityId}
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

### <a name="response"></a><span data-ttu-id="0c28b-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0c28b-154">Response</span></span>
<span data-ttu-id="0c28b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0c28b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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




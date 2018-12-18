---
title: Actualizar importedWindowsAutopilotDeviceIdentity
description: Actualiza las propiedades de un objeto importedWindowsAutopilotDeviceIdentity.
author: tfitzmac
ms.openlocfilehash: ba28b77811082b6339987f173d874e453a91aa75
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334268"
---
# <a name="update-importedwindowsautopilotdeviceidentity"></a><span data-ttu-id="68541-103">Actualizar importedWindowsAutopilotDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="68541-103">Update importedWindowsAutopilotDeviceIdentity</span></span>

> <span data-ttu-id="68541-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="68541-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="68541-105">Actualiza las propiedades de un objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="68541-105">Update the properties of a [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="68541-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="68541-106">Prerequisites</span></span>
<span data-ttu-id="68541-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="68541-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="68541-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="68541-109">Permission type</span></span>|<span data-ttu-id="68541-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="68541-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="68541-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="68541-111">Delegated (work or school account)</span></span>|<span data-ttu-id="68541-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="68541-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="68541-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="68541-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="68541-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="68541-114">Not supported.</span></span>|
|<span data-ttu-id="68541-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="68541-115">Application</span></span>|<span data-ttu-id="68541-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="68541-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="68541-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="68541-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/importedWindowsAutopilotDeviceIdentities/{importedWindowsAutopilotDeviceIdentityId}
PATCH /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads/{importedWindowsAutopilotDeviceIdentityUploadId}/deviceIdentities/{importedWindowsAutopilotDeviceIdentityId}
```

## <a name="request-headers"></a><span data-ttu-id="68541-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="68541-118">Request headers</span></span>
|<span data-ttu-id="68541-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68541-119">Header</span></span>|<span data-ttu-id="68541-120">Valor</span><span class="sxs-lookup"><span data-stu-id="68541-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="68541-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="68541-121">Authorization</span></span>|<span data-ttu-id="68541-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="68541-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="68541-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="68541-123">Accept</span></span>|<span data-ttu-id="68541-124">application/json</span><span class="sxs-lookup"><span data-stu-id="68541-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="68541-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="68541-125">Request body</span></span>
<span data-ttu-id="68541-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="68541-126">In the request body, supply a JSON representation for the [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) object.</span></span>

<span data-ttu-id="68541-127">En la tabla siguiente se muestran las propiedades necesarias para crear [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="68541-127">The following table shows the properties that are required when you create the [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md).</span></span>

|<span data-ttu-id="68541-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="68541-128">Property</span></span>|<span data-ttu-id="68541-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="68541-129">Type</span></span>|<span data-ttu-id="68541-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="68541-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="68541-131">id</span><span class="sxs-lookup"><span data-stu-id="68541-131">id</span></span>|<span data-ttu-id="68541-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="68541-132">String</span></span>|<span data-ttu-id="68541-133">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="68541-133">The GUID for the object</span></span>|
|<span data-ttu-id="68541-134">orderIdentifier</span><span class="sxs-lookup"><span data-stu-id="68541-134">orderIdentifier</span></span>|<span data-ttu-id="68541-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="68541-135">String</span></span>|<span data-ttu-id="68541-136">Id. de pedido del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="68541-136">Order Id of the Windows autopilot device.</span></span>|
|<span data-ttu-id="68541-137">serialNumber</span><span class="sxs-lookup"><span data-stu-id="68541-137">serialNumber</span></span>|<span data-ttu-id="68541-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="68541-138">String</span></span>|<span data-ttu-id="68541-139">Número de serie del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="68541-139">Serial number of the Windows autopilot device.</span></span>|
|<span data-ttu-id="68541-140">productKey</span><span class="sxs-lookup"><span data-stu-id="68541-140">productKey</span></span>|<span data-ttu-id="68541-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="68541-141">String</span></span>|<span data-ttu-id="68541-142">Clave de producto del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="68541-142">Product Key of the Windows autopilot device.</span></span>|
|<span data-ttu-id="68541-143">hardwareIdentifier</span><span class="sxs-lookup"><span data-stu-id="68541-143">hardwareIdentifier</span></span>|<span data-ttu-id="68541-144">Binario</span><span class="sxs-lookup"><span data-stu-id="68541-144">Binary</span></span>|<span data-ttu-id="68541-145">Blob de hardware del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="68541-145">Hardware Blob of the Windows autopilot device.</span></span>|
|<span data-ttu-id="68541-146">estado</span><span class="sxs-lookup"><span data-stu-id="68541-146">state</span></span>|[<span data-ttu-id="68541-147">importedWindowsAutopilotDeviceIdentityState</span><span class="sxs-lookup"><span data-stu-id="68541-147">importedWindowsAutopilotDeviceIdentityState</span></span>](../resources/intune-enrollment-importedwindowsautopilotdeviceidentitystate.md)|<span data-ttu-id="68541-148">Estado actual del dispositivo importado.</span><span class="sxs-lookup"><span data-stu-id="68541-148">Current state of the imported device.</span></span>|



## <a name="response"></a><span data-ttu-id="68541-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68541-149">Response</span></span>
<span data-ttu-id="68541-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68541-150">If successful, this method returns a `200 OK` response code and an updated [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="68541-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="68541-151">Example</span></span>
### <a name="request"></a><span data-ttu-id="68541-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="68541-152">Request</span></span>
<span data-ttu-id="68541-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="68541-153">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="68541-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68541-154">Response</span></span>
<span data-ttu-id="68541-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="68541-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




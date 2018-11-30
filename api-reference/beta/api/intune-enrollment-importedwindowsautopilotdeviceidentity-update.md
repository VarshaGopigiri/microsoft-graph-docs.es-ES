---
title: Actualizar importedWindowsAutopilotDeviceIdentity
description: Actualiza las propiedades de un objeto importedWindowsAutopilotDeviceIdentity.
ms.openlocfilehash: 7b5d79893ec30c203d4272d652ac43a225a37ec5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090091"
---
# <a name="update-importedwindowsautopilotdeviceidentity"></a><span data-ttu-id="6bdcb-103">Actualizar importedWindowsAutopilotDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="6bdcb-103">Update importedWindowsAutopilotDeviceIdentity</span></span>

> <span data-ttu-id="6bdcb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6bdcb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6bdcb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6bdcb-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6bdcb-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6bdcb-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6bdcb-107">Actualiza las propiedades de un objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="6bdcb-107">Update the properties of a [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6bdcb-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6bdcb-108">Prerequisites</span></span>
<span data-ttu-id="6bdcb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6bdcb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6bdcb-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6bdcb-111">Permission type</span></span>|<span data-ttu-id="6bdcb-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6bdcb-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6bdcb-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6bdcb-113">Delegated (work or school account)</span></span>|<span data-ttu-id="6bdcb-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6bdcb-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="6bdcb-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6bdcb-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6bdcb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6bdcb-116">Not supported.</span></span>|
|<span data-ttu-id="6bdcb-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6bdcb-117">Application</span></span>|<span data-ttu-id="6bdcb-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6bdcb-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6bdcb-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6bdcb-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/importedWindowsAutopilotDeviceIdentities/{importedWindowsAutopilotDeviceIdentityId}
PATCH /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads/{importedWindowsAutopilotDeviceIdentityUploadId}/deviceIdentities/{importedWindowsAutopilotDeviceIdentityId}
```

## <a name="request-headers"></a><span data-ttu-id="6bdcb-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6bdcb-120">Request headers</span></span>
|<span data-ttu-id="6bdcb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6bdcb-121">Header</span></span>|<span data-ttu-id="6bdcb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6bdcb-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6bdcb-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6bdcb-123">Authorization</span></span>|<span data-ttu-id="6bdcb-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6bdcb-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6bdcb-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6bdcb-125">Accept</span></span>|<span data-ttu-id="6bdcb-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6bdcb-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6bdcb-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6bdcb-127">Request body</span></span>
<span data-ttu-id="6bdcb-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="6bdcb-128">In the request body, supply a JSON representation for the [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) object.</span></span>

<span data-ttu-id="6bdcb-129">En la tabla siguiente se muestran las propiedades necesarias para crear [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="6bdcb-129">The following table shows the properties that are required when you create the [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md).</span></span>

|<span data-ttu-id="6bdcb-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6bdcb-130">Property</span></span>|<span data-ttu-id="6bdcb-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6bdcb-131">Type</span></span>|<span data-ttu-id="6bdcb-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6bdcb-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6bdcb-133">id</span><span class="sxs-lookup"><span data-stu-id="6bdcb-133">id</span></span>|<span data-ttu-id="6bdcb-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="6bdcb-134">String</span></span>|<span data-ttu-id="6bdcb-135">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="6bdcb-135">The GUID for the object</span></span>|
|<span data-ttu-id="6bdcb-136">orderIdentifier</span><span class="sxs-lookup"><span data-stu-id="6bdcb-136">orderIdentifier</span></span>|<span data-ttu-id="6bdcb-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="6bdcb-137">String</span></span>|<span data-ttu-id="6bdcb-138">Id. de pedido del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="6bdcb-138">Order Id of the Windows autopilot device.</span></span>|
|<span data-ttu-id="6bdcb-139">serialNumber</span><span class="sxs-lookup"><span data-stu-id="6bdcb-139">serialNumber</span></span>|<span data-ttu-id="6bdcb-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="6bdcb-140">String</span></span>|<span data-ttu-id="6bdcb-141">Número de serie del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="6bdcb-141">Serial number of the Windows autopilot device.</span></span>|
|<span data-ttu-id="6bdcb-142">productKey</span><span class="sxs-lookup"><span data-stu-id="6bdcb-142">productKey</span></span>|<span data-ttu-id="6bdcb-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="6bdcb-143">String</span></span>|<span data-ttu-id="6bdcb-144">Clave de producto del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="6bdcb-144">Product Key of the Windows autopilot device.</span></span>|
|<span data-ttu-id="6bdcb-145">hardwareIdentifier</span><span class="sxs-lookup"><span data-stu-id="6bdcb-145">hardwareIdentifier</span></span>|<span data-ttu-id="6bdcb-146">Binario</span><span class="sxs-lookup"><span data-stu-id="6bdcb-146">Binary</span></span>|<span data-ttu-id="6bdcb-147">Blob de hardware del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="6bdcb-147">Hardware Blob of the Windows autopilot device.</span></span>|
|<span data-ttu-id="6bdcb-148">estado</span><span class="sxs-lookup"><span data-stu-id="6bdcb-148">state</span></span>|[<span data-ttu-id="6bdcb-149">importedWindowsAutopilotDeviceIdentityState</span><span class="sxs-lookup"><span data-stu-id="6bdcb-149">importedWindowsAutopilotDeviceIdentityState</span></span>](../resources/intune-enrollment-importedwindowsautopilotdeviceidentitystate.md)|<span data-ttu-id="6bdcb-150">Estado actual del dispositivo importado.</span><span class="sxs-lookup"><span data-stu-id="6bdcb-150">Current state of the imported device.</span></span>|



## <a name="response"></a><span data-ttu-id="6bdcb-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6bdcb-151">Response</span></span>
<span data-ttu-id="6bdcb-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6bdcb-152">If successful, this method returns a `200 OK` response code and an updated [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6bdcb-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6bdcb-153">Example</span></span>
### <a name="request"></a><span data-ttu-id="6bdcb-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6bdcb-154">Request</span></span>
<span data-ttu-id="6bdcb-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6bdcb-155">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/importedWindowsAutopilotDeviceIdentities/{importedWindowsAutopilotDeviceIdentityId}
Content-type: application/json
Content-length: 464

{
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

### <a name="response"></a><span data-ttu-id="6bdcb-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6bdcb-156">Response</span></span>
<span data-ttu-id="6bdcb-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6bdcb-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






---
title: Actualizar importedWindowsAutopilotDeviceIdentityUpload
description: Actualizar las propiedades de un objeto importedWindowsAutopilotDeviceIdentityUpload.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ba5c58b220419cff73e317dcc24e0690eff71b0d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991065"
---
# <a name="update-importedwindowsautopilotdeviceidentityupload"></a><span data-ttu-id="22006-103">Actualizar importedWindowsAutopilotDeviceIdentityUpload</span><span class="sxs-lookup"><span data-stu-id="22006-103">Update importedWindowsAutopilotDeviceIdentityUpload</span></span>

> <span data-ttu-id="22006-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="22006-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="22006-105">Actualizar las propiedades de un objeto [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) .</span><span class="sxs-lookup"><span data-stu-id="22006-105">Update the properties of a [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="22006-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="22006-106">Prerequisites</span></span>
<span data-ttu-id="22006-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="22006-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="22006-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="22006-109">Permission type</span></span>|<span data-ttu-id="22006-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="22006-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="22006-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="22006-111">Delegated (work or school account)</span></span>|<span data-ttu-id="22006-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="22006-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="22006-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="22006-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="22006-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="22006-114">Not supported.</span></span>|
|<span data-ttu-id="22006-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="22006-115">Application</span></span>|<span data-ttu-id="22006-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="22006-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="22006-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="22006-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads/{importedWindowsAutopilotDeviceIdentityUploadId}
```

## <a name="request-headers"></a><span data-ttu-id="22006-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="22006-118">Request headers</span></span>
|<span data-ttu-id="22006-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22006-119">Header</span></span>|<span data-ttu-id="22006-120">Valor</span><span class="sxs-lookup"><span data-stu-id="22006-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="22006-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="22006-121">Authorization</span></span>|<span data-ttu-id="22006-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="22006-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="22006-123">Accept</span><span class="sxs-lookup"><span data-stu-id="22006-123">Accept</span></span>|<span data-ttu-id="22006-124">application/json</span><span class="sxs-lookup"><span data-stu-id="22006-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="22006-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="22006-125">Request body</span></span>
<span data-ttu-id="22006-126">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) .</span><span class="sxs-lookup"><span data-stu-id="22006-126">In the request body, supply a JSON representation for the [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) object.</span></span>

<span data-ttu-id="22006-127">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md).</span><span class="sxs-lookup"><span data-stu-id="22006-127">The following table shows the properties that are required when you create the [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md).</span></span>

|<span data-ttu-id="22006-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="22006-128">Property</span></span>|<span data-ttu-id="22006-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="22006-129">Type</span></span>|<span data-ttu-id="22006-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="22006-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="22006-131">id</span><span class="sxs-lookup"><span data-stu-id="22006-131">id</span></span>|<span data-ttu-id="22006-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="22006-132">String</span></span>|<span data-ttu-id="22006-133">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="22006-133">The GUID for the object</span></span>|
|<span data-ttu-id="22006-134">createdDateTimeUtc</span><span class="sxs-lookup"><span data-stu-id="22006-134">createdDateTimeUtc</span></span>|<span data-ttu-id="22006-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="22006-135">DateTimeOffset</span></span>|<span data-ttu-id="22006-136">Fecha y hora cuando se crea la entidad.</span><span class="sxs-lookup"><span data-stu-id="22006-136">DateTime when the entity is created.</span></span>|
|<span data-ttu-id="22006-137">status</span><span class="sxs-lookup"><span data-stu-id="22006-137">status</span></span>|[<span data-ttu-id="22006-138">importedWindowsAutopilotDeviceIdentityUploadStatus</span><span class="sxs-lookup"><span data-stu-id="22006-138">importedWindowsAutopilotDeviceIdentityUploadStatus</span></span>](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityuploadstatus.md)|<span data-ttu-id="22006-139">Estado de la carga.</span><span class="sxs-lookup"><span data-stu-id="22006-139">Upload status.</span></span> <span data-ttu-id="22006-140">Los valores posibles son: `noUpload`, `pending`, `complete` y `error`.</span><span class="sxs-lookup"><span data-stu-id="22006-140">Possible values are: `noUpload`, `pending`, `complete`, `error`.</span></span>|



## <a name="response"></a><span data-ttu-id="22006-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="22006-141">Response</span></span>
<span data-ttu-id="22006-142">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="22006-142">If successful, this method returns a `200 OK` response code and an updated [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="22006-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="22006-143">Example</span></span>
### <a name="request"></a><span data-ttu-id="22006-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="22006-144">Request</span></span>
<span data-ttu-id="22006-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="22006-145">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/importedWindowsAutopilotDeviceIdentityUploads/{importedWindowsAutopilotDeviceIdentityUploadId}
Content-type: application/json
Content-length: 172

{
  "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentityUpload",
  "createdDateTimeUtc": "2016-12-31T23:59:45.8788427-08:00",
  "status": "pending"
}
```

### <a name="response"></a><span data-ttu-id="22006-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="22006-146">Response</span></span>
<span data-ttu-id="22006-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="22006-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 221

{
  "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentityUpload",
  "id": "8d639524-9524-8d63-2495-638d2495638d",
  "createdDateTimeUtc": "2016-12-31T23:59:45.8788427-08:00",
  "status": "pending"
}
```




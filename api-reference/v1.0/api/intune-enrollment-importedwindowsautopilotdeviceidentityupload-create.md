---
title: Crear importedWindowsAutopilotDeviceIdentityUpload
description: Crear un nuevo objeto importedWindowsAutopilotDeviceIdentityUpload.
ms.openlocfilehash: ff5c28e115499a0b22d977c0d2b6ece1c0d99ad0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030796"
---
# <a name="create-importedwindowsautopilotdeviceidentityupload"></a><span data-ttu-id="ef275-103">Crear importedWindowsAutopilotDeviceIdentityUpload</span><span class="sxs-lookup"><span data-stu-id="ef275-103">Create importedWindowsAutopilotDeviceIdentityUpload</span></span>

> <span data-ttu-id="ef275-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ef275-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ef275-105">Crear un nuevo objeto [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) .</span><span class="sxs-lookup"><span data-stu-id="ef275-105">Create a new [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ef275-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ef275-106">Prerequisites</span></span>
<span data-ttu-id="ef275-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ef275-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ef275-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ef275-109">Permission type</span></span>|<span data-ttu-id="ef275-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ef275-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ef275-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ef275-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ef275-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ef275-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="ef275-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ef275-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ef275-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ef275-114">Not supported.</span></span>|
|<span data-ttu-id="ef275-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ef275-115">Application</span></span>|<span data-ttu-id="ef275-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ef275-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ef275-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ef275-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads
```

## <a name="request-headers"></a><span data-ttu-id="ef275-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ef275-118">Request headers</span></span>
|<span data-ttu-id="ef275-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef275-119">Header</span></span>|<span data-ttu-id="ef275-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ef275-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ef275-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="ef275-121">Authorization</span></span>|<span data-ttu-id="ef275-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ef275-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ef275-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ef275-123">Accept</span></span>|<span data-ttu-id="ef275-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ef275-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ef275-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ef275-125">Request body</span></span>
<span data-ttu-id="ef275-126">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto importedWindowsAutopilotDeviceIdentityUpload.</span><span class="sxs-lookup"><span data-stu-id="ef275-126">In the request body, supply a JSON representation for the importedWindowsAutopilotDeviceIdentityUpload object.</span></span>

<span data-ttu-id="ef275-127">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el importedWindowsAutopilotDeviceIdentityUpload.</span><span class="sxs-lookup"><span data-stu-id="ef275-127">The following table shows the properties that are required when you create the importedWindowsAutopilotDeviceIdentityUpload.</span></span>

|<span data-ttu-id="ef275-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ef275-128">Property</span></span>|<span data-ttu-id="ef275-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ef275-129">Type</span></span>|<span data-ttu-id="ef275-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef275-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ef275-131">id</span><span class="sxs-lookup"><span data-stu-id="ef275-131">id</span></span>|<span data-ttu-id="ef275-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="ef275-132">String</span></span>|<span data-ttu-id="ef275-133">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="ef275-133">The GUID for the object</span></span>|
|<span data-ttu-id="ef275-134">createdDateTimeUtc</span><span class="sxs-lookup"><span data-stu-id="ef275-134">createdDateTimeUtc</span></span>|<span data-ttu-id="ef275-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ef275-135">DateTimeOffset</span></span>|<span data-ttu-id="ef275-136">Fecha y hora cuando se crea la entidad.</span><span class="sxs-lookup"><span data-stu-id="ef275-136">DateTime when the entity is created.</span></span>|
|<span data-ttu-id="ef275-137">status</span><span class="sxs-lookup"><span data-stu-id="ef275-137">status</span></span>|[<span data-ttu-id="ef275-138">importedWindowsAutopilotDeviceIdentityUploadStatus</span><span class="sxs-lookup"><span data-stu-id="ef275-138">importedWindowsAutopilotDeviceIdentityUploadStatus</span></span>](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityuploadstatus.md)|<span data-ttu-id="ef275-139">Estado de la carga.</span><span class="sxs-lookup"><span data-stu-id="ef275-139">Upload status.</span></span> <span data-ttu-id="ef275-140">Los valores posibles son: `noUpload`, `pending`, `complete` y `error`.</span><span class="sxs-lookup"><span data-stu-id="ef275-140">Possible values are: `noUpload`, `pending`, `complete`, `error`.</span></span>|



## <a name="response"></a><span data-ttu-id="ef275-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef275-141">Response</span></span>
<span data-ttu-id="ef275-142">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef275-142">If successful, this method returns a `201 Created` response code and a [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ef275-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ef275-143">Example</span></span>
### <a name="request"></a><span data-ttu-id="ef275-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ef275-144">Request</span></span>
<span data-ttu-id="ef275-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ef275-145">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/importedWindowsAutopilotDeviceIdentityUploads
Content-type: application/json
Content-length: 172

{
  "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentityUpload",
  "createdDateTimeUtc": "2016-12-31T23:59:45.8788427-08:00",
  "status": "pending"
}
```

### <a name="response"></a><span data-ttu-id="ef275-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef275-146">Response</span></span>
<span data-ttu-id="ef275-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ef275-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 221

{
  "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentityUpload",
  "id": "8d639524-9524-8d63-2495-638d2495638d",
  "createdDateTimeUtc": "2016-12-31T23:59:45.8788427-08:00",
  "status": "pending"
}
```



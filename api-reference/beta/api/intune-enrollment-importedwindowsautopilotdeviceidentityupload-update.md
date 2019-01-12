---
title: Actualizar importedWindowsAutopilotDeviceIdentityUpload
description: Actualizar las propiedades de un objeto importedWindowsAutopilotDeviceIdentityUpload.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: cca9472b0ceee0daa4bff04543141a7afe66eb78
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950000"
---
# <a name="update-importedwindowsautopilotdeviceidentityupload"></a><span data-ttu-id="496b1-103">Actualizar importedWindowsAutopilotDeviceIdentityUpload</span><span class="sxs-lookup"><span data-stu-id="496b1-103">Update importedWindowsAutopilotDeviceIdentityUpload</span></span>

> <span data-ttu-id="496b1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="496b1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="496b1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="496b1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="496b1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="496b1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="496b1-107">Actualizar las propiedades de un objeto [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) .</span><span class="sxs-lookup"><span data-stu-id="496b1-107">Update the properties of a [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="496b1-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="496b1-108">Prerequisites</span></span>
<span data-ttu-id="496b1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="496b1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="496b1-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="496b1-111">Permission type</span></span>|<span data-ttu-id="496b1-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="496b1-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="496b1-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="496b1-113">Delegated (work or school account)</span></span>|<span data-ttu-id="496b1-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="496b1-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="496b1-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="496b1-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="496b1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="496b1-116">Not supported.</span></span>|
|<span data-ttu-id="496b1-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="496b1-117">Application</span></span>|<span data-ttu-id="496b1-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="496b1-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="496b1-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="496b1-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads/{importedWindowsAutopilotDeviceIdentityUploadId}
```

## <a name="request-headers"></a><span data-ttu-id="496b1-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="496b1-120">Request headers</span></span>
|<span data-ttu-id="496b1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="496b1-121">Header</span></span>|<span data-ttu-id="496b1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="496b1-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="496b1-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="496b1-123">Authorization</span></span>|<span data-ttu-id="496b1-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="496b1-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="496b1-125">Accept</span><span class="sxs-lookup"><span data-stu-id="496b1-125">Accept</span></span>|<span data-ttu-id="496b1-126">application/json</span><span class="sxs-lookup"><span data-stu-id="496b1-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="496b1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="496b1-127">Request body</span></span>
<span data-ttu-id="496b1-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) .</span><span class="sxs-lookup"><span data-stu-id="496b1-128">In the request body, supply a JSON representation for the [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) object.</span></span>

<span data-ttu-id="496b1-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md).</span><span class="sxs-lookup"><span data-stu-id="496b1-129">The following table shows the properties that are required when you create the [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md).</span></span>

|<span data-ttu-id="496b1-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="496b1-130">Property</span></span>|<span data-ttu-id="496b1-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="496b1-131">Type</span></span>|<span data-ttu-id="496b1-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="496b1-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="496b1-133">id</span><span class="sxs-lookup"><span data-stu-id="496b1-133">id</span></span>|<span data-ttu-id="496b1-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="496b1-134">String</span></span>|<span data-ttu-id="496b1-135">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="496b1-135">The GUID for the object</span></span>|
|<span data-ttu-id="496b1-136">createdDateTimeUtc</span><span class="sxs-lookup"><span data-stu-id="496b1-136">createdDateTimeUtc</span></span>|<span data-ttu-id="496b1-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="496b1-137">DateTimeOffset</span></span>|<span data-ttu-id="496b1-138">Fecha y hora cuando se crea la entidad.</span><span class="sxs-lookup"><span data-stu-id="496b1-138">DateTime when the entity is created.</span></span>|
|<span data-ttu-id="496b1-139">status</span><span class="sxs-lookup"><span data-stu-id="496b1-139">status</span></span>|[<span data-ttu-id="496b1-140">importedWindowsAutopilotDeviceIdentityUploadStatus</span><span class="sxs-lookup"><span data-stu-id="496b1-140">importedWindowsAutopilotDeviceIdentityUploadStatus</span></span>](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityuploadstatus.md)|<span data-ttu-id="496b1-141">Estado de la carga.</span><span class="sxs-lookup"><span data-stu-id="496b1-141">Upload status.</span></span> <span data-ttu-id="496b1-142">Los valores posibles son: `noUpload`, `pending`, `complete` y `error`.</span><span class="sxs-lookup"><span data-stu-id="496b1-142">Possible values are: `noUpload`, `pending`, `complete`, `error`.</span></span>|



## <a name="response"></a><span data-ttu-id="496b1-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="496b1-143">Response</span></span>
<span data-ttu-id="496b1-144">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="496b1-144">If successful, this method returns a `200 OK` response code and an updated [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="496b1-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="496b1-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="496b1-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="496b1-146">Request</span></span>
<span data-ttu-id="496b1-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="496b1-147">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/importedWindowsAutopilotDeviceIdentityUploads/{importedWindowsAutopilotDeviceIdentityUploadId}
Content-type: application/json
Content-length: 89

{
  "createdDateTimeUtc": "2016-12-31T23:59:45.8788427-08:00",
  "status": "pending"
}
```

### <a name="response"></a><span data-ttu-id="496b1-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="496b1-148">Response</span></span>
<span data-ttu-id="496b1-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="496b1-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






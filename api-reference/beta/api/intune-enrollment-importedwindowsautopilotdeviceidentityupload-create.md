---
title: Crear importedWindowsAutopilotDeviceIdentityUpload
description: Crear un nuevo objeto importedWindowsAutopilotDeviceIdentityUpload.
author: tfitzmac
ms.openlocfilehash: f4042129f33b617546e32d46435179af5c9d3282
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27354813"
---
# <a name="create-importedwindowsautopilotdeviceidentityupload"></a><span data-ttu-id="ab594-103">Crear importedWindowsAutopilotDeviceIdentityUpload</span><span class="sxs-lookup"><span data-stu-id="ab594-103">Create importedWindowsAutopilotDeviceIdentityUpload</span></span>

> <span data-ttu-id="ab594-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ab594-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ab594-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ab594-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ab594-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ab594-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ab594-107">Crear un nuevo objeto [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) .</span><span class="sxs-lookup"><span data-stu-id="ab594-107">Create a new [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ab594-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ab594-108">Prerequisites</span></span>
<span data-ttu-id="ab594-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ab594-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ab594-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ab594-111">Permission type</span></span>|<span data-ttu-id="ab594-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ab594-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ab594-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ab594-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ab594-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ab594-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="ab594-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ab594-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ab594-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ab594-116">Not supported.</span></span>|
|<span data-ttu-id="ab594-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ab594-117">Application</span></span>|<span data-ttu-id="ab594-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ab594-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ab594-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ab594-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads
```

## <a name="request-headers"></a><span data-ttu-id="ab594-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ab594-120">Request headers</span></span>
|<span data-ttu-id="ab594-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab594-121">Header</span></span>|<span data-ttu-id="ab594-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ab594-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ab594-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ab594-123">Authorization</span></span>|<span data-ttu-id="ab594-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ab594-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ab594-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ab594-125">Accept</span></span>|<span data-ttu-id="ab594-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ab594-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ab594-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ab594-127">Request body</span></span>
<span data-ttu-id="ab594-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto importedWindowsAutopilotDeviceIdentityUpload.</span><span class="sxs-lookup"><span data-stu-id="ab594-128">In the request body, supply a JSON representation for the importedWindowsAutopilotDeviceIdentityUpload object.</span></span>

<span data-ttu-id="ab594-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el importedWindowsAutopilotDeviceIdentityUpload.</span><span class="sxs-lookup"><span data-stu-id="ab594-129">The following table shows the properties that are required when you create the importedWindowsAutopilotDeviceIdentityUpload.</span></span>

|<span data-ttu-id="ab594-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ab594-130">Property</span></span>|<span data-ttu-id="ab594-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab594-131">Type</span></span>|<span data-ttu-id="ab594-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab594-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ab594-133">id</span><span class="sxs-lookup"><span data-stu-id="ab594-133">id</span></span>|<span data-ttu-id="ab594-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="ab594-134">String</span></span>|<span data-ttu-id="ab594-135">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="ab594-135">The GUID for the object</span></span>|
|<span data-ttu-id="ab594-136">createdDateTimeUtc</span><span class="sxs-lookup"><span data-stu-id="ab594-136">createdDateTimeUtc</span></span>|<span data-ttu-id="ab594-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ab594-137">DateTimeOffset</span></span>|<span data-ttu-id="ab594-138">Fecha y hora cuando se crea la entidad.</span><span class="sxs-lookup"><span data-stu-id="ab594-138">DateTime when the entity is created.</span></span>|
|<span data-ttu-id="ab594-139">status</span><span class="sxs-lookup"><span data-stu-id="ab594-139">status</span></span>|[<span data-ttu-id="ab594-140">importedWindowsAutopilotDeviceIdentityUploadStatus</span><span class="sxs-lookup"><span data-stu-id="ab594-140">importedWindowsAutopilotDeviceIdentityUploadStatus</span></span>](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityuploadstatus.md)|<span data-ttu-id="ab594-141">Estado de la carga.</span><span class="sxs-lookup"><span data-stu-id="ab594-141">Upload status.</span></span> <span data-ttu-id="ab594-142">Los valores posibles son: `noUpload`, `pending`, `complete` y `error`.</span><span class="sxs-lookup"><span data-stu-id="ab594-142">Possible values are: `noUpload`, `pending`, `complete`, `error`.</span></span>|



## <a name="response"></a><span data-ttu-id="ab594-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab594-143">Response</span></span>
<span data-ttu-id="ab594-144">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ab594-144">If successful, this method returns a `201 Created` response code and a [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ab594-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ab594-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="ab594-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ab594-146">Request</span></span>
<span data-ttu-id="ab594-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ab594-147">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/importedWindowsAutopilotDeviceIdentityUploads
Content-type: application/json
Content-length: 172

{
  "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentityUpload",
  "createdDateTimeUtc": "2016-12-31T23:59:45.8788427-08:00",
  "status": "pending"
}
```

### <a name="response"></a><span data-ttu-id="ab594-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab594-148">Response</span></span>
<span data-ttu-id="ab594-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ab594-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






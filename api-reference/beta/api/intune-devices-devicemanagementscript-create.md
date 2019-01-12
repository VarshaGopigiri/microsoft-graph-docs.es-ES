---
title: Crear deviceManagementScript
description: Crear un nuevo objeto deviceManagementScript.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3ef3f9436de79b5839912a44915238267f0c26dd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924030"
---
# <a name="create-devicemanagementscript"></a><span data-ttu-id="d0c5e-103">Crear deviceManagementScript</span><span class="sxs-lookup"><span data-stu-id="d0c5e-103">Create deviceManagementScript</span></span>

> <span data-ttu-id="d0c5e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d0c5e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d0c5e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d0c5e-107">Crear un nuevo objeto [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md) .</span><span class="sxs-lookup"><span data-stu-id="d0c5e-107">Create a new [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d0c5e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d0c5e-108">Prerequisites</span></span>
<span data-ttu-id="d0c5e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d0c5e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d0c5e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d0c5e-111">Permission type</span></span>|<span data-ttu-id="d0c5e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d0c5e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d0c5e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d0c5e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d0c5e-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0c5e-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="d0c5e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d0c5e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d0c5e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-116">Not supported.</span></span>|
|<span data-ttu-id="d0c5e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d0c5e-117">Application</span></span>|<span data-ttu-id="d0c5e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d0c5e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d0c5e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceManagementScripts
```

## <a name="request-headers"></a><span data-ttu-id="d0c5e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d0c5e-120">Request headers</span></span>
|<span data-ttu-id="d0c5e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0c5e-121">Header</span></span>|<span data-ttu-id="d0c5e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d0c5e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d0c5e-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="d0c5e-123">Authorization</span></span>|<span data-ttu-id="d0c5e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d0c5e-125">Accept</span><span class="sxs-lookup"><span data-stu-id="d0c5e-125">Accept</span></span>|<span data-ttu-id="d0c5e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d0c5e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d0c5e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d0c5e-127">Request body</span></span>
<span data-ttu-id="d0c5e-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto deviceManagementScript.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-128">In the request body, supply a JSON representation for the deviceManagementScript object.</span></span>

<span data-ttu-id="d0c5e-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el deviceManagementScript.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-129">The following table shows the properties that are required when you create the deviceManagementScript.</span></span>

|<span data-ttu-id="d0c5e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d0c5e-130">Property</span></span>|<span data-ttu-id="d0c5e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0c5e-131">Type</span></span>|<span data-ttu-id="d0c5e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0c5e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d0c5e-133">id</span><span class="sxs-lookup"><span data-stu-id="d0c5e-133">id</span></span>|<span data-ttu-id="d0c5e-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="d0c5e-134">String</span></span>|<span data-ttu-id="d0c5e-135">Identificador único para la secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-135">Unique Identifier for the device management script.</span></span>|
|<span data-ttu-id="d0c5e-136">displayName</span><span class="sxs-lookup"><span data-stu-id="d0c5e-136">displayName</span></span>|<span data-ttu-id="d0c5e-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="d0c5e-137">String</span></span>|<span data-ttu-id="d0c5e-138">Nombre de la secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-138">Name of the device management script.</span></span>|
|<span data-ttu-id="d0c5e-139">descripción</span><span class="sxs-lookup"><span data-stu-id="d0c5e-139">description</span></span>|<span data-ttu-id="d0c5e-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="d0c5e-140">String</span></span>|<span data-ttu-id="d0c5e-141">Descripción opcional de la secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-141">Optional description for the device management script.</span></span>|
|<span data-ttu-id="d0c5e-142">runSchedule</span><span class="sxs-lookup"><span data-stu-id="d0c5e-142">runSchedule</span></span>|[<span data-ttu-id="d0c5e-143">runSchedule</span><span class="sxs-lookup"><span data-stu-id="d0c5e-143">runSchedule</span></span>](../resources/intune-devices-runschedule.md)|<span data-ttu-id="d0c5e-144">El intervalo para ejecutar la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-144">The interval for script to run.</span></span> <span data-ttu-id="d0c5e-145">Si no ha definido la secuencia de comandos se ejecutará una vez</span><span class="sxs-lookup"><span data-stu-id="d0c5e-145">If not defined the script will run once</span></span>|
|<span data-ttu-id="d0c5e-146">scriptContent</span><span class="sxs-lookup"><span data-stu-id="d0c5e-146">scriptContent</span></span>|<span data-ttu-id="d0c5e-147">Binario</span><span class="sxs-lookup"><span data-stu-id="d0c5e-147">Binary</span></span>|<span data-ttu-id="d0c5e-148">El contenido de la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-148">The script content.</span></span>|
|<span data-ttu-id="d0c5e-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d0c5e-149">createdDateTime</span></span>|<span data-ttu-id="d0c5e-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d0c5e-150">DateTimeOffset</span></span>|<span data-ttu-id="d0c5e-151">La fecha y hora de que creación de la secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-151">The date and time the device management script was created.</span></span>|
|<span data-ttu-id="d0c5e-152">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d0c5e-152">lastModifiedDateTime</span></span>|<span data-ttu-id="d0c5e-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d0c5e-153">DateTimeOffset</span></span>|<span data-ttu-id="d0c5e-154">La fecha y hora de que última modificación de la secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-154">The date and time the device management script was last modified.</span></span>|
|<span data-ttu-id="d0c5e-155">runAsAccount</span><span class="sxs-lookup"><span data-stu-id="d0c5e-155">runAsAccount</span></span>|[<span data-ttu-id="d0c5e-156">runAsAccountType</span><span class="sxs-lookup"><span data-stu-id="d0c5e-156">runAsAccountType</span></span>](../resources/intune-shared-runasaccounttype.md)|<span data-ttu-id="d0c5e-157">Indica el tipo de la secuencia de comandos de administración de dispositivos se ejecuta en el contexto de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-157">Indicates the type of execution context the device management script runs in.</span></span> <span data-ttu-id="d0c5e-158">Los valores posibles son: `system` y `user`.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-158">Possible values are: `system`, `user`.</span></span>|
|<span data-ttu-id="d0c5e-159">enforceSignatureCheck</span><span class="sxs-lookup"><span data-stu-id="d0c5e-159">enforceSignatureCheck</span></span>|<span data-ttu-id="d0c5e-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="d0c5e-160">Boolean</span></span>|<span data-ttu-id="d0c5e-161">Indicar si se debe comprobar la firma de la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-161">Indicate whether the script signature needs be checked.</span></span>|
|<span data-ttu-id="d0c5e-162">fileName</span><span class="sxs-lookup"><span data-stu-id="d0c5e-162">fileName</span></span>|<span data-ttu-id="d0c5e-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="d0c5e-163">String</span></span>|<span data-ttu-id="d0c5e-164">Nombre de archivo de secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-164">Script file name.</span></span>|



## <a name="response"></a><span data-ttu-id="d0c5e-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0c5e-165">Response</span></span>
<span data-ttu-id="d0c5e-166">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-166">If successful, this method returns a `201 Created` response code and a [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d0c5e-167">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0c5e-167">Example</span></span>
### <a name="request"></a><span data-ttu-id="d0c5e-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d0c5e-168">Request</span></span>
<span data-ttu-id="d0c5e-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-169">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceManagementScripts
Content-type: application/json
Content-length: 422

{
  "@odata.type": "#microsoft.graph.deviceManagementScript",
  "displayName": "Display Name value",
  "description": "Description value",
  "runSchedule": {
    "@odata.type": "microsoft.graph.runSchedule"
  },
  "scriptContent": "c2NyaXB0Q29udGVudA==",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "runAsAccount": "user",
  "enforceSignatureCheck": true,
  "fileName": "File Name value"
}
```

### <a name="response"></a><span data-ttu-id="d0c5e-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0c5e-170">Response</span></span>
<span data-ttu-id="d0c5e-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d0c5e-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 530

{
  "@odata.type": "#microsoft.graph.deviceManagementScript",
  "id": "59ea4525-4525-59ea-2545-ea592545ea59",
  "displayName": "Display Name value",
  "description": "Description value",
  "runSchedule": {
    "@odata.type": "microsoft.graph.runSchedule"
  },
  "scriptContent": "c2NyaXB0Q29udGVudA==",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "runAsAccount": "user",
  "enforceSignatureCheck": true,
  "fileName": "File Name value"
}
```






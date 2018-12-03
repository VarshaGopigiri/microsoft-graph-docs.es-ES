---
title: Actualizar deviceManagementScript
description: Actualizar las propiedades de un objeto deviceManagementScript.
ms.openlocfilehash: d88579f130607b08b0d34620b701be5c239bc03f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086282"
---
# <a name="update-devicemanagementscript"></a><span data-ttu-id="936e1-103">Actualizar deviceManagementScript</span><span class="sxs-lookup"><span data-stu-id="936e1-103">Update deviceManagementScript</span></span>

> <span data-ttu-id="936e1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="936e1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="936e1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="936e1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="936e1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="936e1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="936e1-107">Actualizar las propiedades de un objeto [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md) .</span><span class="sxs-lookup"><span data-stu-id="936e1-107">Update the properties of a [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="936e1-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="936e1-108">Prerequisites</span></span>
<span data-ttu-id="936e1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="936e1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="936e1-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="936e1-111">Permission type</span></span>|<span data-ttu-id="936e1-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="936e1-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="936e1-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="936e1-113">Delegated (work or school account)</span></span>|<span data-ttu-id="936e1-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="936e1-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="936e1-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="936e1-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="936e1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="936e1-116">Not supported.</span></span>|
|<span data-ttu-id="936e1-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="936e1-117">Application</span></span>|<span data-ttu-id="936e1-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="936e1-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="936e1-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="936e1-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}
```

## <a name="request-headers"></a><span data-ttu-id="936e1-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="936e1-120">Request headers</span></span>
|<span data-ttu-id="936e1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="936e1-121">Header</span></span>|<span data-ttu-id="936e1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="936e1-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="936e1-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="936e1-123">Authorization</span></span>|<span data-ttu-id="936e1-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="936e1-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="936e1-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="936e1-125">Accept</span></span>|<span data-ttu-id="936e1-126">application/json</span><span class="sxs-lookup"><span data-stu-id="936e1-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="936e1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="936e1-127">Request body</span></span>
<span data-ttu-id="936e1-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md) .</span><span class="sxs-lookup"><span data-stu-id="936e1-128">In the request body, supply a JSON representation for the [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md) object.</span></span>

<span data-ttu-id="936e1-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md).</span><span class="sxs-lookup"><span data-stu-id="936e1-129">The following table shows the properties that are required when you create the [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md).</span></span>

|<span data-ttu-id="936e1-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="936e1-130">Property</span></span>|<span data-ttu-id="936e1-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="936e1-131">Type</span></span>|<span data-ttu-id="936e1-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="936e1-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="936e1-133">id</span><span class="sxs-lookup"><span data-stu-id="936e1-133">id</span></span>|<span data-ttu-id="936e1-134">String</span><span class="sxs-lookup"><span data-stu-id="936e1-134">String</span></span>|<span data-ttu-id="936e1-135">Identificador único para la secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="936e1-135">Unique Identifier for the device management script.</span></span>|
|<span data-ttu-id="936e1-136">displayName</span><span class="sxs-lookup"><span data-stu-id="936e1-136">displayName</span></span>|<span data-ttu-id="936e1-137">String</span><span class="sxs-lookup"><span data-stu-id="936e1-137">String</span></span>|<span data-ttu-id="936e1-138">Nombre de la secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="936e1-138">Name of the device management script.</span></span>|
|<span data-ttu-id="936e1-139">descripción</span><span class="sxs-lookup"><span data-stu-id="936e1-139">description</span></span>|<span data-ttu-id="936e1-140">String</span><span class="sxs-lookup"><span data-stu-id="936e1-140">String</span></span>|<span data-ttu-id="936e1-141">Descripción opcional de la secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="936e1-141">Optional description for the device management script.</span></span>|
|<span data-ttu-id="936e1-142">runSchedule</span><span class="sxs-lookup"><span data-stu-id="936e1-142">runSchedule</span></span>|[<span data-ttu-id="936e1-143">runSchedule</span><span class="sxs-lookup"><span data-stu-id="936e1-143">runSchedule</span></span>](../resources/intune-devices-runschedule.md)|<span data-ttu-id="936e1-144">El intervalo para ejecutar la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="936e1-144">The interval for script to run.</span></span> <span data-ttu-id="936e1-145">Si no ha definido la secuencia de comandos se ejecutará una vez</span><span class="sxs-lookup"><span data-stu-id="936e1-145">If not defined the script will run once</span></span>|
|<span data-ttu-id="936e1-146">scriptContent</span><span class="sxs-lookup"><span data-stu-id="936e1-146">scriptContent</span></span>|<span data-ttu-id="936e1-147">Binario</span><span class="sxs-lookup"><span data-stu-id="936e1-147">Binary</span></span>|<span data-ttu-id="936e1-148">El contenido de la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="936e1-148">The script content.</span></span>|
|<span data-ttu-id="936e1-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="936e1-149">createdDateTime</span></span>|<span data-ttu-id="936e1-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="936e1-150">DateTimeOffset</span></span>|<span data-ttu-id="936e1-151">La fecha y hora de que creación de la secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="936e1-151">The date and time the device management script was created.</span></span>|
|<span data-ttu-id="936e1-152">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="936e1-152">lastModifiedDateTime</span></span>|<span data-ttu-id="936e1-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="936e1-153">DateTimeOffset</span></span>|<span data-ttu-id="936e1-154">La fecha y hora de que última modificación de la secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="936e1-154">The date and time the device management script was last modified.</span></span>|
|<span data-ttu-id="936e1-155">runAsAccount</span><span class="sxs-lookup"><span data-stu-id="936e1-155">runAsAccount</span></span>|[<span data-ttu-id="936e1-156">runAsAccountType</span><span class="sxs-lookup"><span data-stu-id="936e1-156">runAsAccountType</span></span>](../resources/intune-shared-runasaccounttype.md)|<span data-ttu-id="936e1-157">Indica el tipo de la secuencia de comandos de administración de dispositivos se ejecuta en el contexto de ejecución.</span><span class="sxs-lookup"><span data-stu-id="936e1-157">Indicates the type of execution context the device management script runs in.</span></span> <span data-ttu-id="936e1-158">Los valores posibles son: `system` y `user`.</span><span class="sxs-lookup"><span data-stu-id="936e1-158">Possible values are: `system`, `user`.</span></span>|
|<span data-ttu-id="936e1-159">enforceSignatureCheck</span><span class="sxs-lookup"><span data-stu-id="936e1-159">enforceSignatureCheck</span></span>|<span data-ttu-id="936e1-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="936e1-160">Boolean</span></span>|<span data-ttu-id="936e1-161">Indicar si se debe comprobar la firma de la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="936e1-161">Indicate whether the script signature needs be checked.</span></span>|
|<span data-ttu-id="936e1-162">fileName</span><span class="sxs-lookup"><span data-stu-id="936e1-162">fileName</span></span>|<span data-ttu-id="936e1-163">String</span><span class="sxs-lookup"><span data-stu-id="936e1-163">String</span></span>|<span data-ttu-id="936e1-164">Nombre de archivo de secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="936e1-164">Script file name.</span></span>|



## <a name="response"></a><span data-ttu-id="936e1-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="936e1-165">Response</span></span>
<span data-ttu-id="936e1-166">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="936e1-166">If successful, this method returns a `200 OK` response code and an updated [deviceManagementScript](../resources/intune-devices-devicemanagementscript.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="936e1-167">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="936e1-167">Example</span></span>
### <a name="request"></a><span data-ttu-id="936e1-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="936e1-168">Request</span></span>
<span data-ttu-id="936e1-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="936e1-169">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceManagementScripts/{deviceManagementScriptId}
Content-type: application/json
Content-length: 361

{
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

### <a name="response"></a><span data-ttu-id="936e1-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="936e1-170">Response</span></span>
<span data-ttu-id="936e1-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="936e1-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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





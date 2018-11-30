---
title: Crear deviceManagementScriptDeviceState
description: Crear un nuevo objeto deviceManagementScriptDeviceState.
ms.openlocfilehash: 64594aee75d398fb92a0b7150a07409aa4362126
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087811"
---
# <a name="create-devicemanagementscriptdevicestate"></a><span data-ttu-id="54f5c-103">Crear deviceManagementScriptDeviceState</span><span class="sxs-lookup"><span data-stu-id="54f5c-103">Create deviceManagementScriptDeviceState</span></span>

> <span data-ttu-id="54f5c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="54f5c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="54f5c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="54f5c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="54f5c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="54f5c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="54f5c-107">Crear un nuevo objeto [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) .</span><span class="sxs-lookup"><span data-stu-id="54f5c-107">Create a new [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="54f5c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="54f5c-108">Prerequisites</span></span>
<span data-ttu-id="54f5c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="54f5c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="54f5c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="54f5c-111">Permission type</span></span>|<span data-ttu-id="54f5c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="54f5c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="54f5c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="54f5c-113">Delegated (work or school account)</span></span>|<span data-ttu-id="54f5c-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="54f5c-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="54f5c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="54f5c-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="54f5c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54f5c-116">Not supported.</span></span>|
|<span data-ttu-id="54f5c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="54f5c-117">Application</span></span>|<span data-ttu-id="54f5c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54f5c-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="54f5c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="54f5c-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/userRunStates/{deviceManagementScriptUserStateId}/deviceRunStates
```

## <a name="request-headers"></a><span data-ttu-id="54f5c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="54f5c-120">Request headers</span></span>
|<span data-ttu-id="54f5c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54f5c-121">Header</span></span>|<span data-ttu-id="54f5c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="54f5c-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="54f5c-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="54f5c-123">Authorization</span></span>|<span data-ttu-id="54f5c-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="54f5c-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="54f5c-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="54f5c-125">Accept</span></span>|<span data-ttu-id="54f5c-126">application/json</span><span class="sxs-lookup"><span data-stu-id="54f5c-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="54f5c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="54f5c-127">Request body</span></span>
<span data-ttu-id="54f5c-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto deviceManagementScriptDeviceState.</span><span class="sxs-lookup"><span data-stu-id="54f5c-128">In the request body, supply a JSON representation for the deviceManagementScriptDeviceState object.</span></span>

<span data-ttu-id="54f5c-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el deviceManagementScriptDeviceState.</span><span class="sxs-lookup"><span data-stu-id="54f5c-129">The following table shows the properties that are required when you create the deviceManagementScriptDeviceState.</span></span>

|<span data-ttu-id="54f5c-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="54f5c-130">Property</span></span>|<span data-ttu-id="54f5c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="54f5c-131">Type</span></span>|<span data-ttu-id="54f5c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="54f5c-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="54f5c-133">id</span><span class="sxs-lookup"><span data-stu-id="54f5c-133">id</span></span>|<span data-ttu-id="54f5c-134">String</span><span class="sxs-lookup"><span data-stu-id="54f5c-134">String</span></span>|<span data-ttu-id="54f5c-135">Clave de la entidad de estado de dispositivo de secuencia de comandos de dispositivo administración.</span><span class="sxs-lookup"><span data-stu-id="54f5c-135">Key of the device management script device state entity.</span></span>|
|<span data-ttu-id="54f5c-136">runState</span><span class="sxs-lookup"><span data-stu-id="54f5c-136">runState</span></span>|[<span data-ttu-id="54f5c-137">runState</span><span class="sxs-lookup"><span data-stu-id="54f5c-137">runState</span></span>](../resources/intune-shared-runstate.md)|<span data-ttu-id="54f5c-138">Estado de la última ejecución de la secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="54f5c-138">State of latest run of the device management script.</span></span> <span data-ttu-id="54f5c-139">Los valores posibles son: `unknown`, `success` y `fail`.</span><span class="sxs-lookup"><span data-stu-id="54f5c-139">Possible values are: `unknown`, `success`, `fail`.</span></span>|
|<span data-ttu-id="54f5c-140">resultMessage</span><span class="sxs-lookup"><span data-stu-id="54f5c-140">resultMessage</span></span>|<span data-ttu-id="54f5c-141">String</span><span class="sxs-lookup"><span data-stu-id="54f5c-141">String</span></span>|<span data-ttu-id="54f5c-142">Detalles de los resultados de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="54f5c-142">Details of execution output.</span></span>|
|<span data-ttu-id="54f5c-143">lastStateUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="54f5c-143">lastStateUpdateDateTime</span></span>|<span data-ttu-id="54f5c-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="54f5c-144">DateTimeOffset</span></span>|<span data-ttu-id="54f5c-145">Última vez que se ejecuta la secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="54f5c-145">Latest time the device management script executes.</span></span>|
|<span data-ttu-id="54f5c-146">errorCode</span><span class="sxs-lookup"><span data-stu-id="54f5c-146">errorCode</span></span>|<span data-ttu-id="54f5c-147">Int32</span><span class="sxs-lookup"><span data-stu-id="54f5c-147">Int32</span></span>|<span data-ttu-id="54f5c-148">Código de error correspondiente a la ejecución de la secuencia de comandos de administración de dispositivos con errores.</span><span class="sxs-lookup"><span data-stu-id="54f5c-148">Error code corresponding to erroneous execution of the device management script.</span></span>|
|<span data-ttu-id="54f5c-149">errorDescription</span><span class="sxs-lookup"><span data-stu-id="54f5c-149">errorDescription</span></span>|<span data-ttu-id="54f5c-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="54f5c-150">String</span></span>|<span data-ttu-id="54f5c-151">Descripción del error correspondiente a la ejecución de la secuencia de comandos de administración de dispositivos con errores.</span><span class="sxs-lookup"><span data-stu-id="54f5c-151">Error description corresponding to erroneous execution of the device management script.</span></span>|



## <a name="response"></a><span data-ttu-id="54f5c-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54f5c-152">Response</span></span>
<span data-ttu-id="54f5c-153">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="54f5c-153">If successful, this method returns a `201 Created` response code and a [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="54f5c-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54f5c-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="54f5c-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="54f5c-155">Request</span></span>
<span data-ttu-id="54f5c-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="54f5c-156">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates
Content-type: application/json
Content-length: 281

{
  "@odata.type": "#microsoft.graph.deviceManagementScriptDeviceState",
  "runState": "success",
  "resultMessage": "Result Message value",
  "lastStateUpdateDateTime": "2017-01-01T00:02:58.4418045-08:00",
  "errorCode": 9,
  "errorDescription": "Error Description value"
}
```

### <a name="response"></a><span data-ttu-id="54f5c-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54f5c-157">Response</span></span>
<span data-ttu-id="54f5c-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="54f5c-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 330

{
  "@odata.type": "#microsoft.graph.deviceManagementScriptDeviceState",
  "id": "39440cba-0cba-3944-ba0c-4439ba0c4439",
  "runState": "success",
  "resultMessage": "Result Message value",
  "lastStateUpdateDateTime": "2017-01-01T00:02:58.4418045-08:00",
  "errorCode": 9,
  "errorDescription": "Error Description value"
}
```






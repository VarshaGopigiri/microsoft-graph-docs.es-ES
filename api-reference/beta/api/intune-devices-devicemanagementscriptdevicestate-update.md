---
title: Actualizar deviceManagementScriptDeviceState
description: Actualizar las propiedades de un objeto deviceManagementScriptDeviceState.
ms.openlocfilehash: 790b13615d9f00d1e8441f444aeb0340454de098
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086628"
---
# <a name="update-devicemanagementscriptdevicestate"></a><span data-ttu-id="6e64b-103">Actualizar deviceManagementScriptDeviceState</span><span class="sxs-lookup"><span data-stu-id="6e64b-103">Update deviceManagementScriptDeviceState</span></span>

> <span data-ttu-id="6e64b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6e64b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6e64b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6e64b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6e64b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6e64b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6e64b-107">Actualizar las propiedades de un objeto [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) .</span><span class="sxs-lookup"><span data-stu-id="6e64b-107">Update the properties of a [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6e64b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6e64b-108">Prerequisites</span></span>
<span data-ttu-id="6e64b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6e64b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6e64b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6e64b-111">Permission type</span></span>|<span data-ttu-id="6e64b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6e64b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6e64b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6e64b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="6e64b-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6e64b-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="6e64b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6e64b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6e64b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6e64b-116">Not supported.</span></span>|
|<span data-ttu-id="6e64b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6e64b-117">Application</span></span>|<span data-ttu-id="6e64b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6e64b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6e64b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6e64b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}
PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/userRunStates/{deviceManagementScriptUserStateId}/deviceRunStates/{deviceManagementScriptDeviceStateId}
```

## <a name="request-headers"></a><span data-ttu-id="6e64b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6e64b-120">Request headers</span></span>
|<span data-ttu-id="6e64b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e64b-121">Header</span></span>|<span data-ttu-id="6e64b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6e64b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6e64b-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6e64b-123">Authorization</span></span>|<span data-ttu-id="6e64b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6e64b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6e64b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6e64b-125">Accept</span></span>|<span data-ttu-id="6e64b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6e64b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6e64b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6e64b-127">Request body</span></span>
<span data-ttu-id="6e64b-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) .</span><span class="sxs-lookup"><span data-stu-id="6e64b-128">In the request body, supply a JSON representation for the [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) object.</span></span>

<span data-ttu-id="6e64b-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md).</span><span class="sxs-lookup"><span data-stu-id="6e64b-129">The following table shows the properties that are required when you create the [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md).</span></span>

|<span data-ttu-id="6e64b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6e64b-130">Property</span></span>|<span data-ttu-id="6e64b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e64b-131">Type</span></span>|<span data-ttu-id="6e64b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e64b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6e64b-133">id</span><span class="sxs-lookup"><span data-stu-id="6e64b-133">id</span></span>|<span data-ttu-id="6e64b-134">String</span><span class="sxs-lookup"><span data-stu-id="6e64b-134">String</span></span>|<span data-ttu-id="6e64b-135">Clave de la entidad de estado de dispositivo de secuencia de comandos de dispositivo administración.</span><span class="sxs-lookup"><span data-stu-id="6e64b-135">Key of the device management script device state entity.</span></span>|
|<span data-ttu-id="6e64b-136">runState</span><span class="sxs-lookup"><span data-stu-id="6e64b-136">runState</span></span>|[<span data-ttu-id="6e64b-137">runState</span><span class="sxs-lookup"><span data-stu-id="6e64b-137">runState</span></span>](../resources/intune-shared-runstate.md)|<span data-ttu-id="6e64b-138">Estado de la última ejecución de la secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6e64b-138">State of latest run of the device management script.</span></span> <span data-ttu-id="6e64b-139">Los valores posibles son: `unknown`, `success` y `fail`.</span><span class="sxs-lookup"><span data-stu-id="6e64b-139">Possible values are: `unknown`, `success`, `fail`.</span></span>|
|<span data-ttu-id="6e64b-140">resultMessage</span><span class="sxs-lookup"><span data-stu-id="6e64b-140">resultMessage</span></span>|<span data-ttu-id="6e64b-141">String</span><span class="sxs-lookup"><span data-stu-id="6e64b-141">String</span></span>|<span data-ttu-id="6e64b-142">Detalles de los resultados de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="6e64b-142">Details of execution output.</span></span>|
|<span data-ttu-id="6e64b-143">lastStateUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="6e64b-143">lastStateUpdateDateTime</span></span>|<span data-ttu-id="6e64b-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6e64b-144">DateTimeOffset</span></span>|<span data-ttu-id="6e64b-145">Última vez que se ejecuta la secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6e64b-145">Latest time the device management script executes.</span></span>|
|<span data-ttu-id="6e64b-146">errorCode</span><span class="sxs-lookup"><span data-stu-id="6e64b-146">errorCode</span></span>|<span data-ttu-id="6e64b-147">Int32</span><span class="sxs-lookup"><span data-stu-id="6e64b-147">Int32</span></span>|<span data-ttu-id="6e64b-148">Código de error correspondiente a la ejecución de la secuencia de comandos de administración de dispositivos con errores.</span><span class="sxs-lookup"><span data-stu-id="6e64b-148">Error code corresponding to erroneous execution of the device management script.</span></span>|
|<span data-ttu-id="6e64b-149">errorDescription</span><span class="sxs-lookup"><span data-stu-id="6e64b-149">errorDescription</span></span>|<span data-ttu-id="6e64b-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="6e64b-150">String</span></span>|<span data-ttu-id="6e64b-151">Descripción del error correspondiente a la ejecución de la secuencia de comandos de administración de dispositivos con errores.</span><span class="sxs-lookup"><span data-stu-id="6e64b-151">Error description corresponding to erroneous execution of the device management script.</span></span>|



## <a name="response"></a><span data-ttu-id="6e64b-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e64b-152">Response</span></span>
<span data-ttu-id="6e64b-153">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6e64b-153">If successful, this method returns a `200 OK` response code and an updated [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6e64b-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6e64b-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="6e64b-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6e64b-155">Request</span></span>
<span data-ttu-id="6e64b-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6e64b-156">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}
Content-type: application/json
Content-length: 209

{
  "runState": "success",
  "resultMessage": "Result Message value",
  "lastStateUpdateDateTime": "2017-01-01T00:02:58.4418045-08:00",
  "errorCode": 9,
  "errorDescription": "Error Description value"
}
```

### <a name="response"></a><span data-ttu-id="6e64b-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e64b-157">Response</span></span>
<span data-ttu-id="6e64b-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6e64b-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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






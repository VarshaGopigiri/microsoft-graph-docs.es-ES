---
title: Actualizar deviceManagementScriptDeviceState
description: Actualizar las propiedades de un objeto deviceManagementScriptDeviceState.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 857c1cca958088c1c884cb06b7f6e8416b3d8f1e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27983768"
---
# <a name="update-devicemanagementscriptdevicestate"></a><span data-ttu-id="fce1f-103">Actualizar deviceManagementScriptDeviceState</span><span class="sxs-lookup"><span data-stu-id="fce1f-103">Update deviceManagementScriptDeviceState</span></span>

> <span data-ttu-id="fce1f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fce1f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fce1f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fce1f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="fce1f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fce1f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fce1f-107">Actualizar las propiedades de un objeto [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) .</span><span class="sxs-lookup"><span data-stu-id="fce1f-107">Update the properties of a [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fce1f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fce1f-108">Prerequisites</span></span>
<span data-ttu-id="fce1f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fce1f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fce1f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fce1f-111">Permission type</span></span>|<span data-ttu-id="fce1f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fce1f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fce1f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fce1f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="fce1f-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fce1f-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="fce1f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fce1f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fce1f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fce1f-116">Not supported.</span></span>|
|<span data-ttu-id="fce1f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fce1f-117">Application</span></span>|<span data-ttu-id="fce1f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fce1f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fce1f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fce1f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}
PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/userRunStates/{deviceManagementScriptUserStateId}/deviceRunStates/{deviceManagementScriptDeviceStateId}
```

## <a name="request-headers"></a><span data-ttu-id="fce1f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fce1f-120">Request headers</span></span>
|<span data-ttu-id="fce1f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fce1f-121">Header</span></span>|<span data-ttu-id="fce1f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fce1f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fce1f-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="fce1f-123">Authorization</span></span>|<span data-ttu-id="fce1f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fce1f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fce1f-125">Accept</span><span class="sxs-lookup"><span data-stu-id="fce1f-125">Accept</span></span>|<span data-ttu-id="fce1f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="fce1f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fce1f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fce1f-127">Request body</span></span>
<span data-ttu-id="fce1f-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) .</span><span class="sxs-lookup"><span data-stu-id="fce1f-128">In the request body, supply a JSON representation for the [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) object.</span></span>

<span data-ttu-id="fce1f-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md).</span><span class="sxs-lookup"><span data-stu-id="fce1f-129">The following table shows the properties that are required when you create the [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md).</span></span>

|<span data-ttu-id="fce1f-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fce1f-130">Property</span></span>|<span data-ttu-id="fce1f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="fce1f-131">Type</span></span>|<span data-ttu-id="fce1f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="fce1f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fce1f-133">id</span><span class="sxs-lookup"><span data-stu-id="fce1f-133">id</span></span>|<span data-ttu-id="fce1f-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="fce1f-134">String</span></span>|<span data-ttu-id="fce1f-135">Clave de la entidad de estado de dispositivo de secuencia de comandos de dispositivo administración.</span><span class="sxs-lookup"><span data-stu-id="fce1f-135">Key of the device management script device state entity.</span></span>|
|<span data-ttu-id="fce1f-136">runState</span><span class="sxs-lookup"><span data-stu-id="fce1f-136">runState</span></span>|[<span data-ttu-id="fce1f-137">runState</span><span class="sxs-lookup"><span data-stu-id="fce1f-137">runState</span></span>](../resources/intune-shared-runstate.md)|<span data-ttu-id="fce1f-138">Estado de la última ejecución de la secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="fce1f-138">State of latest run of the device management script.</span></span> <span data-ttu-id="fce1f-139">Los valores posibles son: `unknown`, `success` y `fail`.</span><span class="sxs-lookup"><span data-stu-id="fce1f-139">Possible values are: `unknown`, `success`, `fail`.</span></span>|
|<span data-ttu-id="fce1f-140">resultMessage</span><span class="sxs-lookup"><span data-stu-id="fce1f-140">resultMessage</span></span>|<span data-ttu-id="fce1f-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="fce1f-141">String</span></span>|<span data-ttu-id="fce1f-142">Detalles de los resultados de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="fce1f-142">Details of execution output.</span></span>|
|<span data-ttu-id="fce1f-143">lastStateUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="fce1f-143">lastStateUpdateDateTime</span></span>|<span data-ttu-id="fce1f-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fce1f-144">DateTimeOffset</span></span>|<span data-ttu-id="fce1f-145">Última vez que se ejecuta la secuencia de comandos de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="fce1f-145">Latest time the device management script executes.</span></span>|
|<span data-ttu-id="fce1f-146">errorCode</span><span class="sxs-lookup"><span data-stu-id="fce1f-146">errorCode</span></span>|<span data-ttu-id="fce1f-147">Int32</span><span class="sxs-lookup"><span data-stu-id="fce1f-147">Int32</span></span>|<span data-ttu-id="fce1f-148">Código de error correspondiente a la ejecución de la secuencia de comandos de administración de dispositivos con errores.</span><span class="sxs-lookup"><span data-stu-id="fce1f-148">Error code corresponding to erroneous execution of the device management script.</span></span>|
|<span data-ttu-id="fce1f-149">errorDescription</span><span class="sxs-lookup"><span data-stu-id="fce1f-149">errorDescription</span></span>|<span data-ttu-id="fce1f-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="fce1f-150">String</span></span>|<span data-ttu-id="fce1f-151">Descripción del error correspondiente a la ejecución de la secuencia de comandos de administración de dispositivos con errores.</span><span class="sxs-lookup"><span data-stu-id="fce1f-151">Error description corresponding to erroneous execution of the device management script.</span></span>|



## <a name="response"></a><span data-ttu-id="fce1f-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fce1f-152">Response</span></span>
<span data-ttu-id="fce1f-153">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fce1f-153">If successful, this method returns a `200 OK` response code and an updated [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fce1f-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fce1f-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="fce1f-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fce1f-155">Request</span></span>
<span data-ttu-id="fce1f-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fce1f-156">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="fce1f-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fce1f-157">Response</span></span>
<span data-ttu-id="fce1f-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fce1f-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






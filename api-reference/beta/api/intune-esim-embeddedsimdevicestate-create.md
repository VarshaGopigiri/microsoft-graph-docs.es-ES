---
title: Crear embeddedSIMDeviceState
description: Crear un nuevo objeto embeddedSIMDeviceState.
ms.openlocfilehash: 3d52c8910d38f72e9c08e27fe694cea49796b884
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089652"
---
# <a name="create-embeddedsimdevicestate"></a><span data-ttu-id="c53b3-103">Crear embeddedSIMDeviceState</span><span class="sxs-lookup"><span data-stu-id="c53b3-103">Create embeddedSIMDeviceState</span></span>

> <span data-ttu-id="c53b3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c53b3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c53b3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c53b3-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c53b3-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c53b3-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c53b3-107">Crear un nuevo objeto [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) .</span><span class="sxs-lookup"><span data-stu-id="c53b3-107">Create a new [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c53b3-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c53b3-108">Prerequisites</span></span>
<span data-ttu-id="c53b3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c53b3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c53b3-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c53b3-111">Permission type</span></span>|<span data-ttu-id="c53b3-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c53b3-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c53b3-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c53b3-113">Delegated (work or school account)</span></span>|<span data-ttu-id="c53b3-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c53b3-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="c53b3-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c53b3-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c53b3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c53b3-116">Not supported.</span></span>|
|<span data-ttu-id="c53b3-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c53b3-117">Application</span></span>|<span data-ttu-id="c53b3-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c53b3-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c53b3-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c53b3-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/embeddedSIMActivationCodePools/{embeddedSIMActivationCodePoolId}/deviceStates
```

## <a name="request-headers"></a><span data-ttu-id="c53b3-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c53b3-120">Request headers</span></span>
|<span data-ttu-id="c53b3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c53b3-121">Header</span></span>|<span data-ttu-id="c53b3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c53b3-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c53b3-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="c53b3-123">Authorization</span></span>|<span data-ttu-id="c53b3-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c53b3-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c53b3-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c53b3-125">Accept</span></span>|<span data-ttu-id="c53b3-126">application/json</span><span class="sxs-lookup"><span data-stu-id="c53b3-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c53b3-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c53b3-127">Request body</span></span>
<span data-ttu-id="c53b3-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto embeddedSIMDeviceState.</span><span class="sxs-lookup"><span data-stu-id="c53b3-128">In the request body, supply a JSON representation for the embeddedSIMDeviceState object.</span></span>

<span data-ttu-id="c53b3-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el embeddedSIMDeviceState.</span><span class="sxs-lookup"><span data-stu-id="c53b3-129">The following table shows the properties that are required when you create the embeddedSIMDeviceState.</span></span>

|<span data-ttu-id="c53b3-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c53b3-130">Property</span></span>|<span data-ttu-id="c53b3-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c53b3-131">Type</span></span>|<span data-ttu-id="c53b3-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c53b3-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c53b3-133">id</span><span class="sxs-lookup"><span data-stu-id="c53b3-133">id</span></span>|<span data-ttu-id="c53b3-134">String</span><span class="sxs-lookup"><span data-stu-id="c53b3-134">String</span></span>|<span data-ttu-id="c53b3-135">Identificador único para el estado del dispositivo SIM incrustado.</span><span class="sxs-lookup"><span data-stu-id="c53b3-135">Unique identifier for the embedded SIM device status.</span></span> <span data-ttu-id="c53b3-136">Valor asignado al crear generada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="c53b3-136">System generated value assigned when created.</span></span>|
|<span data-ttu-id="c53b3-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c53b3-137">createdDateTime</span></span>|<span data-ttu-id="c53b3-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c53b3-138">DateTimeOffset</span></span>|<span data-ttu-id="c53b3-139">La hora en que se creó el estado del dispositivo SIM incrustado.</span><span class="sxs-lookup"><span data-stu-id="c53b3-139">The time the embedded SIM device status was created.</span></span> <span data-ttu-id="c53b3-140">Servicio generado al lado.</span><span class="sxs-lookup"><span data-stu-id="c53b3-140">Generated service side.</span></span>|
|<span data-ttu-id="c53b3-141">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="c53b3-141">modifiedDateTime</span></span>|<span data-ttu-id="c53b3-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c53b3-142">DateTimeOffset</span></span>|<span data-ttu-id="c53b3-143">La hora en que se modificó por última vez el estado del dispositivo SIM incrustado.</span><span class="sxs-lookup"><span data-stu-id="c53b3-143">The time the embedded SIM device status was last modified.</span></span> <span data-ttu-id="c53b3-144">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="c53b3-144">Updated service side.</span></span>|
|<span data-ttu-id="c53b3-145">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="c53b3-145">lastSyncDateTime</span></span>|<span data-ttu-id="c53b3-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c53b3-146">DateTimeOffset</span></span>|<span data-ttu-id="c53b3-147">El tiempo que el dispositivo SIM incrustado protegida por última vez.</span><span class="sxs-lookup"><span data-stu-id="c53b3-147">The time the embedded SIM device last checked in.</span></span> <span data-ttu-id="c53b3-148">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="c53b3-148">Updated service side.</span></span>|
|<span data-ttu-id="c53b3-149">universalIntegratedCircuitCardIdentifier</span><span class="sxs-lookup"><span data-stu-id="c53b3-149">universalIntegratedCircuitCardIdentifier</span></span>|<span data-ttu-id="c53b3-150">String</span><span class="sxs-lookup"><span data-stu-id="c53b3-150">String</span></span>|<span data-ttu-id="c53b3-151">La Universal circuito integrado tarjeta de identificador (UICCID) que identifica el hardware en el que es un perfil que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="c53b3-151">The Universal Integrated Circuit Card Identifier (UICCID) identifying the hardware onto which a profile is to be deployed.</span></span>|
|<span data-ttu-id="c53b3-152">deviceName</span><span class="sxs-lookup"><span data-stu-id="c53b3-152">deviceName</span></span>|<span data-ttu-id="c53b3-153">String</span><span class="sxs-lookup"><span data-stu-id="c53b3-153">String</span></span>|<span data-ttu-id="c53b3-154">Nombre de dispositivo al que estaba la suscripción a aprovisiona a JOE de escritorio, por ejemplo</span><span class="sxs-lookup"><span data-stu-id="c53b3-154">Device name to which the subscription was provisioned e.g. DESKTOP-JOE</span></span>|
|<span data-ttu-id="c53b3-155">userName</span><span class="sxs-lookup"><span data-stu-id="c53b3-155">userName</span></span>|<span data-ttu-id="c53b3-156">String</span><span class="sxs-lookup"><span data-stu-id="c53b3-156">String</span></span>|<span data-ttu-id="c53b3-157">Nombre de usuario que se aprovisionó la suscripción como, por ejemplo, joe@contoso.com</span><span class="sxs-lookup"><span data-stu-id="c53b3-157">Username which the subscription was provisioned to e.g. joe@contoso.com</span></span>|
|<span data-ttu-id="c53b3-158">estado</span><span class="sxs-lookup"><span data-stu-id="c53b3-158">state</span></span>|[<span data-ttu-id="c53b3-159">embeddedSIMDeviceStateValue</span><span class="sxs-lookup"><span data-stu-id="c53b3-159">embeddedSIMDeviceStateValue</span></span>](../resources/intune-esim-embeddedsimdevicestatevalue.md)|<span data-ttu-id="c53b3-160">El estado de la operación de perfil aplicada al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c53b3-160">The state of the profile operation applied to the device.</span></span> <span data-ttu-id="c53b3-161">Los valores posibles son: `notEvaluated`, `failed`, `installing`, `installed`, `deleting`, `error`, `deleted` y `removedByUser`.</span><span class="sxs-lookup"><span data-stu-id="c53b3-161">Possible values are: `notEvaluated`, `failed`, `installing`, `installed`, `deleting`, `error`, `deleted`, `removedByUser`.</span></span>|
|<span data-ttu-id="c53b3-162">stateDetails</span><span class="sxs-lookup"><span data-stu-id="c53b3-162">stateDetails</span></span>|<span data-ttu-id="c53b3-163">String</span><span class="sxs-lookup"><span data-stu-id="c53b3-163">String</span></span>|<span data-ttu-id="c53b3-164">Descripción del estado de aprovisionamiento de la cadena.</span><span class="sxs-lookup"><span data-stu-id="c53b3-164">String description of the provisioning state.</span></span>|



## <a name="response"></a><span data-ttu-id="c53b3-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c53b3-165">Response</span></span>
<span data-ttu-id="c53b3-166">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c53b3-166">If successful, this method returns a `201 Created` response code and a [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c53b3-167">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c53b3-167">Example</span></span>
### <a name="request"></a><span data-ttu-id="c53b3-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c53b3-168">Request</span></span>
<span data-ttu-id="c53b3-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c53b3-169">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/embeddedSIMActivationCodePools/{embeddedSIMActivationCodePoolId}/deviceStates
Content-type: application/json
Content-length: 361

{
  "@odata.type": "#microsoft.graph.embeddedSIMDeviceState",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "universalIntegratedCircuitCardIdentifier": "Universal Integrated Circuit Card Identifier value",
  "deviceName": "Device Name value",
  "userName": "User Name value",
  "state": "failed",
  "stateDetails": "State Details value"
}
```

### <a name="response"></a><span data-ttu-id="c53b3-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c53b3-170">Response</span></span>
<span data-ttu-id="c53b3-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c53b3-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 529

{
  "@odata.type": "#microsoft.graph.embeddedSIMDeviceState",
  "id": "908884a3-84a3-9088-a384-8890a3848890",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "modifiedDateTime": "2017-01-01T00:00:22.8983556-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "universalIntegratedCircuitCardIdentifier": "Universal Integrated Circuit Card Identifier value",
  "deviceName": "Device Name value",
  "userName": "User Name value",
  "state": "failed",
  "stateDetails": "State Details value"
}
```






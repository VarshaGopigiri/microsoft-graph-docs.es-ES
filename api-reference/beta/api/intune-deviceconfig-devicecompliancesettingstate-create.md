---
title: Crear deviceComplianceSettingState
description: Cree un objeto deviceComplianceSettingState.
ms.openlocfilehash: cb5f4ba5a71b9c7887dabdbf1c51c7665db26d70
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090788"
---
# <a name="create-devicecompliancesettingstate"></a><span data-ttu-id="832f2-103">Crear deviceComplianceSettingState</span><span class="sxs-lookup"><span data-stu-id="832f2-103">Create deviceComplianceSettingState</span></span>

> <span data-ttu-id="832f2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="832f2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="832f2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="832f2-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="832f2-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="832f2-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="832f2-107">Cree un objeto [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md).</span><span class="sxs-lookup"><span data-stu-id="832f2-107">Create a new [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="832f2-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="832f2-108">Prerequisites</span></span>
<span data-ttu-id="832f2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="832f2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="832f2-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="832f2-111">Permission type</span></span>|<span data-ttu-id="832f2-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="832f2-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="832f2-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="832f2-113">Delegated (work or school account)</span></span>|<span data-ttu-id="832f2-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="832f2-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="832f2-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="832f2-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="832f2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="832f2-116">Not supported.</span></span>|
|<span data-ttu-id="832f2-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="832f2-117">Application</span></span>|<span data-ttu-id="832f2-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="832f2-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="832f2-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="832f2-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates
```

## <a name="request-headers"></a><span data-ttu-id="832f2-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="832f2-120">Request headers</span></span>
|<span data-ttu-id="832f2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="832f2-121">Header</span></span>|<span data-ttu-id="832f2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="832f2-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="832f2-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="832f2-123">Authorization</span></span>|<span data-ttu-id="832f2-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="832f2-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="832f2-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="832f2-125">Accept</span></span>|<span data-ttu-id="832f2-126">application/json</span><span class="sxs-lookup"><span data-stu-id="832f2-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="832f2-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="832f2-127">Request body</span></span>
<span data-ttu-id="832f2-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceComplianceSettingState.</span><span class="sxs-lookup"><span data-stu-id="832f2-128">In the request body, supply a JSON representation for the deviceComplianceSettingState object.</span></span>

<span data-ttu-id="832f2-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceComplianceSettingState.</span><span class="sxs-lookup"><span data-stu-id="832f2-129">The following table shows the properties that are required when you create the deviceComplianceSettingState.</span></span>

|<span data-ttu-id="832f2-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="832f2-130">Property</span></span>|<span data-ttu-id="832f2-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="832f2-131">Type</span></span>|<span data-ttu-id="832f2-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="832f2-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="832f2-133">id</span><span class="sxs-lookup"><span data-stu-id="832f2-133">id</span></span>|<span data-ttu-id="832f2-134">String</span><span class="sxs-lookup"><span data-stu-id="832f2-134">String</span></span>|<span data-ttu-id="832f2-135">Clave de la entidad</span><span class="sxs-lookup"><span data-stu-id="832f2-135">Key of the entity</span></span>|
|<span data-ttu-id="832f2-136">platformType</span><span class="sxs-lookup"><span data-stu-id="832f2-136">platformType</span></span>|[<span data-ttu-id="832f2-137">deviceType</span><span class="sxs-lookup"><span data-stu-id="832f2-137">deviceType</span></span>](../resources/intune-shared-devicetype.md)|<span data-ttu-id="832f2-138">Tipo de plataforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="832f2-138">Device platform type.</span></span> <span data-ttu-id="832f2-139">Los valores posibles son: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise` , `blackberry`, `palm`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="832f2-139">Possible values are: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise`, `blackberry`, `palm`, `unknown`.</span></span>|
|<span data-ttu-id="832f2-140">ajustes</span><span class="sxs-lookup"><span data-stu-id="832f2-140">setting</span></span>|<span data-ttu-id="832f2-141">String</span><span class="sxs-lookup"><span data-stu-id="832f2-141">String</span></span>|<span data-ttu-id="832f2-142">El nombre de la clase de configuración y el nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="832f2-142">The setting class name and property name.</span></span>|
|<span data-ttu-id="832f2-143">settingName</span><span class="sxs-lookup"><span data-stu-id="832f2-143">settingName</span></span>|<span data-ttu-id="832f2-144">String</span><span class="sxs-lookup"><span data-stu-id="832f2-144">String</span></span>|<span data-ttu-id="832f2-145">El nombre de configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="832f2-145">The Setting Name that is being reported</span></span>|
|<span data-ttu-id="832f2-146">deviceId</span><span class="sxs-lookup"><span data-stu-id="832f2-146">deviceId</span></span>|<span data-ttu-id="832f2-147">String</span><span class="sxs-lookup"><span data-stu-id="832f2-147">String</span></span>|<span data-ttu-id="832f2-148">El identificador del dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="832f2-148">The Device Id that is being reported</span></span>|
|<span data-ttu-id="832f2-149">deviceName</span><span class="sxs-lookup"><span data-stu-id="832f2-149">deviceName</span></span>|<span data-ttu-id="832f2-150">String</span><span class="sxs-lookup"><span data-stu-id="832f2-150">String</span></span>|<span data-ttu-id="832f2-151">El nombre del dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="832f2-151">The Device Name that is being reported</span></span>|
|<span data-ttu-id="832f2-152">userId</span><span class="sxs-lookup"><span data-stu-id="832f2-152">userId</span></span>|<span data-ttu-id="832f2-153">String</span><span class="sxs-lookup"><span data-stu-id="832f2-153">String</span></span>|<span data-ttu-id="832f2-154">El identificador del usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="832f2-154">The user Id that is being reported</span></span>|
|<span data-ttu-id="832f2-155">userEmail</span><span class="sxs-lookup"><span data-stu-id="832f2-155">userEmail</span></span>|<span data-ttu-id="832f2-156">String</span><span class="sxs-lookup"><span data-stu-id="832f2-156">String</span></span>|<span data-ttu-id="832f2-157">La dirección de correo electrónico del usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="832f2-157">The User email address that is being reported</span></span>|
|<span data-ttu-id="832f2-158">userName</span><span class="sxs-lookup"><span data-stu-id="832f2-158">userName</span></span>|<span data-ttu-id="832f2-159">String</span><span class="sxs-lookup"><span data-stu-id="832f2-159">String</span></span>|<span data-ttu-id="832f2-160">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="832f2-160">The User Name that is being reported</span></span>|
|<span data-ttu-id="832f2-161">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="832f2-161">userPrincipalName</span></span>|<span data-ttu-id="832f2-162">String</span><span class="sxs-lookup"><span data-stu-id="832f2-162">String</span></span>|<span data-ttu-id="832f2-163">El nombre principal de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="832f2-163">The User PrincipalName that is being reported</span></span>|
|<span data-ttu-id="832f2-164">deviceModel</span><span class="sxs-lookup"><span data-stu-id="832f2-164">deviceModel</span></span>|<span data-ttu-id="832f2-165">String</span><span class="sxs-lookup"><span data-stu-id="832f2-165">String</span></span>|<span data-ttu-id="832f2-166">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="832f2-166">The device model that is being reported</span></span>|
|<span data-ttu-id="832f2-167">estado</span><span class="sxs-lookup"><span data-stu-id="832f2-167">state</span></span>|[<span data-ttu-id="832f2-168">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="832f2-168">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="832f2-169">El estado de cumplimiento de la configuración.</span><span class="sxs-lookup"><span data-stu-id="832f2-169">The compliance state of the setting.</span></span> <span data-ttu-id="832f2-170">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="832f2-170">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="832f2-171">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="832f2-171">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="832f2-172">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="832f2-172">DateTimeOffset</span></span>|<span data-ttu-id="832f2-173">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="832f2-173">The DateTime when device compliance grace period expires</span></span>|



## <a name="response"></a><span data-ttu-id="832f2-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="832f2-174">Response</span></span>
<span data-ttu-id="832f2-175">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="832f2-175">If successful, this method returns a `201 Created` response code and a [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="832f2-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="832f2-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="832f2-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="832f2-177">Request</span></span>
<span data-ttu-id="832f2-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="832f2-178">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates
Content-type: application/json
Content-length: 549

{
  "@odata.type": "#microsoft.graph.deviceComplianceSettingState",
  "platformType": "windowsRT",
  "setting": "Setting value",
  "settingName": "Setting Name value",
  "deviceId": "Device Id value",
  "deviceName": "Device Name value",
  "userId": "User Id value",
  "userEmail": "User Email value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value",
  "deviceModel": "Device Model value",
  "state": "notApplicable",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00"
}
```

### <a name="response"></a><span data-ttu-id="832f2-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="832f2-179">Response</span></span>
<span data-ttu-id="832f2-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="832f2-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 598

{
  "@odata.type": "#microsoft.graph.deviceComplianceSettingState",
  "id": "9905f955-f955-9905-55f9-059955f90599",
  "platformType": "windowsRT",
  "setting": "Setting value",
  "settingName": "Setting Name value",
  "deviceId": "Device Id value",
  "deviceName": "Device Name value",
  "userId": "User Id value",
  "userEmail": "User Email value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value",
  "deviceModel": "Device Model value",
  "state": "notApplicable",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00"
}
```






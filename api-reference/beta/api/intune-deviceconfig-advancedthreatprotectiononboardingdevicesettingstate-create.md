---
title: Crear advancedThreatProtectionOnboardingDeviceSettingState
description: Crear un nuevo objeto advancedThreatProtectionOnboardingDeviceSettingState.
ms.openlocfilehash: 623db746a44792f80255b1f76d3d92fca0ab30cb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087275"
---
# <a name="create-advancedthreatprotectiononboardingdevicesettingstate"></a><span data-ttu-id="13e42-103">Crear advancedThreatProtectionOnboardingDeviceSettingState</span><span class="sxs-lookup"><span data-stu-id="13e42-103">Create advancedThreatProtectionOnboardingDeviceSettingState</span></span>

> <span data-ttu-id="13e42-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="13e42-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="13e42-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="13e42-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="13e42-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="13e42-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="13e42-107">Crear un nuevo objeto [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) .</span><span class="sxs-lookup"><span data-stu-id="13e42-107">Create a new [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="13e42-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="13e42-108">Prerequisites</span></span>
<span data-ttu-id="13e42-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="13e42-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="13e42-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="13e42-111">Permission type</span></span>|<span data-ttu-id="13e42-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="13e42-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="13e42-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="13e42-113">Delegated (work or school account)</span></span>|<span data-ttu-id="13e42-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="13e42-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="13e42-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="13e42-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="13e42-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="13e42-116">Not supported.</span></span>|
|<span data-ttu-id="13e42-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="13e42-117">Application</span></span>|<span data-ttu-id="13e42-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="13e42-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="13e42-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="13e42-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/advancedThreatProtectionOnboardingStateSummary/advancedThreatProtectionOnboardingDeviceSettingStates
```

## <a name="request-headers"></a><span data-ttu-id="13e42-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="13e42-120">Request headers</span></span>
|<span data-ttu-id="13e42-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13e42-121">Header</span></span>|<span data-ttu-id="13e42-122">Valor</span><span class="sxs-lookup"><span data-stu-id="13e42-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="13e42-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="13e42-123">Authorization</span></span>|<span data-ttu-id="13e42-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="13e42-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="13e42-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="13e42-125">Accept</span></span>|<span data-ttu-id="13e42-126">application/json</span><span class="sxs-lookup"><span data-stu-id="13e42-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="13e42-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="13e42-127">Request body</span></span>
<span data-ttu-id="13e42-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto advancedThreatProtectionOnboardingDeviceSettingState.</span><span class="sxs-lookup"><span data-stu-id="13e42-128">In the request body, supply a JSON representation for the advancedThreatProtectionOnboardingDeviceSettingState object.</span></span>

<span data-ttu-id="13e42-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el advancedThreatProtectionOnboardingDeviceSettingState.</span><span class="sxs-lookup"><span data-stu-id="13e42-129">The following table shows the properties that are required when you create the advancedThreatProtectionOnboardingDeviceSettingState.</span></span>

|<span data-ttu-id="13e42-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="13e42-130">Property</span></span>|<span data-ttu-id="13e42-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="13e42-131">Type</span></span>|<span data-ttu-id="13e42-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="13e42-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="13e42-133">id</span><span class="sxs-lookup"><span data-stu-id="13e42-133">id</span></span>|<span data-ttu-id="13e42-134">String</span><span class="sxs-lookup"><span data-stu-id="13e42-134">String</span></span>|<span data-ttu-id="13e42-135">Clave de la entidad</span><span class="sxs-lookup"><span data-stu-id="13e42-135">Key of the entity</span></span>|
|<span data-ttu-id="13e42-136">platformType</span><span class="sxs-lookup"><span data-stu-id="13e42-136">platformType</span></span>|[<span data-ttu-id="13e42-137">deviceType</span><span class="sxs-lookup"><span data-stu-id="13e42-137">deviceType</span></span>](../resources/intune-shared-devicetype.md)|<span data-ttu-id="13e42-138">Tipo de plataforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13e42-138">Device platform type.</span></span> <span data-ttu-id="13e42-139">Los valores posibles son: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise` , `blackberry`, `palm`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="13e42-139">Possible values are: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise`, `blackberry`, `palm`, `unknown`.</span></span>|
|<span data-ttu-id="13e42-140">ajustes</span><span class="sxs-lookup"><span data-stu-id="13e42-140">setting</span></span>|<span data-ttu-id="13e42-141">String</span><span class="sxs-lookup"><span data-stu-id="13e42-141">String</span></span>|<span data-ttu-id="13e42-142">El nombre de la clase de configuración y el nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="13e42-142">The setting class name and property name.</span></span>|
|<span data-ttu-id="13e42-143">settingName</span><span class="sxs-lookup"><span data-stu-id="13e42-143">settingName</span></span>|<span data-ttu-id="13e42-144">String</span><span class="sxs-lookup"><span data-stu-id="13e42-144">String</span></span>|<span data-ttu-id="13e42-145">El nombre de configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="13e42-145">The Setting Name that is being reported</span></span>|
|<span data-ttu-id="13e42-146">deviceId</span><span class="sxs-lookup"><span data-stu-id="13e42-146">deviceId</span></span>|<span data-ttu-id="13e42-147">String</span><span class="sxs-lookup"><span data-stu-id="13e42-147">String</span></span>|<span data-ttu-id="13e42-148">El identificador del dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="13e42-148">The Device Id that is being reported</span></span>|
|<span data-ttu-id="13e42-149">deviceName</span><span class="sxs-lookup"><span data-stu-id="13e42-149">deviceName</span></span>|<span data-ttu-id="13e42-150">String</span><span class="sxs-lookup"><span data-stu-id="13e42-150">String</span></span>|<span data-ttu-id="13e42-151">El nombre del dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="13e42-151">The Device Name that is being reported</span></span>|
|<span data-ttu-id="13e42-152">userId</span><span class="sxs-lookup"><span data-stu-id="13e42-152">userId</span></span>|<span data-ttu-id="13e42-153">String</span><span class="sxs-lookup"><span data-stu-id="13e42-153">String</span></span>|<span data-ttu-id="13e42-154">El identificador del usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="13e42-154">The user Id that is being reported</span></span>|
|<span data-ttu-id="13e42-155">userEmail</span><span class="sxs-lookup"><span data-stu-id="13e42-155">userEmail</span></span>|<span data-ttu-id="13e42-156">String</span><span class="sxs-lookup"><span data-stu-id="13e42-156">String</span></span>|<span data-ttu-id="13e42-157">La dirección de correo electrónico del usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="13e42-157">The User email address that is being reported</span></span>|
|<span data-ttu-id="13e42-158">userName</span><span class="sxs-lookup"><span data-stu-id="13e42-158">userName</span></span>|<span data-ttu-id="13e42-159">String</span><span class="sxs-lookup"><span data-stu-id="13e42-159">String</span></span>|<span data-ttu-id="13e42-160">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="13e42-160">The User Name that is being reported</span></span>|
|<span data-ttu-id="13e42-161">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="13e42-161">userPrincipalName</span></span>|<span data-ttu-id="13e42-162">String</span><span class="sxs-lookup"><span data-stu-id="13e42-162">String</span></span>|<span data-ttu-id="13e42-163">El nombre principal de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="13e42-163">The User PrincipalName that is being reported</span></span>|
|<span data-ttu-id="13e42-164">deviceModel</span><span class="sxs-lookup"><span data-stu-id="13e42-164">deviceModel</span></span>|<span data-ttu-id="13e42-165">String</span><span class="sxs-lookup"><span data-stu-id="13e42-165">String</span></span>|<span data-ttu-id="13e42-166">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="13e42-166">The device model that is being reported</span></span>|
|<span data-ttu-id="13e42-167">estado</span><span class="sxs-lookup"><span data-stu-id="13e42-167">state</span></span>|[<span data-ttu-id="13e42-168">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="13e42-168">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="13e42-169">El estado de cumplimiento de la configuración.</span><span class="sxs-lookup"><span data-stu-id="13e42-169">The compliance state of the setting.</span></span> <span data-ttu-id="13e42-170">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="13e42-170">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="13e42-171">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="13e42-171">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="13e42-172">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="13e42-172">DateTimeOffset</span></span>|<span data-ttu-id="13e42-173">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="13e42-173">The DateTime when device compliance grace period expires</span></span>|



## <a name="response"></a><span data-ttu-id="13e42-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13e42-174">Response</span></span>
<span data-ttu-id="13e42-175">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="13e42-175">If successful, this method returns a `201 Created` response code and a [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="13e42-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="13e42-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="13e42-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="13e42-177">Request</span></span>
<span data-ttu-id="13e42-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="13e42-178">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/advancedThreatProtectionOnboardingStateSummary/advancedThreatProtectionOnboardingDeviceSettingStates
Content-type: application/json
Content-length: 573

{
  "@odata.type": "#microsoft.graph.advancedThreatProtectionOnboardingDeviceSettingState",
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

### <a name="response"></a><span data-ttu-id="13e42-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13e42-179">Response</span></span>
<span data-ttu-id="13e42-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="13e42-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 622

{
  "@odata.type": "#microsoft.graph.advancedThreatProtectionOnboardingDeviceSettingState",
  "id": "63593fc6-3fc6-6359-c63f-5963c63f5963",
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






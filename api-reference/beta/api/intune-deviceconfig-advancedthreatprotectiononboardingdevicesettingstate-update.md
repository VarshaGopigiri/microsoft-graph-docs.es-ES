---
title: Actualizar advancedThreatProtectionOnboardingDeviceSettingState
description: Actualizar las propiedades de un objeto advancedThreatProtectionOnboardingDeviceSettingState.
author: tfitzmac
ms.openlocfilehash: 0194eca0c9d36c7d0e4e24cca6eb276beb7d49e3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321696"
---
# <a name="update-advancedthreatprotectiononboardingdevicesettingstate"></a><span data-ttu-id="a8c70-103">Actualizar advancedThreatProtectionOnboardingDeviceSettingState</span><span class="sxs-lookup"><span data-stu-id="a8c70-103">Update advancedThreatProtectionOnboardingDeviceSettingState</span></span>

> <span data-ttu-id="a8c70-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a8c70-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a8c70-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a8c70-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a8c70-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a8c70-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a8c70-107">Actualizar las propiedades de un objeto [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) .</span><span class="sxs-lookup"><span data-stu-id="a8c70-107">Update the properties of a [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a8c70-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a8c70-108">Prerequisites</span></span>
<span data-ttu-id="a8c70-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a8c70-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a8c70-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a8c70-111">Permission type</span></span>|<span data-ttu-id="a8c70-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a8c70-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a8c70-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a8c70-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a8c70-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a8c70-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a8c70-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a8c70-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a8c70-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a8c70-116">Not supported.</span></span>|
|<span data-ttu-id="a8c70-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a8c70-117">Application</span></span>|<span data-ttu-id="a8c70-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a8c70-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a8c70-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a8c70-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/advancedThreatProtectionOnboardingStateSummary/advancedThreatProtectionOnboardingDeviceSettingStates/{advancedThreatProtectionOnboardingDeviceSettingStateId}
```

## <a name="request-headers"></a><span data-ttu-id="a8c70-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a8c70-120">Request headers</span></span>
|<span data-ttu-id="a8c70-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8c70-121">Header</span></span>|<span data-ttu-id="a8c70-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a8c70-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a8c70-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a8c70-123">Authorization</span></span>|<span data-ttu-id="a8c70-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a8c70-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a8c70-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a8c70-125">Accept</span></span>|<span data-ttu-id="a8c70-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a8c70-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a8c70-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a8c70-127">Request body</span></span>
<span data-ttu-id="a8c70-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) .</span><span class="sxs-lookup"><span data-stu-id="a8c70-128">In the request body, supply a JSON representation for the [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) object.</span></span>

<span data-ttu-id="a8c70-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md).</span><span class="sxs-lookup"><span data-stu-id="a8c70-129">The following table shows the properties that are required when you create the [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md).</span></span>

|<span data-ttu-id="a8c70-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a8c70-130">Property</span></span>|<span data-ttu-id="a8c70-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8c70-131">Type</span></span>|<span data-ttu-id="a8c70-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8c70-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a8c70-133">id</span><span class="sxs-lookup"><span data-stu-id="a8c70-133">id</span></span>|<span data-ttu-id="a8c70-134">String</span><span class="sxs-lookup"><span data-stu-id="a8c70-134">String</span></span>|<span data-ttu-id="a8c70-135">Clave de la entidad</span><span class="sxs-lookup"><span data-stu-id="a8c70-135">Key of the entity</span></span>|
|<span data-ttu-id="a8c70-136">platformType</span><span class="sxs-lookup"><span data-stu-id="a8c70-136">platformType</span></span>|[<span data-ttu-id="a8c70-137">deviceType</span><span class="sxs-lookup"><span data-stu-id="a8c70-137">deviceType</span></span>](../resources/intune-shared-devicetype.md)|<span data-ttu-id="a8c70-138">Tipo de plataforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a8c70-138">Device platform type.</span></span> <span data-ttu-id="a8c70-139">Los valores posibles son: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise` , `blackberry`, `palm`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="a8c70-139">Possible values are: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise`, `blackberry`, `palm`, `unknown`.</span></span>|
|<span data-ttu-id="a8c70-140">ajustes</span><span class="sxs-lookup"><span data-stu-id="a8c70-140">setting</span></span>|<span data-ttu-id="a8c70-141">String</span><span class="sxs-lookup"><span data-stu-id="a8c70-141">String</span></span>|<span data-ttu-id="a8c70-142">El nombre de la clase de configuración y el nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="a8c70-142">The setting class name and property name.</span></span>|
|<span data-ttu-id="a8c70-143">settingName</span><span class="sxs-lookup"><span data-stu-id="a8c70-143">settingName</span></span>|<span data-ttu-id="a8c70-144">String</span><span class="sxs-lookup"><span data-stu-id="a8c70-144">String</span></span>|<span data-ttu-id="a8c70-145">El nombre de configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="a8c70-145">The Setting Name that is being reported</span></span>|
|<span data-ttu-id="a8c70-146">deviceId</span><span class="sxs-lookup"><span data-stu-id="a8c70-146">deviceId</span></span>|<span data-ttu-id="a8c70-147">String</span><span class="sxs-lookup"><span data-stu-id="a8c70-147">String</span></span>|<span data-ttu-id="a8c70-148">El identificador del dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="a8c70-148">The Device Id that is being reported</span></span>|
|<span data-ttu-id="a8c70-149">deviceName</span><span class="sxs-lookup"><span data-stu-id="a8c70-149">deviceName</span></span>|<span data-ttu-id="a8c70-150">String</span><span class="sxs-lookup"><span data-stu-id="a8c70-150">String</span></span>|<span data-ttu-id="a8c70-151">El nombre del dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="a8c70-151">The Device Name that is being reported</span></span>|
|<span data-ttu-id="a8c70-152">userId</span><span class="sxs-lookup"><span data-stu-id="a8c70-152">userId</span></span>|<span data-ttu-id="a8c70-153">String</span><span class="sxs-lookup"><span data-stu-id="a8c70-153">String</span></span>|<span data-ttu-id="a8c70-154">El identificador del usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="a8c70-154">The user Id that is being reported</span></span>|
|<span data-ttu-id="a8c70-155">userEmail</span><span class="sxs-lookup"><span data-stu-id="a8c70-155">userEmail</span></span>|<span data-ttu-id="a8c70-156">String</span><span class="sxs-lookup"><span data-stu-id="a8c70-156">String</span></span>|<span data-ttu-id="a8c70-157">La dirección de correo electrónico del usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="a8c70-157">The User email address that is being reported</span></span>|
|<span data-ttu-id="a8c70-158">userName</span><span class="sxs-lookup"><span data-stu-id="a8c70-158">userName</span></span>|<span data-ttu-id="a8c70-159">String</span><span class="sxs-lookup"><span data-stu-id="a8c70-159">String</span></span>|<span data-ttu-id="a8c70-160">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="a8c70-160">The User Name that is being reported</span></span>|
|<span data-ttu-id="a8c70-161">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a8c70-161">userPrincipalName</span></span>|<span data-ttu-id="a8c70-162">String</span><span class="sxs-lookup"><span data-stu-id="a8c70-162">String</span></span>|<span data-ttu-id="a8c70-163">El nombre principal de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="a8c70-163">The User PrincipalName that is being reported</span></span>|
|<span data-ttu-id="a8c70-164">deviceModel</span><span class="sxs-lookup"><span data-stu-id="a8c70-164">deviceModel</span></span>|<span data-ttu-id="a8c70-165">String</span><span class="sxs-lookup"><span data-stu-id="a8c70-165">String</span></span>|<span data-ttu-id="a8c70-166">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="a8c70-166">The device model that is being reported</span></span>|
|<span data-ttu-id="a8c70-167">state</span><span class="sxs-lookup"><span data-stu-id="a8c70-167">state</span></span>|[<span data-ttu-id="a8c70-168">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="a8c70-168">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="a8c70-169">El estado de cumplimiento de la configuración.</span><span class="sxs-lookup"><span data-stu-id="a8c70-169">The compliance state of the setting.</span></span> <span data-ttu-id="a8c70-170">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="a8c70-170">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="a8c70-171">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="a8c70-171">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="a8c70-172">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a8c70-172">DateTimeOffset</span></span>|<span data-ttu-id="a8c70-173">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="a8c70-173">The DateTime when device compliance grace period expires</span></span>|



## <a name="response"></a><span data-ttu-id="a8c70-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a8c70-174">Response</span></span>
<span data-ttu-id="a8c70-175">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a8c70-175">If successful, this method returns a `200 OK` response code and an updated [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a8c70-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a8c70-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="a8c70-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a8c70-177">Request</span></span>
<span data-ttu-id="a8c70-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a8c70-178">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/advancedThreatProtectionOnboardingStateSummary/advancedThreatProtectionOnboardingDeviceSettingStates/{advancedThreatProtectionOnboardingDeviceSettingStateId}
Content-type: application/json
Content-length: 482

{
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

### <a name="response"></a><span data-ttu-id="a8c70-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a8c70-179">Response</span></span>
<span data-ttu-id="a8c70-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a8c70-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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






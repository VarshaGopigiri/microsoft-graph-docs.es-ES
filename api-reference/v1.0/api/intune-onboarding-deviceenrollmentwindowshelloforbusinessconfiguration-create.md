---
title: Crear deviceEnrollmentWindowsHelloForBusinessConfiguration
description: Cree un objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.
ms.openlocfilehash: de4eff1e68157a2f1069e031b209171e90a198fd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029794"
---
# <a name="create-deviceenrollmentwindowshelloforbusinessconfiguration"></a><span data-ttu-id="883c6-103">Crear deviceEnrollmentWindowsHelloForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="883c6-103">Create deviceEnrollmentWindowsHelloForBusinessConfiguration</span></span>

> <span data-ttu-id="883c6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="883c6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="883c6-105">Cree un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="883c6-105">Create a new [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="883c6-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="883c6-106">Prerequisites</span></span>
<span data-ttu-id="883c6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="883c6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="883c6-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="883c6-109">Permission type</span></span>|<span data-ttu-id="883c6-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="883c6-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="883c6-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="883c6-111">Delegated (work or school account)</span></span>|<span data-ttu-id="883c6-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="883c6-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="883c6-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="883c6-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="883c6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="883c6-114">Not supported.</span></span>|
|<span data-ttu-id="883c6-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="883c6-115">Application</span></span>|<span data-ttu-id="883c6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="883c6-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="883c6-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="883c6-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceEnrollmentConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="883c6-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="883c6-118">Request headers</span></span>
|<span data-ttu-id="883c6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="883c6-119">Header</span></span>|<span data-ttu-id="883c6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="883c6-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="883c6-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="883c6-121">Authorization</span></span>|<span data-ttu-id="883c6-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="883c6-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="883c6-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="883c6-123">Accept</span></span>|<span data-ttu-id="883c6-124">application/json</span><span class="sxs-lookup"><span data-stu-id="883c6-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="883c6-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="883c6-125">Request body</span></span>
<span data-ttu-id="883c6-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="883c6-126">In the request body, supply a JSON representation for the deviceEnrollmentWindowsHelloForBusinessConfiguration object.</span></span>

<span data-ttu-id="883c6-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="883c6-127">The following table shows the properties that are required when you create the deviceEnrollmentWindowsHelloForBusinessConfiguration.</span></span>

|<span data-ttu-id="883c6-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="883c6-128">Property</span></span>|<span data-ttu-id="883c6-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="883c6-129">Type</span></span>|<span data-ttu-id="883c6-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="883c6-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="883c6-131">id</span><span class="sxs-lookup"><span data-stu-id="883c6-131">id</span></span>|<span data-ttu-id="883c6-132">String</span><span class="sxs-lookup"><span data-stu-id="883c6-132">String</span></span>|<span data-ttu-id="883c6-133">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="883c6-133">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="883c6-134">displayName</span><span class="sxs-lookup"><span data-stu-id="883c6-134">displayName</span></span>|<span data-ttu-id="883c6-135">String</span><span class="sxs-lookup"><span data-stu-id="883c6-135">String</span></span>|<span data-ttu-id="883c6-136">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="883c6-136">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="883c6-137">descripción</span><span class="sxs-lookup"><span data-stu-id="883c6-137">description</span></span>|<span data-ttu-id="883c6-138">String</span><span class="sxs-lookup"><span data-stu-id="883c6-138">String</span></span>|<span data-ttu-id="883c6-139">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="883c6-139">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="883c6-140">prioridad</span><span class="sxs-lookup"><span data-stu-id="883c6-140">priority</span></span>|<span data-ttu-id="883c6-141">Int32</span><span class="sxs-lookup"><span data-stu-id="883c6-141">Int32</span></span>|<span data-ttu-id="883c6-142">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="883c6-142">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="883c6-143">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="883c6-143">createdDateTime</span></span>|<span data-ttu-id="883c6-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="883c6-144">DateTimeOffset</span></span>|<span data-ttu-id="883c6-145">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="883c6-145">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="883c6-146">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="883c6-146">lastModifiedDateTime</span></span>|<span data-ttu-id="883c6-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="883c6-147">DateTimeOffset</span></span>|<span data-ttu-id="883c6-148">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="883c6-148">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="883c6-149">version</span><span class="sxs-lookup"><span data-stu-id="883c6-149">version</span></span>|<span data-ttu-id="883c6-150">Int32</span><span class="sxs-lookup"><span data-stu-id="883c6-150">Int32</span></span>|<span data-ttu-id="883c6-151">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="883c6-151">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="883c6-152">pinMinimumLength</span><span class="sxs-lookup"><span data-stu-id="883c6-152">pinMinimumLength</span></span>|<span data-ttu-id="883c6-153">Int32</span><span class="sxs-lookup"><span data-stu-id="883c6-153">Int32</span></span>|<span data-ttu-id="883c6-154">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="883c6-154">Not yet documented</span></span>|
|<span data-ttu-id="883c6-155">pinMaximumLength</span><span class="sxs-lookup"><span data-stu-id="883c6-155">pinMaximumLength</span></span>|<span data-ttu-id="883c6-156">Int32</span><span class="sxs-lookup"><span data-stu-id="883c6-156">Int32</span></span>|<span data-ttu-id="883c6-157">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="883c6-157">Not yet documented</span></span>|
|<span data-ttu-id="883c6-158">pinUppercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="883c6-158">pinUppercaseCharactersUsage</span></span>|[<span data-ttu-id="883c6-159">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="883c6-159">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="883c6-160">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="883c6-160">Not yet documented.</span></span> <span data-ttu-id="883c6-161">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="883c6-161">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="883c6-162">pinLowercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="883c6-162">pinLowercaseCharactersUsage</span></span>|[<span data-ttu-id="883c6-163">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="883c6-163">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="883c6-164">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="883c6-164">Not yet documented.</span></span> <span data-ttu-id="883c6-165">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="883c6-165">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="883c6-166">pinSpecialCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="883c6-166">pinSpecialCharactersUsage</span></span>|[<span data-ttu-id="883c6-167">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="883c6-167">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="883c6-168">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="883c6-168">Not yet documented.</span></span> <span data-ttu-id="883c6-169">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="883c6-169">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="883c6-170">estado</span><span class="sxs-lookup"><span data-stu-id="883c6-170">state</span></span>|[<span data-ttu-id="883c6-171">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="883c6-171">enablement</span></span>](../resources/intune-onboarding-enablement.md)|<span data-ttu-id="883c6-172">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="883c6-172">Not yet documented.</span></span> <span data-ttu-id="883c6-173">Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="883c6-173">Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|
|<span data-ttu-id="883c6-174">securityDeviceRequired</span><span class="sxs-lookup"><span data-stu-id="883c6-174">securityDeviceRequired</span></span>|<span data-ttu-id="883c6-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="883c6-175">Boolean</span></span>|<span data-ttu-id="883c6-176">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="883c6-176">Not yet documented</span></span>|
|<span data-ttu-id="883c6-177">unlockWithBiometricsEnabled</span><span class="sxs-lookup"><span data-stu-id="883c6-177">unlockWithBiometricsEnabled</span></span>|<span data-ttu-id="883c6-178">Booleano</span><span class="sxs-lookup"><span data-stu-id="883c6-178">Boolean</span></span>|<span data-ttu-id="883c6-179">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="883c6-179">Not yet documented</span></span>|
|<span data-ttu-id="883c6-180">remotePassportEnabled</span><span class="sxs-lookup"><span data-stu-id="883c6-180">remotePassportEnabled</span></span>|<span data-ttu-id="883c6-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="883c6-181">Boolean</span></span>|<span data-ttu-id="883c6-182">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="883c6-182">Not yet documented</span></span>|
|<span data-ttu-id="883c6-183">pinPreviousBlockCount</span><span class="sxs-lookup"><span data-stu-id="883c6-183">pinPreviousBlockCount</span></span>|<span data-ttu-id="883c6-184">Int32</span><span class="sxs-lookup"><span data-stu-id="883c6-184">Int32</span></span>|<span data-ttu-id="883c6-185">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="883c6-185">Not yet documented</span></span>|
|<span data-ttu-id="883c6-186">pinExpirationInDays</span><span class="sxs-lookup"><span data-stu-id="883c6-186">pinExpirationInDays</span></span>|<span data-ttu-id="883c6-187">Int32</span><span class="sxs-lookup"><span data-stu-id="883c6-187">Int32</span></span>|<span data-ttu-id="883c6-188">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="883c6-188">Not yet documented</span></span>|
|<span data-ttu-id="883c6-189">enhancedBiometricsState</span><span class="sxs-lookup"><span data-stu-id="883c6-189">enhancedBiometricsState</span></span>|[<span data-ttu-id="883c6-190">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="883c6-190">enablement</span></span>](../resources/intune-onboarding-enablement.md)|<span data-ttu-id="883c6-191">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="883c6-191">Not yet documented.</span></span> <span data-ttu-id="883c6-192">Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="883c6-192">Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|



## <a name="response"></a><span data-ttu-id="883c6-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="883c6-193">Response</span></span>
<span data-ttu-id="883c6-194">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="883c6-194">If successful, this method returns a `201 Created` response code and a [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="883c6-195">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="883c6-195">Example</span></span>
### <a name="request"></a><span data-ttu-id="883c6-196">Solicitud</span><span class="sxs-lookup"><span data-stu-id="883c6-196">Request</span></span>
<span data-ttu-id="883c6-197">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="883c6-197">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations
Content-type: application/json
Content-length: 629

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentWindowsHelloForBusinessConfiguration",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "version": 7,
  "pinMinimumLength": 0,
  "pinMaximumLength": 0,
  "pinUppercaseCharactersUsage": "required",
  "pinLowercaseCharactersUsage": "required",
  "pinSpecialCharactersUsage": "required",
  "state": "enabled",
  "securityDeviceRequired": true,
  "unlockWithBiometricsEnabled": true,
  "remotePassportEnabled": true,
  "pinPreviousBlockCount": 5,
  "pinExpirationInDays": 3,
  "enhancedBiometricsState": "enabled"
}
```

### <a name="response"></a><span data-ttu-id="883c6-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="883c6-198">Response</span></span>
<span data-ttu-id="883c6-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="883c6-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 801

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentWindowsHelloForBusinessConfiguration",
  "id": "3068e0cd-e0cd-3068-cde0-6830cde06830",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "pinMinimumLength": 0,
  "pinMaximumLength": 0,
  "pinUppercaseCharactersUsage": "required",
  "pinLowercaseCharactersUsage": "required",
  "pinSpecialCharactersUsage": "required",
  "state": "enabled",
  "securityDeviceRequired": true,
  "unlockWithBiometricsEnabled": true,
  "remotePassportEnabled": true,
  "pinPreviousBlockCount": 5,
  "pinExpirationInDays": 3,
  "enhancedBiometricsState": "enabled"
}
```




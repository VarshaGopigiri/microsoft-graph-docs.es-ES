---
title: Actualizar deviceEnrollmentWindowsHelloForBusinessConfiguration
description: Actualice las propiedades de un objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.
ms.openlocfilehash: 44624aaf7f073d67f8623bdaee8266c80596a90d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084392"
---
# <a name="update-deviceenrollmentwindowshelloforbusinessconfiguration"></a><span data-ttu-id="cac0b-103">Actualizar deviceEnrollmentWindowsHelloForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="cac0b-103">Update deviceEnrollmentWindowsHelloForBusinessConfiguration</span></span>

> <span data-ttu-id="cac0b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cac0b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cac0b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cac0b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cac0b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cac0b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cac0b-107">Actualice las propiedades de un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="cac0b-107">Update the properties of a [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cac0b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cac0b-108">Prerequisites</span></span>
<span data-ttu-id="cac0b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cac0b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cac0b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cac0b-111">Permission type</span></span>|<span data-ttu-id="cac0b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cac0b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cac0b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cac0b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="cac0b-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cac0b-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="cac0b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cac0b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cac0b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cac0b-116">Not supported.</span></span>|
|<span data-ttu-id="cac0b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cac0b-117">Application</span></span>|<span data-ttu-id="cac0b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cac0b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cac0b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cac0b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="cac0b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cac0b-120">Request headers</span></span>
|<span data-ttu-id="cac0b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cac0b-121">Header</span></span>|<span data-ttu-id="cac0b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cac0b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cac0b-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="cac0b-123">Authorization</span></span>|<span data-ttu-id="cac0b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cac0b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cac0b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cac0b-125">Accept</span></span>|<span data-ttu-id="cac0b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="cac0b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cac0b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cac0b-127">Request body</span></span>
<span data-ttu-id="cac0b-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="cac0b-128">In the request body, supply a JSON representation for the [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) object.</span></span>

<span data-ttu-id="cac0b-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="cac0b-129">The following table shows the properties that are required when you create the [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md).</span></span>

|<span data-ttu-id="cac0b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cac0b-130">Property</span></span>|<span data-ttu-id="cac0b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="cac0b-131">Type</span></span>|<span data-ttu-id="cac0b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="cac0b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cac0b-133">id</span><span class="sxs-lookup"><span data-stu-id="cac0b-133">id</span></span>|<span data-ttu-id="cac0b-134">String</span><span class="sxs-lookup"><span data-stu-id="cac0b-134">String</span></span>|<span data-ttu-id="cac0b-135">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cac0b-135">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cac0b-136">displayName</span><span class="sxs-lookup"><span data-stu-id="cac0b-136">displayName</span></span>|<span data-ttu-id="cac0b-137">String</span><span class="sxs-lookup"><span data-stu-id="cac0b-137">String</span></span>|<span data-ttu-id="cac0b-138">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cac0b-138">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cac0b-139">descripción</span><span class="sxs-lookup"><span data-stu-id="cac0b-139">description</span></span>|<span data-ttu-id="cac0b-140">String</span><span class="sxs-lookup"><span data-stu-id="cac0b-140">String</span></span>|<span data-ttu-id="cac0b-141">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cac0b-141">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cac0b-142">prioridad</span><span class="sxs-lookup"><span data-stu-id="cac0b-142">priority</span></span>|<span data-ttu-id="cac0b-143">Int32</span><span class="sxs-lookup"><span data-stu-id="cac0b-143">Int32</span></span>|<span data-ttu-id="cac0b-144">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cac0b-144">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cac0b-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="cac0b-145">createdDateTime</span></span>|<span data-ttu-id="cac0b-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cac0b-146">DateTimeOffset</span></span>|<span data-ttu-id="cac0b-147">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cac0b-147">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cac0b-148">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="cac0b-148">lastModifiedDateTime</span></span>|<span data-ttu-id="cac0b-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cac0b-149">DateTimeOffset</span></span>|<span data-ttu-id="cac0b-150">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cac0b-150">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cac0b-151">version</span><span class="sxs-lookup"><span data-stu-id="cac0b-151">version</span></span>|<span data-ttu-id="cac0b-152">Int32</span><span class="sxs-lookup"><span data-stu-id="cac0b-152">Int32</span></span>|<span data-ttu-id="cac0b-153">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cac0b-153">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cac0b-154">pinMinimumLength</span><span class="sxs-lookup"><span data-stu-id="cac0b-154">pinMinimumLength</span></span>|<span data-ttu-id="cac0b-155">Int32</span><span class="sxs-lookup"><span data-stu-id="cac0b-155">Int32</span></span>|<span data-ttu-id="cac0b-156">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cac0b-156">Not yet documented</span></span>|
|<span data-ttu-id="cac0b-157">pinMaximumLength</span><span class="sxs-lookup"><span data-stu-id="cac0b-157">pinMaximumLength</span></span>|<span data-ttu-id="cac0b-158">Int32</span><span class="sxs-lookup"><span data-stu-id="cac0b-158">Int32</span></span>|<span data-ttu-id="cac0b-159">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cac0b-159">Not yet documented</span></span>|
|<span data-ttu-id="cac0b-160">pinUppercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="cac0b-160">pinUppercaseCharactersUsage</span></span>|[<span data-ttu-id="cac0b-161">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="cac0b-161">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="cac0b-162">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="cac0b-162">Not yet documented.</span></span> <span data-ttu-id="cac0b-163">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="cac0b-163">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="cac0b-164">pinLowercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="cac0b-164">pinLowercaseCharactersUsage</span></span>|[<span data-ttu-id="cac0b-165">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="cac0b-165">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="cac0b-166">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="cac0b-166">Not yet documented.</span></span> <span data-ttu-id="cac0b-167">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="cac0b-167">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="cac0b-168">pinSpecialCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="cac0b-168">pinSpecialCharactersUsage</span></span>|[<span data-ttu-id="cac0b-169">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="cac0b-169">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="cac0b-170">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="cac0b-170">Not yet documented.</span></span> <span data-ttu-id="cac0b-171">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="cac0b-171">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="cac0b-172">estado</span><span class="sxs-lookup"><span data-stu-id="cac0b-172">state</span></span>|[<span data-ttu-id="cac0b-173">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="cac0b-173">enablement</span></span>](../resources/intune-shared-enablement.md)|<span data-ttu-id="cac0b-174">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="cac0b-174">Not yet documented.</span></span> <span data-ttu-id="cac0b-175">Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="cac0b-175">Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|
|<span data-ttu-id="cac0b-176">securityDeviceRequired</span><span class="sxs-lookup"><span data-stu-id="cac0b-176">securityDeviceRequired</span></span>|<span data-ttu-id="cac0b-177">Booleano</span><span class="sxs-lookup"><span data-stu-id="cac0b-177">Boolean</span></span>|<span data-ttu-id="cac0b-178">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cac0b-178">Not yet documented</span></span>|
|<span data-ttu-id="cac0b-179">unlockWithBiometricsEnabled</span><span class="sxs-lookup"><span data-stu-id="cac0b-179">unlockWithBiometricsEnabled</span></span>|<span data-ttu-id="cac0b-180">Booleano</span><span class="sxs-lookup"><span data-stu-id="cac0b-180">Boolean</span></span>|<span data-ttu-id="cac0b-181">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cac0b-181">Not yet documented</span></span>|
|<span data-ttu-id="cac0b-182">remotePassportEnabled</span><span class="sxs-lookup"><span data-stu-id="cac0b-182">remotePassportEnabled</span></span>|<span data-ttu-id="cac0b-183">Booleano</span><span class="sxs-lookup"><span data-stu-id="cac0b-183">Boolean</span></span>|<span data-ttu-id="cac0b-184">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cac0b-184">Not yet documented</span></span>|
|<span data-ttu-id="cac0b-185">pinPreviousBlockCount</span><span class="sxs-lookup"><span data-stu-id="cac0b-185">pinPreviousBlockCount</span></span>|<span data-ttu-id="cac0b-186">Int32</span><span class="sxs-lookup"><span data-stu-id="cac0b-186">Int32</span></span>|<span data-ttu-id="cac0b-187">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cac0b-187">Not yet documented</span></span>|
|<span data-ttu-id="cac0b-188">pinExpirationInDays</span><span class="sxs-lookup"><span data-stu-id="cac0b-188">pinExpirationInDays</span></span>|<span data-ttu-id="cac0b-189">Int32</span><span class="sxs-lookup"><span data-stu-id="cac0b-189">Int32</span></span>|<span data-ttu-id="cac0b-190">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cac0b-190">Not yet documented</span></span>|
|<span data-ttu-id="cac0b-191">enhancedBiometricsState</span><span class="sxs-lookup"><span data-stu-id="cac0b-191">enhancedBiometricsState</span></span>|[<span data-ttu-id="cac0b-192">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="cac0b-192">enablement</span></span>](../resources/intune-shared-enablement.md)|<span data-ttu-id="cac0b-193">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="cac0b-193">Not yet documented.</span></span> <span data-ttu-id="cac0b-194">Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="cac0b-194">Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|



## <a name="response"></a><span data-ttu-id="cac0b-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cac0b-195">Response</span></span>
<span data-ttu-id="cac0b-196">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cac0b-196">If successful, this method returns a `200 OK` response code and an updated [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cac0b-197">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cac0b-197">Example</span></span>
### <a name="request"></a><span data-ttu-id="cac0b-198">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cac0b-198">Request</span></span>
<span data-ttu-id="cac0b-199">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cac0b-199">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
Content-type: application/json
Content-length: 602

{
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
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

### <a name="response"></a><span data-ttu-id="cac0b-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cac0b-200">Response</span></span>
<span data-ttu-id="cac0b-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cac0b-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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





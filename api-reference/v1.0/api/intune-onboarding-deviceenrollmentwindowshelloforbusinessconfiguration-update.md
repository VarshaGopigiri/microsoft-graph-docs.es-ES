---
title: Actualizar deviceEnrollmentWindowsHelloForBusinessConfiguration
description: Actualice las propiedades de un objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 982d28cdea829afd9e569ff97628fcf19b3c4956
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825819"
---
# <a name="update-deviceenrollmentwindowshelloforbusinessconfiguration"></a><span data-ttu-id="e8533-103">Actualizar deviceEnrollmentWindowsHelloForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8533-103">Update deviceEnrollmentWindowsHelloForBusinessConfiguration</span></span>

> <span data-ttu-id="e8533-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e8533-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e8533-105">Actualice las propiedades de un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e8533-105">Update the properties of a [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e8533-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e8533-106">Prerequisites</span></span>
<span data-ttu-id="e8533-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e8533-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e8533-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e8533-109">Permission type</span></span>|<span data-ttu-id="e8533-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e8533-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e8533-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e8533-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e8533-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e8533-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="e8533-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e8533-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e8533-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e8533-114">Not supported.</span></span>|
|<span data-ttu-id="e8533-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e8533-115">Application</span></span>|<span data-ttu-id="e8533-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e8533-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e8533-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e8533-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="e8533-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e8533-118">Request headers</span></span>
|<span data-ttu-id="e8533-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8533-119">Header</span></span>|<span data-ttu-id="e8533-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e8533-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e8533-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="e8533-121">Authorization</span></span>|<span data-ttu-id="e8533-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e8533-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e8533-123">Accept</span><span class="sxs-lookup"><span data-stu-id="e8533-123">Accept</span></span>|<span data-ttu-id="e8533-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e8533-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e8533-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e8533-125">Request body</span></span>
<span data-ttu-id="e8533-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e8533-126">In the request body, supply a JSON representation for the [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) object.</span></span>

<span data-ttu-id="e8533-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e8533-127">The following table shows the properties that are required when you create the [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md).</span></span>

|<span data-ttu-id="e8533-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e8533-128">Property</span></span>|<span data-ttu-id="e8533-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="e8533-129">Type</span></span>|<span data-ttu-id="e8533-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8533-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e8533-131">id</span><span class="sxs-lookup"><span data-stu-id="e8533-131">id</span></span>|<span data-ttu-id="e8533-132">String</span><span class="sxs-lookup"><span data-stu-id="e8533-132">String</span></span>|<span data-ttu-id="e8533-133">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e8533-133">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="e8533-134">displayName</span><span class="sxs-lookup"><span data-stu-id="e8533-134">displayName</span></span>|<span data-ttu-id="e8533-135">String</span><span class="sxs-lookup"><span data-stu-id="e8533-135">String</span></span>|<span data-ttu-id="e8533-136">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e8533-136">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="e8533-137">descripción</span><span class="sxs-lookup"><span data-stu-id="e8533-137">description</span></span>|<span data-ttu-id="e8533-138">String</span><span class="sxs-lookup"><span data-stu-id="e8533-138">String</span></span>|<span data-ttu-id="e8533-139">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e8533-139">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="e8533-140">prioridad</span><span class="sxs-lookup"><span data-stu-id="e8533-140">priority</span></span>|<span data-ttu-id="e8533-141">Int32</span><span class="sxs-lookup"><span data-stu-id="e8533-141">Int32</span></span>|<span data-ttu-id="e8533-142">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e8533-142">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="e8533-143">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e8533-143">createdDateTime</span></span>|<span data-ttu-id="e8533-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e8533-144">DateTimeOffset</span></span>|<span data-ttu-id="e8533-145">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e8533-145">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="e8533-146">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e8533-146">lastModifiedDateTime</span></span>|<span data-ttu-id="e8533-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e8533-147">DateTimeOffset</span></span>|<span data-ttu-id="e8533-148">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e8533-148">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="e8533-149">version</span><span class="sxs-lookup"><span data-stu-id="e8533-149">version</span></span>|<span data-ttu-id="e8533-150">Int32</span><span class="sxs-lookup"><span data-stu-id="e8533-150">Int32</span></span>|<span data-ttu-id="e8533-151">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e8533-151">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="e8533-152">pinMinimumLength</span><span class="sxs-lookup"><span data-stu-id="e8533-152">pinMinimumLength</span></span>|<span data-ttu-id="e8533-153">Int32</span><span class="sxs-lookup"><span data-stu-id="e8533-153">Int32</span></span>|<span data-ttu-id="e8533-154">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e8533-154">Not yet documented</span></span>|
|<span data-ttu-id="e8533-155">pinMaximumLength</span><span class="sxs-lookup"><span data-stu-id="e8533-155">pinMaximumLength</span></span>|<span data-ttu-id="e8533-156">Int32</span><span class="sxs-lookup"><span data-stu-id="e8533-156">Int32</span></span>|<span data-ttu-id="e8533-157">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e8533-157">Not yet documented</span></span>|
|<span data-ttu-id="e8533-158">pinUppercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="e8533-158">pinUppercaseCharactersUsage</span></span>|[<span data-ttu-id="e8533-159">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="e8533-159">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="e8533-160">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="e8533-160">Not yet documented.</span></span> <span data-ttu-id="e8533-161">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="e8533-161">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="e8533-162">pinLowercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="e8533-162">pinLowercaseCharactersUsage</span></span>|[<span data-ttu-id="e8533-163">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="e8533-163">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="e8533-164">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="e8533-164">Not yet documented.</span></span> <span data-ttu-id="e8533-165">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="e8533-165">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="e8533-166">pinSpecialCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="e8533-166">pinSpecialCharactersUsage</span></span>|[<span data-ttu-id="e8533-167">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="e8533-167">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="e8533-168">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="e8533-168">Not yet documented.</span></span> <span data-ttu-id="e8533-169">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="e8533-169">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="e8533-170">state</span><span class="sxs-lookup"><span data-stu-id="e8533-170">state</span></span>|[<span data-ttu-id="e8533-171">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="e8533-171">enablement</span></span>](../resources/intune-onboarding-enablement.md)|<span data-ttu-id="e8533-172">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="e8533-172">Not yet documented.</span></span> <span data-ttu-id="e8533-173">Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="e8533-173">Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|
|<span data-ttu-id="e8533-174">securityDeviceRequired</span><span class="sxs-lookup"><span data-stu-id="e8533-174">securityDeviceRequired</span></span>|<span data-ttu-id="e8533-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="e8533-175">Boolean</span></span>|<span data-ttu-id="e8533-176">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e8533-176">Not yet documented</span></span>|
|<span data-ttu-id="e8533-177">unlockWithBiometricsEnabled</span><span class="sxs-lookup"><span data-stu-id="e8533-177">unlockWithBiometricsEnabled</span></span>|<span data-ttu-id="e8533-178">Booleano</span><span class="sxs-lookup"><span data-stu-id="e8533-178">Boolean</span></span>|<span data-ttu-id="e8533-179">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e8533-179">Not yet documented</span></span>|
|<span data-ttu-id="e8533-180">remotePassportEnabled</span><span class="sxs-lookup"><span data-stu-id="e8533-180">remotePassportEnabled</span></span>|<span data-ttu-id="e8533-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="e8533-181">Boolean</span></span>|<span data-ttu-id="e8533-182">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e8533-182">Not yet documented</span></span>|
|<span data-ttu-id="e8533-183">pinPreviousBlockCount</span><span class="sxs-lookup"><span data-stu-id="e8533-183">pinPreviousBlockCount</span></span>|<span data-ttu-id="e8533-184">Int32</span><span class="sxs-lookup"><span data-stu-id="e8533-184">Int32</span></span>|<span data-ttu-id="e8533-185">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e8533-185">Not yet documented</span></span>|
|<span data-ttu-id="e8533-186">pinExpirationInDays</span><span class="sxs-lookup"><span data-stu-id="e8533-186">pinExpirationInDays</span></span>|<span data-ttu-id="e8533-187">Int32</span><span class="sxs-lookup"><span data-stu-id="e8533-187">Int32</span></span>|<span data-ttu-id="e8533-188">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e8533-188">Not yet documented</span></span>|
|<span data-ttu-id="e8533-189">enhancedBiometricsState</span><span class="sxs-lookup"><span data-stu-id="e8533-189">enhancedBiometricsState</span></span>|[<span data-ttu-id="e8533-190">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="e8533-190">enablement</span></span>](../resources/intune-onboarding-enablement.md)|<span data-ttu-id="e8533-191">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="e8533-191">Not yet documented.</span></span> <span data-ttu-id="e8533-192">Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="e8533-192">Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|



## <a name="response"></a><span data-ttu-id="e8533-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8533-193">Response</span></span>
<span data-ttu-id="e8533-194">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e8533-194">If successful, this method returns a `200 OK` response code and an updated [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e8533-195">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8533-195">Example</span></span>
### <a name="request"></a><span data-ttu-id="e8533-196">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e8533-196">Request</span></span>
<span data-ttu-id="e8533-197">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e8533-197">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
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

### <a name="response"></a><span data-ttu-id="e8533-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8533-198">Response</span></span>
<span data-ttu-id="e8533-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e8533-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




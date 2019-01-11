---
title: Crear deviceEnrollmentWindowsHelloForBusinessConfiguration
description: Cree un objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: dd395803e5940855c3eb21e5ca1ca8b8b1ec3bdc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27829494"
---
# <a name="create-deviceenrollmentwindowshelloforbusinessconfiguration"></a><span data-ttu-id="9ddc1-103">Crear deviceEnrollmentWindowsHelloForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ddc1-103">Create deviceEnrollmentWindowsHelloForBusinessConfiguration</span></span>

> <span data-ttu-id="9ddc1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9ddc1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9ddc1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9ddc1-107">Cree un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="9ddc1-107">Create a new [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9ddc1-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9ddc1-108">Prerequisites</span></span>
<span data-ttu-id="9ddc1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9ddc1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9ddc1-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9ddc1-111">Permission type</span></span>|<span data-ttu-id="9ddc1-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9ddc1-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9ddc1-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9ddc1-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9ddc1-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9ddc1-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="9ddc1-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9ddc1-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9ddc1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-116">Not supported.</span></span>|
|<span data-ttu-id="9ddc1-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9ddc1-117">Application</span></span>|<span data-ttu-id="9ddc1-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9ddc1-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9ddc1-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceEnrollmentConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="9ddc1-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9ddc1-120">Request headers</span></span>
|<span data-ttu-id="9ddc1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ddc1-121">Header</span></span>|<span data-ttu-id="9ddc1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9ddc1-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9ddc1-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="9ddc1-123">Authorization</span></span>|<span data-ttu-id="9ddc1-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9ddc1-125">Accept</span><span class="sxs-lookup"><span data-stu-id="9ddc1-125">Accept</span></span>|<span data-ttu-id="9ddc1-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9ddc1-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9ddc1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9ddc1-127">Request body</span></span>
<span data-ttu-id="9ddc1-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-128">In the request body, supply a JSON representation for the deviceEnrollmentWindowsHelloForBusinessConfiguration object.</span></span>

<span data-ttu-id="9ddc1-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-129">The following table shows the properties that are required when you create the deviceEnrollmentWindowsHelloForBusinessConfiguration.</span></span>

|<span data-ttu-id="9ddc1-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9ddc1-130">Property</span></span>|<span data-ttu-id="9ddc1-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9ddc1-131">Type</span></span>|<span data-ttu-id="9ddc1-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ddc1-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9ddc1-133">id</span><span class="sxs-lookup"><span data-stu-id="9ddc1-133">id</span></span>|<span data-ttu-id="9ddc1-134">String</span><span class="sxs-lookup"><span data-stu-id="9ddc1-134">String</span></span>|<span data-ttu-id="9ddc1-135">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9ddc1-135">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="9ddc1-136">displayName</span><span class="sxs-lookup"><span data-stu-id="9ddc1-136">displayName</span></span>|<span data-ttu-id="9ddc1-137">String</span><span class="sxs-lookup"><span data-stu-id="9ddc1-137">String</span></span>|<span data-ttu-id="9ddc1-138">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9ddc1-138">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="9ddc1-139">descripción</span><span class="sxs-lookup"><span data-stu-id="9ddc1-139">description</span></span>|<span data-ttu-id="9ddc1-140">String</span><span class="sxs-lookup"><span data-stu-id="9ddc1-140">String</span></span>|<span data-ttu-id="9ddc1-141">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9ddc1-141">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="9ddc1-142">prioridad</span><span class="sxs-lookup"><span data-stu-id="9ddc1-142">priority</span></span>|<span data-ttu-id="9ddc1-143">Int32</span><span class="sxs-lookup"><span data-stu-id="9ddc1-143">Int32</span></span>|<span data-ttu-id="9ddc1-144">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9ddc1-144">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="9ddc1-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="9ddc1-145">createdDateTime</span></span>|<span data-ttu-id="9ddc1-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9ddc1-146">DateTimeOffset</span></span>|<span data-ttu-id="9ddc1-147">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9ddc1-147">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="9ddc1-148">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="9ddc1-148">lastModifiedDateTime</span></span>|<span data-ttu-id="9ddc1-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9ddc1-149">DateTimeOffset</span></span>|<span data-ttu-id="9ddc1-150">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9ddc1-150">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="9ddc1-151">version</span><span class="sxs-lookup"><span data-stu-id="9ddc1-151">version</span></span>|<span data-ttu-id="9ddc1-152">Int32</span><span class="sxs-lookup"><span data-stu-id="9ddc1-152">Int32</span></span>|<span data-ttu-id="9ddc1-153">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9ddc1-153">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="9ddc1-154">pinMinimumLength</span><span class="sxs-lookup"><span data-stu-id="9ddc1-154">pinMinimumLength</span></span>|<span data-ttu-id="9ddc1-155">Int32</span><span class="sxs-lookup"><span data-stu-id="9ddc1-155">Int32</span></span>|<span data-ttu-id="9ddc1-156">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9ddc1-156">Not yet documented</span></span>|
|<span data-ttu-id="9ddc1-157">pinMaximumLength</span><span class="sxs-lookup"><span data-stu-id="9ddc1-157">pinMaximumLength</span></span>|<span data-ttu-id="9ddc1-158">Int32</span><span class="sxs-lookup"><span data-stu-id="9ddc1-158">Int32</span></span>|<span data-ttu-id="9ddc1-159">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9ddc1-159">Not yet documented</span></span>|
|<span data-ttu-id="9ddc1-160">pinUppercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="9ddc1-160">pinUppercaseCharactersUsage</span></span>|[<span data-ttu-id="9ddc1-161">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="9ddc1-161">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="9ddc1-162">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-162">Not yet documented.</span></span> <span data-ttu-id="9ddc1-163">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-163">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="9ddc1-164">pinLowercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="9ddc1-164">pinLowercaseCharactersUsage</span></span>|[<span data-ttu-id="9ddc1-165">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="9ddc1-165">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="9ddc1-166">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-166">Not yet documented.</span></span> <span data-ttu-id="9ddc1-167">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-167">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="9ddc1-168">pinSpecialCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="9ddc1-168">pinSpecialCharactersUsage</span></span>|[<span data-ttu-id="9ddc1-169">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="9ddc1-169">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="9ddc1-170">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-170">Not yet documented.</span></span> <span data-ttu-id="9ddc1-171">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-171">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="9ddc1-172">state</span><span class="sxs-lookup"><span data-stu-id="9ddc1-172">state</span></span>|[<span data-ttu-id="9ddc1-173">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="9ddc1-173">enablement</span></span>](../resources/intune-shared-enablement.md)|<span data-ttu-id="9ddc1-174">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-174">Not yet documented.</span></span> <span data-ttu-id="9ddc1-175">Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-175">Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|
|<span data-ttu-id="9ddc1-176">securityDeviceRequired</span><span class="sxs-lookup"><span data-stu-id="9ddc1-176">securityDeviceRequired</span></span>|<span data-ttu-id="9ddc1-177">Booleano</span><span class="sxs-lookup"><span data-stu-id="9ddc1-177">Boolean</span></span>|<span data-ttu-id="9ddc1-178">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9ddc1-178">Not yet documented</span></span>|
|<span data-ttu-id="9ddc1-179">unlockWithBiometricsEnabled</span><span class="sxs-lookup"><span data-stu-id="9ddc1-179">unlockWithBiometricsEnabled</span></span>|<span data-ttu-id="9ddc1-180">Booleano</span><span class="sxs-lookup"><span data-stu-id="9ddc1-180">Boolean</span></span>|<span data-ttu-id="9ddc1-181">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9ddc1-181">Not yet documented</span></span>|
|<span data-ttu-id="9ddc1-182">remotePassportEnabled</span><span class="sxs-lookup"><span data-stu-id="9ddc1-182">remotePassportEnabled</span></span>|<span data-ttu-id="9ddc1-183">Booleano</span><span class="sxs-lookup"><span data-stu-id="9ddc1-183">Boolean</span></span>|<span data-ttu-id="9ddc1-184">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9ddc1-184">Not yet documented</span></span>|
|<span data-ttu-id="9ddc1-185">pinPreviousBlockCount</span><span class="sxs-lookup"><span data-stu-id="9ddc1-185">pinPreviousBlockCount</span></span>|<span data-ttu-id="9ddc1-186">Int32</span><span class="sxs-lookup"><span data-stu-id="9ddc1-186">Int32</span></span>|<span data-ttu-id="9ddc1-187">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9ddc1-187">Not yet documented</span></span>|
|<span data-ttu-id="9ddc1-188">pinExpirationInDays</span><span class="sxs-lookup"><span data-stu-id="9ddc1-188">pinExpirationInDays</span></span>|<span data-ttu-id="9ddc1-189">Int32</span><span class="sxs-lookup"><span data-stu-id="9ddc1-189">Int32</span></span>|<span data-ttu-id="9ddc1-190">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9ddc1-190">Not yet documented</span></span>|
|<span data-ttu-id="9ddc1-191">enhancedBiometricsState</span><span class="sxs-lookup"><span data-stu-id="9ddc1-191">enhancedBiometricsState</span></span>|[<span data-ttu-id="9ddc1-192">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="9ddc1-192">enablement</span></span>](../resources/intune-shared-enablement.md)|<span data-ttu-id="9ddc1-193">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-193">Not yet documented.</span></span> <span data-ttu-id="9ddc1-194">Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-194">Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|



## <a name="response"></a><span data-ttu-id="9ddc1-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ddc1-195">Response</span></span>
<span data-ttu-id="9ddc1-196">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-196">If successful, this method returns a `201 Created` response code and a [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9ddc1-197">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ddc1-197">Example</span></span>
### <a name="request"></a><span data-ttu-id="9ddc1-198">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9ddc1-198">Request</span></span>
<span data-ttu-id="9ddc1-199">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-199">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceEnrollmentConfigurations
Content-type: application/json
Content-length: 693

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentWindowsHelloForBusinessConfiguration",
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

### <a name="response"></a><span data-ttu-id="9ddc1-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ddc1-200">Response</span></span>
<span data-ttu-id="9ddc1-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9ddc1-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






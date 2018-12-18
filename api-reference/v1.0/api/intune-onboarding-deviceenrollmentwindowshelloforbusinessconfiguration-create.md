---
title: Crear deviceEnrollmentWindowsHelloForBusinessConfiguration
description: Cree un objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.
author: tfitzmac
ms.openlocfilehash: 1c17cfccfd6875b11a392e5d8c00785e1f10673b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27348604"
---
# <a name="create-deviceenrollmentwindowshelloforbusinessconfiguration"></a><span data-ttu-id="4c849-103">Crear deviceEnrollmentWindowsHelloForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c849-103">Create deviceEnrollmentWindowsHelloForBusinessConfiguration</span></span>

> <span data-ttu-id="4c849-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4c849-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4c849-105">Cree un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="4c849-105">Create a new [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4c849-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4c849-106">Prerequisites</span></span>
<span data-ttu-id="4c849-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4c849-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4c849-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4c849-109">Permission type</span></span>|<span data-ttu-id="4c849-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4c849-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4c849-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4c849-111">Delegated (work or school account)</span></span>|<span data-ttu-id="4c849-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4c849-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="4c849-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4c849-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4c849-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4c849-114">Not supported.</span></span>|
|<span data-ttu-id="4c849-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4c849-115">Application</span></span>|<span data-ttu-id="4c849-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4c849-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4c849-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4c849-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceEnrollmentConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="4c849-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4c849-118">Request headers</span></span>
|<span data-ttu-id="4c849-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c849-119">Header</span></span>|<span data-ttu-id="4c849-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4c849-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4c849-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="4c849-121">Authorization</span></span>|<span data-ttu-id="4c849-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4c849-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4c849-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4c849-123">Accept</span></span>|<span data-ttu-id="4c849-124">application/json</span><span class="sxs-lookup"><span data-stu-id="4c849-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4c849-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4c849-125">Request body</span></span>
<span data-ttu-id="4c849-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4c849-126">In the request body, supply a JSON representation for the deviceEnrollmentWindowsHelloForBusinessConfiguration object.</span></span>

<span data-ttu-id="4c849-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4c849-127">The following table shows the properties that are required when you create the deviceEnrollmentWindowsHelloForBusinessConfiguration.</span></span>

|<span data-ttu-id="4c849-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4c849-128">Property</span></span>|<span data-ttu-id="4c849-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c849-129">Type</span></span>|<span data-ttu-id="4c849-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c849-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4c849-131">id</span><span class="sxs-lookup"><span data-stu-id="4c849-131">id</span></span>|<span data-ttu-id="4c849-132">String</span><span class="sxs-lookup"><span data-stu-id="4c849-132">String</span></span>|<span data-ttu-id="4c849-133">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4c849-133">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="4c849-134">displayName</span><span class="sxs-lookup"><span data-stu-id="4c849-134">displayName</span></span>|<span data-ttu-id="4c849-135">String</span><span class="sxs-lookup"><span data-stu-id="4c849-135">String</span></span>|<span data-ttu-id="4c849-136">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4c849-136">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="4c849-137">descripción</span><span class="sxs-lookup"><span data-stu-id="4c849-137">description</span></span>|<span data-ttu-id="4c849-138">String</span><span class="sxs-lookup"><span data-stu-id="4c849-138">String</span></span>|<span data-ttu-id="4c849-139">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4c849-139">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="4c849-140">prioridad</span><span class="sxs-lookup"><span data-stu-id="4c849-140">priority</span></span>|<span data-ttu-id="4c849-141">Int32</span><span class="sxs-lookup"><span data-stu-id="4c849-141">Int32</span></span>|<span data-ttu-id="4c849-142">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4c849-142">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="4c849-143">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="4c849-143">createdDateTime</span></span>|<span data-ttu-id="4c849-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4c849-144">DateTimeOffset</span></span>|<span data-ttu-id="4c849-145">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4c849-145">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="4c849-146">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="4c849-146">lastModifiedDateTime</span></span>|<span data-ttu-id="4c849-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4c849-147">DateTimeOffset</span></span>|<span data-ttu-id="4c849-148">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4c849-148">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="4c849-149">version</span><span class="sxs-lookup"><span data-stu-id="4c849-149">version</span></span>|<span data-ttu-id="4c849-150">Int32</span><span class="sxs-lookup"><span data-stu-id="4c849-150">Int32</span></span>|<span data-ttu-id="4c849-151">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4c849-151">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="4c849-152">pinMinimumLength</span><span class="sxs-lookup"><span data-stu-id="4c849-152">pinMinimumLength</span></span>|<span data-ttu-id="4c849-153">Int32</span><span class="sxs-lookup"><span data-stu-id="4c849-153">Int32</span></span>|<span data-ttu-id="4c849-154">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4c849-154">Not yet documented</span></span>|
|<span data-ttu-id="4c849-155">pinMaximumLength</span><span class="sxs-lookup"><span data-stu-id="4c849-155">pinMaximumLength</span></span>|<span data-ttu-id="4c849-156">Int32</span><span class="sxs-lookup"><span data-stu-id="4c849-156">Int32</span></span>|<span data-ttu-id="4c849-157">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4c849-157">Not yet documented</span></span>|
|<span data-ttu-id="4c849-158">pinUppercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="4c849-158">pinUppercaseCharactersUsage</span></span>|[<span data-ttu-id="4c849-159">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="4c849-159">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="4c849-160">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="4c849-160">Not yet documented.</span></span> <span data-ttu-id="4c849-161">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="4c849-161">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="4c849-162">pinLowercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="4c849-162">pinLowercaseCharactersUsage</span></span>|[<span data-ttu-id="4c849-163">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="4c849-163">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="4c849-164">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="4c849-164">Not yet documented.</span></span> <span data-ttu-id="4c849-165">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="4c849-165">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="4c849-166">pinSpecialCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="4c849-166">pinSpecialCharactersUsage</span></span>|[<span data-ttu-id="4c849-167">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="4c849-167">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="4c849-168">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="4c849-168">Not yet documented.</span></span> <span data-ttu-id="4c849-169">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="4c849-169">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="4c849-170">state</span><span class="sxs-lookup"><span data-stu-id="4c849-170">state</span></span>|[<span data-ttu-id="4c849-171">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="4c849-171">enablement</span></span>](../resources/intune-onboarding-enablement.md)|<span data-ttu-id="4c849-172">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="4c849-172">Not yet documented.</span></span> <span data-ttu-id="4c849-173">Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="4c849-173">Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|
|<span data-ttu-id="4c849-174">securityDeviceRequired</span><span class="sxs-lookup"><span data-stu-id="4c849-174">securityDeviceRequired</span></span>|<span data-ttu-id="4c849-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="4c849-175">Boolean</span></span>|<span data-ttu-id="4c849-176">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4c849-176">Not yet documented</span></span>|
|<span data-ttu-id="4c849-177">unlockWithBiometricsEnabled</span><span class="sxs-lookup"><span data-stu-id="4c849-177">unlockWithBiometricsEnabled</span></span>|<span data-ttu-id="4c849-178">Booleano</span><span class="sxs-lookup"><span data-stu-id="4c849-178">Boolean</span></span>|<span data-ttu-id="4c849-179">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4c849-179">Not yet documented</span></span>|
|<span data-ttu-id="4c849-180">remotePassportEnabled</span><span class="sxs-lookup"><span data-stu-id="4c849-180">remotePassportEnabled</span></span>|<span data-ttu-id="4c849-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="4c849-181">Boolean</span></span>|<span data-ttu-id="4c849-182">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4c849-182">Not yet documented</span></span>|
|<span data-ttu-id="4c849-183">pinPreviousBlockCount</span><span class="sxs-lookup"><span data-stu-id="4c849-183">pinPreviousBlockCount</span></span>|<span data-ttu-id="4c849-184">Int32</span><span class="sxs-lookup"><span data-stu-id="4c849-184">Int32</span></span>|<span data-ttu-id="4c849-185">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4c849-185">Not yet documented</span></span>|
|<span data-ttu-id="4c849-186">pinExpirationInDays</span><span class="sxs-lookup"><span data-stu-id="4c849-186">pinExpirationInDays</span></span>|<span data-ttu-id="4c849-187">Int32</span><span class="sxs-lookup"><span data-stu-id="4c849-187">Int32</span></span>|<span data-ttu-id="4c849-188">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4c849-188">Not yet documented</span></span>|
|<span data-ttu-id="4c849-189">enhancedBiometricsState</span><span class="sxs-lookup"><span data-stu-id="4c849-189">enhancedBiometricsState</span></span>|[<span data-ttu-id="4c849-190">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="4c849-190">enablement</span></span>](../resources/intune-onboarding-enablement.md)|<span data-ttu-id="4c849-191">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="4c849-191">Not yet documented.</span></span> <span data-ttu-id="4c849-192">Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="4c849-192">Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|



## <a name="response"></a><span data-ttu-id="4c849-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4c849-193">Response</span></span>
<span data-ttu-id="4c849-194">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4c849-194">If successful, this method returns a `201 Created` response code and a [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4c849-195">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4c849-195">Example</span></span>
### <a name="request"></a><span data-ttu-id="4c849-196">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4c849-196">Request</span></span>
<span data-ttu-id="4c849-197">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4c849-197">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="4c849-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4c849-198">Response</span></span>
<span data-ttu-id="4c849-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4c849-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




---
title: Crear deviceEnrollmentWindowsHelloForBusinessConfiguration
description: Cree un objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 7f86fd9fc1a8028ab983dce46998046b1515c761
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27983082"
---
# <a name="create-deviceenrollmentwindowshelloforbusinessconfiguration"></a><span data-ttu-id="dba0b-103">Crear deviceEnrollmentWindowsHelloForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="dba0b-103">Create deviceEnrollmentWindowsHelloForBusinessConfiguration</span></span>

> <span data-ttu-id="dba0b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dba0b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dba0b-105">Cree un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="dba0b-105">Create a new [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="dba0b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="dba0b-106">Prerequisites</span></span>
<span data-ttu-id="dba0b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dba0b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dba0b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dba0b-109">Permission type</span></span>|<span data-ttu-id="dba0b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dba0b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="dba0b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dba0b-111">Delegated (work or school account)</span></span>|<span data-ttu-id="dba0b-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dba0b-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="dba0b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dba0b-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="dba0b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dba0b-114">Not supported.</span></span>|
|<span data-ttu-id="dba0b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dba0b-115">Application</span></span>|<span data-ttu-id="dba0b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dba0b-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="dba0b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dba0b-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceEnrollmentConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="dba0b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dba0b-118">Request headers</span></span>
|<span data-ttu-id="dba0b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dba0b-119">Header</span></span>|<span data-ttu-id="dba0b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="dba0b-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="dba0b-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="dba0b-121">Authorization</span></span>|<span data-ttu-id="dba0b-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="dba0b-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="dba0b-123">Accept</span><span class="sxs-lookup"><span data-stu-id="dba0b-123">Accept</span></span>|<span data-ttu-id="dba0b-124">application/json</span><span class="sxs-lookup"><span data-stu-id="dba0b-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="dba0b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dba0b-125">Request body</span></span>
<span data-ttu-id="dba0b-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dba0b-126">In the request body, supply a JSON representation for the deviceEnrollmentWindowsHelloForBusinessConfiguration object.</span></span>

<span data-ttu-id="dba0b-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dba0b-127">The following table shows the properties that are required when you create the deviceEnrollmentWindowsHelloForBusinessConfiguration.</span></span>

|<span data-ttu-id="dba0b-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dba0b-128">Property</span></span>|<span data-ttu-id="dba0b-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="dba0b-129">Type</span></span>|<span data-ttu-id="dba0b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="dba0b-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="dba0b-131">id</span><span class="sxs-lookup"><span data-stu-id="dba0b-131">id</span></span>|<span data-ttu-id="dba0b-132">String</span><span class="sxs-lookup"><span data-stu-id="dba0b-132">String</span></span>|<span data-ttu-id="dba0b-133">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="dba0b-133">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="dba0b-134">displayName</span><span class="sxs-lookup"><span data-stu-id="dba0b-134">displayName</span></span>|<span data-ttu-id="dba0b-135">String</span><span class="sxs-lookup"><span data-stu-id="dba0b-135">String</span></span>|<span data-ttu-id="dba0b-136">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="dba0b-136">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="dba0b-137">descripción</span><span class="sxs-lookup"><span data-stu-id="dba0b-137">description</span></span>|<span data-ttu-id="dba0b-138">String</span><span class="sxs-lookup"><span data-stu-id="dba0b-138">String</span></span>|<span data-ttu-id="dba0b-139">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="dba0b-139">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="dba0b-140">prioridad</span><span class="sxs-lookup"><span data-stu-id="dba0b-140">priority</span></span>|<span data-ttu-id="dba0b-141">Int32</span><span class="sxs-lookup"><span data-stu-id="dba0b-141">Int32</span></span>|<span data-ttu-id="dba0b-142">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="dba0b-142">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="dba0b-143">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="dba0b-143">createdDateTime</span></span>|<span data-ttu-id="dba0b-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dba0b-144">DateTimeOffset</span></span>|<span data-ttu-id="dba0b-145">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="dba0b-145">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="dba0b-146">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="dba0b-146">lastModifiedDateTime</span></span>|<span data-ttu-id="dba0b-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dba0b-147">DateTimeOffset</span></span>|<span data-ttu-id="dba0b-148">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="dba0b-148">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="dba0b-149">version</span><span class="sxs-lookup"><span data-stu-id="dba0b-149">version</span></span>|<span data-ttu-id="dba0b-150">Int32</span><span class="sxs-lookup"><span data-stu-id="dba0b-150">Int32</span></span>|<span data-ttu-id="dba0b-151">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="dba0b-151">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="dba0b-152">pinMinimumLength</span><span class="sxs-lookup"><span data-stu-id="dba0b-152">pinMinimumLength</span></span>|<span data-ttu-id="dba0b-153">Int32</span><span class="sxs-lookup"><span data-stu-id="dba0b-153">Int32</span></span>|<span data-ttu-id="dba0b-154">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="dba0b-154">Not yet documented</span></span>|
|<span data-ttu-id="dba0b-155">pinMaximumLength</span><span class="sxs-lookup"><span data-stu-id="dba0b-155">pinMaximumLength</span></span>|<span data-ttu-id="dba0b-156">Int32</span><span class="sxs-lookup"><span data-stu-id="dba0b-156">Int32</span></span>|<span data-ttu-id="dba0b-157">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="dba0b-157">Not yet documented</span></span>|
|<span data-ttu-id="dba0b-158">pinUppercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="dba0b-158">pinUppercaseCharactersUsage</span></span>|[<span data-ttu-id="dba0b-159">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="dba0b-159">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="dba0b-160">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="dba0b-160">Not yet documented.</span></span> <span data-ttu-id="dba0b-161">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="dba0b-161">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="dba0b-162">pinLowercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="dba0b-162">pinLowercaseCharactersUsage</span></span>|[<span data-ttu-id="dba0b-163">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="dba0b-163">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="dba0b-164">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="dba0b-164">Not yet documented.</span></span> <span data-ttu-id="dba0b-165">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="dba0b-165">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="dba0b-166">pinSpecialCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="dba0b-166">pinSpecialCharactersUsage</span></span>|[<span data-ttu-id="dba0b-167">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="dba0b-167">windowsHelloForBusinessPinUsage</span></span>](../resources/intune-onboarding-windowshelloforbusinesspinusage.md)|<span data-ttu-id="dba0b-168">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="dba0b-168">Not yet documented.</span></span> <span data-ttu-id="dba0b-169">Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="dba0b-169">Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="dba0b-170">estado</span><span class="sxs-lookup"><span data-stu-id="dba0b-170">state</span></span>|[<span data-ttu-id="dba0b-171">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="dba0b-171">enablement</span></span>](../resources/intune-onboarding-enablement.md)|<span data-ttu-id="dba0b-172">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="dba0b-172">Not yet documented.</span></span> <span data-ttu-id="dba0b-173">Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="dba0b-173">Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|
|<span data-ttu-id="dba0b-174">securityDeviceRequired</span><span class="sxs-lookup"><span data-stu-id="dba0b-174">securityDeviceRequired</span></span>|<span data-ttu-id="dba0b-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="dba0b-175">Boolean</span></span>|<span data-ttu-id="dba0b-176">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="dba0b-176">Not yet documented</span></span>|
|<span data-ttu-id="dba0b-177">unlockWithBiometricsEnabled</span><span class="sxs-lookup"><span data-stu-id="dba0b-177">unlockWithBiometricsEnabled</span></span>|<span data-ttu-id="dba0b-178">Booleano</span><span class="sxs-lookup"><span data-stu-id="dba0b-178">Boolean</span></span>|<span data-ttu-id="dba0b-179">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="dba0b-179">Not yet documented</span></span>|
|<span data-ttu-id="dba0b-180">remotePassportEnabled</span><span class="sxs-lookup"><span data-stu-id="dba0b-180">remotePassportEnabled</span></span>|<span data-ttu-id="dba0b-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="dba0b-181">Boolean</span></span>|<span data-ttu-id="dba0b-182">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="dba0b-182">Not yet documented</span></span>|
|<span data-ttu-id="dba0b-183">pinPreviousBlockCount</span><span class="sxs-lookup"><span data-stu-id="dba0b-183">pinPreviousBlockCount</span></span>|<span data-ttu-id="dba0b-184">Int32</span><span class="sxs-lookup"><span data-stu-id="dba0b-184">Int32</span></span>|<span data-ttu-id="dba0b-185">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="dba0b-185">Not yet documented</span></span>|
|<span data-ttu-id="dba0b-186">pinExpirationInDays</span><span class="sxs-lookup"><span data-stu-id="dba0b-186">pinExpirationInDays</span></span>|<span data-ttu-id="dba0b-187">Int32</span><span class="sxs-lookup"><span data-stu-id="dba0b-187">Int32</span></span>|<span data-ttu-id="dba0b-188">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="dba0b-188">Not yet documented</span></span>|
|<span data-ttu-id="dba0b-189">enhancedBiometricsState</span><span class="sxs-lookup"><span data-stu-id="dba0b-189">enhancedBiometricsState</span></span>|[<span data-ttu-id="dba0b-190">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="dba0b-190">enablement</span></span>](../resources/intune-onboarding-enablement.md)|<span data-ttu-id="dba0b-191">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="dba0b-191">Not yet documented.</span></span> <span data-ttu-id="dba0b-192">Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="dba0b-192">Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|



## <a name="response"></a><span data-ttu-id="dba0b-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dba0b-193">Response</span></span>
<span data-ttu-id="dba0b-194">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dba0b-194">If successful, this method returns a `201 Created` response code and a [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dba0b-195">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dba0b-195">Example</span></span>
### <a name="request"></a><span data-ttu-id="dba0b-196">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dba0b-196">Request</span></span>
<span data-ttu-id="dba0b-197">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dba0b-197">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="dba0b-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dba0b-198">Response</span></span>
<span data-ttu-id="dba0b-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dba0b-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




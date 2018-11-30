---
title: Actualizar deviceEnrollmentPlatformRestrictionsConfiguration
description: Actualice las propiedades de un objeto deviceEnrollmentPlatformRestrictionsConfiguration.
ms.openlocfilehash: 840f67c25eb0e0cc34e951be12a1dd5cddca17c1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089684"
---
# <a name="update-deviceenrollmentplatformrestrictionsconfiguration"></a><span data-ttu-id="31cef-103">Actualizar deviceEnrollmentPlatformRestrictionsConfiguration</span><span class="sxs-lookup"><span data-stu-id="31cef-103">Update deviceEnrollmentPlatformRestrictionsConfiguration</span></span>

> <span data-ttu-id="31cef-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="31cef-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="31cef-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="31cef-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="31cef-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="31cef-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="31cef-107">Actualice las propiedades de un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="31cef-107">Update the properties of a [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="31cef-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="31cef-108">Prerequisites</span></span>
<span data-ttu-id="31cef-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="31cef-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="31cef-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="31cef-111">Permission type</span></span>|<span data-ttu-id="31cef-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="31cef-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="31cef-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="31cef-113">Delegated (work or school account)</span></span>|<span data-ttu-id="31cef-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="31cef-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="31cef-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="31cef-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="31cef-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="31cef-116">Not supported.</span></span>|
|<span data-ttu-id="31cef-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="31cef-117">Application</span></span>|<span data-ttu-id="31cef-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="31cef-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="31cef-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="31cef-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="31cef-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="31cef-120">Request headers</span></span>
|<span data-ttu-id="31cef-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31cef-121">Header</span></span>|<span data-ttu-id="31cef-122">Valor</span><span class="sxs-lookup"><span data-stu-id="31cef-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="31cef-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="31cef-123">Authorization</span></span>|<span data-ttu-id="31cef-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="31cef-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="31cef-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="31cef-125">Accept</span></span>|<span data-ttu-id="31cef-126">application/json</span><span class="sxs-lookup"><span data-stu-id="31cef-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="31cef-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="31cef-127">Request body</span></span>
<span data-ttu-id="31cef-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="31cef-128">In the request body, supply a JSON representation for the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>

<span data-ttu-id="31cef-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="31cef-129">The following table shows the properties that are required when you create the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span></span>

|<span data-ttu-id="31cef-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="31cef-130">Property</span></span>|<span data-ttu-id="31cef-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="31cef-131">Type</span></span>|<span data-ttu-id="31cef-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="31cef-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="31cef-133">id</span><span class="sxs-lookup"><span data-stu-id="31cef-133">id</span></span>|<span data-ttu-id="31cef-134">String</span><span class="sxs-lookup"><span data-stu-id="31cef-134">String</span></span>|<span data-ttu-id="31cef-135">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="31cef-135">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="31cef-136">displayName</span><span class="sxs-lookup"><span data-stu-id="31cef-136">displayName</span></span>|<span data-ttu-id="31cef-137">String</span><span class="sxs-lookup"><span data-stu-id="31cef-137">String</span></span>|<span data-ttu-id="31cef-138">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="31cef-138">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="31cef-139">descripción</span><span class="sxs-lookup"><span data-stu-id="31cef-139">description</span></span>|<span data-ttu-id="31cef-140">String</span><span class="sxs-lookup"><span data-stu-id="31cef-140">String</span></span>|<span data-ttu-id="31cef-141">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="31cef-141">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="31cef-142">prioridad</span><span class="sxs-lookup"><span data-stu-id="31cef-142">priority</span></span>|<span data-ttu-id="31cef-143">Int32</span><span class="sxs-lookup"><span data-stu-id="31cef-143">Int32</span></span>|<span data-ttu-id="31cef-144">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="31cef-144">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="31cef-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="31cef-145">createdDateTime</span></span>|<span data-ttu-id="31cef-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="31cef-146">DateTimeOffset</span></span>|<span data-ttu-id="31cef-147">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="31cef-147">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="31cef-148">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="31cef-148">lastModifiedDateTime</span></span>|<span data-ttu-id="31cef-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="31cef-149">DateTimeOffset</span></span>|<span data-ttu-id="31cef-150">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="31cef-150">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="31cef-151">version</span><span class="sxs-lookup"><span data-stu-id="31cef-151">version</span></span>|<span data-ttu-id="31cef-152">Int32</span><span class="sxs-lookup"><span data-stu-id="31cef-152">Int32</span></span>|<span data-ttu-id="31cef-153">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="31cef-153">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="31cef-154">iosRestriction</span><span class="sxs-lookup"><span data-stu-id="31cef-154">iosRestriction</span></span>|[<span data-ttu-id="31cef-155">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="31cef-155">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="31cef-156">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="31cef-156">Not yet documented</span></span>|
|<span data-ttu-id="31cef-157">windowsRestriction</span><span class="sxs-lookup"><span data-stu-id="31cef-157">windowsRestriction</span></span>|[<span data-ttu-id="31cef-158">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="31cef-158">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="31cef-159">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="31cef-159">Not yet documented</span></span>|
|<span data-ttu-id="31cef-160">windowsMobileRestriction</span><span class="sxs-lookup"><span data-stu-id="31cef-160">windowsMobileRestriction</span></span>|[<span data-ttu-id="31cef-161">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="31cef-161">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="31cef-162">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="31cef-162">Not yet documented</span></span>|
|<span data-ttu-id="31cef-163">androidRestriction</span><span class="sxs-lookup"><span data-stu-id="31cef-163">androidRestriction</span></span>|[<span data-ttu-id="31cef-164">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="31cef-164">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="31cef-165">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="31cef-165">Not yet documented</span></span>|
|<span data-ttu-id="31cef-166">androidForWorkRestriction</span><span class="sxs-lookup"><span data-stu-id="31cef-166">androidForWorkRestriction</span></span>|[<span data-ttu-id="31cef-167">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="31cef-167">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="31cef-168">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="31cef-168">Not yet documented</span></span>|
|<span data-ttu-id="31cef-169">macRestriction</span><span class="sxs-lookup"><span data-stu-id="31cef-169">macRestriction</span></span>|[<span data-ttu-id="31cef-170">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="31cef-170">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="31cef-171">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="31cef-171">Not yet documented</span></span>|
|<span data-ttu-id="31cef-172">macOSRestriction</span><span class="sxs-lookup"><span data-stu-id="31cef-172">macOSRestriction</span></span>|[<span data-ttu-id="31cef-173">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="31cef-173">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="31cef-174">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="31cef-174">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="31cef-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31cef-175">Response</span></span>
<span data-ttu-id="31cef-176">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="31cef-176">If successful, this method returns a `200 OK` response code and an updated [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="31cef-177">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="31cef-177">Example</span></span>
### <a name="request"></a><span data-ttu-id="31cef-178">Solicitud</span><span class="sxs-lookup"><span data-stu-id="31cef-178">Request</span></span>
<span data-ttu-id="31cef-179">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="31cef-179">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
Content-type: application/json
Content-length: 2207

{
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "iosRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "windowsRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "windowsMobileRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "androidRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "androidForWorkRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "macRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "macOSRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  }
}
```

### <a name="response"></a><span data-ttu-id="31cef-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31cef-180">Response</span></span>
<span data-ttu-id="31cef-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="31cef-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2403

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentPlatformRestrictionsConfiguration",
  "id": "3acb2d75-2d75-3acb-752d-cb3a752dcb3a",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "iosRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "windowsRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "windowsMobileRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "androidRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "androidForWorkRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "macRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "macOSRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  }
}
```






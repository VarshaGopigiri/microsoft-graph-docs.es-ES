---
title: Actualizar deviceEnrollmentPlatformRestrictionsConfiguration
description: Actualice las propiedades de un objeto deviceEnrollmentPlatformRestrictionsConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ee8822d6d3983b63cc90b599e0800a034c35fabd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27965926"
---
# <a name="update-deviceenrollmentplatformrestrictionsconfiguration"></a><span data-ttu-id="ebb0e-103">Actualizar deviceEnrollmentPlatformRestrictionsConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebb0e-103">Update deviceEnrollmentPlatformRestrictionsConfiguration</span></span>

> <span data-ttu-id="ebb0e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ebb0e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ebb0e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ebb0e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ebb0e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ebb0e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ebb0e-107">Actualice las propiedades de un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ebb0e-107">Update the properties of a [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ebb0e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ebb0e-108">Prerequisites</span></span>
<span data-ttu-id="ebb0e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ebb0e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ebb0e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ebb0e-111">Permission type</span></span>|<span data-ttu-id="ebb0e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ebb0e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ebb0e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ebb0e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ebb0e-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ebb0e-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="ebb0e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ebb0e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ebb0e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ebb0e-116">Not supported.</span></span>|
|<span data-ttu-id="ebb0e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ebb0e-117">Application</span></span>|<span data-ttu-id="ebb0e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ebb0e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ebb0e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ebb0e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="ebb0e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ebb0e-120">Request headers</span></span>
|<span data-ttu-id="ebb0e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ebb0e-121">Header</span></span>|<span data-ttu-id="ebb0e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ebb0e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ebb0e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="ebb0e-123">Authorization</span></span>|<span data-ttu-id="ebb0e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ebb0e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ebb0e-125">Accept</span><span class="sxs-lookup"><span data-stu-id="ebb0e-125">Accept</span></span>|<span data-ttu-id="ebb0e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ebb0e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ebb0e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ebb0e-127">Request body</span></span>
<span data-ttu-id="ebb0e-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ebb0e-128">In the request body, supply a JSON representation for the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>

<span data-ttu-id="ebb0e-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ebb0e-129">The following table shows the properties that are required when you create the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span></span>

|<span data-ttu-id="ebb0e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ebb0e-130">Property</span></span>|<span data-ttu-id="ebb0e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ebb0e-131">Type</span></span>|<span data-ttu-id="ebb0e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebb0e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ebb0e-133">id</span><span class="sxs-lookup"><span data-stu-id="ebb0e-133">id</span></span>|<span data-ttu-id="ebb0e-134">String</span><span class="sxs-lookup"><span data-stu-id="ebb0e-134">String</span></span>|<span data-ttu-id="ebb0e-135">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ebb0e-135">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="ebb0e-136">displayName</span><span class="sxs-lookup"><span data-stu-id="ebb0e-136">displayName</span></span>|<span data-ttu-id="ebb0e-137">String</span><span class="sxs-lookup"><span data-stu-id="ebb0e-137">String</span></span>|<span data-ttu-id="ebb0e-138">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ebb0e-138">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="ebb0e-139">descripción</span><span class="sxs-lookup"><span data-stu-id="ebb0e-139">description</span></span>|<span data-ttu-id="ebb0e-140">String</span><span class="sxs-lookup"><span data-stu-id="ebb0e-140">String</span></span>|<span data-ttu-id="ebb0e-141">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ebb0e-141">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="ebb0e-142">prioridad</span><span class="sxs-lookup"><span data-stu-id="ebb0e-142">priority</span></span>|<span data-ttu-id="ebb0e-143">Int32</span><span class="sxs-lookup"><span data-stu-id="ebb0e-143">Int32</span></span>|<span data-ttu-id="ebb0e-144">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ebb0e-144">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="ebb0e-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ebb0e-145">createdDateTime</span></span>|<span data-ttu-id="ebb0e-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ebb0e-146">DateTimeOffset</span></span>|<span data-ttu-id="ebb0e-147">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ebb0e-147">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="ebb0e-148">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ebb0e-148">lastModifiedDateTime</span></span>|<span data-ttu-id="ebb0e-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ebb0e-149">DateTimeOffset</span></span>|<span data-ttu-id="ebb0e-150">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ebb0e-150">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="ebb0e-151">version</span><span class="sxs-lookup"><span data-stu-id="ebb0e-151">version</span></span>|<span data-ttu-id="ebb0e-152">Int32</span><span class="sxs-lookup"><span data-stu-id="ebb0e-152">Int32</span></span>|<span data-ttu-id="ebb0e-153">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ebb0e-153">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="ebb0e-154">iosRestriction</span><span class="sxs-lookup"><span data-stu-id="ebb0e-154">iosRestriction</span></span>|[<span data-ttu-id="ebb0e-155">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="ebb0e-155">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="ebb0e-156">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ebb0e-156">Not yet documented</span></span>|
|<span data-ttu-id="ebb0e-157">windowsRestriction</span><span class="sxs-lookup"><span data-stu-id="ebb0e-157">windowsRestriction</span></span>|[<span data-ttu-id="ebb0e-158">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="ebb0e-158">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="ebb0e-159">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ebb0e-159">Not yet documented</span></span>|
|<span data-ttu-id="ebb0e-160">windowsMobileRestriction</span><span class="sxs-lookup"><span data-stu-id="ebb0e-160">windowsMobileRestriction</span></span>|[<span data-ttu-id="ebb0e-161">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="ebb0e-161">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="ebb0e-162">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ebb0e-162">Not yet documented</span></span>|
|<span data-ttu-id="ebb0e-163">androidRestriction</span><span class="sxs-lookup"><span data-stu-id="ebb0e-163">androidRestriction</span></span>|[<span data-ttu-id="ebb0e-164">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="ebb0e-164">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="ebb0e-165">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ebb0e-165">Not yet documented</span></span>|
|<span data-ttu-id="ebb0e-166">androidForWorkRestriction</span><span class="sxs-lookup"><span data-stu-id="ebb0e-166">androidForWorkRestriction</span></span>|[<span data-ttu-id="ebb0e-167">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="ebb0e-167">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="ebb0e-168">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ebb0e-168">Not yet documented</span></span>|
|<span data-ttu-id="ebb0e-169">macRestriction</span><span class="sxs-lookup"><span data-stu-id="ebb0e-169">macRestriction</span></span>|[<span data-ttu-id="ebb0e-170">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="ebb0e-170">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="ebb0e-171">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ebb0e-171">Not yet documented</span></span>|
|<span data-ttu-id="ebb0e-172">macOSRestriction</span><span class="sxs-lookup"><span data-stu-id="ebb0e-172">macOSRestriction</span></span>|[<span data-ttu-id="ebb0e-173">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="ebb0e-173">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="ebb0e-174">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ebb0e-174">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="ebb0e-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ebb0e-175">Response</span></span>
<span data-ttu-id="ebb0e-176">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ebb0e-176">If successful, this method returns a `200 OK` response code and an updated [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ebb0e-177">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ebb0e-177">Example</span></span>
### <a name="request"></a><span data-ttu-id="ebb0e-178">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ebb0e-178">Request</span></span>
<span data-ttu-id="ebb0e-179">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ebb0e-179">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="ebb0e-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ebb0e-180">Response</span></span>
<span data-ttu-id="ebb0e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ebb0e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






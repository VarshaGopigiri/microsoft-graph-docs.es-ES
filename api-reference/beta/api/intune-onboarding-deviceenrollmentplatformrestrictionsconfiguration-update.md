---
title: Actualizar deviceEnrollmentPlatformRestrictionsConfiguration
description: Actualice las propiedades de un objeto deviceEnrollmentPlatformRestrictionsConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 606bf82b6556f42c661b4cb46d8ddb978cfbbe7b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27813114"
---
# <a name="update-deviceenrollmentplatformrestrictionsconfiguration"></a><span data-ttu-id="63461-103">Actualizar deviceEnrollmentPlatformRestrictionsConfiguration</span><span class="sxs-lookup"><span data-stu-id="63461-103">Update deviceEnrollmentPlatformRestrictionsConfiguration</span></span>

> <span data-ttu-id="63461-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="63461-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="63461-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="63461-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="63461-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="63461-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="63461-107">Actualice las propiedades de un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="63461-107">Update the properties of a [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="63461-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="63461-108">Prerequisites</span></span>
<span data-ttu-id="63461-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="63461-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="63461-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="63461-111">Permission type</span></span>|<span data-ttu-id="63461-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="63461-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="63461-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="63461-113">Delegated (work or school account)</span></span>|<span data-ttu-id="63461-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="63461-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="63461-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="63461-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="63461-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63461-116">Not supported.</span></span>|
|<span data-ttu-id="63461-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="63461-117">Application</span></span>|<span data-ttu-id="63461-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63461-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="63461-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="63461-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="63461-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="63461-120">Request headers</span></span>
|<span data-ttu-id="63461-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63461-121">Header</span></span>|<span data-ttu-id="63461-122">Valor</span><span class="sxs-lookup"><span data-stu-id="63461-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="63461-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="63461-123">Authorization</span></span>|<span data-ttu-id="63461-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="63461-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="63461-125">Accept</span><span class="sxs-lookup"><span data-stu-id="63461-125">Accept</span></span>|<span data-ttu-id="63461-126">application/json</span><span class="sxs-lookup"><span data-stu-id="63461-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="63461-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="63461-127">Request body</span></span>
<span data-ttu-id="63461-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="63461-128">In the request body, supply a JSON representation for the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>

<span data-ttu-id="63461-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="63461-129">The following table shows the properties that are required when you create the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span></span>

|<span data-ttu-id="63461-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="63461-130">Property</span></span>|<span data-ttu-id="63461-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="63461-131">Type</span></span>|<span data-ttu-id="63461-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="63461-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="63461-133">id</span><span class="sxs-lookup"><span data-stu-id="63461-133">id</span></span>|<span data-ttu-id="63461-134">String</span><span class="sxs-lookup"><span data-stu-id="63461-134">String</span></span>|<span data-ttu-id="63461-135">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63461-135">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="63461-136">displayName</span><span class="sxs-lookup"><span data-stu-id="63461-136">displayName</span></span>|<span data-ttu-id="63461-137">String</span><span class="sxs-lookup"><span data-stu-id="63461-137">String</span></span>|<span data-ttu-id="63461-138">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63461-138">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="63461-139">descripción</span><span class="sxs-lookup"><span data-stu-id="63461-139">description</span></span>|<span data-ttu-id="63461-140">String</span><span class="sxs-lookup"><span data-stu-id="63461-140">String</span></span>|<span data-ttu-id="63461-141">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63461-141">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="63461-142">prioridad</span><span class="sxs-lookup"><span data-stu-id="63461-142">priority</span></span>|<span data-ttu-id="63461-143">Int32</span><span class="sxs-lookup"><span data-stu-id="63461-143">Int32</span></span>|<span data-ttu-id="63461-144">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63461-144">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="63461-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="63461-145">createdDateTime</span></span>|<span data-ttu-id="63461-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="63461-146">DateTimeOffset</span></span>|<span data-ttu-id="63461-147">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63461-147">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="63461-148">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="63461-148">lastModifiedDateTime</span></span>|<span data-ttu-id="63461-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="63461-149">DateTimeOffset</span></span>|<span data-ttu-id="63461-150">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63461-150">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="63461-151">version</span><span class="sxs-lookup"><span data-stu-id="63461-151">version</span></span>|<span data-ttu-id="63461-152">Int32</span><span class="sxs-lookup"><span data-stu-id="63461-152">Int32</span></span>|<span data-ttu-id="63461-153">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63461-153">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="63461-154">iosRestriction</span><span class="sxs-lookup"><span data-stu-id="63461-154">iosRestriction</span></span>|[<span data-ttu-id="63461-155">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="63461-155">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="63461-156">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="63461-156">Not yet documented</span></span>|
|<span data-ttu-id="63461-157">windowsRestriction</span><span class="sxs-lookup"><span data-stu-id="63461-157">windowsRestriction</span></span>|[<span data-ttu-id="63461-158">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="63461-158">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="63461-159">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="63461-159">Not yet documented</span></span>|
|<span data-ttu-id="63461-160">windowsMobileRestriction</span><span class="sxs-lookup"><span data-stu-id="63461-160">windowsMobileRestriction</span></span>|[<span data-ttu-id="63461-161">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="63461-161">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="63461-162">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="63461-162">Not yet documented</span></span>|
|<span data-ttu-id="63461-163">androidRestriction</span><span class="sxs-lookup"><span data-stu-id="63461-163">androidRestriction</span></span>|[<span data-ttu-id="63461-164">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="63461-164">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="63461-165">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="63461-165">Not yet documented</span></span>|
|<span data-ttu-id="63461-166">androidForWorkRestriction</span><span class="sxs-lookup"><span data-stu-id="63461-166">androidForWorkRestriction</span></span>|[<span data-ttu-id="63461-167">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="63461-167">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="63461-168">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="63461-168">Not yet documented</span></span>|
|<span data-ttu-id="63461-169">macRestriction</span><span class="sxs-lookup"><span data-stu-id="63461-169">macRestriction</span></span>|[<span data-ttu-id="63461-170">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="63461-170">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="63461-171">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="63461-171">Not yet documented</span></span>|
|<span data-ttu-id="63461-172">macOSRestriction</span><span class="sxs-lookup"><span data-stu-id="63461-172">macOSRestriction</span></span>|[<span data-ttu-id="63461-173">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="63461-173">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="63461-174">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="63461-174">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="63461-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63461-175">Response</span></span>
<span data-ttu-id="63461-176">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63461-176">If successful, this method returns a `200 OK` response code and an updated [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="63461-177">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63461-177">Example</span></span>
### <a name="request"></a><span data-ttu-id="63461-178">Solicitud</span><span class="sxs-lookup"><span data-stu-id="63461-178">Request</span></span>
<span data-ttu-id="63461-179">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63461-179">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="63461-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63461-180">Response</span></span>
<span data-ttu-id="63461-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="63461-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






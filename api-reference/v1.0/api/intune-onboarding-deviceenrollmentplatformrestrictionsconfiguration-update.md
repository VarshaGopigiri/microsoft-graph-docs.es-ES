---
title: Actualizar deviceEnrollmentPlatformRestrictionsConfiguration
description: Actualice las propiedades de un objeto deviceEnrollmentPlatformRestrictionsConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 3794933b6dabbc9f6a6bfc4957ff0e9a795c3f80
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27849472"
---
# <a name="update-deviceenrollmentplatformrestrictionsconfiguration"></a><span data-ttu-id="1b567-103">Actualizar deviceEnrollmentPlatformRestrictionsConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b567-103">Update deviceEnrollmentPlatformRestrictionsConfiguration</span></span>

> <span data-ttu-id="1b567-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1b567-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1b567-105">Actualice las propiedades de un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="1b567-105">Update the properties of a [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1b567-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1b567-106">Prerequisites</span></span>
<span data-ttu-id="1b567-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1b567-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1b567-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1b567-109">Permission type</span></span>|<span data-ttu-id="1b567-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1b567-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1b567-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1b567-111">Delegated (work or school account)</span></span>|<span data-ttu-id="1b567-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1b567-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="1b567-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1b567-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1b567-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1b567-114">Not supported.</span></span>|
|<span data-ttu-id="1b567-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1b567-115">Application</span></span>|<span data-ttu-id="1b567-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1b567-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1b567-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1b567-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="1b567-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1b567-118">Request headers</span></span>
|<span data-ttu-id="1b567-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b567-119">Header</span></span>|<span data-ttu-id="1b567-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1b567-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1b567-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="1b567-121">Authorization</span></span>|<span data-ttu-id="1b567-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1b567-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1b567-123">Accept</span><span class="sxs-lookup"><span data-stu-id="1b567-123">Accept</span></span>|<span data-ttu-id="1b567-124">application/json</span><span class="sxs-lookup"><span data-stu-id="1b567-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1b567-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1b567-125">Request body</span></span>
<span data-ttu-id="1b567-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="1b567-126">In the request body, supply a JSON representation for the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>

<span data-ttu-id="1b567-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="1b567-127">The following table shows the properties that are required when you create the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span></span>

|<span data-ttu-id="1b567-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1b567-128">Property</span></span>|<span data-ttu-id="1b567-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b567-129">Type</span></span>|<span data-ttu-id="1b567-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b567-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1b567-131">id</span><span class="sxs-lookup"><span data-stu-id="1b567-131">id</span></span>|<span data-ttu-id="1b567-132">String</span><span class="sxs-lookup"><span data-stu-id="1b567-132">String</span></span>|<span data-ttu-id="1b567-133">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1b567-133">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="1b567-134">displayName</span><span class="sxs-lookup"><span data-stu-id="1b567-134">displayName</span></span>|<span data-ttu-id="1b567-135">String</span><span class="sxs-lookup"><span data-stu-id="1b567-135">String</span></span>|<span data-ttu-id="1b567-136">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1b567-136">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="1b567-137">descripción</span><span class="sxs-lookup"><span data-stu-id="1b567-137">description</span></span>|<span data-ttu-id="1b567-138">String</span><span class="sxs-lookup"><span data-stu-id="1b567-138">String</span></span>|<span data-ttu-id="1b567-139">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1b567-139">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="1b567-140">prioridad</span><span class="sxs-lookup"><span data-stu-id="1b567-140">priority</span></span>|<span data-ttu-id="1b567-141">Int32</span><span class="sxs-lookup"><span data-stu-id="1b567-141">Int32</span></span>|<span data-ttu-id="1b567-142">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1b567-142">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="1b567-143">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="1b567-143">createdDateTime</span></span>|<span data-ttu-id="1b567-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1b567-144">DateTimeOffset</span></span>|<span data-ttu-id="1b567-145">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1b567-145">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="1b567-146">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="1b567-146">lastModifiedDateTime</span></span>|<span data-ttu-id="1b567-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1b567-147">DateTimeOffset</span></span>|<span data-ttu-id="1b567-148">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1b567-148">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="1b567-149">version</span><span class="sxs-lookup"><span data-stu-id="1b567-149">version</span></span>|<span data-ttu-id="1b567-150">Int32</span><span class="sxs-lookup"><span data-stu-id="1b567-150">Int32</span></span>|<span data-ttu-id="1b567-151">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1b567-151">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="1b567-152">iosRestriction</span><span class="sxs-lookup"><span data-stu-id="1b567-152">iosRestriction</span></span>|[<span data-ttu-id="1b567-153">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="1b567-153">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="1b567-154">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="1b567-154">Not yet documented</span></span>|
|<span data-ttu-id="1b567-155">windowsRestriction</span><span class="sxs-lookup"><span data-stu-id="1b567-155">windowsRestriction</span></span>|[<span data-ttu-id="1b567-156">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="1b567-156">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="1b567-157">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="1b567-157">Not yet documented</span></span>|
|<span data-ttu-id="1b567-158">windowsMobileRestriction</span><span class="sxs-lookup"><span data-stu-id="1b567-158">windowsMobileRestriction</span></span>|[<span data-ttu-id="1b567-159">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="1b567-159">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="1b567-160">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="1b567-160">Not yet documented</span></span>|
|<span data-ttu-id="1b567-161">androidRestriction</span><span class="sxs-lookup"><span data-stu-id="1b567-161">androidRestriction</span></span>|[<span data-ttu-id="1b567-162">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="1b567-162">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="1b567-163">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="1b567-163">Not yet documented</span></span>|
|<span data-ttu-id="1b567-164">macOSRestriction</span><span class="sxs-lookup"><span data-stu-id="1b567-164">macOSRestriction</span></span>|[<span data-ttu-id="1b567-165">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="1b567-165">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="1b567-166">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="1b567-166">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="1b567-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b567-167">Response</span></span>
<span data-ttu-id="1b567-168">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1b567-168">If successful, this method returns a `200 OK` response code and an updated [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1b567-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1b567-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="1b567-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1b567-170">Request</span></span>
<span data-ttu-id="1b567-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1b567-171">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
Content-type: application/json
Content-length: 1650

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentPlatformRestrictionsConfiguration",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
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
  "macOSRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  }
}
```

### <a name="response"></a><span data-ttu-id="1b567-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b567-172">Response</span></span>
<span data-ttu-id="1b567-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1b567-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1822

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
  "macOSRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  }
}
```




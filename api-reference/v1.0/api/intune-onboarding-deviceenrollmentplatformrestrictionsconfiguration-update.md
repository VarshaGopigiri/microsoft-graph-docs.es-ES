---
title: Actualizar deviceEnrollmentPlatformRestrictionsConfiguration
description: Actualice las propiedades de un objeto deviceEnrollmentPlatformRestrictionsConfiguration.
ms.openlocfilehash: 2f78952d3eeae8f88e66ca1b5441141b7172153f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028779"
---
# <a name="update-deviceenrollmentplatformrestrictionsconfiguration"></a><span data-ttu-id="ad195-103">Actualizar deviceEnrollmentPlatformRestrictionsConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad195-103">Update deviceEnrollmentPlatformRestrictionsConfiguration</span></span>

> <span data-ttu-id="ad195-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ad195-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ad195-105">Actualice las propiedades de un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ad195-105">Update the properties of a [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ad195-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ad195-106">Prerequisites</span></span>
<span data-ttu-id="ad195-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ad195-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ad195-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ad195-109">Permission type</span></span>|<span data-ttu-id="ad195-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ad195-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ad195-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ad195-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ad195-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ad195-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="ad195-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ad195-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ad195-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ad195-114">Not supported.</span></span>|
|<span data-ttu-id="ad195-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ad195-115">Application</span></span>|<span data-ttu-id="ad195-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ad195-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ad195-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ad195-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="ad195-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ad195-118">Request headers</span></span>
|<span data-ttu-id="ad195-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad195-119">Header</span></span>|<span data-ttu-id="ad195-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ad195-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ad195-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="ad195-121">Authorization</span></span>|<span data-ttu-id="ad195-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ad195-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ad195-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ad195-123">Accept</span></span>|<span data-ttu-id="ad195-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ad195-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ad195-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ad195-125">Request body</span></span>
<span data-ttu-id="ad195-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ad195-126">In the request body, supply a JSON representation for the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>

<span data-ttu-id="ad195-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ad195-127">The following table shows the properties that are required when you create the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span></span>

|<span data-ttu-id="ad195-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ad195-128">Property</span></span>|<span data-ttu-id="ad195-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad195-129">Type</span></span>|<span data-ttu-id="ad195-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad195-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ad195-131">id</span><span class="sxs-lookup"><span data-stu-id="ad195-131">id</span></span>|<span data-ttu-id="ad195-132">String</span><span class="sxs-lookup"><span data-stu-id="ad195-132">String</span></span>|<span data-ttu-id="ad195-133">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ad195-133">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="ad195-134">displayName</span><span class="sxs-lookup"><span data-stu-id="ad195-134">displayName</span></span>|<span data-ttu-id="ad195-135">String</span><span class="sxs-lookup"><span data-stu-id="ad195-135">String</span></span>|<span data-ttu-id="ad195-136">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ad195-136">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="ad195-137">descripción</span><span class="sxs-lookup"><span data-stu-id="ad195-137">description</span></span>|<span data-ttu-id="ad195-138">String</span><span class="sxs-lookup"><span data-stu-id="ad195-138">String</span></span>|<span data-ttu-id="ad195-139">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ad195-139">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="ad195-140">prioridad</span><span class="sxs-lookup"><span data-stu-id="ad195-140">priority</span></span>|<span data-ttu-id="ad195-141">Int32</span><span class="sxs-lookup"><span data-stu-id="ad195-141">Int32</span></span>|<span data-ttu-id="ad195-142">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ad195-142">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="ad195-143">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ad195-143">createdDateTime</span></span>|<span data-ttu-id="ad195-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ad195-144">DateTimeOffset</span></span>|<span data-ttu-id="ad195-145">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ad195-145">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="ad195-146">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ad195-146">lastModifiedDateTime</span></span>|<span data-ttu-id="ad195-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ad195-147">DateTimeOffset</span></span>|<span data-ttu-id="ad195-148">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ad195-148">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="ad195-149">version</span><span class="sxs-lookup"><span data-stu-id="ad195-149">version</span></span>|<span data-ttu-id="ad195-150">Int32</span><span class="sxs-lookup"><span data-stu-id="ad195-150">Int32</span></span>|<span data-ttu-id="ad195-151">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ad195-151">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="ad195-152">iosRestriction</span><span class="sxs-lookup"><span data-stu-id="ad195-152">iosRestriction</span></span>|[<span data-ttu-id="ad195-153">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="ad195-153">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="ad195-154">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ad195-154">Not yet documented</span></span>|
|<span data-ttu-id="ad195-155">windowsRestriction</span><span class="sxs-lookup"><span data-stu-id="ad195-155">windowsRestriction</span></span>|[<span data-ttu-id="ad195-156">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="ad195-156">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="ad195-157">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ad195-157">Not yet documented</span></span>|
|<span data-ttu-id="ad195-158">windowsMobileRestriction</span><span class="sxs-lookup"><span data-stu-id="ad195-158">windowsMobileRestriction</span></span>|[<span data-ttu-id="ad195-159">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="ad195-159">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="ad195-160">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ad195-160">Not yet documented</span></span>|
|<span data-ttu-id="ad195-161">androidRestriction</span><span class="sxs-lookup"><span data-stu-id="ad195-161">androidRestriction</span></span>|[<span data-ttu-id="ad195-162">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="ad195-162">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="ad195-163">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ad195-163">Not yet documented</span></span>|
|<span data-ttu-id="ad195-164">macOSRestriction</span><span class="sxs-lookup"><span data-stu-id="ad195-164">macOSRestriction</span></span>|[<span data-ttu-id="ad195-165">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="ad195-165">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="ad195-166">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ad195-166">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="ad195-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad195-167">Response</span></span>
<span data-ttu-id="ad195-168">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad195-168">If successful, this method returns a `200 OK` response code and an updated [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ad195-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ad195-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="ad195-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ad195-170">Request</span></span>
<span data-ttu-id="ad195-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ad195-171">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="ad195-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad195-172">Response</span></span>
<span data-ttu-id="ad195-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ad195-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



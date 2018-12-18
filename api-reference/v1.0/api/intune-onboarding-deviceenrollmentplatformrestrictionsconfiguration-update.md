---
title: Actualizar deviceEnrollmentPlatformRestrictionsConfiguration
description: Actualice las propiedades de un objeto deviceEnrollmentPlatformRestrictionsConfiguration.
author: tfitzmac
ms.openlocfilehash: dc7ac904df5ae18b0476cfeeb2d1c98a6533a7c3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308207"
---
# <a name="update-deviceenrollmentplatformrestrictionsconfiguration"></a><span data-ttu-id="cd660-103">Actualizar deviceEnrollmentPlatformRestrictionsConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd660-103">Update deviceEnrollmentPlatformRestrictionsConfiguration</span></span>

> <span data-ttu-id="cd660-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cd660-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cd660-105">Actualice las propiedades de un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="cd660-105">Update the properties of a [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cd660-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cd660-106">Prerequisites</span></span>
<span data-ttu-id="cd660-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cd660-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cd660-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cd660-109">Permission type</span></span>|<span data-ttu-id="cd660-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cd660-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cd660-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cd660-111">Delegated (work or school account)</span></span>|<span data-ttu-id="cd660-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cd660-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="cd660-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cd660-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cd660-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cd660-114">Not supported.</span></span>|
|<span data-ttu-id="cd660-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cd660-115">Application</span></span>|<span data-ttu-id="cd660-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cd660-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cd660-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cd660-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="cd660-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cd660-118">Request headers</span></span>
|<span data-ttu-id="cd660-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd660-119">Header</span></span>|<span data-ttu-id="cd660-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cd660-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cd660-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="cd660-121">Authorization</span></span>|<span data-ttu-id="cd660-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cd660-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cd660-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cd660-123">Accept</span></span>|<span data-ttu-id="cd660-124">application/json</span><span class="sxs-lookup"><span data-stu-id="cd660-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cd660-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cd660-125">Request body</span></span>
<span data-ttu-id="cd660-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="cd660-126">In the request body, supply a JSON representation for the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>

<span data-ttu-id="cd660-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="cd660-127">The following table shows the properties that are required when you create the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span></span>

|<span data-ttu-id="cd660-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cd660-128">Property</span></span>|<span data-ttu-id="cd660-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd660-129">Type</span></span>|<span data-ttu-id="cd660-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd660-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cd660-131">id</span><span class="sxs-lookup"><span data-stu-id="cd660-131">id</span></span>|<span data-ttu-id="cd660-132">String</span><span class="sxs-lookup"><span data-stu-id="cd660-132">String</span></span>|<span data-ttu-id="cd660-133">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cd660-133">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cd660-134">displayName</span><span class="sxs-lookup"><span data-stu-id="cd660-134">displayName</span></span>|<span data-ttu-id="cd660-135">String</span><span class="sxs-lookup"><span data-stu-id="cd660-135">String</span></span>|<span data-ttu-id="cd660-136">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cd660-136">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cd660-137">descripción</span><span class="sxs-lookup"><span data-stu-id="cd660-137">description</span></span>|<span data-ttu-id="cd660-138">String</span><span class="sxs-lookup"><span data-stu-id="cd660-138">String</span></span>|<span data-ttu-id="cd660-139">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cd660-139">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cd660-140">prioridad</span><span class="sxs-lookup"><span data-stu-id="cd660-140">priority</span></span>|<span data-ttu-id="cd660-141">Int32</span><span class="sxs-lookup"><span data-stu-id="cd660-141">Int32</span></span>|<span data-ttu-id="cd660-142">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cd660-142">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cd660-143">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="cd660-143">createdDateTime</span></span>|<span data-ttu-id="cd660-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cd660-144">DateTimeOffset</span></span>|<span data-ttu-id="cd660-145">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cd660-145">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cd660-146">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="cd660-146">lastModifiedDateTime</span></span>|<span data-ttu-id="cd660-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cd660-147">DateTimeOffset</span></span>|<span data-ttu-id="cd660-148">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cd660-148">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cd660-149">version</span><span class="sxs-lookup"><span data-stu-id="cd660-149">version</span></span>|<span data-ttu-id="cd660-150">Int32</span><span class="sxs-lookup"><span data-stu-id="cd660-150">Int32</span></span>|<span data-ttu-id="cd660-151">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cd660-151">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cd660-152">iosRestriction</span><span class="sxs-lookup"><span data-stu-id="cd660-152">iosRestriction</span></span>|[<span data-ttu-id="cd660-153">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="cd660-153">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="cd660-154">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cd660-154">Not yet documented</span></span>|
|<span data-ttu-id="cd660-155">windowsRestriction</span><span class="sxs-lookup"><span data-stu-id="cd660-155">windowsRestriction</span></span>|[<span data-ttu-id="cd660-156">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="cd660-156">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="cd660-157">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cd660-157">Not yet documented</span></span>|
|<span data-ttu-id="cd660-158">windowsMobileRestriction</span><span class="sxs-lookup"><span data-stu-id="cd660-158">windowsMobileRestriction</span></span>|[<span data-ttu-id="cd660-159">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="cd660-159">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="cd660-160">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cd660-160">Not yet documented</span></span>|
|<span data-ttu-id="cd660-161">androidRestriction</span><span class="sxs-lookup"><span data-stu-id="cd660-161">androidRestriction</span></span>|[<span data-ttu-id="cd660-162">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="cd660-162">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="cd660-163">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cd660-163">Not yet documented</span></span>|
|<span data-ttu-id="cd660-164">macOSRestriction</span><span class="sxs-lookup"><span data-stu-id="cd660-164">macOSRestriction</span></span>|[<span data-ttu-id="cd660-165">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="cd660-165">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="cd660-166">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cd660-166">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="cd660-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd660-167">Response</span></span>
<span data-ttu-id="cd660-168">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd660-168">If successful, this method returns a `200 OK` response code and an updated [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cd660-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd660-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="cd660-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cd660-170">Request</span></span>
<span data-ttu-id="cd660-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cd660-171">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="cd660-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd660-172">Response</span></span>
<span data-ttu-id="cd660-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cd660-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




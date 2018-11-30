---
title: Crear deviceEnrollmentPlatformRestrictionsConfiguration
description: Cree un objeto deviceEnrollmentPlatformRestrictionsConfiguration.
ms.openlocfilehash: e28bea6cc182684ec10abddf97801772c111bf0e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085518"
---
# <a name="create-deviceenrollmentplatformrestrictionsconfiguration"></a><span data-ttu-id="d4a07-103">Crear deviceEnrollmentPlatformRestrictionsConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4a07-103">Create deviceEnrollmentPlatformRestrictionsConfiguration</span></span>

> <span data-ttu-id="d4a07-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d4a07-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d4a07-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d4a07-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d4a07-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d4a07-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d4a07-107">Cree un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="d4a07-107">Create a new [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d4a07-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d4a07-108">Prerequisites</span></span>
<span data-ttu-id="d4a07-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d4a07-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d4a07-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d4a07-111">Permission type</span></span>|<span data-ttu-id="d4a07-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d4a07-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d4a07-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d4a07-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d4a07-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d4a07-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="d4a07-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d4a07-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d4a07-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d4a07-116">Not supported.</span></span>|
|<span data-ttu-id="d4a07-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d4a07-117">Application</span></span>|<span data-ttu-id="d4a07-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d4a07-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d4a07-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d4a07-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceEnrollmentConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="d4a07-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d4a07-120">Request headers</span></span>
|<span data-ttu-id="d4a07-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4a07-121">Header</span></span>|<span data-ttu-id="d4a07-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d4a07-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d4a07-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="d4a07-123">Authorization</span></span>|<span data-ttu-id="d4a07-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d4a07-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d4a07-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d4a07-125">Accept</span></span>|<span data-ttu-id="d4a07-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d4a07-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d4a07-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d4a07-127">Request body</span></span>
<span data-ttu-id="d4a07-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceEnrollmentPlatformRestrictionsConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4a07-128">In the request body, supply a JSON representation for the deviceEnrollmentPlatformRestrictionsConfiguration object.</span></span>

<span data-ttu-id="d4a07-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceEnrollmentPlatformRestrictionsConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4a07-129">The following table shows the properties that are required when you create the deviceEnrollmentPlatformRestrictionsConfiguration.</span></span>

|<span data-ttu-id="d4a07-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d4a07-130">Property</span></span>|<span data-ttu-id="d4a07-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4a07-131">Type</span></span>|<span data-ttu-id="d4a07-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4a07-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d4a07-133">id</span><span class="sxs-lookup"><span data-stu-id="d4a07-133">id</span></span>|<span data-ttu-id="d4a07-134">String</span><span class="sxs-lookup"><span data-stu-id="d4a07-134">String</span></span>|<span data-ttu-id="d4a07-135">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4a07-135">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="d4a07-136">displayName</span><span class="sxs-lookup"><span data-stu-id="d4a07-136">displayName</span></span>|<span data-ttu-id="d4a07-137">String</span><span class="sxs-lookup"><span data-stu-id="d4a07-137">String</span></span>|<span data-ttu-id="d4a07-138">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4a07-138">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="d4a07-139">descripción</span><span class="sxs-lookup"><span data-stu-id="d4a07-139">description</span></span>|<span data-ttu-id="d4a07-140">String</span><span class="sxs-lookup"><span data-stu-id="d4a07-140">String</span></span>|<span data-ttu-id="d4a07-141">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4a07-141">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="d4a07-142">prioridad</span><span class="sxs-lookup"><span data-stu-id="d4a07-142">priority</span></span>|<span data-ttu-id="d4a07-143">Int32</span><span class="sxs-lookup"><span data-stu-id="d4a07-143">Int32</span></span>|<span data-ttu-id="d4a07-144">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4a07-144">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="d4a07-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d4a07-145">createdDateTime</span></span>|<span data-ttu-id="d4a07-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d4a07-146">DateTimeOffset</span></span>|<span data-ttu-id="d4a07-147">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4a07-147">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="d4a07-148">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d4a07-148">lastModifiedDateTime</span></span>|<span data-ttu-id="d4a07-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d4a07-149">DateTimeOffset</span></span>|<span data-ttu-id="d4a07-150">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4a07-150">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="d4a07-151">version</span><span class="sxs-lookup"><span data-stu-id="d4a07-151">version</span></span>|<span data-ttu-id="d4a07-152">Int32</span><span class="sxs-lookup"><span data-stu-id="d4a07-152">Int32</span></span>|<span data-ttu-id="d4a07-153">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4a07-153">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="d4a07-154">iosRestriction</span><span class="sxs-lookup"><span data-stu-id="d4a07-154">iosRestriction</span></span>|[<span data-ttu-id="d4a07-155">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="d4a07-155">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="d4a07-156">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d4a07-156">Not yet documented</span></span>|
|<span data-ttu-id="d4a07-157">windowsRestriction</span><span class="sxs-lookup"><span data-stu-id="d4a07-157">windowsRestriction</span></span>|[<span data-ttu-id="d4a07-158">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="d4a07-158">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="d4a07-159">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d4a07-159">Not yet documented</span></span>|
|<span data-ttu-id="d4a07-160">windowsMobileRestriction</span><span class="sxs-lookup"><span data-stu-id="d4a07-160">windowsMobileRestriction</span></span>|[<span data-ttu-id="d4a07-161">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="d4a07-161">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="d4a07-162">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d4a07-162">Not yet documented</span></span>|
|<span data-ttu-id="d4a07-163">androidRestriction</span><span class="sxs-lookup"><span data-stu-id="d4a07-163">androidRestriction</span></span>|[<span data-ttu-id="d4a07-164">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="d4a07-164">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="d4a07-165">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d4a07-165">Not yet documented</span></span>|
|<span data-ttu-id="d4a07-166">androidForWorkRestriction</span><span class="sxs-lookup"><span data-stu-id="d4a07-166">androidForWorkRestriction</span></span>|[<span data-ttu-id="d4a07-167">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="d4a07-167">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="d4a07-168">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d4a07-168">Not yet documented</span></span>|
|<span data-ttu-id="d4a07-169">macRestriction</span><span class="sxs-lookup"><span data-stu-id="d4a07-169">macRestriction</span></span>|[<span data-ttu-id="d4a07-170">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="d4a07-170">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="d4a07-171">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d4a07-171">Not yet documented</span></span>|
|<span data-ttu-id="d4a07-172">macOSRestriction</span><span class="sxs-lookup"><span data-stu-id="d4a07-172">macOSRestriction</span></span>|[<span data-ttu-id="d4a07-173">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="d4a07-173">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="d4a07-174">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d4a07-174">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="d4a07-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d4a07-175">Response</span></span>
<span data-ttu-id="d4a07-176">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d4a07-176">If successful, this method returns a `201 Created` response code and a [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d4a07-177">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d4a07-177">Example</span></span>
### <a name="request"></a><span data-ttu-id="d4a07-178">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d4a07-178">Request</span></span>
<span data-ttu-id="d4a07-179">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d4a07-179">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceEnrollmentConfigurations
Content-type: application/json
Content-length: 2295

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentPlatformRestrictionsConfiguration",
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

### <a name="response"></a><span data-ttu-id="d4a07-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d4a07-180">Response</span></span>
<span data-ttu-id="d4a07-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d4a07-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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






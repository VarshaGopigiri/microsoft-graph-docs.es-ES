---
title: Crear deviceEnrollmentPlatformRestrictionsConfiguration
description: Cree un objeto deviceEnrollmentPlatformRestrictionsConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 82ff5652cb70cb05f8df5620ba1ef59f601d6645
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846931"
---
# <a name="create-deviceenrollmentplatformrestrictionsconfiguration"></a><span data-ttu-id="3ca1c-103">Crear deviceEnrollmentPlatformRestrictionsConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ca1c-103">Create deviceEnrollmentPlatformRestrictionsConfiguration</span></span>

> <span data-ttu-id="3ca1c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3ca1c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3ca1c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3ca1c-107">Cree un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="3ca1c-107">Create a new [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3ca1c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3ca1c-108">Prerequisites</span></span>
<span data-ttu-id="3ca1c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3ca1c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3ca1c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3ca1c-111">Permission type</span></span>|<span data-ttu-id="3ca1c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3ca1c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3ca1c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3ca1c-113">Delegated (work or school account)</span></span>|<span data-ttu-id="3ca1c-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3ca1c-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="3ca1c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3ca1c-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3ca1c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-116">Not supported.</span></span>|
|<span data-ttu-id="3ca1c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3ca1c-117">Application</span></span>|<span data-ttu-id="3ca1c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3ca1c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3ca1c-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceEnrollmentConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="3ca1c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3ca1c-120">Request headers</span></span>
|<span data-ttu-id="3ca1c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ca1c-121">Header</span></span>|<span data-ttu-id="3ca1c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3ca1c-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3ca1c-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="3ca1c-123">Authorization</span></span>|<span data-ttu-id="3ca1c-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3ca1c-125">Accept</span><span class="sxs-lookup"><span data-stu-id="3ca1c-125">Accept</span></span>|<span data-ttu-id="3ca1c-126">application/json</span><span class="sxs-lookup"><span data-stu-id="3ca1c-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3ca1c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3ca1c-127">Request body</span></span>
<span data-ttu-id="3ca1c-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceEnrollmentPlatformRestrictionsConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-128">In the request body, supply a JSON representation for the deviceEnrollmentPlatformRestrictionsConfiguration object.</span></span>

<span data-ttu-id="3ca1c-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceEnrollmentPlatformRestrictionsConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-129">The following table shows the properties that are required when you create the deviceEnrollmentPlatformRestrictionsConfiguration.</span></span>

|<span data-ttu-id="3ca1c-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3ca1c-130">Property</span></span>|<span data-ttu-id="3ca1c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ca1c-131">Type</span></span>|<span data-ttu-id="3ca1c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ca1c-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3ca1c-133">id</span><span class="sxs-lookup"><span data-stu-id="3ca1c-133">id</span></span>|<span data-ttu-id="3ca1c-134">String</span><span class="sxs-lookup"><span data-stu-id="3ca1c-134">String</span></span>|<span data-ttu-id="3ca1c-135">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3ca1c-135">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="3ca1c-136">displayName</span><span class="sxs-lookup"><span data-stu-id="3ca1c-136">displayName</span></span>|<span data-ttu-id="3ca1c-137">String</span><span class="sxs-lookup"><span data-stu-id="3ca1c-137">String</span></span>|<span data-ttu-id="3ca1c-138">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3ca1c-138">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="3ca1c-139">descripción</span><span class="sxs-lookup"><span data-stu-id="3ca1c-139">description</span></span>|<span data-ttu-id="3ca1c-140">String</span><span class="sxs-lookup"><span data-stu-id="3ca1c-140">String</span></span>|<span data-ttu-id="3ca1c-141">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3ca1c-141">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="3ca1c-142">prioridad</span><span class="sxs-lookup"><span data-stu-id="3ca1c-142">priority</span></span>|<span data-ttu-id="3ca1c-143">Int32</span><span class="sxs-lookup"><span data-stu-id="3ca1c-143">Int32</span></span>|<span data-ttu-id="3ca1c-144">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3ca1c-144">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="3ca1c-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="3ca1c-145">createdDateTime</span></span>|<span data-ttu-id="3ca1c-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3ca1c-146">DateTimeOffset</span></span>|<span data-ttu-id="3ca1c-147">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3ca1c-147">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="3ca1c-148">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="3ca1c-148">lastModifiedDateTime</span></span>|<span data-ttu-id="3ca1c-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3ca1c-149">DateTimeOffset</span></span>|<span data-ttu-id="3ca1c-150">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3ca1c-150">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="3ca1c-151">version</span><span class="sxs-lookup"><span data-stu-id="3ca1c-151">version</span></span>|<span data-ttu-id="3ca1c-152">Int32</span><span class="sxs-lookup"><span data-stu-id="3ca1c-152">Int32</span></span>|<span data-ttu-id="3ca1c-153">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3ca1c-153">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="3ca1c-154">iosRestriction</span><span class="sxs-lookup"><span data-stu-id="3ca1c-154">iosRestriction</span></span>|[<span data-ttu-id="3ca1c-155">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="3ca1c-155">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="3ca1c-156">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3ca1c-156">Not yet documented</span></span>|
|<span data-ttu-id="3ca1c-157">windowsRestriction</span><span class="sxs-lookup"><span data-stu-id="3ca1c-157">windowsRestriction</span></span>|[<span data-ttu-id="3ca1c-158">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="3ca1c-158">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="3ca1c-159">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3ca1c-159">Not yet documented</span></span>|
|<span data-ttu-id="3ca1c-160">windowsMobileRestriction</span><span class="sxs-lookup"><span data-stu-id="3ca1c-160">windowsMobileRestriction</span></span>|[<span data-ttu-id="3ca1c-161">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="3ca1c-161">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="3ca1c-162">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3ca1c-162">Not yet documented</span></span>|
|<span data-ttu-id="3ca1c-163">androidRestriction</span><span class="sxs-lookup"><span data-stu-id="3ca1c-163">androidRestriction</span></span>|[<span data-ttu-id="3ca1c-164">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="3ca1c-164">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="3ca1c-165">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3ca1c-165">Not yet documented</span></span>|
|<span data-ttu-id="3ca1c-166">androidForWorkRestriction</span><span class="sxs-lookup"><span data-stu-id="3ca1c-166">androidForWorkRestriction</span></span>|[<span data-ttu-id="3ca1c-167">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="3ca1c-167">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="3ca1c-168">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3ca1c-168">Not yet documented</span></span>|
|<span data-ttu-id="3ca1c-169">macRestriction</span><span class="sxs-lookup"><span data-stu-id="3ca1c-169">macRestriction</span></span>|[<span data-ttu-id="3ca1c-170">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="3ca1c-170">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="3ca1c-171">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3ca1c-171">Not yet documented</span></span>|
|<span data-ttu-id="3ca1c-172">macOSRestriction</span><span class="sxs-lookup"><span data-stu-id="3ca1c-172">macOSRestriction</span></span>|[<span data-ttu-id="3ca1c-173">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="3ca1c-173">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="3ca1c-174">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3ca1c-174">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="3ca1c-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3ca1c-175">Response</span></span>
<span data-ttu-id="3ca1c-176">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-176">If successful, this method returns a `201 Created` response code and a [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3ca1c-177">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3ca1c-177">Example</span></span>
### <a name="request"></a><span data-ttu-id="3ca1c-178">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3ca1c-178">Request</span></span>
<span data-ttu-id="3ca1c-179">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-179">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="3ca1c-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3ca1c-180">Response</span></span>
<span data-ttu-id="3ca1c-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3ca1c-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






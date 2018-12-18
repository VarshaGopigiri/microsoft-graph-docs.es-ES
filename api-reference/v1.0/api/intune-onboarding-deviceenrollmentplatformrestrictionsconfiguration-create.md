---
title: Crear deviceEnrollmentPlatformRestrictionsConfiguration
description: Cree un objeto deviceEnrollmentPlatformRestrictionsConfiguration.
author: tfitzmac
ms.openlocfilehash: 2815043ae2a0c6f8c2130c413b15337c05fc1749
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27324265"
---
# <a name="create-deviceenrollmentplatformrestrictionsconfiguration"></a><span data-ttu-id="2b6a7-103">Crear deviceEnrollmentPlatformRestrictionsConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b6a7-103">Create deviceEnrollmentPlatformRestrictionsConfiguration</span></span>

> <span data-ttu-id="2b6a7-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2b6a7-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2b6a7-105">Cree un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="2b6a7-105">Create a new [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2b6a7-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2b6a7-106">Prerequisites</span></span>
<span data-ttu-id="2b6a7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2b6a7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2b6a7-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2b6a7-109">Permission type</span></span>|<span data-ttu-id="2b6a7-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2b6a7-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2b6a7-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2b6a7-111">Delegated (work or school account)</span></span>|<span data-ttu-id="2b6a7-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2b6a7-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="2b6a7-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2b6a7-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2b6a7-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2b6a7-114">Not supported.</span></span>|
|<span data-ttu-id="2b6a7-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2b6a7-115">Application</span></span>|<span data-ttu-id="2b6a7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2b6a7-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2b6a7-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2b6a7-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceEnrollmentConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="2b6a7-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2b6a7-118">Request headers</span></span>
|<span data-ttu-id="2b6a7-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b6a7-119">Header</span></span>|<span data-ttu-id="2b6a7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2b6a7-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2b6a7-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="2b6a7-121">Authorization</span></span>|<span data-ttu-id="2b6a7-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2b6a7-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2b6a7-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2b6a7-123">Accept</span></span>|<span data-ttu-id="2b6a7-124">application/json</span><span class="sxs-lookup"><span data-stu-id="2b6a7-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2b6a7-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2b6a7-125">Request body</span></span>
<span data-ttu-id="2b6a7-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceEnrollmentPlatformRestrictionsConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2b6a7-126">In the request body, supply a JSON representation for the deviceEnrollmentPlatformRestrictionsConfiguration object.</span></span>

<span data-ttu-id="2b6a7-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceEnrollmentPlatformRestrictionsConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2b6a7-127">The following table shows the properties that are required when you create the deviceEnrollmentPlatformRestrictionsConfiguration.</span></span>

|<span data-ttu-id="2b6a7-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2b6a7-128">Property</span></span>|<span data-ttu-id="2b6a7-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="2b6a7-129">Type</span></span>|<span data-ttu-id="2b6a7-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b6a7-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2b6a7-131">id</span><span class="sxs-lookup"><span data-stu-id="2b6a7-131">id</span></span>|<span data-ttu-id="2b6a7-132">String</span><span class="sxs-lookup"><span data-stu-id="2b6a7-132">String</span></span>|<span data-ttu-id="2b6a7-133">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2b6a7-133">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="2b6a7-134">displayName</span><span class="sxs-lookup"><span data-stu-id="2b6a7-134">displayName</span></span>|<span data-ttu-id="2b6a7-135">String</span><span class="sxs-lookup"><span data-stu-id="2b6a7-135">String</span></span>|<span data-ttu-id="2b6a7-136">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2b6a7-136">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="2b6a7-137">descripción</span><span class="sxs-lookup"><span data-stu-id="2b6a7-137">description</span></span>|<span data-ttu-id="2b6a7-138">String</span><span class="sxs-lookup"><span data-stu-id="2b6a7-138">String</span></span>|<span data-ttu-id="2b6a7-139">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2b6a7-139">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="2b6a7-140">prioridad</span><span class="sxs-lookup"><span data-stu-id="2b6a7-140">priority</span></span>|<span data-ttu-id="2b6a7-141">Int32</span><span class="sxs-lookup"><span data-stu-id="2b6a7-141">Int32</span></span>|<span data-ttu-id="2b6a7-142">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2b6a7-142">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="2b6a7-143">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2b6a7-143">createdDateTime</span></span>|<span data-ttu-id="2b6a7-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2b6a7-144">DateTimeOffset</span></span>|<span data-ttu-id="2b6a7-145">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2b6a7-145">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="2b6a7-146">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2b6a7-146">lastModifiedDateTime</span></span>|<span data-ttu-id="2b6a7-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2b6a7-147">DateTimeOffset</span></span>|<span data-ttu-id="2b6a7-148">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2b6a7-148">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="2b6a7-149">version</span><span class="sxs-lookup"><span data-stu-id="2b6a7-149">version</span></span>|<span data-ttu-id="2b6a7-150">Int32</span><span class="sxs-lookup"><span data-stu-id="2b6a7-150">Int32</span></span>|<span data-ttu-id="2b6a7-151">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2b6a7-151">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="2b6a7-152">iosRestriction</span><span class="sxs-lookup"><span data-stu-id="2b6a7-152">iosRestriction</span></span>|[<span data-ttu-id="2b6a7-153">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="2b6a7-153">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="2b6a7-154">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="2b6a7-154">Not yet documented</span></span>|
|<span data-ttu-id="2b6a7-155">windowsRestriction</span><span class="sxs-lookup"><span data-stu-id="2b6a7-155">windowsRestriction</span></span>|[<span data-ttu-id="2b6a7-156">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="2b6a7-156">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="2b6a7-157">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="2b6a7-157">Not yet documented</span></span>|
|<span data-ttu-id="2b6a7-158">windowsMobileRestriction</span><span class="sxs-lookup"><span data-stu-id="2b6a7-158">windowsMobileRestriction</span></span>|[<span data-ttu-id="2b6a7-159">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="2b6a7-159">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="2b6a7-160">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="2b6a7-160">Not yet documented</span></span>|
|<span data-ttu-id="2b6a7-161">androidRestriction</span><span class="sxs-lookup"><span data-stu-id="2b6a7-161">androidRestriction</span></span>|[<span data-ttu-id="2b6a7-162">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="2b6a7-162">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="2b6a7-163">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="2b6a7-163">Not yet documented</span></span>|
|<span data-ttu-id="2b6a7-164">macOSRestriction</span><span class="sxs-lookup"><span data-stu-id="2b6a7-164">macOSRestriction</span></span>|[<span data-ttu-id="2b6a7-165">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="2b6a7-165">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|<span data-ttu-id="2b6a7-166">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="2b6a7-166">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="2b6a7-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b6a7-167">Response</span></span>
<span data-ttu-id="2b6a7-168">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2b6a7-168">If successful, this method returns a `201 Created` response code and a [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2b6a7-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2b6a7-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="2b6a7-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b6a7-170">Request</span></span>
<span data-ttu-id="2b6a7-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2b6a7-171">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations
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

### <a name="response"></a><span data-ttu-id="2b6a7-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b6a7-172">Response</span></span>
<span data-ttu-id="2b6a7-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2b6a7-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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




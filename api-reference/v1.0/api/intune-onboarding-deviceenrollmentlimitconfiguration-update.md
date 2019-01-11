---
title: Actualizar deviceEnrollmentLimitConfiguration
description: Actualice las propiedades de un objeto deviceEnrollmentLimitConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: f41238c42159f40821b2913f51e0b46a1f21725d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27804917"
---
# <a name="update-deviceenrollmentlimitconfiguration"></a><span data-ttu-id="bca41-103">Actualizar deviceEnrollmentLimitConfiguration</span><span class="sxs-lookup"><span data-stu-id="bca41-103">Update deviceEnrollmentLimitConfiguration</span></span>

> <span data-ttu-id="bca41-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bca41-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bca41-105">Actualice las propiedades de un objeto [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="bca41-105">Update the properties of a [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bca41-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bca41-106">Prerequisites</span></span>
<span data-ttu-id="bca41-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bca41-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bca41-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bca41-109">Permission type</span></span>|<span data-ttu-id="bca41-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bca41-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bca41-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bca41-111">Delegated (work or school account)</span></span>|<span data-ttu-id="bca41-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bca41-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="bca41-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bca41-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bca41-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bca41-114">Not supported.</span></span>|
|<span data-ttu-id="bca41-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bca41-115">Application</span></span>|<span data-ttu-id="bca41-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bca41-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bca41-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bca41-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="bca41-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bca41-118">Request headers</span></span>
|<span data-ttu-id="bca41-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bca41-119">Header</span></span>|<span data-ttu-id="bca41-120">Valor</span><span class="sxs-lookup"><span data-stu-id="bca41-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bca41-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="bca41-121">Authorization</span></span>|<span data-ttu-id="bca41-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bca41-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bca41-123">Accept</span><span class="sxs-lookup"><span data-stu-id="bca41-123">Accept</span></span>|<span data-ttu-id="bca41-124">application/json</span><span class="sxs-lookup"><span data-stu-id="bca41-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bca41-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bca41-125">Request body</span></span>
<span data-ttu-id="bca41-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="bca41-126">In the request body, supply a JSON representation for the [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md) object.</span></span>

<span data-ttu-id="bca41-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="bca41-127">The following table shows the properties that are required when you create the [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md).</span></span>

|<span data-ttu-id="bca41-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bca41-128">Property</span></span>|<span data-ttu-id="bca41-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="bca41-129">Type</span></span>|<span data-ttu-id="bca41-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="bca41-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bca41-131">id</span><span class="sxs-lookup"><span data-stu-id="bca41-131">id</span></span>|<span data-ttu-id="bca41-132">String</span><span class="sxs-lookup"><span data-stu-id="bca41-132">String</span></span>|<span data-ttu-id="bca41-133">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bca41-133">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="bca41-134">displayName</span><span class="sxs-lookup"><span data-stu-id="bca41-134">displayName</span></span>|<span data-ttu-id="bca41-135">String</span><span class="sxs-lookup"><span data-stu-id="bca41-135">String</span></span>|<span data-ttu-id="bca41-136">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bca41-136">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="bca41-137">descripción</span><span class="sxs-lookup"><span data-stu-id="bca41-137">description</span></span>|<span data-ttu-id="bca41-138">String</span><span class="sxs-lookup"><span data-stu-id="bca41-138">String</span></span>|<span data-ttu-id="bca41-139">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bca41-139">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="bca41-140">prioridad</span><span class="sxs-lookup"><span data-stu-id="bca41-140">priority</span></span>|<span data-ttu-id="bca41-141">Int32</span><span class="sxs-lookup"><span data-stu-id="bca41-141">Int32</span></span>|<span data-ttu-id="bca41-142">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bca41-142">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="bca41-143">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="bca41-143">createdDateTime</span></span>|<span data-ttu-id="bca41-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bca41-144">DateTimeOffset</span></span>|<span data-ttu-id="bca41-145">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bca41-145">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="bca41-146">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="bca41-146">lastModifiedDateTime</span></span>|<span data-ttu-id="bca41-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bca41-147">DateTimeOffset</span></span>|<span data-ttu-id="bca41-148">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bca41-148">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="bca41-149">version</span><span class="sxs-lookup"><span data-stu-id="bca41-149">version</span></span>|<span data-ttu-id="bca41-150">Int32</span><span class="sxs-lookup"><span data-stu-id="bca41-150">Int32</span></span>|<span data-ttu-id="bca41-151">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bca41-151">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="bca41-152">límite</span><span class="sxs-lookup"><span data-stu-id="bca41-152">limit</span></span>|<span data-ttu-id="bca41-153">Int32</span><span class="sxs-lookup"><span data-stu-id="bca41-153">Int32</span></span>|<span data-ttu-id="bca41-154">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="bca41-154">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="bca41-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bca41-155">Response</span></span>
<span data-ttu-id="bca41-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bca41-156">If successful, this method returns a `200 OK` response code and an updated [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bca41-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bca41-157">Example</span></span>
### <a name="request"></a><span data-ttu-id="bca41-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bca41-158">Request</span></span>
<span data-ttu-id="bca41-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bca41-159">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
Content-type: application/json
Content-length: 205

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentLimitConfiguration",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "version": 7,
  "limit": 5
}
```

### <a name="response"></a><span data-ttu-id="bca41-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bca41-160">Response</span></span>
<span data-ttu-id="bca41-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bca41-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 377

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentLimitConfiguration",
  "id": "4f8c4e4c-4e4c-4f8c-4c4e-8c4f4c4e8c4f",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "limit": 5
}
```




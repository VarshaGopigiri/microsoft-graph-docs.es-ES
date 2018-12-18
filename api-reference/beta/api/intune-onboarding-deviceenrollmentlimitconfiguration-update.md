---
title: Actualizar deviceEnrollmentLimitConfiguration
description: Actualice las propiedades de un objeto deviceEnrollmentLimitConfiguration.
author: tfitzmac
ms.openlocfilehash: 2d285ad19e907e40494c5ff7da9e112be3a20112
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27329515"
---
# <a name="update-deviceenrollmentlimitconfiguration"></a><span data-ttu-id="a6907-103">Actualizar deviceEnrollmentLimitConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6907-103">Update deviceEnrollmentLimitConfiguration</span></span>

> <span data-ttu-id="a6907-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a6907-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a6907-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a6907-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a6907-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a6907-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a6907-107">Actualice las propiedades de un objeto [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="a6907-107">Update the properties of a [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a6907-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a6907-108">Prerequisites</span></span>
<span data-ttu-id="a6907-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a6907-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a6907-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a6907-111">Permission type</span></span>|<span data-ttu-id="a6907-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a6907-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a6907-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a6907-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a6907-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a6907-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="a6907-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a6907-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a6907-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a6907-116">Not supported.</span></span>|
|<span data-ttu-id="a6907-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a6907-117">Application</span></span>|<span data-ttu-id="a6907-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a6907-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a6907-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a6907-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="a6907-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a6907-120">Request headers</span></span>
|<span data-ttu-id="a6907-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6907-121">Header</span></span>|<span data-ttu-id="a6907-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a6907-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a6907-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a6907-123">Authorization</span></span>|<span data-ttu-id="a6907-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a6907-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a6907-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a6907-125">Accept</span></span>|<span data-ttu-id="a6907-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a6907-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a6907-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a6907-127">Request body</span></span>
<span data-ttu-id="a6907-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="a6907-128">In the request body, supply a JSON representation for the [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md) object.</span></span>

<span data-ttu-id="a6907-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="a6907-129">The following table shows the properties that are required when you create the [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md).</span></span>

|<span data-ttu-id="a6907-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a6907-130">Property</span></span>|<span data-ttu-id="a6907-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a6907-131">Type</span></span>|<span data-ttu-id="a6907-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6907-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a6907-133">id</span><span class="sxs-lookup"><span data-stu-id="a6907-133">id</span></span>|<span data-ttu-id="a6907-134">String</span><span class="sxs-lookup"><span data-stu-id="a6907-134">String</span></span>|<span data-ttu-id="a6907-135">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a6907-135">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="a6907-136">displayName</span><span class="sxs-lookup"><span data-stu-id="a6907-136">displayName</span></span>|<span data-ttu-id="a6907-137">String</span><span class="sxs-lookup"><span data-stu-id="a6907-137">String</span></span>|<span data-ttu-id="a6907-138">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a6907-138">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="a6907-139">descripción</span><span class="sxs-lookup"><span data-stu-id="a6907-139">description</span></span>|<span data-ttu-id="a6907-140">String</span><span class="sxs-lookup"><span data-stu-id="a6907-140">String</span></span>|<span data-ttu-id="a6907-141">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a6907-141">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="a6907-142">prioridad</span><span class="sxs-lookup"><span data-stu-id="a6907-142">priority</span></span>|<span data-ttu-id="a6907-143">Int32</span><span class="sxs-lookup"><span data-stu-id="a6907-143">Int32</span></span>|<span data-ttu-id="a6907-144">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a6907-144">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="a6907-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a6907-145">createdDateTime</span></span>|<span data-ttu-id="a6907-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a6907-146">DateTimeOffset</span></span>|<span data-ttu-id="a6907-147">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a6907-147">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="a6907-148">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a6907-148">lastModifiedDateTime</span></span>|<span data-ttu-id="a6907-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a6907-149">DateTimeOffset</span></span>|<span data-ttu-id="a6907-150">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a6907-150">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="a6907-151">version</span><span class="sxs-lookup"><span data-stu-id="a6907-151">version</span></span>|<span data-ttu-id="a6907-152">Int32</span><span class="sxs-lookup"><span data-stu-id="a6907-152">Int32</span></span>|<span data-ttu-id="a6907-153">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a6907-153">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="a6907-154">límite</span><span class="sxs-lookup"><span data-stu-id="a6907-154">limit</span></span>|<span data-ttu-id="a6907-155">Int32</span><span class="sxs-lookup"><span data-stu-id="a6907-155">Int32</span></span>|<span data-ttu-id="a6907-156">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a6907-156">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="a6907-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6907-157">Response</span></span>
<span data-ttu-id="a6907-158">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a6907-158">If successful, this method returns a `200 OK` response code and an updated [deviceEnrollmentLimitConfiguration](../resources/intune-onboarding-deviceenrollmentlimitconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a6907-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a6907-159">Example</span></span>
### <a name="request"></a><span data-ttu-id="a6907-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a6907-160">Request</span></span>
<span data-ttu-id="a6907-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a6907-161">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
Content-type: application/json
Content-length: 196

{
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "limit": 5
}
```

### <a name="response"></a><span data-ttu-id="a6907-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6907-162">Response</span></span>
<span data-ttu-id="a6907-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a6907-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






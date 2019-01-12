---
title: Actualizar windowsDefenderAdvancedThreatProtectionConfiguration
description: Actualice las propiedades de un objeto windowsDefenderAdvancedThreatProtectionConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: d06ad3b402d1666cf5746e22919adca25c29fc97
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27957189"
---
# <a name="update-windowsdefenderadvancedthreatprotectionconfiguration"></a><span data-ttu-id="5c210-103">Actualizar windowsDefenderAdvancedThreatProtectionConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c210-103">Update windowsDefenderAdvancedThreatProtectionConfiguration</span></span>

> <span data-ttu-id="5c210-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5c210-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5c210-105">Actualice las propiedades de un objeto [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="5c210-105">Update the properties of a [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5c210-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5c210-106">Prerequisites</span></span>
<span data-ttu-id="5c210-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5c210-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5c210-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5c210-109">Permission type</span></span>|<span data-ttu-id="5c210-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5c210-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5c210-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5c210-111">Delegated (work or school account)</span></span>|<span data-ttu-id="5c210-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5c210-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="5c210-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5c210-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5c210-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5c210-114">Not supported.</span></span>|
|<span data-ttu-id="5c210-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5c210-115">Application</span></span>|<span data-ttu-id="5c210-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5c210-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5c210-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5c210-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="5c210-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5c210-118">Request headers</span></span>
|<span data-ttu-id="5c210-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c210-119">Header</span></span>|<span data-ttu-id="5c210-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5c210-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5c210-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="5c210-121">Authorization</span></span>|<span data-ttu-id="5c210-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5c210-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5c210-123">Accept</span><span class="sxs-lookup"><span data-stu-id="5c210-123">Accept</span></span>|<span data-ttu-id="5c210-124">application/json</span><span class="sxs-lookup"><span data-stu-id="5c210-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5c210-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5c210-125">Request body</span></span>
<span data-ttu-id="5c210-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="5c210-126">In the request body, supply a JSON representation for the [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md) object.</span></span>

<span data-ttu-id="5c210-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="5c210-127">The following table shows the properties that are required when you create the [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md).</span></span>

|<span data-ttu-id="5c210-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5c210-128">Property</span></span>|<span data-ttu-id="5c210-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c210-129">Type</span></span>|<span data-ttu-id="5c210-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c210-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5c210-131">id</span><span class="sxs-lookup"><span data-stu-id="5c210-131">id</span></span>|<span data-ttu-id="5c210-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c210-132">String</span></span>|<span data-ttu-id="5c210-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5c210-133">Key of the entity.</span></span> <span data-ttu-id="5c210-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5c210-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5c210-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="5c210-135">lastModifiedDateTime</span></span>|<span data-ttu-id="5c210-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5c210-136">DateTimeOffset</span></span>|<span data-ttu-id="5c210-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="5c210-137">DateTime the object was last modified.</span></span> <span data-ttu-id="5c210-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5c210-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5c210-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="5c210-139">createdDateTime</span></span>|<span data-ttu-id="5c210-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5c210-140">DateTimeOffset</span></span>|<span data-ttu-id="5c210-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="5c210-141">DateTime the object was created.</span></span> <span data-ttu-id="5c210-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5c210-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5c210-143">descripción</span><span class="sxs-lookup"><span data-stu-id="5c210-143">description</span></span>|<span data-ttu-id="5c210-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c210-144">String</span></span>|<span data-ttu-id="5c210-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c210-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="5c210-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5c210-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5c210-147">displayName</span><span class="sxs-lookup"><span data-stu-id="5c210-147">displayName</span></span>|<span data-ttu-id="5c210-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c210-148">String</span></span>|<span data-ttu-id="5c210-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c210-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="5c210-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5c210-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5c210-151">version</span><span class="sxs-lookup"><span data-stu-id="5c210-151">version</span></span>|<span data-ttu-id="5c210-152">Int32</span><span class="sxs-lookup"><span data-stu-id="5c210-152">Int32</span></span>|<span data-ttu-id="5c210-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c210-153">Version of the device configuration.</span></span> <span data-ttu-id="5c210-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5c210-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5c210-155">allowSampleSharing</span><span class="sxs-lookup"><span data-stu-id="5c210-155">allowSampleSharing</span></span>|<span data-ttu-id="5c210-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c210-156">Boolean</span></span>|<span data-ttu-id="5c210-157">Regla "Permitir el uso compartido de muestras" de Windows Defender AdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="5c210-157">Windows Defender AdvancedThreatProtection "Allow Sample Sharing" Rule</span></span>|
|<span data-ttu-id="5c210-158">enableExpeditedTelemetryReporting</span><span class="sxs-lookup"><span data-stu-id="5c210-158">enableExpeditedTelemetryReporting</span></span>|<span data-ttu-id="5c210-159">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c210-159">Boolean</span></span>|<span data-ttu-id="5c210-160">Acelere la frecuencia de informes de telemetría de Protección contra amenazas avanzada de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="5c210-160">Expedite Windows Defender Advanced Threat Protection telemetry reporting frequency.</span></span>|



## <a name="response"></a><span data-ttu-id="5c210-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c210-161">Response</span></span>
<span data-ttu-id="5c210-162">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c210-162">If successful, this method returns a `200 OK` response code and an updated [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5c210-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5c210-163">Example</span></span>
### <a name="request"></a><span data-ttu-id="5c210-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5c210-164">Request</span></span>
<span data-ttu-id="5c210-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5c210-165">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 267

{
  "@odata.type": "#microsoft.graph.windowsDefenderAdvancedThreatProtectionConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "allowSampleSharing": true,
  "enableExpeditedTelemetryReporting": true
}
```

### <a name="response"></a><span data-ttu-id="5c210-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c210-166">Response</span></span>
<span data-ttu-id="5c210-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5c210-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 439

{
  "@odata.type": "#microsoft.graph.windowsDefenderAdvancedThreatProtectionConfiguration",
  "id": "294373aa-73aa-2943-aa73-4329aa734329",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "allowSampleSharing": true,
  "enableExpeditedTelemetryReporting": true
}
```




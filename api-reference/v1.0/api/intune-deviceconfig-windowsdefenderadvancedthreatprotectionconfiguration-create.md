---
title: Crear windowsDefenderAdvancedThreatProtectionConfiguration
description: Cree un objeto windowsDefenderAdvancedThreatProtectionConfiguration.
author: tfitzmac
ms.openlocfilehash: 31db5f1c254ebe5721748c4e8f35907c49b72217
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27355506"
---
# <a name="create-windowsdefenderadvancedthreatprotectionconfiguration"></a><span data-ttu-id="a281c-103">Crear windowsDefenderAdvancedThreatProtectionConfiguration</span><span class="sxs-lookup"><span data-stu-id="a281c-103">Create windowsDefenderAdvancedThreatProtectionConfiguration</span></span>

> <span data-ttu-id="a281c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a281c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a281c-105">Cree un objeto [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="a281c-105">Create a new [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a281c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a281c-106">Prerequisites</span></span>
<span data-ttu-id="a281c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a281c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a281c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a281c-109">Permission type</span></span>|<span data-ttu-id="a281c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a281c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a281c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a281c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="a281c-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a281c-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a281c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a281c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a281c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a281c-114">Not supported.</span></span>|
|<span data-ttu-id="a281c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a281c-115">Application</span></span>|<span data-ttu-id="a281c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a281c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a281c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a281c-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="a281c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a281c-118">Request headers</span></span>
|<span data-ttu-id="a281c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a281c-119">Header</span></span>|<span data-ttu-id="a281c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a281c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a281c-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="a281c-121">Authorization</span></span>|<span data-ttu-id="a281c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a281c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a281c-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a281c-123">Accept</span></span>|<span data-ttu-id="a281c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="a281c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a281c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a281c-125">Request body</span></span>
<span data-ttu-id="a281c-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsDefenderAdvancedThreatProtectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a281c-126">In the request body, supply a JSON representation for the windowsDefenderAdvancedThreatProtectionConfiguration object.</span></span>

<span data-ttu-id="a281c-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsDefenderAdvancedThreatProtectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a281c-127">The following table shows the properties that are required when you create the windowsDefenderAdvancedThreatProtectionConfiguration.</span></span>

|<span data-ttu-id="a281c-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a281c-128">Property</span></span>|<span data-ttu-id="a281c-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="a281c-129">Type</span></span>|<span data-ttu-id="a281c-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a281c-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a281c-131">id</span><span class="sxs-lookup"><span data-stu-id="a281c-131">id</span></span>|<span data-ttu-id="a281c-132">String</span><span class="sxs-lookup"><span data-stu-id="a281c-132">String</span></span>|<span data-ttu-id="a281c-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a281c-133">Key of the entity.</span></span> <span data-ttu-id="a281c-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a281c-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a281c-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a281c-135">lastModifiedDateTime</span></span>|<span data-ttu-id="a281c-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a281c-136">DateTimeOffset</span></span>|<span data-ttu-id="a281c-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="a281c-137">DateTime the object was last modified.</span></span> <span data-ttu-id="a281c-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a281c-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a281c-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a281c-139">createdDateTime</span></span>|<span data-ttu-id="a281c-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a281c-140">DateTimeOffset</span></span>|<span data-ttu-id="a281c-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="a281c-141">DateTime the object was created.</span></span> <span data-ttu-id="a281c-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a281c-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a281c-143">descripción</span><span class="sxs-lookup"><span data-stu-id="a281c-143">description</span></span>|<span data-ttu-id="a281c-144">String</span><span class="sxs-lookup"><span data-stu-id="a281c-144">String</span></span>|<span data-ttu-id="a281c-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a281c-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="a281c-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a281c-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a281c-147">displayName</span><span class="sxs-lookup"><span data-stu-id="a281c-147">displayName</span></span>|<span data-ttu-id="a281c-148">String</span><span class="sxs-lookup"><span data-stu-id="a281c-148">String</span></span>|<span data-ttu-id="a281c-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a281c-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="a281c-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a281c-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a281c-151">version</span><span class="sxs-lookup"><span data-stu-id="a281c-151">version</span></span>|<span data-ttu-id="a281c-152">Int32</span><span class="sxs-lookup"><span data-stu-id="a281c-152">Int32</span></span>|<span data-ttu-id="a281c-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a281c-153">Version of the device configuration.</span></span> <span data-ttu-id="a281c-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a281c-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a281c-155">allowSampleSharing</span><span class="sxs-lookup"><span data-stu-id="a281c-155">allowSampleSharing</span></span>|<span data-ttu-id="a281c-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="a281c-156">Boolean</span></span>|<span data-ttu-id="a281c-157">Regla "Permitir el uso compartido de muestras" de Windows Defender AdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="a281c-157">Windows Defender AdvancedThreatProtection "Allow Sample Sharing" Rule</span></span>|
|<span data-ttu-id="a281c-158">enableExpeditedTelemetryReporting</span><span class="sxs-lookup"><span data-stu-id="a281c-158">enableExpeditedTelemetryReporting</span></span>|<span data-ttu-id="a281c-159">Boolean</span><span class="sxs-lookup"><span data-stu-id="a281c-159">Boolean</span></span>|<span data-ttu-id="a281c-160">Acelere la frecuencia de informes de telemetría de Protección contra amenazas avanzada de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="a281c-160">Expedite Windows Defender Advanced Threat Protection telemetry reporting frequency.</span></span>|



## <a name="response"></a><span data-ttu-id="a281c-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a281c-161">Response</span></span>
<span data-ttu-id="a281c-162">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a281c-162">If successful, this method returns a `201 Created` response code and a [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a281c-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a281c-163">Example</span></span>
### <a name="request"></a><span data-ttu-id="a281c-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a281c-164">Request</span></span>
<span data-ttu-id="a281c-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a281c-165">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
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

### <a name="response"></a><span data-ttu-id="a281c-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a281c-166">Response</span></span>
<span data-ttu-id="a281c-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a281c-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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




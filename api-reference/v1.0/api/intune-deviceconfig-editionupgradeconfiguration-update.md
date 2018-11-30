---
title: Actualizar editionUpgradeConfiguration
description: Actualice las propiedades de un objeto editionUpgradeConfiguration.
ms.openlocfilehash: 81564ae9430566212efcc100de779dc83e9ed664
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031576"
---
# <a name="update-editionupgradeconfiguration"></a><span data-ttu-id="6e075-103">Actualizar editionUpgradeConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e075-103">Update editionUpgradeConfiguration</span></span>

> <span data-ttu-id="6e075-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6e075-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6e075-105">Actualice las propiedades de un objeto [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="6e075-105">Update the properties of a [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6e075-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6e075-106">Prerequisites</span></span>
<span data-ttu-id="6e075-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6e075-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6e075-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6e075-109">Permission type</span></span>|<span data-ttu-id="6e075-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6e075-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6e075-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6e075-111">Delegated (work or school account)</span></span>|<span data-ttu-id="6e075-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6e075-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="6e075-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6e075-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6e075-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6e075-114">Not supported.</span></span>|
|<span data-ttu-id="6e075-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6e075-115">Application</span></span>|<span data-ttu-id="6e075-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6e075-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6e075-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6e075-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="6e075-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6e075-118">Request headers</span></span>
|<span data-ttu-id="6e075-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e075-119">Header</span></span>|<span data-ttu-id="6e075-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6e075-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6e075-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="6e075-121">Authorization</span></span>|<span data-ttu-id="6e075-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6e075-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6e075-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6e075-123">Accept</span></span>|<span data-ttu-id="6e075-124">application/json</span><span class="sxs-lookup"><span data-stu-id="6e075-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6e075-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6e075-125">Request body</span></span>
<span data-ttu-id="6e075-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="6e075-126">In the request body, supply a JSON representation for the [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md) object.</span></span>

<span data-ttu-id="6e075-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="6e075-127">The following table shows the properties that are required when you create the [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md).</span></span>

|<span data-ttu-id="6e075-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6e075-128">Property</span></span>|<span data-ttu-id="6e075-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e075-129">Type</span></span>|<span data-ttu-id="6e075-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e075-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6e075-131">id</span><span class="sxs-lookup"><span data-stu-id="6e075-131">id</span></span>|<span data-ttu-id="6e075-132">String</span><span class="sxs-lookup"><span data-stu-id="6e075-132">String</span></span>|<span data-ttu-id="6e075-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6e075-133">Key of the entity.</span></span> <span data-ttu-id="6e075-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6e075-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6e075-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="6e075-135">lastModifiedDateTime</span></span>|<span data-ttu-id="6e075-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6e075-136">DateTimeOffset</span></span>|<span data-ttu-id="6e075-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="6e075-137">DateTime the object was last modified.</span></span> <span data-ttu-id="6e075-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6e075-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6e075-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="6e075-139">createdDateTime</span></span>|<span data-ttu-id="6e075-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6e075-140">DateTimeOffset</span></span>|<span data-ttu-id="6e075-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="6e075-141">DateTime the object was created.</span></span> <span data-ttu-id="6e075-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6e075-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6e075-143">descripción</span><span class="sxs-lookup"><span data-stu-id="6e075-143">description</span></span>|<span data-ttu-id="6e075-144">String</span><span class="sxs-lookup"><span data-stu-id="6e075-144">String</span></span>|<span data-ttu-id="6e075-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6e075-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="6e075-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6e075-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6e075-147">displayName</span><span class="sxs-lookup"><span data-stu-id="6e075-147">displayName</span></span>|<span data-ttu-id="6e075-148">String</span><span class="sxs-lookup"><span data-stu-id="6e075-148">String</span></span>|<span data-ttu-id="6e075-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6e075-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="6e075-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6e075-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6e075-151">version</span><span class="sxs-lookup"><span data-stu-id="6e075-151">version</span></span>|<span data-ttu-id="6e075-152">Int32</span><span class="sxs-lookup"><span data-stu-id="6e075-152">Int32</span></span>|<span data-ttu-id="6e075-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6e075-153">Version of the device configuration.</span></span> <span data-ttu-id="6e075-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6e075-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6e075-155">licenseType</span><span class="sxs-lookup"><span data-stu-id="6e075-155">licenseType</span></span>|[<span data-ttu-id="6e075-156">editionUpgradeLicenseType</span><span class="sxs-lookup"><span data-stu-id="6e075-156">editionUpgradeLicenseType</span></span>](../resources/intune-deviceconfig-editionupgradelicensetype.md)|<span data-ttu-id="6e075-157">Tipo de licencia de actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="6e075-157">Edition Upgrade License Type.</span></span> <span data-ttu-id="6e075-158">Los valores posibles son: `productKey` y `licenseFile`.</span><span class="sxs-lookup"><span data-stu-id="6e075-158">Possible values are: `productKey`, `licenseFile`.</span></span>|
|<span data-ttu-id="6e075-159">targetEdition</span><span class="sxs-lookup"><span data-stu-id="6e075-159">targetEdition</span></span>|[<span data-ttu-id="6e075-160">windows10EditionType</span><span class="sxs-lookup"><span data-stu-id="6e075-160">windows10EditionType</span></span>](../resources/intune-deviceconfig-windows10editiontype.md)|<span data-ttu-id="6e075-161">Edición de destino de la actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="6e075-161">Edition Upgrade Target Edition.</span></span> <span data-ttu-id="6e075-162">Los valores posibles son: `windows10Enterprise`, `windows10EnterpriseN`, `windows10Education`, `windows10EducationN`, `windows10MobileEnterprise`, `windows10HolographicEnterprise`, `windows10Professional`, `windows10ProfessionalN`, `windows10ProfessionalEducation`, `windows10ProfessionalEducationN`, `windows10ProfessionalWorkstation` y `windows10ProfessionalWorkstationN`.</span><span class="sxs-lookup"><span data-stu-id="6e075-162">Possible values are: `windows10Enterprise`, `windows10EnterpriseN`, `windows10Education`, `windows10EducationN`, `windows10MobileEnterprise`, `windows10HolographicEnterprise`, `windows10Professional`, `windows10ProfessionalN`, `windows10ProfessionalEducation`, `windows10ProfessionalEducationN`, `windows10ProfessionalWorkstation`, `windows10ProfessionalWorkstationN`.</span></span>|
|<span data-ttu-id="6e075-163">licencia</span><span class="sxs-lookup"><span data-stu-id="6e075-163">license</span></span>|<span data-ttu-id="6e075-164">String</span><span class="sxs-lookup"><span data-stu-id="6e075-164">String</span></span>|<span data-ttu-id="6e075-165">Contenido de archivo de actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="6e075-165">Edition Upgrade License File Content.</span></span>|
|<span data-ttu-id="6e075-166">productKey</span><span class="sxs-lookup"><span data-stu-id="6e075-166">productKey</span></span>|<span data-ttu-id="6e075-167">String</span><span class="sxs-lookup"><span data-stu-id="6e075-167">String</span></span>|<span data-ttu-id="6e075-168">Clave de producto de actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="6e075-168">Edition Upgrade Product Key.</span></span>|



## <a name="response"></a><span data-ttu-id="6e075-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e075-169">Response</span></span>
<span data-ttu-id="6e075-170">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6e075-170">If successful, this method returns a `200 OK` response code and an updated [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6e075-171">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6e075-171">Example</span></span>
### <a name="request"></a><span data-ttu-id="6e075-172">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6e075-172">Request</span></span>
<span data-ttu-id="6e075-173">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6e075-173">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 311

{
  "@odata.type": "#microsoft.graph.editionUpgradeConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "licenseType": "licenseFile",
  "targetEdition": "windows10EnterpriseN",
  "license": "License value",
  "productKey": "Product Key value"
}
```

### <a name="response"></a><span data-ttu-id="6e075-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e075-174">Response</span></span>
<span data-ttu-id="6e075-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6e075-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 483

{
  "@odata.type": "#microsoft.graph.editionUpgradeConfiguration",
  "id": "f39fc471-c471-f39f-71c4-9ff371c49ff3",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "licenseType": "licenseFile",
  "targetEdition": "windows10EnterpriseN",
  "license": "License value",
  "productKey": "Product Key value"
}
```



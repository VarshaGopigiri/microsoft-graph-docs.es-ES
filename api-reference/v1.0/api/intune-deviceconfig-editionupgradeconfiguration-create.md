---
title: Crear editionUpgradeConfiguration
description: Cree un objeto editionUpgradeConfiguration.
ms.openlocfilehash: 2c71c4514fd00c5ae50e5fe15b3a6b9c904e8ded
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028992"
---
# <a name="create-editionupgradeconfiguration"></a><span data-ttu-id="f17d5-103">Crear editionUpgradeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f17d5-103">Create editionUpgradeConfiguration</span></span>

> <span data-ttu-id="f17d5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f17d5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f17d5-105">Cree un objeto [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="f17d5-105">Create a new [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f17d5-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f17d5-106">Prerequisites</span></span>
<span data-ttu-id="f17d5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f17d5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f17d5-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f17d5-109">Permission type</span></span>|<span data-ttu-id="f17d5-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f17d5-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f17d5-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f17d5-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f17d5-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f17d5-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="f17d5-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f17d5-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f17d5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f17d5-114">Not supported.</span></span>|
|<span data-ttu-id="f17d5-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f17d5-115">Application</span></span>|<span data-ttu-id="f17d5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f17d5-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f17d5-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f17d5-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="f17d5-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f17d5-118">Request headers</span></span>
|<span data-ttu-id="f17d5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f17d5-119">Header</span></span>|<span data-ttu-id="f17d5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f17d5-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f17d5-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="f17d5-121">Authorization</span></span>|<span data-ttu-id="f17d5-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f17d5-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f17d5-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f17d5-123">Accept</span></span>|<span data-ttu-id="f17d5-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f17d5-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f17d5-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f17d5-125">Request body</span></span>
<span data-ttu-id="f17d5-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto editionUpgradeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f17d5-126">In the request body, supply a JSON representation for the editionUpgradeConfiguration object.</span></span>

<span data-ttu-id="f17d5-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto editionUpgradeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f17d5-127">The following table shows the properties that are required when you create the editionUpgradeConfiguration.</span></span>

|<span data-ttu-id="f17d5-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f17d5-128">Property</span></span>|<span data-ttu-id="f17d5-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f17d5-129">Type</span></span>|<span data-ttu-id="f17d5-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f17d5-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f17d5-131">id</span><span class="sxs-lookup"><span data-stu-id="f17d5-131">id</span></span>|<span data-ttu-id="f17d5-132">String</span><span class="sxs-lookup"><span data-stu-id="f17d5-132">String</span></span>|<span data-ttu-id="f17d5-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f17d5-133">Key of the entity.</span></span> <span data-ttu-id="f17d5-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f17d5-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f17d5-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="f17d5-135">lastModifiedDateTime</span></span>|<span data-ttu-id="f17d5-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f17d5-136">DateTimeOffset</span></span>|<span data-ttu-id="f17d5-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="f17d5-137">DateTime the object was last modified.</span></span> <span data-ttu-id="f17d5-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f17d5-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f17d5-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f17d5-139">createdDateTime</span></span>|<span data-ttu-id="f17d5-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f17d5-140">DateTimeOffset</span></span>|<span data-ttu-id="f17d5-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="f17d5-141">DateTime the object was created.</span></span> <span data-ttu-id="f17d5-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f17d5-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f17d5-143">descripción</span><span class="sxs-lookup"><span data-stu-id="f17d5-143">description</span></span>|<span data-ttu-id="f17d5-144">String</span><span class="sxs-lookup"><span data-stu-id="f17d5-144">String</span></span>|<span data-ttu-id="f17d5-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f17d5-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="f17d5-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f17d5-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f17d5-147">displayName</span><span class="sxs-lookup"><span data-stu-id="f17d5-147">displayName</span></span>|<span data-ttu-id="f17d5-148">String</span><span class="sxs-lookup"><span data-stu-id="f17d5-148">String</span></span>|<span data-ttu-id="f17d5-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f17d5-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="f17d5-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f17d5-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f17d5-151">version</span><span class="sxs-lookup"><span data-stu-id="f17d5-151">version</span></span>|<span data-ttu-id="f17d5-152">Int32</span><span class="sxs-lookup"><span data-stu-id="f17d5-152">Int32</span></span>|<span data-ttu-id="f17d5-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f17d5-153">Version of the device configuration.</span></span> <span data-ttu-id="f17d5-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f17d5-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f17d5-155">licenseType</span><span class="sxs-lookup"><span data-stu-id="f17d5-155">licenseType</span></span>|[<span data-ttu-id="f17d5-156">editionUpgradeLicenseType</span><span class="sxs-lookup"><span data-stu-id="f17d5-156">editionUpgradeLicenseType</span></span>](../resources/intune-deviceconfig-editionupgradelicensetype.md)|<span data-ttu-id="f17d5-157">Tipo de licencia de actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="f17d5-157">Edition Upgrade License Type.</span></span> <span data-ttu-id="f17d5-158">Los valores posibles son: `productKey` y `licenseFile`.</span><span class="sxs-lookup"><span data-stu-id="f17d5-158">Possible values are: `productKey`, `licenseFile`.</span></span>|
|<span data-ttu-id="f17d5-159">targetEdition</span><span class="sxs-lookup"><span data-stu-id="f17d5-159">targetEdition</span></span>|[<span data-ttu-id="f17d5-160">windows10EditionType</span><span class="sxs-lookup"><span data-stu-id="f17d5-160">windows10EditionType</span></span>](../resources/intune-deviceconfig-windows10editiontype.md)|<span data-ttu-id="f17d5-161">Edición de destino de la actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="f17d5-161">Edition Upgrade Target Edition.</span></span> <span data-ttu-id="f17d5-162">Los valores posibles son: `windows10Enterprise`, `windows10EnterpriseN`, `windows10Education`, `windows10EducationN`, `windows10MobileEnterprise`, `windows10HolographicEnterprise`, `windows10Professional`, `windows10ProfessionalN`, `windows10ProfessionalEducation`, `windows10ProfessionalEducationN`, `windows10ProfessionalWorkstation` y `windows10ProfessionalWorkstationN`.</span><span class="sxs-lookup"><span data-stu-id="f17d5-162">Possible values are: `windows10Enterprise`, `windows10EnterpriseN`, `windows10Education`, `windows10EducationN`, `windows10MobileEnterprise`, `windows10HolographicEnterprise`, `windows10Professional`, `windows10ProfessionalN`, `windows10ProfessionalEducation`, `windows10ProfessionalEducationN`, `windows10ProfessionalWorkstation`, `windows10ProfessionalWorkstationN`.</span></span>|
|<span data-ttu-id="f17d5-163">licencia</span><span class="sxs-lookup"><span data-stu-id="f17d5-163">license</span></span>|<span data-ttu-id="f17d5-164">String</span><span class="sxs-lookup"><span data-stu-id="f17d5-164">String</span></span>|<span data-ttu-id="f17d5-165">Contenido de archivo de actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="f17d5-165">Edition Upgrade License File Content.</span></span>|
|<span data-ttu-id="f17d5-166">productKey</span><span class="sxs-lookup"><span data-stu-id="f17d5-166">productKey</span></span>|<span data-ttu-id="f17d5-167">String</span><span class="sxs-lookup"><span data-stu-id="f17d5-167">String</span></span>|<span data-ttu-id="f17d5-168">Clave de producto de actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="f17d5-168">Edition Upgrade Product Key.</span></span>|



## <a name="response"></a><span data-ttu-id="f17d5-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f17d5-169">Response</span></span>
<span data-ttu-id="f17d5-170">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f17d5-170">If successful, this method returns a `201 Created` response code and a [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f17d5-171">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f17d5-171">Example</span></span>
### <a name="request"></a><span data-ttu-id="f17d5-172">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f17d5-172">Request</span></span>
<span data-ttu-id="f17d5-173">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f17d5-173">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
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

### <a name="response"></a><span data-ttu-id="f17d5-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f17d5-174">Response</span></span>
<span data-ttu-id="f17d5-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f17d5-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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




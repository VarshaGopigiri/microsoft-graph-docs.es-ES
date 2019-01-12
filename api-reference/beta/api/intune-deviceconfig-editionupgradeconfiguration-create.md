---
title: Crear editionUpgradeConfiguration
description: Cree un objeto editionUpgradeConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 60694b4aa97b5b57c1dcb5ee15da7ba92350d2a6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939458"
---
# <a name="create-editionupgradeconfiguration"></a><span data-ttu-id="2f494-103">Crear editionUpgradeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f494-103">Create editionUpgradeConfiguration</span></span>

> <span data-ttu-id="2f494-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2f494-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2f494-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2f494-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2f494-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2f494-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2f494-107">Cree un objeto [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="2f494-107">Create a new [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2f494-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2f494-108">Prerequisites</span></span>
<span data-ttu-id="2f494-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2f494-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2f494-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2f494-111">Permission type</span></span>|<span data-ttu-id="2f494-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2f494-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2f494-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2f494-113">Delegated (work or school account)</span></span>|<span data-ttu-id="2f494-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2f494-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="2f494-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2f494-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2f494-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2f494-116">Not supported.</span></span>|
|<span data-ttu-id="2f494-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2f494-117">Application</span></span>|<span data-ttu-id="2f494-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2f494-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2f494-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2f494-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="2f494-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2f494-120">Request headers</span></span>
|<span data-ttu-id="2f494-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f494-121">Header</span></span>|<span data-ttu-id="2f494-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2f494-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2f494-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="2f494-123">Authorization</span></span>|<span data-ttu-id="2f494-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2f494-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2f494-125">Accept</span><span class="sxs-lookup"><span data-stu-id="2f494-125">Accept</span></span>|<span data-ttu-id="2f494-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2f494-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2f494-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2f494-127">Request body</span></span>
<span data-ttu-id="2f494-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto editionUpgradeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2f494-128">In the request body, supply a JSON representation for the editionUpgradeConfiguration object.</span></span>

<span data-ttu-id="2f494-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto editionUpgradeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2f494-129">The following table shows the properties that are required when you create the editionUpgradeConfiguration.</span></span>

|<span data-ttu-id="2f494-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2f494-130">Property</span></span>|<span data-ttu-id="2f494-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="2f494-131">Type</span></span>|<span data-ttu-id="2f494-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f494-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2f494-133">id</span><span class="sxs-lookup"><span data-stu-id="2f494-133">id</span></span>|<span data-ttu-id="2f494-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="2f494-134">String</span></span>|<span data-ttu-id="2f494-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2f494-135">Key of the entity.</span></span> <span data-ttu-id="2f494-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2f494-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2f494-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2f494-137">lastModifiedDateTime</span></span>|<span data-ttu-id="2f494-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2f494-138">DateTimeOffset</span></span>|<span data-ttu-id="2f494-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="2f494-139">DateTime the object was last modified.</span></span> <span data-ttu-id="2f494-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2f494-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2f494-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="2f494-141">roleScopeTagIds</span></span>|<span data-ttu-id="2f494-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="2f494-142">String collection</span></span>|<span data-ttu-id="2f494-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="2f494-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="2f494-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2f494-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2f494-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="2f494-145">supportsScopeTags</span></span>|<span data-ttu-id="2f494-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="2f494-146">Boolean</span></span>|<span data-ttu-id="2f494-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="2f494-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="2f494-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="2f494-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="2f494-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="2f494-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="2f494-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="2f494-150">This property is read-only.</span></span> <span data-ttu-id="2f494-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2f494-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2f494-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2f494-152">createdDateTime</span></span>|<span data-ttu-id="2f494-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2f494-153">DateTimeOffset</span></span>|<span data-ttu-id="2f494-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="2f494-154">DateTime the object was created.</span></span> <span data-ttu-id="2f494-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2f494-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2f494-156">descripción</span><span class="sxs-lookup"><span data-stu-id="2f494-156">description</span></span>|<span data-ttu-id="2f494-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="2f494-157">String</span></span>|<span data-ttu-id="2f494-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f494-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="2f494-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2f494-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2f494-160">displayName</span><span class="sxs-lookup"><span data-stu-id="2f494-160">displayName</span></span>|<span data-ttu-id="2f494-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="2f494-161">String</span></span>|<span data-ttu-id="2f494-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f494-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="2f494-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2f494-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2f494-164">version</span><span class="sxs-lookup"><span data-stu-id="2f494-164">version</span></span>|<span data-ttu-id="2f494-165">Int32</span><span class="sxs-lookup"><span data-stu-id="2f494-165">Int32</span></span>|<span data-ttu-id="2f494-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f494-166">Version of the device configuration.</span></span> <span data-ttu-id="2f494-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2f494-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2f494-168">licenseType</span><span class="sxs-lookup"><span data-stu-id="2f494-168">licenseType</span></span>|[<span data-ttu-id="2f494-169">editionUpgradeLicenseType</span><span class="sxs-lookup"><span data-stu-id="2f494-169">editionUpgradeLicenseType</span></span>](../resources/intune-deviceconfig-editionupgradelicensetype.md)|<span data-ttu-id="2f494-170">Tipo de licencia de actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="2f494-170">Edition Upgrade License Type.</span></span> <span data-ttu-id="2f494-171">Los valores posibles son: `productKey`, `licenseFile` y `notConfigured`.</span><span class="sxs-lookup"><span data-stu-id="2f494-171">Possible values are: `productKey`, `licenseFile`, `notConfigured`.</span></span>|
|<span data-ttu-id="2f494-172">targetEdition</span><span class="sxs-lookup"><span data-stu-id="2f494-172">targetEdition</span></span>|[<span data-ttu-id="2f494-173">windows10EditionType</span><span class="sxs-lookup"><span data-stu-id="2f494-173">windows10EditionType</span></span>](../resources/intune-deviceconfig-windows10editiontype.md)|<span data-ttu-id="2f494-174">Edición de destino de la actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="2f494-174">Edition Upgrade Target Edition.</span></span> <span data-ttu-id="2f494-175">Los valores posibles son: `windows10Enterprise`, `windows10EnterpriseN`, `windows10Education`, `windows10EducationN`, `windows10MobileEnterprise`, `windows10HolographicEnterprise`, `windows10Professional`, `windows10ProfessionalN`, `windows10ProfessionalEducation`, `windows10ProfessionalEducationN`, `windows10ProfessionalWorkstation`, `windows10ProfessionalWorkstationN`, `notConfigured`.</span><span class="sxs-lookup"><span data-stu-id="2f494-175">Possible values are: `windows10Enterprise`, `windows10EnterpriseN`, `windows10Education`, `windows10EducationN`, `windows10MobileEnterprise`, `windows10HolographicEnterprise`, `windows10Professional`, `windows10ProfessionalN`, `windows10ProfessionalEducation`, `windows10ProfessionalEducationN`, `windows10ProfessionalWorkstation`, `windows10ProfessionalWorkstationN`, `notConfigured`.</span></span>|
|<span data-ttu-id="2f494-176">licencia</span><span class="sxs-lookup"><span data-stu-id="2f494-176">license</span></span>|<span data-ttu-id="2f494-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="2f494-177">String</span></span>|<span data-ttu-id="2f494-178">Contenido de archivo de actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="2f494-178">Edition Upgrade License File Content.</span></span>|
|<span data-ttu-id="2f494-179">productKey</span><span class="sxs-lookup"><span data-stu-id="2f494-179">productKey</span></span>|<span data-ttu-id="2f494-180">Cadena</span><span class="sxs-lookup"><span data-stu-id="2f494-180">String</span></span>|<span data-ttu-id="2f494-181">Clave de producto de actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="2f494-181">Edition Upgrade Product Key.</span></span>|
|<span data-ttu-id="2f494-182">windowsSMode</span><span class="sxs-lookup"><span data-stu-id="2f494-182">windowsSMode</span></span>|[<span data-ttu-id="2f494-183">windowsSModeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f494-183">windowsSModeConfiguration</span></span>](../resources/intune-deviceconfig-windowssmodeconfiguration.md)|<span data-ttu-id="2f494-184">Configuración del modo de S.</span><span class="sxs-lookup"><span data-stu-id="2f494-184">S mode configuration.</span></span> <span data-ttu-id="2f494-185">Los valores posibles son: `noRestriction`, `block` y `unlock`.</span><span class="sxs-lookup"><span data-stu-id="2f494-185">Possible values are: `noRestriction`, `block`, `unlock`.</span></span>|



## <a name="response"></a><span data-ttu-id="2f494-186">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2f494-186">Response</span></span>
<span data-ttu-id="2f494-187">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2f494-187">If successful, this method returns a `201 Created` response code and a [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2f494-188">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2f494-188">Example</span></span>
### <a name="request"></a><span data-ttu-id="2f494-189">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2f494-189">Request</span></span>
<span data-ttu-id="2f494-190">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2f494-190">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 495

{
  "@odata.type": "#microsoft.graph.editionUpgradeConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "licenseType": "licenseFile",
  "targetEdition": "windows10EnterpriseN",
  "license": "License value",
  "productKey": "Product Key value",
  "windowsSMode": "block"
}
```

### <a name="response"></a><span data-ttu-id="2f494-191">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2f494-191">Response</span></span>
<span data-ttu-id="2f494-p114">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2f494-p114">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 603

{
  "@odata.type": "#microsoft.graph.editionUpgradeConfiguration",
  "id": "f39fc471-c471-f39f-71c4-9ff371c49ff3",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "licenseType": "licenseFile",
  "targetEdition": "windows10EnterpriseN",
  "license": "License value",
  "productKey": "Product Key value",
  "windowsSMode": "block"
}
```






---
title: Actualizar editionUpgradeConfiguration
description: Actualice las propiedades de un objeto editionUpgradeConfiguration.
author: tfitzmac
ms.openlocfilehash: 2ece07f1d0efbcf67f4c28a8fcc3dd2a0b349287
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27302117"
---
# <a name="update-editionupgradeconfiguration"></a><span data-ttu-id="11624-103">Actualizar editionUpgradeConfiguration</span><span class="sxs-lookup"><span data-stu-id="11624-103">Update editionUpgradeConfiguration</span></span>

> <span data-ttu-id="11624-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="11624-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="11624-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="11624-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="11624-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="11624-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="11624-107">Actualice las propiedades de un objeto [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="11624-107">Update the properties of a [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="11624-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="11624-108">Prerequisites</span></span>
<span data-ttu-id="11624-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="11624-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="11624-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="11624-111">Permission type</span></span>|<span data-ttu-id="11624-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="11624-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="11624-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="11624-113">Delegated (work or school account)</span></span>|<span data-ttu-id="11624-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="11624-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="11624-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="11624-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="11624-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="11624-116">Not supported.</span></span>|
|<span data-ttu-id="11624-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="11624-117">Application</span></span>|<span data-ttu-id="11624-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="11624-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="11624-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="11624-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="11624-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="11624-120">Request headers</span></span>
|<span data-ttu-id="11624-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11624-121">Header</span></span>|<span data-ttu-id="11624-122">Valor</span><span class="sxs-lookup"><span data-stu-id="11624-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="11624-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="11624-123">Authorization</span></span>|<span data-ttu-id="11624-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="11624-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="11624-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="11624-125">Accept</span></span>|<span data-ttu-id="11624-126">application/json</span><span class="sxs-lookup"><span data-stu-id="11624-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="11624-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="11624-127">Request body</span></span>
<span data-ttu-id="11624-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="11624-128">In the request body, supply a JSON representation for the [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md) object.</span></span>

<span data-ttu-id="11624-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="11624-129">The following table shows the properties that are required when you create the [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md).</span></span>

|<span data-ttu-id="11624-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11624-130">Property</span></span>|<span data-ttu-id="11624-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="11624-131">Type</span></span>|<span data-ttu-id="11624-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="11624-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="11624-133">id</span><span class="sxs-lookup"><span data-stu-id="11624-133">id</span></span>|<span data-ttu-id="11624-134">String</span><span class="sxs-lookup"><span data-stu-id="11624-134">String</span></span>|<span data-ttu-id="11624-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="11624-135">Key of the entity.</span></span> <span data-ttu-id="11624-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="11624-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="11624-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="11624-137">lastModifiedDateTime</span></span>|<span data-ttu-id="11624-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="11624-138">DateTimeOffset</span></span>|<span data-ttu-id="11624-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="11624-139">DateTime the object was last modified.</span></span> <span data-ttu-id="11624-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="11624-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="11624-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="11624-141">roleScopeTagIds</span></span>|<span data-ttu-id="11624-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="11624-142">String collection</span></span>|<span data-ttu-id="11624-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="11624-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="11624-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="11624-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="11624-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="11624-145">supportsScopeTags</span></span>|<span data-ttu-id="11624-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="11624-146">Boolean</span></span>|<span data-ttu-id="11624-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="11624-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="11624-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="11624-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="11624-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="11624-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="11624-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="11624-150">This property is read-only.</span></span> <span data-ttu-id="11624-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="11624-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="11624-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="11624-152">createdDateTime</span></span>|<span data-ttu-id="11624-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="11624-153">DateTimeOffset</span></span>|<span data-ttu-id="11624-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="11624-154">DateTime the object was created.</span></span> <span data-ttu-id="11624-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="11624-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="11624-156">descripción</span><span class="sxs-lookup"><span data-stu-id="11624-156">description</span></span>|<span data-ttu-id="11624-157">String</span><span class="sxs-lookup"><span data-stu-id="11624-157">String</span></span>|<span data-ttu-id="11624-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11624-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="11624-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="11624-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="11624-160">displayName</span><span class="sxs-lookup"><span data-stu-id="11624-160">displayName</span></span>|<span data-ttu-id="11624-161">String</span><span class="sxs-lookup"><span data-stu-id="11624-161">String</span></span>|<span data-ttu-id="11624-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11624-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="11624-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="11624-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="11624-164">version</span><span class="sxs-lookup"><span data-stu-id="11624-164">version</span></span>|<span data-ttu-id="11624-165">Int32</span><span class="sxs-lookup"><span data-stu-id="11624-165">Int32</span></span>|<span data-ttu-id="11624-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11624-166">Version of the device configuration.</span></span> <span data-ttu-id="11624-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="11624-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="11624-168">licenseType</span><span class="sxs-lookup"><span data-stu-id="11624-168">licenseType</span></span>|[<span data-ttu-id="11624-169">editionUpgradeLicenseType</span><span class="sxs-lookup"><span data-stu-id="11624-169">editionUpgradeLicenseType</span></span>](../resources/intune-deviceconfig-editionupgradelicensetype.md)|<span data-ttu-id="11624-170">Tipo de licencia de actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="11624-170">Edition Upgrade License Type.</span></span> <span data-ttu-id="11624-171">Los valores posibles son: `productKey`, `licenseFile` y `notConfigured`.</span><span class="sxs-lookup"><span data-stu-id="11624-171">Possible values are: `productKey`, `licenseFile`, `notConfigured`.</span></span>|
|<span data-ttu-id="11624-172">targetEdition</span><span class="sxs-lookup"><span data-stu-id="11624-172">targetEdition</span></span>|[<span data-ttu-id="11624-173">windows10EditionType</span><span class="sxs-lookup"><span data-stu-id="11624-173">windows10EditionType</span></span>](../resources/intune-deviceconfig-windows10editiontype.md)|<span data-ttu-id="11624-174">Edición de destino de la actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="11624-174">Edition Upgrade Target Edition.</span></span> <span data-ttu-id="11624-175">Los valores posibles son: `windows10Enterprise`, `windows10EnterpriseN`, `windows10Education`, `windows10EducationN`, `windows10MobileEnterprise`, `windows10HolographicEnterprise`, `windows10Professional`, `windows10ProfessionalN`, `windows10ProfessionalEducation`, `windows10ProfessionalEducationN`, `windows10ProfessionalWorkstation`, `windows10ProfessionalWorkstationN`, `notConfigured`.</span><span class="sxs-lookup"><span data-stu-id="11624-175">Possible values are: `windows10Enterprise`, `windows10EnterpriseN`, `windows10Education`, `windows10EducationN`, `windows10MobileEnterprise`, `windows10HolographicEnterprise`, `windows10Professional`, `windows10ProfessionalN`, `windows10ProfessionalEducation`, `windows10ProfessionalEducationN`, `windows10ProfessionalWorkstation`, `windows10ProfessionalWorkstationN`, `notConfigured`.</span></span>|
|<span data-ttu-id="11624-176">licencia</span><span class="sxs-lookup"><span data-stu-id="11624-176">license</span></span>|<span data-ttu-id="11624-177">String</span><span class="sxs-lookup"><span data-stu-id="11624-177">String</span></span>|<span data-ttu-id="11624-178">Contenido de archivo de actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="11624-178">Edition Upgrade License File Content.</span></span>|
|<span data-ttu-id="11624-179">productKey</span><span class="sxs-lookup"><span data-stu-id="11624-179">productKey</span></span>|<span data-ttu-id="11624-180">String</span><span class="sxs-lookup"><span data-stu-id="11624-180">String</span></span>|<span data-ttu-id="11624-181">Clave de producto de actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="11624-181">Edition Upgrade Product Key.</span></span>|
|<span data-ttu-id="11624-182">windowsSMode</span><span class="sxs-lookup"><span data-stu-id="11624-182">windowsSMode</span></span>|[<span data-ttu-id="11624-183">windowsSModeConfiguration</span><span class="sxs-lookup"><span data-stu-id="11624-183">windowsSModeConfiguration</span></span>](../resources/intune-deviceconfig-windowssmodeconfiguration.md)|<span data-ttu-id="11624-184">Configuración del modo de S.</span><span class="sxs-lookup"><span data-stu-id="11624-184">S mode configuration.</span></span> <span data-ttu-id="11624-185">Los valores posibles son: `noRestriction`, `block` y `unlock`.</span><span class="sxs-lookup"><span data-stu-id="11624-185">Possible values are: `noRestriction`, `block`, `unlock`.</span></span>|



## <a name="response"></a><span data-ttu-id="11624-186">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11624-186">Response</span></span>
<span data-ttu-id="11624-187">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="11624-187">If successful, this method returns a `200 OK` response code and an updated [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="11624-188">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="11624-188">Example</span></span>
### <a name="request"></a><span data-ttu-id="11624-189">Solicitud</span><span class="sxs-lookup"><span data-stu-id="11624-189">Request</span></span>
<span data-ttu-id="11624-190">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="11624-190">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 429

{
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

### <a name="response"></a><span data-ttu-id="11624-191">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11624-191">Response</span></span>
<span data-ttu-id="11624-p114">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="11624-p114">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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






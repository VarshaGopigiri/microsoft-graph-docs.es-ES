---
title: Actualizar windows10EnterpriseModernAppManagementConfiguration
description: Actualice las propiedades de un objeto windows10EnterpriseModernAppManagementConfiguration.
author: tfitzmac
ms.openlocfilehash: f01daf0847fc22d68b9ebe186ea164b8b8dfb65d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27345692"
---
# <a name="update-windows10enterprisemodernappmanagementconfiguration"></a><span data-ttu-id="c4caf-103">Actualizar windows10EnterpriseModernAppManagementConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4caf-103">Update windows10EnterpriseModernAppManagementConfiguration</span></span>

> <span data-ttu-id="c4caf-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c4caf-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c4caf-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c4caf-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c4caf-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c4caf-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c4caf-107">Actualice las propiedades de un objeto [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="c4caf-107">Update the properties of a [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c4caf-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c4caf-108">Prerequisites</span></span>
<span data-ttu-id="c4caf-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c4caf-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c4caf-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c4caf-111">Permission type</span></span>|<span data-ttu-id="c4caf-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c4caf-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c4caf-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c4caf-113">Delegated (work or school account)</span></span>|<span data-ttu-id="c4caf-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c4caf-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="c4caf-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c4caf-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c4caf-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c4caf-116">Not supported.</span></span>|
|<span data-ttu-id="c4caf-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c4caf-117">Application</span></span>|<span data-ttu-id="c4caf-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c4caf-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c4caf-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c4caf-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="c4caf-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c4caf-120">Request headers</span></span>
|<span data-ttu-id="c4caf-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4caf-121">Header</span></span>|<span data-ttu-id="c4caf-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c4caf-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c4caf-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="c4caf-123">Authorization</span></span>|<span data-ttu-id="c4caf-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c4caf-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c4caf-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c4caf-125">Accept</span></span>|<span data-ttu-id="c4caf-126">application/json</span><span class="sxs-lookup"><span data-stu-id="c4caf-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c4caf-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c4caf-127">Request body</span></span>
<span data-ttu-id="c4caf-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="c4caf-128">In the request body, supply a JSON representation for the [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md) object.</span></span>

<span data-ttu-id="c4caf-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="c4caf-129">The following table shows the properties that are required when you create the [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md).</span></span>

|<span data-ttu-id="c4caf-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c4caf-130">Property</span></span>|<span data-ttu-id="c4caf-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4caf-131">Type</span></span>|<span data-ttu-id="c4caf-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4caf-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c4caf-133">id</span><span class="sxs-lookup"><span data-stu-id="c4caf-133">id</span></span>|<span data-ttu-id="c4caf-134">String</span><span class="sxs-lookup"><span data-stu-id="c4caf-134">String</span></span>|<span data-ttu-id="c4caf-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c4caf-135">Key of the entity.</span></span> <span data-ttu-id="c4caf-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c4caf-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c4caf-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="c4caf-137">lastModifiedDateTime</span></span>|<span data-ttu-id="c4caf-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c4caf-138">DateTimeOffset</span></span>|<span data-ttu-id="c4caf-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="c4caf-139">DateTime the object was last modified.</span></span> <span data-ttu-id="c4caf-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c4caf-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c4caf-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="c4caf-141">roleScopeTagIds</span></span>|<span data-ttu-id="c4caf-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="c4caf-142">String collection</span></span>|<span data-ttu-id="c4caf-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="c4caf-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="c4caf-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c4caf-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c4caf-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="c4caf-145">supportsScopeTags</span></span>|<span data-ttu-id="c4caf-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="c4caf-146">Boolean</span></span>|<span data-ttu-id="c4caf-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="c4caf-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="c4caf-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="c4caf-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="c4caf-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="c4caf-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="c4caf-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="c4caf-150">This property is read-only.</span></span> <span data-ttu-id="c4caf-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c4caf-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c4caf-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c4caf-152">createdDateTime</span></span>|<span data-ttu-id="c4caf-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c4caf-153">DateTimeOffset</span></span>|<span data-ttu-id="c4caf-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="c4caf-154">DateTime the object was created.</span></span> <span data-ttu-id="c4caf-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c4caf-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c4caf-156">descripción</span><span class="sxs-lookup"><span data-stu-id="c4caf-156">description</span></span>|<span data-ttu-id="c4caf-157">String</span><span class="sxs-lookup"><span data-stu-id="c4caf-157">String</span></span>|<span data-ttu-id="c4caf-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4caf-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="c4caf-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c4caf-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c4caf-160">displayName</span><span class="sxs-lookup"><span data-stu-id="c4caf-160">displayName</span></span>|<span data-ttu-id="c4caf-161">String</span><span class="sxs-lookup"><span data-stu-id="c4caf-161">String</span></span>|<span data-ttu-id="c4caf-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4caf-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="c4caf-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c4caf-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c4caf-164">version</span><span class="sxs-lookup"><span data-stu-id="c4caf-164">version</span></span>|<span data-ttu-id="c4caf-165">Int32</span><span class="sxs-lookup"><span data-stu-id="c4caf-165">Int32</span></span>|<span data-ttu-id="c4caf-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4caf-166">Version of the device configuration.</span></span> <span data-ttu-id="c4caf-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c4caf-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c4caf-168">uninstallBuiltInApps</span><span class="sxs-lookup"><span data-stu-id="c4caf-168">uninstallBuiltInApps</span></span>|<span data-ttu-id="c4caf-169">Boolean</span><span class="sxs-lookup"><span data-stu-id="c4caf-169">Boolean</span></span>|<span data-ttu-id="c4caf-170">Indica si se desinstalará o no una lista fija de aplicaciones integradas de Windows.</span><span class="sxs-lookup"><span data-stu-id="c4caf-170">Indicates whether or not to uninstall a fixed list of built-in Windows apps.</span></span>|



## <a name="response"></a><span data-ttu-id="c4caf-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c4caf-171">Response</span></span>
<span data-ttu-id="c4caf-172">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c4caf-172">If successful, this method returns a `200 OK` response code and an updated [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c4caf-173">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c4caf-173">Example</span></span>
### <a name="request"></a><span data-ttu-id="c4caf-174">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c4caf-174">Request</span></span>
<span data-ttu-id="c4caf-175">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c4caf-175">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 288

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "uninstallBuiltInApps": true
}
```

### <a name="response"></a><span data-ttu-id="c4caf-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c4caf-176">Response</span></span>
<span data-ttu-id="c4caf-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c4caf-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 486

{
  "@odata.type": "#microsoft.graph.windows10EnterpriseModernAppManagementConfiguration",
  "id": "d6577687-7687-d657-8776-57d6877657d6",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "uninstallBuiltInApps": true
}
```






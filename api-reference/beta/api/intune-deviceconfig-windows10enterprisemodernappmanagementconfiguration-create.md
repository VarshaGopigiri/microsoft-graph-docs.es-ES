---
title: Crear windows10EnterpriseModernAppManagementConfiguration
description: Cree un objeto windows10EnterpriseModernAppManagementConfiguration.
ms.openlocfilehash: be13bf64b871d17a617c9da87b142f2858b2286a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086391"
---
# <a name="create-windows10enterprisemodernappmanagementconfiguration"></a><span data-ttu-id="1a5e6-103">Crear windows10EnterpriseModernAppManagementConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a5e6-103">Create windows10EnterpriseModernAppManagementConfiguration</span></span>

> <span data-ttu-id="1a5e6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1a5e6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1a5e6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1a5e6-107">Cree un objeto [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="1a5e6-107">Create a new [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1a5e6-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1a5e6-108">Prerequisites</span></span>
<span data-ttu-id="1a5e6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1a5e6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1a5e6-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1a5e6-111">Permission type</span></span>|<span data-ttu-id="1a5e6-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1a5e6-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1a5e6-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1a5e6-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1a5e6-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1a5e6-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="1a5e6-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1a5e6-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1a5e6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-116">Not supported.</span></span>|
|<span data-ttu-id="1a5e6-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1a5e6-117">Application</span></span>|<span data-ttu-id="1a5e6-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1a5e6-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1a5e6-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="1a5e6-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1a5e6-120">Request headers</span></span>
|<span data-ttu-id="1a5e6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a5e6-121">Header</span></span>|<span data-ttu-id="1a5e6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1a5e6-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1a5e6-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="1a5e6-123">Authorization</span></span>|<span data-ttu-id="1a5e6-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1a5e6-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1a5e6-125">Accept</span></span>|<span data-ttu-id="1a5e6-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1a5e6-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1a5e6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1a5e6-127">Request body</span></span>
<span data-ttu-id="1a5e6-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows10EnterpriseModernAppManagementConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-128">In the request body, supply a JSON representation for the windows10EnterpriseModernAppManagementConfiguration object.</span></span>

<span data-ttu-id="1a5e6-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows10EnterpriseModernAppManagementConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-129">The following table shows the properties that are required when you create the windows10EnterpriseModernAppManagementConfiguration.</span></span>

|<span data-ttu-id="1a5e6-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1a5e6-130">Property</span></span>|<span data-ttu-id="1a5e6-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="1a5e6-131">Type</span></span>|<span data-ttu-id="1a5e6-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1a5e6-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1a5e6-133">id</span><span class="sxs-lookup"><span data-stu-id="1a5e6-133">id</span></span>|<span data-ttu-id="1a5e6-134">String</span><span class="sxs-lookup"><span data-stu-id="1a5e6-134">String</span></span>|<span data-ttu-id="1a5e6-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-135">Key of the entity.</span></span> <span data-ttu-id="1a5e6-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1a5e6-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1a5e6-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="1a5e6-137">lastModifiedDateTime</span></span>|<span data-ttu-id="1a5e6-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1a5e6-138">DateTimeOffset</span></span>|<span data-ttu-id="1a5e6-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-139">DateTime the object was last modified.</span></span> <span data-ttu-id="1a5e6-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1a5e6-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1a5e6-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="1a5e6-141">roleScopeTagIds</span></span>|<span data-ttu-id="1a5e6-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="1a5e6-142">String collection</span></span>|<span data-ttu-id="1a5e6-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="1a5e6-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1a5e6-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1a5e6-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="1a5e6-145">supportsScopeTags</span></span>|<span data-ttu-id="1a5e6-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="1a5e6-146">Boolean</span></span>|<span data-ttu-id="1a5e6-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="1a5e6-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="1a5e6-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="1a5e6-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-150">This property is read-only.</span></span> <span data-ttu-id="1a5e6-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1a5e6-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1a5e6-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="1a5e6-152">createdDateTime</span></span>|<span data-ttu-id="1a5e6-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1a5e6-153">DateTimeOffset</span></span>|<span data-ttu-id="1a5e6-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-154">DateTime the object was created.</span></span> <span data-ttu-id="1a5e6-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1a5e6-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1a5e6-156">descripción</span><span class="sxs-lookup"><span data-stu-id="1a5e6-156">description</span></span>|<span data-ttu-id="1a5e6-157">String</span><span class="sxs-lookup"><span data-stu-id="1a5e6-157">String</span></span>|<span data-ttu-id="1a5e6-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="1a5e6-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1a5e6-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1a5e6-160">displayName</span><span class="sxs-lookup"><span data-stu-id="1a5e6-160">displayName</span></span>|<span data-ttu-id="1a5e6-161">String</span><span class="sxs-lookup"><span data-stu-id="1a5e6-161">String</span></span>|<span data-ttu-id="1a5e6-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="1a5e6-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1a5e6-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1a5e6-164">version</span><span class="sxs-lookup"><span data-stu-id="1a5e6-164">version</span></span>|<span data-ttu-id="1a5e6-165">Int32</span><span class="sxs-lookup"><span data-stu-id="1a5e6-165">Int32</span></span>|<span data-ttu-id="1a5e6-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-166">Version of the device configuration.</span></span> <span data-ttu-id="1a5e6-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1a5e6-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1a5e6-168">uninstallBuiltInApps</span><span class="sxs-lookup"><span data-stu-id="1a5e6-168">uninstallBuiltInApps</span></span>|<span data-ttu-id="1a5e6-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="1a5e6-169">Boolean</span></span>|<span data-ttu-id="1a5e6-170">Indica si se desinstalará o no una lista fija de aplicaciones integradas de Windows.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-170">Indicates whether or not to uninstall a fixed list of built-in Windows apps.</span></span>|



## <a name="response"></a><span data-ttu-id="1a5e6-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1a5e6-171">Response</span></span>
<span data-ttu-id="1a5e6-172">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-172">If successful, this method returns a `201 Created` response code and a [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1a5e6-173">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1a5e6-173">Example</span></span>
### <a name="request"></a><span data-ttu-id="1a5e6-174">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1a5e6-174">Request</span></span>
<span data-ttu-id="1a5e6-175">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-175">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 378

{
  "@odata.type": "#microsoft.graph.windows10EnterpriseModernAppManagementConfiguration",
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

### <a name="response"></a><span data-ttu-id="1a5e6-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1a5e6-176">Response</span></span>
<span data-ttu-id="1a5e6-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





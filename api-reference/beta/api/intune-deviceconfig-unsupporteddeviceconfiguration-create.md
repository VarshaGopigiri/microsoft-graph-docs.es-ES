---
title: Crear unsupportedDeviceConfiguration
description: Crear un nuevo objeto unsupportedDeviceConfiguration.
ms.openlocfilehash: 83dd3f14d564d2e8f0511772788281a5e5748b3a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086137"
---
# <a name="create-unsupporteddeviceconfiguration"></a><span data-ttu-id="d4087-103">Crear unsupportedDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4087-103">Create unsupportedDeviceConfiguration</span></span>

> <span data-ttu-id="d4087-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d4087-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d4087-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d4087-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d4087-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d4087-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d4087-107">Crear un nuevo objeto [unsupportedDeviceConfiguration](../resources/intune-deviceconfig-unsupporteddeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="d4087-107">Create a new [unsupportedDeviceConfiguration](../resources/intune-deviceconfig-unsupporteddeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d4087-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d4087-108">Prerequisites</span></span>
<span data-ttu-id="d4087-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d4087-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d4087-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d4087-111">Permission type</span></span>|<span data-ttu-id="d4087-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d4087-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d4087-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d4087-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d4087-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d4087-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="d4087-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d4087-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d4087-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d4087-116">Not supported.</span></span>|
|<span data-ttu-id="d4087-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d4087-117">Application</span></span>|<span data-ttu-id="d4087-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d4087-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d4087-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d4087-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="d4087-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d4087-120">Request headers</span></span>
|<span data-ttu-id="d4087-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4087-121">Header</span></span>|<span data-ttu-id="d4087-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d4087-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d4087-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="d4087-123">Authorization</span></span>|<span data-ttu-id="d4087-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d4087-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d4087-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d4087-125">Accept</span></span>|<span data-ttu-id="d4087-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d4087-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d4087-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d4087-127">Request body</span></span>
<span data-ttu-id="d4087-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto unsupportedDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4087-128">In the request body, supply a JSON representation for the unsupportedDeviceConfiguration object.</span></span>

<span data-ttu-id="d4087-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el unsupportedDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4087-129">The following table shows the properties that are required when you create the unsupportedDeviceConfiguration.</span></span>

|<span data-ttu-id="d4087-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d4087-130">Property</span></span>|<span data-ttu-id="d4087-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4087-131">Type</span></span>|<span data-ttu-id="d4087-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4087-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d4087-133">id</span><span class="sxs-lookup"><span data-stu-id="d4087-133">id</span></span>|<span data-ttu-id="d4087-134">String</span><span class="sxs-lookup"><span data-stu-id="d4087-134">String</span></span>|<span data-ttu-id="d4087-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d4087-135">Key of the entity.</span></span> <span data-ttu-id="d4087-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4087-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d4087-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d4087-137">lastModifiedDateTime</span></span>|<span data-ttu-id="d4087-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d4087-138">DateTimeOffset</span></span>|<span data-ttu-id="d4087-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="d4087-139">DateTime the object was last modified.</span></span> <span data-ttu-id="d4087-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4087-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d4087-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="d4087-141">roleScopeTagIds</span></span>|<span data-ttu-id="d4087-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="d4087-142">String collection</span></span>|<span data-ttu-id="d4087-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="d4087-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="d4087-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4087-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d4087-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="d4087-145">supportsScopeTags</span></span>|<span data-ttu-id="d4087-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="d4087-146">Boolean</span></span>|<span data-ttu-id="d4087-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d4087-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="d4087-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="d4087-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="d4087-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="d4087-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="d4087-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="d4087-150">This property is read-only.</span></span> <span data-ttu-id="d4087-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4087-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d4087-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d4087-152">createdDateTime</span></span>|<span data-ttu-id="d4087-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d4087-153">DateTimeOffset</span></span>|<span data-ttu-id="d4087-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="d4087-154">DateTime the object was created.</span></span> <span data-ttu-id="d4087-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4087-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d4087-156">descripción</span><span class="sxs-lookup"><span data-stu-id="d4087-156">description</span></span>|<span data-ttu-id="d4087-157">String</span><span class="sxs-lookup"><span data-stu-id="d4087-157">String</span></span>|<span data-ttu-id="d4087-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4087-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="d4087-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4087-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d4087-160">displayName</span><span class="sxs-lookup"><span data-stu-id="d4087-160">displayName</span></span>|<span data-ttu-id="d4087-161">String</span><span class="sxs-lookup"><span data-stu-id="d4087-161">String</span></span>|<span data-ttu-id="d4087-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4087-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="d4087-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4087-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d4087-164">version</span><span class="sxs-lookup"><span data-stu-id="d4087-164">version</span></span>|<span data-ttu-id="d4087-165">Int32</span><span class="sxs-lookup"><span data-stu-id="d4087-165">Int32</span></span>|<span data-ttu-id="d4087-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4087-166">Version of the device configuration.</span></span> <span data-ttu-id="d4087-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d4087-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d4087-168">originalEntityTypeName</span><span class="sxs-lookup"><span data-stu-id="d4087-168">originalEntityTypeName</span></span>|<span data-ttu-id="d4087-169">String</span><span class="sxs-lookup"><span data-stu-id="d4087-169">String</span></span>|<span data-ttu-id="d4087-170">El tipo de entidad que se devolverá en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d4087-170">The type of entity that would be returned otherwise.</span></span>|
|<span data-ttu-id="d4087-171">details</span><span class="sxs-lookup"><span data-stu-id="d4087-171">details</span></span>|<span data-ttu-id="d4087-172">colección de [unsupportedDeviceConfigurationDetail](../resources/intune-deviceconfig-unsupporteddeviceconfigurationdetail.md)</span><span class="sxs-lookup"><span data-stu-id="d4087-172">[unsupportedDeviceConfigurationDetail](../resources/intune-deviceconfig-unsupporteddeviceconfigurationdetail.md) collection</span></span>|<span data-ttu-id="d4087-173">Obtener información detallada que describe por qué la entidad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="d4087-173">Details describing why the entity is unsupported.</span></span> <span data-ttu-id="d4087-174">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="d4087-174">This collection can contain a maximum of 1000 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="d4087-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d4087-175">Response</span></span>
<span data-ttu-id="d4087-176">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [unsupportedDeviceConfiguration](../resources/intune-deviceconfig-unsupporteddeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d4087-176">If successful, this method returns a `201 Created` response code and a [unsupportedDeviceConfiguration](../resources/intune-deviceconfig-unsupporteddeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d4087-177">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d4087-177">Example</span></span>
### <a name="request"></a><span data-ttu-id="d4087-178">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d4087-178">Request</span></span>
<span data-ttu-id="d4087-179">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d4087-179">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 582

{
  "@odata.type": "#microsoft.graph.unsupportedDeviceConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "originalEntityTypeName": "Original Entity Type Name value",
  "details": [
    {
      "@odata.type": "microsoft.graph.unsupportedDeviceConfigurationDetail",
      "message": "Message value",
      "propertyName": "Property Name value"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="d4087-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d4087-180">Response</span></span>
<span data-ttu-id="d4087-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d4087-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 690

{
  "@odata.type": "#microsoft.graph.unsupportedDeviceConfiguration",
  "id": "f80d6fc8-6fc8-f80d-c86f-0df8c86f0df8",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "originalEntityTypeName": "Original Entity Type Name value",
  "details": [
    {
      "@odata.type": "microsoft.graph.unsupportedDeviceConfigurationDetail",
      "message": "Message value",
      "propertyName": "Property Name value"
    }
  ]
}
```






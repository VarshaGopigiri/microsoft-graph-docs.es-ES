---
title: Actualizar unsupportedDeviceConfiguration
description: Actualizar las propiedades de un objeto unsupportedDeviceConfiguration.
ms.openlocfilehash: 0f8594642908aef125556f06fdca911c9530db76
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084884"
---
# <a name="update-unsupporteddeviceconfiguration"></a><span data-ttu-id="e85a7-103">Actualizar unsupportedDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e85a7-103">Update unsupportedDeviceConfiguration</span></span>

> <span data-ttu-id="e85a7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e85a7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e85a7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e85a7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e85a7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e85a7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e85a7-107">Actualizar las propiedades de un objeto [unsupportedDeviceConfiguration](../resources/intune-deviceconfig-unsupporteddeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="e85a7-107">Update the properties of a [unsupportedDeviceConfiguration](../resources/intune-deviceconfig-unsupporteddeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e85a7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e85a7-108">Prerequisites</span></span>
<span data-ttu-id="e85a7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e85a7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e85a7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e85a7-111">Permission type</span></span>|<span data-ttu-id="e85a7-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e85a7-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e85a7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e85a7-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e85a7-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e85a7-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="e85a7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e85a7-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e85a7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e85a7-116">Not supported.</span></span>|
|<span data-ttu-id="e85a7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e85a7-117">Application</span></span>|<span data-ttu-id="e85a7-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e85a7-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e85a7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e85a7-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="e85a7-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e85a7-120">Request headers</span></span>
|<span data-ttu-id="e85a7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e85a7-121">Header</span></span>|<span data-ttu-id="e85a7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e85a7-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e85a7-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="e85a7-123">Authorization</span></span>|<span data-ttu-id="e85a7-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e85a7-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e85a7-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e85a7-125">Accept</span></span>|<span data-ttu-id="e85a7-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e85a7-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e85a7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e85a7-127">Request body</span></span>
<span data-ttu-id="e85a7-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [unsupportedDeviceConfiguration](../resources/intune-deviceconfig-unsupporteddeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="e85a7-128">In the request body, supply a JSON representation for the [unsupportedDeviceConfiguration](../resources/intune-deviceconfig-unsupporteddeviceconfiguration.md) object.</span></span>

<span data-ttu-id="e85a7-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [unsupportedDeviceConfiguration](../resources/intune-deviceconfig-unsupporteddeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e85a7-129">The following table shows the properties that are required when you create the [unsupportedDeviceConfiguration](../resources/intune-deviceconfig-unsupporteddeviceconfiguration.md).</span></span>

|<span data-ttu-id="e85a7-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e85a7-130">Property</span></span>|<span data-ttu-id="e85a7-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e85a7-131">Type</span></span>|<span data-ttu-id="e85a7-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e85a7-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e85a7-133">id</span><span class="sxs-lookup"><span data-stu-id="e85a7-133">id</span></span>|<span data-ttu-id="e85a7-134">String</span><span class="sxs-lookup"><span data-stu-id="e85a7-134">String</span></span>|<span data-ttu-id="e85a7-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e85a7-135">Key of the entity.</span></span> <span data-ttu-id="e85a7-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e85a7-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e85a7-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e85a7-137">lastModifiedDateTime</span></span>|<span data-ttu-id="e85a7-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e85a7-138">DateTimeOffset</span></span>|<span data-ttu-id="e85a7-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="e85a7-139">DateTime the object was last modified.</span></span> <span data-ttu-id="e85a7-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e85a7-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e85a7-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="e85a7-141">roleScopeTagIds</span></span>|<span data-ttu-id="e85a7-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="e85a7-142">String collection</span></span>|<span data-ttu-id="e85a7-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="e85a7-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="e85a7-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e85a7-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e85a7-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="e85a7-145">supportsScopeTags</span></span>|<span data-ttu-id="e85a7-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="e85a7-146">Boolean</span></span>|<span data-ttu-id="e85a7-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e85a7-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="e85a7-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="e85a7-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="e85a7-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="e85a7-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="e85a7-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="e85a7-150">This property is read-only.</span></span> <span data-ttu-id="e85a7-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e85a7-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e85a7-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e85a7-152">createdDateTime</span></span>|<span data-ttu-id="e85a7-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e85a7-153">DateTimeOffset</span></span>|<span data-ttu-id="e85a7-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="e85a7-154">DateTime the object was created.</span></span> <span data-ttu-id="e85a7-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e85a7-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e85a7-156">descripción</span><span class="sxs-lookup"><span data-stu-id="e85a7-156">description</span></span>|<span data-ttu-id="e85a7-157">String</span><span class="sxs-lookup"><span data-stu-id="e85a7-157">String</span></span>|<span data-ttu-id="e85a7-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e85a7-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="e85a7-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e85a7-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e85a7-160">displayName</span><span class="sxs-lookup"><span data-stu-id="e85a7-160">displayName</span></span>|<span data-ttu-id="e85a7-161">String</span><span class="sxs-lookup"><span data-stu-id="e85a7-161">String</span></span>|<span data-ttu-id="e85a7-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e85a7-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="e85a7-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e85a7-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e85a7-164">version</span><span class="sxs-lookup"><span data-stu-id="e85a7-164">version</span></span>|<span data-ttu-id="e85a7-165">Int32</span><span class="sxs-lookup"><span data-stu-id="e85a7-165">Int32</span></span>|<span data-ttu-id="e85a7-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e85a7-166">Version of the device configuration.</span></span> <span data-ttu-id="e85a7-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e85a7-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e85a7-168">originalEntityTypeName</span><span class="sxs-lookup"><span data-stu-id="e85a7-168">originalEntityTypeName</span></span>|<span data-ttu-id="e85a7-169">String</span><span class="sxs-lookup"><span data-stu-id="e85a7-169">String</span></span>|<span data-ttu-id="e85a7-170">El tipo de entidad que se devolverá en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e85a7-170">The type of entity that would be returned otherwise.</span></span>|
|<span data-ttu-id="e85a7-171">details</span><span class="sxs-lookup"><span data-stu-id="e85a7-171">details</span></span>|<span data-ttu-id="e85a7-172">colección de [unsupportedDeviceConfigurationDetail](../resources/intune-deviceconfig-unsupporteddeviceconfigurationdetail.md)</span><span class="sxs-lookup"><span data-stu-id="e85a7-172">[unsupportedDeviceConfigurationDetail](../resources/intune-deviceconfig-unsupporteddeviceconfigurationdetail.md) collection</span></span>|<span data-ttu-id="e85a7-173">Obtener información detallada que describe por qué la entidad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="e85a7-173">Details describing why the entity is unsupported.</span></span> <span data-ttu-id="e85a7-174">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="e85a7-174">This collection can contain a maximum of 1000 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="e85a7-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e85a7-175">Response</span></span>
<span data-ttu-id="e85a7-176">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [unsupportedDeviceConfiguration](../resources/intune-deviceconfig-unsupporteddeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e85a7-176">If successful, this method returns a `200 OK` response code and an updated [unsupportedDeviceConfiguration](../resources/intune-deviceconfig-unsupporteddeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e85a7-177">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e85a7-177">Example</span></span>
### <a name="request"></a><span data-ttu-id="e85a7-178">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e85a7-178">Request</span></span>
<span data-ttu-id="e85a7-179">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e85a7-179">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 513

{
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

### <a name="response"></a><span data-ttu-id="e85a7-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e85a7-180">Response</span></span>
<span data-ttu-id="e85a7-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e85a7-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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





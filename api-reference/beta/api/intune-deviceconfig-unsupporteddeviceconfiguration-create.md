---
title: Crear unsupportedDeviceConfiguration
description: Crear un nuevo objeto unsupportedDeviceConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: aa776cee2504a3383db862ab4aea59fd19347f1f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27882785"
---
# <a name="create-unsupporteddeviceconfiguration"></a><span data-ttu-id="12ada-103">Crear unsupportedDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="12ada-103">Create unsupportedDeviceConfiguration</span></span>

> <span data-ttu-id="12ada-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="12ada-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="12ada-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="12ada-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="12ada-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="12ada-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="12ada-107">Crear un nuevo objeto [unsupportedDeviceConfiguration](../resources/intune-deviceconfig-unsupporteddeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="12ada-107">Create a new [unsupportedDeviceConfiguration](../resources/intune-deviceconfig-unsupporteddeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="12ada-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="12ada-108">Prerequisites</span></span>
<span data-ttu-id="12ada-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="12ada-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="12ada-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="12ada-111">Permission type</span></span>|<span data-ttu-id="12ada-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="12ada-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="12ada-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="12ada-113">Delegated (work or school account)</span></span>|<span data-ttu-id="12ada-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="12ada-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="12ada-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="12ada-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="12ada-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="12ada-116">Not supported.</span></span>|
|<span data-ttu-id="12ada-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="12ada-117">Application</span></span>|<span data-ttu-id="12ada-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="12ada-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="12ada-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="12ada-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="12ada-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="12ada-120">Request headers</span></span>
|<span data-ttu-id="12ada-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12ada-121">Header</span></span>|<span data-ttu-id="12ada-122">Valor</span><span class="sxs-lookup"><span data-stu-id="12ada-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="12ada-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="12ada-123">Authorization</span></span>|<span data-ttu-id="12ada-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="12ada-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="12ada-125">Accept</span><span class="sxs-lookup"><span data-stu-id="12ada-125">Accept</span></span>|<span data-ttu-id="12ada-126">application/json</span><span class="sxs-lookup"><span data-stu-id="12ada-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="12ada-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="12ada-127">Request body</span></span>
<span data-ttu-id="12ada-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto unsupportedDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="12ada-128">In the request body, supply a JSON representation for the unsupportedDeviceConfiguration object.</span></span>

<span data-ttu-id="12ada-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el unsupportedDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="12ada-129">The following table shows the properties that are required when you create the unsupportedDeviceConfiguration.</span></span>

|<span data-ttu-id="12ada-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="12ada-130">Property</span></span>|<span data-ttu-id="12ada-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="12ada-131">Type</span></span>|<span data-ttu-id="12ada-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="12ada-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="12ada-133">id</span><span class="sxs-lookup"><span data-stu-id="12ada-133">id</span></span>|<span data-ttu-id="12ada-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="12ada-134">String</span></span>|<span data-ttu-id="12ada-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="12ada-135">Key of the entity.</span></span> <span data-ttu-id="12ada-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="12ada-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="12ada-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="12ada-137">lastModifiedDateTime</span></span>|<span data-ttu-id="12ada-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="12ada-138">DateTimeOffset</span></span>|<span data-ttu-id="12ada-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="12ada-139">DateTime the object was last modified.</span></span> <span data-ttu-id="12ada-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="12ada-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="12ada-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="12ada-141">roleScopeTagIds</span></span>|<span data-ttu-id="12ada-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="12ada-142">String collection</span></span>|<span data-ttu-id="12ada-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="12ada-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="12ada-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="12ada-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="12ada-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="12ada-145">supportsScopeTags</span></span>|<span data-ttu-id="12ada-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="12ada-146">Boolean</span></span>|<span data-ttu-id="12ada-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="12ada-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="12ada-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="12ada-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="12ada-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="12ada-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="12ada-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="12ada-150">This property is read-only.</span></span> <span data-ttu-id="12ada-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="12ada-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="12ada-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="12ada-152">createdDateTime</span></span>|<span data-ttu-id="12ada-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="12ada-153">DateTimeOffset</span></span>|<span data-ttu-id="12ada-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="12ada-154">DateTime the object was created.</span></span> <span data-ttu-id="12ada-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="12ada-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="12ada-156">descripción</span><span class="sxs-lookup"><span data-stu-id="12ada-156">description</span></span>|<span data-ttu-id="12ada-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="12ada-157">String</span></span>|<span data-ttu-id="12ada-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12ada-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="12ada-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="12ada-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="12ada-160">displayName</span><span class="sxs-lookup"><span data-stu-id="12ada-160">displayName</span></span>|<span data-ttu-id="12ada-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="12ada-161">String</span></span>|<span data-ttu-id="12ada-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12ada-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="12ada-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="12ada-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="12ada-164">version</span><span class="sxs-lookup"><span data-stu-id="12ada-164">version</span></span>|<span data-ttu-id="12ada-165">Int32</span><span class="sxs-lookup"><span data-stu-id="12ada-165">Int32</span></span>|<span data-ttu-id="12ada-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12ada-166">Version of the device configuration.</span></span> <span data-ttu-id="12ada-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="12ada-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="12ada-168">originalEntityTypeName</span><span class="sxs-lookup"><span data-stu-id="12ada-168">originalEntityTypeName</span></span>|<span data-ttu-id="12ada-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="12ada-169">String</span></span>|<span data-ttu-id="12ada-170">El tipo de entidad que se devolverá en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="12ada-170">The type of entity that would be returned otherwise.</span></span>|
|<span data-ttu-id="12ada-171">details</span><span class="sxs-lookup"><span data-stu-id="12ada-171">details</span></span>|<span data-ttu-id="12ada-172">colección de [unsupportedDeviceConfigurationDetail](../resources/intune-deviceconfig-unsupporteddeviceconfigurationdetail.md)</span><span class="sxs-lookup"><span data-stu-id="12ada-172">[unsupportedDeviceConfigurationDetail](../resources/intune-deviceconfig-unsupporteddeviceconfigurationdetail.md) collection</span></span>|<span data-ttu-id="12ada-173">Obtener información detallada que describe por qué la entidad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="12ada-173">Details describing why the entity is unsupported.</span></span> <span data-ttu-id="12ada-174">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="12ada-174">This collection can contain a maximum of 1000 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="12ada-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="12ada-175">Response</span></span>
<span data-ttu-id="12ada-176">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [unsupportedDeviceConfiguration](../resources/intune-deviceconfig-unsupporteddeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="12ada-176">If successful, this method returns a `201 Created` response code and a [unsupportedDeviceConfiguration](../resources/intune-deviceconfig-unsupporteddeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="12ada-177">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="12ada-177">Example</span></span>
### <a name="request"></a><span data-ttu-id="12ada-178">Solicitud</span><span class="sxs-lookup"><span data-stu-id="12ada-178">Request</span></span>
<span data-ttu-id="12ada-179">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="12ada-179">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="12ada-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="12ada-180">Response</span></span>
<span data-ttu-id="12ada-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="12ada-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






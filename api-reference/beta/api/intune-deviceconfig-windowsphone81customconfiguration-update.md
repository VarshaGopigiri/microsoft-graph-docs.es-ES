---
title: Actualizar windowsPhone81CustomConfiguration
description: Actualice las propiedades de un objeto windowsPhone81CustomConfiguration.
author: tfitzmac
ms.openlocfilehash: 8ad92c8068ee1c345fc4552de1bc40fb29b4f13f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27353427"
---
# <a name="update-windowsphone81customconfiguration"></a><span data-ttu-id="e250a-103">Actualizar windowsPhone81CustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="e250a-103">Update windowsPhone81CustomConfiguration</span></span>

> <span data-ttu-id="e250a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e250a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e250a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e250a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e250a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e250a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e250a-107">Actualice las propiedades de un objeto [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e250a-107">Update the properties of a [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e250a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e250a-108">Prerequisites</span></span>
<span data-ttu-id="e250a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e250a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e250a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e250a-111">Permission type</span></span>|<span data-ttu-id="e250a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e250a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e250a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e250a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e250a-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e250a-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="e250a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e250a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e250a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e250a-116">Not supported.</span></span>|
|<span data-ttu-id="e250a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e250a-117">Application</span></span>|<span data-ttu-id="e250a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e250a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e250a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e250a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="e250a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e250a-120">Request headers</span></span>
|<span data-ttu-id="e250a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e250a-121">Header</span></span>|<span data-ttu-id="e250a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e250a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e250a-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e250a-123">Authorization</span></span>|<span data-ttu-id="e250a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e250a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e250a-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e250a-125">Accept</span></span>|<span data-ttu-id="e250a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e250a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e250a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e250a-127">Request body</span></span>
<span data-ttu-id="e250a-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e250a-128">In the request body, supply a JSON representation for the [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md) object.</span></span>

<span data-ttu-id="e250a-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e250a-129">The following table shows the properties that are required when you create the [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md).</span></span>

|<span data-ttu-id="e250a-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e250a-130">Property</span></span>|<span data-ttu-id="e250a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e250a-131">Type</span></span>|<span data-ttu-id="e250a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e250a-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e250a-133">id</span><span class="sxs-lookup"><span data-stu-id="e250a-133">id</span></span>|<span data-ttu-id="e250a-134">String</span><span class="sxs-lookup"><span data-stu-id="e250a-134">String</span></span>|<span data-ttu-id="e250a-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e250a-135">Key of the entity.</span></span> <span data-ttu-id="e250a-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e250a-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e250a-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e250a-137">lastModifiedDateTime</span></span>|<span data-ttu-id="e250a-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e250a-138">DateTimeOffset</span></span>|<span data-ttu-id="e250a-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="e250a-139">DateTime the object was last modified.</span></span> <span data-ttu-id="e250a-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e250a-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e250a-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="e250a-141">roleScopeTagIds</span></span>|<span data-ttu-id="e250a-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="e250a-142">String collection</span></span>|<span data-ttu-id="e250a-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="e250a-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="e250a-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e250a-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e250a-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="e250a-145">supportsScopeTags</span></span>|<span data-ttu-id="e250a-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="e250a-146">Boolean</span></span>|<span data-ttu-id="e250a-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e250a-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="e250a-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="e250a-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="e250a-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="e250a-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="e250a-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="e250a-150">This property is read-only.</span></span> <span data-ttu-id="e250a-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e250a-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e250a-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e250a-152">createdDateTime</span></span>|<span data-ttu-id="e250a-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e250a-153">DateTimeOffset</span></span>|<span data-ttu-id="e250a-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="e250a-154">DateTime the object was created.</span></span> <span data-ttu-id="e250a-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e250a-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e250a-156">descripción</span><span class="sxs-lookup"><span data-stu-id="e250a-156">description</span></span>|<span data-ttu-id="e250a-157">String</span><span class="sxs-lookup"><span data-stu-id="e250a-157">String</span></span>|<span data-ttu-id="e250a-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e250a-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="e250a-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e250a-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e250a-160">displayName</span><span class="sxs-lookup"><span data-stu-id="e250a-160">displayName</span></span>|<span data-ttu-id="e250a-161">String</span><span class="sxs-lookup"><span data-stu-id="e250a-161">String</span></span>|<span data-ttu-id="e250a-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e250a-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="e250a-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e250a-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e250a-164">version</span><span class="sxs-lookup"><span data-stu-id="e250a-164">version</span></span>|<span data-ttu-id="e250a-165">Int32</span><span class="sxs-lookup"><span data-stu-id="e250a-165">Int32</span></span>|<span data-ttu-id="e250a-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e250a-166">Version of the device configuration.</span></span> <span data-ttu-id="e250a-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e250a-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e250a-168">omaSettings</span><span class="sxs-lookup"><span data-stu-id="e250a-168">omaSettings</span></span>|<span data-ttu-id="e250a-169">Colección [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="e250a-169">[omaSetting](../resources/intune-deviceconfig-omasetting.md) collection</span></span>|<span data-ttu-id="e250a-170">Configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="e250a-170">OMA settings.</span></span> <span data-ttu-id="e250a-171">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="e250a-171">This collection can contain a maximum of 1000 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="e250a-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e250a-172">Response</span></span>
<span data-ttu-id="e250a-173">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e250a-173">If successful, this method returns a `200 OK` response code and an updated [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e250a-174">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e250a-174">Example</span></span>
### <a name="request"></a><span data-ttu-id="e250a-175">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e250a-175">Request</span></span>
<span data-ttu-id="e250a-176">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e250a-176">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 493

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "omaSettings": [
    {
      "@odata.type": "microsoft.graph.omaSettingInteger",
      "displayName": "Display Name value",
      "description": "Description value",
      "omaUri": "Oma Uri value",
      "value": 5
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="e250a-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e250a-177">Response</span></span>
<span data-ttu-id="e250a-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e250a-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 673

{
  "@odata.type": "#microsoft.graph.windowsPhone81CustomConfiguration",
  "id": "0d98693c-693c-0d98-3c69-980d3c69980d",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "omaSettings": [
    {
      "@odata.type": "microsoft.graph.omaSettingInteger",
      "displayName": "Display Name value",
      "description": "Description value",
      "omaUri": "Oma Uri value",
      "value": 5
    }
  ]
}
```






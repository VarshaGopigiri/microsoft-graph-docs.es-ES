---
title: Actualizar androidWorkProfileCustomConfiguration
description: Actualizar las propiedades de un objeto androidWorkProfileCustomConfiguration.
ms.openlocfilehash: 70f733344a7aa79d851fe1275a04760645586765
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085304"
---
# <a name="update-androidworkprofilecustomconfiguration"></a><span data-ttu-id="46bec-103">Actualizar androidWorkProfileCustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="46bec-103">Update androidWorkProfileCustomConfiguration</span></span>

> <span data-ttu-id="46bec-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="46bec-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="46bec-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="46bec-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="46bec-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="46bec-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="46bec-107">Actualizar las propiedades de un objeto [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="46bec-107">Update the properties of a [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="46bec-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="46bec-108">Prerequisites</span></span>
<span data-ttu-id="46bec-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="46bec-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="46bec-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="46bec-111">Permission type</span></span>|<span data-ttu-id="46bec-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="46bec-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="46bec-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="46bec-113">Delegated (work or school account)</span></span>|<span data-ttu-id="46bec-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="46bec-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="46bec-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="46bec-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="46bec-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="46bec-116">Not supported.</span></span>|
|<span data-ttu-id="46bec-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="46bec-117">Application</span></span>|<span data-ttu-id="46bec-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="46bec-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="46bec-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="46bec-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="46bec-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="46bec-120">Request headers</span></span>
|<span data-ttu-id="46bec-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46bec-121">Header</span></span>|<span data-ttu-id="46bec-122">Valor</span><span class="sxs-lookup"><span data-stu-id="46bec-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="46bec-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="46bec-123">Authorization</span></span>|<span data-ttu-id="46bec-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="46bec-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="46bec-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="46bec-125">Accept</span></span>|<span data-ttu-id="46bec-126">application/json</span><span class="sxs-lookup"><span data-stu-id="46bec-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="46bec-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="46bec-127">Request body</span></span>
<span data-ttu-id="46bec-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="46bec-128">In the request body, supply a JSON representation for the [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) object.</span></span>

<span data-ttu-id="46bec-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="46bec-129">The following table shows the properties that are required when you create the [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md).</span></span>

|<span data-ttu-id="46bec-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="46bec-130">Property</span></span>|<span data-ttu-id="46bec-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="46bec-131">Type</span></span>|<span data-ttu-id="46bec-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="46bec-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="46bec-133">id</span><span class="sxs-lookup"><span data-stu-id="46bec-133">id</span></span>|<span data-ttu-id="46bec-134">String</span><span class="sxs-lookup"><span data-stu-id="46bec-134">String</span></span>|<span data-ttu-id="46bec-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="46bec-135">Key of the entity.</span></span> <span data-ttu-id="46bec-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="46bec-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46bec-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="46bec-137">lastModifiedDateTime</span></span>|<span data-ttu-id="46bec-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="46bec-138">DateTimeOffset</span></span>|<span data-ttu-id="46bec-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="46bec-139">DateTime the object was last modified.</span></span> <span data-ttu-id="46bec-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="46bec-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46bec-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="46bec-141">roleScopeTagIds</span></span>|<span data-ttu-id="46bec-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="46bec-142">String collection</span></span>|<span data-ttu-id="46bec-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="46bec-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="46bec-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="46bec-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46bec-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="46bec-145">supportsScopeTags</span></span>|<span data-ttu-id="46bec-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="46bec-146">Boolean</span></span>|<span data-ttu-id="46bec-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="46bec-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="46bec-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="46bec-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="46bec-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="46bec-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="46bec-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="46bec-150">This property is read-only.</span></span> <span data-ttu-id="46bec-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="46bec-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46bec-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="46bec-152">createdDateTime</span></span>|<span data-ttu-id="46bec-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="46bec-153">DateTimeOffset</span></span>|<span data-ttu-id="46bec-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="46bec-154">DateTime the object was created.</span></span> <span data-ttu-id="46bec-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="46bec-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46bec-156">descripción</span><span class="sxs-lookup"><span data-stu-id="46bec-156">description</span></span>|<span data-ttu-id="46bec-157">String</span><span class="sxs-lookup"><span data-stu-id="46bec-157">String</span></span>|<span data-ttu-id="46bec-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46bec-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="46bec-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="46bec-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46bec-160">displayName</span><span class="sxs-lookup"><span data-stu-id="46bec-160">displayName</span></span>|<span data-ttu-id="46bec-161">String</span><span class="sxs-lookup"><span data-stu-id="46bec-161">String</span></span>|<span data-ttu-id="46bec-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46bec-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="46bec-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="46bec-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46bec-164">version</span><span class="sxs-lookup"><span data-stu-id="46bec-164">version</span></span>|<span data-ttu-id="46bec-165">Int32</span><span class="sxs-lookup"><span data-stu-id="46bec-165">Int32</span></span>|<span data-ttu-id="46bec-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46bec-166">Version of the device configuration.</span></span> <span data-ttu-id="46bec-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="46bec-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46bec-168">omaSettings</span><span class="sxs-lookup"><span data-stu-id="46bec-168">omaSettings</span></span>|<span data-ttu-id="46bec-169">Colección [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="46bec-169">[omaSetting](../resources/intune-deviceconfig-omasetting.md) collection</span></span>|<span data-ttu-id="46bec-170">Configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="46bec-170">OMA settings.</span></span> <span data-ttu-id="46bec-171">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="46bec-171">This collection can contain a maximum of 500 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="46bec-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46bec-172">Response</span></span>
<span data-ttu-id="46bec-173">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="46bec-173">If successful, this method returns a `200 OK` response code and an updated [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="46bec-174">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="46bec-174">Example</span></span>
### <a name="request"></a><span data-ttu-id="46bec-175">Solicitud</span><span class="sxs-lookup"><span data-stu-id="46bec-175">Request</span></span>
<span data-ttu-id="46bec-176">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="46bec-176">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="46bec-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46bec-177">Response</span></span>
<span data-ttu-id="46bec-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="46bec-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 677

{
  "@odata.type": "#microsoft.graph.androidWorkProfileCustomConfiguration",
  "id": "76c5d59b-d59b-76c5-9bd5-c5769bd5c576",
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





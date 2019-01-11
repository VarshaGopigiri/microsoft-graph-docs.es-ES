---
title: Crear iosEducationDeviceConfiguration
description: Crear un nuevo objeto iosEducationDeviceConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c1a03aa4919c935a3d910209d53d1b8040a8746a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27891878"
---
# <a name="create-ioseducationdeviceconfiguration"></a><span data-ttu-id="21a78-103">Crear iosEducationDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="21a78-103">Create iosEducationDeviceConfiguration</span></span>

> <span data-ttu-id="21a78-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="21a78-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="21a78-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="21a78-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="21a78-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="21a78-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="21a78-107">Crear un nuevo objeto [iosEducationDeviceConfiguration](../resources/intune-deviceconfig-ioseducationdeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="21a78-107">Create a new [iosEducationDeviceConfiguration](../resources/intune-deviceconfig-ioseducationdeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="21a78-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="21a78-108">Prerequisites</span></span>
<span data-ttu-id="21a78-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="21a78-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="21a78-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="21a78-111">Permission type</span></span>|<span data-ttu-id="21a78-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="21a78-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="21a78-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="21a78-113">Delegated (work or school account)</span></span>|<span data-ttu-id="21a78-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="21a78-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="21a78-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="21a78-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="21a78-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="21a78-116">Not supported.</span></span>|
|<span data-ttu-id="21a78-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="21a78-117">Application</span></span>|<span data-ttu-id="21a78-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="21a78-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="21a78-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="21a78-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="21a78-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="21a78-120">Request headers</span></span>
|<span data-ttu-id="21a78-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21a78-121">Header</span></span>|<span data-ttu-id="21a78-122">Valor</span><span class="sxs-lookup"><span data-stu-id="21a78-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="21a78-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="21a78-123">Authorization</span></span>|<span data-ttu-id="21a78-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="21a78-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="21a78-125">Accept</span><span class="sxs-lookup"><span data-stu-id="21a78-125">Accept</span></span>|<span data-ttu-id="21a78-126">application/json</span><span class="sxs-lookup"><span data-stu-id="21a78-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="21a78-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="21a78-127">Request body</span></span>
<span data-ttu-id="21a78-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto iosEducationDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="21a78-128">In the request body, supply a JSON representation for the iosEducationDeviceConfiguration object.</span></span>

<span data-ttu-id="21a78-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el iosEducationDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="21a78-129">The following table shows the properties that are required when you create the iosEducationDeviceConfiguration.</span></span>

|<span data-ttu-id="21a78-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="21a78-130">Property</span></span>|<span data-ttu-id="21a78-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="21a78-131">Type</span></span>|<span data-ttu-id="21a78-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="21a78-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="21a78-133">id</span><span class="sxs-lookup"><span data-stu-id="21a78-133">id</span></span>|<span data-ttu-id="21a78-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="21a78-134">String</span></span>|<span data-ttu-id="21a78-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="21a78-135">Key of the entity.</span></span> <span data-ttu-id="21a78-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="21a78-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="21a78-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="21a78-137">lastModifiedDateTime</span></span>|<span data-ttu-id="21a78-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="21a78-138">DateTimeOffset</span></span>|<span data-ttu-id="21a78-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="21a78-139">DateTime the object was last modified.</span></span> <span data-ttu-id="21a78-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="21a78-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="21a78-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="21a78-141">roleScopeTagIds</span></span>|<span data-ttu-id="21a78-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="21a78-142">String collection</span></span>|<span data-ttu-id="21a78-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="21a78-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="21a78-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="21a78-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="21a78-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="21a78-145">supportsScopeTags</span></span>|<span data-ttu-id="21a78-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="21a78-146">Boolean</span></span>|<span data-ttu-id="21a78-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="21a78-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="21a78-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="21a78-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="21a78-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="21a78-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="21a78-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="21a78-150">This property is read-only.</span></span> <span data-ttu-id="21a78-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="21a78-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="21a78-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="21a78-152">createdDateTime</span></span>|<span data-ttu-id="21a78-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="21a78-153">DateTimeOffset</span></span>|<span data-ttu-id="21a78-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="21a78-154">DateTime the object was created.</span></span> <span data-ttu-id="21a78-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="21a78-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="21a78-156">descripción</span><span class="sxs-lookup"><span data-stu-id="21a78-156">description</span></span>|<span data-ttu-id="21a78-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="21a78-157">String</span></span>|<span data-ttu-id="21a78-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="21a78-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="21a78-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="21a78-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="21a78-160">displayName</span><span class="sxs-lookup"><span data-stu-id="21a78-160">displayName</span></span>|<span data-ttu-id="21a78-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="21a78-161">String</span></span>|<span data-ttu-id="21a78-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="21a78-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="21a78-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="21a78-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="21a78-164">version</span><span class="sxs-lookup"><span data-stu-id="21a78-164">version</span></span>|<span data-ttu-id="21a78-165">Int32</span><span class="sxs-lookup"><span data-stu-id="21a78-165">Int32</span></span>|<span data-ttu-id="21a78-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="21a78-166">Version of the device configuration.</span></span> <span data-ttu-id="21a78-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="21a78-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|



## <a name="response"></a><span data-ttu-id="21a78-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21a78-168">Response</span></span>
<span data-ttu-id="21a78-169">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [iosEducationDeviceConfiguration](../resources/intune-deviceconfig-ioseducationdeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21a78-169">If successful, this method returns a `201 Created` response code and a [iosEducationDeviceConfiguration](../resources/intune-deviceconfig-ioseducationdeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="21a78-170">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="21a78-170">Example</span></span>
### <a name="request"></a><span data-ttu-id="21a78-171">Solicitud</span><span class="sxs-lookup"><span data-stu-id="21a78-171">Request</span></span>
<span data-ttu-id="21a78-172">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="21a78-172">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 325

{
  "@odata.type": "#microsoft.graph.iosEducationDeviceConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7
}
```

### <a name="response"></a><span data-ttu-id="21a78-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21a78-173">Response</span></span>
<span data-ttu-id="21a78-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="21a78-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 433

{
  "@odata.type": "#microsoft.graph.iosEducationDeviceConfiguration",
  "id": "3d563be4-3be4-3d56-e43b-563de43b563d",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7
}
```






---
title: Actualizar macOSCustomConfiguration
description: Actualice las propiedades de un objeto macOSCustomConfiguration.
ms.openlocfilehash: f40e06a262cffd0445a3b2f4cfcd97804cad46e4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083498"
---
# <a name="update-macoscustomconfiguration"></a><span data-ttu-id="eef4c-103">Actualizar macOSCustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="eef4c-103">Update macOSCustomConfiguration</span></span>

> <span data-ttu-id="eef4c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eef4c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eef4c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eef4c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="eef4c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="eef4c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="eef4c-107">Actualice las propiedades de un objeto [macOSCustomConfiguration](../resources/intune-deviceconfig-macoscustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="eef4c-107">Update the properties of a [macOSCustomConfiguration](../resources/intune-deviceconfig-macoscustomconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="eef4c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="eef4c-108">Prerequisites</span></span>
<span data-ttu-id="eef4c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eef4c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eef4c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eef4c-111">Permission type</span></span>|<span data-ttu-id="eef4c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eef4c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="eef4c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eef4c-113">Delegated (work or school account)</span></span>|<span data-ttu-id="eef4c-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eef4c-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="eef4c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eef4c-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="eef4c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eef4c-116">Not supported.</span></span>|
|<span data-ttu-id="eef4c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eef4c-117">Application</span></span>|<span data-ttu-id="eef4c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eef4c-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="eef4c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eef4c-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="eef4c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eef4c-120">Request headers</span></span>
|<span data-ttu-id="eef4c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eef4c-121">Header</span></span>|<span data-ttu-id="eef4c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="eef4c-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="eef4c-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="eef4c-123">Authorization</span></span>|<span data-ttu-id="eef4c-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="eef4c-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="eef4c-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="eef4c-125">Accept</span></span>|<span data-ttu-id="eef4c-126">application/json</span><span class="sxs-lookup"><span data-stu-id="eef4c-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="eef4c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eef4c-127">Request body</span></span>
<span data-ttu-id="eef4c-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [macOSCustomConfiguration](../resources/intune-deviceconfig-macoscustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="eef4c-128">In the request body, supply a JSON representation for the [macOSCustomConfiguration](../resources/intune-deviceconfig-macoscustomconfiguration.md) object.</span></span>

<span data-ttu-id="eef4c-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [macOSCustomConfiguration](../resources/intune-deviceconfig-macoscustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="eef4c-129">The following table shows the properties that are required when you create the [macOSCustomConfiguration](../resources/intune-deviceconfig-macoscustomconfiguration.md).</span></span>

|<span data-ttu-id="eef4c-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eef4c-130">Property</span></span>|<span data-ttu-id="eef4c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="eef4c-131">Type</span></span>|<span data-ttu-id="eef4c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="eef4c-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="eef4c-133">id</span><span class="sxs-lookup"><span data-stu-id="eef4c-133">id</span></span>|<span data-ttu-id="eef4c-134">String</span><span class="sxs-lookup"><span data-stu-id="eef4c-134">String</span></span>|<span data-ttu-id="eef4c-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="eef4c-135">Key of the entity.</span></span> <span data-ttu-id="eef4c-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="eef4c-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="eef4c-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="eef4c-137">lastModifiedDateTime</span></span>|<span data-ttu-id="eef4c-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="eef4c-138">DateTimeOffset</span></span>|<span data-ttu-id="eef4c-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="eef4c-139">DateTime the object was last modified.</span></span> <span data-ttu-id="eef4c-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="eef4c-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="eef4c-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="eef4c-141">roleScopeTagIds</span></span>|<span data-ttu-id="eef4c-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="eef4c-142">String collection</span></span>|<span data-ttu-id="eef4c-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="eef4c-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="eef4c-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="eef4c-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="eef4c-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="eef4c-145">supportsScopeTags</span></span>|<span data-ttu-id="eef4c-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="eef4c-146">Boolean</span></span>|<span data-ttu-id="eef4c-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="eef4c-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="eef4c-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="eef4c-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="eef4c-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="eef4c-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="eef4c-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="eef4c-150">This property is read-only.</span></span> <span data-ttu-id="eef4c-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="eef4c-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="eef4c-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="eef4c-152">createdDateTime</span></span>|<span data-ttu-id="eef4c-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="eef4c-153">DateTimeOffset</span></span>|<span data-ttu-id="eef4c-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="eef4c-154">DateTime the object was created.</span></span> <span data-ttu-id="eef4c-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="eef4c-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="eef4c-156">descripción</span><span class="sxs-lookup"><span data-stu-id="eef4c-156">description</span></span>|<span data-ttu-id="eef4c-157">String</span><span class="sxs-lookup"><span data-stu-id="eef4c-157">String</span></span>|<span data-ttu-id="eef4c-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eef4c-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="eef4c-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="eef4c-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="eef4c-160">displayName</span><span class="sxs-lookup"><span data-stu-id="eef4c-160">displayName</span></span>|<span data-ttu-id="eef4c-161">String</span><span class="sxs-lookup"><span data-stu-id="eef4c-161">String</span></span>|<span data-ttu-id="eef4c-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eef4c-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="eef4c-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="eef4c-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="eef4c-164">version</span><span class="sxs-lookup"><span data-stu-id="eef4c-164">version</span></span>|<span data-ttu-id="eef4c-165">Int32</span><span class="sxs-lookup"><span data-stu-id="eef4c-165">Int32</span></span>|<span data-ttu-id="eef4c-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eef4c-166">Version of the device configuration.</span></span> <span data-ttu-id="eef4c-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="eef4c-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="eef4c-168">payloadName</span><span class="sxs-lookup"><span data-stu-id="eef4c-168">payloadName</span></span>|<span data-ttu-id="eef4c-169">String</span><span class="sxs-lookup"><span data-stu-id="eef4c-169">String</span></span>|<span data-ttu-id="eef4c-170">Nombre que se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="eef4c-170">Name that is displayed to the user.</span></span>|
|<span data-ttu-id="eef4c-171">payloadFileName</span><span class="sxs-lookup"><span data-stu-id="eef4c-171">payloadFileName</span></span>|<span data-ttu-id="eef4c-172">String</span><span class="sxs-lookup"><span data-stu-id="eef4c-172">String</span></span>|<span data-ttu-id="eef4c-173">Nombre de archivo de carga útil (\*.mobileconfig</span><span class="sxs-lookup"><span data-stu-id="eef4c-173">Payload file name (\*.mobileconfig</span></span> | <span data-ttu-id="eef4c-174">\*.xml).</span><span class="sxs-lookup"><span data-stu-id="eef4c-174">\*.xml).</span></span>|
|<span data-ttu-id="eef4c-175">carga útil</span><span class="sxs-lookup"><span data-stu-id="eef4c-175">payload</span></span>|<span data-ttu-id="eef4c-176">Binario</span><span class="sxs-lookup"><span data-stu-id="eef4c-176">Binary</span></span>|<span data-ttu-id="eef4c-177">Carga útil.</span><span class="sxs-lookup"><span data-stu-id="eef4c-177">Payload.</span></span> <span data-ttu-id="eef4c-178">(Matriz de bytes codificada UTF8)</span><span class="sxs-lookup"><span data-stu-id="eef4c-178">(UTF8 encoded byte array)</span></span>|



## <a name="response"></a><span data-ttu-id="eef4c-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eef4c-179">Response</span></span>
<span data-ttu-id="eef4c-180">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [macOSCustomConfiguration](../resources/intune-deviceconfig-macoscustomconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eef4c-180">If successful, this method returns a `200 OK` response code and an updated [macOSCustomConfiguration](../resources/intune-deviceconfig-macoscustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eef4c-181">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eef4c-181">Example</span></span>
### <a name="request"></a><span data-ttu-id="eef4c-182">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eef4c-182">Request</span></span>
<span data-ttu-id="eef4c-183">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eef4c-183">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 374

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "payloadName": "Payload Name value",
  "payloadFileName": "Payload File Name value",
  "payload": "cGF5bG9hZA=="
}
```

### <a name="response"></a><span data-ttu-id="eef4c-184">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eef4c-184">Response</span></span>
<span data-ttu-id="eef4c-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eef4c-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 545

{
  "@odata.type": "#microsoft.graph.macOSCustomConfiguration",
  "id": "a253835d-835d-a253-5d83-53a25d8353a2",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "payloadName": "Payload Name value",
  "payloadFileName": "Payload File Name value",
  "payload": "cGF5bG9hZA=="
}
```





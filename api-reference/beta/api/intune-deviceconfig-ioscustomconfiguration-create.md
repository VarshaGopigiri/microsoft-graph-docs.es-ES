---
title: Crear iosCustomConfiguration
description: Cree un objeto iosCustomConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 55660128a2f962711ddaa33556cee7539e165c06
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858376"
---
# <a name="create-ioscustomconfiguration"></a><span data-ttu-id="b6909-103">Crear iosCustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6909-103">Create iosCustomConfiguration</span></span>

> <span data-ttu-id="b6909-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b6909-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b6909-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b6909-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b6909-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b6909-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b6909-107">Cree un objeto [iosCustomConfiguration](../resources/intune-deviceconfig-ioscustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="b6909-107">Create a new [iosCustomConfiguration](../resources/intune-deviceconfig-ioscustomconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b6909-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b6909-108">Prerequisites</span></span>
<span data-ttu-id="b6909-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b6909-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b6909-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b6909-111">Permission type</span></span>|<span data-ttu-id="b6909-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b6909-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b6909-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b6909-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b6909-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b6909-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="b6909-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b6909-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b6909-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6909-116">Not supported.</span></span>|
|<span data-ttu-id="b6909-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b6909-117">Application</span></span>|<span data-ttu-id="b6909-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6909-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b6909-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b6909-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="b6909-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b6909-120">Request headers</span></span>
|<span data-ttu-id="b6909-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6909-121">Header</span></span>|<span data-ttu-id="b6909-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b6909-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b6909-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="b6909-123">Authorization</span></span>|<span data-ttu-id="b6909-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b6909-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b6909-125">Accept</span><span class="sxs-lookup"><span data-stu-id="b6909-125">Accept</span></span>|<span data-ttu-id="b6909-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b6909-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b6909-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b6909-127">Request body</span></span>
<span data-ttu-id="b6909-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosCustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b6909-128">In the request body, supply a JSON representation for the iosCustomConfiguration object.</span></span>

<span data-ttu-id="b6909-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosCustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b6909-129">The following table shows the properties that are required when you create the iosCustomConfiguration.</span></span>

|<span data-ttu-id="b6909-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b6909-130">Property</span></span>|<span data-ttu-id="b6909-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6909-131">Type</span></span>|<span data-ttu-id="b6909-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6909-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b6909-133">id</span><span class="sxs-lookup"><span data-stu-id="b6909-133">id</span></span>|<span data-ttu-id="b6909-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="b6909-134">String</span></span>|<span data-ttu-id="b6909-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b6909-135">Key of the entity.</span></span> <span data-ttu-id="b6909-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b6909-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b6909-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b6909-137">lastModifiedDateTime</span></span>|<span data-ttu-id="b6909-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b6909-138">DateTimeOffset</span></span>|<span data-ttu-id="b6909-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="b6909-139">DateTime the object was last modified.</span></span> <span data-ttu-id="b6909-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b6909-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b6909-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="b6909-141">roleScopeTagIds</span></span>|<span data-ttu-id="b6909-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="b6909-142">String collection</span></span>|<span data-ttu-id="b6909-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="b6909-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="b6909-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b6909-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b6909-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="b6909-145">supportsScopeTags</span></span>|<span data-ttu-id="b6909-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="b6909-146">Boolean</span></span>|<span data-ttu-id="b6909-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b6909-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="b6909-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="b6909-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="b6909-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="b6909-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="b6909-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="b6909-150">This property is read-only.</span></span> <span data-ttu-id="b6909-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b6909-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b6909-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b6909-152">createdDateTime</span></span>|<span data-ttu-id="b6909-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b6909-153">DateTimeOffset</span></span>|<span data-ttu-id="b6909-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="b6909-154">DateTime the object was created.</span></span> <span data-ttu-id="b6909-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b6909-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b6909-156">descripción</span><span class="sxs-lookup"><span data-stu-id="b6909-156">description</span></span>|<span data-ttu-id="b6909-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="b6909-157">String</span></span>|<span data-ttu-id="b6909-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b6909-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="b6909-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b6909-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b6909-160">displayName</span><span class="sxs-lookup"><span data-stu-id="b6909-160">displayName</span></span>|<span data-ttu-id="b6909-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="b6909-161">String</span></span>|<span data-ttu-id="b6909-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b6909-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="b6909-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b6909-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b6909-164">version</span><span class="sxs-lookup"><span data-stu-id="b6909-164">version</span></span>|<span data-ttu-id="b6909-165">Int32</span><span class="sxs-lookup"><span data-stu-id="b6909-165">Int32</span></span>|<span data-ttu-id="b6909-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b6909-166">Version of the device configuration.</span></span> <span data-ttu-id="b6909-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b6909-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b6909-168">payloadName</span><span class="sxs-lookup"><span data-stu-id="b6909-168">payloadName</span></span>|<span data-ttu-id="b6909-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="b6909-169">String</span></span>|<span data-ttu-id="b6909-170">Nombre que se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="b6909-170">Name that is displayed to the user.</span></span>|
|<span data-ttu-id="b6909-171">payloadFileName</span><span class="sxs-lookup"><span data-stu-id="b6909-171">payloadFileName</span></span>|<span data-ttu-id="b6909-172">Cadena</span><span class="sxs-lookup"><span data-stu-id="b6909-172">String</span></span>|<span data-ttu-id="b6909-173">Nombre de archivo de carga útil (\*.mobileconfig</span><span class="sxs-lookup"><span data-stu-id="b6909-173">Payload file name (\*.mobileconfig</span></span> | <span data-ttu-id="b6909-174">\*.xml).</span><span class="sxs-lookup"><span data-stu-id="b6909-174">\*.xml).</span></span>|
|<span data-ttu-id="b6909-175">carga útil</span><span class="sxs-lookup"><span data-stu-id="b6909-175">payload</span></span>|<span data-ttu-id="b6909-176">Binario</span><span class="sxs-lookup"><span data-stu-id="b6909-176">Binary</span></span>|<span data-ttu-id="b6909-177">Carga útil.</span><span class="sxs-lookup"><span data-stu-id="b6909-177">Payload.</span></span> <span data-ttu-id="b6909-178">(Matriz de bytes codificada UTF8)</span><span class="sxs-lookup"><span data-stu-id="b6909-178">(UTF8 encoded byte array)</span></span>|



## <a name="response"></a><span data-ttu-id="b6909-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6909-179">Response</span></span>
<span data-ttu-id="b6909-180">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosCustomConfiguration](../resources/intune-deviceconfig-ioscustomconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6909-180">If successful, this method returns a `201 Created` response code and a [iosCustomConfiguration](../resources/intune-deviceconfig-ioscustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b6909-181">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6909-181">Example</span></span>
### <a name="request"></a><span data-ttu-id="b6909-182">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b6909-182">Request</span></span>
<span data-ttu-id="b6909-183">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6909-183">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 435

{
  "@odata.type": "#microsoft.graph.iosCustomConfiguration",
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

### <a name="response"></a><span data-ttu-id="b6909-184">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6909-184">Response</span></span>
<span data-ttu-id="b6909-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b6909-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 543

{
  "@odata.type": "#microsoft.graph.iosCustomConfiguration",
  "id": "f34428e3-28e3-f344-e328-44f3e32844f3",
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






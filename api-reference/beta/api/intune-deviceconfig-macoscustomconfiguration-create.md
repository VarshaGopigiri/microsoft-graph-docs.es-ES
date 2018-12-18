---
title: Crear macOSCustomConfiguration
description: Cree un objeto macOSCustomConfiguration.
author: tfitzmac
ms.openlocfilehash: 0169ba83335be2202ca3034df7205a407021d0c0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27340253"
---
# <a name="create-macoscustomconfiguration"></a><span data-ttu-id="29542-103">Crear macOSCustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="29542-103">Create macOSCustomConfiguration</span></span>

> <span data-ttu-id="29542-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="29542-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="29542-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="29542-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="29542-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="29542-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="29542-107">Cree un objeto [macOSCustomConfiguration](../resources/intune-deviceconfig-macoscustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="29542-107">Create a new [macOSCustomConfiguration](../resources/intune-deviceconfig-macoscustomconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="29542-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="29542-108">Prerequisites</span></span>
<span data-ttu-id="29542-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="29542-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="29542-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="29542-111">Permission type</span></span>|<span data-ttu-id="29542-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="29542-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="29542-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="29542-113">Delegated (work or school account)</span></span>|<span data-ttu-id="29542-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="29542-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="29542-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="29542-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="29542-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="29542-116">Not supported.</span></span>|
|<span data-ttu-id="29542-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="29542-117">Application</span></span>|<span data-ttu-id="29542-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="29542-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="29542-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="29542-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="29542-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="29542-120">Request headers</span></span>
|<span data-ttu-id="29542-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29542-121">Header</span></span>|<span data-ttu-id="29542-122">Valor</span><span class="sxs-lookup"><span data-stu-id="29542-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="29542-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="29542-123">Authorization</span></span>|<span data-ttu-id="29542-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="29542-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="29542-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="29542-125">Accept</span></span>|<span data-ttu-id="29542-126">application/json</span><span class="sxs-lookup"><span data-stu-id="29542-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="29542-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="29542-127">Request body</span></span>
<span data-ttu-id="29542-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto macOSCustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="29542-128">In the request body, supply a JSON representation for the macOSCustomConfiguration object.</span></span>

<span data-ttu-id="29542-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto macOSCustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="29542-129">The following table shows the properties that are required when you create the macOSCustomConfiguration.</span></span>

|<span data-ttu-id="29542-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="29542-130">Property</span></span>|<span data-ttu-id="29542-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="29542-131">Type</span></span>|<span data-ttu-id="29542-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="29542-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="29542-133">id</span><span class="sxs-lookup"><span data-stu-id="29542-133">id</span></span>|<span data-ttu-id="29542-134">String</span><span class="sxs-lookup"><span data-stu-id="29542-134">String</span></span>|<span data-ttu-id="29542-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="29542-135">Key of the entity.</span></span> <span data-ttu-id="29542-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="29542-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="29542-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="29542-137">lastModifiedDateTime</span></span>|<span data-ttu-id="29542-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="29542-138">DateTimeOffset</span></span>|<span data-ttu-id="29542-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="29542-139">DateTime the object was last modified.</span></span> <span data-ttu-id="29542-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="29542-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="29542-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="29542-141">roleScopeTagIds</span></span>|<span data-ttu-id="29542-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="29542-142">String collection</span></span>|<span data-ttu-id="29542-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="29542-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="29542-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="29542-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="29542-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="29542-145">supportsScopeTags</span></span>|<span data-ttu-id="29542-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="29542-146">Boolean</span></span>|<span data-ttu-id="29542-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="29542-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="29542-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="29542-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="29542-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="29542-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="29542-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="29542-150">This property is read-only.</span></span> <span data-ttu-id="29542-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="29542-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="29542-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="29542-152">createdDateTime</span></span>|<span data-ttu-id="29542-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="29542-153">DateTimeOffset</span></span>|<span data-ttu-id="29542-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="29542-154">DateTime the object was created.</span></span> <span data-ttu-id="29542-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="29542-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="29542-156">descripción</span><span class="sxs-lookup"><span data-stu-id="29542-156">description</span></span>|<span data-ttu-id="29542-157">String</span><span class="sxs-lookup"><span data-stu-id="29542-157">String</span></span>|<span data-ttu-id="29542-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29542-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="29542-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="29542-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="29542-160">displayName</span><span class="sxs-lookup"><span data-stu-id="29542-160">displayName</span></span>|<span data-ttu-id="29542-161">String</span><span class="sxs-lookup"><span data-stu-id="29542-161">String</span></span>|<span data-ttu-id="29542-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29542-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="29542-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="29542-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="29542-164">version</span><span class="sxs-lookup"><span data-stu-id="29542-164">version</span></span>|<span data-ttu-id="29542-165">Int32</span><span class="sxs-lookup"><span data-stu-id="29542-165">Int32</span></span>|<span data-ttu-id="29542-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29542-166">Version of the device configuration.</span></span> <span data-ttu-id="29542-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="29542-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="29542-168">payloadName</span><span class="sxs-lookup"><span data-stu-id="29542-168">payloadName</span></span>|<span data-ttu-id="29542-169">String</span><span class="sxs-lookup"><span data-stu-id="29542-169">String</span></span>|<span data-ttu-id="29542-170">Nombre que se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="29542-170">Name that is displayed to the user.</span></span>|
|<span data-ttu-id="29542-171">payloadFileName</span><span class="sxs-lookup"><span data-stu-id="29542-171">payloadFileName</span></span>|<span data-ttu-id="29542-172">String</span><span class="sxs-lookup"><span data-stu-id="29542-172">String</span></span>|<span data-ttu-id="29542-173">Nombre de archivo de carga útil (\*.mobileconfig</span><span class="sxs-lookup"><span data-stu-id="29542-173">Payload file name (\*.mobileconfig</span></span> | <span data-ttu-id="29542-174">\*.xml).</span><span class="sxs-lookup"><span data-stu-id="29542-174">\*.xml).</span></span>|
|<span data-ttu-id="29542-175">carga útil</span><span class="sxs-lookup"><span data-stu-id="29542-175">payload</span></span>|<span data-ttu-id="29542-176">Binario</span><span class="sxs-lookup"><span data-stu-id="29542-176">Binary</span></span>|<span data-ttu-id="29542-177">Carga útil.</span><span class="sxs-lookup"><span data-stu-id="29542-177">Payload.</span></span> <span data-ttu-id="29542-178">(Matriz de bytes codificada UTF8)</span><span class="sxs-lookup"><span data-stu-id="29542-178">(UTF8 encoded byte array)</span></span>|



## <a name="response"></a><span data-ttu-id="29542-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="29542-179">Response</span></span>
<span data-ttu-id="29542-180">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [macOSCustomConfiguration](../resources/intune-deviceconfig-macoscustomconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="29542-180">If successful, this method returns a `201 Created` response code and a [macOSCustomConfiguration](../resources/intune-deviceconfig-macoscustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="29542-181">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="29542-181">Example</span></span>
### <a name="request"></a><span data-ttu-id="29542-182">Solicitud</span><span class="sxs-lookup"><span data-stu-id="29542-182">Request</span></span>
<span data-ttu-id="29542-183">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="29542-183">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 437

{
  "@odata.type": "#microsoft.graph.macOSCustomConfiguration",
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

### <a name="response"></a><span data-ttu-id="29542-184">Respuesta</span><span class="sxs-lookup"><span data-stu-id="29542-184">Response</span></span>
<span data-ttu-id="29542-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="29542-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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






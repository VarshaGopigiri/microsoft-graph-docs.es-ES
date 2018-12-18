---
title: Crear androidCustomConfiguration
description: Cree un objeto androidCustomConfiguration.
author: tfitzmac
ms.openlocfilehash: 1395119e1602ad59a5be2d8f96b37b12bf6e6124
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27347827"
---
# <a name="create-androidcustomconfiguration"></a><span data-ttu-id="4f56b-103">Crear androidCustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f56b-103">Create androidCustomConfiguration</span></span>

> <span data-ttu-id="4f56b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4f56b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4f56b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4f56b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4f56b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4f56b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4f56b-107">Cree un objeto [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="4f56b-107">Create a new [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4f56b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4f56b-108">Prerequisites</span></span>
<span data-ttu-id="4f56b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4f56b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4f56b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4f56b-111">Permission type</span></span>|<span data-ttu-id="4f56b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4f56b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4f56b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4f56b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="4f56b-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4f56b-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="4f56b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4f56b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4f56b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4f56b-116">Not supported.</span></span>|
|<span data-ttu-id="4f56b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4f56b-117">Application</span></span>|<span data-ttu-id="4f56b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4f56b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4f56b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4f56b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="4f56b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4f56b-120">Request headers</span></span>
|<span data-ttu-id="4f56b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f56b-121">Header</span></span>|<span data-ttu-id="4f56b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4f56b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4f56b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="4f56b-123">Authorization</span></span>|<span data-ttu-id="4f56b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4f56b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4f56b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4f56b-125">Accept</span></span>|<span data-ttu-id="4f56b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="4f56b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4f56b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4f56b-127">Request body</span></span>
<span data-ttu-id="4f56b-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidCustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4f56b-128">In the request body, supply a JSON representation for the androidCustomConfiguration object.</span></span>

<span data-ttu-id="4f56b-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidCustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4f56b-129">The following table shows the properties that are required when you create the androidCustomConfiguration.</span></span>

|<span data-ttu-id="4f56b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4f56b-130">Property</span></span>|<span data-ttu-id="4f56b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="4f56b-131">Type</span></span>|<span data-ttu-id="4f56b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f56b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4f56b-133">id</span><span class="sxs-lookup"><span data-stu-id="4f56b-133">id</span></span>|<span data-ttu-id="4f56b-134">String</span><span class="sxs-lookup"><span data-stu-id="4f56b-134">String</span></span>|<span data-ttu-id="4f56b-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4f56b-135">Key of the entity.</span></span> <span data-ttu-id="4f56b-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4f56b-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4f56b-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="4f56b-137">lastModifiedDateTime</span></span>|<span data-ttu-id="4f56b-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4f56b-138">DateTimeOffset</span></span>|<span data-ttu-id="4f56b-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="4f56b-139">DateTime the object was last modified.</span></span> <span data-ttu-id="4f56b-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4f56b-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4f56b-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="4f56b-141">roleScopeTagIds</span></span>|<span data-ttu-id="4f56b-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="4f56b-142">String collection</span></span>|<span data-ttu-id="4f56b-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="4f56b-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="4f56b-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4f56b-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4f56b-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="4f56b-145">supportsScopeTags</span></span>|<span data-ttu-id="4f56b-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="4f56b-146">Boolean</span></span>|<span data-ttu-id="4f56b-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="4f56b-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="4f56b-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="4f56b-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="4f56b-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="4f56b-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="4f56b-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="4f56b-150">This property is read-only.</span></span> <span data-ttu-id="4f56b-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4f56b-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4f56b-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="4f56b-152">createdDateTime</span></span>|<span data-ttu-id="4f56b-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4f56b-153">DateTimeOffset</span></span>|<span data-ttu-id="4f56b-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="4f56b-154">DateTime the object was created.</span></span> <span data-ttu-id="4f56b-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4f56b-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4f56b-156">descripción</span><span class="sxs-lookup"><span data-stu-id="4f56b-156">description</span></span>|<span data-ttu-id="4f56b-157">String</span><span class="sxs-lookup"><span data-stu-id="4f56b-157">String</span></span>|<span data-ttu-id="4f56b-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f56b-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="4f56b-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4f56b-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4f56b-160">displayName</span><span class="sxs-lookup"><span data-stu-id="4f56b-160">displayName</span></span>|<span data-ttu-id="4f56b-161">String</span><span class="sxs-lookup"><span data-stu-id="4f56b-161">String</span></span>|<span data-ttu-id="4f56b-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f56b-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="4f56b-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4f56b-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4f56b-164">version</span><span class="sxs-lookup"><span data-stu-id="4f56b-164">version</span></span>|<span data-ttu-id="4f56b-165">Int32</span><span class="sxs-lookup"><span data-stu-id="4f56b-165">Int32</span></span>|<span data-ttu-id="4f56b-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f56b-166">Version of the device configuration.</span></span> <span data-ttu-id="4f56b-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4f56b-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4f56b-168">omaSettings</span><span class="sxs-lookup"><span data-stu-id="4f56b-168">omaSettings</span></span>|<span data-ttu-id="4f56b-169">Colección [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="4f56b-169">[omaSetting](../resources/intune-deviceconfig-omasetting.md) collection</span></span>|<span data-ttu-id="4f56b-170">Configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="4f56b-170">OMA settings.</span></span> <span data-ttu-id="4f56b-171">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="4f56b-171">This collection can contain a maximum of 1000 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="4f56b-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f56b-172">Response</span></span>
<span data-ttu-id="4f56b-173">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4f56b-173">If successful, this method returns a `201 Created` response code and a [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4f56b-174">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f56b-174">Example</span></span>
### <a name="request"></a><span data-ttu-id="4f56b-175">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4f56b-175">Request</span></span>
<span data-ttu-id="4f56b-176">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4f56b-176">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 558

{
  "@odata.type": "#microsoft.graph.androidCustomConfiguration",
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

### <a name="response"></a><span data-ttu-id="4f56b-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f56b-177">Response</span></span>
<span data-ttu-id="4f56b-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4f56b-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 666

{
  "@odata.type": "#microsoft.graph.androidCustomConfiguration",
  "id": "619b5e6d-5e6d-619b-6d5e-9b616d5e9b61",
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






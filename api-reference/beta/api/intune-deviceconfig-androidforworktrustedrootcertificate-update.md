---
title: Actualizar androidForWorkTrustedRootCertificate
description: Actualizar las propiedades de un objeto androidForWorkTrustedRootCertificate.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4f36e69d97caa3e334d95b2ecf1de427a80f2215
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968004"
---
# <a name="update-androidforworktrustedrootcertificate"></a><span data-ttu-id="0e8fb-103">Actualizar androidForWorkTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0e8fb-103">Update androidForWorkTrustedRootCertificate</span></span>

> <span data-ttu-id="0e8fb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0e8fb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0e8fb-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0e8fb-107">Actualizar las propiedades de un objeto [androidForWorkTrustedRootCertificate](../resources/intune-deviceconfig-androidforworktrustedrootcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="0e8fb-107">Update the properties of a [androidForWorkTrustedRootCertificate](../resources/intune-deviceconfig-androidforworktrustedrootcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0e8fb-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0e8fb-108">Prerequisites</span></span>
<span data-ttu-id="0e8fb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0e8fb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0e8fb-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0e8fb-111">Permission type</span></span>|<span data-ttu-id="0e8fb-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0e8fb-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0e8fb-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0e8fb-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0e8fb-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0e8fb-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="0e8fb-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0e8fb-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0e8fb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-116">Not supported.</span></span>|
|<span data-ttu-id="0e8fb-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0e8fb-117">Application</span></span>|<span data-ttu-id="0e8fb-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0e8fb-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0e8fb-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidForWorkEnterpriseWiFiConfiguration/rootCertificateForServerValidation
```

## <a name="request-headers"></a><span data-ttu-id="0e8fb-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0e8fb-120">Request headers</span></span>
|<span data-ttu-id="0e8fb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e8fb-121">Header</span></span>|<span data-ttu-id="0e8fb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0e8fb-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0e8fb-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="0e8fb-123">Authorization</span></span>|<span data-ttu-id="0e8fb-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0e8fb-125">Accept</span><span class="sxs-lookup"><span data-stu-id="0e8fb-125">Accept</span></span>|<span data-ttu-id="0e8fb-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0e8fb-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0e8fb-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0e8fb-127">Request body</span></span>
<span data-ttu-id="0e8fb-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidForWorkTrustedRootCertificate](../resources/intune-deviceconfig-androidforworktrustedrootcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="0e8fb-128">In the request body, supply a JSON representation for the [androidForWorkTrustedRootCertificate](../resources/intune-deviceconfig-androidforworktrustedrootcertificate.md) object.</span></span>

<span data-ttu-id="0e8fb-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidForWorkTrustedRootCertificate](../resources/intune-deviceconfig-androidforworktrustedrootcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="0e8fb-129">The following table shows the properties that are required when you create the [androidForWorkTrustedRootCertificate](../resources/intune-deviceconfig-androidforworktrustedrootcertificate.md).</span></span>

|<span data-ttu-id="0e8fb-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0e8fb-130">Property</span></span>|<span data-ttu-id="0e8fb-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e8fb-131">Type</span></span>|<span data-ttu-id="0e8fb-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e8fb-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0e8fb-133">id</span><span class="sxs-lookup"><span data-stu-id="0e8fb-133">id</span></span>|<span data-ttu-id="0e8fb-134">String</span><span class="sxs-lookup"><span data-stu-id="0e8fb-134">String</span></span>|<span data-ttu-id="0e8fb-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-135">Key of the entity.</span></span> <span data-ttu-id="0e8fb-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0e8fb-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0e8fb-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0e8fb-137">lastModifiedDateTime</span></span>|<span data-ttu-id="0e8fb-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0e8fb-138">DateTimeOffset</span></span>|<span data-ttu-id="0e8fb-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-139">DateTime the object was last modified.</span></span> <span data-ttu-id="0e8fb-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0e8fb-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0e8fb-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="0e8fb-141">roleScopeTagIds</span></span>|<span data-ttu-id="0e8fb-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="0e8fb-142">String collection</span></span>|<span data-ttu-id="0e8fb-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="0e8fb-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0e8fb-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0e8fb-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="0e8fb-145">supportsScopeTags</span></span>|<span data-ttu-id="0e8fb-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e8fb-146">Boolean</span></span>|<span data-ttu-id="0e8fb-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="0e8fb-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="0e8fb-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="0e8fb-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-150">This property is read-only.</span></span> <span data-ttu-id="0e8fb-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0e8fb-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0e8fb-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="0e8fb-152">createdDateTime</span></span>|<span data-ttu-id="0e8fb-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0e8fb-153">DateTimeOffset</span></span>|<span data-ttu-id="0e8fb-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-154">DateTime the object was created.</span></span> <span data-ttu-id="0e8fb-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0e8fb-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0e8fb-156">descripción</span><span class="sxs-lookup"><span data-stu-id="0e8fb-156">description</span></span>|<span data-ttu-id="0e8fb-157">String</span><span class="sxs-lookup"><span data-stu-id="0e8fb-157">String</span></span>|<span data-ttu-id="0e8fb-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="0e8fb-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0e8fb-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0e8fb-160">displayName</span><span class="sxs-lookup"><span data-stu-id="0e8fb-160">displayName</span></span>|<span data-ttu-id="0e8fb-161">String</span><span class="sxs-lookup"><span data-stu-id="0e8fb-161">String</span></span>|<span data-ttu-id="0e8fb-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="0e8fb-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0e8fb-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0e8fb-164">version</span><span class="sxs-lookup"><span data-stu-id="0e8fb-164">version</span></span>|<span data-ttu-id="0e8fb-165">Int32</span><span class="sxs-lookup"><span data-stu-id="0e8fb-165">Int32</span></span>|<span data-ttu-id="0e8fb-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-166">Version of the device configuration.</span></span> <span data-ttu-id="0e8fb-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0e8fb-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0e8fb-168">trustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0e8fb-168">trustedRootCertificate</span></span>|<span data-ttu-id="0e8fb-169">Binario</span><span class="sxs-lookup"><span data-stu-id="0e8fb-169">Binary</span></span>|<span data-ttu-id="0e8fb-170">Certificado raíz de confianza</span><span class="sxs-lookup"><span data-stu-id="0e8fb-170">Trusted Root Certificate</span></span>|
|<span data-ttu-id="0e8fb-171">certFileName</span><span class="sxs-lookup"><span data-stu-id="0e8fb-171">certFileName</span></span>|<span data-ttu-id="0e8fb-172">String</span><span class="sxs-lookup"><span data-stu-id="0e8fb-172">String</span></span>|<span data-ttu-id="0e8fb-173">Nombre de archivo para mostrar en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-173">File name to display in UI.</span></span>|



## <a name="response"></a><span data-ttu-id="0e8fb-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e8fb-174">Response</span></span>
<span data-ttu-id="0e8fb-175">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidForWorkTrustedRootCertificate](../resources/intune-deviceconfig-androidforworktrustedrootcertificate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-175">If successful, this method returns a `200 OK` response code and an updated [androidForWorkTrustedRootCertificate](../resources/intune-deviceconfig-androidforworktrustedrootcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0e8fb-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0e8fb-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="0e8fb-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0e8fb-177">Request</span></span>
<span data-ttu-id="0e8fb-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-178">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate
Content-type: application/json
Content-length: 363

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "trustedRootCertificate": "dHJ1c3RlZFJvb3RDZXJ0aWZpY2F0ZQ==",
  "certFileName": "Cert File Name value"
}
```

### <a name="response"></a><span data-ttu-id="0e8fb-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e8fb-179">Response</span></span>
<span data-ttu-id="0e8fb-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0e8fb-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 546

{
  "@odata.type": "#microsoft.graph.androidForWorkTrustedRootCertificate",
  "id": "2f78834c-834c-2f78-4c83-782f4c83782f",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "trustedRootCertificate": "dHJ1c3RlZFJvb3RDZXJ0aWZpY2F0ZQ==",
  "certFileName": "Cert File Name value"
}
```






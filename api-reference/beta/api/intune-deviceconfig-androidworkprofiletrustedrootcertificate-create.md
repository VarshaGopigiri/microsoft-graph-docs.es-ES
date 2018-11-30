---
title: Crear androidWorkProfileTrustedRootCertificate
description: Crear un nuevo objeto androidWorkProfileTrustedRootCertificate.
ms.openlocfilehash: c57000f207db40c268cc455ea9e668b3deabb9af
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086935"
---
# <a name="create-androidworkprofiletrustedrootcertificate"></a><span data-ttu-id="6b631-103">Crear androidWorkProfileTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6b631-103">Create androidWorkProfileTrustedRootCertificate</span></span>

> <span data-ttu-id="6b631-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6b631-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6b631-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6b631-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6b631-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6b631-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6b631-107">Crear un nuevo objeto [androidWorkProfileTrustedRootCertificate](../resources/intune-deviceconfig-androidworkprofiletrustedrootcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="6b631-107">Create a new [androidWorkProfileTrustedRootCertificate](../resources/intune-deviceconfig-androidworkprofiletrustedrootcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6b631-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6b631-108">Prerequisites</span></span>
<span data-ttu-id="6b631-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6b631-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6b631-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6b631-111">Permission type</span></span>|<span data-ttu-id="6b631-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6b631-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6b631-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6b631-113">Delegated (work or school account)</span></span>|<span data-ttu-id="6b631-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6b631-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="6b631-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6b631-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6b631-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6b631-116">Not supported.</span></span>|
|<span data-ttu-id="6b631-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6b631-117">Application</span></span>|<span data-ttu-id="6b631-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6b631-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6b631-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6b631-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="6b631-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6b631-120">Request headers</span></span>
|<span data-ttu-id="6b631-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b631-121">Header</span></span>|<span data-ttu-id="6b631-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6b631-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6b631-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6b631-123">Authorization</span></span>|<span data-ttu-id="6b631-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6b631-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6b631-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6b631-125">Accept</span></span>|<span data-ttu-id="6b631-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6b631-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6b631-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6b631-127">Request body</span></span>
<span data-ttu-id="6b631-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidWorkProfileTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="6b631-128">In the request body, supply a JSON representation for the androidWorkProfileTrustedRootCertificate object.</span></span>

<span data-ttu-id="6b631-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidWorkProfileTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="6b631-129">The following table shows the properties that are required when you create the androidWorkProfileTrustedRootCertificate.</span></span>

|<span data-ttu-id="6b631-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6b631-130">Property</span></span>|<span data-ttu-id="6b631-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6b631-131">Type</span></span>|<span data-ttu-id="6b631-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b631-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6b631-133">id</span><span class="sxs-lookup"><span data-stu-id="6b631-133">id</span></span>|<span data-ttu-id="6b631-134">String</span><span class="sxs-lookup"><span data-stu-id="6b631-134">String</span></span>|<span data-ttu-id="6b631-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6b631-135">Key of the entity.</span></span> <span data-ttu-id="6b631-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6b631-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6b631-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="6b631-137">lastModifiedDateTime</span></span>|<span data-ttu-id="6b631-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6b631-138">DateTimeOffset</span></span>|<span data-ttu-id="6b631-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="6b631-139">DateTime the object was last modified.</span></span> <span data-ttu-id="6b631-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6b631-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6b631-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="6b631-141">roleScopeTagIds</span></span>|<span data-ttu-id="6b631-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="6b631-142">String collection</span></span>|<span data-ttu-id="6b631-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="6b631-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="6b631-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6b631-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6b631-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="6b631-145">supportsScopeTags</span></span>|<span data-ttu-id="6b631-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="6b631-146">Boolean</span></span>|<span data-ttu-id="6b631-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="6b631-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="6b631-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="6b631-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="6b631-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="6b631-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="6b631-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="6b631-150">This property is read-only.</span></span> <span data-ttu-id="6b631-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6b631-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6b631-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="6b631-152">createdDateTime</span></span>|<span data-ttu-id="6b631-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6b631-153">DateTimeOffset</span></span>|<span data-ttu-id="6b631-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="6b631-154">DateTime the object was created.</span></span> <span data-ttu-id="6b631-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6b631-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6b631-156">descripción</span><span class="sxs-lookup"><span data-stu-id="6b631-156">description</span></span>|<span data-ttu-id="6b631-157">String</span><span class="sxs-lookup"><span data-stu-id="6b631-157">String</span></span>|<span data-ttu-id="6b631-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b631-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="6b631-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6b631-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6b631-160">displayName</span><span class="sxs-lookup"><span data-stu-id="6b631-160">displayName</span></span>|<span data-ttu-id="6b631-161">String</span><span class="sxs-lookup"><span data-stu-id="6b631-161">String</span></span>|<span data-ttu-id="6b631-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b631-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="6b631-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6b631-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6b631-164">version</span><span class="sxs-lookup"><span data-stu-id="6b631-164">version</span></span>|<span data-ttu-id="6b631-165">Int32</span><span class="sxs-lookup"><span data-stu-id="6b631-165">Int32</span></span>|<span data-ttu-id="6b631-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b631-166">Version of the device configuration.</span></span> <span data-ttu-id="6b631-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6b631-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6b631-168">trustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6b631-168">trustedRootCertificate</span></span>|<span data-ttu-id="6b631-169">Binario</span><span class="sxs-lookup"><span data-stu-id="6b631-169">Binary</span></span>|<span data-ttu-id="6b631-170">Certificado raíz de confianza</span><span class="sxs-lookup"><span data-stu-id="6b631-170">Trusted Root Certificate</span></span>|
|<span data-ttu-id="6b631-171">certFileName</span><span class="sxs-lookup"><span data-stu-id="6b631-171">certFileName</span></span>|<span data-ttu-id="6b631-172">String</span><span class="sxs-lookup"><span data-stu-id="6b631-172">String</span></span>|<span data-ttu-id="6b631-173">Nombre de archivo para mostrar en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="6b631-173">File name to display in UI.</span></span>|



## <a name="response"></a><span data-ttu-id="6b631-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6b631-174">Response</span></span>
<span data-ttu-id="6b631-175">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidWorkProfileTrustedRootCertificate](../resources/intune-deviceconfig-androidworkprofiletrustedrootcertificate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6b631-175">If successful, this method returns a `201 Created` response code and a [androidWorkProfileTrustedRootCertificate](../resources/intune-deviceconfig-androidworkprofiletrustedrootcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6b631-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6b631-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="6b631-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6b631-177">Request</span></span>
<span data-ttu-id="6b631-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6b631-178">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 442

{
  "@odata.type": "#microsoft.graph.androidWorkProfileTrustedRootCertificate",
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

### <a name="response"></a><span data-ttu-id="6b631-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6b631-179">Response</span></span>
<span data-ttu-id="6b631-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6b631-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 550

{
  "@odata.type": "#microsoft.graph.androidWorkProfileTrustedRootCertificate",
  "id": "37cc7454-7454-37cc-5474-cc375474cc37",
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






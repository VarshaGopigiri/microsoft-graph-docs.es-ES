---
title: Actualizar windows81TrustedRootCertificate
description: Actualizar las propiedades de un objeto windows81TrustedRootCertificate.
author: tfitzmac
ms.openlocfilehash: ce95eda15d57a4e44b5c3c4756205638e2eb9cbb
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27307431"
---
# <a name="update-windows81trustedrootcertificate"></a><span data-ttu-id="51b05-103">Actualizar windows81TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="51b05-103">Update windows81TrustedRootCertificate</span></span>

> <span data-ttu-id="51b05-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="51b05-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="51b05-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="51b05-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="51b05-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="51b05-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="51b05-107">Actualizar las propiedades de un objeto [windows81TrustedRootCertificate](../resources/intune-deviceconfig-windows81trustedrootcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="51b05-107">Update the properties of a [windows81TrustedRootCertificate](../resources/intune-deviceconfig-windows81trustedrootcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="51b05-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="51b05-108">Prerequisites</span></span>
<span data-ttu-id="51b05-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="51b05-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="51b05-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="51b05-111">Permission type</span></span>|<span data-ttu-id="51b05-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="51b05-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="51b05-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="51b05-113">Delegated (work or school account)</span></span>|<span data-ttu-id="51b05-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="51b05-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="51b05-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="51b05-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="51b05-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51b05-116">Not supported.</span></span>|
|<span data-ttu-id="51b05-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="51b05-117">Application</span></span>|<span data-ttu-id="51b05-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51b05-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="51b05-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="51b05-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windows81SCEPCertificateProfile/rootCertificate
```

## <a name="request-headers"></a><span data-ttu-id="51b05-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="51b05-120">Request headers</span></span>
|<span data-ttu-id="51b05-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51b05-121">Header</span></span>|<span data-ttu-id="51b05-122">Valor</span><span class="sxs-lookup"><span data-stu-id="51b05-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="51b05-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="51b05-123">Authorization</span></span>|<span data-ttu-id="51b05-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="51b05-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="51b05-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="51b05-125">Accept</span></span>|<span data-ttu-id="51b05-126">application/json</span><span class="sxs-lookup"><span data-stu-id="51b05-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="51b05-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="51b05-127">Request body</span></span>
<span data-ttu-id="51b05-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windows81TrustedRootCertificate](../resources/intune-deviceconfig-windows81trustedrootcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="51b05-128">In the request body, supply a JSON representation for the [windows81TrustedRootCertificate](../resources/intune-deviceconfig-windows81trustedrootcertificate.md) object.</span></span>

<span data-ttu-id="51b05-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windows81TrustedRootCertificate](../resources/intune-deviceconfig-windows81trustedrootcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="51b05-129">The following table shows the properties that are required when you create the [windows81TrustedRootCertificate](../resources/intune-deviceconfig-windows81trustedrootcertificate.md).</span></span>

|<span data-ttu-id="51b05-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="51b05-130">Property</span></span>|<span data-ttu-id="51b05-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="51b05-131">Type</span></span>|<span data-ttu-id="51b05-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="51b05-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="51b05-133">id</span><span class="sxs-lookup"><span data-stu-id="51b05-133">id</span></span>|<span data-ttu-id="51b05-134">String</span><span class="sxs-lookup"><span data-stu-id="51b05-134">String</span></span>|<span data-ttu-id="51b05-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="51b05-135">Key of the entity.</span></span> <span data-ttu-id="51b05-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="51b05-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="51b05-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="51b05-137">lastModifiedDateTime</span></span>|<span data-ttu-id="51b05-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="51b05-138">DateTimeOffset</span></span>|<span data-ttu-id="51b05-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="51b05-139">DateTime the object was last modified.</span></span> <span data-ttu-id="51b05-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="51b05-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="51b05-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="51b05-141">roleScopeTagIds</span></span>|<span data-ttu-id="51b05-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="51b05-142">String collection</span></span>|<span data-ttu-id="51b05-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="51b05-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="51b05-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="51b05-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="51b05-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="51b05-145">supportsScopeTags</span></span>|<span data-ttu-id="51b05-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="51b05-146">Boolean</span></span>|<span data-ttu-id="51b05-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="51b05-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="51b05-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="51b05-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="51b05-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="51b05-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="51b05-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="51b05-150">This property is read-only.</span></span> <span data-ttu-id="51b05-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="51b05-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="51b05-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="51b05-152">createdDateTime</span></span>|<span data-ttu-id="51b05-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="51b05-153">DateTimeOffset</span></span>|<span data-ttu-id="51b05-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="51b05-154">DateTime the object was created.</span></span> <span data-ttu-id="51b05-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="51b05-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="51b05-156">descripción</span><span class="sxs-lookup"><span data-stu-id="51b05-156">description</span></span>|<span data-ttu-id="51b05-157">String</span><span class="sxs-lookup"><span data-stu-id="51b05-157">String</span></span>|<span data-ttu-id="51b05-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51b05-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="51b05-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="51b05-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="51b05-160">displayName</span><span class="sxs-lookup"><span data-stu-id="51b05-160">displayName</span></span>|<span data-ttu-id="51b05-161">String</span><span class="sxs-lookup"><span data-stu-id="51b05-161">String</span></span>|<span data-ttu-id="51b05-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51b05-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="51b05-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="51b05-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="51b05-164">version</span><span class="sxs-lookup"><span data-stu-id="51b05-164">version</span></span>|<span data-ttu-id="51b05-165">Int32</span><span class="sxs-lookup"><span data-stu-id="51b05-165">Int32</span></span>|<span data-ttu-id="51b05-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51b05-166">Version of the device configuration.</span></span> <span data-ttu-id="51b05-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="51b05-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="51b05-168">trustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="51b05-168">trustedRootCertificate</span></span>|<span data-ttu-id="51b05-169">Binario</span><span class="sxs-lookup"><span data-stu-id="51b05-169">Binary</span></span>|<span data-ttu-id="51b05-170">Certificado raíz de confianza</span><span class="sxs-lookup"><span data-stu-id="51b05-170">Trusted Root Certificate</span></span>|
|<span data-ttu-id="51b05-171">certFileName</span><span class="sxs-lookup"><span data-stu-id="51b05-171">certFileName</span></span>|<span data-ttu-id="51b05-172">String</span><span class="sxs-lookup"><span data-stu-id="51b05-172">String</span></span>|<span data-ttu-id="51b05-173">Nombre de archivo para mostrar en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="51b05-173">File name to display in UI.</span></span>|
|<span data-ttu-id="51b05-174">destinationStore</span><span class="sxs-lookup"><span data-stu-id="51b05-174">destinationStore</span></span>|[<span data-ttu-id="51b05-175">certificateDestinationStore</span><span class="sxs-lookup"><span data-stu-id="51b05-175">certificateDestinationStore</span></span>](../resources/intune-deviceconfig-certificatedestinationstore.md)|<span data-ttu-id="51b05-176">Ubicación del almacén de destino para el certificado raíz de confianza.</span><span class="sxs-lookup"><span data-stu-id="51b05-176">Destination store location for the Trusted Root Certificate.</span></span> <span data-ttu-id="51b05-177">Los valores posibles son: `computerCertStoreRoot`, `computerCertStoreIntermediate` y `userCertStoreIntermediate`.</span><span class="sxs-lookup"><span data-stu-id="51b05-177">Possible values are: `computerCertStoreRoot`, `computerCertStoreIntermediate`, `userCertStoreIntermediate`.</span></span>|



## <a name="response"></a><span data-ttu-id="51b05-178">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51b05-178">Response</span></span>
<span data-ttu-id="51b05-179">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windows81TrustedRootCertificate](../resources/intune-deviceconfig-windows81trustedrootcertificate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="51b05-179">If successful, this method returns a `200 OK` response code and an updated [windows81TrustedRootCertificate](../resources/intune-deviceconfig-windows81trustedrootcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="51b05-180">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="51b05-180">Example</span></span>
### <a name="request"></a><span data-ttu-id="51b05-181">Solicitud</span><span class="sxs-lookup"><span data-stu-id="51b05-181">Request</span></span>
<span data-ttu-id="51b05-182">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="51b05-182">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}
Content-type: application/json
Content-length: 419

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
  "certFileName": "Cert File Name value",
  "destinationStore": "computerCertStoreIntermediate"
}
```

### <a name="response"></a><span data-ttu-id="51b05-183">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51b05-183">Response</span></span>
<span data-ttu-id="51b05-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="51b05-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 597

{
  "@odata.type": "#microsoft.graph.windows81TrustedRootCertificate",
  "id": "3fb588f9-88f9-3fb5-f988-b53ff988b53f",
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
  "certFileName": "Cert File Name value",
  "destinationStore": "computerCertStoreIntermediate"
}
```






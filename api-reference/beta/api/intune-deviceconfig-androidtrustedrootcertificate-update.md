---
title: Actualizar androidTrustedRootCertificate
description: Actualizar las propiedades de un objeto androidTrustedRootCertificate.
ms.openlocfilehash: 26e88ff939778ce6e3fec5f67282a51bba70d654
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085814"
---
# <a name="update-androidtrustedrootcertificate"></a><span data-ttu-id="b1e00-103">Actualizar androidTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b1e00-103">Update androidTrustedRootCertificate</span></span>

> <span data-ttu-id="b1e00-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b1e00-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b1e00-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b1e00-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b1e00-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b1e00-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b1e00-107">Actualizar las propiedades de un objeto [androidTrustedRootCertificate](../resources/intune-deviceconfig-androidtrustedrootcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="b1e00-107">Update the properties of a [androidTrustedRootCertificate](../resources/intune-deviceconfig-androidtrustedrootcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b1e00-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b1e00-108">Prerequisites</span></span>
<span data-ttu-id="b1e00-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b1e00-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b1e00-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b1e00-111">Permission type</span></span>|<span data-ttu-id="b1e00-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b1e00-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b1e00-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b1e00-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b1e00-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b1e00-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="b1e00-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b1e00-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b1e00-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b1e00-116">Not supported.</span></span>|
|<span data-ttu-id="b1e00-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b1e00-117">Application</span></span>|<span data-ttu-id="b1e00-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b1e00-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b1e00-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b1e00-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidCertificateProfileBase/rootCertificate
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidEnterpriseWiFiConfiguration/rootCertificateForServerValidation
```

## <a name="request-headers"></a><span data-ttu-id="b1e00-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b1e00-120">Request headers</span></span>
|<span data-ttu-id="b1e00-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1e00-121">Header</span></span>|<span data-ttu-id="b1e00-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b1e00-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b1e00-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="b1e00-123">Authorization</span></span>|<span data-ttu-id="b1e00-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b1e00-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b1e00-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b1e00-125">Accept</span></span>|<span data-ttu-id="b1e00-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b1e00-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b1e00-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b1e00-127">Request body</span></span>
<span data-ttu-id="b1e00-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidTrustedRootCertificate](../resources/intune-deviceconfig-androidtrustedrootcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="b1e00-128">In the request body, supply a JSON representation for the [androidTrustedRootCertificate](../resources/intune-deviceconfig-androidtrustedrootcertificate.md) object.</span></span>

<span data-ttu-id="b1e00-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidTrustedRootCertificate](../resources/intune-deviceconfig-androidtrustedrootcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="b1e00-129">The following table shows the properties that are required when you create the [androidTrustedRootCertificate](../resources/intune-deviceconfig-androidtrustedrootcertificate.md).</span></span>

|<span data-ttu-id="b1e00-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b1e00-130">Property</span></span>|<span data-ttu-id="b1e00-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1e00-131">Type</span></span>|<span data-ttu-id="b1e00-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1e00-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b1e00-133">id</span><span class="sxs-lookup"><span data-stu-id="b1e00-133">id</span></span>|<span data-ttu-id="b1e00-134">String</span><span class="sxs-lookup"><span data-stu-id="b1e00-134">String</span></span>|<span data-ttu-id="b1e00-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b1e00-135">Key of the entity.</span></span> <span data-ttu-id="b1e00-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b1e00-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b1e00-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b1e00-137">lastModifiedDateTime</span></span>|<span data-ttu-id="b1e00-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b1e00-138">DateTimeOffset</span></span>|<span data-ttu-id="b1e00-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="b1e00-139">DateTime the object was last modified.</span></span> <span data-ttu-id="b1e00-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b1e00-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b1e00-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="b1e00-141">roleScopeTagIds</span></span>|<span data-ttu-id="b1e00-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="b1e00-142">String collection</span></span>|<span data-ttu-id="b1e00-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="b1e00-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="b1e00-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b1e00-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b1e00-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="b1e00-145">supportsScopeTags</span></span>|<span data-ttu-id="b1e00-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="b1e00-146">Boolean</span></span>|<span data-ttu-id="b1e00-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b1e00-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="b1e00-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="b1e00-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="b1e00-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="b1e00-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="b1e00-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="b1e00-150">This property is read-only.</span></span> <span data-ttu-id="b1e00-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b1e00-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b1e00-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b1e00-152">createdDateTime</span></span>|<span data-ttu-id="b1e00-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b1e00-153">DateTimeOffset</span></span>|<span data-ttu-id="b1e00-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="b1e00-154">DateTime the object was created.</span></span> <span data-ttu-id="b1e00-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b1e00-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b1e00-156">descripción</span><span class="sxs-lookup"><span data-stu-id="b1e00-156">description</span></span>|<span data-ttu-id="b1e00-157">String</span><span class="sxs-lookup"><span data-stu-id="b1e00-157">String</span></span>|<span data-ttu-id="b1e00-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1e00-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="b1e00-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b1e00-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b1e00-160">displayName</span><span class="sxs-lookup"><span data-stu-id="b1e00-160">displayName</span></span>|<span data-ttu-id="b1e00-161">String</span><span class="sxs-lookup"><span data-stu-id="b1e00-161">String</span></span>|<span data-ttu-id="b1e00-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1e00-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="b1e00-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b1e00-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b1e00-164">version</span><span class="sxs-lookup"><span data-stu-id="b1e00-164">version</span></span>|<span data-ttu-id="b1e00-165">Int32</span><span class="sxs-lookup"><span data-stu-id="b1e00-165">Int32</span></span>|<span data-ttu-id="b1e00-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1e00-166">Version of the device configuration.</span></span> <span data-ttu-id="b1e00-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b1e00-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b1e00-168">trustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b1e00-168">trustedRootCertificate</span></span>|<span data-ttu-id="b1e00-169">Binario</span><span class="sxs-lookup"><span data-stu-id="b1e00-169">Binary</span></span>|<span data-ttu-id="b1e00-170">Certificado raíz de confianza</span><span class="sxs-lookup"><span data-stu-id="b1e00-170">Trusted Root Certificate</span></span>|
|<span data-ttu-id="b1e00-171">certFileName</span><span class="sxs-lookup"><span data-stu-id="b1e00-171">certFileName</span></span>|<span data-ttu-id="b1e00-172">String</span><span class="sxs-lookup"><span data-stu-id="b1e00-172">String</span></span>|<span data-ttu-id="b1e00-173">Nombre de archivo para mostrar en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="b1e00-173">File name to display in UI.</span></span>|



## <a name="response"></a><span data-ttu-id="b1e00-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b1e00-174">Response</span></span>
<span data-ttu-id="b1e00-175">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidTrustedRootCertificate](../resources/intune-deviceconfig-androidtrustedrootcertificate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b1e00-175">If successful, this method returns a `200 OK` response code and an updated [androidTrustedRootCertificate](../resources/intune-deviceconfig-androidtrustedrootcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b1e00-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b1e00-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="b1e00-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b1e00-177">Request</span></span>
<span data-ttu-id="b1e00-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b1e00-178">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate
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

### <a name="response"></a><span data-ttu-id="b1e00-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b1e00-179">Response</span></span>
<span data-ttu-id="b1e00-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b1e00-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 539

{
  "@odata.type": "#microsoft.graph.androidTrustedRootCertificate",
  "id": "7f8d751e-751e-7f8d-1e75-8d7f1e758d7f",
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






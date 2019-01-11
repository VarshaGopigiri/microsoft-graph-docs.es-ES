---
title: Actualizar iosTrustedRootCertificate
description: Actualizar las propiedades de un objeto iosTrustedRootCertificate.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 74023665c8690373a6804cb586fe639b45491ed8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27806807"
---
# <a name="update-iostrustedrootcertificate"></a><span data-ttu-id="8a788-103">Actualizar iosTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8a788-103">Update iosTrustedRootCertificate</span></span>

> <span data-ttu-id="8a788-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8a788-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8a788-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8a788-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8a788-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8a788-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8a788-107">Actualizar las propiedades de un objeto [iosTrustedRootCertificate](../resources/intune-deviceconfig-iostrustedrootcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="8a788-107">Update the properties of a [iosTrustedRootCertificate](../resources/intune-deviceconfig-iostrustedrootcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8a788-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8a788-108">Prerequisites</span></span>
<span data-ttu-id="8a788-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8a788-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8a788-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8a788-111">Permission type</span></span>|<span data-ttu-id="8a788-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8a788-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8a788-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8a788-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8a788-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8a788-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="8a788-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8a788-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8a788-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8a788-116">Not supported.</span></span>|
|<span data-ttu-id="8a788-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8a788-117">Application</span></span>|<span data-ttu-id="8a788-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8a788-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8a788-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8a788-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/rootCertificate
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosEnterpriseWiFiConfiguration/rootCertificatesForServerValidation/{iosTrustedRootCertificateId}
```

## <a name="request-headers"></a><span data-ttu-id="8a788-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8a788-120">Request headers</span></span>
|<span data-ttu-id="8a788-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a788-121">Header</span></span>|<span data-ttu-id="8a788-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8a788-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8a788-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="8a788-123">Authorization</span></span>|<span data-ttu-id="8a788-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8a788-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8a788-125">Accept</span><span class="sxs-lookup"><span data-stu-id="8a788-125">Accept</span></span>|<span data-ttu-id="8a788-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8a788-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8a788-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8a788-127">Request body</span></span>
<span data-ttu-id="8a788-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [iosTrustedRootCertificate](../resources/intune-deviceconfig-iostrustedrootcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="8a788-128">In the request body, supply a JSON representation for the [iosTrustedRootCertificate](../resources/intune-deviceconfig-iostrustedrootcertificate.md) object.</span></span>

<span data-ttu-id="8a788-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [iosTrustedRootCertificate](../resources/intune-deviceconfig-iostrustedrootcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="8a788-129">The following table shows the properties that are required when you create the [iosTrustedRootCertificate](../resources/intune-deviceconfig-iostrustedrootcertificate.md).</span></span>

|<span data-ttu-id="8a788-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8a788-130">Property</span></span>|<span data-ttu-id="8a788-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a788-131">Type</span></span>|<span data-ttu-id="8a788-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a788-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8a788-133">id</span><span class="sxs-lookup"><span data-stu-id="8a788-133">id</span></span>|<span data-ttu-id="8a788-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a788-134">String</span></span>|<span data-ttu-id="8a788-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8a788-135">Key of the entity.</span></span> <span data-ttu-id="8a788-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8a788-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8a788-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8a788-137">lastModifiedDateTime</span></span>|<span data-ttu-id="8a788-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8a788-138">DateTimeOffset</span></span>|<span data-ttu-id="8a788-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="8a788-139">DateTime the object was last modified.</span></span> <span data-ttu-id="8a788-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8a788-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8a788-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="8a788-141">roleScopeTagIds</span></span>|<span data-ttu-id="8a788-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="8a788-142">String collection</span></span>|<span data-ttu-id="8a788-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="8a788-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="8a788-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8a788-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8a788-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="8a788-145">supportsScopeTags</span></span>|<span data-ttu-id="8a788-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="8a788-146">Boolean</span></span>|<span data-ttu-id="8a788-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8a788-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="8a788-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="8a788-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="8a788-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="8a788-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="8a788-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="8a788-150">This property is read-only.</span></span> <span data-ttu-id="8a788-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8a788-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8a788-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8a788-152">createdDateTime</span></span>|<span data-ttu-id="8a788-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8a788-153">DateTimeOffset</span></span>|<span data-ttu-id="8a788-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="8a788-154">DateTime the object was created.</span></span> <span data-ttu-id="8a788-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8a788-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8a788-156">descripción</span><span class="sxs-lookup"><span data-stu-id="8a788-156">description</span></span>|<span data-ttu-id="8a788-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a788-157">String</span></span>|<span data-ttu-id="8a788-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a788-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="8a788-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8a788-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8a788-160">displayName</span><span class="sxs-lookup"><span data-stu-id="8a788-160">displayName</span></span>|<span data-ttu-id="8a788-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a788-161">String</span></span>|<span data-ttu-id="8a788-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a788-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="8a788-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8a788-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8a788-164">version</span><span class="sxs-lookup"><span data-stu-id="8a788-164">version</span></span>|<span data-ttu-id="8a788-165">Int32</span><span class="sxs-lookup"><span data-stu-id="8a788-165">Int32</span></span>|<span data-ttu-id="8a788-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a788-166">Version of the device configuration.</span></span> <span data-ttu-id="8a788-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8a788-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8a788-168">trustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8a788-168">trustedRootCertificate</span></span>|<span data-ttu-id="8a788-169">Binario</span><span class="sxs-lookup"><span data-stu-id="8a788-169">Binary</span></span>|<span data-ttu-id="8a788-170">Certificado raíz de confianza.</span><span class="sxs-lookup"><span data-stu-id="8a788-170">Trusted Root Certificate.</span></span>|
|<span data-ttu-id="8a788-171">certFileName</span><span class="sxs-lookup"><span data-stu-id="8a788-171">certFileName</span></span>|<span data-ttu-id="8a788-172">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a788-172">String</span></span>|<span data-ttu-id="8a788-173">Nombre de archivo para mostrar en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="8a788-173">File name to display in UI.</span></span>|



## <a name="response"></a><span data-ttu-id="8a788-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a788-174">Response</span></span>
<span data-ttu-id="8a788-175">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [iosTrustedRootCertificate](../resources/intune-deviceconfig-iostrustedrootcertificate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a788-175">If successful, this method returns a `200 OK` response code and an updated [iosTrustedRootCertificate](../resources/intune-deviceconfig-iostrustedrootcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8a788-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a788-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="8a788-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8a788-177">Request</span></span>
<span data-ttu-id="8a788-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8a788-178">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/rootCertificate
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

### <a name="response"></a><span data-ttu-id="8a788-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a788-179">Response</span></span>
<span data-ttu-id="8a788-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8a788-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 535

{
  "@odata.type": "#microsoft.graph.iosTrustedRootCertificate",
  "id": "9bc72bb8-2bb8-9bc7-b82b-c79bb82bc79b",
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






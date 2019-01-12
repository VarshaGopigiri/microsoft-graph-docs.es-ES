---
title: Crear androidTrustedRootCertificate
description: Crear un nuevo objeto androidTrustedRootCertificate.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 13b25f3dbe300820107f05c2787c79a8817a67fb
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27929098"
---
# <a name="create-androidtrustedrootcertificate"></a><span data-ttu-id="11baf-103">Crear androidTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="11baf-103">Create androidTrustedRootCertificate</span></span>

> <span data-ttu-id="11baf-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="11baf-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="11baf-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="11baf-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="11baf-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="11baf-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="11baf-107">Crear un nuevo objeto [androidTrustedRootCertificate](../resources/intune-deviceconfig-androidtrustedrootcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="11baf-107">Create a new [androidTrustedRootCertificate](../resources/intune-deviceconfig-androidtrustedrootcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="11baf-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="11baf-108">Prerequisites</span></span>
<span data-ttu-id="11baf-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="11baf-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="11baf-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="11baf-111">Permission type</span></span>|<span data-ttu-id="11baf-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="11baf-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="11baf-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="11baf-113">Delegated (work or school account)</span></span>|<span data-ttu-id="11baf-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="11baf-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="11baf-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="11baf-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="11baf-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="11baf-116">Not supported.</span></span>|
|<span data-ttu-id="11baf-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="11baf-117">Application</span></span>|<span data-ttu-id="11baf-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="11baf-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="11baf-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="11baf-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="11baf-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="11baf-120">Request headers</span></span>
|<span data-ttu-id="11baf-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11baf-121">Header</span></span>|<span data-ttu-id="11baf-122">Valor</span><span class="sxs-lookup"><span data-stu-id="11baf-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="11baf-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="11baf-123">Authorization</span></span>|<span data-ttu-id="11baf-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="11baf-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="11baf-125">Accept</span><span class="sxs-lookup"><span data-stu-id="11baf-125">Accept</span></span>|<span data-ttu-id="11baf-126">application/json</span><span class="sxs-lookup"><span data-stu-id="11baf-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="11baf-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="11baf-127">Request body</span></span>
<span data-ttu-id="11baf-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="11baf-128">In the request body, supply a JSON representation for the androidTrustedRootCertificate object.</span></span>

<span data-ttu-id="11baf-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="11baf-129">The following table shows the properties that are required when you create the androidTrustedRootCertificate.</span></span>

|<span data-ttu-id="11baf-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11baf-130">Property</span></span>|<span data-ttu-id="11baf-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="11baf-131">Type</span></span>|<span data-ttu-id="11baf-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="11baf-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="11baf-133">id</span><span class="sxs-lookup"><span data-stu-id="11baf-133">id</span></span>|<span data-ttu-id="11baf-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="11baf-134">String</span></span>|<span data-ttu-id="11baf-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="11baf-135">Key of the entity.</span></span> <span data-ttu-id="11baf-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="11baf-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="11baf-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="11baf-137">lastModifiedDateTime</span></span>|<span data-ttu-id="11baf-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="11baf-138">DateTimeOffset</span></span>|<span data-ttu-id="11baf-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="11baf-139">DateTime the object was last modified.</span></span> <span data-ttu-id="11baf-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="11baf-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="11baf-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="11baf-141">roleScopeTagIds</span></span>|<span data-ttu-id="11baf-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="11baf-142">String collection</span></span>|<span data-ttu-id="11baf-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="11baf-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="11baf-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="11baf-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="11baf-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="11baf-145">supportsScopeTags</span></span>|<span data-ttu-id="11baf-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="11baf-146">Boolean</span></span>|<span data-ttu-id="11baf-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="11baf-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="11baf-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="11baf-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="11baf-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="11baf-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="11baf-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="11baf-150">This property is read-only.</span></span> <span data-ttu-id="11baf-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="11baf-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="11baf-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="11baf-152">createdDateTime</span></span>|<span data-ttu-id="11baf-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="11baf-153">DateTimeOffset</span></span>|<span data-ttu-id="11baf-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="11baf-154">DateTime the object was created.</span></span> <span data-ttu-id="11baf-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="11baf-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="11baf-156">descripción</span><span class="sxs-lookup"><span data-stu-id="11baf-156">description</span></span>|<span data-ttu-id="11baf-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="11baf-157">String</span></span>|<span data-ttu-id="11baf-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11baf-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="11baf-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="11baf-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="11baf-160">displayName</span><span class="sxs-lookup"><span data-stu-id="11baf-160">displayName</span></span>|<span data-ttu-id="11baf-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="11baf-161">String</span></span>|<span data-ttu-id="11baf-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11baf-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="11baf-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="11baf-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="11baf-164">version</span><span class="sxs-lookup"><span data-stu-id="11baf-164">version</span></span>|<span data-ttu-id="11baf-165">Int32</span><span class="sxs-lookup"><span data-stu-id="11baf-165">Int32</span></span>|<span data-ttu-id="11baf-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11baf-166">Version of the device configuration.</span></span> <span data-ttu-id="11baf-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="11baf-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="11baf-168">trustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="11baf-168">trustedRootCertificate</span></span>|<span data-ttu-id="11baf-169">Binario</span><span class="sxs-lookup"><span data-stu-id="11baf-169">Binary</span></span>|<span data-ttu-id="11baf-170">Certificado raíz de confianza</span><span class="sxs-lookup"><span data-stu-id="11baf-170">Trusted Root Certificate</span></span>|
|<span data-ttu-id="11baf-171">certFileName</span><span class="sxs-lookup"><span data-stu-id="11baf-171">certFileName</span></span>|<span data-ttu-id="11baf-172">Cadena</span><span class="sxs-lookup"><span data-stu-id="11baf-172">String</span></span>|<span data-ttu-id="11baf-173">Nombre de archivo para mostrar en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="11baf-173">File name to display in UI.</span></span>|



## <a name="response"></a><span data-ttu-id="11baf-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11baf-174">Response</span></span>
<span data-ttu-id="11baf-175">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidTrustedRootCertificate](../resources/intune-deviceconfig-androidtrustedrootcertificate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="11baf-175">If successful, this method returns a `201 Created` response code and a [androidTrustedRootCertificate](../resources/intune-deviceconfig-androidtrustedrootcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="11baf-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="11baf-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="11baf-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="11baf-177">Request</span></span>
<span data-ttu-id="11baf-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="11baf-178">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 431

{
  "@odata.type": "#microsoft.graph.androidTrustedRootCertificate",
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

### <a name="response"></a><span data-ttu-id="11baf-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11baf-179">Response</span></span>
<span data-ttu-id="11baf-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="11baf-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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






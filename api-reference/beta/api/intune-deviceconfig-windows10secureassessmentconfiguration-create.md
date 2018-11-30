---
title: Crear windows10SecureAssessmentConfiguration
description: Crear un objeto windows10SecureAssessmentConfiguration.
ms.openlocfilehash: 79fbeb6633cc589a58bcb24349e417f61b07377e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083259"
---
# <a name="create-windows10secureassessmentconfiguration"></a><span data-ttu-id="845f4-103">Crear windows10SecureAssessmentConfiguration</span><span class="sxs-lookup"><span data-stu-id="845f4-103">Create windows10SecureAssessmentConfiguration</span></span>

> <span data-ttu-id="845f4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="845f4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="845f4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="845f4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="845f4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="845f4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="845f4-107">Crear un objeto [windows10SecureAssessmentConfiguration](../resources/intune-deviceconfig-windows10secureassessmentconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="845f4-107">Create a new [windows10SecureAssessmentConfiguration](../resources/intune-deviceconfig-windows10secureassessmentconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="845f4-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="845f4-108">Prerequisites</span></span>
<span data-ttu-id="845f4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="845f4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="845f4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="845f4-111">Permission type</span></span>|<span data-ttu-id="845f4-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="845f4-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="845f4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="845f4-113">Delegated (work or school account)</span></span>|<span data-ttu-id="845f4-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="845f4-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="845f4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="845f4-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="845f4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="845f4-116">Not supported.</span></span>|
|<span data-ttu-id="845f4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="845f4-117">Application</span></span>|<span data-ttu-id="845f4-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="845f4-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="845f4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="845f4-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="845f4-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="845f4-120">Request headers</span></span>
|<span data-ttu-id="845f4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="845f4-121">Header</span></span>|<span data-ttu-id="845f4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="845f4-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="845f4-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="845f4-123">Authorization</span></span>|<span data-ttu-id="845f4-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="845f4-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="845f4-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="845f4-125">Accept</span></span>|<span data-ttu-id="845f4-126">application/json</span><span class="sxs-lookup"><span data-stu-id="845f4-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="845f4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="845f4-127">Request body</span></span>
<span data-ttu-id="845f4-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows10SecureAssessmentConfiguration.</span><span class="sxs-lookup"><span data-stu-id="845f4-128">In the request body, supply a JSON representation for the windows10SecureAssessmentConfiguration object.</span></span>

<span data-ttu-id="845f4-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows10SecureAssessmentConfiguration.</span><span class="sxs-lookup"><span data-stu-id="845f4-129">The following table shows the properties that are required when you create the windows10SecureAssessmentConfiguration.</span></span>

|<span data-ttu-id="845f4-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="845f4-130">Property</span></span>|<span data-ttu-id="845f4-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="845f4-131">Type</span></span>|<span data-ttu-id="845f4-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="845f4-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="845f4-133">id</span><span class="sxs-lookup"><span data-stu-id="845f4-133">id</span></span>|<span data-ttu-id="845f4-134">String</span><span class="sxs-lookup"><span data-stu-id="845f4-134">String</span></span>|<span data-ttu-id="845f4-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="845f4-135">Key of the entity.</span></span> <span data-ttu-id="845f4-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="845f4-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="845f4-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="845f4-137">lastModifiedDateTime</span></span>|<span data-ttu-id="845f4-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="845f4-138">DateTimeOffset</span></span>|<span data-ttu-id="845f4-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="845f4-139">DateTime the object was last modified.</span></span> <span data-ttu-id="845f4-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="845f4-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="845f4-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="845f4-141">roleScopeTagIds</span></span>|<span data-ttu-id="845f4-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="845f4-142">String collection</span></span>|<span data-ttu-id="845f4-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="845f4-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="845f4-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="845f4-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="845f4-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="845f4-145">supportsScopeTags</span></span>|<span data-ttu-id="845f4-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="845f4-146">Boolean</span></span>|<span data-ttu-id="845f4-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="845f4-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="845f4-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="845f4-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="845f4-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="845f4-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="845f4-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="845f4-150">This property is read-only.</span></span> <span data-ttu-id="845f4-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="845f4-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="845f4-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="845f4-152">createdDateTime</span></span>|<span data-ttu-id="845f4-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="845f4-153">DateTimeOffset</span></span>|<span data-ttu-id="845f4-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="845f4-154">DateTime the object was created.</span></span> <span data-ttu-id="845f4-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="845f4-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="845f4-156">descripción</span><span class="sxs-lookup"><span data-stu-id="845f4-156">description</span></span>|<span data-ttu-id="845f4-157">String</span><span class="sxs-lookup"><span data-stu-id="845f4-157">String</span></span>|<span data-ttu-id="845f4-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="845f4-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="845f4-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="845f4-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="845f4-160">displayName</span><span class="sxs-lookup"><span data-stu-id="845f4-160">displayName</span></span>|<span data-ttu-id="845f4-161">String</span><span class="sxs-lookup"><span data-stu-id="845f4-161">String</span></span>|<span data-ttu-id="845f4-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="845f4-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="845f4-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="845f4-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="845f4-164">version</span><span class="sxs-lookup"><span data-stu-id="845f4-164">version</span></span>|<span data-ttu-id="845f4-165">Int32</span><span class="sxs-lookup"><span data-stu-id="845f4-165">Int32</span></span>|<span data-ttu-id="845f4-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="845f4-166">Version of the device configuration.</span></span> <span data-ttu-id="845f4-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="845f4-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="845f4-168">launchUri</span><span class="sxs-lookup"><span data-stu-id="845f4-168">launchUri</span></span>|<span data-ttu-id="845f4-169">String</span><span class="sxs-lookup"><span data-stu-id="845f4-169">String</span></span>|<span data-ttu-id="845f4-170">Vínculo de dirección URL a una evaluación que se carga automáticamente al iniciar el explorador de evaluaciones seguras.</span><span class="sxs-lookup"><span data-stu-id="845f4-170">Url link to an assessment that's automatically loaded when the secure assessment browser is launched.</span></span> <span data-ttu-id="845f4-171">Tiene que ser una dirección URL válida (http\[s\]://msdn.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="845f4-171">It has to be a valid Url (http\[s\]://msdn.microsoft.com/).</span></span>|
|<span data-ttu-id="845f4-172">configurationAccount</span><span class="sxs-lookup"><span data-stu-id="845f4-172">configurationAccount</span></span>|<span data-ttu-id="845f4-173">String</span><span class="sxs-lookup"><span data-stu-id="845f4-173">String</span></span>|<span data-ttu-id="845f4-174">Cuenta usada al configurar el dispositivo Windows para realizar la prueba.</span><span class="sxs-lookup"><span data-stu-id="845f4-174">The account used to configure the Windows device for taking the test.</span></span> <span data-ttu-id="845f4-175">El usuario puede ser una cuenta de dominio (dominio\usuario), una cuenta de AAD (nombredeusuario@espacioempresarial.com) o una cuenta local (nombredeusuario).</span><span class="sxs-lookup"><span data-stu-id="845f4-175">The user can be a domain account (domain\user), an AAD account (username@tenant.com) or a local account (username).</span></span>|
|<span data-ttu-id="845f4-176">configurationAccountType</span><span class="sxs-lookup"><span data-stu-id="845f4-176">configurationAccountType</span></span>|[<span data-ttu-id="845f4-177">secureAssessmentAccountType</span><span class="sxs-lookup"><span data-stu-id="845f4-177">secureAssessmentAccountType</span></span>](../resources/intune-deviceconfig-secureassessmentaccounttype.md)|<span data-ttu-id="845f4-178">El tipo de cuenta que se usa para ConfigurationAccount.</span><span class="sxs-lookup"><span data-stu-id="845f4-178">The account type used to by ConfigurationAccount.</span></span> <span data-ttu-id="845f4-179">Los valores posibles son: `azureADAccount`, `domainAccount` y `localAccount`.</span><span class="sxs-lookup"><span data-stu-id="845f4-179">Possible values are: `azureADAccount`, `domainAccount`, `localAccount`.</span></span>|
|<span data-ttu-id="845f4-180">allowPrinting</span><span class="sxs-lookup"><span data-stu-id="845f4-180">allowPrinting</span></span>|<span data-ttu-id="845f4-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="845f4-181">Boolean</span></span>|<span data-ttu-id="845f4-182">Indica si se va a permitir que la aplicación imprima durante la prueba.</span><span class="sxs-lookup"><span data-stu-id="845f4-182">Indicates whether or not to allow the app from printing during the test.</span></span>|
|<span data-ttu-id="845f4-183">allowScreenCapture</span><span class="sxs-lookup"><span data-stu-id="845f4-183">allowScreenCapture</span></span>|<span data-ttu-id="845f4-184">Booleano</span><span class="sxs-lookup"><span data-stu-id="845f4-184">Boolean</span></span>|<span data-ttu-id="845f4-185">Indica si se va a permitir la funcionalidad de captura de pantalla durante una prueba.</span><span class="sxs-lookup"><span data-stu-id="845f4-185">Indicates whether or not to allow screen capture capability during a test.</span></span>|
|<span data-ttu-id="845f4-186">allowTextSuggestion</span><span class="sxs-lookup"><span data-stu-id="845f4-186">allowTextSuggestion</span></span>|<span data-ttu-id="845f4-187">Booleano</span><span class="sxs-lookup"><span data-stu-id="845f4-187">Boolean</span></span>|<span data-ttu-id="845f4-188">Indica si se van a permitir las sugerencias de texto durante la prueba.</span><span class="sxs-lookup"><span data-stu-id="845f4-188">Indicates whether or not to allow text suggestions during the test.</span></span>|



## <a name="response"></a><span data-ttu-id="845f4-189">Respuesta</span><span class="sxs-lookup"><span data-stu-id="845f4-189">Response</span></span>
<span data-ttu-id="845f4-190">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows10SecureAssessmentConfiguration](../resources/intune-deviceconfig-windows10secureassessmentconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="845f4-190">If successful, this method returns a `201 Created` response code and a [windows10SecureAssessmentConfiguration](../resources/intune-deviceconfig-windows10secureassessmentconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="845f4-191">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="845f4-191">Example</span></span>
### <a name="request"></a><span data-ttu-id="845f4-192">Solicitud</span><span class="sxs-lookup"><span data-stu-id="845f4-192">Request</span></span>
<span data-ttu-id="845f4-193">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="845f4-193">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 563

{
  "@odata.type": "#microsoft.graph.windows10SecureAssessmentConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "launchUri": "Launch Uri value",
  "configurationAccount": "Configuration Account value",
  "configurationAccountType": "domainAccount",
  "allowPrinting": true,
  "allowScreenCapture": true,
  "allowTextSuggestion": true
}
```

### <a name="response"></a><span data-ttu-id="845f4-194">Respuesta</span><span class="sxs-lookup"><span data-stu-id="845f4-194">Response</span></span>
<span data-ttu-id="845f4-p114">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="845f4-p114">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 671

{
  "@odata.type": "#microsoft.graph.windows10SecureAssessmentConfiguration",
  "id": "f60d71be-71be-f60d-be71-0df6be710df6",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "launchUri": "Launch Uri value",
  "configurationAccount": "Configuration Account value",
  "configurationAccountType": "domainAccount",
  "allowPrinting": true,
  "allowScreenCapture": true,
  "allowTextSuggestion": true
}
```





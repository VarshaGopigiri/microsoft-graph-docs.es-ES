---
title: Actualizar iosEduDeviceConfiguration
description: Actualizar las propiedades de un objeto iosEduDeviceConfiguration.
ms.openlocfilehash: e911337bcbe220cff76d58dc01c462324bb2226f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088270"
---
# <a name="update-iosedudeviceconfiguration"></a><span data-ttu-id="e92ed-103">Actualizar iosEduDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e92ed-103">Update iosEduDeviceConfiguration</span></span>

> <span data-ttu-id="e92ed-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e92ed-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e92ed-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e92ed-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e92ed-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e92ed-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e92ed-107">Actualizar las propiedades de un objeto [iosEduDeviceConfiguration](../resources/intune-deviceconfig-iosedudeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="e92ed-107">Update the properties of a [iosEduDeviceConfiguration](../resources/intune-deviceconfig-iosedudeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e92ed-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e92ed-108">Prerequisites</span></span>
<span data-ttu-id="e92ed-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e92ed-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e92ed-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e92ed-111">Permission type</span></span>|<span data-ttu-id="e92ed-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e92ed-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e92ed-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e92ed-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e92ed-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e92ed-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="e92ed-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e92ed-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e92ed-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e92ed-116">Not supported.</span></span>|
|<span data-ttu-id="e92ed-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e92ed-117">Application</span></span>|<span data-ttu-id="e92ed-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e92ed-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e92ed-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e92ed-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="e92ed-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e92ed-120">Request headers</span></span>
|<span data-ttu-id="e92ed-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e92ed-121">Header</span></span>|<span data-ttu-id="e92ed-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e92ed-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e92ed-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="e92ed-123">Authorization</span></span>|<span data-ttu-id="e92ed-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e92ed-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e92ed-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e92ed-125">Accept</span></span>|<span data-ttu-id="e92ed-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e92ed-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e92ed-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e92ed-127">Request body</span></span>
<span data-ttu-id="e92ed-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [iosEduDeviceConfiguration](../resources/intune-deviceconfig-iosedudeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="e92ed-128">In the request body, supply a JSON representation for the [iosEduDeviceConfiguration](../resources/intune-deviceconfig-iosedudeviceconfiguration.md) object.</span></span>

<span data-ttu-id="e92ed-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [iosEduDeviceConfiguration](../resources/intune-deviceconfig-iosedudeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e92ed-129">The following table shows the properties that are required when you create the [iosEduDeviceConfiguration](../resources/intune-deviceconfig-iosedudeviceconfiguration.md).</span></span>

|<span data-ttu-id="e92ed-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e92ed-130">Property</span></span>|<span data-ttu-id="e92ed-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e92ed-131">Type</span></span>|<span data-ttu-id="e92ed-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e92ed-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e92ed-133">id</span><span class="sxs-lookup"><span data-stu-id="e92ed-133">id</span></span>|<span data-ttu-id="e92ed-134">String</span><span class="sxs-lookup"><span data-stu-id="e92ed-134">String</span></span>|<span data-ttu-id="e92ed-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e92ed-135">Key of the entity.</span></span> <span data-ttu-id="e92ed-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e92ed-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e92ed-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e92ed-137">lastModifiedDateTime</span></span>|<span data-ttu-id="e92ed-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e92ed-138">DateTimeOffset</span></span>|<span data-ttu-id="e92ed-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="e92ed-139">DateTime the object was last modified.</span></span> <span data-ttu-id="e92ed-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e92ed-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e92ed-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="e92ed-141">roleScopeTagIds</span></span>|<span data-ttu-id="e92ed-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="e92ed-142">String collection</span></span>|<span data-ttu-id="e92ed-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="e92ed-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="e92ed-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e92ed-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e92ed-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="e92ed-145">supportsScopeTags</span></span>|<span data-ttu-id="e92ed-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="e92ed-146">Boolean</span></span>|<span data-ttu-id="e92ed-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e92ed-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="e92ed-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="e92ed-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="e92ed-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="e92ed-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="e92ed-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="e92ed-150">This property is read-only.</span></span> <span data-ttu-id="e92ed-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e92ed-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e92ed-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e92ed-152">createdDateTime</span></span>|<span data-ttu-id="e92ed-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e92ed-153">DateTimeOffset</span></span>|<span data-ttu-id="e92ed-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="e92ed-154">DateTime the object was created.</span></span> <span data-ttu-id="e92ed-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e92ed-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e92ed-156">descripción</span><span class="sxs-lookup"><span data-stu-id="e92ed-156">description</span></span>|<span data-ttu-id="e92ed-157">String</span><span class="sxs-lookup"><span data-stu-id="e92ed-157">String</span></span>|<span data-ttu-id="e92ed-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e92ed-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="e92ed-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e92ed-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e92ed-160">displayName</span><span class="sxs-lookup"><span data-stu-id="e92ed-160">displayName</span></span>|<span data-ttu-id="e92ed-161">String</span><span class="sxs-lookup"><span data-stu-id="e92ed-161">String</span></span>|<span data-ttu-id="e92ed-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e92ed-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="e92ed-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e92ed-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e92ed-164">version</span><span class="sxs-lookup"><span data-stu-id="e92ed-164">version</span></span>|<span data-ttu-id="e92ed-165">Int32</span><span class="sxs-lookup"><span data-stu-id="e92ed-165">Int32</span></span>|<span data-ttu-id="e92ed-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e92ed-166">Version of the device configuration.</span></span> <span data-ttu-id="e92ed-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e92ed-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e92ed-168">teacherCertificateSettings</span><span class="sxs-lookup"><span data-stu-id="e92ed-168">teacherCertificateSettings</span></span>|[<span data-ttu-id="e92ed-169">iosEduCertificateSettings</span><span class="sxs-lookup"><span data-stu-id="e92ed-169">iosEduCertificateSettings</span></span>](../resources/intune-deviceconfig-ioseducertificatesettings.md)|<span data-ttu-id="e92ed-170">Los certificados raíz de confianza y PFX de profesor</span><span class="sxs-lookup"><span data-stu-id="e92ed-170">The Trusted Root and PFX certificates for Teacher</span></span>|
|<span data-ttu-id="e92ed-171">studentCertificateSettings</span><span class="sxs-lookup"><span data-stu-id="e92ed-171">studentCertificateSettings</span></span>|[<span data-ttu-id="e92ed-172">iosEduCertificateSettings</span><span class="sxs-lookup"><span data-stu-id="e92ed-172">iosEduCertificateSettings</span></span>](../resources/intune-deviceconfig-ioseducertificatesettings.md)|<span data-ttu-id="e92ed-173">Los certificados raíz de confianza y PFX de estudiante</span><span class="sxs-lookup"><span data-stu-id="e92ed-173">The Trusted Root and PFX certificates for Student</span></span>|
|<span data-ttu-id="e92ed-174">deviceCertificateSettings</span><span class="sxs-lookup"><span data-stu-id="e92ed-174">deviceCertificateSettings</span></span>|[<span data-ttu-id="e92ed-175">iosEduCertificateSettings</span><span class="sxs-lookup"><span data-stu-id="e92ed-175">iosEduCertificateSettings</span></span>](../resources/intune-deviceconfig-ioseducertificatesettings.md)|<span data-ttu-id="e92ed-176">Los certificados raíz de confianza y PFX de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e92ed-176">The Trusted Root and PFX certificates for Device</span></span>|



## <a name="response"></a><span data-ttu-id="e92ed-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e92ed-177">Response</span></span>
<span data-ttu-id="e92ed-178">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [iosEduDeviceConfiguration](../resources/intune-deviceconfig-iosedudeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e92ed-178">If successful, this method returns a `200 OK` response code and an updated [iosEduDeviceConfiguration](../resources/intune-deviceconfig-iosedudeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e92ed-179">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e92ed-179">Example</span></span>
### <a name="request"></a><span data-ttu-id="e92ed-180">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e92ed-180">Request</span></span>
<span data-ttu-id="e92ed-181">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e92ed-181">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1910

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "teacherCertificateSettings": {
    "@odata.type": "microsoft.graph.iosEduCertificateSettings",
    "trustedRootCertificate": "dHJ1c3RlZFJvb3RDZXJ0aWZpY2F0ZQ==",
    "certFileName": "Cert File Name value",
    "certificationAuthority": "Certification Authority value",
    "certificationAuthorityName": "Certification Authority Name value",
    "certificateTemplateName": "Certificate Template Name value",
    "renewalThresholdPercentage": 10,
    "certificateValidityPeriodValue": 14,
    "certificateValidityPeriodScale": "months"
  },
  "studentCertificateSettings": {
    "@odata.type": "microsoft.graph.iosEduCertificateSettings",
    "trustedRootCertificate": "dHJ1c3RlZFJvb3RDZXJ0aWZpY2F0ZQ==",
    "certFileName": "Cert File Name value",
    "certificationAuthority": "Certification Authority value",
    "certificationAuthorityName": "Certification Authority Name value",
    "certificateTemplateName": "Certificate Template Name value",
    "renewalThresholdPercentage": 10,
    "certificateValidityPeriodValue": 14,
    "certificateValidityPeriodScale": "months"
  },
  "deviceCertificateSettings": {
    "@odata.type": "microsoft.graph.iosEduCertificateSettings",
    "trustedRootCertificate": "dHJ1c3RlZFJvb3RDZXJ0aWZpY2F0ZQ==",
    "certFileName": "Cert File Name value",
    "certificationAuthority": "Certification Authority value",
    "certificationAuthorityName": "Certification Authority Name value",
    "certificateTemplateName": "Certificate Template Name value",
    "renewalThresholdPercentage": 10,
    "certificateValidityPeriodValue": 14,
    "certificateValidityPeriodScale": "months"
  }
}
```

### <a name="response"></a><span data-ttu-id="e92ed-182">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e92ed-182">Response</span></span>
<span data-ttu-id="e92ed-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e92ed-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2082

{
  "@odata.type": "#microsoft.graph.iosEduDeviceConfiguration",
  "id": "4c5df9b6-f9b6-4c5d-b6f9-5d4cb6f95d4c",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "teacherCertificateSettings": {
    "@odata.type": "microsoft.graph.iosEduCertificateSettings",
    "trustedRootCertificate": "dHJ1c3RlZFJvb3RDZXJ0aWZpY2F0ZQ==",
    "certFileName": "Cert File Name value",
    "certificationAuthority": "Certification Authority value",
    "certificationAuthorityName": "Certification Authority Name value",
    "certificateTemplateName": "Certificate Template Name value",
    "renewalThresholdPercentage": 10,
    "certificateValidityPeriodValue": 14,
    "certificateValidityPeriodScale": "months"
  },
  "studentCertificateSettings": {
    "@odata.type": "microsoft.graph.iosEduCertificateSettings",
    "trustedRootCertificate": "dHJ1c3RlZFJvb3RDZXJ0aWZpY2F0ZQ==",
    "certFileName": "Cert File Name value",
    "certificationAuthority": "Certification Authority value",
    "certificationAuthorityName": "Certification Authority Name value",
    "certificateTemplateName": "Certificate Template Name value",
    "renewalThresholdPercentage": 10,
    "certificateValidityPeriodValue": 14,
    "certificateValidityPeriodScale": "months"
  },
  "deviceCertificateSettings": {
    "@odata.type": "microsoft.graph.iosEduCertificateSettings",
    "trustedRootCertificate": "dHJ1c3RlZFJvb3RDZXJ0aWZpY2F0ZQ==",
    "certFileName": "Cert File Name value",
    "certificationAuthority": "Certification Authority value",
    "certificationAuthorityName": "Certification Authority Name value",
    "certificateTemplateName": "Certificate Template Name value",
    "renewalThresholdPercentage": 10,
    "certificateValidityPeriodValue": 14,
    "certificateValidityPeriodScale": "months"
  }
}
```





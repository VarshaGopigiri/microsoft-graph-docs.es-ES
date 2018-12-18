---
title: Actualizar windowsInformationProtectionPolicy
description: Actualice las propiedades de un objeto windowsInformationProtectionPolicy.
author: tfitzmac
ms.openlocfilehash: 0b2ab06d8ee197842314a2bd03d4cc457401c4ef
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27363770"
---
# <a name="update-windowsinformationprotectionpolicy"></a><span data-ttu-id="c2611-103">Actualizar windowsInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c2611-103">Update windowsInformationProtectionPolicy</span></span>

> <span data-ttu-id="c2611-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c2611-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c2611-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c2611-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c2611-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c2611-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c2611-107">Actualice las propiedades de un objeto [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-107">Update the properties of a [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c2611-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c2611-108">Prerequisites</span></span>
<span data-ttu-id="c2611-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c2611-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c2611-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c2611-111">Permission type</span></span>|<span data-ttu-id="c2611-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c2611-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c2611-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c2611-113">Delegated (work or school account)</span></span>|<span data-ttu-id="c2611-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c2611-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="c2611-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c2611-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c2611-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c2611-116">Not supported.</span></span>|
|<span data-ttu-id="c2611-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c2611-117">Application</span></span>|<span data-ttu-id="c2611-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c2611-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c2611-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c2611-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="c2611-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c2611-120">Request headers</span></span>
|<span data-ttu-id="c2611-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2611-121">Header</span></span>|<span data-ttu-id="c2611-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c2611-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c2611-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="c2611-123">Authorization</span></span>|<span data-ttu-id="c2611-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c2611-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c2611-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c2611-125">Accept</span></span>|<span data-ttu-id="c2611-126">application/json</span><span class="sxs-lookup"><span data-stu-id="c2611-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c2611-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c2611-127">Request body</span></span>
<span data-ttu-id="c2611-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-128">In the request body, supply a JSON representation for the [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md) object.</span></span>

<span data-ttu-id="c2611-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-129">The following table shows the properties that are required when you create the [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md).</span></span>

|<span data-ttu-id="c2611-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c2611-130">Property</span></span>|<span data-ttu-id="c2611-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c2611-131">Type</span></span>|<span data-ttu-id="c2611-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2611-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c2611-133">displayName</span><span class="sxs-lookup"><span data-stu-id="c2611-133">displayName</span></span>|<span data-ttu-id="c2611-134">String</span><span class="sxs-lookup"><span data-stu-id="c2611-134">String</span></span>|<span data-ttu-id="c2611-135">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="c2611-135">Policy display name.</span></span> <span data-ttu-id="c2611-136">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-136">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="c2611-137">descripción</span><span class="sxs-lookup"><span data-stu-id="c2611-137">description</span></span>|<span data-ttu-id="c2611-138">String</span><span class="sxs-lookup"><span data-stu-id="c2611-138">String</span></span>|<span data-ttu-id="c2611-139">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="c2611-139">The policy's description.</span></span> <span data-ttu-id="c2611-140">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-140">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="c2611-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c2611-141">createdDateTime</span></span>|<span data-ttu-id="c2611-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c2611-142">DateTimeOffset</span></span>|<span data-ttu-id="c2611-143">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="c2611-143">The date and time the policy was created.</span></span> <span data-ttu-id="c2611-144">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-144">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="c2611-145">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="c2611-145">lastModifiedDateTime</span></span>|<span data-ttu-id="c2611-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c2611-146">DateTimeOffset</span></span>|<span data-ttu-id="c2611-147">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="c2611-147">Last time the policy was modified.</span></span> <span data-ttu-id="c2611-148">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-148">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="c2611-149">id</span><span class="sxs-lookup"><span data-stu-id="c2611-149">id</span></span>|<span data-ttu-id="c2611-150">String</span><span class="sxs-lookup"><span data-stu-id="c2611-150">String</span></span>|<span data-ttu-id="c2611-151">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c2611-151">Key of the entity.</span></span> <span data-ttu-id="c2611-152">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-152">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="c2611-153">version</span><span class="sxs-lookup"><span data-stu-id="c2611-153">version</span></span>|<span data-ttu-id="c2611-154">String</span><span class="sxs-lookup"><span data-stu-id="c2611-154">String</span></span>|<span data-ttu-id="c2611-155">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c2611-155">Version of the entity.</span></span> <span data-ttu-id="c2611-156">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-156">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="c2611-157">enforcementLevel</span><span class="sxs-lookup"><span data-stu-id="c2611-157">enforcementLevel</span></span>|[<span data-ttu-id="c2611-158">windowsInformationProtectionEnforcementLevel</span><span class="sxs-lookup"><span data-stu-id="c2611-158">windowsInformationProtectionEnforcementLevel</span></span>](../resources/intune-mam-windowsinformationprotectionenforcementlevel.md)|<span data-ttu-id="c2611-159">Nivel de aplicación de trabajo en curso. Vea la definición de enumeración para los valores admitidos Inherited desde [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-159">WIP enforcement level.See the Enum definition for supported values Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span></span> <span data-ttu-id="c2611-160">Los valores posibles son: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt` y `encryptAuditAndBlock`.</span><span class="sxs-lookup"><span data-stu-id="c2611-160">Possible values are: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt`, `encryptAuditAndBlock`.</span></span>|
|<span data-ttu-id="c2611-161">enterpriseDomain</span><span class="sxs-lookup"><span data-stu-id="c2611-161">enterpriseDomain</span></span>|<span data-ttu-id="c2611-162">String</span><span class="sxs-lookup"><span data-stu-id="c2611-162">String</span></span>|<span data-ttu-id="c2611-163">Dominio empresarial principal. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-163">Primary enterprise domain Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-164">enterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="c2611-164">enterpriseProtectedDomainNames</span></span>|<span data-ttu-id="c2611-165">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="c2611-165">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="c2611-166">Lista de dominios de empresa que se van a proteger. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-166">List of enterprise domains to be protected Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-167">protectionUnderLockConfigRequired</span><span class="sxs-lookup"><span data-stu-id="c2611-167">protectionUnderLockConfigRequired</span></span>|<span data-ttu-id="c2611-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="c2611-168">Boolean</span></span>|<span data-ttu-id="c2611-169">Especifica si es necesario configurar la protección en la característica de bloqueo (también conocida como cifrar con PIN). Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-169">Specifies whether the protection under lock feature (also known as encrypt under pin) should be configured Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-170">dataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="c2611-170">dataRecoveryCertificate</span></span>|[<span data-ttu-id="c2611-171">windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="c2611-171">windowsInformationProtectionDataRecoveryCertificate</span></span>](../resources/intune-mam-windowsinformationprotectiondatarecoverycertificate.md)|<span data-ttu-id="c2611-172">Especifica un certificado de recuperación que se puede usar para recuperar datos de archivos cifrados.</span><span class="sxs-lookup"><span data-stu-id="c2611-172">Specifies a recovery certificate that can be used for data recovery of encrypted files.</span></span> <span data-ttu-id="c2611-173">Es igual al certificado del agente de recuperación de datos (DRA) para el sistema de cifrado de archivos (EFS). Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="c2611-173">This is the same as the data recovery agent(DRA) certificate for encrypting file system(EFS) Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-174">revokeOnUnenrollDisabled</span><span class="sxs-lookup"><span data-stu-id="c2611-174">revokeOnUnenrollDisabled</span></span>|<span data-ttu-id="c2611-175">Boolean</span><span class="sxs-lookup"><span data-stu-id="c2611-175">Boolean</span></span>|<span data-ttu-id="c2611-176">Esta directiva controla si se revocan las claves de trabajo en curso cuando se anula la inscripción de un dispositivo en el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="c2611-176">This policy controls whether to revoke the WIP keys when a device unenrolls from the management service.</span></span> <span data-ttu-id="c2611-177">Si se establece en 1 (no revocar las claves), no se revocarán las claves y el usuario seguirá teniendo acceso a archivos protegidos después de anular la inscripción.</span><span class="sxs-lookup"><span data-stu-id="c2611-177">If set to 1 (Don't revoke keys), the keys will not be revoked and the user will continue to have access to protected files after unenrollment.</span></span> <span data-ttu-id="c2611-178">Si no se revocan las claves, no habrá ninguna limpieza de archivos revocados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="c2611-178">If the keys are not revoked, there will be no revoked file cleanup subsequently.</span></span> <span data-ttu-id="c2611-179">Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="c2611-179">Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-180">rightsManagementServicesTemplateId</span><span class="sxs-lookup"><span data-stu-id="c2611-180">rightsManagementServicesTemplateId</span></span>|<span data-ttu-id="c2611-181">Guid</span><span class="sxs-lookup"><span data-stu-id="c2611-181">Guid</span></span>|<span data-ttu-id="c2611-182">GUID de TemplateID que se va a usar para el cifrado RMS.</span><span class="sxs-lookup"><span data-stu-id="c2611-182">TemplateID GUID to use for RMS encryption.</span></span> <span data-ttu-id="c2611-183">La plantilla de RMS permite que el administrador de TI configure los detalles sobre quién tiene acceso a los archivos protegidos por RMS y durante cuánto tiempo. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-183">The RMS template allows the IT admin to configure the details about who has access to RMS-protected file and how long they have access Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-184">azureRightsManagementServicesAllowed</span><span class="sxs-lookup"><span data-stu-id="c2611-184">azureRightsManagementServicesAllowed</span></span>|<span data-ttu-id="c2611-185">Booleano</span><span class="sxs-lookup"><span data-stu-id="c2611-185">Boolean</span></span>|<span data-ttu-id="c2611-186">Especifica si se permite el cifrado de Azure RMS para WIP. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-186">Specifies whether to allow Azure RMS encryption for WIP Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-187">iconsVisible</span><span class="sxs-lookup"><span data-stu-id="c2611-187">iconsVisible</span></span>|<span data-ttu-id="c2611-188">Boolean</span><span class="sxs-lookup"><span data-stu-id="c2611-188">Boolean</span></span>|<span data-ttu-id="c2611-189">Determina si se agregan las superposiciones a los iconos para los archivos protegidos mediante WIP en Explorer y en los iconos de aplicación solo de empresa en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="c2611-189">Determines whether overlays are added to icons for WIP protected files in Explorer and enterprise only app tiles in the Start menu.</span></span> <span data-ttu-id="c2611-190">A partir de Windows 10, versión 1703, estos ajustes también configuran la visibilidad del icono de WIP en la barra de título de una aplicación protegida mediante WIP. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-190">Starting in Windows 10, version 1703 this setting also configures the visibility of the WIP icon in the title bar of a WIP-protected app Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-191">protectedApps</span><span class="sxs-lookup"><span data-stu-id="c2611-191">protectedApps</span></span>|<span data-ttu-id="c2611-192">Colección [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="c2611-192">[windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="c2611-193">Las aplicaciones protegidas pueden tener acceso a datos empresariales y los datos controlados por dichas aplicaciones están protegidos mediante cifrado. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-193">Protected applications can access enterprise data and the data handled by those applications are protected with encryption Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-194">exemptApps</span><span class="sxs-lookup"><span data-stu-id="c2611-194">exemptApps</span></span>|<span data-ttu-id="c2611-195">Colección [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="c2611-195">[windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="c2611-196">Las aplicaciones exentas también pueden tener acceso a datos empresariales, pero los datos controlados por dichas aplicaciones no están protegidos.</span><span class="sxs-lookup"><span data-stu-id="c2611-196">Exempt applications can also access enterprise data, but the data handled by those applications are not protected.</span></span> <span data-ttu-id="c2611-197">Esto ocurre porque algunas aplicaciones empresariales críticas podrían tener problemas de compatibilidad con los datos cifrados.</span><span class="sxs-lookup"><span data-stu-id="c2611-197">This is because some critical enterprise applications may have compatibility problems with encrypted data.</span></span> <span data-ttu-id="c2611-198">Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="c2611-198">Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-199">enterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="c2611-199">enterpriseNetworkDomainNames</span></span>|<span data-ttu-id="c2611-200">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="c2611-200">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="c2611-201">Esta es la lista de dominios que forman parte de los límites de la empresa.</span><span class="sxs-lookup"><span data-stu-id="c2611-201">This is the list of domains that comprise the boundaries of the enterprise.</span></span> <span data-ttu-id="c2611-202">Los datos de uno de estos dominios que se envíen a un dispositivo se considerarán datos empresariales y protegidos. Estas ubicaciones se consideran un destino seguro con el que compartir datos empresariales. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-202">Data from one of these domains that is sent to a device will be considered enterprise data and protected These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-203">enterpriseProxiedDomains</span><span class="sxs-lookup"><span data-stu-id="c2611-203">enterpriseProxiedDomains</span></span>|<span data-ttu-id="c2611-204">Colección [windowsInformationProtectionProxiedDomainCollection](../resources/intune-mam-windowsinformationprotectionproxieddomaincollection.md)</span><span class="sxs-lookup"><span data-stu-id="c2611-204">[windowsInformationProtectionProxiedDomainCollection](../resources/intune-mam-windowsinformationprotectionproxieddomaincollection.md) collection</span></span>|<span data-ttu-id="c2611-205">Contiene una lista de dominios de recursos empresariales hospedados en la nube que necesitan protección.</span><span class="sxs-lookup"><span data-stu-id="c2611-205">Contains a list of Enterprise resource domains hosted in the cloud that need to be protected.</span></span> <span data-ttu-id="c2611-206">Las conexiones a estos recursos se consideran datos empresariales.</span><span class="sxs-lookup"><span data-stu-id="c2611-206">Connections to these resources are considered enterprise data.</span></span> <span data-ttu-id="c2611-207">Si un proxy se corresponde con un recurso de nube, el tráfico al recurso de la nube se dirigirá a través de la red empresarial mediante el servidor proxy indicado (en el puerto 80).</span><span class="sxs-lookup"><span data-stu-id="c2611-207">If a proxy is paired with a cloud resource, traffic to the cloud resource will be routed through the enterprise network via the denoted proxy server (on Port 80).</span></span> <span data-ttu-id="c2611-208">Un servidor proxy que se use con esta finalidad debe configurarse también mediante la directiva EnterpriseInternalProxyServers. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-208">A proxy server used for this purpose must also be configured using the EnterpriseInternalProxyServers policy Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-209">enterpriseIPRanges</span><span class="sxs-lookup"><span data-stu-id="c2611-209">enterpriseIPRanges</span></span>|<span data-ttu-id="c2611-210">Colección [windowsInformationProtectionIPRangeCollection](../resources/intune-mam-windowsinformationprotectioniprangecollection.md)</span><span class="sxs-lookup"><span data-stu-id="c2611-210">[windowsInformationProtectionIPRangeCollection](../resources/intune-mam-windowsinformationprotectioniprangecollection.md) collection</span></span>|<span data-ttu-id="c2611-211">Establece los intervalos IP empresariales que definen los equipos de la red empresarial.</span><span class="sxs-lookup"><span data-stu-id="c2611-211">Sets the enterprise IP ranges that define the computers in the enterprise network.</span></span> <span data-ttu-id="c2611-212">Los datos que provienen de dichos equipos se consideran parte de la empresa y están protegidos.</span><span class="sxs-lookup"><span data-stu-id="c2611-212">Data that comes from those computers will be considered part of the enterprise and protected.</span></span> <span data-ttu-id="c2611-213">Estas ubicaciones se consideran un destino seguro en el que compartir datos empresariales. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-213">These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-214">enterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="c2611-214">enterpriseIPRangesAreAuthoritative</span></span>|<span data-ttu-id="c2611-215">Boolean</span><span class="sxs-lookup"><span data-stu-id="c2611-215">Boolean</span></span>|<span data-ttu-id="c2611-216">Valor booleano que indica al cliente que acepte la lista configurada y que no use la heurística para intentar buscar otras subredes.</span><span class="sxs-lookup"><span data-stu-id="c2611-216">Boolean value that tells the client to accept the configured list and not to use heuristics to attempt to find other subnets.</span></span> <span data-ttu-id="c2611-217">El valor predeterminado es False. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-217">Default is false Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-218">enterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="c2611-218">enterpriseProxyServers</span></span>|<span data-ttu-id="c2611-219">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="c2611-219">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="c2611-220">Esta es una lista de servidores proxy.</span><span class="sxs-lookup"><span data-stu-id="c2611-220">This is a list of proxy servers.</span></span> <span data-ttu-id="c2611-221">Cualquier servidor que no esté en esta lista se considera no empresarial. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-221">Any server not on this list is considered non-enterprise Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-222">enterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="c2611-222">enterpriseInternalProxyServers</span></span>|<span data-ttu-id="c2611-223">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="c2611-223">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="c2611-224">Se trata de la lista de valores separados por comas de servidores proxy internos.</span><span class="sxs-lookup"><span data-stu-id="c2611-224">This is the comma-separated list of internal proxy servers.</span></span> <span data-ttu-id="c2611-225">Por ejemplo, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span><span class="sxs-lookup"><span data-stu-id="c2611-225">For example, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span></span> <span data-ttu-id="c2611-226">El administrador ha configurado estos servidores proxy para que se conecten a los recursos específicos de Internet.</span><span class="sxs-lookup"><span data-stu-id="c2611-226">These proxies have been configured by the admin to connect to specific resources on the Internet.</span></span> <span data-ttu-id="c2611-227">Se consideran ubicaciones de red empresarial.</span><span class="sxs-lookup"><span data-stu-id="c2611-227">They are considered to be enterprise network locations.</span></span> <span data-ttu-id="c2611-228">Los servidores proxy solo se usan al configurar la directiva EnterpriseProxiedDomains para forzar el tráfico a los dominios coincidentes mediante estos proxy. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-228">The proxies are only leveraged in configuring the EnterpriseProxiedDomains policy to force traffic to the matched domains through these proxies Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-229">enterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="c2611-229">enterpriseProxyServersAreAuthoritative</span></span>|<span data-ttu-id="c2611-230">Boolean</span><span class="sxs-lookup"><span data-stu-id="c2611-230">Boolean</span></span>|<span data-ttu-id="c2611-231">Valor booleano que indica al cliente que acepte la lista de configuración de servidores proxy y no intente detectar otros servidores proxy de trabajo.</span><span class="sxs-lookup"><span data-stu-id="c2611-231">Boolean value that tells the client to accept the configured list of proxies and not try to detect other work proxies.</span></span> <span data-ttu-id="c2611-232">El valor predeterminado es False. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-232">Default is false Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-233">neutralDomainResources</span><span class="sxs-lookup"><span data-stu-id="c2611-233">neutralDomainResources</span></span>|<span data-ttu-id="c2611-234">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="c2611-234">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="c2611-235">Lista de nombres de dominio que se pueden usar para el recurso de trabajo o personal. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-235">List of domain names that can used for work or personal resource Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-236">indexingEncryptedStoresOrItemsBlocked</span><span class="sxs-lookup"><span data-stu-id="c2611-236">indexingEncryptedStoresOrItemsBlocked</span></span>|<span data-ttu-id="c2611-237">Boolean</span><span class="sxs-lookup"><span data-stu-id="c2611-237">Boolean</span></span>|<span data-ttu-id="c2611-238">Este identificador es para que el indexador de Windows Search permita o impida la indexación de los elementos. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-238">This switch is for the Windows Search Indexer, to allow or disallow indexing of items Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-239">smbAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="c2611-239">smbAutoEncryptedFileExtensions</span></span>|<span data-ttu-id="c2611-240">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="c2611-240">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="c2611-241">Especifica una lista de extensiones de archivo, para que los archivos con estas extensiones se cifren cuando se copian desde un recurso compartido de SMB dentro del límite de la empresa. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c2611-241">Specifies a list of file extensions, so that files with these extensions are encrypted when copying from an SMB share within the corporate boundary Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-242">isAssigned</span><span class="sxs-lookup"><span data-stu-id="c2611-242">isAssigned</span></span>|<span data-ttu-id="c2611-243">Boolean</span><span class="sxs-lookup"><span data-stu-id="c2611-243">Boolean</span></span>|<span data-ttu-id="c2611-244">Indica si la directiva se implementará en los grupos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="c2611-244">Indicates if the policy is deployed to any inclusion groups or not.</span></span> <span data-ttu-id="c2611-245">Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="c2611-245">Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="c2611-246">revokeOnMdmHandoffDisabled</span><span class="sxs-lookup"><span data-stu-id="c2611-246">revokeOnMdmHandoffDisabled</span></span>|<span data-ttu-id="c2611-247">Booleano</span><span class="sxs-lookup"><span data-stu-id="c2611-247">Boolean</span></span>|<span data-ttu-id="c2611-248">Nueva propiedad en RS2, pendiente de documentación.</span><span class="sxs-lookup"><span data-stu-id="c2611-248">New property in RS2, pending documentation</span></span>|
|<span data-ttu-id="c2611-249">mdmEnrollmentUrl</span><span class="sxs-lookup"><span data-stu-id="c2611-249">mdmEnrollmentUrl</span></span>|<span data-ttu-id="c2611-250">String</span><span class="sxs-lookup"><span data-stu-id="c2611-250">String</span></span>|<span data-ttu-id="c2611-251">Dirección URL de la inscripción para MDM.</span><span class="sxs-lookup"><span data-stu-id="c2611-251">Enrollment url for the MDM</span></span>|
|<span data-ttu-id="c2611-252">windowsHelloForBusinessBlocked</span><span class="sxs-lookup"><span data-stu-id="c2611-252">windowsHelloForBusinessBlocked</span></span>|<span data-ttu-id="c2611-253">Boolean</span><span class="sxs-lookup"><span data-stu-id="c2611-253">Boolean</span></span>|<span data-ttu-id="c2611-254">Valor booleano que establece Windows Hello para empresas como método de inicio de sesión en Windows.</span><span class="sxs-lookup"><span data-stu-id="c2611-254">Boolean value that sets Windows Hello for Business as a method for signing into Windows.</span></span>|
|<span data-ttu-id="c2611-255">pinMinimumLength</span><span class="sxs-lookup"><span data-stu-id="c2611-255">pinMinimumLength</span></span>|<span data-ttu-id="c2611-256">Int32</span><span class="sxs-lookup"><span data-stu-id="c2611-256">Int32</span></span>|<span data-ttu-id="c2611-257">Valor entero que establece el número mínimo de caracteres necesarios para el PIN.</span><span class="sxs-lookup"><span data-stu-id="c2611-257">Integer value that sets the minimum number of characters required for the PIN.</span></span> <span data-ttu-id="c2611-258">El valor predeterminado es 4.</span><span class="sxs-lookup"><span data-stu-id="c2611-258">Default value is 4.</span></span> <span data-ttu-id="c2611-259">El número más bajo que se puede configurar para esta configuración de directiva es 4.</span><span class="sxs-lookup"><span data-stu-id="c2611-259">The lowest number you can configure for this policy setting is 4.</span></span> <span data-ttu-id="c2611-260">El número más alto que se puede configurar debe ser menor que el número establecido en la configuración de directiva de longitud máxima del PIN o el número 127, el que sea más bajo.</span><span class="sxs-lookup"><span data-stu-id="c2611-260">The largest number you can configure must be less than the number configured in the Maximum PIN length policy setting or the number 127, whichever is the lowest.</span></span>|
|<span data-ttu-id="c2611-261">pinUppercaseLetters</span><span class="sxs-lookup"><span data-stu-id="c2611-261">pinUppercaseLetters</span></span>|[<span data-ttu-id="c2611-262">windowsInformationProtectionPinCharacterRequirements</span><span class="sxs-lookup"><span data-stu-id="c2611-262">windowsInformationProtectionPinCharacterRequirements</span></span>](../resources/intune-mam-windowsinformationprotectionpincharacterrequirements.md)|<span data-ttu-id="c2611-263">Valor entero que configura el uso de mayúsculas en el PIN de Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="c2611-263">Integer value that configures the use of uppercase letters in the Windows Hello for Business PIN.</span></span> <span data-ttu-id="c2611-264">El valor predeterminado es NotAllow.</span><span class="sxs-lookup"><span data-stu-id="c2611-264">Default is NotAllow.</span></span> <span data-ttu-id="c2611-265">Los valores posibles son: `notAllow`, `requireAtLeastOne` y `allow`.</span><span class="sxs-lookup"><span data-stu-id="c2611-265">Possible values are: `notAllow`, `requireAtLeastOne`, `allow`.</span></span>|
|<span data-ttu-id="c2611-266">pinLowercaseLetters</span><span class="sxs-lookup"><span data-stu-id="c2611-266">pinLowercaseLetters</span></span>|[<span data-ttu-id="c2611-267">windowsInformationProtectionPinCharacterRequirements</span><span class="sxs-lookup"><span data-stu-id="c2611-267">windowsInformationProtectionPinCharacterRequirements</span></span>](../resources/intune-mam-windowsinformationprotectionpincharacterrequirements.md)|<span data-ttu-id="c2611-268">Valor entero que configura el uso de minúsculas en el PIN de Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="c2611-268">Integer value that configures the use of lowercase letters in the Windows Hello for Business PIN.</span></span> <span data-ttu-id="c2611-269">El valor predeterminado es NotAllow.</span><span class="sxs-lookup"><span data-stu-id="c2611-269">Default is NotAllow.</span></span> <span data-ttu-id="c2611-270">Los valores posibles son: `notAllow`, `requireAtLeastOne` y `allow`.</span><span class="sxs-lookup"><span data-stu-id="c2611-270">Possible values are: `notAllow`, `requireAtLeastOne`, `allow`.</span></span>|
|<span data-ttu-id="c2611-271">pinSpecialCharacters</span><span class="sxs-lookup"><span data-stu-id="c2611-271">pinSpecialCharacters</span></span>|[<span data-ttu-id="c2611-272">windowsInformationProtectionPinCharacterRequirements</span><span class="sxs-lookup"><span data-stu-id="c2611-272">windowsInformationProtectionPinCharacterRequirements</span></span>](../resources/intune-mam-windowsinformationprotectionpincharacterrequirements.md)|<span data-ttu-id="c2611-273">Valor entero que configura el uso de caracteres especiales en el PIN de Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="c2611-273">Integer value that configures the use of special characters in the Windows Hello for Business PIN.</span></span> <span data-ttu-id="c2611-274">Los caracteres especiales válidos para el PIN de Windows Hello para empresas incluyen: !</span><span class="sxs-lookup"><span data-stu-id="c2611-274">Valid special characters for Windows Hello for Business PIN gestures include: !</span></span> <span data-ttu-id="c2611-275">" # $ % & ' ( ) \* + , - .</span><span class="sxs-lookup"><span data-stu-id="c2611-275">" # $ % & ' ( ) \* + , - .</span></span> <span data-ttu-id="c2611-276">/ : ; < = > ?</span><span class="sxs-lookup"><span data-stu-id="c2611-276">/ : ; < = > ?</span></span><span data-ttu-id="c2611-277"> @ \[ \ \] ^ _ \` {</span><span class="sxs-lookup"><span data-stu-id="c2611-277"> @ \[ \ \] ^ _ \` {</span></span> | <span data-ttu-id="c2611-278">} ~.</span><span class="sxs-lookup"><span data-stu-id="c2611-278">} ~.</span></span> <span data-ttu-id="c2611-279">El valor predeterminado es NotAllow.</span><span class="sxs-lookup"><span data-stu-id="c2611-279">Default is NotAllow.</span></span> <span data-ttu-id="c2611-280">Los valores posibles son: `notAllow`, `requireAtLeastOne` y `allow`.</span><span class="sxs-lookup"><span data-stu-id="c2611-280">Possible values are: `notAllow`, `requireAtLeastOne`, `allow`.</span></span>|
|<span data-ttu-id="c2611-281">pinExpirationDays</span><span class="sxs-lookup"><span data-stu-id="c2611-281">pinExpirationDays</span></span>|<span data-ttu-id="c2611-282">Int32</span><span class="sxs-lookup"><span data-stu-id="c2611-282">Int32</span></span>|<span data-ttu-id="c2611-283">Valor entero que especifica el período de tiempo (en días) que se puede usar un PIN antes de que el sistema solicite que el usuario lo cambie.</span><span class="sxs-lookup"><span data-stu-id="c2611-283">Integer value specifies the period of time (in days) that a PIN can be used before the system requires the user to change it.</span></span> <span data-ttu-id="c2611-284">El número más alto que puede configurar para esta configuración de directiva es 730.</span><span class="sxs-lookup"><span data-stu-id="c2611-284">The largest number you can configure for this policy setting is 730.</span></span> <span data-ttu-id="c2611-285">El número más bajo que puede configurar para esta configuración de directiva es 0.</span><span class="sxs-lookup"><span data-stu-id="c2611-285">The lowest number you can configure for this policy setting is 0.</span></span> <span data-ttu-id="c2611-286">Si esta directiva se establece en 0, el PIN del usuario nunca expirará.</span><span class="sxs-lookup"><span data-stu-id="c2611-286">If this policy is set to 0, then the user's PIN will never expire.</span></span> <span data-ttu-id="c2611-287">Este nodo se agregó en Windows 10, versión 1511.</span><span class="sxs-lookup"><span data-stu-id="c2611-287">This node was added in Windows 10, version 1511.</span></span> <span data-ttu-id="c2611-288">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="c2611-288">Default is 0.</span></span>|
|<span data-ttu-id="c2611-289">numberOfPastPinsRemembered</span><span class="sxs-lookup"><span data-stu-id="c2611-289">numberOfPastPinsRemembered</span></span>|<span data-ttu-id="c2611-290">Int32</span><span class="sxs-lookup"><span data-stu-id="c2611-290">Int32</span></span>|<span data-ttu-id="c2611-291">Valor entero que especifica el número de PIN anteriores que se pueden asociar a una cuenta de usuario que no se pueden volver a usar.</span><span class="sxs-lookup"><span data-stu-id="c2611-291">Integer value that specifies the number of past PINs that can be associated to a user account that can't be reused.</span></span> <span data-ttu-id="c2611-292">El número más alto que puede configurar para esta configuración de directiva es 50.</span><span class="sxs-lookup"><span data-stu-id="c2611-292">The largest number you can configure for this policy setting is 50.</span></span> <span data-ttu-id="c2611-293">El número más bajo que puede configurar para esta configuración de directiva es 0.</span><span class="sxs-lookup"><span data-stu-id="c2611-293">The lowest number you can configure for this policy setting is 0.</span></span> <span data-ttu-id="c2611-294">Si esta directiva se establece en 0, no es necesario almacenar los PIN antiguos.</span><span class="sxs-lookup"><span data-stu-id="c2611-294">If this policy is set to 0, then storage of previous PINs is not required.</span></span> <span data-ttu-id="c2611-295">Este nodo se agregó en Windows 10, versión 1511.</span><span class="sxs-lookup"><span data-stu-id="c2611-295">This node was added in Windows 10, version 1511.</span></span> <span data-ttu-id="c2611-296">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="c2611-296">Default is 0.</span></span>|
|<span data-ttu-id="c2611-297">passwordMaximumAttemptCount</span><span class="sxs-lookup"><span data-stu-id="c2611-297">passwordMaximumAttemptCount</span></span>|<span data-ttu-id="c2611-298">Int32</span><span class="sxs-lookup"><span data-stu-id="c2611-298">Int32</span></span>|<span data-ttu-id="c2611-299">Número de errores de autenticación permitidos antes de que se borre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2611-299">The number of authentication failures allowed before the device will be wiped.</span></span> <span data-ttu-id="c2611-300">Un valor de 0 deshabilita la funcionalidad de borrado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2611-300">A value of 0 disables device wipe functionality.</span></span> <span data-ttu-id="c2611-301">El intervalo es un entero X donde 4 < = X < = 16 para equipos de escritorio y 0 < = X < = 999 para dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="c2611-301">Range is an integer X where 4 <= X <= 16 for desktop and 0 <= X <= 999 for mobile devices.</span></span>|
|<span data-ttu-id="c2611-302">minutesOfInactivityBeforeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="c2611-302">minutesOfInactivityBeforeDeviceLock</span></span>|<span data-ttu-id="c2611-303">Int32</span><span class="sxs-lookup"><span data-stu-id="c2611-303">Int32</span></span>|<span data-ttu-id="c2611-304">Especifica la cantidad máxima de tiempo (en minutos) permitida después de que el dispositivo esté inactivo que hará que el dispositivo esté bloqueado con PIN o contraseña.</span><span class="sxs-lookup"><span data-stu-id="c2611-304">Specifies the maximum amount of time (in minutes) allowed after the device is idle that will cause the device to become PIN or password locked.</span></span>   <span data-ttu-id="c2611-305">El intervalo es un entero X, donde 0 < = X < = 999.</span><span class="sxs-lookup"><span data-stu-id="c2611-305">Range is an integer X where 0 <= X <= 999.</span></span>|
|<span data-ttu-id="c2611-306">daysWithoutContactBeforeUnenroll</span><span class="sxs-lookup"><span data-stu-id="c2611-306">daysWithoutContactBeforeUnenroll</span></span>|<span data-ttu-id="c2611-307">Int32</span><span class="sxs-lookup"><span data-stu-id="c2611-307">Int32</span></span>|<span data-ttu-id="c2611-308">Intervalo sin conexión antes de que se borren los datos de la aplicación (días)</span><span class="sxs-lookup"><span data-stu-id="c2611-308">Offline interval before app data is wiped (days)</span></span> |



## <a name="response"></a><span data-ttu-id="c2611-309">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2611-309">Response</span></span>
<span data-ttu-id="c2611-310">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c2611-310">If successful, this method returns a `200 OK` response code and an updated [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c2611-311">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2611-311">Example</span></span>
### <a name="request"></a><span data-ttu-id="c2611-312">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2611-312">Request</span></span>
<span data-ttu-id="c2611-313">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c2611-313">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}
Content-type: application/json
Content-length: 4396

{
  "displayName": "Display Name value",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": "Version value",
  "enforcementLevel": "encryptAndAuditOnly",
  "enterpriseDomain": "Enterprise Domain value",
  "enterpriseProtectedDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "protectionUnderLockConfigRequired": true,
  "dataRecoveryCertificate": {
    "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
    "subjectName": "Subject Name value",
    "description": "Description value",
    "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
    "certificate": "Y2VydGlmaWNhdGU="
  },
  "revokeOnUnenrollDisabled": true,
  "rightsManagementServicesTemplateId": "abf7b16f-b16f-abf7-6fb1-f7ab6fb1f7ab",
  "azureRightsManagementServicesAllowed": true,
  "iconsVisible": true,
  "protectedApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisherName": "Publisher Name value",
      "productName": "Product Name value",
      "denied": true
    }
  ],
  "exemptApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisherName": "Publisher Name value",
      "productName": "Product Name value",
      "denied": true
    }
  ],
  "enterpriseNetworkDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseProxiedDomains": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionProxiedDomainCollection",
      "displayName": "Display Name value",
      "proxiedDomains": [
        {
          "@odata.type": "microsoft.graph.proxiedDomain",
          "ipAddressOrFQDN": "Ip Address Or FQDN value",
          "proxy": "Proxy value"
        }
      ]
    }
  ],
  "enterpriseIPRanges": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionIPRangeCollection",
      "displayName": "Display Name value",
      "ranges": [
        {
          "@odata.type": "microsoft.graph.iPv6Range",
          "lowerAddress": "Lower Address value",
          "upperAddress": "Upper Address value"
        }
      ]
    }
  ],
  "enterpriseIPRangesAreAuthoritative": true,
  "enterpriseProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseInternalProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseProxyServersAreAuthoritative": true,
  "neutralDomainResources": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "indexingEncryptedStoresOrItemsBlocked": true,
  "smbAutoEncryptedFileExtensions": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "isAssigned": true,
  "revokeOnMdmHandoffDisabled": true,
  "mdmEnrollmentUrl": "https://example.com/mdmEnrollmentUrl/",
  "windowsHelloForBusinessBlocked": true,
  "pinMinimumLength": 0,
  "pinUppercaseLetters": "requireAtLeastOne",
  "pinLowercaseLetters": "requireAtLeastOne",
  "pinSpecialCharacters": "requireAtLeastOne",
  "pinExpirationDays": 1,
  "numberOfPastPinsRemembered": 10,
  "passwordMaximumAttemptCount": 11,
  "minutesOfInactivityBeforeDeviceLock": 3,
  "daysWithoutContactBeforeUnenroll": 0
}
```

### <a name="response"></a><span data-ttu-id="c2611-314">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2611-314">Response</span></span>
<span data-ttu-id="c2611-p132">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c2611-p132">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 4577

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionPolicy",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "id": "6397be61-be61-6397-61be-976361be9763",
  "version": "Version value",
  "enforcementLevel": "encryptAndAuditOnly",
  "enterpriseDomain": "Enterprise Domain value",
  "enterpriseProtectedDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "protectionUnderLockConfigRequired": true,
  "dataRecoveryCertificate": {
    "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
    "subjectName": "Subject Name value",
    "description": "Description value",
    "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
    "certificate": "Y2VydGlmaWNhdGU="
  },
  "revokeOnUnenrollDisabled": true,
  "rightsManagementServicesTemplateId": "abf7b16f-b16f-abf7-6fb1-f7ab6fb1f7ab",
  "azureRightsManagementServicesAllowed": true,
  "iconsVisible": true,
  "protectedApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisherName": "Publisher Name value",
      "productName": "Product Name value",
      "denied": true
    }
  ],
  "exemptApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisherName": "Publisher Name value",
      "productName": "Product Name value",
      "denied": true
    }
  ],
  "enterpriseNetworkDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseProxiedDomains": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionProxiedDomainCollection",
      "displayName": "Display Name value",
      "proxiedDomains": [
        {
          "@odata.type": "microsoft.graph.proxiedDomain",
          "ipAddressOrFQDN": "Ip Address Or FQDN value",
          "proxy": "Proxy value"
        }
      ]
    }
  ],
  "enterpriseIPRanges": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionIPRangeCollection",
      "displayName": "Display Name value",
      "ranges": [
        {
          "@odata.type": "microsoft.graph.iPv6Range",
          "lowerAddress": "Lower Address value",
          "upperAddress": "Upper Address value"
        }
      ]
    }
  ],
  "enterpriseIPRangesAreAuthoritative": true,
  "enterpriseProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseInternalProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseProxyServersAreAuthoritative": true,
  "neutralDomainResources": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "indexingEncryptedStoresOrItemsBlocked": true,
  "smbAutoEncryptedFileExtensions": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "isAssigned": true,
  "revokeOnMdmHandoffDisabled": true,
  "mdmEnrollmentUrl": "https://example.com/mdmEnrollmentUrl/",
  "windowsHelloForBusinessBlocked": true,
  "pinMinimumLength": 0,
  "pinUppercaseLetters": "requireAtLeastOne",
  "pinLowercaseLetters": "requireAtLeastOne",
  "pinSpecialCharacters": "requireAtLeastOne",
  "pinExpirationDays": 1,
  "numberOfPastPinsRemembered": 10,
  "passwordMaximumAttemptCount": 11,
  "minutesOfInactivityBeforeDeviceLock": 3,
  "daysWithoutContactBeforeUnenroll": 0
}
```






---
title: Actualizar windowsInformationProtectionPolicy
description: Actualice las propiedades de un objeto windowsInformationProtectionPolicy.
ms.openlocfilehash: 15fc74d9f5155fdda9513812ab0dbbdb6770c879
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032234"
---
# <a name="update-windowsinformationprotectionpolicy"></a><span data-ttu-id="d5a65-103">Actualizar windowsInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d5a65-103">Update windowsInformationProtectionPolicy</span></span>

> <span data-ttu-id="d5a65-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d5a65-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d5a65-105">Actualice las propiedades de un objeto [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-105">Update the properties of a [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d5a65-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d5a65-106">Prerequisites</span></span>
<span data-ttu-id="d5a65-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d5a65-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d5a65-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d5a65-109">Permission type</span></span>|<span data-ttu-id="d5a65-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d5a65-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d5a65-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d5a65-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d5a65-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d5a65-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="d5a65-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d5a65-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d5a65-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d5a65-114">Not supported.</span></span>|
|<span data-ttu-id="d5a65-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d5a65-115">Application</span></span>|<span data-ttu-id="d5a65-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d5a65-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d5a65-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d5a65-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="d5a65-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d5a65-118">Request headers</span></span>
|<span data-ttu-id="d5a65-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5a65-119">Header</span></span>|<span data-ttu-id="d5a65-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d5a65-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d5a65-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="d5a65-121">Authorization</span></span>|<span data-ttu-id="d5a65-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d5a65-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d5a65-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d5a65-123">Accept</span></span>|<span data-ttu-id="d5a65-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d5a65-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d5a65-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d5a65-125">Request body</span></span>
<span data-ttu-id="d5a65-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-126">In the request body, supply a JSON representation for the [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md) object.</span></span>

<span data-ttu-id="d5a65-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-127">The following table shows the properties that are required when you create the [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md).</span></span>

|<span data-ttu-id="d5a65-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d5a65-128">Property</span></span>|<span data-ttu-id="d5a65-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d5a65-129">Type</span></span>|<span data-ttu-id="d5a65-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5a65-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d5a65-131">displayName</span><span class="sxs-lookup"><span data-stu-id="d5a65-131">displayName</span></span>|<span data-ttu-id="d5a65-132">String</span><span class="sxs-lookup"><span data-stu-id="d5a65-132">String</span></span>|<span data-ttu-id="d5a65-133">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="d5a65-133">Policy display name.</span></span> <span data-ttu-id="d5a65-134">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-134">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="d5a65-135">descripción</span><span class="sxs-lookup"><span data-stu-id="d5a65-135">description</span></span>|<span data-ttu-id="d5a65-136">String</span><span class="sxs-lookup"><span data-stu-id="d5a65-136">String</span></span>|<span data-ttu-id="d5a65-137">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="d5a65-137">The policy's description.</span></span> <span data-ttu-id="d5a65-138">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-138">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="d5a65-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d5a65-139">createdDateTime</span></span>|<span data-ttu-id="d5a65-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d5a65-140">DateTimeOffset</span></span>|<span data-ttu-id="d5a65-141">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="d5a65-141">The date and time the policy was created.</span></span> <span data-ttu-id="d5a65-142">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-142">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="d5a65-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d5a65-143">lastModifiedDateTime</span></span>|<span data-ttu-id="d5a65-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d5a65-144">DateTimeOffset</span></span>|<span data-ttu-id="d5a65-145">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="d5a65-145">Last time the policy was modified.</span></span> <span data-ttu-id="d5a65-146">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-146">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="d5a65-147">id</span><span class="sxs-lookup"><span data-stu-id="d5a65-147">id</span></span>|<span data-ttu-id="d5a65-148">String</span><span class="sxs-lookup"><span data-stu-id="d5a65-148">String</span></span>|<span data-ttu-id="d5a65-149">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d5a65-149">Key of the entity.</span></span> <span data-ttu-id="d5a65-150">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-150">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="d5a65-151">version</span><span class="sxs-lookup"><span data-stu-id="d5a65-151">version</span></span>|<span data-ttu-id="d5a65-152">String</span><span class="sxs-lookup"><span data-stu-id="d5a65-152">String</span></span>|<span data-ttu-id="d5a65-153">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d5a65-153">Version of the entity.</span></span> <span data-ttu-id="d5a65-154">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-154">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="d5a65-155">enforcementLevel</span><span class="sxs-lookup"><span data-stu-id="d5a65-155">enforcementLevel</span></span>|[<span data-ttu-id="d5a65-156">windowsInformationProtectionEnforcementLevel</span><span class="sxs-lookup"><span data-stu-id="d5a65-156">windowsInformationProtectionEnforcementLevel</span></span>](../resources/intune-mam-windowsinformationprotectionenforcementlevel.md)|<span data-ttu-id="d5a65-157">Nivel de aplicación de trabajo en curso. Vea la definición de enumeración para los valores admitidos Inherited desde [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-157">WIP enforcement level.See the Enum definition for supported values Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span></span> <span data-ttu-id="d5a65-158">Los valores posibles son: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt` y `encryptAuditAndBlock`.</span><span class="sxs-lookup"><span data-stu-id="d5a65-158">Possible values are: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt`, `encryptAuditAndBlock`.</span></span>|
|<span data-ttu-id="d5a65-159">enterpriseDomain</span><span class="sxs-lookup"><span data-stu-id="d5a65-159">enterpriseDomain</span></span>|<span data-ttu-id="d5a65-160">String</span><span class="sxs-lookup"><span data-stu-id="d5a65-160">String</span></span>|<span data-ttu-id="d5a65-161">Dominio empresarial principal. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-161">Primary enterprise domain Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-162">enterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="d5a65-162">enterpriseProtectedDomainNames</span></span>|<span data-ttu-id="d5a65-163">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="d5a65-163">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="d5a65-164">Lista de dominios de empresa que se van a proteger. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-164">List of enterprise domains to be protected Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-165">protectionUnderLockConfigRequired</span><span class="sxs-lookup"><span data-stu-id="d5a65-165">protectionUnderLockConfigRequired</span></span>|<span data-ttu-id="d5a65-166">Booleano</span><span class="sxs-lookup"><span data-stu-id="d5a65-166">Boolean</span></span>|<span data-ttu-id="d5a65-167">Especifica si es necesario configurar la protección en la característica de bloqueo (también conocida como cifrar con PIN). Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-167">Specifies whether the protection under lock feature (also known as encrypt under pin) should be configured Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-168">dataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="d5a65-168">dataRecoveryCertificate</span></span>|[<span data-ttu-id="d5a65-169">windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="d5a65-169">windowsInformationProtectionDataRecoveryCertificate</span></span>](../resources/intune-mam-windowsinformationprotectiondatarecoverycertificate.md)|<span data-ttu-id="d5a65-170">Especifica un certificado de recuperación que se puede usar para recuperar datos de archivos cifrados.</span><span class="sxs-lookup"><span data-stu-id="d5a65-170">Specifies a recovery certificate that can be used for data recovery of encrypted files.</span></span> <span data-ttu-id="d5a65-171">Es igual al certificado del agente de recuperación de datos (DRA) para el sistema de cifrado de archivos (EFS). Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="d5a65-171">This is the same as the data recovery agent(DRA) certificate for encrypting file system(EFS) Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-172">revokeOnUnenrollDisabled</span><span class="sxs-lookup"><span data-stu-id="d5a65-172">revokeOnUnenrollDisabled</span></span>|<span data-ttu-id="d5a65-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="d5a65-173">Boolean</span></span>|<span data-ttu-id="d5a65-174">Esta directiva controla si se revocan las claves de trabajo en curso cuando se anula la inscripción de un dispositivo en el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="d5a65-174">This policy controls whether to revoke the WIP keys when a device unenrolls from the management service.</span></span> <span data-ttu-id="d5a65-175">Si se establece en 1 (no revocar las claves), no se revocarán las claves y el usuario seguirá teniendo acceso a archivos protegidos después de anular la inscripción.</span><span class="sxs-lookup"><span data-stu-id="d5a65-175">If set to 1 (Don't revoke keys), the keys will not be revoked and the user will continue to have access to protected files after unenrollment.</span></span> <span data-ttu-id="d5a65-176">Si no se revocan las claves, no habrá ninguna limpieza de archivos revocados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="d5a65-176">If the keys are not revoked, there will be no revoked file cleanup subsequently.</span></span> <span data-ttu-id="d5a65-177">Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="d5a65-177">Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-178">rightsManagementServicesTemplateId</span><span class="sxs-lookup"><span data-stu-id="d5a65-178">rightsManagementServicesTemplateId</span></span>|<span data-ttu-id="d5a65-179">Guid</span><span class="sxs-lookup"><span data-stu-id="d5a65-179">Guid</span></span>|<span data-ttu-id="d5a65-180">GUID de TemplateID que se va a usar para el cifrado RMS.</span><span class="sxs-lookup"><span data-stu-id="d5a65-180">TemplateID GUID to use for RMS encryption.</span></span> <span data-ttu-id="d5a65-181">La plantilla de RMS permite que el administrador de TI configure los detalles sobre quién tiene acceso a los archivos protegidos por RMS y durante cuánto tiempo. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-181">The RMS template allows the IT admin to configure the details about who has access to RMS-protected file and how long they have access Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-182">azureRightsManagementServicesAllowed</span><span class="sxs-lookup"><span data-stu-id="d5a65-182">azureRightsManagementServicesAllowed</span></span>|<span data-ttu-id="d5a65-183">Booleano</span><span class="sxs-lookup"><span data-stu-id="d5a65-183">Boolean</span></span>|<span data-ttu-id="d5a65-184">Especifica si se permite el cifrado de Azure RMS para WIP. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-184">Specifies whether to allow Azure RMS encryption for WIP Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-185">iconsVisible</span><span class="sxs-lookup"><span data-stu-id="d5a65-185">iconsVisible</span></span>|<span data-ttu-id="d5a65-186">Booleano</span><span class="sxs-lookup"><span data-stu-id="d5a65-186">Boolean</span></span>|<span data-ttu-id="d5a65-187">Determina si se agregan las superposiciones a los iconos para los archivos protegidos mediante WIP en Explorer y en los iconos de aplicación solo de empresa en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="d5a65-187">Determines whether overlays are added to icons for WIP protected files in Explorer and enterprise only app tiles in the Start menu.</span></span> <span data-ttu-id="d5a65-188">A partir de Windows 10, versión 1703, estos ajustes también configuran la visibilidad del icono de WIP en la barra de título de una aplicación protegida mediante WIP. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-188">Starting in Windows 10, version 1703 this setting also configures the visibility of the WIP icon in the title bar of a WIP-protected app Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-189">protectedApps</span><span class="sxs-lookup"><span data-stu-id="d5a65-189">protectedApps</span></span>|<span data-ttu-id="d5a65-190">Colección [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="d5a65-190">[windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="d5a65-191">Las aplicaciones protegidas pueden tener acceso a datos empresariales y los datos controlados por dichas aplicaciones están protegidos mediante cifrado. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-191">Protected applications can access enterprise data and the data handled by those applications are protected with encryption Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-192">exemptApps</span><span class="sxs-lookup"><span data-stu-id="d5a65-192">exemptApps</span></span>|<span data-ttu-id="d5a65-193">Colección [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="d5a65-193">[windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="d5a65-194">Las aplicaciones exentas también pueden tener acceso a datos empresariales, pero los datos controlados por dichas aplicaciones no están protegidos.</span><span class="sxs-lookup"><span data-stu-id="d5a65-194">Exempt applications can also access enterprise data, but the data handled by those applications are not protected.</span></span> <span data-ttu-id="d5a65-195">Esto ocurre porque algunas aplicaciones empresariales críticas podrían tener problemas de compatibilidad con los datos cifrados.</span><span class="sxs-lookup"><span data-stu-id="d5a65-195">This is because some critical enterprise applications may have compatibility problems with encrypted data.</span></span> <span data-ttu-id="d5a65-196">Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="d5a65-196">Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-197">enterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="d5a65-197">enterpriseNetworkDomainNames</span></span>|<span data-ttu-id="d5a65-198">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="d5a65-198">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="d5a65-199">Esta es la lista de dominios que forman parte de los límites de la empresa.</span><span class="sxs-lookup"><span data-stu-id="d5a65-199">This is the list of domains that comprise the boundaries of the enterprise.</span></span> <span data-ttu-id="d5a65-200">Los datos de uno de estos dominios que se envíen a un dispositivo se considerarán datos empresariales y protegidos. Estas ubicaciones se consideran un destino seguro con el que compartir datos empresariales. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-200">Data from one of these domains that is sent to a device will be considered enterprise data and protected These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-201">enterpriseProxiedDomains</span><span class="sxs-lookup"><span data-stu-id="d5a65-201">enterpriseProxiedDomains</span></span>|<span data-ttu-id="d5a65-202">Colección [windowsInformationProtectionProxiedDomainCollection](../resources/intune-mam-windowsinformationprotectionproxieddomaincollection.md)</span><span class="sxs-lookup"><span data-stu-id="d5a65-202">[windowsInformationProtectionProxiedDomainCollection](../resources/intune-mam-windowsinformationprotectionproxieddomaincollection.md) collection</span></span>|<span data-ttu-id="d5a65-203">Contiene una lista de dominios de recursos empresariales hospedados en la nube que necesitan protección.</span><span class="sxs-lookup"><span data-stu-id="d5a65-203">Contains a list of Enterprise resource domains hosted in the cloud that need to be protected.</span></span> <span data-ttu-id="d5a65-204">Las conexiones a estos recursos se consideran datos empresariales.</span><span class="sxs-lookup"><span data-stu-id="d5a65-204">Connections to these resources are considered enterprise data.</span></span> <span data-ttu-id="d5a65-205">Si un proxy se corresponde con un recurso de nube, el tráfico al recurso de la nube se dirigirá a través de la red empresarial mediante el servidor proxy indicado (en el puerto 80).</span><span class="sxs-lookup"><span data-stu-id="d5a65-205">If a proxy is paired with a cloud resource, traffic to the cloud resource will be routed through the enterprise network via the denoted proxy server (on Port 80).</span></span> <span data-ttu-id="d5a65-206">Un servidor proxy que se use con esta finalidad debe configurarse también mediante la directiva EnterpriseInternalProxyServers. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-206">A proxy server used for this purpose must also be configured using the EnterpriseInternalProxyServers policy Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-207">enterpriseIPRanges</span><span class="sxs-lookup"><span data-stu-id="d5a65-207">enterpriseIPRanges</span></span>|<span data-ttu-id="d5a65-208">Colección [windowsInformationProtectionIPRangeCollection](../resources/intune-mam-windowsinformationprotectioniprangecollection.md)</span><span class="sxs-lookup"><span data-stu-id="d5a65-208">[windowsInformationProtectionIPRangeCollection](../resources/intune-mam-windowsinformationprotectioniprangecollection.md) collection</span></span>|<span data-ttu-id="d5a65-209">Establece los intervalos IP empresariales que definen los equipos de la red empresarial.</span><span class="sxs-lookup"><span data-stu-id="d5a65-209">Sets the enterprise IP ranges that define the computers in the enterprise network.</span></span> <span data-ttu-id="d5a65-210">Los datos que provienen de dichos equipos se consideran parte de la empresa y están protegidos.</span><span class="sxs-lookup"><span data-stu-id="d5a65-210">Data that comes from those computers will be considered part of the enterprise and protected.</span></span> <span data-ttu-id="d5a65-211">Estas ubicaciones se consideran un destino seguro en el que compartir datos empresariales. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-211">These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-212">enterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="d5a65-212">enterpriseIPRangesAreAuthoritative</span></span>|<span data-ttu-id="d5a65-213">Booleano</span><span class="sxs-lookup"><span data-stu-id="d5a65-213">Boolean</span></span>|<span data-ttu-id="d5a65-214">Valor booleano que indica al cliente que acepte la lista configurada y que no use la heurística para intentar buscar otras subredes.</span><span class="sxs-lookup"><span data-stu-id="d5a65-214">Boolean value that tells the client to accept the configured list and not to use heuristics to attempt to find other subnets.</span></span> <span data-ttu-id="d5a65-215">El valor predeterminado es False. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-215">Default is false Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-216">enterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="d5a65-216">enterpriseProxyServers</span></span>|<span data-ttu-id="d5a65-217">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="d5a65-217">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="d5a65-218">Esta es una lista de servidores proxy.</span><span class="sxs-lookup"><span data-stu-id="d5a65-218">This is a list of proxy servers.</span></span> <span data-ttu-id="d5a65-219">Cualquier servidor que no esté en esta lista se considera no empresarial. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-219">Any server not on this list is considered non-enterprise Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-220">enterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="d5a65-220">enterpriseInternalProxyServers</span></span>|<span data-ttu-id="d5a65-221">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="d5a65-221">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="d5a65-222">Se trata de la lista de valores separados por comas de servidores proxy internos.</span><span class="sxs-lookup"><span data-stu-id="d5a65-222">This is the comma-separated list of internal proxy servers.</span></span> <span data-ttu-id="d5a65-223">Por ejemplo, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span><span class="sxs-lookup"><span data-stu-id="d5a65-223">For example, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span></span> <span data-ttu-id="d5a65-224">El administrador ha configurado estos servidores proxy para que se conecten a los recursos específicos de Internet.</span><span class="sxs-lookup"><span data-stu-id="d5a65-224">These proxies have been configured by the admin to connect to specific resources on the Internet.</span></span> <span data-ttu-id="d5a65-225">Se consideran ubicaciones de red empresarial.</span><span class="sxs-lookup"><span data-stu-id="d5a65-225">They are considered to be enterprise network locations.</span></span> <span data-ttu-id="d5a65-226">Los servidores proxy solo se usan al configurar la directiva EnterpriseProxiedDomains para forzar el tráfico a los dominios coincidentes mediante estos proxy. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-226">The proxies are only leveraged in configuring the EnterpriseProxiedDomains policy to force traffic to the matched domains through these proxies Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-227">enterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="d5a65-227">enterpriseProxyServersAreAuthoritative</span></span>|<span data-ttu-id="d5a65-228">Booleano</span><span class="sxs-lookup"><span data-stu-id="d5a65-228">Boolean</span></span>|<span data-ttu-id="d5a65-229">Valor booleano que indica al cliente que acepte la lista de configuración de servidores proxy y no intente detectar otros servidores proxy de trabajo.</span><span class="sxs-lookup"><span data-stu-id="d5a65-229">Boolean value that tells the client to accept the configured list of proxies and not try to detect other work proxies.</span></span> <span data-ttu-id="d5a65-230">El valor predeterminado es False. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-230">Default is false Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-231">neutralDomainResources</span><span class="sxs-lookup"><span data-stu-id="d5a65-231">neutralDomainResources</span></span>|<span data-ttu-id="d5a65-232">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="d5a65-232">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="d5a65-233">Lista de nombres de dominio que se pueden usar para el recurso de trabajo o personal. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-233">List of domain names that can used for work or personal resource Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-234">indexingEncryptedStoresOrItemsBlocked</span><span class="sxs-lookup"><span data-stu-id="d5a65-234">indexingEncryptedStoresOrItemsBlocked</span></span>|<span data-ttu-id="d5a65-235">Booleano</span><span class="sxs-lookup"><span data-stu-id="d5a65-235">Boolean</span></span>|<span data-ttu-id="d5a65-236">Este identificador es para que el indexador de Windows Search permita o impida la indexación de los elementos. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-236">This switch is for the Windows Search Indexer, to allow or disallow indexing of items Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-237">smbAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="d5a65-237">smbAutoEncryptedFileExtensions</span></span>|<span data-ttu-id="d5a65-238">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="d5a65-238">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="d5a65-239">Especifica una lista de extensiones de archivo, para que los archivos con estas extensiones se cifren cuando se copian desde un recurso compartido de SMB dentro del límite de la empresa. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="d5a65-239">Specifies a list of file extensions, so that files with these extensions are encrypted when copying from an SMB share within the corporate boundary Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-240">isAssigned</span><span class="sxs-lookup"><span data-stu-id="d5a65-240">isAssigned</span></span>|<span data-ttu-id="d5a65-241">Booleano</span><span class="sxs-lookup"><span data-stu-id="d5a65-241">Boolean</span></span>|<span data-ttu-id="d5a65-242">Indica si la directiva se implementará en los grupos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="d5a65-242">Indicates if the policy is deployed to any inclusion groups or not.</span></span> <span data-ttu-id="d5a65-243">Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="d5a65-243">Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d5a65-244">revokeOnMdmHandoffDisabled</span><span class="sxs-lookup"><span data-stu-id="d5a65-244">revokeOnMdmHandoffDisabled</span></span>|<span data-ttu-id="d5a65-245">Booleano</span><span class="sxs-lookup"><span data-stu-id="d5a65-245">Boolean</span></span>|<span data-ttu-id="d5a65-246">Nueva propiedad en RS2, pendiente de documentación.</span><span class="sxs-lookup"><span data-stu-id="d5a65-246">New property in RS2, pending documentation</span></span>|
|<span data-ttu-id="d5a65-247">mdmEnrollmentUrl</span><span class="sxs-lookup"><span data-stu-id="d5a65-247">mdmEnrollmentUrl</span></span>|<span data-ttu-id="d5a65-248">String</span><span class="sxs-lookup"><span data-stu-id="d5a65-248">String</span></span>|<span data-ttu-id="d5a65-249">Dirección URL de la inscripción para MDM.</span><span class="sxs-lookup"><span data-stu-id="d5a65-249">Enrollment url for the MDM</span></span>|
|<span data-ttu-id="d5a65-250">windowsHelloForBusinessBlocked</span><span class="sxs-lookup"><span data-stu-id="d5a65-250">windowsHelloForBusinessBlocked</span></span>|<span data-ttu-id="d5a65-251">Booleano</span><span class="sxs-lookup"><span data-stu-id="d5a65-251">Boolean</span></span>|<span data-ttu-id="d5a65-252">Valor booleano que establece Windows Hello para empresas como método de inicio de sesión en Windows.</span><span class="sxs-lookup"><span data-stu-id="d5a65-252">Boolean value that sets Windows Hello for Business as a method for signing into Windows.</span></span>|
|<span data-ttu-id="d5a65-253">pinMinimumLength</span><span class="sxs-lookup"><span data-stu-id="d5a65-253">pinMinimumLength</span></span>|<span data-ttu-id="d5a65-254">Int32</span><span class="sxs-lookup"><span data-stu-id="d5a65-254">Int32</span></span>|<span data-ttu-id="d5a65-255">Valor entero que establece el número mínimo de caracteres necesarios para el PIN.</span><span class="sxs-lookup"><span data-stu-id="d5a65-255">Integer value that sets the minimum number of characters required for the PIN.</span></span> <span data-ttu-id="d5a65-256">El valor predeterminado es 4.</span><span class="sxs-lookup"><span data-stu-id="d5a65-256">Default value is 4.</span></span> <span data-ttu-id="d5a65-257">El número más bajo que se puede configurar para esta configuración de directiva es 4.</span><span class="sxs-lookup"><span data-stu-id="d5a65-257">The lowest number you can configure for this policy setting is 4.</span></span> <span data-ttu-id="d5a65-258">El número más alto que se puede configurar debe ser menor que el número establecido en la configuración de directiva de longitud máxima del PIN o el número 127, el que sea más bajo.</span><span class="sxs-lookup"><span data-stu-id="d5a65-258">The largest number you can configure must be less than the number configured in the Maximum PIN length policy setting or the number 127, whichever is the lowest.</span></span>|
|<span data-ttu-id="d5a65-259">pinUppercaseLetters</span><span class="sxs-lookup"><span data-stu-id="d5a65-259">pinUppercaseLetters</span></span>|[<span data-ttu-id="d5a65-260">windowsInformationProtectionPinCharacterRequirements</span><span class="sxs-lookup"><span data-stu-id="d5a65-260">windowsInformationProtectionPinCharacterRequirements</span></span>](../resources/intune-mam-windowsinformationprotectionpincharacterrequirements.md)|<span data-ttu-id="d5a65-261">Valor entero que configura el uso de mayúsculas en el PIN de Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="d5a65-261">Integer value that configures the use of uppercase letters in the Windows Hello for Business PIN.</span></span> <span data-ttu-id="d5a65-262">El valor predeterminado es NotAllow.</span><span class="sxs-lookup"><span data-stu-id="d5a65-262">Default is NotAllow.</span></span> <span data-ttu-id="d5a65-263">Los valores posibles son: `notAllow`, `requireAtLeastOne` y `allow`.</span><span class="sxs-lookup"><span data-stu-id="d5a65-263">Possible values are: `notAllow`, `requireAtLeastOne`, `allow`.</span></span>|
|<span data-ttu-id="d5a65-264">pinLowercaseLetters</span><span class="sxs-lookup"><span data-stu-id="d5a65-264">pinLowercaseLetters</span></span>|[<span data-ttu-id="d5a65-265">windowsInformationProtectionPinCharacterRequirements</span><span class="sxs-lookup"><span data-stu-id="d5a65-265">windowsInformationProtectionPinCharacterRequirements</span></span>](../resources/intune-mam-windowsinformationprotectionpincharacterrequirements.md)|<span data-ttu-id="d5a65-266">Valor entero que configura el uso de minúsculas en el PIN de Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="d5a65-266">Integer value that configures the use of lowercase letters in the Windows Hello for Business PIN.</span></span> <span data-ttu-id="d5a65-267">El valor predeterminado es NotAllow.</span><span class="sxs-lookup"><span data-stu-id="d5a65-267">Default is NotAllow.</span></span> <span data-ttu-id="d5a65-268">Los valores posibles son: `notAllow`, `requireAtLeastOne` y `allow`.</span><span class="sxs-lookup"><span data-stu-id="d5a65-268">Possible values are: `notAllow`, `requireAtLeastOne`, `allow`.</span></span>|
|<span data-ttu-id="d5a65-269">pinSpecialCharacters</span><span class="sxs-lookup"><span data-stu-id="d5a65-269">pinSpecialCharacters</span></span>|[<span data-ttu-id="d5a65-270">windowsInformationProtectionPinCharacterRequirements</span><span class="sxs-lookup"><span data-stu-id="d5a65-270">windowsInformationProtectionPinCharacterRequirements</span></span>](../resources/intune-mam-windowsinformationprotectionpincharacterrequirements.md)|<span data-ttu-id="d5a65-271">Valor entero que configura el uso de caracteres especiales en el PIN de Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="d5a65-271">Integer value that configures the use of special characters in the Windows Hello for Business PIN.</span></span> <span data-ttu-id="d5a65-272">Los caracteres especiales válidos para el PIN de Windows Hello para empresas incluyen: !</span><span class="sxs-lookup"><span data-stu-id="d5a65-272">Valid special characters for Windows Hello for Business PIN gestures include: !</span></span> <span data-ttu-id="d5a65-273">" # $ % & ' ( ) \* + , - .</span><span class="sxs-lookup"><span data-stu-id="d5a65-273">" # $ % & ' ( ) \* + , - .</span></span> <span data-ttu-id="d5a65-274">/ : ; < = > ?</span><span class="sxs-lookup"><span data-stu-id="d5a65-274">/ : ; < = > ?</span></span><span data-ttu-id="d5a65-275"> @ \[ \ \] ^ _ \` {</span><span class="sxs-lookup"><span data-stu-id="d5a65-275"> @ \[ \ \] ^ _ \` {</span></span> | <span data-ttu-id="d5a65-276">} ~.</span><span class="sxs-lookup"><span data-stu-id="d5a65-276">} ~.</span></span> <span data-ttu-id="d5a65-277">El valor predeterminado es NotAllow.</span><span class="sxs-lookup"><span data-stu-id="d5a65-277">Default is NotAllow.</span></span> <span data-ttu-id="d5a65-278">Los valores posibles son: `notAllow`, `requireAtLeastOne` y `allow`.</span><span class="sxs-lookup"><span data-stu-id="d5a65-278">Possible values are: `notAllow`, `requireAtLeastOne`, `allow`.</span></span>|
|<span data-ttu-id="d5a65-279">pinExpirationDays</span><span class="sxs-lookup"><span data-stu-id="d5a65-279">pinExpirationDays</span></span>|<span data-ttu-id="d5a65-280">Int32</span><span class="sxs-lookup"><span data-stu-id="d5a65-280">Int32</span></span>|<span data-ttu-id="d5a65-281">Valor entero que especifica el período de tiempo (en días) que se puede usar un PIN antes de que el sistema solicite que el usuario lo cambie.</span><span class="sxs-lookup"><span data-stu-id="d5a65-281">Integer value specifies the period of time (in days) that a PIN can be used before the system requires the user to change it.</span></span> <span data-ttu-id="d5a65-282">El número más alto que puede configurar para esta configuración de directiva es 730.</span><span class="sxs-lookup"><span data-stu-id="d5a65-282">The largest number you can configure for this policy setting is 730.</span></span> <span data-ttu-id="d5a65-283">El número más bajo que puede configurar para esta configuración de directiva es 0.</span><span class="sxs-lookup"><span data-stu-id="d5a65-283">The lowest number you can configure for this policy setting is 0.</span></span> <span data-ttu-id="d5a65-284">Si esta directiva se establece en 0, el PIN del usuario nunca expirará.</span><span class="sxs-lookup"><span data-stu-id="d5a65-284">If this policy is set to 0, then the user's PIN will never expire.</span></span> <span data-ttu-id="d5a65-285">Este nodo se agregó en Windows 10, versión 1511.</span><span class="sxs-lookup"><span data-stu-id="d5a65-285">This node was added in Windows 10, version 1511.</span></span> <span data-ttu-id="d5a65-286">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="d5a65-286">Default is 0.</span></span>|
|<span data-ttu-id="d5a65-287">numberOfPastPinsRemembered</span><span class="sxs-lookup"><span data-stu-id="d5a65-287">numberOfPastPinsRemembered</span></span>|<span data-ttu-id="d5a65-288">Int32</span><span class="sxs-lookup"><span data-stu-id="d5a65-288">Int32</span></span>|<span data-ttu-id="d5a65-289">Valor entero que especifica el número de PIN anteriores que se pueden asociar a una cuenta de usuario que no se pueden volver a usar.</span><span class="sxs-lookup"><span data-stu-id="d5a65-289">Integer value that specifies the number of past PINs that can be associated to a user account that can't be reused.</span></span> <span data-ttu-id="d5a65-290">El número más alto que puede configurar para esta configuración de directiva es 50.</span><span class="sxs-lookup"><span data-stu-id="d5a65-290">The largest number you can configure for this policy setting is 50.</span></span> <span data-ttu-id="d5a65-291">El número más bajo que puede configurar para esta configuración de directiva es 0.</span><span class="sxs-lookup"><span data-stu-id="d5a65-291">The lowest number you can configure for this policy setting is 0.</span></span> <span data-ttu-id="d5a65-292">Si esta directiva se establece en 0, no es necesario almacenar los PIN antiguos.</span><span class="sxs-lookup"><span data-stu-id="d5a65-292">If this policy is set to 0, then storage of previous PINs is not required.</span></span> <span data-ttu-id="d5a65-293">Este nodo se agregó en Windows 10, versión 1511.</span><span class="sxs-lookup"><span data-stu-id="d5a65-293">This node was added in Windows 10, version 1511.</span></span> <span data-ttu-id="d5a65-294">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="d5a65-294">Default is 0.</span></span>|
|<span data-ttu-id="d5a65-295">passwordMaximumAttemptCount</span><span class="sxs-lookup"><span data-stu-id="d5a65-295">passwordMaximumAttemptCount</span></span>|<span data-ttu-id="d5a65-296">Int32</span><span class="sxs-lookup"><span data-stu-id="d5a65-296">Int32</span></span>|<span data-ttu-id="d5a65-297">Número de errores de autenticación permitidos antes de que se borre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5a65-297">The number of authentication failures allowed before the device will be wiped.</span></span> <span data-ttu-id="d5a65-298">Un valor de 0 deshabilita la funcionalidad de borrado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5a65-298">A value of 0 disables device wipe functionality.</span></span> <span data-ttu-id="d5a65-299">El intervalo es un entero X donde 4 < = X < = 16 para equipos de escritorio y 0 < = X < = 999 para dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="d5a65-299">Range is an integer X where 4 <= X <= 16 for desktop and 0 <= X <= 999 for mobile devices.</span></span>|
|<span data-ttu-id="d5a65-300">minutesOfInactivityBeforeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="d5a65-300">minutesOfInactivityBeforeDeviceLock</span></span>|<span data-ttu-id="d5a65-301">Int32</span><span class="sxs-lookup"><span data-stu-id="d5a65-301">Int32</span></span>|<span data-ttu-id="d5a65-302">Especifica la cantidad máxima de tiempo (en minutos) permitida después de que el dispositivo esté inactivo que hará que el dispositivo esté bloqueado con PIN o contraseña.</span><span class="sxs-lookup"><span data-stu-id="d5a65-302">Specifies the maximum amount of time (in minutes) allowed after the device is idle that will cause the device to become PIN or password locked.</span></span>   <span data-ttu-id="d5a65-303">El intervalo es un entero X, donde 0 < = X < = 999.</span><span class="sxs-lookup"><span data-stu-id="d5a65-303">Range is an integer X where 0 <= X <= 999.</span></span>|
|<span data-ttu-id="d5a65-304">daysWithoutContactBeforeUnenroll</span><span class="sxs-lookup"><span data-stu-id="d5a65-304">daysWithoutContactBeforeUnenroll</span></span>|<span data-ttu-id="d5a65-305">Int32</span><span class="sxs-lookup"><span data-stu-id="d5a65-305">Int32</span></span>|<span data-ttu-id="d5a65-306">Intervalo sin conexión antes de que se borren los datos de la aplicación (días)</span><span class="sxs-lookup"><span data-stu-id="d5a65-306">Offline interval before app data is wiped (days)</span></span> |



## <a name="response"></a><span data-ttu-id="d5a65-307">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d5a65-307">Response</span></span>
<span data-ttu-id="d5a65-308">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d5a65-308">If successful, this method returns a `200 OK` response code and an updated [windowsInformationProtectionPolicy](../resources/intune-mam-windowsinformationprotectionpolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d5a65-309">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d5a65-309">Example</span></span>
### <a name="request"></a><span data-ttu-id="d5a65-310">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d5a65-310">Request</span></span>
<span data-ttu-id="d5a65-311">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d5a65-311">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}
Content-type: application/json
Content-length: 4405

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionPolicy",
  "displayName": "Display Name value",
  "description": "Description value",
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

### <a name="response"></a><span data-ttu-id="d5a65-312">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d5a65-312">Response</span></span>
<span data-ttu-id="d5a65-p131">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d5a65-p131">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




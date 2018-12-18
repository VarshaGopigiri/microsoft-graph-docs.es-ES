---
title: Actualizar mdmWindowsInformationProtectionPolicy
description: Actualice las propiedades de un objeto mdmWindowsInformationProtectionPolicy.
author: tfitzmac
ms.openlocfilehash: e4b05831f91336cb5adafb6840b77a2120e6a42b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308634"
---
# <a name="update-mdmwindowsinformationprotectionpolicy"></a><span data-ttu-id="98d49-103">Actualizar mdmWindowsInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="98d49-103">Update mdmWindowsInformationProtectionPolicy</span></span>

> <span data-ttu-id="98d49-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="98d49-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="98d49-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="98d49-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="98d49-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="98d49-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="98d49-107">Actualice las propiedades de un objeto [mdmWindowsInformationProtectionPolicy](../resources/intune-mam-mdmwindowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-107">Update the properties of a [mdmWindowsInformationProtectionPolicy](../resources/intune-mam-mdmwindowsinformationprotectionpolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="98d49-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="98d49-108">Prerequisites</span></span>
<span data-ttu-id="98d49-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="98d49-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="98d49-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="98d49-111">Permission type</span></span>|<span data-ttu-id="98d49-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="98d49-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="98d49-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="98d49-113">Delegated (work or school account)</span></span>|<span data-ttu-id="98d49-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98d49-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="98d49-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="98d49-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="98d49-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="98d49-116">Not supported.</span></span>|
|<span data-ttu-id="98d49-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="98d49-117">Application</span></span>|<span data-ttu-id="98d49-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="98d49-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="98d49-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="98d49-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="98d49-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="98d49-120">Request headers</span></span>
|<span data-ttu-id="98d49-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98d49-121">Header</span></span>|<span data-ttu-id="98d49-122">Valor</span><span class="sxs-lookup"><span data-stu-id="98d49-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="98d49-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="98d49-123">Authorization</span></span>|<span data-ttu-id="98d49-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="98d49-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="98d49-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="98d49-125">Accept</span></span>|<span data-ttu-id="98d49-126">application/json</span><span class="sxs-lookup"><span data-stu-id="98d49-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="98d49-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="98d49-127">Request body</span></span>
<span data-ttu-id="98d49-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [mdmWindowsInformationProtectionPolicy](../resources/intune-mam-mdmwindowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-128">In the request body, supply a JSON representation for the [mdmWindowsInformationProtectionPolicy](../resources/intune-mam-mdmwindowsinformationprotectionpolicy.md) object.</span></span>

<span data-ttu-id="98d49-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [mdmWindowsInformationProtectionPolicy](../resources/intune-mam-mdmwindowsinformationprotectionpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-129">The following table shows the properties that are required when you create the [mdmWindowsInformationProtectionPolicy](../resources/intune-mam-mdmwindowsinformationprotectionpolicy.md).</span></span>

|<span data-ttu-id="98d49-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="98d49-130">Property</span></span>|<span data-ttu-id="98d49-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="98d49-131">Type</span></span>|<span data-ttu-id="98d49-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="98d49-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="98d49-133">displayName</span><span class="sxs-lookup"><span data-stu-id="98d49-133">displayName</span></span>|<span data-ttu-id="98d49-134">String</span><span class="sxs-lookup"><span data-stu-id="98d49-134">String</span></span>|<span data-ttu-id="98d49-135">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="98d49-135">Policy display name.</span></span> <span data-ttu-id="98d49-136">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-136">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="98d49-137">descripción</span><span class="sxs-lookup"><span data-stu-id="98d49-137">description</span></span>|<span data-ttu-id="98d49-138">String</span><span class="sxs-lookup"><span data-stu-id="98d49-138">String</span></span>|<span data-ttu-id="98d49-139">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="98d49-139">The policy's description.</span></span> <span data-ttu-id="98d49-140">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-140">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="98d49-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="98d49-141">createdDateTime</span></span>|<span data-ttu-id="98d49-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="98d49-142">DateTimeOffset</span></span>|<span data-ttu-id="98d49-143">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="98d49-143">The date and time the policy was created.</span></span> <span data-ttu-id="98d49-144">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-144">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="98d49-145">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="98d49-145">lastModifiedDateTime</span></span>|<span data-ttu-id="98d49-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="98d49-146">DateTimeOffset</span></span>|<span data-ttu-id="98d49-147">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="98d49-147">Last time the policy was modified.</span></span> <span data-ttu-id="98d49-148">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-148">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="98d49-149">id</span><span class="sxs-lookup"><span data-stu-id="98d49-149">id</span></span>|<span data-ttu-id="98d49-150">String</span><span class="sxs-lookup"><span data-stu-id="98d49-150">String</span></span>|<span data-ttu-id="98d49-151">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="98d49-151">Key of the entity.</span></span> <span data-ttu-id="98d49-152">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-152">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="98d49-153">version</span><span class="sxs-lookup"><span data-stu-id="98d49-153">version</span></span>|<span data-ttu-id="98d49-154">String</span><span class="sxs-lookup"><span data-stu-id="98d49-154">String</span></span>|<span data-ttu-id="98d49-155">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="98d49-155">Version of the entity.</span></span> <span data-ttu-id="98d49-156">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-156">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="98d49-157">enforcementLevel</span><span class="sxs-lookup"><span data-stu-id="98d49-157">enforcementLevel</span></span>|[<span data-ttu-id="98d49-158">windowsInformationProtectionEnforcementLevel</span><span class="sxs-lookup"><span data-stu-id="98d49-158">windowsInformationProtectionEnforcementLevel</span></span>](../resources/intune-mam-windowsinformationprotectionenforcementlevel.md)|<span data-ttu-id="98d49-159">Nivel de aplicación de trabajo en curso. Vea la definición de enumeración para los valores admitidos Inherited desde [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-159">WIP enforcement level.See the Enum definition for supported values Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span></span> <span data-ttu-id="98d49-160">Los valores posibles son: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt` y `encryptAuditAndBlock`.</span><span class="sxs-lookup"><span data-stu-id="98d49-160">Possible values are: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt`, `encryptAuditAndBlock`.</span></span>|
|<span data-ttu-id="98d49-161">enterpriseDomain</span><span class="sxs-lookup"><span data-stu-id="98d49-161">enterpriseDomain</span></span>|<span data-ttu-id="98d49-162">String</span><span class="sxs-lookup"><span data-stu-id="98d49-162">String</span></span>|<span data-ttu-id="98d49-163">Dominio empresarial principal. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-163">Primary enterprise domain Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-164">enterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="98d49-164">enterpriseProtectedDomainNames</span></span>|<span data-ttu-id="98d49-165">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="98d49-165">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="98d49-166">Lista de dominios de empresa que se van a proteger. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-166">List of enterprise domains to be protected Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-167">protectionUnderLockConfigRequired</span><span class="sxs-lookup"><span data-stu-id="98d49-167">protectionUnderLockConfigRequired</span></span>|<span data-ttu-id="98d49-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="98d49-168">Boolean</span></span>|<span data-ttu-id="98d49-169">Especifica si es necesario configurar la protección en la característica de bloqueo (también conocida como cifrar con PIN). Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-169">Specifies whether the protection under lock feature (also known as encrypt under pin) should be configured Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-170">dataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="98d49-170">dataRecoveryCertificate</span></span>|[<span data-ttu-id="98d49-171">windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="98d49-171">windowsInformationProtectionDataRecoveryCertificate</span></span>](../resources/intune-mam-windowsinformationprotectiondatarecoverycertificate.md)|<span data-ttu-id="98d49-172">Especifica un certificado de recuperación que se puede usar para recuperar datos de archivos cifrados.</span><span class="sxs-lookup"><span data-stu-id="98d49-172">Specifies a recovery certificate that can be used for data recovery of encrypted files.</span></span> <span data-ttu-id="98d49-173">Es igual al certificado del agente de recuperación de datos (DRA) para el sistema de cifrado de archivos (EFS). Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="98d49-173">This is the same as the data recovery agent(DRA) certificate for encrypting file system(EFS) Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-174">revokeOnUnenrollDisabled</span><span class="sxs-lookup"><span data-stu-id="98d49-174">revokeOnUnenrollDisabled</span></span>|<span data-ttu-id="98d49-175">Boolean</span><span class="sxs-lookup"><span data-stu-id="98d49-175">Boolean</span></span>|<span data-ttu-id="98d49-176">Esta directiva controla si se revocan las claves de trabajo en curso cuando se anula la inscripción de un dispositivo en el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="98d49-176">This policy controls whether to revoke the WIP keys when a device unenrolls from the management service.</span></span> <span data-ttu-id="98d49-177">Si se establece en 1 (no revocar las claves), no se revocarán las claves y el usuario seguirá teniendo acceso a archivos protegidos después de anular la inscripción.</span><span class="sxs-lookup"><span data-stu-id="98d49-177">If set to 1 (Don't revoke keys), the keys will not be revoked and the user will continue to have access to protected files after unenrollment.</span></span> <span data-ttu-id="98d49-178">Si no se revocan las claves, no habrá ninguna limpieza de archivos revocados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="98d49-178">If the keys are not revoked, there will be no revoked file cleanup subsequently.</span></span> <span data-ttu-id="98d49-179">Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="98d49-179">Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-180">rightsManagementServicesTemplateId</span><span class="sxs-lookup"><span data-stu-id="98d49-180">rightsManagementServicesTemplateId</span></span>|<span data-ttu-id="98d49-181">Guid</span><span class="sxs-lookup"><span data-stu-id="98d49-181">Guid</span></span>|<span data-ttu-id="98d49-182">GUID de TemplateID que se va a usar para el cifrado RMS.</span><span class="sxs-lookup"><span data-stu-id="98d49-182">TemplateID GUID to use for RMS encryption.</span></span> <span data-ttu-id="98d49-183">La plantilla de RMS permite que el administrador de TI configure los detalles sobre quién tiene acceso a los archivos protegidos por RMS y durante cuánto tiempo. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-183">The RMS template allows the IT admin to configure the details about who has access to RMS-protected file and how long they have access Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-184">azureRightsManagementServicesAllowed</span><span class="sxs-lookup"><span data-stu-id="98d49-184">azureRightsManagementServicesAllowed</span></span>|<span data-ttu-id="98d49-185">Booleano</span><span class="sxs-lookup"><span data-stu-id="98d49-185">Boolean</span></span>|<span data-ttu-id="98d49-186">Especifica si se permite el cifrado de Azure RMS para WIP. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-186">Specifies whether to allow Azure RMS encryption for WIP Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-187">iconsVisible</span><span class="sxs-lookup"><span data-stu-id="98d49-187">iconsVisible</span></span>|<span data-ttu-id="98d49-188">Boolean</span><span class="sxs-lookup"><span data-stu-id="98d49-188">Boolean</span></span>|<span data-ttu-id="98d49-189">Determina si se agregan las superposiciones a los iconos para los archivos protegidos mediante WIP en Explorer y en los iconos de aplicación solo de empresa en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="98d49-189">Determines whether overlays are added to icons for WIP protected files in Explorer and enterprise only app tiles in the Start menu.</span></span> <span data-ttu-id="98d49-190">A partir de Windows 10, versión 1703, estos ajustes también configuran la visibilidad del icono de WIP en la barra de título de una aplicación protegida mediante WIP. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-190">Starting in Windows 10, version 1703 this setting also configures the visibility of the WIP icon in the title bar of a WIP-protected app Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-191">protectedApps</span><span class="sxs-lookup"><span data-stu-id="98d49-191">protectedApps</span></span>|<span data-ttu-id="98d49-192">Colección [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="98d49-192">[windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="98d49-193">Las aplicaciones protegidas pueden tener acceso a datos empresariales y los datos controlados por dichas aplicaciones están protegidos mediante cifrado. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-193">Protected applications can access enterprise data and the data handled by those applications are protected with encryption Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-194">exemptApps</span><span class="sxs-lookup"><span data-stu-id="98d49-194">exemptApps</span></span>|<span data-ttu-id="98d49-195">Colección [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="98d49-195">[windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="98d49-196">Las aplicaciones exentas también pueden tener acceso a datos empresariales, pero los datos controlados por dichas aplicaciones no están protegidos.</span><span class="sxs-lookup"><span data-stu-id="98d49-196">Exempt applications can also access enterprise data, but the data handled by those applications are not protected.</span></span> <span data-ttu-id="98d49-197">Esto ocurre porque algunas aplicaciones empresariales críticas podrían tener problemas de compatibilidad con los datos cifrados.</span><span class="sxs-lookup"><span data-stu-id="98d49-197">This is because some critical enterprise applications may have compatibility problems with encrypted data.</span></span> <span data-ttu-id="98d49-198">Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="98d49-198">Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-199">enterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="98d49-199">enterpriseNetworkDomainNames</span></span>|<span data-ttu-id="98d49-200">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="98d49-200">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="98d49-201">Esta es la lista de dominios que forman parte de los límites de la empresa.</span><span class="sxs-lookup"><span data-stu-id="98d49-201">This is the list of domains that comprise the boundaries of the enterprise.</span></span> <span data-ttu-id="98d49-202">Los datos de uno de estos dominios que se envíen a un dispositivo se considerarán datos empresariales y protegidos. Estas ubicaciones se consideran un destino seguro con el que compartir datos empresariales. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-202">Data from one of these domains that is sent to a device will be considered enterprise data and protected These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-203">enterpriseProxiedDomains</span><span class="sxs-lookup"><span data-stu-id="98d49-203">enterpriseProxiedDomains</span></span>|<span data-ttu-id="98d49-204">Colección [windowsInformationProtectionProxiedDomainCollection](../resources/intune-mam-windowsinformationprotectionproxieddomaincollection.md)</span><span class="sxs-lookup"><span data-stu-id="98d49-204">[windowsInformationProtectionProxiedDomainCollection](../resources/intune-mam-windowsinformationprotectionproxieddomaincollection.md) collection</span></span>|<span data-ttu-id="98d49-205">Contiene una lista de dominios de recursos empresariales hospedados en la nube que necesitan protección.</span><span class="sxs-lookup"><span data-stu-id="98d49-205">Contains a list of Enterprise resource domains hosted in the cloud that need to be protected.</span></span> <span data-ttu-id="98d49-206">Las conexiones a estos recursos se consideran datos empresariales.</span><span class="sxs-lookup"><span data-stu-id="98d49-206">Connections to these resources are considered enterprise data.</span></span> <span data-ttu-id="98d49-207">Si un proxy se corresponde con un recurso de nube, el tráfico al recurso de la nube se dirigirá a través de la red empresarial mediante el servidor proxy indicado (en el puerto 80).</span><span class="sxs-lookup"><span data-stu-id="98d49-207">If a proxy is paired with a cloud resource, traffic to the cloud resource will be routed through the enterprise network via the denoted proxy server (on Port 80).</span></span> <span data-ttu-id="98d49-208">Un servidor proxy que se use con esta finalidad debe configurarse también mediante la directiva EnterpriseInternalProxyServers. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-208">A proxy server used for this purpose must also be configured using the EnterpriseInternalProxyServers policy Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-209">enterpriseIPRanges</span><span class="sxs-lookup"><span data-stu-id="98d49-209">enterpriseIPRanges</span></span>|<span data-ttu-id="98d49-210">Colección [windowsInformationProtectionIPRangeCollection](../resources/intune-mam-windowsinformationprotectioniprangecollection.md)</span><span class="sxs-lookup"><span data-stu-id="98d49-210">[windowsInformationProtectionIPRangeCollection](../resources/intune-mam-windowsinformationprotectioniprangecollection.md) collection</span></span>|<span data-ttu-id="98d49-211">Establece los intervalos IP empresariales que definen los equipos de la red empresarial.</span><span class="sxs-lookup"><span data-stu-id="98d49-211">Sets the enterprise IP ranges that define the computers in the enterprise network.</span></span> <span data-ttu-id="98d49-212">Los datos que provienen de dichos equipos se consideran parte de la empresa y están protegidos.</span><span class="sxs-lookup"><span data-stu-id="98d49-212">Data that comes from those computers will be considered part of the enterprise and protected.</span></span> <span data-ttu-id="98d49-213">Estas ubicaciones se consideran un destino seguro en el que compartir datos empresariales. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-213">These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-214">enterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="98d49-214">enterpriseIPRangesAreAuthoritative</span></span>|<span data-ttu-id="98d49-215">Boolean</span><span class="sxs-lookup"><span data-stu-id="98d49-215">Boolean</span></span>|<span data-ttu-id="98d49-216">Valor booleano que indica al cliente que acepte la lista configurada y que no use la heurística para intentar buscar otras subredes.</span><span class="sxs-lookup"><span data-stu-id="98d49-216">Boolean value that tells the client to accept the configured list and not to use heuristics to attempt to find other subnets.</span></span> <span data-ttu-id="98d49-217">El valor predeterminado es False. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-217">Default is false Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-218">enterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="98d49-218">enterpriseProxyServers</span></span>|<span data-ttu-id="98d49-219">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="98d49-219">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="98d49-220">Esta es una lista de servidores proxy.</span><span class="sxs-lookup"><span data-stu-id="98d49-220">This is a list of proxy servers.</span></span> <span data-ttu-id="98d49-221">Cualquier servidor que no esté en esta lista se considera no empresarial. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-221">Any server not on this list is considered non-enterprise Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-222">enterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="98d49-222">enterpriseInternalProxyServers</span></span>|<span data-ttu-id="98d49-223">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="98d49-223">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="98d49-224">Se trata de la lista de valores separados por comas de servidores proxy internos.</span><span class="sxs-lookup"><span data-stu-id="98d49-224">This is the comma-separated list of internal proxy servers.</span></span> <span data-ttu-id="98d49-225">Por ejemplo, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span><span class="sxs-lookup"><span data-stu-id="98d49-225">For example, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span></span> <span data-ttu-id="98d49-226">El administrador ha configurado estos servidores proxy para que se conecten a los recursos específicos de Internet.</span><span class="sxs-lookup"><span data-stu-id="98d49-226">These proxies have been configured by the admin to connect to specific resources on the Internet.</span></span> <span data-ttu-id="98d49-227">Se consideran ubicaciones de red empresarial.</span><span class="sxs-lookup"><span data-stu-id="98d49-227">They are considered to be enterprise network locations.</span></span> <span data-ttu-id="98d49-228">Los servidores proxy solo se usan al configurar la directiva EnterpriseProxiedDomains para forzar el tráfico a los dominios coincidentes mediante estos proxy. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-228">The proxies are only leveraged in configuring the EnterpriseProxiedDomains policy to force traffic to the matched domains through these proxies Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-229">enterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="98d49-229">enterpriseProxyServersAreAuthoritative</span></span>|<span data-ttu-id="98d49-230">Boolean</span><span class="sxs-lookup"><span data-stu-id="98d49-230">Boolean</span></span>|<span data-ttu-id="98d49-231">Valor booleano que indica al cliente que acepte la lista de configuración de servidores proxy y no intente detectar otros servidores proxy de trabajo.</span><span class="sxs-lookup"><span data-stu-id="98d49-231">Boolean value that tells the client to accept the configured list of proxies and not try to detect other work proxies.</span></span> <span data-ttu-id="98d49-232">El valor predeterminado es False. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-232">Default is false Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-233">neutralDomainResources</span><span class="sxs-lookup"><span data-stu-id="98d49-233">neutralDomainResources</span></span>|<span data-ttu-id="98d49-234">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="98d49-234">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="98d49-235">Lista de nombres de dominio que se pueden usar para el recurso de trabajo o personal. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-235">List of domain names that can used for work or personal resource Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-236">indexingEncryptedStoresOrItemsBlocked</span><span class="sxs-lookup"><span data-stu-id="98d49-236">indexingEncryptedStoresOrItemsBlocked</span></span>|<span data-ttu-id="98d49-237">Boolean</span><span class="sxs-lookup"><span data-stu-id="98d49-237">Boolean</span></span>|<span data-ttu-id="98d49-238">Este identificador es para que el indexador de Windows Search permita o impida la indexación de los elementos. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-238">This switch is for the Windows Search Indexer, to allow or disallow indexing of items Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-239">smbAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="98d49-239">smbAutoEncryptedFileExtensions</span></span>|<span data-ttu-id="98d49-240">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="98d49-240">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="98d49-241">Especifica una lista de extensiones de archivo, para que los archivos con estas extensiones se cifren cuando se copian desde un recurso compartido de SMB dentro del límite de la empresa. Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="98d49-241">Specifies a list of file extensions, so that files with these extensions are encrypted when copying from an SMB share within the corporate boundary Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="98d49-242">isAssigned</span><span class="sxs-lookup"><span data-stu-id="98d49-242">isAssigned</span></span>|<span data-ttu-id="98d49-243">Boolean</span><span class="sxs-lookup"><span data-stu-id="98d49-243">Boolean</span></span>|<span data-ttu-id="98d49-244">Indica si la directiva se implementará en los grupos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="98d49-244">Indicates if the policy is deployed to any inclusion groups or not.</span></span> <span data-ttu-id="98d49-245">Heredado de [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="98d49-245">Inherited from [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span></span>|



## <a name="response"></a><span data-ttu-id="98d49-246">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98d49-246">Response</span></span>
<span data-ttu-id="98d49-247">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [mdmWindowsInformationProtectionPolicy](../resources/intune-mam-mdmwindowsinformationprotectionpolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98d49-247">If successful, this method returns a `200 OK` response code and an updated [mdmWindowsInformationProtectionPolicy](../resources/intune-mam-mdmwindowsinformationprotectionpolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="98d49-248">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="98d49-248">Example</span></span>
### <a name="request"></a><span data-ttu-id="98d49-249">Solicitud</span><span class="sxs-lookup"><span data-stu-id="98d49-249">Request</span></span>
<span data-ttu-id="98d49-250">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="98d49-250">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}
Content-type: application/json
Content-length: 3893

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
  "isAssigned": true
}
```

### <a name="response"></a><span data-ttu-id="98d49-251">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98d49-251">Response</span></span>
<span data-ttu-id="98d49-p123">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="98d49-p123">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 4077

{
  "@odata.type": "#microsoft.graph.mdmWindowsInformationProtectionPolicy",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "id": "8efb0c35-0c35-8efb-350c-fb8e350cfb8e",
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
  "isAssigned": true
}
```






---
title: Tipo de recurso windowsInformationProtection
description: Directiva de Windows Information Protection para configurar las opciones de administración detalladas
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: e768047c1807c804deebcea566a7d45265d6c498
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962663"
---
# <a name="windowsinformationprotection-resource-type"></a><span data-ttu-id="c148a-103">Tipo de recurso windowsInformationProtection</span><span class="sxs-lookup"><span data-stu-id="c148a-103">windowsInformationProtection resource type</span></span>

> <span data-ttu-id="c148a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c148a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c148a-105">Directiva de Windows Information Protection para configurar las opciones de administración detalladas</span><span class="sxs-lookup"><span data-stu-id="c148a-105">Policy for Windows information protection to configure detailed management settings</span></span>

<span data-ttu-id="c148a-106">Hereda de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="c148a-106">Inherits from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>

## <a name="methods"></a><span data-ttu-id="c148a-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="c148a-107">Methods</span></span>
|<span data-ttu-id="c148a-108">Método</span><span class="sxs-lookup"><span data-stu-id="c148a-108">Method</span></span>|<span data-ttu-id="c148a-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c148a-109">Return Type</span></span>|<span data-ttu-id="c148a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c148a-110">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="c148a-111">Enumerar windowsInformationProtections</span><span class="sxs-lookup"><span data-stu-id="c148a-111">List windowsInformationProtections</span></span>](../api/intune-mam-windowsinformationprotection-list.md)|<span data-ttu-id="c148a-112">Colección [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="c148a-112">[windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md) collection</span></span>|<span data-ttu-id="c148a-113">Enumere las propiedades y las relaciones de los objetos [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c148a-113">List properties and relationships of the [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md) objects.</span></span>|
|[<span data-ttu-id="c148a-114">Obtener windowsInformationProtection</span><span class="sxs-lookup"><span data-stu-id="c148a-114">Get windowsInformationProtection</span></span>](../api/intune-mam-windowsinformationprotection-get.md)|[<span data-ttu-id="c148a-115">windowsInformationProtection</span><span class="sxs-lookup"><span data-stu-id="c148a-115">windowsInformationProtection</span></span>](../resources/intune-mam-windowsinformationprotection.md)|<span data-ttu-id="c148a-116">Lea las propiedades y las relaciones del objeto [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="c148a-116">Read properties and relationships of the [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md) object.</span></span>|
|[<span data-ttu-id="c148a-117">Acción assign</span><span class="sxs-lookup"><span data-stu-id="c148a-117">assign action</span></span>](../api/intune-mam-windowsinformationprotection-assign.md)|<span data-ttu-id="c148a-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c148a-118">None</span></span>|<span data-ttu-id="c148a-119">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="c148a-119">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="c148a-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c148a-120">Properties</span></span>
|<span data-ttu-id="c148a-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c148a-121">Property</span></span>|<span data-ttu-id="c148a-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="c148a-122">Type</span></span>|<span data-ttu-id="c148a-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="c148a-123">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c148a-124">displayName</span><span class="sxs-lookup"><span data-stu-id="c148a-124">displayName</span></span>|<span data-ttu-id="c148a-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="c148a-125">String</span></span>|<span data-ttu-id="c148a-126">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="c148a-126">Policy display name.</span></span> <span data-ttu-id="c148a-127">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c148a-127">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="c148a-128">descripción</span><span class="sxs-lookup"><span data-stu-id="c148a-128">description</span></span>|<span data-ttu-id="c148a-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="c148a-129">String</span></span>|<span data-ttu-id="c148a-130">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="c148a-130">The policy's description.</span></span> <span data-ttu-id="c148a-131">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c148a-131">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="c148a-132">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c148a-132">createdDateTime</span></span>|<span data-ttu-id="c148a-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c148a-133">DateTimeOffset</span></span>|<span data-ttu-id="c148a-134">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="c148a-134">The date and time the policy was created.</span></span> <span data-ttu-id="c148a-135">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c148a-135">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="c148a-136">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="c148a-136">lastModifiedDateTime</span></span>|<span data-ttu-id="c148a-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c148a-137">DateTimeOffset</span></span>|<span data-ttu-id="c148a-138">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="c148a-138">Last time the policy was modified.</span></span> <span data-ttu-id="c148a-139">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c148a-139">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="c148a-140">id</span><span class="sxs-lookup"><span data-stu-id="c148a-140">id</span></span>|<span data-ttu-id="c148a-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="c148a-141">String</span></span>|<span data-ttu-id="c148a-142">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c148a-142">Key of the entity.</span></span> <span data-ttu-id="c148a-143">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c148a-143">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="c148a-144">version</span><span class="sxs-lookup"><span data-stu-id="c148a-144">version</span></span>|<span data-ttu-id="c148a-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="c148a-145">String</span></span>|<span data-ttu-id="c148a-146">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c148a-146">Version of the entity.</span></span> <span data-ttu-id="c148a-147">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c148a-147">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="c148a-148">enforcementLevel</span><span class="sxs-lookup"><span data-stu-id="c148a-148">enforcementLevel</span></span>|[<span data-ttu-id="c148a-149">windowsInformationProtectionEnforcementLevel</span><span class="sxs-lookup"><span data-stu-id="c148a-149">windowsInformationProtectionEnforcementLevel</span></span>](../resources/intune-mam-windowsinformationprotectionenforcementlevel.md)|<span data-ttu-id="c148a-150">Nivel de aplicación de trabajo en curso. Vea la definición de enumeración para los valores admitidos.</span><span class="sxs-lookup"><span data-stu-id="c148a-150">WIP enforcement level.See the Enum definition for supported values.</span></span> <span data-ttu-id="c148a-151">Los valores posibles son: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt` y `encryptAuditAndBlock`.</span><span class="sxs-lookup"><span data-stu-id="c148a-151">Possible values are: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt`, `encryptAuditAndBlock`.</span></span>|
|<span data-ttu-id="c148a-152">enterpriseDomain</span><span class="sxs-lookup"><span data-stu-id="c148a-152">enterpriseDomain</span></span>|<span data-ttu-id="c148a-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="c148a-153">String</span></span>|<span data-ttu-id="c148a-154">Dominio empresarial principal</span><span class="sxs-lookup"><span data-stu-id="c148a-154">Primary enterprise domain</span></span>|
|<span data-ttu-id="c148a-155">enterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="c148a-155">enterpriseProtectedDomainNames</span></span>|<span data-ttu-id="c148a-156">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="c148a-156">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="c148a-157">Lista de dominios empresariales que quiere proteger</span><span class="sxs-lookup"><span data-stu-id="c148a-157">List of enterprise domains to be protected</span></span>|
|<span data-ttu-id="c148a-158">protectionUnderLockConfigRequired</span><span class="sxs-lookup"><span data-stu-id="c148a-158">protectionUnderLockConfigRequired</span></span>|<span data-ttu-id="c148a-159">Booleano</span><span class="sxs-lookup"><span data-stu-id="c148a-159">Boolean</span></span>|<span data-ttu-id="c148a-160">Especifica si es necesario configurar la protección en la característica de bloqueo (también conocida como cifrar con PIN)</span><span class="sxs-lookup"><span data-stu-id="c148a-160">Specifies whether the protection under lock feature (also known as encrypt under pin) should be configured</span></span>|
|<span data-ttu-id="c148a-161">dataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="c148a-161">dataRecoveryCertificate</span></span>|[<span data-ttu-id="c148a-162">windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="c148a-162">windowsInformationProtectionDataRecoveryCertificate</span></span>](../resources/intune-mam-windowsinformationprotectiondatarecoverycertificate.md)|<span data-ttu-id="c148a-163">Especifica un certificado de recuperación que se puede usar para recuperar datos de archivos cifrados.</span><span class="sxs-lookup"><span data-stu-id="c148a-163">Specifies a recovery certificate that can be used for data recovery of encrypted files.</span></span> <span data-ttu-id="c148a-164">Esto es lo mismo que el certificado del agente de recuperación de datos (DRA) para el sistema de cifrado de archivos (EFS)</span><span class="sxs-lookup"><span data-stu-id="c148a-164">This is the same as the data recovery agent(DRA) certificate for encrypting file system(EFS)</span></span>|
|<span data-ttu-id="c148a-165">revokeOnUnenrollDisabled</span><span class="sxs-lookup"><span data-stu-id="c148a-165">revokeOnUnenrollDisabled</span></span>|<span data-ttu-id="c148a-166">Booleano</span><span class="sxs-lookup"><span data-stu-id="c148a-166">Boolean</span></span>|<span data-ttu-id="c148a-167">Esta directiva controla si se revocan las claves de trabajo en curso cuando se anula la inscripción de un dispositivo en el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="c148a-167">This policy controls whether to revoke the WIP keys when a device unenrolls from the management service.</span></span> <span data-ttu-id="c148a-168">Si se establece en 1 (no revocar las claves), no se revocarán las claves y el usuario seguirá teniendo acceso a archivos protegidos después de anular la inscripción.</span><span class="sxs-lookup"><span data-stu-id="c148a-168">If set to 1 (Don't revoke keys), the keys will not be revoked and the user will continue to have access to protected files after unenrollment.</span></span> <span data-ttu-id="c148a-169">Si no se revocan las claves, no habrá ninguna limpieza de archivos revocados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="c148a-169">If the keys are not revoked, there will be no revoked file cleanup subsequently.</span></span>|
|<span data-ttu-id="c148a-170">rightsManagementServicesTemplateId</span><span class="sxs-lookup"><span data-stu-id="c148a-170">rightsManagementServicesTemplateId</span></span>|<span data-ttu-id="c148a-171">Guid</span><span class="sxs-lookup"><span data-stu-id="c148a-171">Guid</span></span>|<span data-ttu-id="c148a-172">GUID de TemplateID que se va a usar para el cifrado RMS.</span><span class="sxs-lookup"><span data-stu-id="c148a-172">TemplateID GUID to use for RMS encryption.</span></span> <span data-ttu-id="c148a-173">La plantilla de RMS permite que el administrador de TI configure los detalles sobre quién tiene acceso a los archivos protegidos por RMS y durante cuánto tiempo tienen acceso</span><span class="sxs-lookup"><span data-stu-id="c148a-173">The RMS template allows the IT admin to configure the details about who has access to RMS-protected file and how long they have access</span></span>|
|<span data-ttu-id="c148a-174">azureRightsManagementServicesAllowed</span><span class="sxs-lookup"><span data-stu-id="c148a-174">azureRightsManagementServicesAllowed</span></span>|<span data-ttu-id="c148a-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="c148a-175">Boolean</span></span>|<span data-ttu-id="c148a-176">Especifica si se permite el cifrado de Azure RMS para WIP.</span><span class="sxs-lookup"><span data-stu-id="c148a-176">Specifies whether to allow Azure RMS encryption for WIP</span></span>|
|<span data-ttu-id="c148a-177">iconsVisible</span><span class="sxs-lookup"><span data-stu-id="c148a-177">iconsVisible</span></span>|<span data-ttu-id="c148a-178">Booleano</span><span class="sxs-lookup"><span data-stu-id="c148a-178">Boolean</span></span>|<span data-ttu-id="c148a-179">Determina si se agregan las superposiciones a los iconos para los archivos protegidos mediante WIP en Explorer y en los iconos de aplicación solo de empresa en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="c148a-179">Determines whether overlays are added to icons for WIP protected files in Explorer and enterprise only app tiles in the Start menu.</span></span> <span data-ttu-id="c148a-180">A partir de Windows 10, versión 1703, estos ajustes también configuran la visibilidad del icono de WIP en la barra de título de una aplicación protegida mediante WIP</span><span class="sxs-lookup"><span data-stu-id="c148a-180">Starting in Windows 10, version 1703 this setting also configures the visibility of the WIP icon in the title bar of a WIP-protected app</span></span>|
|<span data-ttu-id="c148a-181">protectedApps</span><span class="sxs-lookup"><span data-stu-id="c148a-181">protectedApps</span></span>|<span data-ttu-id="c148a-182">Colección [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="c148a-182">[windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="c148a-183">Las aplicaciones protegidas pueden tener acceso a datos empresariales y los datos controlados por dichas aplicaciones están protegidos mediante cifrado</span><span class="sxs-lookup"><span data-stu-id="c148a-183">Protected applications can access enterprise data and the data handled by those applications are protected with encryption</span></span>|
|<span data-ttu-id="c148a-184">exemptApps</span><span class="sxs-lookup"><span data-stu-id="c148a-184">exemptApps</span></span>|<span data-ttu-id="c148a-185">Colección [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="c148a-185">[windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="c148a-186">Las aplicaciones exentas también pueden tener acceso a datos empresariales, pero los datos controlados por dichas aplicaciones no están protegidos.</span><span class="sxs-lookup"><span data-stu-id="c148a-186">Exempt applications can also access enterprise data, but the data handled by those applications are not protected.</span></span> <span data-ttu-id="c148a-187">Esto ocurre porque algunas aplicaciones empresariales críticas podrían tener problemas de compatibilidad con los datos cifrados.</span><span class="sxs-lookup"><span data-stu-id="c148a-187">This is because some critical enterprise applications may have compatibility problems with encrypted data.</span></span>|
|<span data-ttu-id="c148a-188">enterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="c148a-188">enterpriseNetworkDomainNames</span></span>|<span data-ttu-id="c148a-189">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="c148a-189">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="c148a-190">Esta es la lista de dominios que forman parte de los límites de la empresa.</span><span class="sxs-lookup"><span data-stu-id="c148a-190">This is the list of domains that comprise the boundaries of the enterprise.</span></span> <span data-ttu-id="c148a-191">Los datos de uno de estos dominios que se envíen a un dispositivo se considerarán datos empresariales y protegidos. Estas ubicaciones se consideran un destino seguro con el que compartir datos empresariales</span><span class="sxs-lookup"><span data-stu-id="c148a-191">Data from one of these domains that is sent to a device will be considered enterprise data and protected These locations will be considered a safe destination for enterprise data to be shared to</span></span>|
|<span data-ttu-id="c148a-192">enterpriseProxiedDomains</span><span class="sxs-lookup"><span data-stu-id="c148a-192">enterpriseProxiedDomains</span></span>|<span data-ttu-id="c148a-193">Colección [windowsInformationProtectionProxiedDomainCollection](../resources/intune-mam-windowsinformationprotectionproxieddomaincollection.md)</span><span class="sxs-lookup"><span data-stu-id="c148a-193">[windowsInformationProtectionProxiedDomainCollection](../resources/intune-mam-windowsinformationprotectionproxieddomaincollection.md) collection</span></span>|<span data-ttu-id="c148a-194">Contiene una lista de dominios de recursos empresariales hospedados en la nube que necesitan protección.</span><span class="sxs-lookup"><span data-stu-id="c148a-194">Contains a list of Enterprise resource domains hosted in the cloud that need to be protected.</span></span> <span data-ttu-id="c148a-195">Las conexiones a estos recursos se consideran datos empresariales.</span><span class="sxs-lookup"><span data-stu-id="c148a-195">Connections to these resources are considered enterprise data.</span></span> <span data-ttu-id="c148a-196">Si un proxy se corresponde con un recurso de nube, el tráfico al recurso de la nube se dirigirá a través de la red empresarial mediante el servidor proxy indicado (en el puerto 80).</span><span class="sxs-lookup"><span data-stu-id="c148a-196">If a proxy is paired with a cloud resource, traffic to the cloud resource will be routed through the enterprise network via the denoted proxy server (on Port 80).</span></span> <span data-ttu-id="c148a-197">Un servidor proxy que se use para este propósito también debe configurarse mediante la directiva EnterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="c148a-197">A proxy server used for this purpose must also be configured using the EnterpriseInternalProxyServers policy</span></span>|
|<span data-ttu-id="c148a-198">enterpriseIPRanges</span><span class="sxs-lookup"><span data-stu-id="c148a-198">enterpriseIPRanges</span></span>|<span data-ttu-id="c148a-199">Colección [windowsInformationProtectionIPRangeCollection](../resources/intune-mam-windowsinformationprotectioniprangecollection.md)</span><span class="sxs-lookup"><span data-stu-id="c148a-199">[windowsInformationProtectionIPRangeCollection](../resources/intune-mam-windowsinformationprotectioniprangecollection.md) collection</span></span>|<span data-ttu-id="c148a-200">Establece los intervalos IP empresariales que definen los equipos de la red empresarial.</span><span class="sxs-lookup"><span data-stu-id="c148a-200">Sets the enterprise IP ranges that define the computers in the enterprise network.</span></span> <span data-ttu-id="c148a-201">Los datos que provienen de dichos equipos se consideran parte de la empresa y están protegidos.</span><span class="sxs-lookup"><span data-stu-id="c148a-201">Data that comes from those computers will be considered part of the enterprise and protected.</span></span> <span data-ttu-id="c148a-202">Estas ubicaciones se consideran un destino seguro en el que compartir datos empresariales</span><span class="sxs-lookup"><span data-stu-id="c148a-202">These locations will be considered a safe destination for enterprise data to be shared to</span></span>|
|<span data-ttu-id="c148a-203">enterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="c148a-203">enterpriseIPRangesAreAuthoritative</span></span>|<span data-ttu-id="c148a-204">Booleano</span><span class="sxs-lookup"><span data-stu-id="c148a-204">Boolean</span></span>|<span data-ttu-id="c148a-205">Valor booleano que indica al cliente que acepte la lista configurada y que no use la heurística para intentar buscar otras subredes.</span><span class="sxs-lookup"><span data-stu-id="c148a-205">Boolean value that tells the client to accept the configured list and not to use heuristics to attempt to find other subnets.</span></span> <span data-ttu-id="c148a-206">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="c148a-206">Default is false</span></span>|
|<span data-ttu-id="c148a-207">enterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="c148a-207">enterpriseProxyServers</span></span>|<span data-ttu-id="c148a-208">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="c148a-208">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="c148a-209">Esta es una lista de servidores proxy.</span><span class="sxs-lookup"><span data-stu-id="c148a-209">This is a list of proxy servers.</span></span> <span data-ttu-id="c148a-210">Cualquier servidor que no esté en esta lista se considera no empresarial</span><span class="sxs-lookup"><span data-stu-id="c148a-210">Any server not on this list is considered non-enterprise</span></span>|
|<span data-ttu-id="c148a-211">enterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="c148a-211">enterpriseInternalProxyServers</span></span>|<span data-ttu-id="c148a-212">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="c148a-212">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="c148a-213">Se trata de la lista de valores separados por comas de servidores proxy internos.</span><span class="sxs-lookup"><span data-stu-id="c148a-213">This is the comma-separated list of internal proxy servers.</span></span> <span data-ttu-id="c148a-214">Por ejemplo, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span><span class="sxs-lookup"><span data-stu-id="c148a-214">For example, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span></span> <span data-ttu-id="c148a-215">El administrador ha configurado estos servidores proxy para que se conecten a los recursos específicos de Internet.</span><span class="sxs-lookup"><span data-stu-id="c148a-215">These proxies have been configured by the admin to connect to specific resources on the Internet.</span></span> <span data-ttu-id="c148a-216">Se consideran ubicaciones de red empresarial.</span><span class="sxs-lookup"><span data-stu-id="c148a-216">They are considered to be enterprise network locations.</span></span> <span data-ttu-id="c148a-217">Los servidores proxy solo se usan para configurar la directiva EnterpriseProxiedDomains para forzar el tráfico a los dominios coincidentes mediante estos proxy</span><span class="sxs-lookup"><span data-stu-id="c148a-217">The proxies are only leveraged in configuring the EnterpriseProxiedDomains policy to force traffic to the matched domains through these proxies</span></span>|
|<span data-ttu-id="c148a-218">enterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="c148a-218">enterpriseProxyServersAreAuthoritative</span></span>|<span data-ttu-id="c148a-219">Booleano</span><span class="sxs-lookup"><span data-stu-id="c148a-219">Boolean</span></span>|<span data-ttu-id="c148a-220">Valor booleano que indica al cliente que acepte la lista de configuración de servidores proxy y no intente detectar otros servidores proxy de trabajo.</span><span class="sxs-lookup"><span data-stu-id="c148a-220">Boolean value that tells the client to accept the configured list of proxies and not try to detect other work proxies.</span></span> <span data-ttu-id="c148a-221">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="c148a-221">Default is false</span></span>|
|<span data-ttu-id="c148a-222">neutralDomainResources</span><span class="sxs-lookup"><span data-stu-id="c148a-222">neutralDomainResources</span></span>|<span data-ttu-id="c148a-223">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="c148a-223">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="c148a-224">Lista de nombres de dominio que se pueden usar para el recurso de trabajo o personal</span><span class="sxs-lookup"><span data-stu-id="c148a-224">List of domain names that can used for work or personal resource</span></span>|
|<span data-ttu-id="c148a-225">indexingEncryptedStoresOrItemsBlocked</span><span class="sxs-lookup"><span data-stu-id="c148a-225">indexingEncryptedStoresOrItemsBlocked</span></span>|<span data-ttu-id="c148a-226">Booleano</span><span class="sxs-lookup"><span data-stu-id="c148a-226">Boolean</span></span>|<span data-ttu-id="c148a-227">Esta opción es para que el indexador de Windows Search permita o impida la indexación de los elementos</span><span class="sxs-lookup"><span data-stu-id="c148a-227">This switch is for the Windows Search Indexer, to allow or disallow indexing of items</span></span>|
|<span data-ttu-id="c148a-228">smbAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="c148a-228">smbAutoEncryptedFileExtensions</span></span>|<span data-ttu-id="c148a-229">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="c148a-229">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="c148a-230">Especifica una lista de extensiones de archivo, para que los archivos con estas extensiones se cifren cuando se copian desde un recurso compartido de SMB dentro del límite de la empresa</span><span class="sxs-lookup"><span data-stu-id="c148a-230">Specifies a list of file extensions, so that files with these extensions are encrypted when copying from an SMB share within the corporate boundary</span></span>|
|<span data-ttu-id="c148a-231">isAssigned</span><span class="sxs-lookup"><span data-stu-id="c148a-231">isAssigned</span></span>|<span data-ttu-id="c148a-232">Booleano</span><span class="sxs-lookup"><span data-stu-id="c148a-232">Boolean</span></span>|<span data-ttu-id="c148a-233">Indica si la directiva se implementará en los grupos de inclusión o no.</span><span class="sxs-lookup"><span data-stu-id="c148a-233">Indicates if the policy is deployed to any inclusion groups or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c148a-234">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c148a-234">Relationships</span></span>
|<span data-ttu-id="c148a-235">Relación</span><span class="sxs-lookup"><span data-stu-id="c148a-235">Relationship</span></span>|<span data-ttu-id="c148a-236">Tipo</span><span class="sxs-lookup"><span data-stu-id="c148a-236">Type</span></span>|<span data-ttu-id="c148a-237">Descripción</span><span class="sxs-lookup"><span data-stu-id="c148a-237">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c148a-238">protectedAppLockerFiles</span><span class="sxs-lookup"><span data-stu-id="c148a-238">protectedAppLockerFiles</span></span>|<span data-ttu-id="c148a-239">Colección [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md)</span><span class="sxs-lookup"><span data-stu-id="c148a-239">[windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) collection</span></span>|<span data-ttu-id="c148a-240">Otra forma de introducir aplicaciones protegidas mediante archivos XML</span><span class="sxs-lookup"><span data-stu-id="c148a-240">Another way to input protected apps through xml files</span></span>|
|<span data-ttu-id="c148a-241">exemptAppLockerFiles</span><span class="sxs-lookup"><span data-stu-id="c148a-241">exemptAppLockerFiles</span></span>|<span data-ttu-id="c148a-242">Colección [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md)</span><span class="sxs-lookup"><span data-stu-id="c148a-242">[windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) collection</span></span>|<span data-ttu-id="c148a-243">Otra forma de introducir aplicaciones exentas mediante archivos XML</span><span class="sxs-lookup"><span data-stu-id="c148a-243">Another way to input exempt apps through xml files</span></span>|
|<span data-ttu-id="c148a-244">asignaciones</span><span class="sxs-lookup"><span data-stu-id="c148a-244">assignments</span></span>|<span data-ttu-id="c148a-245">Colección [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md)</span><span class="sxs-lookup"><span data-stu-id="c148a-245">[targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) collection</span></span>|<span data-ttu-id="c148a-246">Propiedad de navegación a la lista de grupos de seguridad destinados a la directiva.</span><span class="sxs-lookup"><span data-stu-id="c148a-246">Navigation property to list of security groups targeted for policy.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="c148a-247">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c148a-247">JSON Representation</span></span>
<span data-ttu-id="c148a-248">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c148a-248">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsInformationProtection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtection",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "version": "String",
  "enforcementLevel": "String",
  "enterpriseDomain": "String",
  "enterpriseProtectedDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "protectionUnderLockConfigRequired": true,
  "dataRecoveryCertificate": {
    "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
    "subjectName": "String",
    "description": "String",
    "expirationDateTime": "String (timestamp)",
    "certificate": "binary"
  },
  "revokeOnUnenrollDisabled": true,
  "rightsManagementServicesTemplateId": "Guid",
  "azureRightsManagementServicesAllowed": true,
  "iconsVisible": true,
  "protectedApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionApp",
      "displayName": "String",
      "description": "String",
      "publisherName": "String",
      "productName": "String",
      "denied": true
    }
  ],
  "exemptApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionApp",
      "displayName": "String",
      "description": "String",
      "publisherName": "String",
      "productName": "String",
      "denied": true
    }
  ],
  "enterpriseNetworkDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "enterpriseProxiedDomains": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionProxiedDomainCollection",
      "displayName": "String",
      "proxiedDomains": [
        {
          "@odata.type": "microsoft.graph.proxiedDomain",
          "ipAddressOrFQDN": "String",
          "proxy": "String"
        }
      ]
    }
  ],
  "enterpriseIPRanges": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionIPRangeCollection",
      "displayName": "String",
      "ranges": [
        {
          "@odata.type": "microsoft.graph.iPv6Range",
          "lowerAddress": "String",
          "upperAddress": "String"
        }
      ]
    }
  ],
  "enterpriseIPRangesAreAuthoritative": true,
  "enterpriseProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "enterpriseInternalProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "enterpriseProxyServersAreAuthoritative": true,
  "neutralDomainResources": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "indexingEncryptedStoresOrItemsBlocked": true,
  "smbAutoEncryptedFileExtensions": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "String",
      "resources": [
        "String"
      ]
    }
  ],
  "isAssigned": true
}
```




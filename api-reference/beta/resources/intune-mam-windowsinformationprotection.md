---
title: Tipo de recurso windowsInformationProtection
description: Directiva de Windows Information Protection para configurar las opciones de administración detalladas
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 422bc13c8546d72c2a8ab04c6b684d69f0ed6f85
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953206"
---
# <a name="windowsinformationprotection-resource-type"></a><span data-ttu-id="7aa17-103">Tipo de recurso windowsInformationProtection</span><span class="sxs-lookup"><span data-stu-id="7aa17-103">windowsInformationProtection resource type</span></span>

> <span data-ttu-id="7aa17-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7aa17-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7aa17-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7aa17-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7aa17-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7aa17-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7aa17-107">Directiva de Windows Information Protection para configurar las opciones de administración detalladas</span><span class="sxs-lookup"><span data-stu-id="7aa17-107">Policy for Windows information protection to configure detailed management settings</span></span>

<span data-ttu-id="7aa17-108">Hereda de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="7aa17-108">Inherits from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>

## <a name="methods"></a><span data-ttu-id="7aa17-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="7aa17-109">Methods</span></span>
|<span data-ttu-id="7aa17-110">Método</span><span class="sxs-lookup"><span data-stu-id="7aa17-110">Method</span></span>|<span data-ttu-id="7aa17-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7aa17-111">Return Type</span></span>|<span data-ttu-id="7aa17-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7aa17-112">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="7aa17-113">Enumerar windowsInformationProtections</span><span class="sxs-lookup"><span data-stu-id="7aa17-113">List windowsInformationProtections</span></span>](../api/intune-mam-windowsinformationprotection-list.md)|<span data-ttu-id="7aa17-114">Colección [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md)</span><span class="sxs-lookup"><span data-stu-id="7aa17-114">[windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md) collection</span></span>|<span data-ttu-id="7aa17-115">Enumere las propiedades y las relaciones de los objetos [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="7aa17-115">List properties and relationships of the [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md) objects.</span></span>|
|[<span data-ttu-id="7aa17-116">Obtener windowsInformationProtection</span><span class="sxs-lookup"><span data-stu-id="7aa17-116">Get windowsInformationProtection</span></span>](../api/intune-mam-windowsinformationprotection-get.md)|[<span data-ttu-id="7aa17-117">windowsInformationProtection</span><span class="sxs-lookup"><span data-stu-id="7aa17-117">windowsInformationProtection</span></span>](../resources/intune-mam-windowsinformationprotection.md)|<span data-ttu-id="7aa17-118">Lea las propiedades y las relaciones del objeto [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md).</span><span class="sxs-lookup"><span data-stu-id="7aa17-118">Read properties and relationships of the [windowsInformationProtection](../resources/intune-mam-windowsinformationprotection.md) object.</span></span>|
|[<span data-ttu-id="7aa17-119">Acción assign</span><span class="sxs-lookup"><span data-stu-id="7aa17-119">assign action</span></span>](../api/intune-mam-windowsinformationprotection-assign.md)|<span data-ttu-id="7aa17-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7aa17-120">None</span></span>|<span data-ttu-id="7aa17-121">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7aa17-121">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="7aa17-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7aa17-122">Properties</span></span>
|<span data-ttu-id="7aa17-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7aa17-123">Property</span></span>|<span data-ttu-id="7aa17-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="7aa17-124">Type</span></span>|<span data-ttu-id="7aa17-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="7aa17-125">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7aa17-126">displayName</span><span class="sxs-lookup"><span data-stu-id="7aa17-126">displayName</span></span>|<span data-ttu-id="7aa17-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="7aa17-127">String</span></span>|<span data-ttu-id="7aa17-128">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="7aa17-128">Policy display name.</span></span> <span data-ttu-id="7aa17-129">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="7aa17-129">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="7aa17-130">descripción</span><span class="sxs-lookup"><span data-stu-id="7aa17-130">description</span></span>|<span data-ttu-id="7aa17-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="7aa17-131">String</span></span>|<span data-ttu-id="7aa17-132">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="7aa17-132">The policy's description.</span></span> <span data-ttu-id="7aa17-133">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="7aa17-133">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="7aa17-134">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="7aa17-134">createdDateTime</span></span>|<span data-ttu-id="7aa17-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7aa17-135">DateTimeOffset</span></span>|<span data-ttu-id="7aa17-136">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="7aa17-136">The date and time the policy was created.</span></span> <span data-ttu-id="7aa17-137">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="7aa17-137">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="7aa17-138">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7aa17-138">lastModifiedDateTime</span></span>|<span data-ttu-id="7aa17-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7aa17-139">DateTimeOffset</span></span>|<span data-ttu-id="7aa17-140">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="7aa17-140">Last time the policy was modified.</span></span> <span data-ttu-id="7aa17-141">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="7aa17-141">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="7aa17-142">id</span><span class="sxs-lookup"><span data-stu-id="7aa17-142">id</span></span>|<span data-ttu-id="7aa17-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="7aa17-143">String</span></span>|<span data-ttu-id="7aa17-144">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7aa17-144">Key of the entity.</span></span> <span data-ttu-id="7aa17-145">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="7aa17-145">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="7aa17-146">version</span><span class="sxs-lookup"><span data-stu-id="7aa17-146">version</span></span>|<span data-ttu-id="7aa17-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="7aa17-147">String</span></span>|<span data-ttu-id="7aa17-148">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7aa17-148">Version of the entity.</span></span> <span data-ttu-id="7aa17-149">Heredado de [managedAppPolicy](../resources/intune-mam-managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="7aa17-149">Inherited from [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span></span>|
|<span data-ttu-id="7aa17-150">enforcementLevel</span><span class="sxs-lookup"><span data-stu-id="7aa17-150">enforcementLevel</span></span>|[<span data-ttu-id="7aa17-151">windowsInformationProtectionEnforcementLevel</span><span class="sxs-lookup"><span data-stu-id="7aa17-151">windowsInformationProtectionEnforcementLevel</span></span>](../resources/intune-mam-windowsinformationprotectionenforcementlevel.md)|<span data-ttu-id="7aa17-152">Nivel de aplicación de trabajo en curso. Vea la definición de enumeración para los valores admitidos.</span><span class="sxs-lookup"><span data-stu-id="7aa17-152">WIP enforcement level.See the Enum definition for supported values.</span></span> <span data-ttu-id="7aa17-153">Los valores posibles son: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt` y `encryptAuditAndBlock`.</span><span class="sxs-lookup"><span data-stu-id="7aa17-153">Possible values are: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt`, `encryptAuditAndBlock`.</span></span>|
|<span data-ttu-id="7aa17-154">enterpriseDomain</span><span class="sxs-lookup"><span data-stu-id="7aa17-154">enterpriseDomain</span></span>|<span data-ttu-id="7aa17-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="7aa17-155">String</span></span>|<span data-ttu-id="7aa17-156">Dominio empresarial principal</span><span class="sxs-lookup"><span data-stu-id="7aa17-156">Primary enterprise domain</span></span>|
|<span data-ttu-id="7aa17-157">enterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="7aa17-157">enterpriseProtectedDomainNames</span></span>|<span data-ttu-id="7aa17-158">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="7aa17-158">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="7aa17-159">Lista de dominios empresariales que quiere proteger</span><span class="sxs-lookup"><span data-stu-id="7aa17-159">List of enterprise domains to be protected</span></span>|
|<span data-ttu-id="7aa17-160">protectionUnderLockConfigRequired</span><span class="sxs-lookup"><span data-stu-id="7aa17-160">protectionUnderLockConfigRequired</span></span>|<span data-ttu-id="7aa17-161">Booleano</span><span class="sxs-lookup"><span data-stu-id="7aa17-161">Boolean</span></span>|<span data-ttu-id="7aa17-162">Especifica si es necesario configurar la protección en la característica de bloqueo (también conocida como cifrar con PIN)</span><span class="sxs-lookup"><span data-stu-id="7aa17-162">Specifies whether the protection under lock feature (also known as encrypt under pin) should be configured</span></span>|
|<span data-ttu-id="7aa17-163">dataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="7aa17-163">dataRecoveryCertificate</span></span>|[<span data-ttu-id="7aa17-164">windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="7aa17-164">windowsInformationProtectionDataRecoveryCertificate</span></span>](../resources/intune-mam-windowsinformationprotectiondatarecoverycertificate.md)|<span data-ttu-id="7aa17-165">Especifica un certificado de recuperación que se puede usar para recuperar datos de archivos cifrados.</span><span class="sxs-lookup"><span data-stu-id="7aa17-165">Specifies a recovery certificate that can be used for data recovery of encrypted files.</span></span> <span data-ttu-id="7aa17-166">Esto es lo mismo que el certificado del agente de recuperación de datos (DRA) para el sistema de cifrado de archivos (EFS)</span><span class="sxs-lookup"><span data-stu-id="7aa17-166">This is the same as the data recovery agent(DRA) certificate for encrypting file system(EFS)</span></span>|
|<span data-ttu-id="7aa17-167">revokeOnUnenrollDisabled</span><span class="sxs-lookup"><span data-stu-id="7aa17-167">revokeOnUnenrollDisabled</span></span>|<span data-ttu-id="7aa17-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="7aa17-168">Boolean</span></span>|<span data-ttu-id="7aa17-169">Esta directiva controla si se revocan las claves de trabajo en curso cuando se anula la inscripción de un dispositivo en el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="7aa17-169">This policy controls whether to revoke the WIP keys when a device unenrolls from the management service.</span></span> <span data-ttu-id="7aa17-170">Si se establece en 1 (no revocar las claves), no se revocarán las claves y el usuario seguirá teniendo acceso a archivos protegidos después de anular la inscripción.</span><span class="sxs-lookup"><span data-stu-id="7aa17-170">If set to 1 (Don't revoke keys), the keys will not be revoked and the user will continue to have access to protected files after unenrollment.</span></span> <span data-ttu-id="7aa17-171">Si no se revocan las claves, no habrá ninguna limpieza de archivos revocados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="7aa17-171">If the keys are not revoked, there will be no revoked file cleanup subsequently.</span></span>|
|<span data-ttu-id="7aa17-172">rightsManagementServicesTemplateId</span><span class="sxs-lookup"><span data-stu-id="7aa17-172">rightsManagementServicesTemplateId</span></span>|<span data-ttu-id="7aa17-173">Guid</span><span class="sxs-lookup"><span data-stu-id="7aa17-173">Guid</span></span>|<span data-ttu-id="7aa17-174">GUID de TemplateID que se va a usar para el cifrado RMS.</span><span class="sxs-lookup"><span data-stu-id="7aa17-174">TemplateID GUID to use for RMS encryption.</span></span> <span data-ttu-id="7aa17-175">La plantilla de RMS permite que el administrador de TI configure los detalles sobre quién tiene acceso a los archivos protegidos por RMS y durante cuánto tiempo tienen acceso</span><span class="sxs-lookup"><span data-stu-id="7aa17-175">The RMS template allows the IT admin to configure the details about who has access to RMS-protected file and how long they have access</span></span>|
|<span data-ttu-id="7aa17-176">azureRightsManagementServicesAllowed</span><span class="sxs-lookup"><span data-stu-id="7aa17-176">azureRightsManagementServicesAllowed</span></span>|<span data-ttu-id="7aa17-177">Booleano</span><span class="sxs-lookup"><span data-stu-id="7aa17-177">Boolean</span></span>|<span data-ttu-id="7aa17-178">Especifica si se permite el cifrado de Azure RMS para WIP.</span><span class="sxs-lookup"><span data-stu-id="7aa17-178">Specifies whether to allow Azure RMS encryption for WIP</span></span>|
|<span data-ttu-id="7aa17-179">iconsVisible</span><span class="sxs-lookup"><span data-stu-id="7aa17-179">iconsVisible</span></span>|<span data-ttu-id="7aa17-180">Booleano</span><span class="sxs-lookup"><span data-stu-id="7aa17-180">Boolean</span></span>|<span data-ttu-id="7aa17-181">Determina si se agregan las superposiciones a los iconos para los archivos protegidos mediante WIP en Explorer y en los iconos de aplicación solo de empresa en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="7aa17-181">Determines whether overlays are added to icons for WIP protected files in Explorer and enterprise only app tiles in the Start menu.</span></span> <span data-ttu-id="7aa17-182">A partir de Windows 10, versión 1703, estos ajustes también configuran la visibilidad del icono de WIP en la barra de título de una aplicación protegida mediante WIP</span><span class="sxs-lookup"><span data-stu-id="7aa17-182">Starting in Windows 10, version 1703 this setting also configures the visibility of the WIP icon in the title bar of a WIP-protected app</span></span>|
|<span data-ttu-id="7aa17-183">protectedApps</span><span class="sxs-lookup"><span data-stu-id="7aa17-183">protectedApps</span></span>|<span data-ttu-id="7aa17-184">Colección [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="7aa17-184">[windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="7aa17-185">Las aplicaciones protegidas pueden tener acceso a datos empresariales y los datos controlados por dichas aplicaciones están protegidos mediante cifrado</span><span class="sxs-lookup"><span data-stu-id="7aa17-185">Protected applications can access enterprise data and the data handled by those applications are protected with encryption</span></span>|
|<span data-ttu-id="7aa17-186">exemptApps</span><span class="sxs-lookup"><span data-stu-id="7aa17-186">exemptApps</span></span>|<span data-ttu-id="7aa17-187">Colección [windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md)</span><span class="sxs-lookup"><span data-stu-id="7aa17-187">[windowsInformationProtectionApp](../resources/intune-mam-windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="7aa17-188">Las aplicaciones exentas también pueden tener acceso a datos empresariales, pero los datos controlados por dichas aplicaciones no están protegidos.</span><span class="sxs-lookup"><span data-stu-id="7aa17-188">Exempt applications can also access enterprise data, but the data handled by those applications are not protected.</span></span> <span data-ttu-id="7aa17-189">Esto ocurre porque algunas aplicaciones empresariales críticas podrían tener problemas de compatibilidad con los datos cifrados.</span><span class="sxs-lookup"><span data-stu-id="7aa17-189">This is because some critical enterprise applications may have compatibility problems with encrypted data.</span></span>|
|<span data-ttu-id="7aa17-190">enterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="7aa17-190">enterpriseNetworkDomainNames</span></span>|<span data-ttu-id="7aa17-191">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="7aa17-191">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="7aa17-192">Esta es la lista de dominios que forman parte de los límites de la empresa.</span><span class="sxs-lookup"><span data-stu-id="7aa17-192">This is the list of domains that comprise the boundaries of the enterprise.</span></span> <span data-ttu-id="7aa17-193">Los datos de uno de estos dominios que se envíen a un dispositivo se considerarán datos empresariales y protegidos. Estas ubicaciones se consideran un destino seguro con el que compartir datos empresariales</span><span class="sxs-lookup"><span data-stu-id="7aa17-193">Data from one of these domains that is sent to a device will be considered enterprise data and protected These locations will be considered a safe destination for enterprise data to be shared to</span></span>|
|<span data-ttu-id="7aa17-194">enterpriseProxiedDomains</span><span class="sxs-lookup"><span data-stu-id="7aa17-194">enterpriseProxiedDomains</span></span>|<span data-ttu-id="7aa17-195">Colección [windowsInformationProtectionProxiedDomainCollection](../resources/intune-mam-windowsinformationprotectionproxieddomaincollection.md)</span><span class="sxs-lookup"><span data-stu-id="7aa17-195">[windowsInformationProtectionProxiedDomainCollection](../resources/intune-mam-windowsinformationprotectionproxieddomaincollection.md) collection</span></span>|<span data-ttu-id="7aa17-196">Contiene una lista de dominios de recursos empresariales hospedados en la nube que necesitan protección.</span><span class="sxs-lookup"><span data-stu-id="7aa17-196">Contains a list of Enterprise resource domains hosted in the cloud that need to be protected.</span></span> <span data-ttu-id="7aa17-197">Las conexiones a estos recursos se consideran datos empresariales.</span><span class="sxs-lookup"><span data-stu-id="7aa17-197">Connections to these resources are considered enterprise data.</span></span> <span data-ttu-id="7aa17-198">Si un proxy se corresponde con un recurso de nube, el tráfico al recurso de la nube se dirigirá a través de la red empresarial mediante el servidor proxy indicado (en el puerto 80).</span><span class="sxs-lookup"><span data-stu-id="7aa17-198">If a proxy is paired with a cloud resource, traffic to the cloud resource will be routed through the enterprise network via the denoted proxy server (on Port 80).</span></span> <span data-ttu-id="7aa17-199">Un servidor proxy que se use para este propósito también debe configurarse mediante la directiva EnterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="7aa17-199">A proxy server used for this purpose must also be configured using the EnterpriseInternalProxyServers policy</span></span>|
|<span data-ttu-id="7aa17-200">enterpriseIPRanges</span><span class="sxs-lookup"><span data-stu-id="7aa17-200">enterpriseIPRanges</span></span>|<span data-ttu-id="7aa17-201">Colección [windowsInformationProtectionIPRangeCollection](../resources/intune-mam-windowsinformationprotectioniprangecollection.md)</span><span class="sxs-lookup"><span data-stu-id="7aa17-201">[windowsInformationProtectionIPRangeCollection](../resources/intune-mam-windowsinformationprotectioniprangecollection.md) collection</span></span>|<span data-ttu-id="7aa17-202">Establece los intervalos IP empresariales que definen los equipos de la red empresarial.</span><span class="sxs-lookup"><span data-stu-id="7aa17-202">Sets the enterprise IP ranges that define the computers in the enterprise network.</span></span> <span data-ttu-id="7aa17-203">Los datos que provienen de dichos equipos se consideran parte de la empresa y están protegidos.</span><span class="sxs-lookup"><span data-stu-id="7aa17-203">Data that comes from those computers will be considered part of the enterprise and protected.</span></span> <span data-ttu-id="7aa17-204">Estas ubicaciones se consideran un destino seguro en el que compartir datos empresariales</span><span class="sxs-lookup"><span data-stu-id="7aa17-204">These locations will be considered a safe destination for enterprise data to be shared to</span></span>|
|<span data-ttu-id="7aa17-205">enterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="7aa17-205">enterpriseIPRangesAreAuthoritative</span></span>|<span data-ttu-id="7aa17-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="7aa17-206">Boolean</span></span>|<span data-ttu-id="7aa17-207">Valor booleano que indica al cliente que acepte la lista configurada y que no use la heurística para intentar buscar otras subredes.</span><span class="sxs-lookup"><span data-stu-id="7aa17-207">Boolean value that tells the client to accept the configured list and not to use heuristics to attempt to find other subnets.</span></span> <span data-ttu-id="7aa17-208">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="7aa17-208">Default is false</span></span>|
|<span data-ttu-id="7aa17-209">enterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="7aa17-209">enterpriseProxyServers</span></span>|<span data-ttu-id="7aa17-210">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="7aa17-210">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="7aa17-211">Esta es una lista de servidores proxy.</span><span class="sxs-lookup"><span data-stu-id="7aa17-211">This is a list of proxy servers.</span></span> <span data-ttu-id="7aa17-212">Cualquier servidor que no esté en esta lista se considera no empresarial</span><span class="sxs-lookup"><span data-stu-id="7aa17-212">Any server not on this list is considered non-enterprise</span></span>|
|<span data-ttu-id="7aa17-213">enterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="7aa17-213">enterpriseInternalProxyServers</span></span>|<span data-ttu-id="7aa17-214">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="7aa17-214">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="7aa17-215">Se trata de la lista de valores separados por comas de servidores proxy internos.</span><span class="sxs-lookup"><span data-stu-id="7aa17-215">This is the comma-separated list of internal proxy servers.</span></span> <span data-ttu-id="7aa17-216">Por ejemplo, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span><span class="sxs-lookup"><span data-stu-id="7aa17-216">For example, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span></span> <span data-ttu-id="7aa17-217">El administrador ha configurado estos servidores proxy para que se conecten a los recursos específicos de Internet.</span><span class="sxs-lookup"><span data-stu-id="7aa17-217">These proxies have been configured by the admin to connect to specific resources on the Internet.</span></span> <span data-ttu-id="7aa17-218">Se consideran ubicaciones de red empresarial.</span><span class="sxs-lookup"><span data-stu-id="7aa17-218">They are considered to be enterprise network locations.</span></span> <span data-ttu-id="7aa17-219">Los servidores proxy solo se usan para configurar la directiva EnterpriseProxiedDomains para forzar el tráfico a los dominios coincidentes mediante estos proxy</span><span class="sxs-lookup"><span data-stu-id="7aa17-219">The proxies are only leveraged in configuring the EnterpriseProxiedDomains policy to force traffic to the matched domains through these proxies</span></span>|
|<span data-ttu-id="7aa17-220">enterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="7aa17-220">enterpriseProxyServersAreAuthoritative</span></span>|<span data-ttu-id="7aa17-221">Booleano</span><span class="sxs-lookup"><span data-stu-id="7aa17-221">Boolean</span></span>|<span data-ttu-id="7aa17-222">Valor booleano que indica al cliente que acepte la lista de configuración de servidores proxy y no intente detectar otros servidores proxy de trabajo.</span><span class="sxs-lookup"><span data-stu-id="7aa17-222">Boolean value that tells the client to accept the configured list of proxies and not try to detect other work proxies.</span></span> <span data-ttu-id="7aa17-223">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="7aa17-223">Default is false</span></span>|
|<span data-ttu-id="7aa17-224">neutralDomainResources</span><span class="sxs-lookup"><span data-stu-id="7aa17-224">neutralDomainResources</span></span>|<span data-ttu-id="7aa17-225">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="7aa17-225">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="7aa17-226">Lista de nombres de dominio que se pueden usar para el recurso de trabajo o personal</span><span class="sxs-lookup"><span data-stu-id="7aa17-226">List of domain names that can used for work or personal resource</span></span>|
|<span data-ttu-id="7aa17-227">indexingEncryptedStoresOrItemsBlocked</span><span class="sxs-lookup"><span data-stu-id="7aa17-227">indexingEncryptedStoresOrItemsBlocked</span></span>|<span data-ttu-id="7aa17-228">Booleano</span><span class="sxs-lookup"><span data-stu-id="7aa17-228">Boolean</span></span>|<span data-ttu-id="7aa17-229">Esta opción es para que el indexador de Windows Search permita o impida la indexación de los elementos</span><span class="sxs-lookup"><span data-stu-id="7aa17-229">This switch is for the Windows Search Indexer, to allow or disallow indexing of items</span></span>|
|<span data-ttu-id="7aa17-230">smbAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="7aa17-230">smbAutoEncryptedFileExtensions</span></span>|<span data-ttu-id="7aa17-231">Colección [windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md)</span><span class="sxs-lookup"><span data-stu-id="7aa17-231">[windowsInformationProtectionResourceCollection](../resources/intune-mam-windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="7aa17-232">Especifica una lista de extensiones de archivo, para que los archivos con estas extensiones se cifren cuando se copian desde un recurso compartido de SMB dentro del límite de la empresa</span><span class="sxs-lookup"><span data-stu-id="7aa17-232">Specifies a list of file extensions, so that files with these extensions are encrypted when copying from an SMB share within the corporate boundary</span></span>|
|<span data-ttu-id="7aa17-233">isAssigned</span><span class="sxs-lookup"><span data-stu-id="7aa17-233">isAssigned</span></span>|<span data-ttu-id="7aa17-234">Booleano</span><span class="sxs-lookup"><span data-stu-id="7aa17-234">Boolean</span></span>|<span data-ttu-id="7aa17-235">Indica si la directiva se implementará en los grupos de inclusión o no.</span><span class="sxs-lookup"><span data-stu-id="7aa17-235">Indicates if the policy is deployed to any inclusion groups or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7aa17-236">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7aa17-236">Relationships</span></span>
|<span data-ttu-id="7aa17-237">Relación</span><span class="sxs-lookup"><span data-stu-id="7aa17-237">Relationship</span></span>|<span data-ttu-id="7aa17-238">Tipo</span><span class="sxs-lookup"><span data-stu-id="7aa17-238">Type</span></span>|<span data-ttu-id="7aa17-239">Descripción</span><span class="sxs-lookup"><span data-stu-id="7aa17-239">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7aa17-240">protectedAppLockerFiles</span><span class="sxs-lookup"><span data-stu-id="7aa17-240">protectedAppLockerFiles</span></span>|<span data-ttu-id="7aa17-241">Colección [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md)</span><span class="sxs-lookup"><span data-stu-id="7aa17-241">[windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) collection</span></span>|<span data-ttu-id="7aa17-242">Otra forma de introducir aplicaciones protegidas mediante archivos XML</span><span class="sxs-lookup"><span data-stu-id="7aa17-242">Another way to input protected apps through xml files</span></span>|
|<span data-ttu-id="7aa17-243">exemptAppLockerFiles</span><span class="sxs-lookup"><span data-stu-id="7aa17-243">exemptAppLockerFiles</span></span>|<span data-ttu-id="7aa17-244">Colección [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md)</span><span class="sxs-lookup"><span data-stu-id="7aa17-244">[windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) collection</span></span>|<span data-ttu-id="7aa17-245">Otra forma de introducir aplicaciones exentas mediante archivos XML</span><span class="sxs-lookup"><span data-stu-id="7aa17-245">Another way to input exempt apps through xml files</span></span>|
|<span data-ttu-id="7aa17-246">asignaciones</span><span class="sxs-lookup"><span data-stu-id="7aa17-246">assignments</span></span>|<span data-ttu-id="7aa17-247">Colección [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md)</span><span class="sxs-lookup"><span data-stu-id="7aa17-247">[targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) collection</span></span>|<span data-ttu-id="7aa17-248">Propiedad de navegación a la lista de grupos de seguridad destinados a la directiva.</span><span class="sxs-lookup"><span data-stu-id="7aa17-248">Navigation property to list of security groups targeted for policy.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7aa17-249">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7aa17-249">JSON Representation</span></span>
<span data-ttu-id="7aa17-250">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7aa17-250">Here is a JSON representation of the resource.</span></span>
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
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "String",
      "description": "String",
      "publisherName": "String",
      "productName": "String",
      "denied": true
    }
  ],
  "exemptApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
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






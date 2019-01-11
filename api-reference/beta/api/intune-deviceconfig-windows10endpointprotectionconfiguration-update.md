---
title: Actualizar windows10EndpointProtectionConfiguration
description: Actualice las propiedades de un objeto windows10EndpointProtectionConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: edf38ba5b7bf308bfa2cd70846b310ca86f6758f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875561"
---
# <a name="update-windows10endpointprotectionconfiguration"></a><span data-ttu-id="68e0a-103">Actualizar windows10EndpointProtectionConfiguration</span><span class="sxs-lookup"><span data-stu-id="68e0a-103">Update windows10EndpointProtectionConfiguration</span></span>

> <span data-ttu-id="68e0a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="68e0a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="68e0a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="68e0a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="68e0a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="68e0a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="68e0a-107">Actualice las propiedades de un objeto [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="68e0a-107">Update the properties of a [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="68e0a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="68e0a-108">Prerequisites</span></span>
<span data-ttu-id="68e0a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="68e0a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="68e0a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="68e0a-111">Permission type</span></span>|<span data-ttu-id="68e0a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="68e0a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="68e0a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="68e0a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="68e0a-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="68e0a-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="68e0a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="68e0a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="68e0a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="68e0a-116">Not supported.</span></span>|
|<span data-ttu-id="68e0a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="68e0a-117">Application</span></span>|<span data-ttu-id="68e0a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="68e0a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="68e0a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="68e0a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="68e0a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="68e0a-120">Request headers</span></span>
|<span data-ttu-id="68e0a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68e0a-121">Header</span></span>|<span data-ttu-id="68e0a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="68e0a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="68e0a-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="68e0a-123">Authorization</span></span>|<span data-ttu-id="68e0a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="68e0a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="68e0a-125">Accept</span><span class="sxs-lookup"><span data-stu-id="68e0a-125">Accept</span></span>|<span data-ttu-id="68e0a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="68e0a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="68e0a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="68e0a-127">Request body</span></span>
<span data-ttu-id="68e0a-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="68e0a-128">In the request body, supply a JSON representation for the [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md) object.</span></span>

<span data-ttu-id="68e0a-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="68e0a-129">The following table shows the properties that are required when you create the [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).</span></span>

|<span data-ttu-id="68e0a-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="68e0a-130">Property</span></span>|<span data-ttu-id="68e0a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="68e0a-131">Type</span></span>|<span data-ttu-id="68e0a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="68e0a-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="68e0a-133">id</span><span class="sxs-lookup"><span data-stu-id="68e0a-133">id</span></span>|<span data-ttu-id="68e0a-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="68e0a-134">String</span></span>|<span data-ttu-id="68e0a-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="68e0a-135">Key of the entity.</span></span> <span data-ttu-id="68e0a-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="68e0a-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="68e0a-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="68e0a-137">lastModifiedDateTime</span></span>|<span data-ttu-id="68e0a-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="68e0a-138">DateTimeOffset</span></span>|<span data-ttu-id="68e0a-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="68e0a-139">DateTime the object was last modified.</span></span> <span data-ttu-id="68e0a-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="68e0a-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="68e0a-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="68e0a-141">roleScopeTagIds</span></span>|<span data-ttu-id="68e0a-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="68e0a-142">String collection</span></span>|<span data-ttu-id="68e0a-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="68e0a-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="68e0a-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="68e0a-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="68e0a-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="68e0a-145">supportsScopeTags</span></span>|<span data-ttu-id="68e0a-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-146">Boolean</span></span>|<span data-ttu-id="68e0a-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="68e0a-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="68e0a-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="68e0a-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="68e0a-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="68e0a-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="68e0a-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="68e0a-150">This property is read-only.</span></span> <span data-ttu-id="68e0a-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="68e0a-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="68e0a-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="68e0a-152">createdDateTime</span></span>|<span data-ttu-id="68e0a-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="68e0a-153">DateTimeOffset</span></span>|<span data-ttu-id="68e0a-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="68e0a-154">DateTime the object was created.</span></span> <span data-ttu-id="68e0a-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="68e0a-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="68e0a-156">descripción</span><span class="sxs-lookup"><span data-stu-id="68e0a-156">description</span></span>|<span data-ttu-id="68e0a-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="68e0a-157">String</span></span>|<span data-ttu-id="68e0a-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68e0a-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="68e0a-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="68e0a-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="68e0a-160">displayName</span><span class="sxs-lookup"><span data-stu-id="68e0a-160">displayName</span></span>|<span data-ttu-id="68e0a-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="68e0a-161">String</span></span>|<span data-ttu-id="68e0a-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68e0a-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="68e0a-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="68e0a-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="68e0a-164">version</span><span class="sxs-lookup"><span data-stu-id="68e0a-164">version</span></span>|<span data-ttu-id="68e0a-165">Int32</span><span class="sxs-lookup"><span data-stu-id="68e0a-165">Int32</span></span>|<span data-ttu-id="68e0a-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68e0a-166">Version of the device configuration.</span></span> <span data-ttu-id="68e0a-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="68e0a-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="68e0a-168">userRightsAccessCredentialManagerAsTrustedCaller</span><span class="sxs-lookup"><span data-stu-id="68e0a-168">userRightsAccessCredentialManagerAsTrustedCaller</span></span>|[<span data-ttu-id="68e0a-169">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-169">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-170">Este derecho de usuario se utiliza por el Administrador de credenciales durante la copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="68e0a-170">This user right is used by Credential Manager during Backup/Restore.</span></span> <span data-ttu-id="68e0a-171">Las credenciales guardadas de los usuarios podrían verse comprometidas si este privilegio se concede a otras entidades.</span><span class="sxs-lookup"><span data-stu-id="68e0a-171">Users' saved credentials might be compromised if this privilege is given to other entities.</span></span> <span data-ttu-id="68e0a-172">Se admiten sólo los Estados no configurado y permitido</span><span class="sxs-lookup"><span data-stu-id="68e0a-172">Only states NotConfigured and Allowed are supported</span></span>|
|<span data-ttu-id="68e0a-173">userRightsAllowAccessFromNetwork</span><span class="sxs-lookup"><span data-stu-id="68e0a-173">userRightsAllowAccessFromNetwork</span></span>|[<span data-ttu-id="68e0a-174">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-174">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-175">Este derecho de usuario determina qué usuarios y grupos tienen permiso para conectarse al equipo a través de la red.</span><span class="sxs-lookup"><span data-stu-id="68e0a-175">This user right determines which users and groups are allowed to connect to the computer over the network.</span></span> <span data-ttu-id="68e0a-176">Es compatible con el estado permitido.</span><span class="sxs-lookup"><span data-stu-id="68e0a-176">State Allowed is supported.</span></span>|
|<span data-ttu-id="68e0a-177">userRightsBlockAccessFromNetwork</span><span class="sxs-lookup"><span data-stu-id="68e0a-177">userRightsBlockAccessFromNetwork</span></span>|[<span data-ttu-id="68e0a-178">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-178">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-179">Este derecho de usuario determina qué usuarios y grupos son el bloque de conectar con el equipo a través de la red.</span><span class="sxs-lookup"><span data-stu-id="68e0a-179">This user right determines which users and groups are block from connecting to the computer over the network.</span></span> <span data-ttu-id="68e0a-180">Se admite el bloque de estado.</span><span class="sxs-lookup"><span data-stu-id="68e0a-180">State Block is supported.</span></span>|
|<span data-ttu-id="68e0a-181">userRightsActAsPartOfTheOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="68e0a-181">userRightsActAsPartOfTheOperatingSystem</span></span>|[<span data-ttu-id="68e0a-182">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-182">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-183">Este derecho de usuario permite a un proceso suplantar a cualquier usuario sin autenticación.</span><span class="sxs-lookup"><span data-stu-id="68e0a-183">This user right allows a process to impersonate any user without authentication.</span></span> <span data-ttu-id="68e0a-184">El proceso por lo tanto, puede obtener acceso a los mismos recursos locales que dicho usuario.</span><span class="sxs-lookup"><span data-stu-id="68e0a-184">The process can therefore gain access to the same local resources as that user.</span></span> <span data-ttu-id="68e0a-185">Se admiten sólo los Estados no configurado y permitido</span><span class="sxs-lookup"><span data-stu-id="68e0a-185">Only states NotConfigured and Allowed are supported</span></span>|
|<span data-ttu-id="68e0a-186">userRightsLocalLogOn</span><span class="sxs-lookup"><span data-stu-id="68e0a-186">userRightsLocalLogOn</span></span>|[<span data-ttu-id="68e0a-187">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-187">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-188">Este derecho de usuario determina qué usuarios pueden iniciar sesión en el equipo.</span><span class="sxs-lookup"><span data-stu-id="68e0a-188">This user right determines which users can log on to the computer.</span></span> <span data-ttu-id="68e0a-189">No configurado Estados, permitidos y bloqueados se admiten</span><span class="sxs-lookup"><span data-stu-id="68e0a-189">States NotConfigured, Allowed and Blocked are all supported</span></span> |
|<span data-ttu-id="68e0a-190">userRightsBackupData</span><span class="sxs-lookup"><span data-stu-id="68e0a-190">userRightsBackupData</span></span>|[<span data-ttu-id="68e0a-191">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-191">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-192">Este derecho de usuario determina qué usuarios pueden omitir archivo, directorio, registro y otros permisos de objetos persistentes al realizar copias de seguridad de archivos y directorios.</span><span class="sxs-lookup"><span data-stu-id="68e0a-192">This user right determines which users can bypass file, directory, registry, and other persistent objects permissions when backing up files and directories.</span></span> <span data-ttu-id="68e0a-193">Se admiten sólo los Estados no configurado y permitido</span><span class="sxs-lookup"><span data-stu-id="68e0a-193">Only states NotConfigured and Allowed are supported</span></span>|
|<span data-ttu-id="68e0a-194">userRightsChangeSystemTime</span><span class="sxs-lookup"><span data-stu-id="68e0a-194">userRightsChangeSystemTime</span></span>|[<span data-ttu-id="68e0a-195">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-195">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-196">Este derecho de usuario determina qué usuarios y grupos pueden cambiar la hora y la fecha del reloj interno del equipo.</span><span class="sxs-lookup"><span data-stu-id="68e0a-196">This user right determines which users and groups can change the time and date on the internal clock of the computer.</span></span> <span data-ttu-id="68e0a-197">Se admiten sólo los Estados no configurado y permitido</span><span class="sxs-lookup"><span data-stu-id="68e0a-197">Only states NotConfigured and Allowed are supported</span></span>|
|<span data-ttu-id="68e0a-198">userRightsCreateGlobalObjects</span><span class="sxs-lookup"><span data-stu-id="68e0a-198">userRightsCreateGlobalObjects</span></span>|[<span data-ttu-id="68e0a-199">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-199">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-200">Esta configuración de seguridad determina si los usuarios pueden crear objetos globales que están disponibles para todas las sesiones.</span><span class="sxs-lookup"><span data-stu-id="68e0a-200">This security setting determines whether users can create global objects that are available to all sessions.</span></span> <span data-ttu-id="68e0a-201">Los usuarios que pueden crear objetos globales pueden afectar a los procesos que se ejecutan en sesiones de otros usuarios, lo que podrían provocar daños de error o datos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="68e0a-201">Users who can create global objects could affect processes that run under other users' sessions, which could lead to application failure or data corruption.</span></span> <span data-ttu-id="68e0a-202">Se admiten sólo los Estados no configurado y permitido</span><span class="sxs-lookup"><span data-stu-id="68e0a-202">Only states NotConfigured and Allowed are supported</span></span>|
|<span data-ttu-id="68e0a-203">userRightsCreatePageFile</span><span class="sxs-lookup"><span data-stu-id="68e0a-203">userRightsCreatePageFile</span></span>|[<span data-ttu-id="68e0a-204">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-204">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-205">Este derecho de usuario determina qué usuarios y grupos pueden llamar a una API interna para crear y cambiar el tamaño de un archivo de página.</span><span class="sxs-lookup"><span data-stu-id="68e0a-205">This user right determines which users and groups can call an internal API to create and change the size of a page file.</span></span> <span data-ttu-id="68e0a-206">Se admiten sólo los Estados no configurado y permitido</span><span class="sxs-lookup"><span data-stu-id="68e0a-206">Only states NotConfigured and Allowed are supported</span></span>|
|<span data-ttu-id="68e0a-207">userRightsCreatePermanentSharedObjects</span><span class="sxs-lookup"><span data-stu-id="68e0a-207">userRightsCreatePermanentSharedObjects</span></span>|[<span data-ttu-id="68e0a-208">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-208">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-209">Este derecho de usuario determina qué cuentas pueden usarse por los procesos para crear un objeto de Active directory con el objeto administrador.</span><span class="sxs-lookup"><span data-stu-id="68e0a-209">This user right determines which accounts can be used by processes to create a directory object using the object manager.</span></span> <span data-ttu-id="68e0a-210">Se admiten sólo los Estados no configurado y permitido</span><span class="sxs-lookup"><span data-stu-id="68e0a-210">Only states NotConfigured and Allowed are supported</span></span>|
|<span data-ttu-id="68e0a-211">userRightsCreateSymbolicLinks</span><span class="sxs-lookup"><span data-stu-id="68e0a-211">userRightsCreateSymbolicLinks</span></span>|[<span data-ttu-id="68e0a-212">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-212">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-213">Este derecho de usuario determina si el usuario puede crear un vínculo simbólico desde el equipo a la que se registran en.</span><span class="sxs-lookup"><span data-stu-id="68e0a-213">This user right determines if the user can create a symbolic link from the computer to which they are logged on.</span></span> <span data-ttu-id="68e0a-214">Se admiten sólo los Estados no configurado y permitido</span><span class="sxs-lookup"><span data-stu-id="68e0a-214">Only states NotConfigured and Allowed are supported</span></span>|
|<span data-ttu-id="68e0a-215">userRightsCreateToken</span><span class="sxs-lookup"><span data-stu-id="68e0a-215">userRightsCreateToken</span></span>|[<span data-ttu-id="68e0a-216">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-216">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-217">Este derecho de usuario determina qué usuarios o grupos pueden usarse por procesos para crear un símbolo (token) que puede usarse para obtener acceso a cualquier recurso local cuando el proceso utiliza una API interna para crear un token de acceso.</span><span class="sxs-lookup"><span data-stu-id="68e0a-217">This user right determines which users/groups can be used by processes to create a token that can then be used to get access to any local resources when the process uses an internal API to create an access token.</span></span> <span data-ttu-id="68e0a-218">Se admiten sólo los Estados no configurado y permitido</span><span class="sxs-lookup"><span data-stu-id="68e0a-218">Only states NotConfigured and Allowed are supported</span></span>|
|<span data-ttu-id="68e0a-219">userRightsDebugPrograms</span><span class="sxs-lookup"><span data-stu-id="68e0a-219">userRightsDebugPrograms</span></span>|[<span data-ttu-id="68e0a-220">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-220">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-221">Este derecho de usuario determina qué usuarios pueden adjuntar un depurador a cualquier proceso o al kernel.</span><span class="sxs-lookup"><span data-stu-id="68e0a-221">This user right determines which users can attach a debugger to any process or to the kernel.</span></span> <span data-ttu-id="68e0a-222">Se admiten sólo los Estados no configurado y permitido</span><span class="sxs-lookup"><span data-stu-id="68e0a-222">Only states NotConfigured and Allowed are supported</span></span>|
|<span data-ttu-id="68e0a-223">userRightsRemoteDesktopServicesLogOn</span><span class="sxs-lookup"><span data-stu-id="68e0a-223">userRightsRemoteDesktopServicesLogOn</span></span>|[<span data-ttu-id="68e0a-224">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-224">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-225">Este derecho de usuario determina qué usuarios y grupos no pueden iniciar sesión como un cliente de servicios de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="68e0a-225">This user right determines which users and groups are prohibited from logging on as a Remote Desktop Services client.</span></span> <span data-ttu-id="68e0a-226">Se admiten sólo los Estados no configurado y bloqueado</span><span class="sxs-lookup"><span data-stu-id="68e0a-226">Only states NotConfigured and Blocked are supported</span></span>|
|<span data-ttu-id="68e0a-227">userRightsDelegation</span><span class="sxs-lookup"><span data-stu-id="68e0a-227">userRightsDelegation</span></span>|[<span data-ttu-id="68e0a-228">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-228">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-229">Este derecho de usuario determina qué usuarios pueden establecer la opción de confianza para la delegación en un objeto de usuario o equipo.</span><span class="sxs-lookup"><span data-stu-id="68e0a-229">This user right determines which users can set the Trusted for Delegation setting on a user or computer object.</span></span> <span data-ttu-id="68e0a-230">Se admiten sólo los Estados no configurado y permitidos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-230">Only states NotConfigured and Allowed are supported.</span></span>|
|<span data-ttu-id="68e0a-231">userRightsGenerateSecurityAudits</span><span class="sxs-lookup"><span data-stu-id="68e0a-231">userRightsGenerateSecurityAudits</span></span>|[<span data-ttu-id="68e0a-232">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-232">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-233">Este derecho de usuario determina qué cuentas se pueden usar un proceso para agregar entradas al registro de seguridad.</span><span class="sxs-lookup"><span data-stu-id="68e0a-233">This user right determines which accounts can be used by a process to add entries to the security log.</span></span> <span data-ttu-id="68e0a-234">El registro de seguridad se usa para el seguimiento de acceso al sistema no autorizado.</span><span class="sxs-lookup"><span data-stu-id="68e0a-234">The security log is used to trace unauthorized system access.</span></span>  <span data-ttu-id="68e0a-235">Se admiten sólo los Estados no configurado y permitidos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-235">Only states NotConfigured and Allowed are supported.</span></span>|
|<span data-ttu-id="68e0a-236">userRightsImpersonateClient</span><span class="sxs-lookup"><span data-stu-id="68e0a-236">userRightsImpersonateClient</span></span>|[<span data-ttu-id="68e0a-237">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-237">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-238">Asignar este derecho de usuario a un usuario permite programas que se ejecutan en nombre de ese usuario para suplantar a un cliente.</span><span class="sxs-lookup"><span data-stu-id="68e0a-238">Assigning this user right to a user allows programs running on behalf of that user to impersonate a client.</span></span> <span data-ttu-id="68e0a-239">Necesidad de utilizar este derecho de usuario para este tipo de suplantación impide que un usuario no autorizado convencer a un cliente para conectarse a un servicio que ha creado y, a continuación, suplantar a dicho cliente, lo que puede elevar los permisos no autorizados del usuario a administrativas o niveles de sistema.</span><span class="sxs-lookup"><span data-stu-id="68e0a-239">Requiring this user right for this kind of impersonation prevents an unauthorized user from convincing a client to connect to a service that they have created and then impersonating that client, which can elevate the unauthorized user's permissions to administrative or system levels.</span></span> <span data-ttu-id="68e0a-240">Se admiten sólo los Estados no configurado y permitidos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-240">Only states NotConfigured and Allowed are supported.</span></span>|
|<span data-ttu-id="68e0a-241">userRightsIncreaseSchedulingPriority</span><span class="sxs-lookup"><span data-stu-id="68e0a-241">userRightsIncreaseSchedulingPriority</span></span>|[<span data-ttu-id="68e0a-242">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-242">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-243">Este derecho de usuario determina qué cuentas pueden utilizar un proceso con acceso propiedad de escritura a otro proceso para aumentar la prioridad de ejecución asignada al otro proceso.</span><span class="sxs-lookup"><span data-stu-id="68e0a-243">This user right determines which accounts can use a process with Write Property access to another process to increase the execution priority assigned to the other process.</span></span> <span data-ttu-id="68e0a-244">Se admiten sólo los Estados no configurado y permitidos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-244">Only states NotConfigured and Allowed are supported.</span></span>|
|<span data-ttu-id="68e0a-245">userRightsLoadUnloadDrivers</span><span class="sxs-lookup"><span data-stu-id="68e0a-245">userRightsLoadUnloadDrivers</span></span>|[<span data-ttu-id="68e0a-246">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-246">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-247">Este derecho de usuario determina qué usuarios pueden cargar y descargar los controladores de dispositivos u otro código en modo de kernel.</span><span class="sxs-lookup"><span data-stu-id="68e0a-247">This user right determines which users can dynamically load and unload device drivers or other code in to kernel mode.</span></span> <span data-ttu-id="68e0a-248">Se admiten sólo los Estados no configurado y permitidos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-248">Only states NotConfigured and Allowed are supported.</span></span>|
|<span data-ttu-id="68e0a-249">userRightsLockMemory</span><span class="sxs-lookup"><span data-stu-id="68e0a-249">userRightsLockMemory</span></span>|[<span data-ttu-id="68e0a-250">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-250">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-251">Este derecho de usuario determina qué cuentas pueden utilizar un proceso para mantener los datos en la memoria física, lo que impide que el sistema de paginación de los datos de memoria virtual en el disco.</span><span class="sxs-lookup"><span data-stu-id="68e0a-251">This user right determines which accounts can use a process to keep data in physical memory, which prevents the system from paging the data to virtual memory on disk.</span></span> <span data-ttu-id="68e0a-252">Se admiten sólo los Estados no configurado y permitidos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-252">Only states NotConfigured and Allowed are supported.</span></span>|
|<span data-ttu-id="68e0a-253">userRightsManageAuditingAndSecurityLogs</span><span class="sxs-lookup"><span data-stu-id="68e0a-253">userRightsManageAuditingAndSecurityLogs</span></span>|[<span data-ttu-id="68e0a-254">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-254">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-255">Este derecho de usuario determina qué usuarios pueden especificar opciones para recursos individuales, como archivos, objetos de Active Directory y claves del registro de auditoría de acceso a objetos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-255">This user right determines which users can specify object access auditing options for individual resources, such as files, Active Directory objects, and registry keys.</span></span> <span data-ttu-id="68e0a-256">Se admiten sólo los Estados no configurado y permitidos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-256">Only states NotConfigured and Allowed are supported.</span></span>|
|<span data-ttu-id="68e0a-257">userRightsManageVolumes</span><span class="sxs-lookup"><span data-stu-id="68e0a-257">userRightsManageVolumes</span></span>|[<span data-ttu-id="68e0a-258">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-258">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-259">Este derecho de usuario determina qué usuarios y grupos pueden ejecutar tareas de mantenimiento en un volumen, como la desfragmentación remota.</span><span class="sxs-lookup"><span data-stu-id="68e0a-259">This user right determines which users and groups can run maintenance tasks on a volume, such as remote defragmentation.</span></span> <span data-ttu-id="68e0a-260">Se admiten sólo los Estados no configurado y permitidos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-260">Only states NotConfigured and Allowed are supported.</span></span>|
|<span data-ttu-id="68e0a-261">userRightsModifyFirmwareEnvironment</span><span class="sxs-lookup"><span data-stu-id="68e0a-261">userRightsModifyFirmwareEnvironment</span></span>|[<span data-ttu-id="68e0a-262">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-262">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-263">Este derecho de usuario determina quién puede modificar valores de entorno firmware.</span><span class="sxs-lookup"><span data-stu-id="68e0a-263">This user right determines who can modify firmware environment values.</span></span> <span data-ttu-id="68e0a-264">Se admiten sólo los Estados no configurado y permitidos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-264">Only states NotConfigured and Allowed are supported.</span></span>|
|<span data-ttu-id="68e0a-265">userRightsModifyObjectLabels</span><span class="sxs-lookup"><span data-stu-id="68e0a-265">userRightsModifyObjectLabels</span></span>|[<span data-ttu-id="68e0a-266">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-266">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-267">Este derecho de usuario determina qué cuentas de usuario pueden modificar la etiqueta de la integridad de los objetos, como archivos, claves del registro o procesos que pertenecen a otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="68e0a-267">This user right determines which user accounts can modify the integrity label of objects, such as files, registry keys, or processes owned by other users.</span></span> <span data-ttu-id="68e0a-268">Se admiten sólo los Estados no configurado y permitidos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-268">Only states NotConfigured and Allowed are supported.</span></span>|
|<span data-ttu-id="68e0a-269">userRightsProfileSingleProcess</span><span class="sxs-lookup"><span data-stu-id="68e0a-269">userRightsProfileSingleProcess</span></span>|[<span data-ttu-id="68e0a-270">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-270">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-271">Este derecho de usuario determina qué usuarios pueden utilizar herramientas de supervisión de rendimiento para supervisar el rendimiento de los procesos del sistema.</span><span class="sxs-lookup"><span data-stu-id="68e0a-271">This user right determines which users can use performance monitoring tools to monitor the performance of system processes.</span></span> <span data-ttu-id="68e0a-272">Se admiten sólo los Estados no configurado y permitidos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-272">Only states NotConfigured and Allowed are supported.</span></span>|
|<span data-ttu-id="68e0a-273">userRightsRemoteShutdown</span><span class="sxs-lookup"><span data-stu-id="68e0a-273">userRightsRemoteShutdown</span></span>|[<span data-ttu-id="68e0a-274">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-274">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-275">Este derecho de usuario determina qué usuarios pueden apagar un equipo desde una ubicación remota en la red.</span><span class="sxs-lookup"><span data-stu-id="68e0a-275">This user right determines which users are allowed to shut down a computer from a remote location on the network.</span></span> <span data-ttu-id="68e0a-276">Uso incorrecto de este derecho de usuario puede provocar una denegación de servicio.</span><span class="sxs-lookup"><span data-stu-id="68e0a-276">Misuse of this user right can result in a denial of service.</span></span> <span data-ttu-id="68e0a-277">Se admiten sólo los Estados no configurado y permitidos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-277">Only states NotConfigured and Allowed are supported.</span></span>|
|<span data-ttu-id="68e0a-278">userRightsRestoreData</span><span class="sxs-lookup"><span data-stu-id="68e0a-278">userRightsRestoreData</span></span>|[<span data-ttu-id="68e0a-279">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-279">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-280">Este derecho de usuario determina qué usuarios pueden omitir archivo, directorio, registro y otros objetos persistentes permisos al restaurar una copia de archivos y directorios y determina qué usuarios pueden establecer cualquier entidad de seguridad válida como propietario de un objeto.</span><span class="sxs-lookup"><span data-stu-id="68e0a-280">This user right determines which users can bypass file, directory, registry, and other persistent objects permissions when restoring backed up files and directories, and determines which users can set any valid security principal as the owner of an object.</span></span> <span data-ttu-id="68e0a-281">Se admiten sólo los Estados no configurado y permitidos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-281">Only states NotConfigured and Allowed are supported.</span></span>|
|<span data-ttu-id="68e0a-282">userRightsTakeOwnership</span><span class="sxs-lookup"><span data-stu-id="68e0a-282">userRightsTakeOwnership</span></span>|[<span data-ttu-id="68e0a-283">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-283">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-284">Este derecho de usuario determina qué usuarios pueden tomar posesión de cualquier objeto protegible en el sistema, incluidos los objetos de Active Directory, archivos y carpetas, impresoras, claves del registro, procesos y subprocesos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-284">This user right determines which users can take ownership of any securable object in the system, including Active Directory objects, files and folders, printers, registry keys, processes, and threads.</span></span> <span data-ttu-id="68e0a-285">Se admiten sólo los Estados no configurado y permitidos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-285">Only states NotConfigured and Allowed are supported.</span></span>|
|<span data-ttu-id="68e0a-286">userRightsRegisterProcessAsService</span><span class="sxs-lookup"><span data-stu-id="68e0a-286">userRightsRegisterProcessAsService</span></span>|[<span data-ttu-id="68e0a-287">deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="68e0a-287">deviceManagementUserRightsSetting</span></span>](../resources/intune-deviceconfig-devicemanagementuserrightssetting.md)|<span data-ttu-id="68e0a-288">Esta configuración de seguridad determina qué cuentas de servicio no se pueden registrar un proceso como un servicio.</span><span class="sxs-lookup"><span data-stu-id="68e0a-288">This security setting determines which service accounts are prevented from registering a process as a service.</span></span> <span data-ttu-id="68e0a-289">Nota: Esta configuración de seguridad no se aplica a las cuentas del sistema, servicio Local o servicio de red.</span><span class="sxs-lookup"><span data-stu-id="68e0a-289">Note: This security setting does not apply to the System, Local Service, or Network Service accounts.</span></span> <span data-ttu-id="68e0a-290">Se admite solo estado bloqueado.</span><span class="sxs-lookup"><span data-stu-id="68e0a-290">Only state Blocked is supported.</span></span>|
|<span data-ttu-id="68e0a-291">xboxServicesEnableXboxGameSaveTask</span><span class="sxs-lookup"><span data-stu-id="68e0a-291">xboxServicesEnableXboxGameSaveTask</span></span>|<span data-ttu-id="68e0a-292">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-292">Boolean</span></span>|<span data-ttu-id="68e0a-293">Esta configuración determina si guardar juego xbox está habilitado (1) o deshabilitado (0).</span><span class="sxs-lookup"><span data-stu-id="68e0a-293">This setting determines whether xbox game save is enabled (1) or disabled (0).</span></span>|
|<span data-ttu-id="68e0a-294">xboxServicesAccessoryManagementServiceStartupMode</span><span class="sxs-lookup"><span data-stu-id="68e0a-294">xboxServicesAccessoryManagementServiceStartupMode</span></span>|[<span data-ttu-id="68e0a-295">serviceStartType</span><span class="sxs-lookup"><span data-stu-id="68e0a-295">serviceStartType</span></span>](../resources/intune-deviceconfig-servicestarttype.md)|<span data-ttu-id="68e0a-296">Esta configuración determina si el tipo de inicio del servicio de administración de accesorio es Automatic(2), Manual(3), Disabled(4).</span><span class="sxs-lookup"><span data-stu-id="68e0a-296">This setting determines whether the Accessory management service's start type is Automatic(2), Manual(3), Disabled(4).</span></span> <span data-ttu-id="68e0a-297">Valor predeterminado: Manual.</span><span class="sxs-lookup"><span data-stu-id="68e0a-297">Default: Manual.</span></span> <span data-ttu-id="68e0a-298">Los valores posibles son: `manual`, `automatic` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-298">Possible values are: `manual`, `automatic`, `disabled`.</span></span>|
|<span data-ttu-id="68e0a-299">xboxServicesLiveAuthManagerServiceStartupMode</span><span class="sxs-lookup"><span data-stu-id="68e0a-299">xboxServicesLiveAuthManagerServiceStartupMode</span></span>|[<span data-ttu-id="68e0a-300">serviceStartType</span><span class="sxs-lookup"><span data-stu-id="68e0a-300">serviceStartType</span></span>](../resources/intune-deviceconfig-servicestarttype.md)|<span data-ttu-id="68e0a-301">Esta configuración determina si el tipo de inicio del servicio Live Auth Manager es Automatic(2), Manual(3), Disabled(4).</span><span class="sxs-lookup"><span data-stu-id="68e0a-301">This setting determines whether Live Auth Manager service's start type is Automatic(2), Manual(3), Disabled(4).</span></span> <span data-ttu-id="68e0a-302">Valor predeterminado: Manual.</span><span class="sxs-lookup"><span data-stu-id="68e0a-302">Default: Manual.</span></span> <span data-ttu-id="68e0a-303">Los valores posibles son: `manual`, `automatic` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-303">Possible values are: `manual`, `automatic`, `disabled`.</span></span>|
|<span data-ttu-id="68e0a-304">xboxServicesLiveGameSaveServiceStartupMode</span><span class="sxs-lookup"><span data-stu-id="68e0a-304">xboxServicesLiveGameSaveServiceStartupMode</span></span>|[<span data-ttu-id="68e0a-305">serviceStartType</span><span class="sxs-lookup"><span data-stu-id="68e0a-305">serviceStartType</span></span>](../resources/intune-deviceconfig-servicestarttype.md)|<span data-ttu-id="68e0a-306">Esta configuración determina si el juego Live guardar el tipo de inicio del servicio es Automatic(2), Manual(3), Disabled(4).</span><span class="sxs-lookup"><span data-stu-id="68e0a-306">This setting determines whether Live Game save service's start type is Automatic(2), Manual(3), Disabled(4).</span></span> <span data-ttu-id="68e0a-307">Valor predeterminado: Manual.</span><span class="sxs-lookup"><span data-stu-id="68e0a-307">Default: Manual.</span></span> <span data-ttu-id="68e0a-308">Los valores posibles son: `manual`, `automatic` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-308">Possible values are: `manual`, `automatic`, `disabled`.</span></span>|
|<span data-ttu-id="68e0a-309">xboxServicesLiveNetworkingServiceStartupMode</span><span class="sxs-lookup"><span data-stu-id="68e0a-309">xboxServicesLiveNetworkingServiceStartupMode</span></span>|[<span data-ttu-id="68e0a-310">serviceStartType</span><span class="sxs-lookup"><span data-stu-id="68e0a-310">serviceStartType</span></span>](../resources/intune-deviceconfig-servicestarttype.md)|<span data-ttu-id="68e0a-311">Esta configuración determina si el tipo de inicio del servicio de red es Automatic(2), Manual(3), Disabled(4).</span><span class="sxs-lookup"><span data-stu-id="68e0a-311">This setting determines whether Networking service's start type is Automatic(2), Manual(3), Disabled(4).</span></span> <span data-ttu-id="68e0a-312">Valor predeterminado: Manual.</span><span class="sxs-lookup"><span data-stu-id="68e0a-312">Default: Manual.</span></span> <span data-ttu-id="68e0a-313">Los valores posibles son: `manual`, `automatic` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-313">Possible values are: `manual`, `automatic`, `disabled`.</span></span>|
|<span data-ttu-id="68e0a-314">localSecurityOptionsBlockMicrosoftAccounts</span><span class="sxs-lookup"><span data-stu-id="68e0a-314">localSecurityOptionsBlockMicrosoftAccounts</span></span>|<span data-ttu-id="68e0a-315">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-315">Boolean</span></span>|<span data-ttu-id="68e0a-316">Impedir que los usuarios agreguen nuevas cuentas de Microsoft a este equipo.</span><span class="sxs-lookup"><span data-stu-id="68e0a-316">Prevent users from adding new Microsoft accounts to this computer.</span></span>|
|<span data-ttu-id="68e0a-317">localSecurityOptionsBlockRemoteLogonWithBlankPassword</span><span class="sxs-lookup"><span data-stu-id="68e0a-317">localSecurityOptionsBlockRemoteLogonWithBlankPassword</span></span>|<span data-ttu-id="68e0a-318">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-318">Boolean</span></span>|<span data-ttu-id="68e0a-319">Habilite las cuentas locales que no están protegido para iniciar sesión desde ubicaciones que no sean el dispositivo físico de contraseña. Es el comportamiento predeterminado</span><span class="sxs-lookup"><span data-stu-id="68e0a-319">Enable Local accounts that are not password protected to log on from locations other than the physical device.Default is enabled</span></span>|
|<span data-ttu-id="68e0a-320">localSecurityOptionsEnableAdministratorAccount</span><span class="sxs-lookup"><span data-stu-id="68e0a-320">localSecurityOptionsEnableAdministratorAccount</span></span>|<span data-ttu-id="68e0a-321">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-321">Boolean</span></span>|<span data-ttu-id="68e0a-322">Determina si la cuenta de administrador Local está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="68e0a-322">Determines whether the Local Administrator account is enabled or disabled.</span></span>|
|<span data-ttu-id="68e0a-323">localSecurityOptionsAdministratorAccountName</span><span class="sxs-lookup"><span data-stu-id="68e0a-323">localSecurityOptionsAdministratorAccountName</span></span>|<span data-ttu-id="68e0a-324">Cadena</span><span class="sxs-lookup"><span data-stu-id="68e0a-324">String</span></span>|<span data-ttu-id="68e0a-325">Definir un nombre de cuenta diferente que se asociará con el identificador de seguridad (SID) para la cuenta "Administrador".</span><span class="sxs-lookup"><span data-stu-id="68e0a-325">Define a different account name to be associated with the security identifier (SID) for the account “Administrator”.</span></span>|
|<span data-ttu-id="68e0a-326">localSecurityOptionsEnableGuestAccount</span><span class="sxs-lookup"><span data-stu-id="68e0a-326">localSecurityOptionsEnableGuestAccount</span></span>|<span data-ttu-id="68e0a-327">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-327">Boolean</span></span>|<span data-ttu-id="68e0a-328">Determina si la cuenta de invitado está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="68e0a-328">Determines if the Guest account is enabled or disabled.</span></span>|
|<span data-ttu-id="68e0a-329">localSecurityOptionsGuestAccountName</span><span class="sxs-lookup"><span data-stu-id="68e0a-329">localSecurityOptionsGuestAccountName</span></span>|<span data-ttu-id="68e0a-330">Cadena</span><span class="sxs-lookup"><span data-stu-id="68e0a-330">String</span></span>|<span data-ttu-id="68e0a-331">Definir un nombre de cuenta diferente que se asociará con el identificador de seguridad (SID) para la cuenta "Invitado".</span><span class="sxs-lookup"><span data-stu-id="68e0a-331">Define a different account name to be associated with the security identifier (SID) for the account “Guest”.</span></span>|
|<span data-ttu-id="68e0a-332">localSecurityOptionsAllowUndockWithoutHavingToLogon</span><span class="sxs-lookup"><span data-stu-id="68e0a-332">localSecurityOptionsAllowUndockWithoutHavingToLogon</span></span>|<span data-ttu-id="68e0a-333">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-333">Boolean</span></span>|<span data-ttu-id="68e0a-334">Impedir que se desacoplado sin tener que inicie sesión un equipo portátil.</span><span class="sxs-lookup"><span data-stu-id="68e0a-334">Prevent a portable computer from being undocked without having to log in.</span></span>|
|<span data-ttu-id="68e0a-335">localSecurityOptionsBlockUsersInstallingPrinterDrivers</span><span class="sxs-lookup"><span data-stu-id="68e0a-335">localSecurityOptionsBlockUsersInstallingPrinterDrivers</span></span>|<span data-ttu-id="68e0a-336">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-336">Boolean</span></span>|<span data-ttu-id="68e0a-337">Restringir instalar controladores de impresora como parte de la conexión a una impresora compartida a los administradores de únicamente.</span><span class="sxs-lookup"><span data-stu-id="68e0a-337">Restrict installing printer drivers as part of connecting to a shared printer to admins only.</span></span>|
|<span data-ttu-id="68e0a-338">localSecurityOptionsBlockRemoteOpticalDriveAccess</span><span class="sxs-lookup"><span data-stu-id="68e0a-338">localSecurityOptionsBlockRemoteOpticalDriveAccess</span></span>|<span data-ttu-id="68e0a-339">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-339">Boolean</span></span>|<span data-ttu-id="68e0a-340">Habilitación de esta configuración permite único usuario inició la sesión de forma interactiva a los medios de CD-ROM de access.</span><span class="sxs-lookup"><span data-stu-id="68e0a-340">Enabling this settings allows only interactively logged on user to access CD-ROM media.</span></span>|
|<span data-ttu-id="68e0a-341">localSecurityOptionsFormatAndEjectOfRemovableMediaAllowedUser</span><span class="sxs-lookup"><span data-stu-id="68e0a-341">localSecurityOptionsFormatAndEjectOfRemovableMediaAllowedUser</span></span>|[<span data-ttu-id="68e0a-342">localSecurityOptionsFormatAndEjectOfRemovableMediaAllowedUserType</span><span class="sxs-lookup"><span data-stu-id="68e0a-342">localSecurityOptionsFormatAndEjectOfRemovableMediaAllowedUserType</span></span>](../resources/intune-deviceconfig-localsecurityoptionsformatandejectofremovablemediaallowedusertype.md)|<span data-ttu-id="68e0a-343">Definir quién tiene permiso para formatear y expulsar medios NTFS extraíbles.</span><span class="sxs-lookup"><span data-stu-id="68e0a-343">Define who is allowed to format and eject removable NTFS media.</span></span> <span data-ttu-id="68e0a-344">Los valores posibles son: `notConfigured`, `administrators`, `administratorsAndPowerUsers` y `administratorsAndInteractiveUsers`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-344">Possible values are: `notConfigured`, `administrators`, `administratorsAndPowerUsers`, `administratorsAndInteractiveUsers`.</span></span>|
|<span data-ttu-id="68e0a-345">localSecurityOptionsMachineInactivityLimit</span><span class="sxs-lookup"><span data-stu-id="68e0a-345">localSecurityOptionsMachineInactivityLimit</span></span>|<span data-ttu-id="68e0a-346">Int32</span><span class="sxs-lookup"><span data-stu-id="68e0a-346">Int32</span></span>|<span data-ttu-id="68e0a-347">Definir el número máximo de minutos de inactividad en la pantalla de inicio de sesión del escritorio interactivo hasta que se ejecuta el protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="68e0a-347">Define maximum minutes of inactivity on the interactive desktop’s login screen until the screen saver runs.</span></span> <span data-ttu-id="68e0a-348">Valores válidos de 0 a 9999</span><span class="sxs-lookup"><span data-stu-id="68e0a-348">Valid values 0 to 9999</span></span>|
|<span data-ttu-id="68e0a-349">localSecurityOptionsMachineInactivityLimitInMinutes</span><span class="sxs-lookup"><span data-stu-id="68e0a-349">localSecurityOptionsMachineInactivityLimitInMinutes</span></span>|<span data-ttu-id="68e0a-350">Int32</span><span class="sxs-lookup"><span data-stu-id="68e0a-350">Int32</span></span>|<span data-ttu-id="68e0a-351">Definir el número máximo de minutos de inactividad en la pantalla de inicio de sesión del escritorio interactivo hasta que se ejecuta el protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="68e0a-351">Define maximum minutes of inactivity on the interactive desktop’s login screen until the screen saver runs.</span></span> <span data-ttu-id="68e0a-352">Valores válidos de 0 a 9999</span><span class="sxs-lookup"><span data-stu-id="68e0a-352">Valid values 0 to 9999</span></span>|
|<span data-ttu-id="68e0a-353">localSecurityOptionsDoNotRequireCtrlAltDel</span><span class="sxs-lookup"><span data-stu-id="68e0a-353">localSecurityOptionsDoNotRequireCtrlAltDel</span></span>|<span data-ttu-id="68e0a-354">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-354">Boolean</span></span>|<span data-ttu-id="68e0a-355">Requerir CTRL + ALT + SUPR que se debe presionar antes de que un usuario puede iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="68e0a-355">Require CTRL+ALT+DEL to be pressed before a user can log on.</span></span>|
|<span data-ttu-id="68e0a-356">localSecurityOptionsHideLastSignedInUser</span><span class="sxs-lookup"><span data-stu-id="68e0a-356">localSecurityOptionsHideLastSignedInUser</span></span>|<span data-ttu-id="68e0a-357">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-357">Boolean</span></span>|<span data-ttu-id="68e0a-358">No mostrar el nombre de usuario de la última persona que ha iniciado sesión en este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68e0a-358">Do not display the username of the last person who signed in on this device.</span></span>|
|<span data-ttu-id="68e0a-359">localSecurityOptionsHideUsernameAtSignIn</span><span class="sxs-lookup"><span data-stu-id="68e0a-359">localSecurityOptionsHideUsernameAtSignIn</span></span>|<span data-ttu-id="68e0a-360">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-360">Boolean</span></span>|<span data-ttu-id="68e0a-361">No mostrar el nombre de usuario de la persona que inicio de sesión para este dispositivo después de que se escriben las credenciales y antes de que se muestra el escritorio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68e0a-361">Do not display the username of the person signing in to this device after credentials are entered and before the device’s desktop is shown.</span></span>|
|<span data-ttu-id="68e0a-362">localSecurityOptionsLogOnMessageTitle</span><span class="sxs-lookup"><span data-stu-id="68e0a-362">localSecurityOptionsLogOnMessageTitle</span></span>|<span data-ttu-id="68e0a-363">Cadena</span><span class="sxs-lookup"><span data-stu-id="68e0a-363">String</span></span>|<span data-ttu-id="68e0a-364">Establecer el título del mensaje para los usuarios que intentan iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="68e0a-364">Set message title for users attempting to log in.</span></span>|
|<span data-ttu-id="68e0a-365">localSecurityOptionsLogOnMessageText</span><span class="sxs-lookup"><span data-stu-id="68e0a-365">localSecurityOptionsLogOnMessageText</span></span>|<span data-ttu-id="68e0a-366">Cadena</span><span class="sxs-lookup"><span data-stu-id="68e0a-366">String</span></span>|<span data-ttu-id="68e0a-367">Establecer el texto del mensaje para los usuarios que intentan iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="68e0a-367">Set message text for users attempting to log in.</span></span>|
|<span data-ttu-id="68e0a-368">localSecurityOptionsAllowPKU2UAuthenticationRequests</span><span class="sxs-lookup"><span data-stu-id="68e0a-368">localSecurityOptionsAllowPKU2UAuthenticationRequests</span></span>|<span data-ttu-id="68e0a-369">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-369">Boolean</span></span>|<span data-ttu-id="68e0a-370">Bloque PKU2U las solicitudes de autenticación para este dispositivo para utilizar las identidades en línea.</span><span class="sxs-lookup"><span data-stu-id="68e0a-370">Block PKU2U authentication requests to this device to use online identities.</span></span>|
|<span data-ttu-id="68e0a-371">localSecurityOptionsAllowRemoteCallsToSecurityAccountsManagerHelperBool</span><span class="sxs-lookup"><span data-stu-id="68e0a-371">localSecurityOptionsAllowRemoteCallsToSecurityAccountsManagerHelperBool</span></span>|<span data-ttu-id="68e0a-372">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-372">Boolean</span></span>|<span data-ttu-id="68e0a-373">Auxiliares de la interfaz de usuario booleano de entidad LocalSecurityOptionsAllowRemoteCallsToSecurityAccountsManager</span><span class="sxs-lookup"><span data-stu-id="68e0a-373">UI helper boolean for LocalSecurityOptionsAllowRemoteCallsToSecurityAccountsManager entity</span></span>|
|<span data-ttu-id="68e0a-374">localSecurityOptionsAllowRemoteCallsToSecurityAccountsManager</span><span class="sxs-lookup"><span data-stu-id="68e0a-374">localSecurityOptionsAllowRemoteCallsToSecurityAccountsManager</span></span>|<span data-ttu-id="68e0a-375">Cadena</span><span class="sxs-lookup"><span data-stu-id="68e0a-375">String</span></span>|<span data-ttu-id="68e0a-376">Editar la cadena de lenguaje de definición de Descriptor de seguridad predeterminado para permitir o denegar a los usuarios y grupos para que las llamadas remotas al SAM.</span><span class="sxs-lookup"><span data-stu-id="68e0a-376">Edit the default Security Descriptor Definition Language string to allow or deny users and groups to make remote calls to the SAM.</span></span>|
|<span data-ttu-id="68e0a-377">localSecurityOptionsMinimumSessionSecurityForNtlmSspBasedClients</span><span class="sxs-lookup"><span data-stu-id="68e0a-377">localSecurityOptionsMinimumSessionSecurityForNtlmSspBasedClients</span></span>|[<span data-ttu-id="68e0a-378">localSecurityOptionsMinimumSessionSecurity</span><span class="sxs-lookup"><span data-stu-id="68e0a-378">localSecurityOptionsMinimumSessionSecurity</span></span>](../resources/intune-deviceconfig-localsecurityoptionsminimumsessionsecurity.md)|<span data-ttu-id="68e0a-379">Esta configuración de seguridad permite que un cliente requerir la negociación de cifrado de 128 bits o seguridad de sesión NTLMv2.</span><span class="sxs-lookup"><span data-stu-id="68e0a-379">This security setting allows a client to require the negotiation of 128-bit encryption and/or NTLMv2 session security.</span></span> <span data-ttu-id="68e0a-380">Los valores posibles son: `none`, `requireNtmlV2SessionSecurity`, `require128BitEncryption` y `ntlmV2And128BitEncryption`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-380">Possible values are: `none`, `requireNtmlV2SessionSecurity`, `require128BitEncryption`, `ntlmV2And128BitEncryption`.</span></span>|
|<span data-ttu-id="68e0a-381">localSecurityOptionsMinimumSessionSecurityForNtlmSspBasedServers</span><span class="sxs-lookup"><span data-stu-id="68e0a-381">localSecurityOptionsMinimumSessionSecurityForNtlmSspBasedServers</span></span>|[<span data-ttu-id="68e0a-382">localSecurityOptionsMinimumSessionSecurity</span><span class="sxs-lookup"><span data-stu-id="68e0a-382">localSecurityOptionsMinimumSessionSecurity</span></span>](../resources/intune-deviceconfig-localsecurityoptionsminimumsessionsecurity.md)|<span data-ttu-id="68e0a-383">Esta configuración de seguridad permite a un servidor requerir la negociación de cifrado de 128 bits o seguridad de sesión NTLMv2.</span><span class="sxs-lookup"><span data-stu-id="68e0a-383">This security setting allows a server to require the negotiation of 128-bit encryption and/or NTLMv2 session security.</span></span> <span data-ttu-id="68e0a-384">Los valores posibles son: `none`, `requireNtmlV2SessionSecurity`, `require128BitEncryption` y `ntlmV2And128BitEncryption`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-384">Possible values are: `none`, `requireNtmlV2SessionSecurity`, `require128BitEncryption`, `ntlmV2And128BitEncryption`.</span></span>|
|<span data-ttu-id="68e0a-385">lanManagerAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="68e0a-385">lanManagerAuthenticationLevel</span></span>|[<span data-ttu-id="68e0a-386">lanManagerAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="68e0a-386">lanManagerAuthenticationLevel</span></span>](../resources/intune-deviceconfig-lanmanagerauthenticationlevel.md)|<span data-ttu-id="68e0a-387">Esta configuración de seguridad determina qué protocolo de autenticación de desafío/respuesta se usa para inicios de sesión de red.</span><span class="sxs-lookup"><span data-stu-id="68e0a-387">This security setting determines which challenge/response authentication protocol is used for network logons.</span></span> <span data-ttu-id="68e0a-388">Los valores posibles son: `lmAndNltm`, `lmNtlmAndNtlmV2`, `lmAndNtlmOnly`, `lmAndNtlmV2`, `lmNtlmV2AndNotLm`, `lmNtlmV2AndNotLmOrNtm`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-388">Possible values are: `lmAndNltm`, `lmNtlmAndNtlmV2`, `lmAndNtlmOnly`, `lmAndNtlmV2`, `lmNtlmV2AndNotLm`, `lmNtlmV2AndNotLmOrNtm`.</span></span>|
|<span data-ttu-id="68e0a-389">lanManagerWorkstationEnableInsecureGuestLogons</span><span class="sxs-lookup"><span data-stu-id="68e0a-389">lanManagerWorkstationEnableInsecureGuestLogons</span></span>|<span data-ttu-id="68e0a-390">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-390">Boolean</span></span>|<span data-ttu-id="68e0a-391">Si se habilita, el cliente SMB le permitirá los inicios de sesión de invitado no segura.</span><span class="sxs-lookup"><span data-stu-id="68e0a-391">If enabled,the SMB client will allow insecure guest logons.</span></span> <span data-ttu-id="68e0a-392">Si no está definida, el cliente SMB rechazará los inicios de sesión de invitado no segura.</span><span class="sxs-lookup"><span data-stu-id="68e0a-392">If not configured, the SMB client will reject insecure guest logons.</span></span>|
|<span data-ttu-id="68e0a-393">localSecurityOptionsClearVirtualMemoryPageFile</span><span class="sxs-lookup"><span data-stu-id="68e0a-393">localSecurityOptionsClearVirtualMemoryPageFile</span></span>|<span data-ttu-id="68e0a-394">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-394">Boolean</span></span>|<span data-ttu-id="68e0a-395">Esta configuración de seguridad determina si el archivo de paginación de memoria virtual se borra cuando se apaga el sistema.</span><span class="sxs-lookup"><span data-stu-id="68e0a-395">This security setting determines whether the virtual memory pagefile is cleared when the system is shut down.</span></span>|
|<span data-ttu-id="68e0a-396">localSecurityOptionsAllowSystemToBeShutDownWithoutHavingToLogOn</span><span class="sxs-lookup"><span data-stu-id="68e0a-396">localSecurityOptionsAllowSystemToBeShutDownWithoutHavingToLogOn</span></span>|<span data-ttu-id="68e0a-397">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-397">Boolean</span></span>|<span data-ttu-id="68e0a-398">Esta configuración de seguridad determina si un equipo se puede apagar sin tener que volver a iniciar sesión en Windows.</span><span class="sxs-lookup"><span data-stu-id="68e0a-398">This security setting determines whether a computer can be shut down without having to log on to Windows.</span></span>|
|<span data-ttu-id="68e0a-399">localSecurityOptionsAllowUIAccessApplicationElevation</span><span class="sxs-lookup"><span data-stu-id="68e0a-399">localSecurityOptionsAllowUIAccessApplicationElevation</span></span>|<span data-ttu-id="68e0a-400">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-400">Boolean</span></span>|<span data-ttu-id="68e0a-401">Permitir aplicaciones UIAccess pedir confirmación de elevación sin usar el escritorio seguro.</span><span class="sxs-lookup"><span data-stu-id="68e0a-401">Allow UIAccess apps to prompt for elevation without using the secure desktop.</span></span>|
|<span data-ttu-id="68e0a-402">localSecurityOptionsVirtualizeFileAndRegistryWriteFailuresToPerUserLocations</span><span class="sxs-lookup"><span data-stu-id="68e0a-402">localSecurityOptionsVirtualizeFileAndRegistryWriteFailuresToPerUserLocations</span></span>|<span data-ttu-id="68e0a-403">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-403">Boolean</span></span>|<span data-ttu-id="68e0a-404">Virtualizar archivo y registro de errores de escritura por ubicaciones de usuario</span><span class="sxs-lookup"><span data-stu-id="68e0a-404">Virtualize file and registry write failures to per user locations</span></span>|
|<span data-ttu-id="68e0a-405">localSecurityOptionsOnlyElevateSignedExecutables</span><span class="sxs-lookup"><span data-stu-id="68e0a-405">localSecurityOptionsOnlyElevateSignedExecutables</span></span>|<span data-ttu-id="68e0a-406">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-406">Boolean</span></span>|<span data-ttu-id="68e0a-407">Aplica la validación de ruta de acceso de certificación PKI para un determinado archivo ejecutable antes de que se le permite ejecutar.</span><span class="sxs-lookup"><span data-stu-id="68e0a-407">Enforce PKI certification path validation for a given executable file before it is permitted to run.</span></span>|
|<span data-ttu-id="68e0a-408">localSecurityOptionsAdministratorElevationPromptBehavior</span><span class="sxs-lookup"><span data-stu-id="68e0a-408">localSecurityOptionsAdministratorElevationPromptBehavior</span></span>|[<span data-ttu-id="68e0a-409">localSecurityOptionsAdministratorElevationPromptBehaviorType</span><span class="sxs-lookup"><span data-stu-id="68e0a-409">localSecurityOptionsAdministratorElevationPromptBehaviorType</span></span>](../resources/intune-deviceconfig-localsecurityoptionsadministratorelevationpromptbehaviortype.md)|<span data-ttu-id="68e0a-410">Defina el comportamiento de la petición de elevación para los administradores en modo de aprobación de administrador.</span><span class="sxs-lookup"><span data-stu-id="68e0a-410">Define the behavior of the elevation prompt for admins in Admin Approval Mode.</span></span> <span data-ttu-id="68e0a-411">Los valores posibles son: `notConfigured`, `elevateWithoutPrompting`, `promptForCredentialsOnTheSecureDesktop`, `promptForConsentOnTheSecureDesktop`, `promptForCredentials`, `promptForConsent` y `promptForConsentForNonWindowsBinaries`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-411">Possible values are: `notConfigured`, `elevateWithoutPrompting`, `promptForCredentialsOnTheSecureDesktop`, `promptForConsentOnTheSecureDesktop`, `promptForCredentials`, `promptForConsent`, `promptForConsentForNonWindowsBinaries`.</span></span>|
|<span data-ttu-id="68e0a-412">localSecurityOptionsStandardUserElevationPromptBehavior</span><span class="sxs-lookup"><span data-stu-id="68e0a-412">localSecurityOptionsStandardUserElevationPromptBehavior</span></span>|[<span data-ttu-id="68e0a-413">localSecurityOptionsStandardUserElevationPromptBehaviorType</span><span class="sxs-lookup"><span data-stu-id="68e0a-413">localSecurityOptionsStandardUserElevationPromptBehaviorType</span></span>](../resources/intune-deviceconfig-localsecurityoptionsstandarduserelevationpromptbehaviortype.md)|<span data-ttu-id="68e0a-414">Defina el comportamiento de la petición de elevación para los usuarios estándar.</span><span class="sxs-lookup"><span data-stu-id="68e0a-414">Define the behavior of the elevation prompt for standard users.</span></span> <span data-ttu-id="68e0a-415">Los valores posibles son: `notConfigured`, `automaticallyDenyElevationRequests`, `promptForCredentialsOnTheSecureDesktop` y `promptForCredentials`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-415">Possible values are: `notConfigured`, `automaticallyDenyElevationRequests`, `promptForCredentialsOnTheSecureDesktop`, `promptForCredentials`.</span></span>|
|<span data-ttu-id="68e0a-416">localSecurityOptionsSwitchToSecureDesktopWhenPromptingForElevation</span><span class="sxs-lookup"><span data-stu-id="68e0a-416">localSecurityOptionsSwitchToSecureDesktopWhenPromptingForElevation</span></span>|<span data-ttu-id="68e0a-417">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-417">Boolean</span></span>|<span data-ttu-id="68e0a-418">Habilitar todas las solicitudes de elevación ir al escritorio del usuario interactivo en lugar del escritorio seguro.</span><span class="sxs-lookup"><span data-stu-id="68e0a-418">Enable all elevation requests to go to the interactive user's desktop rather than the secure desktop.</span></span> <span data-ttu-id="68e0a-419">Se usa la configuración de la directiva de comportamiento de solicitud para los administradores y usuarios estándar.</span><span class="sxs-lookup"><span data-stu-id="68e0a-419">Prompt behavior policy settings for admins and standard users are used.</span></span>|
|<span data-ttu-id="68e0a-420">localSecurityOptionsDetectApplicationInstallationsAndPromptForElevation</span><span class="sxs-lookup"><span data-stu-id="68e0a-420">localSecurityOptionsDetectApplicationInstallationsAndPromptForElevation</span></span>|<span data-ttu-id="68e0a-421">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-421">Boolean</span></span>|<span data-ttu-id="68e0a-422">Las instalaciones de aplicaciones que requieren privilegios elevados solicitará las credenciales de administrador. Es el comportamiento predeterminado</span><span class="sxs-lookup"><span data-stu-id="68e0a-422">App installations requiring elevated privileges will prompt for admin credentials.Default is enabled</span></span>|
|<span data-ttu-id="68e0a-423">localSecurityOptionsAllowUIAccessApplicationsForSecureLocations</span><span class="sxs-lookup"><span data-stu-id="68e0a-423">localSecurityOptionsAllowUIAccessApplicationsForSecureLocations</span></span>|<span data-ttu-id="68e0a-424">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-424">Boolean</span></span>|<span data-ttu-id="68e0a-425">Permitir aplicaciones UIAccess pedir confirmación de elevación sin usar el escritorio seguro. Es el comportamiento predeterminado</span><span class="sxs-lookup"><span data-stu-id="68e0a-425">Allow UIAccess apps to prompt for elevation without using the secure desktop.Default is enabled</span></span>|
|<span data-ttu-id="68e0a-426">localSecurityOptionsUseAdminApprovalMode</span><span class="sxs-lookup"><span data-stu-id="68e0a-426">localSecurityOptionsUseAdminApprovalMode</span></span>|<span data-ttu-id="68e0a-427">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-427">Boolean</span></span>|<span data-ttu-id="68e0a-428">Define si la cuenta de administrador integrada usa el modo de aprobación de administrador o ejecuta todas las aplicaciones con privilegios completos de administrador. Es el comportamiento predeterminado</span><span class="sxs-lookup"><span data-stu-id="68e0a-428">Defines whether the built-in admin account uses Admin Approval Mode or runs all apps with full admin privileges.Default is enabled</span></span>|
|<span data-ttu-id="68e0a-429">localSecurityOptionsUseAdminApprovalModeForAdministrators</span><span class="sxs-lookup"><span data-stu-id="68e0a-429">localSecurityOptionsUseAdminApprovalModeForAdministrators</span></span>|<span data-ttu-id="68e0a-430">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-430">Boolean</span></span>|<span data-ttu-id="68e0a-431">Definir si están habilitadas el modo de aprobación de administrador y todas las configuraciones de directiva UAC, es el comportamiento predeterminado</span><span class="sxs-lookup"><span data-stu-id="68e0a-431">Define whether Admin Approval Mode and all UAC policy settings are enabled, default is enabled</span></span>|
|<span data-ttu-id="68e0a-432">localSecurityOptionsInformationShownOnLockScreen</span><span class="sxs-lookup"><span data-stu-id="68e0a-432">localSecurityOptionsInformationShownOnLockScreen</span></span>|[<span data-ttu-id="68e0a-433">localSecurityOptionsInformationShownOnLockScreenType</span><span class="sxs-lookup"><span data-stu-id="68e0a-433">localSecurityOptionsInformationShownOnLockScreenType</span></span>](../resources/intune-deviceconfig-localsecurityoptionsinformationshownonlockscreentype.md)|<span data-ttu-id="68e0a-434">Configurar la información de usuario que se muestra cuando la sesión está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="68e0a-434">Configure the user information that is displayed when the session is locked.</span></span> <span data-ttu-id="68e0a-435">Si no está definida, se muestran el nombre de usuario, dominio y nombre de usuario para mostrar.</span><span class="sxs-lookup"><span data-stu-id="68e0a-435">If not configured, user display name, domain and username are shown.</span></span> <span data-ttu-id="68e0a-436">Los valores posibles son: `notConfigured`, `userDisplayNameDomainUser`, `userDisplayNameOnly` y `doNotDisplayUser`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-436">Possible values are: `notConfigured`, `userDisplayNameDomainUser`, `userDisplayNameOnly`, `doNotDisplayUser`.</span></span>|
|<span data-ttu-id="68e0a-437">localSecurityOptionsInformationDisplayedOnLockScreen</span><span class="sxs-lookup"><span data-stu-id="68e0a-437">localSecurityOptionsInformationDisplayedOnLockScreen</span></span>|[<span data-ttu-id="68e0a-438">localSecurityOptionsInformationDisplayedOnLockScreenType</span><span class="sxs-lookup"><span data-stu-id="68e0a-438">localSecurityOptionsInformationDisplayedOnLockScreenType</span></span>](../resources/intune-deviceconfig-localsecurityoptionsinformationdisplayedonlockscreentype.md)|<span data-ttu-id="68e0a-439">Configurar la información de usuario que se muestra cuando la sesión está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="68e0a-439">Configure the user information that is displayed when the session is locked.</span></span> <span data-ttu-id="68e0a-440">Si no está definida, se muestran el nombre de usuario, dominio y nombre de usuario para mostrar.</span><span class="sxs-lookup"><span data-stu-id="68e0a-440">If not configured, user display name, domain and username are shown.</span></span> <span data-ttu-id="68e0a-441">Los valores posibles son: `notConfigured`, `administrators`, `administratorsAndPowerUsers` y `administratorsAndInteractiveUsers`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-441">Possible values are: `notConfigured`, `administrators`, `administratorsAndPowerUsers`, `administratorsAndInteractiveUsers`.</span></span>|
|<span data-ttu-id="68e0a-442">localSecurityOptionsDisableClientDigitallySignCommunicationsIfServerAgrees</span><span class="sxs-lookup"><span data-stu-id="68e0a-442">localSecurityOptionsDisableClientDigitallySignCommunicationsIfServerAgrees</span></span>|<span data-ttu-id="68e0a-443">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-443">Boolean</span></span>|<span data-ttu-id="68e0a-444">Esta configuración de seguridad determina si el cliente SMB intenta negociar la firma de paquetes SMB.</span><span class="sxs-lookup"><span data-stu-id="68e0a-444">This security setting determines whether the SMB client attempts to negotiate SMB packet signing.</span></span>|
|<span data-ttu-id="68e0a-445">localSecurityOptionsClientDigitallySignCommunicationsAlways</span><span class="sxs-lookup"><span data-stu-id="68e0a-445">localSecurityOptionsClientDigitallySignCommunicationsAlways</span></span>|<span data-ttu-id="68e0a-446">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-446">Boolean</span></span>|<span data-ttu-id="68e0a-447">Esta configuración de seguridad determina si el componente de cliente SMB requiere la firma de paquetes.</span><span class="sxs-lookup"><span data-stu-id="68e0a-447">This security setting determines whether packet signing is required by the SMB client component.</span></span>|
|<span data-ttu-id="68e0a-448">localSecurityOptionsClientSendUnencryptedPasswordToThirdPartySMBServers</span><span class="sxs-lookup"><span data-stu-id="68e0a-448">localSecurityOptionsClientSendUnencryptedPasswordToThirdPartySMBServers</span></span>|<span data-ttu-id="68e0a-449">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-449">Boolean</span></span>|<span data-ttu-id="68e0a-450">Si se habilita esta configuración de seguridad, se permite el redirector de bloque de mensajes del servidor (SMB) para enviar contraseñas de texto simple a servidores SMB que no son Microsoft que no admiten el cifrado de contraseña durante la autenticación.</span><span class="sxs-lookup"><span data-stu-id="68e0a-450">If this security setting is enabled, the Server Message Block (SMB) redirector is allowed to send plaintext passwords to non-Microsoft SMB servers that do not support password encryption during authentication.</span></span>|
|<span data-ttu-id="68e0a-451">localSecurityOptionsDisableServerDigitallySignCommunicationsAlways</span><span class="sxs-lookup"><span data-stu-id="68e0a-451">localSecurityOptionsDisableServerDigitallySignCommunicationsAlways</span></span>|<span data-ttu-id="68e0a-452">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-452">Boolean</span></span>|<span data-ttu-id="68e0a-453">Esta configuración de seguridad determina si el componente de servidor SMB requiere la firma de paquetes.</span><span class="sxs-lookup"><span data-stu-id="68e0a-453">This security setting determines whether packet signing is required by the SMB server component.</span></span>|
|<span data-ttu-id="68e0a-454">localSecurityOptionsDisableServerDigitallySignCommunicationsIfClientAgrees</span><span class="sxs-lookup"><span data-stu-id="68e0a-454">localSecurityOptionsDisableServerDigitallySignCommunicationsIfClientAgrees</span></span>|<span data-ttu-id="68e0a-455">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-455">Boolean</span></span>|<span data-ttu-id="68e0a-456">Esta configuración de seguridad determina si el servidor SMB negociará la firma con clientes que lo soliciten de paquetes SMB.</span><span class="sxs-lookup"><span data-stu-id="68e0a-456">This security setting determines whether the SMB server will negotiate SMB packet signing with clients that request it.</span></span>|
|<span data-ttu-id="68e0a-457">localSecurityOptionsRestrictAnonymousAccessToNamedPipesAndShares</span><span class="sxs-lookup"><span data-stu-id="68e0a-457">localSecurityOptionsRestrictAnonymousAccessToNamedPipesAndShares</span></span>|<span data-ttu-id="68e0a-458">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-458">Boolean</span></span>|<span data-ttu-id="68e0a-459">De forma predeterminada, esta configuración de seguridad restringe el acceso anónimo a recursos compartidos y canalizaciones a la configuración de canalizaciones con nombre que se pueden tener acceso de forma anónima y los recursos compartidos que se pueden tener acceso de forma anónima</span><span class="sxs-lookup"><span data-stu-id="68e0a-459">By default, this security setting restricts anonymous access to shares and pipes to the settings for named pipes that can be accessed anonymously and Shares that can be accessed anonymously</span></span>|
|<span data-ttu-id="68e0a-460">localSecurityOptionsDoNotAllowAnonymousEnumerationOfSAMAccounts</span><span class="sxs-lookup"><span data-stu-id="68e0a-460">localSecurityOptionsDoNotAllowAnonymousEnumerationOfSAMAccounts</span></span>|<span data-ttu-id="68e0a-461">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-461">Boolean</span></span>|<span data-ttu-id="68e0a-462">Esta configuración de seguridad determina qué permisos adicionales se concederán para las conexiones anónimas al equipo.</span><span class="sxs-lookup"><span data-stu-id="68e0a-462">This security setting determines what additional permissions will be granted for anonymous connections to the computer.</span></span>|
|<span data-ttu-id="68e0a-463">localSecurityOptionsAllowAnonymousEnumerationOfSAMAccountsAndShares</span><span class="sxs-lookup"><span data-stu-id="68e0a-463">localSecurityOptionsAllowAnonymousEnumerationOfSAMAccountsAndShares</span></span>|<span data-ttu-id="68e0a-464">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-464">Boolean</span></span>|<span data-ttu-id="68e0a-465">Esta configuración de seguridad determina si se permite a los usuarios anónimos realizar determinadas actividades, como enumerar los nombres de las cuentas de dominio y recursos compartidos de red.</span><span class="sxs-lookup"><span data-stu-id="68e0a-465">This security setting determines whether to allows anonymous users to perform certain activities, such as enumerating the names of domain accounts and network shares.</span></span>|
|<span data-ttu-id="68e0a-466">localSecurityOptionsDoNotStoreLANManagerHashValueOnNextPasswordChange</span><span class="sxs-lookup"><span data-stu-id="68e0a-466">localSecurityOptionsDoNotStoreLANManagerHashValueOnNextPasswordChange</span></span>|<span data-ttu-id="68e0a-467">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-467">Boolean</span></span>|<span data-ttu-id="68e0a-468">Esta configuración de seguridad determina si, en el próximo cambio de contraseña, se almacena el valor de hash de LAN Manager (LM) para la nueva contraseña.</span><span class="sxs-lookup"><span data-stu-id="68e0a-468">This security setting determines if, at the next password change, the LAN Manager (LM) hash value for the new password is stored.</span></span> <span data-ttu-id="68e0a-469">No se almacena de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="68e0a-469">It’s not stored by default.</span></span>|
|<span data-ttu-id="68e0a-470">localSecurityOptionsSmartCardRemovalBehavior</span><span class="sxs-lookup"><span data-stu-id="68e0a-470">localSecurityOptionsSmartCardRemovalBehavior</span></span>|[<span data-ttu-id="68e0a-471">localSecurityOptionsSmartCardRemovalBehaviorType</span><span class="sxs-lookup"><span data-stu-id="68e0a-471">localSecurityOptionsSmartCardRemovalBehaviorType</span></span>](../resources/intune-deviceconfig-localsecurityoptionssmartcardremovalbehaviortype.md)|<span data-ttu-id="68e0a-472">Esta configuración de seguridad determina qué ocurre cuando se ha quitado la tarjeta inteligente de un usuario ha iniciado sesión desde el lector de tarjetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="68e0a-472">This security setting determines what happens when the smart card for a logged-on user is removed from the smart card reader.</span></span> <span data-ttu-id="68e0a-473">Los valores posibles son: `lockWorkstation`, `noAction`, `forceLogoff` y `disconnectRemoteDesktopSession`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-473">Possible values are: `lockWorkstation`, `noAction`, `forceLogoff`, `disconnectRemoteDesktopSession`.</span></span>|
|<span data-ttu-id="68e0a-474">defenderSecurityCenterDisableAppBrowserUI</span><span class="sxs-lookup"><span data-stu-id="68e0a-474">defenderSecurityCenterDisableAppBrowserUI</span></span>|<span data-ttu-id="68e0a-475">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-475">Boolean</span></span>|<span data-ttu-id="68e0a-476">Se usa para deshabilitar la presentación de la zona de protección de aplicación y el explorador.</span><span class="sxs-lookup"><span data-stu-id="68e0a-476">Used to disable the display of the app and browser protection area.</span></span>|
|<span data-ttu-id="68e0a-477">defenderSecurityCenterDisableFamilyUI</span><span class="sxs-lookup"><span data-stu-id="68e0a-477">defenderSecurityCenterDisableFamilyUI</span></span>|<span data-ttu-id="68e0a-478">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-478">Boolean</span></span>|<span data-ttu-id="68e0a-479">Se usa para deshabilitar la presentación del área de opciones de la familia.</span><span class="sxs-lookup"><span data-stu-id="68e0a-479">Used to disable the display of the family options area.</span></span>|
|<span data-ttu-id="68e0a-480">defenderSecurityCenterDisableHealthUI</span><span class="sxs-lookup"><span data-stu-id="68e0a-480">defenderSecurityCenterDisableHealthUI</span></span>|<span data-ttu-id="68e0a-481">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-481">Boolean</span></span>|<span data-ttu-id="68e0a-482">Se usa para deshabilitar la presentación del área de mantenimiento y rendimiento de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68e0a-482">Used to disable the display of the device performance and health area.</span></span>|
|<span data-ttu-id="68e0a-483">defenderSecurityCenterDisableNetworkUI</span><span class="sxs-lookup"><span data-stu-id="68e0a-483">defenderSecurityCenterDisableNetworkUI</span></span>|<span data-ttu-id="68e0a-484">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-484">Boolean</span></span>|<span data-ttu-id="68e0a-485">Se usa para deshabilitar la presentación de la zona de protección de firewall y de red.</span><span class="sxs-lookup"><span data-stu-id="68e0a-485">Used to disable the display of the firewall and network protection area.</span></span>|
|<span data-ttu-id="68e0a-486">defenderSecurityCenterDisableVirusUI</span><span class="sxs-lookup"><span data-stu-id="68e0a-486">defenderSecurityCenterDisableVirusUI</span></span>|<span data-ttu-id="68e0a-487">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-487">Boolean</span></span>|<span data-ttu-id="68e0a-488">Se usa para deshabilitar la presentación de la zona de protección contra virus y amenazas.</span><span class="sxs-lookup"><span data-stu-id="68e0a-488">Used to disable the display of the virus and threat protection area.</span></span>|
|<span data-ttu-id="68e0a-489">defenderSecurityCenterDisableAccountUI</span><span class="sxs-lookup"><span data-stu-id="68e0a-489">defenderSecurityCenterDisableAccountUI</span></span>|<span data-ttu-id="68e0a-490">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-490">Boolean</span></span>|<span data-ttu-id="68e0a-491">Se usa para deshabilitar la presentación de la zona de protección de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="68e0a-491">Used to disable the display of the account protection area.</span></span>|
|<span data-ttu-id="68e0a-492">defenderSecurityCenterDisableHardwareUI</span><span class="sxs-lookup"><span data-stu-id="68e0a-492">defenderSecurityCenterDisableHardwareUI</span></span>|<span data-ttu-id="68e0a-493">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-493">Boolean</span></span>|<span data-ttu-id="68e0a-494">Se usa para deshabilitar la presentación de la zona de protección de hardware.</span><span class="sxs-lookup"><span data-stu-id="68e0a-494">Used to disable the display of the hardware protection area.</span></span>|
|<span data-ttu-id="68e0a-495">defenderSecurityCenterDisableRansomwareUI</span><span class="sxs-lookup"><span data-stu-id="68e0a-495">defenderSecurityCenterDisableRansomwareUI</span></span>|<span data-ttu-id="68e0a-496">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-496">Boolean</span></span>|<span data-ttu-id="68e0a-497">Se usa para deshabilitar la presentación de la zona de protección ransomware.</span><span class="sxs-lookup"><span data-stu-id="68e0a-497">Used to disable the display of the ransomware protection area.</span></span> |
|<span data-ttu-id="68e0a-498">defenderSecurityCenterDisableSecureBootUI</span><span class="sxs-lookup"><span data-stu-id="68e0a-498">defenderSecurityCenterDisableSecureBootUI</span></span>|<span data-ttu-id="68e0a-499">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-499">Boolean</span></span>|<span data-ttu-id="68e0a-500">Se usa para deshabilitar la presentación del área de inicialización segura en seguridad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68e0a-500">Used to disable the display of the secure boot area under Device security.</span></span>|
|<span data-ttu-id="68e0a-501">defenderSecurityCenterDisableTroubleshootingUI</span><span class="sxs-lookup"><span data-stu-id="68e0a-501">defenderSecurityCenterDisableTroubleshootingUI</span></span>|<span data-ttu-id="68e0a-502">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-502">Boolean</span></span>|<span data-ttu-id="68e0a-503">Se usa para deshabilitar la visualización del proceso de seguridad de solución de problemas en la seguridad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68e0a-503">Used to disable the display of the security process troubleshooting under Device security.</span></span>|
|<span data-ttu-id="68e0a-504">defenderSecurityCenterOrganizationDisplayName</span><span class="sxs-lookup"><span data-stu-id="68e0a-504">defenderSecurityCenterOrganizationDisplayName</span></span>|<span data-ttu-id="68e0a-505">Cadena</span><span class="sxs-lookup"><span data-stu-id="68e0a-505">String</span></span>|<span data-ttu-id="68e0a-506">El nombre de la compañía que se muestra a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="68e0a-506">The company name that is displayed to the users.</span></span>|
|<span data-ttu-id="68e0a-507">defenderSecurityCenterHelpEmail</span><span class="sxs-lookup"><span data-stu-id="68e0a-507">defenderSecurityCenterHelpEmail</span></span>|<span data-ttu-id="68e0a-508">Cadena</span><span class="sxs-lookup"><span data-stu-id="68e0a-508">String</span></span>|<span data-ttu-id="68e0a-509">La dirección de correo electrónico que se mostrará a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="68e0a-509">The email address that is displayed to users.</span></span>|
|<span data-ttu-id="68e0a-510">defenderSecurityCenterHelpPhone</span><span class="sxs-lookup"><span data-stu-id="68e0a-510">defenderSecurityCenterHelpPhone</span></span>|<span data-ttu-id="68e0a-511">Cadena</span><span class="sxs-lookup"><span data-stu-id="68e0a-511">String</span></span>|<span data-ttu-id="68e0a-512">El número de teléfono o el identificador de Skype que se muestra a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="68e0a-512">The phone number or Skype ID that is displayed to users.</span></span>|
|<span data-ttu-id="68e0a-513">defenderSecurityCenterHelpURL</span><span class="sxs-lookup"><span data-stu-id="68e0a-513">defenderSecurityCenterHelpURL</span></span>|<span data-ttu-id="68e0a-514">Cadena</span><span class="sxs-lookup"><span data-stu-id="68e0a-514">String</span></span>|<span data-ttu-id="68e0a-515">El portal de Ayuda de dirección URL que se mostrará a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="68e0a-515">The help portal URL this is displayed to users.</span></span>|
|<span data-ttu-id="68e0a-516">defenderSecurityCenterNotificationsFromApp</span><span class="sxs-lookup"><span data-stu-id="68e0a-516">defenderSecurityCenterNotificationsFromApp</span></span>|[<span data-ttu-id="68e0a-517">defenderSecurityCenterNotificationsFromAppType</span><span class="sxs-lookup"><span data-stu-id="68e0a-517">defenderSecurityCenterNotificationsFromAppType</span></span>](../resources/intune-deviceconfig-defendersecuritycenternotificationsfromapptype.md)|<span data-ttu-id="68e0a-518">Notificaciones para mostrar de las áreas de aplicación que se muestra.</span><span class="sxs-lookup"><span data-stu-id="68e0a-518">Notifications to show from the displayed areas of app.</span></span> <span data-ttu-id="68e0a-519">Los valores posibles son: `notConfigured`, `blockNoncriticalNotifications` y `blockAllNotifications`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-519">Possible values are: `notConfigured`, `blockNoncriticalNotifications`, `blockAllNotifications`.</span></span>|
|<span data-ttu-id="68e0a-520">defenderSecurityCenterITContactDisplay</span><span class="sxs-lookup"><span data-stu-id="68e0a-520">defenderSecurityCenterITContactDisplay</span></span>|[<span data-ttu-id="68e0a-521">defenderSecurityCenterITContactDisplayType</span><span class="sxs-lookup"><span data-stu-id="68e0a-521">defenderSecurityCenterITContactDisplayType</span></span>](../resources/intune-deviceconfig-defendersecuritycenteritcontactdisplaytype.md)|<span data-ttu-id="68e0a-522">Configurar dónde mostrar el contacto de TI información a los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="68e0a-522">Configure where to display IT contact information to end users.</span></span> <span data-ttu-id="68e0a-523">Los valores posibles son: `notConfigured`, `displayInAppAndInNotifications`, `displayOnlyInApp` y `displayOnlyInNotifications`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-523">Possible values are: `notConfigured`, `displayInAppAndInNotifications`, `displayOnlyInApp`, `displayOnlyInNotifications`.</span></span>|
|<span data-ttu-id="68e0a-524">firewallBlockStatefulFTP</span><span class="sxs-lookup"><span data-stu-id="68e0a-524">firewallBlockStatefulFTP</span></span>|<span data-ttu-id="68e0a-525">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-525">Boolean</span></span>|<span data-ttu-id="68e0a-526">Bloquea las conexiones FTP con estado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68e0a-526">Blocks stateful FTP connections to the device</span></span>|
|<span data-ttu-id="68e0a-527">firewallIdleTimeoutForSecurityAssociationInSeconds</span><span class="sxs-lookup"><span data-stu-id="68e0a-527">firewallIdleTimeoutForSecurityAssociationInSeconds</span></span>|<span data-ttu-id="68e0a-528">Int32</span><span class="sxs-lookup"><span data-stu-id="68e0a-528">Int32</span></span>|<span data-ttu-id="68e0a-529">Configura el tiempo de espera inactivo para asociaciones de seguridad, en segundos, de 300 a 3600 inclusive.</span><span class="sxs-lookup"><span data-stu-id="68e0a-529">Configures the idle timeout for security associations, in seconds, from 300 to 3600 inclusive.</span></span> <span data-ttu-id="68e0a-530">Se trata del período tras el cual expiran y se eliminan las asociaciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="68e0a-530">This is the period after which security associations will expire and be deleted.</span></span> <span data-ttu-id="68e0a-531">Valores válidos de 300 a 3600.</span><span class="sxs-lookup"><span data-stu-id="68e0a-531">Valid values 300 to 3600</span></span>|
|<span data-ttu-id="68e0a-532">firewallPreSharedKeyEncodingMethod</span><span class="sxs-lookup"><span data-stu-id="68e0a-532">firewallPreSharedKeyEncodingMethod</span></span>|[<span data-ttu-id="68e0a-533">firewallPreSharedKeyEncodingMethodType</span><span class="sxs-lookup"><span data-stu-id="68e0a-533">firewallPreSharedKeyEncodingMethodType</span></span>](../resources/intune-deviceconfig-firewallpresharedkeyencodingmethodtype.md)|<span data-ttu-id="68e0a-534">Seleccione la clave previamente compartida de codificación que se utilizará.</span><span class="sxs-lookup"><span data-stu-id="68e0a-534">Select the preshared key encoding to be used.</span></span> <span data-ttu-id="68e0a-535">Los valores posibles son: `deviceDefault`, `none` y `utF8`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-535">Possible values are: `deviceDefault`, `none`, `utF8`.</span></span>|
|<span data-ttu-id="68e0a-536">firewallIPSecExemptionsAllowNeighborDiscovery</span><span class="sxs-lookup"><span data-stu-id="68e0a-536">firewallIPSecExemptionsAllowNeighborDiscovery</span></span>|<span data-ttu-id="68e0a-537">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-537">Boolean</span></span>|<span data-ttu-id="68e0a-538">Configura las exenciones IPSec para permitir los códigos de tipo ICMP de IPv6 de detección de vecinos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-538">Configures IPSec exemptions to allow neighbor discovery IPv6 ICMP type-codes</span></span>|
|<span data-ttu-id="68e0a-539">firewallIPSecExemptionsAllowICMP</span><span class="sxs-lookup"><span data-stu-id="68e0a-539">firewallIPSecExemptionsAllowICMP</span></span>|<span data-ttu-id="68e0a-540">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-540">Boolean</span></span>|<span data-ttu-id="68e0a-541">Configura las exenciones IPSec para permitir ICMP.</span><span class="sxs-lookup"><span data-stu-id="68e0a-541">Configures IPSec exemptions to allow ICMP</span></span>|
|<span data-ttu-id="68e0a-542">firewallIPSecExemptionsAllowRouterDiscovery</span><span class="sxs-lookup"><span data-stu-id="68e0a-542">firewallIPSecExemptionsAllowRouterDiscovery</span></span>|<span data-ttu-id="68e0a-543">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-543">Boolean</span></span>|<span data-ttu-id="68e0a-544">Configura las exenciones IPSec para permitir los códigos de tipo ICMP de IPv6 de detección de enrutadores.</span><span class="sxs-lookup"><span data-stu-id="68e0a-544">Configures IPSec exemptions to allow router discovery IPv6 ICMP type-codes</span></span>|
|<span data-ttu-id="68e0a-545">firewallIPSecExemptionsAllowDHCP</span><span class="sxs-lookup"><span data-stu-id="68e0a-545">firewallIPSecExemptionsAllowDHCP</span></span>|<span data-ttu-id="68e0a-546">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-546">Boolean</span></span>|<span data-ttu-id="68e0a-547">Configura las exenciones IPSec para permitir el tráfico DHCP de IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="68e0a-547">Configures IPSec exemptions to allow both IPv4 and IPv6 DHCP traffic</span></span>|
|<span data-ttu-id="68e0a-548">firewallCertificateRevocationListCheckMethod</span><span class="sxs-lookup"><span data-stu-id="68e0a-548">firewallCertificateRevocationListCheckMethod</span></span>|[<span data-ttu-id="68e0a-549">firewallCertificateRevocationListCheckMethodType</span><span class="sxs-lookup"><span data-stu-id="68e0a-549">firewallCertificateRevocationListCheckMethodType</span></span>](../resources/intune-deviceconfig-firewallcertificaterevocationlistcheckmethodtype.md)|<span data-ttu-id="68e0a-550">Especificar cómo se aplica la lista de revocación de certificados.</span><span class="sxs-lookup"><span data-stu-id="68e0a-550">Specify how the certificate revocation list is to be enforced.</span></span> <span data-ttu-id="68e0a-551">Los valores posibles son: `deviceDefault`, `none`, `attempt` y `require`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-551">Possible values are: `deviceDefault`, `none`, `attempt`, `require`.</span></span>|
|<span data-ttu-id="68e0a-552">firewallMergeKeyingModuleSettings</span><span class="sxs-lookup"><span data-stu-id="68e0a-552">firewallMergeKeyingModuleSettings</span></span>|<span data-ttu-id="68e0a-553">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-553">Boolean</span></span>|<span data-ttu-id="68e0a-554">Si un conjunto de autenticación no es totalmente compatible con un módulo de generación de claves, dirija el módulo para que solo ignore los conjuntos de autenticación no admitidos, en lugar de todo el conjunto.</span><span class="sxs-lookup"><span data-stu-id="68e0a-554">If an authentication set is not fully supported by a keying module, direct the module to ignore only unsupported authentication suites rather than the entire set</span></span>|
|<span data-ttu-id="68e0a-555">firewallPacketQueueingMethod</span><span class="sxs-lookup"><span data-stu-id="68e0a-555">firewallPacketQueueingMethod</span></span>|[<span data-ttu-id="68e0a-556">firewallPacketQueueingMethodType</span><span class="sxs-lookup"><span data-stu-id="68e0a-556">firewallPacketQueueingMethodType</span></span>](../resources/intune-deviceconfig-firewallpacketqueueingmethodtype.md)|<span data-ttu-id="68e0a-557">Configura cómo debe aplicarse queueing de paquetes en el escenario de puerta de enlace de túnel.</span><span class="sxs-lookup"><span data-stu-id="68e0a-557">Configures how packet queueing should be applied in the tunnel gateway scenario.</span></span> <span data-ttu-id="68e0a-558">Los valores posibles son: `deviceDefault`, `disabled`, `queueInbound`, `queueOutbound` y `queueBoth`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-558">Possible values are: `deviceDefault`, `disabled`, `queueInbound`, `queueOutbound`, `queueBoth`.</span></span>|
|<span data-ttu-id="68e0a-559">firewallProfileDomain</span><span class="sxs-lookup"><span data-stu-id="68e0a-559">firewallProfileDomain</span></span>|[<span data-ttu-id="68e0a-560">windowsFirewallNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="68e0a-560">windowsFirewallNetworkProfile</span></span>](../resources/intune-deviceconfig-windowsfirewallnetworkprofile.md)|<span data-ttu-id="68e0a-561">Configura las opciones del perfil de firewall para redes de dominio.</span><span class="sxs-lookup"><span data-stu-id="68e0a-561">Configures the firewall profile settings for domain networks</span></span>|
|<span data-ttu-id="68e0a-562">firewallProfilePublic</span><span class="sxs-lookup"><span data-stu-id="68e0a-562">firewallProfilePublic</span></span>|[<span data-ttu-id="68e0a-563">windowsFirewallNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="68e0a-563">windowsFirewallNetworkProfile</span></span>](../resources/intune-deviceconfig-windowsfirewallnetworkprofile.md)|<span data-ttu-id="68e0a-564">Configura las opciones del perfil de firewall para redes públicas.</span><span class="sxs-lookup"><span data-stu-id="68e0a-564">Configures the firewall profile settings for public networks</span></span>|
|<span data-ttu-id="68e0a-565">firewallProfilePrivate</span><span class="sxs-lookup"><span data-stu-id="68e0a-565">firewallProfilePrivate</span></span>|[<span data-ttu-id="68e0a-566">windowsFirewallNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="68e0a-566">windowsFirewallNetworkProfile</span></span>](../resources/intune-deviceconfig-windowsfirewallnetworkprofile.md)|<span data-ttu-id="68e0a-567">Configura las opciones del perfil de firewall para redes privadas.</span><span class="sxs-lookup"><span data-stu-id="68e0a-567">Configures the firewall profile settings for private networks</span></span>|
|<span data-ttu-id="68e0a-568">defenderAttackSurfaceReductionExcludedPaths</span><span class="sxs-lookup"><span data-stu-id="68e0a-568">defenderAttackSurfaceReductionExcludedPaths</span></span>|<span data-ttu-id="68e0a-569">Colección String</span><span class="sxs-lookup"><span data-stu-id="68e0a-569">String collection</span></span>|<span data-ttu-id="68e0a-570">Lista de archivos exe y carpetas que se deben excluir de las reglas de reducción de la superficie expuesta a ataques.</span><span class="sxs-lookup"><span data-stu-id="68e0a-570">List of exe files and folders to be excluded from attack surface reduction rules</span></span>|
|<span data-ttu-id="68e0a-571">defenderOfficeAppsOtherProcessInjectionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-571">defenderOfficeAppsOtherProcessInjectionType</span></span>|[<span data-ttu-id="68e0a-572">defenderAttackSurfaceType</span><span class="sxs-lookup"><span data-stu-id="68e0a-572">defenderAttackSurfaceType</span></span>](../resources/intune-deviceconfig-defenderattacksurfacetype.md)|<span data-ttu-id="68e0a-573">Valor que indica el comportamiento de las aplicaciones de Office que está insertando en otros procesos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-573">Value indicating the behavior of Office applications injecting into other processes.</span></span> <span data-ttu-id="68e0a-574">Los valores posibles son: `userDefined`, `block` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-574">Possible values are: `userDefined`, `block`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-575">defenderOfficeAppsOtherProcessInjection</span><span class="sxs-lookup"><span data-stu-id="68e0a-575">defenderOfficeAppsOtherProcessInjection</span></span>|[<span data-ttu-id="68e0a-576">defenderProtectionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-576">defenderProtectionType</span></span>](../resources/intune-deviceconfig-defenderprotectiontype.md)|<span data-ttu-id="68e0a-577">Valor que indica el comportamiento de las aplicaciones de Office que está insertando en otros procesos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-577">Value indicating the behavior of  Office applications injecting into other processes.</span></span> <span data-ttu-id="68e0a-578">Los valores posibles son: `userDefined`, `enable` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-578">Possible values are: `userDefined`, `enable`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-579">defenderOfficeAppsExecutableContentCreationOrLaunchType</span><span class="sxs-lookup"><span data-stu-id="68e0a-579">defenderOfficeAppsExecutableContentCreationOrLaunchType</span></span>|[<span data-ttu-id="68e0a-580">defenderAttackSurfaceType</span><span class="sxs-lookup"><span data-stu-id="68e0a-580">defenderAttackSurfaceType</span></span>](../resources/intune-deviceconfig-defenderattacksurfacetype.md)|<span data-ttu-id="68e0a-581">Valor que indica el comportamiento de las aplicaciones y las macros de Office crear o iniciar contenido ejecutable.</span><span class="sxs-lookup"><span data-stu-id="68e0a-581">Value indicating the behavior of Office applications/macros creating or launching executable content.</span></span> <span data-ttu-id="68e0a-582">Los valores posibles son: `userDefined`, `block` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-582">Possible values are: `userDefined`, `block`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-583">defenderOfficeAppsExecutableContentCreationOrLaunch</span><span class="sxs-lookup"><span data-stu-id="68e0a-583">defenderOfficeAppsExecutableContentCreationOrLaunch</span></span>|[<span data-ttu-id="68e0a-584">defenderProtectionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-584">defenderProtectionType</span></span>](../resources/intune-deviceconfig-defenderprotectiontype.md)|<span data-ttu-id="68e0a-585">Valor que indica el comportamiento de las aplicaciones y las macros de Office crear o iniciar contenido ejecutable.</span><span class="sxs-lookup"><span data-stu-id="68e0a-585">Value indicating the behavior of Office applications/macros creating or launching executable content.</span></span> <span data-ttu-id="68e0a-586">Los valores posibles son: `userDefined`, `enable` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-586">Possible values are: `userDefined`, `enable`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-587">defenderOfficeAppsLaunchChildProcessType</span><span class="sxs-lookup"><span data-stu-id="68e0a-587">defenderOfficeAppsLaunchChildProcessType</span></span>|[<span data-ttu-id="68e0a-588">defenderAttackSurfaceType</span><span class="sxs-lookup"><span data-stu-id="68e0a-588">defenderAttackSurfaceType</span></span>](../resources/intune-deviceconfig-defenderattacksurfacetype.md)|<span data-ttu-id="68e0a-589">Valor que indica el comportamiento de la aplicación de Office para iniciar procesos secundarios.</span><span class="sxs-lookup"><span data-stu-id="68e0a-589">Value indicating the behavior of Office application launching child processes.</span></span> <span data-ttu-id="68e0a-590">Los valores posibles son: `userDefined`, `block` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-590">Possible values are: `userDefined`, `block`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-591">defenderOfficeAppsLaunchChildProcess</span><span class="sxs-lookup"><span data-stu-id="68e0a-591">defenderOfficeAppsLaunchChildProcess</span></span>|[<span data-ttu-id="68e0a-592">defenderProtectionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-592">defenderProtectionType</span></span>](../resources/intune-deviceconfig-defenderprotectiontype.md)|<span data-ttu-id="68e0a-593">Valor que indica el comportamiento de la aplicación de Office para iniciar procesos secundarios.</span><span class="sxs-lookup"><span data-stu-id="68e0a-593">Value indicating the behavior of Office application launching child processes.</span></span> <span data-ttu-id="68e0a-594">Los valores posibles son: `userDefined`, `enable` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-594">Possible values are: `userDefined`, `enable`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-595">defenderOfficeMacroCodeAllowWin32ImportsType</span><span class="sxs-lookup"><span data-stu-id="68e0a-595">defenderOfficeMacroCodeAllowWin32ImportsType</span></span>|[<span data-ttu-id="68e0a-596">defenderAttackSurfaceType</span><span class="sxs-lookup"><span data-stu-id="68e0a-596">defenderAttackSurfaceType</span></span>](../resources/intune-deviceconfig-defenderattacksurfacetype.md)|<span data-ttu-id="68e0a-597">Valor que indica el comportamiento de Win32 que se importa desde el código de Macro de Office.</span><span class="sxs-lookup"><span data-stu-id="68e0a-597">Value indicating the behavior of Win32 imports from Macro code in Office.</span></span> <span data-ttu-id="68e0a-598">Los valores posibles son: `userDefined`, `block` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-598">Possible values are: `userDefined`, `block`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-599">defenderOfficeMacroCodeAllowWin32Imports</span><span class="sxs-lookup"><span data-stu-id="68e0a-599">defenderOfficeMacroCodeAllowWin32Imports</span></span>|[<span data-ttu-id="68e0a-600">defenderProtectionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-600">defenderProtectionType</span></span>](../resources/intune-deviceconfig-defenderprotectiontype.md)|<span data-ttu-id="68e0a-601">Valor que indica el comportamiento de Win32 que se importa desde el código de Macro de Office.</span><span class="sxs-lookup"><span data-stu-id="68e0a-601">Value indicating the behavior of Win32 imports from Macro code in Office.</span></span> <span data-ttu-id="68e0a-602">Los valores posibles son: `userDefined`, `enable` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-602">Possible values are: `userDefined`, `enable`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-603">defenderScriptObfuscatedMacroCodeType</span><span class="sxs-lookup"><span data-stu-id="68e0a-603">defenderScriptObfuscatedMacroCodeType</span></span>|[<span data-ttu-id="68e0a-604">defenderAttackSurfaceType</span><span class="sxs-lookup"><span data-stu-id="68e0a-604">defenderAttackSurfaceType</span></span>](../resources/intune-deviceconfig-defenderattacksurfacetype.md)|<span data-ttu-id="68e0a-605">Valor que indica el comportamiento del código de macro/js/vbs/ps alterada.</span><span class="sxs-lookup"><span data-stu-id="68e0a-605">Value indicating the behavior of obfuscated js/vbs/ps/macro code.</span></span> <span data-ttu-id="68e0a-606">Los valores posibles son: `userDefined`, `block` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-606">Possible values are: `userDefined`, `block`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-607">defenderScriptObfuscatedMacroCode</span><span class="sxs-lookup"><span data-stu-id="68e0a-607">defenderScriptObfuscatedMacroCode</span></span>|[<span data-ttu-id="68e0a-608">defenderProtectionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-608">defenderProtectionType</span></span>](../resources/intune-deviceconfig-defenderprotectiontype.md)|<span data-ttu-id="68e0a-609">Valor que indica el comportamiento del código de macro/js/vbs/ps alterada.</span><span class="sxs-lookup"><span data-stu-id="68e0a-609">Value indicating the behavior of obfuscated js/vbs/ps/macro code.</span></span> <span data-ttu-id="68e0a-610">Los valores posibles son: `userDefined`, `enable` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-610">Possible values are: `userDefined`, `enable`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-611">defenderScriptDownloadedPayloadExecutionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-611">defenderScriptDownloadedPayloadExecutionType</span></span>|[<span data-ttu-id="68e0a-612">defenderAttackSurfaceType</span><span class="sxs-lookup"><span data-stu-id="68e0a-612">defenderAttackSurfaceType</span></span>](../resources/intune-deviceconfig-defenderattacksurfacetype.md)|<span data-ttu-id="68e0a-613">Valor que indica el comportamiento de ejecución carga js/vbs descarga desde Internet.</span><span class="sxs-lookup"><span data-stu-id="68e0a-613">Value indicating the behavior of js/vbs executing payload downloaded from Internet.</span></span> <span data-ttu-id="68e0a-614">Los valores posibles son: `userDefined`, `block` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-614">Possible values are: `userDefined`, `block`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-615">defenderScriptDownloadedPayloadExecution</span><span class="sxs-lookup"><span data-stu-id="68e0a-615">defenderScriptDownloadedPayloadExecution</span></span>|[<span data-ttu-id="68e0a-616">defenderProtectionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-616">defenderProtectionType</span></span>](../resources/intune-deviceconfig-defenderprotectiontype.md)|<span data-ttu-id="68e0a-617">Valor que indica el comportamiento de ejecución carga js/vbs descarga desde Internet.</span><span class="sxs-lookup"><span data-stu-id="68e0a-617">Value indicating the behavior of js/vbs executing payload downloaded from Internet.</span></span> <span data-ttu-id="68e0a-618">Los valores posibles son: `userDefined`, `enable` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-618">Possible values are: `userDefined`, `enable`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-619">defenderPreventCredentialStealingType</span><span class="sxs-lookup"><span data-stu-id="68e0a-619">defenderPreventCredentialStealingType</span></span>|[<span data-ttu-id="68e0a-620">defenderProtectionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-620">defenderProtectionType</span></span>](../resources/intune-deviceconfig-defenderprotectiontype.md)|<span data-ttu-id="68e0a-621">Valor que indica si se permite la credencial robar desde el subsistema de autoridad de seguridad local de Windows.</span><span class="sxs-lookup"><span data-stu-id="68e0a-621">Value indicating if credential stealing from the Windows local security authority subsystem is permitted.</span></span> <span data-ttu-id="68e0a-622">Los valores posibles son: `userDefined`, `enable` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-622">Possible values are: `userDefined`, `enable`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-623">defenderProcessCreationType</span><span class="sxs-lookup"><span data-stu-id="68e0a-623">defenderProcessCreationType</span></span>|[<span data-ttu-id="68e0a-624">defenderAttackSurfaceType</span><span class="sxs-lookup"><span data-stu-id="68e0a-624">defenderAttackSurfaceType</span></span>](../resources/intune-deviceconfig-defenderattacksurfacetype.md)|<span data-ttu-id="68e0a-625">El valor de respuesta que indica a creaciones de proceso que se originan desde los comandos PSExec y WMI.</span><span class="sxs-lookup"><span data-stu-id="68e0a-625">Value indicating response to process creations originating from PSExec and WMI commands.</span></span> <span data-ttu-id="68e0a-626">Los valores posibles son: `userDefined`, `block` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-626">Possible values are: `userDefined`, `block`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-627">defenderProcessCreation</span><span class="sxs-lookup"><span data-stu-id="68e0a-627">defenderProcessCreation</span></span>|[<span data-ttu-id="68e0a-628">defenderProtectionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-628">defenderProtectionType</span></span>](../resources/intune-deviceconfig-defenderprotectiontype.md)|<span data-ttu-id="68e0a-629">El valor de respuesta que indica a creaciones de proceso que se originan desde los comandos PSExec y WMI.</span><span class="sxs-lookup"><span data-stu-id="68e0a-629">Value indicating response to process creations originating from PSExec and WMI commands.</span></span> <span data-ttu-id="68e0a-630">Los valores posibles son: `userDefined`, `enable` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-630">Possible values are: `userDefined`, `enable`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-631">defenderUntrustedUSBProcessType</span><span class="sxs-lookup"><span data-stu-id="68e0a-631">defenderUntrustedUSBProcessType</span></span>|[<span data-ttu-id="68e0a-632">defenderAttackSurfaceType</span><span class="sxs-lookup"><span data-stu-id="68e0a-632">defenderAttackSurfaceType</span></span>](../resources/intune-deviceconfig-defenderattacksurfacetype.md)|<span data-ttu-id="68e0a-633">Valor que indica la respuesta a sin firmar y que no son procesos que se ejecutan desde USB.</span><span class="sxs-lookup"><span data-stu-id="68e0a-633">Value indicating response to untrusted and unsigned processes that run from USB.</span></span> <span data-ttu-id="68e0a-634">Los valores posibles son: `userDefined`, `block` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-634">Possible values are: `userDefined`, `block`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-635">defenderUntrustedUSBProcess</span><span class="sxs-lookup"><span data-stu-id="68e0a-635">defenderUntrustedUSBProcess</span></span>|[<span data-ttu-id="68e0a-636">defenderProtectionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-636">defenderProtectionType</span></span>](../resources/intune-deviceconfig-defenderprotectiontype.md)|<span data-ttu-id="68e0a-637">Valor que indica la respuesta a sin firmar y que no son procesos que se ejecutan desde USB.</span><span class="sxs-lookup"><span data-stu-id="68e0a-637">Value indicating response to untrusted and unsigned processes that run from USB.</span></span> <span data-ttu-id="68e0a-638">Los valores posibles son: `userDefined`, `enable` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-638">Possible values are: `userDefined`, `enable`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-639">defenderUntrustedExecutableType</span><span class="sxs-lookup"><span data-stu-id="68e0a-639">defenderUntrustedExecutableType</span></span>|[<span data-ttu-id="68e0a-640">defenderAttackSurfaceType</span><span class="sxs-lookup"><span data-stu-id="68e0a-640">defenderAttackSurfaceType</span></span>](../resources/intune-deviceconfig-defenderattacksurfacetype.md)|<span data-ttu-id="68e0a-641">Valor que indica la respuesta a los archivos ejecutables que no cumplen con una frecuencia, edad o la lista de confianza criterios.</span><span class="sxs-lookup"><span data-stu-id="68e0a-641">Value indicating response to executables that don't meet a prevalence, age, or trusted list criteria.</span></span> <span data-ttu-id="68e0a-642">Los valores posibles son: `userDefined`, `block` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-642">Possible values are: `userDefined`, `block`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-643">defenderUntrustedExecutable</span><span class="sxs-lookup"><span data-stu-id="68e0a-643">defenderUntrustedExecutable</span></span>|[<span data-ttu-id="68e0a-644">defenderProtectionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-644">defenderProtectionType</span></span>](../resources/intune-deviceconfig-defenderprotectiontype.md)|<span data-ttu-id="68e0a-645">Valor que indica la respuesta a los archivos ejecutables que no cumplen con una frecuencia, edad o la lista de confianza criterios.</span><span class="sxs-lookup"><span data-stu-id="68e0a-645">Value indicating response to executables that don't meet a prevalence, age, or trusted list criteria.</span></span> <span data-ttu-id="68e0a-646">Los valores posibles son: `userDefined`, `enable` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-646">Possible values are: `userDefined`, `enable`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-647">defenderEmailContentExecutionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-647">defenderEmailContentExecutionType</span></span>|[<span data-ttu-id="68e0a-648">defenderAttackSurfaceType</span><span class="sxs-lookup"><span data-stu-id="68e0a-648">defenderAttackSurfaceType</span></span>](../resources/intune-deviceconfig-defenderattacksurfacetype.md)|<span data-ttu-id="68e0a-649">Valor que indica si la ejecución de contenido ejecutable (exe, dll, ps, js, vbs, etcetera) debe quitarse de correo electrónico (correo electrónico Web/correo-cliente).</span><span class="sxs-lookup"><span data-stu-id="68e0a-649">Value indicating if execution of executable content (exe, dll, ps, js, vbs, etc) should be dropped from email (webmail/mail-client).</span></span> <span data-ttu-id="68e0a-650">Los valores posibles son: `userDefined`, `block` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-650">Possible values are: `userDefined`, `block`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-651">defenderEmailContentExecution</span><span class="sxs-lookup"><span data-stu-id="68e0a-651">defenderEmailContentExecution</span></span>|[<span data-ttu-id="68e0a-652">defenderProtectionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-652">defenderProtectionType</span></span>](../resources/intune-deviceconfig-defenderprotectiontype.md)|<span data-ttu-id="68e0a-653">Valor que indica si la ejecución de contenido ejecutable (exe, dll, ps, js, vbs, etcetera) debe quitarse de correo electrónico (correo electrónico Web/correo-cliente).</span><span class="sxs-lookup"><span data-stu-id="68e0a-653">Value indicating if execution of executable content (exe, dll, ps, js, vbs, etc) should be dropped from email (webmail/mail-client).</span></span> <span data-ttu-id="68e0a-654">Los valores posibles son: `userDefined`, `enable` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-654">Possible values are: `userDefined`, `enable`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-655">defenderAdvancedRansomewareProtectionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-655">defenderAdvancedRansomewareProtectionType</span></span>|[<span data-ttu-id="68e0a-656">defenderProtectionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-656">defenderProtectionType</span></span>](../resources/intune-deviceconfig-defenderprotectiontype.md)|<span data-ttu-id="68e0a-657">Valor que indica el uso de la protección avanzada frente a ransomeware.</span><span class="sxs-lookup"><span data-stu-id="68e0a-657">Value indicating use of advanced protection against ransomeware.</span></span> <span data-ttu-id="68e0a-658">Los valores posibles son: `userDefined`, `enable` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-658">Possible values are: `userDefined`, `enable`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-659">defenderGuardMyFoldersType</span><span class="sxs-lookup"><span data-stu-id="68e0a-659">defenderGuardMyFoldersType</span></span>|[<span data-ttu-id="68e0a-660">folderProtectionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-660">folderProtectionType</span></span>](../resources/intune-deviceconfig-folderprotectiontype.md)|<span data-ttu-id="68e0a-661">Valor que indica el comportamiento de carpetas protegidas.</span><span class="sxs-lookup"><span data-stu-id="68e0a-661">Value indicating the behavior of protected folders.</span></span> <span data-ttu-id="68e0a-662">Los valores posibles son: `userDefined`, `enable`, `auditMode`, `blockDiskModification` y `auditDiskModification`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-662">Possible values are: `userDefined`, `enable`, `auditMode`, `blockDiskModification`, `auditDiskModification`.</span></span>|
|<span data-ttu-id="68e0a-663">defenderGuardedFoldersAllowedAppPaths</span><span class="sxs-lookup"><span data-stu-id="68e0a-663">defenderGuardedFoldersAllowedAppPaths</span></span>|<span data-ttu-id="68e0a-664">Colección String</span><span class="sxs-lookup"><span data-stu-id="68e0a-664">String collection</span></span>|<span data-ttu-id="68e0a-665">Lista de rutas de acceso a exe que pueden obtener acceso a carpetas protegidas.</span><span class="sxs-lookup"><span data-stu-id="68e0a-665">List of paths to exe that are allowed to access protected folders</span></span>|
|<span data-ttu-id="68e0a-666">defenderAdditionalGuardedFolders</span><span class="sxs-lookup"><span data-stu-id="68e0a-666">defenderAdditionalGuardedFolders</span></span>|<span data-ttu-id="68e0a-667">Colección String</span><span class="sxs-lookup"><span data-stu-id="68e0a-667">String collection</span></span>|<span data-ttu-id="68e0a-668">Lista de las rutas de acceso de carpeta que se van a agregar a la lista de carpetas protegidas.</span><span class="sxs-lookup"><span data-stu-id="68e0a-668">List of folder paths to be added to the list of protected folders</span></span>|
|<span data-ttu-id="68e0a-669">defenderNetworkProtectionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-669">defenderNetworkProtectionType</span></span>|[<span data-ttu-id="68e0a-670">defenderProtectionType</span><span class="sxs-lookup"><span data-stu-id="68e0a-670">defenderProtectionType</span></span>](../resources/intune-deviceconfig-defenderprotectiontype.md)|<span data-ttu-id="68e0a-671">Valor que indica el comportamiento de NetworkProtection.</span><span class="sxs-lookup"><span data-stu-id="68e0a-671">Value indicating the behavior of NetworkProtection.</span></span> <span data-ttu-id="68e0a-672">Los valores posibles son: `userDefined`, `enable` y `auditMode`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-672">Possible values are: `userDefined`, `enable`, `auditMode`.</span></span>|
|<span data-ttu-id="68e0a-673">defenderExploitProtectionXml</span><span class="sxs-lookup"><span data-stu-id="68e0a-673">defenderExploitProtectionXml</span></span>|<span data-ttu-id="68e0a-674">Binario</span><span class="sxs-lookup"><span data-stu-id="68e0a-674">Binary</span></span>|<span data-ttu-id="68e0a-675">Contenido XML que contiene información sobre detalles de protección contra vulnerabilidades de seguridad.</span><span class="sxs-lookup"><span data-stu-id="68e0a-675">Xml content containing information regarding exploit protection details.</span></span>|
|<span data-ttu-id="68e0a-676">defenderExploitProtectionXmlFileName</span><span class="sxs-lookup"><span data-stu-id="68e0a-676">defenderExploitProtectionXmlFileName</span></span>|<span data-ttu-id="68e0a-677">Cadena</span><span class="sxs-lookup"><span data-stu-id="68e0a-677">String</span></span>|<span data-ttu-id="68e0a-678">Nombre del archivo del que se obtuvo DefenderExploitProtectionXml.</span><span class="sxs-lookup"><span data-stu-id="68e0a-678">Name of the file from which DefenderExploitProtectionXml was obtained.</span></span>|
|<span data-ttu-id="68e0a-679">defenderSecurityCenterBlockExploitProtectionOverride</span><span class="sxs-lookup"><span data-stu-id="68e0a-679">defenderSecurityCenterBlockExploitProtectionOverride</span></span>|<span data-ttu-id="68e0a-680">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-680">Boolean</span></span>|<span data-ttu-id="68e0a-681">Indica si se va a impedir que el usuario invalide la configuración de protección contra vulnerabilidades.</span><span class="sxs-lookup"><span data-stu-id="68e0a-681">Indicates whether or not to block user from overriding Exploit Protection settings.</span></span>|
|<span data-ttu-id="68e0a-682">appLockerApplicationControl</span><span class="sxs-lookup"><span data-stu-id="68e0a-682">appLockerApplicationControl</span></span>|[<span data-ttu-id="68e0a-683">appLockerApplicationControlType</span><span class="sxs-lookup"><span data-stu-id="68e0a-683">appLockerApplicationControlType</span></span>](../resources/intune-deviceconfig-applockerapplicationcontroltype.md)|<span data-ttu-id="68e0a-684">Permite que el administrador elija los tipos de aplicación que se permiten en los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-684">Enables the Admin to choose what types of app to allow on devices.</span></span> <span data-ttu-id="68e0a-685">Los valores posibles son: `notConfigured`, `enforceComponentsAndStoreApps`, `auditComponentsAndStoreApps`, `enforceComponentsStoreAppsAndSmartlocker` y `auditComponentsStoreAppsAndSmartlocker`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-685">Possible values are: `notConfigured`, `enforceComponentsAndStoreApps`, `auditComponentsAndStoreApps`, `enforceComponentsStoreAppsAndSmartlocker`, `auditComponentsStoreAppsAndSmartlocker`.</span></span>|
|<span data-ttu-id="68e0a-686">deviceGuardLocalSystemAuthorityCredentialGuardSettings</span><span class="sxs-lookup"><span data-stu-id="68e0a-686">deviceGuardLocalSystemAuthorityCredentialGuardSettings</span></span>|[<span data-ttu-id="68e0a-687">deviceGuardLocalSystemAuthorityCredentialGuardType</span><span class="sxs-lookup"><span data-stu-id="68e0a-687">deviceGuardLocalSystemAuthorityCredentialGuardType</span></span>](../resources/intune-deviceconfig-deviceguardlocalsystemauthoritycredentialguardtype.md)|<span data-ttu-id="68e0a-688">Activar Guard credenciales al nivel de seguridad de la plataforma con arranque seguro y seguridad en función de virtualización están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="68e0a-688">Turn on Credential Guard when Platform Security Level with Secure Boot and Virtualization Based Security are both enabled.</span></span> <span data-ttu-id="68e0a-689">Los valores posibles son: `notConfigured`, `enableWithUEFILock` y `enableWithoutUEFILock`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-689">Possible values are: `notConfigured`, `enableWithUEFILock`, `enableWithoutUEFILock`.</span></span>|
|<span data-ttu-id="68e0a-690">deviceGuardEnableVirtualizationBasedSecurity</span><span class="sxs-lookup"><span data-stu-id="68e0a-690">deviceGuardEnableVirtualizationBasedSecurity</span></span>|<span data-ttu-id="68e0a-691">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-691">Boolean</span></span>|<span data-ttu-id="68e0a-692">Activa en la virtualización habían basada Security(VBS).</span><span class="sxs-lookup"><span data-stu-id="68e0a-692">Turns On Virtualization Based Security(VBS).</span></span>|
|<span data-ttu-id="68e0a-693">deviceGuardEnableSecureBootWithDMA</span><span class="sxs-lookup"><span data-stu-id="68e0a-693">deviceGuardEnableSecureBootWithDMA</span></span>|<span data-ttu-id="68e0a-694">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-694">Boolean</span></span>|<span data-ttu-id="68e0a-695">Especifica si el nivel de seguridad de plataforma está habilitado en el siguiente reinicio.</span><span class="sxs-lookup"><span data-stu-id="68e0a-695">Specifies whether Platform Security Level is enabled at next reboot.</span></span>|
|<span data-ttu-id="68e0a-696">smartScreenEnableInShell</span><span class="sxs-lookup"><span data-stu-id="68e0a-696">smartScreenEnableInShell</span></span>|<span data-ttu-id="68e0a-697">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-697">Boolean</span></span>|<span data-ttu-id="68e0a-698">Permite que los administradores de TI configuren SmartScreen para Windows.</span><span class="sxs-lookup"><span data-stu-id="68e0a-698">Allows IT Admins to configure SmartScreen for Windows.</span></span>|
|<span data-ttu-id="68e0a-699">smartScreenBlockOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="68e0a-699">smartScreenBlockOverrideForFiles</span></span>|<span data-ttu-id="68e0a-700">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-700">Boolean</span></span>|<span data-ttu-id="68e0a-701">Permite que los administradores de TI controlen si los usuarios pueden omitir advertencias de SmartScreen y ejecutar archivos malintencionados.</span><span class="sxs-lookup"><span data-stu-id="68e0a-701">Allows IT Admins to control whether users can can ignore SmartScreen warnings and run malicious files.</span></span>|
|<span data-ttu-id="68e0a-702">applicationGuardEnabled</span><span class="sxs-lookup"><span data-stu-id="68e0a-702">applicationGuardEnabled</span></span>|<span data-ttu-id="68e0a-703">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-703">Boolean</span></span>|<span data-ttu-id="68e0a-704">Habilita la Protección de aplicaciones de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="68e0a-704">Enable Windows Defender Application Guard</span></span>|
|<span data-ttu-id="68e0a-705">applicationGuardEnabledOptions</span><span class="sxs-lookup"><span data-stu-id="68e0a-705">applicationGuardEnabledOptions</span></span>|[<span data-ttu-id="68e0a-706">applicationGuardEnabledOptions</span><span class="sxs-lookup"><span data-stu-id="68e0a-706">applicationGuardEnabledOptions</span></span>](../resources/intune-deviceconfig-applicationguardenabledoptions.md)|<span data-ttu-id="68e0a-707">Habilitar a Windows Defender aplicación Guard para las versiones más recientes de Windows.</span><span class="sxs-lookup"><span data-stu-id="68e0a-707">Enable Windows Defender Application Guard for newer Windows builds.</span></span> <span data-ttu-id="68e0a-708">Los valores posibles son: `notConfigured`, `enabledForEdge`, `enabledForOffice` y `enabledForEdgeAndOffice`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-708">Possible values are: `notConfigured`, `enabledForEdge`, `enabledForOffice`, `enabledForEdgeAndOffice`.</span></span>|
|<span data-ttu-id="68e0a-709">applicationGuardBlockFileTransfer</span><span class="sxs-lookup"><span data-stu-id="68e0a-709">applicationGuardBlockFileTransfer</span></span>|[<span data-ttu-id="68e0a-710">applicationGuardBlockFileTransferType</span><span class="sxs-lookup"><span data-stu-id="68e0a-710">applicationGuardBlockFileTransferType</span></span>](../resources/intune-deviceconfig-applicationguardblockfiletransfertype.md)|<span data-ttu-id="68e0a-711">Portapapeles de bloqueo para el archivo de transferencia de imagen, archivo de texto o ninguno de ellos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-711">Block clipboard to transfer image file, text file or neither of them.</span></span> <span data-ttu-id="68e0a-712">Los valores posibles son: `notConfigured`, `blockImageAndTextFile`, `blockImageFile`, `blockNone` y `blockTextFile`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-712">Possible values are: `notConfigured`, `blockImageAndTextFile`, `blockImageFile`, `blockNone`, `blockTextFile`.</span></span>|
|<span data-ttu-id="68e0a-713">applicationGuardBlockNonEnterpriseContent</span><span class="sxs-lookup"><span data-stu-id="68e0a-713">applicationGuardBlockNonEnterpriseContent</span></span>|<span data-ttu-id="68e0a-714">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-714">Boolean</span></span>|<span data-ttu-id="68e0a-715">Impide que los sitios de la empresa carguen contenido no empresarial, como complementos de terceros.</span><span class="sxs-lookup"><span data-stu-id="68e0a-715">Block enterprise sites to load non-enterprise content, such as third party plug-ins</span></span>|
|<span data-ttu-id="68e0a-716">applicationGuardAllowPersistence</span><span class="sxs-lookup"><span data-stu-id="68e0a-716">applicationGuardAllowPersistence</span></span>|<span data-ttu-id="68e0a-717">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-717">Boolean</span></span>|<span data-ttu-id="68e0a-718">Permite el almacenamiento de los datos generados por el usuario en el contenedor de la protección de aplicaciones (favoritos, cookies, contraseñas web, etc.).</span><span class="sxs-lookup"><span data-stu-id="68e0a-718">Allow persisting user generated data inside the App Guard Containter (favorites, cookies, web passwords, etc.)</span></span>|
|<span data-ttu-id="68e0a-719">applicationGuardForceAuditing</span><span class="sxs-lookup"><span data-stu-id="68e0a-719">applicationGuardForceAuditing</span></span>|<span data-ttu-id="68e0a-720">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-720">Boolean</span></span>|<span data-ttu-id="68e0a-721">La auditoría forzada conservará los registros y eventos de Windows para cumplir con los criterios de seguridad y cumplimiento (algunos eventos de ejemplo son el inicio y cierre de sesión del usuario, el uso de derechos de privilegio, la instalación de software, los cambios del sistema, etc.).</span><span class="sxs-lookup"><span data-stu-id="68e0a-721">Force auditing will persist Windows logs and events to meet security/compliance criteria (sample events are user login-logoff, use of privilege rights, software installation, system changes, etc.)</span></span>|
|<span data-ttu-id="68e0a-722">applicationGuardBlockClipboardSharing</span><span class="sxs-lookup"><span data-stu-id="68e0a-722">applicationGuardBlockClipboardSharing</span></span>|[<span data-ttu-id="68e0a-723">applicationGuardBlockClipboardSharingType</span><span class="sxs-lookup"><span data-stu-id="68e0a-723">applicationGuardBlockClipboardSharingType</span></span>](../resources/intune-deviceconfig-applicationguardblockclipboardsharingtype.md)|<span data-ttu-id="68e0a-724">Impide que el Portapapeles comparta los datos del host al contenedor, del contenedor al host, en ambas direcciones o en ninguna.</span><span class="sxs-lookup"><span data-stu-id="68e0a-724">Block clipboard to share data from Host to Container, or from Container to Host, or both ways, or neither ways.</span></span> <span data-ttu-id="68e0a-725">Los valores posibles son: `notConfigured`, `blockBoth`, `blockHostToContainer`, `blockContainerToHost` y `blockNone`.</span><span class="sxs-lookup"><span data-stu-id="68e0a-725">Possible values are: `notConfigured`, `blockBoth`, `blockHostToContainer`, `blockContainerToHost`, `blockNone`.</span></span>|
|<span data-ttu-id="68e0a-726">applicationGuardAllowPrintToPDF</span><span class="sxs-lookup"><span data-stu-id="68e0a-726">applicationGuardAllowPrintToPDF</span></span>|<span data-ttu-id="68e0a-727">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-727">Boolean</span></span>|<span data-ttu-id="68e0a-728">Permite la impresión en PDF desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="68e0a-728">Allow printing to PDF from Container</span></span>|
|<span data-ttu-id="68e0a-729">applicationGuardAllowPrintToXPS</span><span class="sxs-lookup"><span data-stu-id="68e0a-729">applicationGuardAllowPrintToXPS</span></span>|<span data-ttu-id="68e0a-730">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-730">Boolean</span></span>|<span data-ttu-id="68e0a-731">Permite la impresión en XPS desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="68e0a-731">Allow printing to XPS from Container</span></span>|
|<span data-ttu-id="68e0a-732">applicationGuardAllowPrintToLocalPrinters</span><span class="sxs-lookup"><span data-stu-id="68e0a-732">applicationGuardAllowPrintToLocalPrinters</span></span>|<span data-ttu-id="68e0a-733">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-733">Boolean</span></span>|<span data-ttu-id="68e0a-734">Permite la impresión en impresoras locales desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="68e0a-734">Allow printing to Local Printers from Container</span></span>|
|<span data-ttu-id="68e0a-735">applicationGuardAllowPrintToNetworkPrinters</span><span class="sxs-lookup"><span data-stu-id="68e0a-735">applicationGuardAllowPrintToNetworkPrinters</span></span>|<span data-ttu-id="68e0a-736">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-736">Boolean</span></span>|<span data-ttu-id="68e0a-737">Permite la impresión en impresoras en red desde el contenedor.</span><span class="sxs-lookup"><span data-stu-id="68e0a-737">Allow printing to Network Printers from Container</span></span>|
|<span data-ttu-id="68e0a-738">applicationGuardAllowVirtualGPU</span><span class="sxs-lookup"><span data-stu-id="68e0a-738">applicationGuardAllowVirtualGPU</span></span>|<span data-ttu-id="68e0a-739">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-739">Boolean</span></span>|<span data-ttu-id="68e0a-740">Permitir protección de aplicación para usar GPU virtual</span><span class="sxs-lookup"><span data-stu-id="68e0a-740">Allow application guard to use virtual GPU</span></span>|
|<span data-ttu-id="68e0a-741">applicationGuardAllowFileSaveOnHost</span><span class="sxs-lookup"><span data-stu-id="68e0a-741">applicationGuardAllowFileSaveOnHost</span></span>|<span data-ttu-id="68e0a-742">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-742">Boolean</span></span>|<span data-ttu-id="68e0a-743">Permitir a los usuarios descargar archivos desde el borde en el contenedor de protección de la aplicación y guardarlos en el host de sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="68e0a-743">Allow users to download files from Edge in the application guard container and save them on the host file system</span></span>|
|<span data-ttu-id="68e0a-744">bitLockerDisableWarningForOtherDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="68e0a-744">bitLockerDisableWarningForOtherDiskEncryption</span></span>|<span data-ttu-id="68e0a-745">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-745">Boolean</span></span>|<span data-ttu-id="68e0a-746">Permite que el administrador deshabilite el mensaje de advertencia para otro cifrado de disco en los equipos de usuario.</span><span class="sxs-lookup"><span data-stu-id="68e0a-746">Allows the Admin to disable the warning prompt for other disk encryption on the user machines.</span></span>|
|<span data-ttu-id="68e0a-747">bitLockerEnableStorageCardEncryptionOnMobile</span><span class="sxs-lookup"><span data-stu-id="68e0a-747">bitLockerEnableStorageCardEncryptionOnMobile</span></span>|<span data-ttu-id="68e0a-748">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-748">Boolean</span></span>|<span data-ttu-id="68e0a-749">Permite que el administrador exija que se active el cifrado con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="68e0a-749">Allows the admin to require encryption to be turned on using BitLocker.</span></span> <span data-ttu-id="68e0a-750">Esta directiva solo es válida para una SKU móvil.</span><span class="sxs-lookup"><span data-stu-id="68e0a-750">This policy is valid only for a mobile SKU.</span></span>|
|<span data-ttu-id="68e0a-751">bitLockerEncryptDevice</span><span class="sxs-lookup"><span data-stu-id="68e0a-751">bitLockerEncryptDevice</span></span>|<span data-ttu-id="68e0a-752">Booleano</span><span class="sxs-lookup"><span data-stu-id="68e0a-752">Boolean</span></span>|<span data-ttu-id="68e0a-753">Permite que el administrador exija que se active el cifrado con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="68e0a-753">Allows the admin to require encryption to be turned on using BitLocker.</span></span>|
|<span data-ttu-id="68e0a-754">bitLockerSystemDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="68e0a-754">bitLockerSystemDrivePolicy</span></span>|[<span data-ttu-id="68e0a-755">bitLockerSystemDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="68e0a-755">bitLockerSystemDrivePolicy</span></span>](../resources/intune-deviceconfig-bitlockersystemdrivepolicy.md)|<span data-ttu-id="68e0a-756">Directiva de la unidad del sistema de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="68e0a-756">BitLocker System Drive Policy.</span></span>|
|<span data-ttu-id="68e0a-757">bitLockerFixedDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="68e0a-757">bitLockerFixedDrivePolicy</span></span>|[<span data-ttu-id="68e0a-758">bitLockerFixedDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="68e0a-758">bitLockerFixedDrivePolicy</span></span>](../resources/intune-deviceconfig-bitlockerfixeddrivepolicy.md)|<span data-ttu-id="68e0a-759">Rol fijo de directiva de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="68e0a-759">BitLocker Fixed Drive Policy.</span></span>|
|<span data-ttu-id="68e0a-760">bitLockerRemovableDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="68e0a-760">bitLockerRemovableDrivePolicy</span></span>|[<span data-ttu-id="68e0a-761">bitLockerRemovableDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="68e0a-761">bitLockerRemovableDrivePolicy</span></span>](../resources/intune-deviceconfig-bitlockerremovabledrivepolicy.md)|<span data-ttu-id="68e0a-762">Directiva de unidad extraíble de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="68e0a-762">BitLocker Removable Drive Policy.</span></span>|



## <a name="response"></a><span data-ttu-id="68e0a-763">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68e0a-763">Response</span></span>
<span data-ttu-id="68e0a-764">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68e0a-764">If successful, this method returns a `200 OK` response code and an updated [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="68e0a-765">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="68e0a-765">Example</span></span>
### <a name="request"></a><span data-ttu-id="68e0a-766">Solicitud</span><span class="sxs-lookup"><span data-stu-id="68e0a-766">Request</span></span>
<span data-ttu-id="68e0a-767">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="68e0a-767">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 26312

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "userRightsAccessCredentialManagerAsTrustedCaller": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsAllowAccessFromNetwork": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsBlockAccessFromNetwork": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsActAsPartOfTheOperatingSystem": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsLocalLogOn": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsBackupData": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsChangeSystemTime": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsCreateGlobalObjects": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsCreatePageFile": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsCreatePermanentSharedObjects": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsCreateSymbolicLinks": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsCreateToken": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsDebugPrograms": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsRemoteDesktopServicesLogOn": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsDelegation": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsGenerateSecurityAudits": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsImpersonateClient": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsIncreaseSchedulingPriority": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsLoadUnloadDrivers": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsLockMemory": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsManageAuditingAndSecurityLogs": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsManageVolumes": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsModifyFirmwareEnvironment": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsModifyObjectLabels": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsProfileSingleProcess": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsRemoteShutdown": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsRestoreData": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsTakeOwnership": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsRegisterProcessAsService": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "xboxServicesEnableXboxGameSaveTask": true,
  "xboxServicesAccessoryManagementServiceStartupMode": "automatic",
  "xboxServicesLiveAuthManagerServiceStartupMode": "automatic",
  "xboxServicesLiveGameSaveServiceStartupMode": "automatic",
  "xboxServicesLiveNetworkingServiceStartupMode": "automatic",
  "localSecurityOptionsBlockMicrosoftAccounts": true,
  "localSecurityOptionsBlockRemoteLogonWithBlankPassword": true,
  "localSecurityOptionsEnableAdministratorAccount": true,
  "localSecurityOptionsAdministratorAccountName": "Local Security Options Administrator Account Name value",
  "localSecurityOptionsEnableGuestAccount": true,
  "localSecurityOptionsGuestAccountName": "Local Security Options Guest Account Name value",
  "localSecurityOptionsAllowUndockWithoutHavingToLogon": true,
  "localSecurityOptionsBlockUsersInstallingPrinterDrivers": true,
  "localSecurityOptionsBlockRemoteOpticalDriveAccess": true,
  "localSecurityOptionsFormatAndEjectOfRemovableMediaAllowedUser": "administrators",
  "localSecurityOptionsMachineInactivityLimit": 10,
  "localSecurityOptionsMachineInactivityLimitInMinutes": 3,
  "localSecurityOptionsDoNotRequireCtrlAltDel": true,
  "localSecurityOptionsHideLastSignedInUser": true,
  "localSecurityOptionsHideUsernameAtSignIn": true,
  "localSecurityOptionsLogOnMessageTitle": "Local Security Options Log On Message Title value",
  "localSecurityOptionsLogOnMessageText": "Local Security Options Log On Message Text value",
  "localSecurityOptionsAllowPKU2UAuthenticationRequests": true,
  "localSecurityOptionsAllowRemoteCallsToSecurityAccountsManagerHelperBool": true,
  "localSecurityOptionsAllowRemoteCallsToSecurityAccountsManager": "Local Security Options Allow Remote Calls To Security Accounts Manager value",
  "localSecurityOptionsMinimumSessionSecurityForNtlmSspBasedClients": "requireNtmlV2SessionSecurity",
  "localSecurityOptionsMinimumSessionSecurityForNtlmSspBasedServers": "requireNtmlV2SessionSecurity",
  "lanManagerAuthenticationLevel": "lmNtlmAndNtlmV2",
  "lanManagerWorkstationEnableInsecureGuestLogons": true,
  "localSecurityOptionsClearVirtualMemoryPageFile": true,
  "localSecurityOptionsAllowSystemToBeShutDownWithoutHavingToLogOn": true,
  "localSecurityOptionsAllowUIAccessApplicationElevation": true,
  "localSecurityOptionsVirtualizeFileAndRegistryWriteFailuresToPerUserLocations": true,
  "localSecurityOptionsOnlyElevateSignedExecutables": true,
  "localSecurityOptionsAdministratorElevationPromptBehavior": "elevateWithoutPrompting",
  "localSecurityOptionsStandardUserElevationPromptBehavior": "automaticallyDenyElevationRequests",
  "localSecurityOptionsSwitchToSecureDesktopWhenPromptingForElevation": true,
  "localSecurityOptionsDetectApplicationInstallationsAndPromptForElevation": true,
  "localSecurityOptionsAllowUIAccessApplicationsForSecureLocations": true,
  "localSecurityOptionsUseAdminApprovalMode": true,
  "localSecurityOptionsUseAdminApprovalModeForAdministrators": true,
  "localSecurityOptionsInformationShownOnLockScreen": "userDisplayNameDomainUser",
  "localSecurityOptionsInformationDisplayedOnLockScreen": "administrators",
  "localSecurityOptionsDisableClientDigitallySignCommunicationsIfServerAgrees": true,
  "localSecurityOptionsClientDigitallySignCommunicationsAlways": true,
  "localSecurityOptionsClientSendUnencryptedPasswordToThirdPartySMBServers": true,
  "localSecurityOptionsDisableServerDigitallySignCommunicationsAlways": true,
  "localSecurityOptionsDisableServerDigitallySignCommunicationsIfClientAgrees": true,
  "localSecurityOptionsRestrictAnonymousAccessToNamedPipesAndShares": true,
  "localSecurityOptionsDoNotAllowAnonymousEnumerationOfSAMAccounts": true,
  "localSecurityOptionsAllowAnonymousEnumerationOfSAMAccountsAndShares": true,
  "localSecurityOptionsDoNotStoreLANManagerHashValueOnNextPasswordChange": true,
  "localSecurityOptionsSmartCardRemovalBehavior": "noAction",
  "defenderSecurityCenterDisableAppBrowserUI": true,
  "defenderSecurityCenterDisableFamilyUI": true,
  "defenderSecurityCenterDisableHealthUI": true,
  "defenderSecurityCenterDisableNetworkUI": true,
  "defenderSecurityCenterDisableVirusUI": true,
  "defenderSecurityCenterDisableAccountUI": true,
  "defenderSecurityCenterDisableHardwareUI": true,
  "defenderSecurityCenterDisableRansomwareUI": true,
  "defenderSecurityCenterDisableSecureBootUI": true,
  "defenderSecurityCenterDisableTroubleshootingUI": true,
  "defenderSecurityCenterOrganizationDisplayName": "Defender Security Center Organization Display Name value",
  "defenderSecurityCenterHelpEmail": "Defender Security Center Help Email value",
  "defenderSecurityCenterHelpPhone": "Defender Security Center Help Phone value",
  "defenderSecurityCenterHelpURL": "Defender Security Center Help URL value",
  "defenderSecurityCenterNotificationsFromApp": "blockNoncriticalNotifications",
  "defenderSecurityCenterITContactDisplay": "displayInAppAndInNotifications",
  "firewallBlockStatefulFTP": true,
  "firewallIdleTimeoutForSecurityAssociationInSeconds": 2,
  "firewallPreSharedKeyEncodingMethod": "none",
  "firewallIPSecExemptionsAllowNeighborDiscovery": true,
  "firewallIPSecExemptionsAllowICMP": true,
  "firewallIPSecExemptionsAllowRouterDiscovery": true,
  "firewallIPSecExemptionsAllowDHCP": true,
  "firewallCertificateRevocationListCheckMethod": "none",
  "firewallMergeKeyingModuleSettings": true,
  "firewallPacketQueueingMethod": "disabled",
  "firewallProfileDomain": {
    "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
    "firewallEnabled": "blocked",
    "stealthModeRequired": true,
    "stealthModeBlocked": true,
    "incomingTrafficRequired": true,
    "incomingTrafficBlocked": true,
    "unicastResponsesToMulticastBroadcastsRequired": true,
    "unicastResponsesToMulticastBroadcastsBlocked": true,
    "inboundNotificationsRequired": true,
    "inboundNotificationsBlocked": true,
    "authorizedApplicationRulesFromGroupPolicyMerged": true,
    "authorizedApplicationRulesFromGroupPolicyNotMerged": true,
    "globalPortRulesFromGroupPolicyMerged": true,
    "globalPortRulesFromGroupPolicyNotMerged": true,
    "connectionSecurityRulesFromGroupPolicyMerged": true,
    "connectionSecurityRulesFromGroupPolicyNotMerged": true,
    "outboundConnectionsRequired": true,
    "outboundConnectionsBlocked": true,
    "inboundConnectionsRequired": true,
    "inboundConnectionsBlocked": true,
    "securedPacketExemptionAllowed": true,
    "securedPacketExemptionBlocked": true,
    "policyRulesFromGroupPolicyMerged": true,
    "policyRulesFromGroupPolicyNotMerged": true
  },
  "firewallProfilePublic": {
    "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
    "firewallEnabled": "blocked",
    "stealthModeRequired": true,
    "stealthModeBlocked": true,
    "incomingTrafficRequired": true,
    "incomingTrafficBlocked": true,
    "unicastResponsesToMulticastBroadcastsRequired": true,
    "unicastResponsesToMulticastBroadcastsBlocked": true,
    "inboundNotificationsRequired": true,
    "inboundNotificationsBlocked": true,
    "authorizedApplicationRulesFromGroupPolicyMerged": true,
    "authorizedApplicationRulesFromGroupPolicyNotMerged": true,
    "globalPortRulesFromGroupPolicyMerged": true,
    "globalPortRulesFromGroupPolicyNotMerged": true,
    "connectionSecurityRulesFromGroupPolicyMerged": true,
    "connectionSecurityRulesFromGroupPolicyNotMerged": true,
    "outboundConnectionsRequired": true,
    "outboundConnectionsBlocked": true,
    "inboundConnectionsRequired": true,
    "inboundConnectionsBlocked": true,
    "securedPacketExemptionAllowed": true,
    "securedPacketExemptionBlocked": true,
    "policyRulesFromGroupPolicyMerged": true,
    "policyRulesFromGroupPolicyNotMerged": true
  },
  "firewallProfilePrivate": {
    "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
    "firewallEnabled": "blocked",
    "stealthModeRequired": true,
    "stealthModeBlocked": true,
    "incomingTrafficRequired": true,
    "incomingTrafficBlocked": true,
    "unicastResponsesToMulticastBroadcastsRequired": true,
    "unicastResponsesToMulticastBroadcastsBlocked": true,
    "inboundNotificationsRequired": true,
    "inboundNotificationsBlocked": true,
    "authorizedApplicationRulesFromGroupPolicyMerged": true,
    "authorizedApplicationRulesFromGroupPolicyNotMerged": true,
    "globalPortRulesFromGroupPolicyMerged": true,
    "globalPortRulesFromGroupPolicyNotMerged": true,
    "connectionSecurityRulesFromGroupPolicyMerged": true,
    "connectionSecurityRulesFromGroupPolicyNotMerged": true,
    "outboundConnectionsRequired": true,
    "outboundConnectionsBlocked": true,
    "inboundConnectionsRequired": true,
    "inboundConnectionsBlocked": true,
    "securedPacketExemptionAllowed": true,
    "securedPacketExemptionBlocked": true,
    "policyRulesFromGroupPolicyMerged": true,
    "policyRulesFromGroupPolicyNotMerged": true
  },
  "defenderAttackSurfaceReductionExcludedPaths": [
    "Defender Attack Surface Reduction Excluded Paths value"
  ],
  "defenderOfficeAppsOtherProcessInjectionType": "block",
  "defenderOfficeAppsOtherProcessInjection": "enable",
  "defenderOfficeAppsExecutableContentCreationOrLaunchType": "block",
  "defenderOfficeAppsExecutableContentCreationOrLaunch": "enable",
  "defenderOfficeAppsLaunchChildProcessType": "block",
  "defenderOfficeAppsLaunchChildProcess": "enable",
  "defenderOfficeMacroCodeAllowWin32ImportsType": "block",
  "defenderOfficeMacroCodeAllowWin32Imports": "enable",
  "defenderScriptObfuscatedMacroCodeType": "block",
  "defenderScriptObfuscatedMacroCode": "enable",
  "defenderScriptDownloadedPayloadExecutionType": "block",
  "defenderScriptDownloadedPayloadExecution": "enable",
  "defenderPreventCredentialStealingType": "enable",
  "defenderProcessCreationType": "block",
  "defenderProcessCreation": "enable",
  "defenderUntrustedUSBProcessType": "block",
  "defenderUntrustedUSBProcess": "enable",
  "defenderUntrustedExecutableType": "block",
  "defenderUntrustedExecutable": "enable",
  "defenderEmailContentExecutionType": "block",
  "defenderEmailContentExecution": "enable",
  "defenderAdvancedRansomewareProtectionType": "enable",
  "defenderGuardMyFoldersType": "enable",
  "defenderGuardedFoldersAllowedAppPaths": [
    "Defender Guarded Folders Allowed App Paths value"
  ],
  "defenderAdditionalGuardedFolders": [
    "Defender Additional Guarded Folders value"
  ],
  "defenderNetworkProtectionType": "enable",
  "defenderExploitProtectionXml": "ZGVmZW5kZXJFeHBsb2l0UHJvdGVjdGlvblhtbA==",
  "defenderExploitProtectionXmlFileName": "Defender Exploit Protection Xml File Name value",
  "defenderSecurityCenterBlockExploitProtectionOverride": true,
  "appLockerApplicationControl": "enforceComponentsAndStoreApps",
  "deviceGuardLocalSystemAuthorityCredentialGuardSettings": "enableWithUEFILock",
  "deviceGuardEnableVirtualizationBasedSecurity": true,
  "deviceGuardEnableSecureBootWithDMA": true,
  "smartScreenEnableInShell": true,
  "smartScreenBlockOverrideForFiles": true,
  "applicationGuardEnabled": true,
  "applicationGuardEnabledOptions": "enabledForEdge",
  "applicationGuardBlockFileTransfer": "blockImageAndTextFile",
  "applicationGuardBlockNonEnterpriseContent": true,
  "applicationGuardAllowPersistence": true,
  "applicationGuardForceAuditing": true,
  "applicationGuardBlockClipboardSharing": "blockBoth",
  "applicationGuardAllowPrintToPDF": true,
  "applicationGuardAllowPrintToXPS": true,
  "applicationGuardAllowPrintToLocalPrinters": true,
  "applicationGuardAllowPrintToNetworkPrinters": true,
  "applicationGuardAllowVirtualGPU": true,
  "applicationGuardAllowFileSaveOnHost": true,
  "bitLockerDisableWarningForOtherDiskEncryption": true,
  "bitLockerEnableStorageCardEncryptionOnMobile": true,
  "bitLockerEncryptDevice": true,
  "bitLockerSystemDrivePolicy": {
    "@odata.type": "microsoft.graph.bitLockerSystemDrivePolicy",
    "encryptionMethod": "aesCbc256",
    "startupAuthenticationRequired": true,
    "startupAuthenticationBlockWithoutTpmChip": true,
    "startupAuthenticationTpmUsage": "required",
    "startupAuthenticationTpmPinUsage": "required",
    "startupAuthenticationTpmKeyUsage": "required",
    "startupAuthenticationTpmPinAndKeyUsage": "required",
    "minimumPinLength": 0,
    "recoveryOptions": {
      "@odata.type": "microsoft.graph.bitLockerRecoveryOptions",
      "blockDataRecoveryAgent": true,
      "recoveryPasswordUsage": "required",
      "recoveryKeyUsage": "required",
      "hideRecoveryOptions": true,
      "enableRecoveryInformationSaveToStore": true,
      "recoveryInformationToStore": "passwordOnly",
      "enableBitLockerAfterRecoveryInformationToStore": true
    },
    "prebootRecoveryEnableMessageAndUrl": true,
    "prebootRecoveryMessage": "Preboot Recovery Message value",
    "prebootRecoveryUrl": "https://example.com/prebootRecoveryUrl/"
  },
  "bitLockerFixedDrivePolicy": {
    "@odata.type": "microsoft.graph.bitLockerFixedDrivePolicy",
    "encryptionMethod": "aesCbc256",
    "requireEncryptionForWriteAccess": true,
    "recoveryOptions": {
      "@odata.type": "microsoft.graph.bitLockerRecoveryOptions",
      "blockDataRecoveryAgent": true,
      "recoveryPasswordUsage": "required",
      "recoveryKeyUsage": "required",
      "hideRecoveryOptions": true,
      "enableRecoveryInformationSaveToStore": true,
      "recoveryInformationToStore": "passwordOnly",
      "enableBitLockerAfterRecoveryInformationToStore": true
    }
  },
  "bitLockerRemovableDrivePolicy": {
    "@odata.type": "microsoft.graph.bitLockerRemovableDrivePolicy",
    "encryptionMethod": "aesCbc256",
    "requireEncryptionForWriteAccess": true,
    "blockCrossOrganizationWriteAccess": true
  }
}
```

### <a name="response"></a><span data-ttu-id="68e0a-768">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68e0a-768">Response</span></span>
<span data-ttu-id="68e0a-p194">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="68e0a-p194">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 26499

{
  "@odata.type": "#microsoft.graph.windows10EndpointProtectionConfiguration",
  "id": "09709403-9403-0970-0394-700903947009",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "userRightsAccessCredentialManagerAsTrustedCaller": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsAllowAccessFromNetwork": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsBlockAccessFromNetwork": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsActAsPartOfTheOperatingSystem": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsLocalLogOn": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsBackupData": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsChangeSystemTime": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsCreateGlobalObjects": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsCreatePageFile": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsCreatePermanentSharedObjects": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsCreateSymbolicLinks": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsCreateToken": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsDebugPrograms": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsRemoteDesktopServicesLogOn": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsDelegation": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsGenerateSecurityAudits": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsImpersonateClient": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsIncreaseSchedulingPriority": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsLoadUnloadDrivers": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsLockMemory": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsManageAuditingAndSecurityLogs": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsManageVolumes": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsModifyFirmwareEnvironment": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsModifyObjectLabels": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsProfileSingleProcess": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsRemoteShutdown": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsRestoreData": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsTakeOwnership": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "userRightsRegisterProcessAsService": {
    "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting",
    "state": "blocked",
    "localUsersOrGroups": [
      {
        "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
        "name": "Name value",
        "description": "Description value",
        "securityIdentifier": "Security Identifier value"
      }
    ]
  },
  "xboxServicesEnableXboxGameSaveTask": true,
  "xboxServicesAccessoryManagementServiceStartupMode": "automatic",
  "xboxServicesLiveAuthManagerServiceStartupMode": "automatic",
  "xboxServicesLiveGameSaveServiceStartupMode": "automatic",
  "xboxServicesLiveNetworkingServiceStartupMode": "automatic",
  "localSecurityOptionsBlockMicrosoftAccounts": true,
  "localSecurityOptionsBlockRemoteLogonWithBlankPassword": true,
  "localSecurityOptionsEnableAdministratorAccount": true,
  "localSecurityOptionsAdministratorAccountName": "Local Security Options Administrator Account Name value",
  "localSecurityOptionsEnableGuestAccount": true,
  "localSecurityOptionsGuestAccountName": "Local Security Options Guest Account Name value",
  "localSecurityOptionsAllowUndockWithoutHavingToLogon": true,
  "localSecurityOptionsBlockUsersInstallingPrinterDrivers": true,
  "localSecurityOptionsBlockRemoteOpticalDriveAccess": true,
  "localSecurityOptionsFormatAndEjectOfRemovableMediaAllowedUser": "administrators",
  "localSecurityOptionsMachineInactivityLimit": 10,
  "localSecurityOptionsMachineInactivityLimitInMinutes": 3,
  "localSecurityOptionsDoNotRequireCtrlAltDel": true,
  "localSecurityOptionsHideLastSignedInUser": true,
  "localSecurityOptionsHideUsernameAtSignIn": true,
  "localSecurityOptionsLogOnMessageTitle": "Local Security Options Log On Message Title value",
  "localSecurityOptionsLogOnMessageText": "Local Security Options Log On Message Text value",
  "localSecurityOptionsAllowPKU2UAuthenticationRequests": true,
  "localSecurityOptionsAllowRemoteCallsToSecurityAccountsManagerHelperBool": true,
  "localSecurityOptionsAllowRemoteCallsToSecurityAccountsManager": "Local Security Options Allow Remote Calls To Security Accounts Manager value",
  "localSecurityOptionsMinimumSessionSecurityForNtlmSspBasedClients": "requireNtmlV2SessionSecurity",
  "localSecurityOptionsMinimumSessionSecurityForNtlmSspBasedServers": "requireNtmlV2SessionSecurity",
  "lanManagerAuthenticationLevel": "lmNtlmAndNtlmV2",
  "lanManagerWorkstationEnableInsecureGuestLogons": true,
  "localSecurityOptionsClearVirtualMemoryPageFile": true,
  "localSecurityOptionsAllowSystemToBeShutDownWithoutHavingToLogOn": true,
  "localSecurityOptionsAllowUIAccessApplicationElevation": true,
  "localSecurityOptionsVirtualizeFileAndRegistryWriteFailuresToPerUserLocations": true,
  "localSecurityOptionsOnlyElevateSignedExecutables": true,
  "localSecurityOptionsAdministratorElevationPromptBehavior": "elevateWithoutPrompting",
  "localSecurityOptionsStandardUserElevationPromptBehavior": "automaticallyDenyElevationRequests",
  "localSecurityOptionsSwitchToSecureDesktopWhenPromptingForElevation": true,
  "localSecurityOptionsDetectApplicationInstallationsAndPromptForElevation": true,
  "localSecurityOptionsAllowUIAccessApplicationsForSecureLocations": true,
  "localSecurityOptionsUseAdminApprovalMode": true,
  "localSecurityOptionsUseAdminApprovalModeForAdministrators": true,
  "localSecurityOptionsInformationShownOnLockScreen": "userDisplayNameDomainUser",
  "localSecurityOptionsInformationDisplayedOnLockScreen": "administrators",
  "localSecurityOptionsDisableClientDigitallySignCommunicationsIfServerAgrees": true,
  "localSecurityOptionsClientDigitallySignCommunicationsAlways": true,
  "localSecurityOptionsClientSendUnencryptedPasswordToThirdPartySMBServers": true,
  "localSecurityOptionsDisableServerDigitallySignCommunicationsAlways": true,
  "localSecurityOptionsDisableServerDigitallySignCommunicationsIfClientAgrees": true,
  "localSecurityOptionsRestrictAnonymousAccessToNamedPipesAndShares": true,
  "localSecurityOptionsDoNotAllowAnonymousEnumerationOfSAMAccounts": true,
  "localSecurityOptionsAllowAnonymousEnumerationOfSAMAccountsAndShares": true,
  "localSecurityOptionsDoNotStoreLANManagerHashValueOnNextPasswordChange": true,
  "localSecurityOptionsSmartCardRemovalBehavior": "noAction",
  "defenderSecurityCenterDisableAppBrowserUI": true,
  "defenderSecurityCenterDisableFamilyUI": true,
  "defenderSecurityCenterDisableHealthUI": true,
  "defenderSecurityCenterDisableNetworkUI": true,
  "defenderSecurityCenterDisableVirusUI": true,
  "defenderSecurityCenterDisableAccountUI": true,
  "defenderSecurityCenterDisableHardwareUI": true,
  "defenderSecurityCenterDisableRansomwareUI": true,
  "defenderSecurityCenterDisableSecureBootUI": true,
  "defenderSecurityCenterDisableTroubleshootingUI": true,
  "defenderSecurityCenterOrganizationDisplayName": "Defender Security Center Organization Display Name value",
  "defenderSecurityCenterHelpEmail": "Defender Security Center Help Email value",
  "defenderSecurityCenterHelpPhone": "Defender Security Center Help Phone value",
  "defenderSecurityCenterHelpURL": "Defender Security Center Help URL value",
  "defenderSecurityCenterNotificationsFromApp": "blockNoncriticalNotifications",
  "defenderSecurityCenterITContactDisplay": "displayInAppAndInNotifications",
  "firewallBlockStatefulFTP": true,
  "firewallIdleTimeoutForSecurityAssociationInSeconds": 2,
  "firewallPreSharedKeyEncodingMethod": "none",
  "firewallIPSecExemptionsAllowNeighborDiscovery": true,
  "firewallIPSecExemptionsAllowICMP": true,
  "firewallIPSecExemptionsAllowRouterDiscovery": true,
  "firewallIPSecExemptionsAllowDHCP": true,
  "firewallCertificateRevocationListCheckMethod": "none",
  "firewallMergeKeyingModuleSettings": true,
  "firewallPacketQueueingMethod": "disabled",
  "firewallProfileDomain": {
    "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
    "firewallEnabled": "blocked",
    "stealthModeRequired": true,
    "stealthModeBlocked": true,
    "incomingTrafficRequired": true,
    "incomingTrafficBlocked": true,
    "unicastResponsesToMulticastBroadcastsRequired": true,
    "unicastResponsesToMulticastBroadcastsBlocked": true,
    "inboundNotificationsRequired": true,
    "inboundNotificationsBlocked": true,
    "authorizedApplicationRulesFromGroupPolicyMerged": true,
    "authorizedApplicationRulesFromGroupPolicyNotMerged": true,
    "globalPortRulesFromGroupPolicyMerged": true,
    "globalPortRulesFromGroupPolicyNotMerged": true,
    "connectionSecurityRulesFromGroupPolicyMerged": true,
    "connectionSecurityRulesFromGroupPolicyNotMerged": true,
    "outboundConnectionsRequired": true,
    "outboundConnectionsBlocked": true,
    "inboundConnectionsRequired": true,
    "inboundConnectionsBlocked": true,
    "securedPacketExemptionAllowed": true,
    "securedPacketExemptionBlocked": true,
    "policyRulesFromGroupPolicyMerged": true,
    "policyRulesFromGroupPolicyNotMerged": true
  },
  "firewallProfilePublic": {
    "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
    "firewallEnabled": "blocked",
    "stealthModeRequired": true,
    "stealthModeBlocked": true,
    "incomingTrafficRequired": true,
    "incomingTrafficBlocked": true,
    "unicastResponsesToMulticastBroadcastsRequired": true,
    "unicastResponsesToMulticastBroadcastsBlocked": true,
    "inboundNotificationsRequired": true,
    "inboundNotificationsBlocked": true,
    "authorizedApplicationRulesFromGroupPolicyMerged": true,
    "authorizedApplicationRulesFromGroupPolicyNotMerged": true,
    "globalPortRulesFromGroupPolicyMerged": true,
    "globalPortRulesFromGroupPolicyNotMerged": true,
    "connectionSecurityRulesFromGroupPolicyMerged": true,
    "connectionSecurityRulesFromGroupPolicyNotMerged": true,
    "outboundConnectionsRequired": true,
    "outboundConnectionsBlocked": true,
    "inboundConnectionsRequired": true,
    "inboundConnectionsBlocked": true,
    "securedPacketExemptionAllowed": true,
    "securedPacketExemptionBlocked": true,
    "policyRulesFromGroupPolicyMerged": true,
    "policyRulesFromGroupPolicyNotMerged": true
  },
  "firewallProfilePrivate": {
    "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
    "firewallEnabled": "blocked",
    "stealthModeRequired": true,
    "stealthModeBlocked": true,
    "incomingTrafficRequired": true,
    "incomingTrafficBlocked": true,
    "unicastResponsesToMulticastBroadcastsRequired": true,
    "unicastResponsesToMulticastBroadcastsBlocked": true,
    "inboundNotificationsRequired": true,
    "inboundNotificationsBlocked": true,
    "authorizedApplicationRulesFromGroupPolicyMerged": true,
    "authorizedApplicationRulesFromGroupPolicyNotMerged": true,
    "globalPortRulesFromGroupPolicyMerged": true,
    "globalPortRulesFromGroupPolicyNotMerged": true,
    "connectionSecurityRulesFromGroupPolicyMerged": true,
    "connectionSecurityRulesFromGroupPolicyNotMerged": true,
    "outboundConnectionsRequired": true,
    "outboundConnectionsBlocked": true,
    "inboundConnectionsRequired": true,
    "inboundConnectionsBlocked": true,
    "securedPacketExemptionAllowed": true,
    "securedPacketExemptionBlocked": true,
    "policyRulesFromGroupPolicyMerged": true,
    "policyRulesFromGroupPolicyNotMerged": true
  },
  "defenderAttackSurfaceReductionExcludedPaths": [
    "Defender Attack Surface Reduction Excluded Paths value"
  ],
  "defenderOfficeAppsOtherProcessInjectionType": "block",
  "defenderOfficeAppsOtherProcessInjection": "enable",
  "defenderOfficeAppsExecutableContentCreationOrLaunchType": "block",
  "defenderOfficeAppsExecutableContentCreationOrLaunch": "enable",
  "defenderOfficeAppsLaunchChildProcessType": "block",
  "defenderOfficeAppsLaunchChildProcess": "enable",
  "defenderOfficeMacroCodeAllowWin32ImportsType": "block",
  "defenderOfficeMacroCodeAllowWin32Imports": "enable",
  "defenderScriptObfuscatedMacroCodeType": "block",
  "defenderScriptObfuscatedMacroCode": "enable",
  "defenderScriptDownloadedPayloadExecutionType": "block",
  "defenderScriptDownloadedPayloadExecution": "enable",
  "defenderPreventCredentialStealingType": "enable",
  "defenderProcessCreationType": "block",
  "defenderProcessCreation": "enable",
  "defenderUntrustedUSBProcessType": "block",
  "defenderUntrustedUSBProcess": "enable",
  "defenderUntrustedExecutableType": "block",
  "defenderUntrustedExecutable": "enable",
  "defenderEmailContentExecutionType": "block",
  "defenderEmailContentExecution": "enable",
  "defenderAdvancedRansomewareProtectionType": "enable",
  "defenderGuardMyFoldersType": "enable",
  "defenderGuardedFoldersAllowedAppPaths": [
    "Defender Guarded Folders Allowed App Paths value"
  ],
  "defenderAdditionalGuardedFolders": [
    "Defender Additional Guarded Folders value"
  ],
  "defenderNetworkProtectionType": "enable",
  "defenderExploitProtectionXml": "ZGVmZW5kZXJFeHBsb2l0UHJvdGVjdGlvblhtbA==",
  "defenderExploitProtectionXmlFileName": "Defender Exploit Protection Xml File Name value",
  "defenderSecurityCenterBlockExploitProtectionOverride": true,
  "appLockerApplicationControl": "enforceComponentsAndStoreApps",
  "deviceGuardLocalSystemAuthorityCredentialGuardSettings": "enableWithUEFILock",
  "deviceGuardEnableVirtualizationBasedSecurity": true,
  "deviceGuardEnableSecureBootWithDMA": true,
  "smartScreenEnableInShell": true,
  "smartScreenBlockOverrideForFiles": true,
  "applicationGuardEnabled": true,
  "applicationGuardEnabledOptions": "enabledForEdge",
  "applicationGuardBlockFileTransfer": "blockImageAndTextFile",
  "applicationGuardBlockNonEnterpriseContent": true,
  "applicationGuardAllowPersistence": true,
  "applicationGuardForceAuditing": true,
  "applicationGuardBlockClipboardSharing": "blockBoth",
  "applicationGuardAllowPrintToPDF": true,
  "applicationGuardAllowPrintToXPS": true,
  "applicationGuardAllowPrintToLocalPrinters": true,
  "applicationGuardAllowPrintToNetworkPrinters": true,
  "applicationGuardAllowVirtualGPU": true,
  "applicationGuardAllowFileSaveOnHost": true,
  "bitLockerDisableWarningForOtherDiskEncryption": true,
  "bitLockerEnableStorageCardEncryptionOnMobile": true,
  "bitLockerEncryptDevice": true,
  "bitLockerSystemDrivePolicy": {
    "@odata.type": "microsoft.graph.bitLockerSystemDrivePolicy",
    "encryptionMethod": "aesCbc256",
    "startupAuthenticationRequired": true,
    "startupAuthenticationBlockWithoutTpmChip": true,
    "startupAuthenticationTpmUsage": "required",
    "startupAuthenticationTpmPinUsage": "required",
    "startupAuthenticationTpmKeyUsage": "required",
    "startupAuthenticationTpmPinAndKeyUsage": "required",
    "minimumPinLength": 0,
    "recoveryOptions": {
      "@odata.type": "microsoft.graph.bitLockerRecoveryOptions",
      "blockDataRecoveryAgent": true,
      "recoveryPasswordUsage": "required",
      "recoveryKeyUsage": "required",
      "hideRecoveryOptions": true,
      "enableRecoveryInformationSaveToStore": true,
      "recoveryInformationToStore": "passwordOnly",
      "enableBitLockerAfterRecoveryInformationToStore": true
    },
    "prebootRecoveryEnableMessageAndUrl": true,
    "prebootRecoveryMessage": "Preboot Recovery Message value",
    "prebootRecoveryUrl": "https://example.com/prebootRecoveryUrl/"
  },
  "bitLockerFixedDrivePolicy": {
    "@odata.type": "microsoft.graph.bitLockerFixedDrivePolicy",
    "encryptionMethod": "aesCbc256",
    "requireEncryptionForWriteAccess": true,
    "recoveryOptions": {
      "@odata.type": "microsoft.graph.bitLockerRecoveryOptions",
      "blockDataRecoveryAgent": true,
      "recoveryPasswordUsage": "required",
      "recoveryKeyUsage": "required",
      "hideRecoveryOptions": true,
      "enableRecoveryInformationSaveToStore": true,
      "recoveryInformationToStore": "passwordOnly",
      "enableBitLockerAfterRecoveryInformationToStore": true
    }
  },
  "bitLockerRemovableDrivePolicy": {
    "@odata.type": "microsoft.graph.bitLockerRemovableDrivePolicy",
    "encryptionMethod": "aesCbc256",
    "requireEncryptionForWriteAccess": true,
    "blockCrossOrganizationWriteAccess": true
  }
}
```






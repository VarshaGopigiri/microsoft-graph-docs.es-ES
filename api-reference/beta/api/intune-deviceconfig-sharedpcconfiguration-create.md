---
title: Crear sharedPCConfiguration
description: Crear un objeto sharedPCConfiguration.
ms.openlocfilehash: 2cd92e4e2d3147cccbd9099d16ecfaaac0c8c656
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084226"
---
# <a name="create-sharedpcconfiguration"></a><span data-ttu-id="4c0b7-103">Crear sharedPCConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c0b7-103">Create sharedPCConfiguration</span></span>

> <span data-ttu-id="4c0b7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4c0b7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4c0b7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4c0b7-107">Crear un objeto [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="4c0b7-107">Create a new [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4c0b7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4c0b7-108">Prerequisites</span></span>
<span data-ttu-id="4c0b7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4c0b7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4c0b7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4c0b7-111">Permission type</span></span>|<span data-ttu-id="4c0b7-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4c0b7-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4c0b7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4c0b7-113">Delegated (work or school account)</span></span>|<span data-ttu-id="4c0b7-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4c0b7-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="4c0b7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4c0b7-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4c0b7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-116">Not supported.</span></span>|
|<span data-ttu-id="4c0b7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4c0b7-117">Application</span></span>|<span data-ttu-id="4c0b7-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4c0b7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4c0b7-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="4c0b7-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4c0b7-120">Request headers</span></span>
|<span data-ttu-id="4c0b7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c0b7-121">Header</span></span>|<span data-ttu-id="4c0b7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4c0b7-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4c0b7-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="4c0b7-123">Authorization</span></span>|<span data-ttu-id="4c0b7-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4c0b7-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4c0b7-125">Accept</span></span>|<span data-ttu-id="4c0b7-126">application/json</span><span class="sxs-lookup"><span data-stu-id="4c0b7-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4c0b7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4c0b7-127">Request body</span></span>
<span data-ttu-id="4c0b7-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto sharedPCConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-128">In the request body, supply a JSON representation for the sharedPCConfiguration object.</span></span>

<span data-ttu-id="4c0b7-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto sharedPCConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-129">The following table shows the properties that are required when you create the sharedPCConfiguration.</span></span>

|<span data-ttu-id="4c0b7-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4c0b7-130">Property</span></span>|<span data-ttu-id="4c0b7-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c0b7-131">Type</span></span>|<span data-ttu-id="4c0b7-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c0b7-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4c0b7-133">id</span><span class="sxs-lookup"><span data-stu-id="4c0b7-133">id</span></span>|<span data-ttu-id="4c0b7-134">String</span><span class="sxs-lookup"><span data-stu-id="4c0b7-134">String</span></span>|<span data-ttu-id="4c0b7-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-135">Key of the entity.</span></span> <span data-ttu-id="4c0b7-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4c0b7-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4c0b7-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="4c0b7-137">lastModifiedDateTime</span></span>|<span data-ttu-id="4c0b7-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4c0b7-138">DateTimeOffset</span></span>|<span data-ttu-id="4c0b7-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-139">DateTime the object was last modified.</span></span> <span data-ttu-id="4c0b7-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4c0b7-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4c0b7-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="4c0b7-141">roleScopeTagIds</span></span>|<span data-ttu-id="4c0b7-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="4c0b7-142">String collection</span></span>|<span data-ttu-id="4c0b7-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="4c0b7-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4c0b7-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4c0b7-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="4c0b7-145">supportsScopeTags</span></span>|<span data-ttu-id="4c0b7-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="4c0b7-146">Boolean</span></span>|<span data-ttu-id="4c0b7-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="4c0b7-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="4c0b7-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="4c0b7-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-150">This property is read-only.</span></span> <span data-ttu-id="4c0b7-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4c0b7-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4c0b7-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="4c0b7-152">createdDateTime</span></span>|<span data-ttu-id="4c0b7-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4c0b7-153">DateTimeOffset</span></span>|<span data-ttu-id="4c0b7-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-154">DateTime the object was created.</span></span> <span data-ttu-id="4c0b7-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4c0b7-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4c0b7-156">descripción</span><span class="sxs-lookup"><span data-stu-id="4c0b7-156">description</span></span>|<span data-ttu-id="4c0b7-157">String</span><span class="sxs-lookup"><span data-stu-id="4c0b7-157">String</span></span>|<span data-ttu-id="4c0b7-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="4c0b7-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4c0b7-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4c0b7-160">displayName</span><span class="sxs-lookup"><span data-stu-id="4c0b7-160">displayName</span></span>|<span data-ttu-id="4c0b7-161">String</span><span class="sxs-lookup"><span data-stu-id="4c0b7-161">String</span></span>|<span data-ttu-id="4c0b7-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="4c0b7-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4c0b7-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4c0b7-164">version</span><span class="sxs-lookup"><span data-stu-id="4c0b7-164">version</span></span>|<span data-ttu-id="4c0b7-165">Int32</span><span class="sxs-lookup"><span data-stu-id="4c0b7-165">Int32</span></span>|<span data-ttu-id="4c0b7-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-166">Version of the device configuration.</span></span> <span data-ttu-id="4c0b7-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4c0b7-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4c0b7-168">accountManagerPolicy</span><span class="sxs-lookup"><span data-stu-id="4c0b7-168">accountManagerPolicy</span></span>|[<span data-ttu-id="4c0b7-169">sharedPCAccountManagerPolicy</span><span class="sxs-lookup"><span data-stu-id="4c0b7-169">sharedPCAccountManagerPolicy</span></span>](../resources/intune-deviceconfig-sharedpcaccountmanagerpolicy.md)|<span data-ttu-id="4c0b7-170">Especifica cómo se administran las cuentas en un equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-170">Specifies how accounts are managed on a shared PC.</span></span> <span data-ttu-id="4c0b7-171">Solo se aplica cuando disableAccountManager es False.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-171">Only applies when disableAccountManager is false.</span></span>|
|<span data-ttu-id="4c0b7-172">allowedAccounts</span><span class="sxs-lookup"><span data-stu-id="4c0b7-172">allowedAccounts</span></span>|[<span data-ttu-id="4c0b7-173">sharedPCAllowedAccountType</span><span class="sxs-lookup"><span data-stu-id="4c0b7-173">sharedPCAllowedAccountType</span></span>](../resources/intune-deviceconfig-sharedpcallowedaccounttype.md)|<span data-ttu-id="4c0b7-174">Indica el tipo de cuentas que se pueden usar en un equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-174">Indicates which type of accounts are allowed to use on a shared PC.</span></span> <span data-ttu-id="4c0b7-175">Los valores posibles son: `guest` y `domain`.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-175">Possible values are: `guest`, `domain`.</span></span>|
|<span data-ttu-id="4c0b7-176">localStorage</span><span class="sxs-lookup"><span data-stu-id="4c0b7-176">localStorage</span></span>|[<span data-ttu-id="4c0b7-177">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="4c0b7-177">enablement</span></span>](../resources/intune-shared-enablement.md)|<span data-ttu-id="4c0b7-178">Especifica si se permite el almacenamiento local en un equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-178">Specifies whether local storage is allowed on a shared PC.</span></span> <span data-ttu-id="4c0b7-179">Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-179">Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|
|<span data-ttu-id="4c0b7-180">allowLocalStorage</span><span class="sxs-lookup"><span data-stu-id="4c0b7-180">allowLocalStorage</span></span>|<span data-ttu-id="4c0b7-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="4c0b7-181">Boolean</span></span>|<span data-ttu-id="4c0b7-182">Especifica si se permite el almacenamiento local en un equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-182">Specifies whether local storage is allowed on a shared PC.</span></span>|
|<span data-ttu-id="4c0b7-183">setAccountManager</span><span class="sxs-lookup"><span data-stu-id="4c0b7-183">setAccountManager</span></span>|[<span data-ttu-id="4c0b7-184">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="4c0b7-184">enablement</span></span>](../resources/intune-shared-enablement.md)|<span data-ttu-id="4c0b7-185">Deshabilita al administrador de cuentas para el modo de equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-185">Disables the account manager for shared PC mode.</span></span> <span data-ttu-id="4c0b7-186">Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-186">Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|
|<span data-ttu-id="4c0b7-187">disableAccountManager</span><span class="sxs-lookup"><span data-stu-id="4c0b7-187">disableAccountManager</span></span>|<span data-ttu-id="4c0b7-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="4c0b7-188">Boolean</span></span>|<span data-ttu-id="4c0b7-189">Deshabilita al administrador de cuentas para el modo de equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-189">Disables the account manager for shared PC mode.</span></span>|
|<span data-ttu-id="4c0b7-190">setEduPolicies</span><span class="sxs-lookup"><span data-stu-id="4c0b7-190">setEduPolicies</span></span>|[<span data-ttu-id="4c0b7-191">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="4c0b7-191">enablement</span></span>](../resources/intune-shared-enablement.md)|<span data-ttu-id="4c0b7-192">Especifica si las directivas de entorno compartido predeterminado el ámbito educativo de PC deben ser habilitado o deshabilitado o no configuradas.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-192">Specifies whether the default shared PC education environment policies should be enabled/disabled/not configured.</span></span> <span data-ttu-id="4c0b7-193">Para Windows 10 RS2 y versiones posteriores, se aplicará esta directiva sin establecer Habilitado en true.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-193">For Windows 10 RS2 and later, this policy will be applied without setting Enabled to true.</span></span> <span data-ttu-id="4c0b7-194">Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-194">Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|
|<span data-ttu-id="4c0b7-195">disableEduPolicies</span><span class="sxs-lookup"><span data-stu-id="4c0b7-195">disableEduPolicies</span></span>|<span data-ttu-id="4c0b7-196">Booleano</span><span class="sxs-lookup"><span data-stu-id="4c0b7-196">Boolean</span></span>|<span data-ttu-id="4c0b7-197">Especifica si se deben deshabilitar las directivas predeterminadas de entorno educativo de equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-197">Specifies whether the default shared PC education environment policies should be disabled.</span></span> <span data-ttu-id="4c0b7-198">Para Windows 10 RS2 y versiones posteriores, se aplicará esta directiva sin establecer Habilitado en true.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-198">For Windows 10 RS2 and later, this policy will be applied without setting Enabled to true.</span></span>|
|<span data-ttu-id="4c0b7-199">setPowerPolicies</span><span class="sxs-lookup"><span data-stu-id="4c0b7-199">setPowerPolicies</span></span>|[<span data-ttu-id="4c0b7-200">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="4c0b7-200">enablement</span></span>](../resources/intune-shared-enablement.md)|<span data-ttu-id="4c0b7-201">Especifica si las directivas de power PC compartido predeterminado deben estar habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-201">Specifies whether the default shared PC power policies should be enabled/disabled.</span></span> <span data-ttu-id="4c0b7-202">Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-202">Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|
|<span data-ttu-id="4c0b7-203">disablePowerPolicies</span><span class="sxs-lookup"><span data-stu-id="4c0b7-203">disablePowerPolicies</span></span>|<span data-ttu-id="4c0b7-204">Booleano</span><span class="sxs-lookup"><span data-stu-id="4c0b7-204">Boolean</span></span>|<span data-ttu-id="4c0b7-205">Especifica si se deben deshabilitar las directivas predeterminadas de energía de equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-205">Specifies whether the default shared PC power policies should be disabled.</span></span>|
|<span data-ttu-id="4c0b7-206">signInOnResume</span><span class="sxs-lookup"><span data-stu-id="4c0b7-206">signInOnResume</span></span>|[<span data-ttu-id="4c0b7-207">Habilitación de</span><span class="sxs-lookup"><span data-stu-id="4c0b7-207">enablement</span></span>](../resources/intune-shared-enablement.md)|<span data-ttu-id="4c0b7-208">Especifica el requisito para iniciar sesión en cada vez que el dispositivo se reactiva copia de seguridad del modo de suspensión.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-208">Specifies the requirement to sign in whenever the device wakes up from sleep mode.</span></span> <span data-ttu-id="4c0b7-209">Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-209">Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|
|<span data-ttu-id="4c0b7-210">disableSignInOnResume</span><span class="sxs-lookup"><span data-stu-id="4c0b7-210">disableSignInOnResume</span></span>|<span data-ttu-id="4c0b7-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="4c0b7-211">Boolean</span></span>|<span data-ttu-id="4c0b7-212">Deshabilita el requisito de iniciar sesión siempre que el dispositivo salga del modo de suspensión.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-212">Disables the requirement to sign in whenever the device wakes up from sleep mode.</span></span>|
|<span data-ttu-id="4c0b7-213">enabled</span><span class="sxs-lookup"><span data-stu-id="4c0b7-213">enabled</span></span>|<span data-ttu-id="4c0b7-214">Booleano</span><span class="sxs-lookup"><span data-stu-id="4c0b7-214">Boolean</span></span>|<span data-ttu-id="4c0b7-215">Habilita el modo de equipo compartido y se aplica a las directivas de equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-215">Enables shared PC mode and applies the shared pc policies.</span></span>|
|<span data-ttu-id="4c0b7-216">idleTimeBeforeSleepInSeconds</span><span class="sxs-lookup"><span data-stu-id="4c0b7-216">idleTimeBeforeSleepInSeconds</span></span>|<span data-ttu-id="4c0b7-217">Int32</span><span class="sxs-lookup"><span data-stu-id="4c0b7-217">Int32</span></span>|<span data-ttu-id="4c0b7-218">Especifica el tiempo en segundos que un dispositivo debe permanecer inactivo antes de que el equipo pase al estado de suspensión.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-218">Specifies the time in seconds that a device must sit idle before the PC goes to sleep.</span></span> <span data-ttu-id="4c0b7-219">Si este valor se establece en 0 impide que se produzca el tiempo de espera en suspensión.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-219">Setting this value to 0 prevents the sleep timeout from occurring.</span></span>|
|<span data-ttu-id="4c0b7-220">kioskAppDisplayName</span><span class="sxs-lookup"><span data-stu-id="4c0b7-220">kioskAppDisplayName</span></span>|<span data-ttu-id="4c0b7-221">String</span><span class="sxs-lookup"><span data-stu-id="4c0b7-221">String</span></span>|<span data-ttu-id="4c0b7-222">Especifica el texto para mostrar de la cuenta que se muestra en la pantalla de inicio de sesión que inicia la aplicación especificada por SetKioskAppUserModelId.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-222">Specifies the display text for the account shown on the sign-in screen which launches the app specified by SetKioskAppUserModelId.</span></span> <span data-ttu-id="4c0b7-223">Solo se aplica cuando se establece KioskAppUserModelId.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-223">Only applies when KioskAppUserModelId is set.</span></span>|
|<span data-ttu-id="4c0b7-224">kioskAppUserModelId</span><span class="sxs-lookup"><span data-stu-id="4c0b7-224">kioskAppUserModelId</span></span>|<span data-ttu-id="4c0b7-225">String</span><span class="sxs-lookup"><span data-stu-id="4c0b7-225">String</span></span>|<span data-ttu-id="4c0b7-226">Especifica el identificador del modelo de usuario de la aplicación correspondiente a la aplicación para que se use con el acceso asignado.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-226">Specifies the application user model ID of the app to use with assigned access.</span></span>|
|<span data-ttu-id="4c0b7-227">maintenanceStartTime</span><span class="sxs-lookup"><span data-stu-id="4c0b7-227">maintenanceStartTime</span></span>|<span data-ttu-id="4c0b7-228">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="4c0b7-228">TimeOfDay</span></span>|<span data-ttu-id="4c0b7-229">Especifica la hora de inicio diaria de la hora de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-229">Specifies the daily start time of maintenance hour.</span></span>|



## <a name="response"></a><span data-ttu-id="4c0b7-230">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4c0b7-230">Response</span></span>
<span data-ttu-id="4c0b7-231">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-231">If successful, this method returns a `201 Created` response code and a [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4c0b7-232">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4c0b7-232">Example</span></span>
### <a name="request"></a><span data-ttu-id="4c0b7-233">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4c0b7-233">Request</span></span>
<span data-ttu-id="4c0b7-234">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-234">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1179

{
  "@odata.type": "#microsoft.graph.sharedPCConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountManagerPolicy": {
    "@odata.type": "microsoft.graph.sharedPCAccountManagerPolicy",
    "accountDeletionPolicy": "diskSpaceThreshold",
    "cacheAccountsAboveDiskFreePercentage": 4,
    "inactiveThresholdDays": 5,
    "removeAccountsBelowDiskFreePercentage": 5
  },
  "allowedAccounts": "domain",
  "localStorage": "enabled",
  "allowLocalStorage": true,
  "setAccountManager": "enabled",
  "disableAccountManager": true,
  "setEduPolicies": "enabled",
  "disableEduPolicies": true,
  "setPowerPolicies": "enabled",
  "disablePowerPolicies": true,
  "signInOnResume": "enabled",
  "disableSignInOnResume": true,
  "enabled": true,
  "idleTimeBeforeSleepInSeconds": 12,
  "kioskAppDisplayName": "Kiosk App Display Name value",
  "kioskAppUserModelId": "Kiosk App User Model Id value",
  "maintenanceStartTime": "11:59:24.7240000"
}
```

### <a name="response"></a><span data-ttu-id="4c0b7-235">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4c0b7-235">Response</span></span>
<span data-ttu-id="4c0b7-p121">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4c0b7-p121">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1287

{
  "@odata.type": "#microsoft.graph.sharedPCConfiguration",
  "id": "5206be3b-be3b-5206-3bbe-06523bbe0652",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountManagerPolicy": {
    "@odata.type": "microsoft.graph.sharedPCAccountManagerPolicy",
    "accountDeletionPolicy": "diskSpaceThreshold",
    "cacheAccountsAboveDiskFreePercentage": 4,
    "inactiveThresholdDays": 5,
    "removeAccountsBelowDiskFreePercentage": 5
  },
  "allowedAccounts": "domain",
  "localStorage": "enabled",
  "allowLocalStorage": true,
  "setAccountManager": "enabled",
  "disableAccountManager": true,
  "setEduPolicies": "enabled",
  "disableEduPolicies": true,
  "setPowerPolicies": "enabled",
  "disablePowerPolicies": true,
  "signInOnResume": "enabled",
  "disableSignInOnResume": true,
  "enabled": true,
  "idleTimeBeforeSleepInSeconds": 12,
  "kioskAppDisplayName": "Kiosk App Display Name value",
  "kioskAppUserModelId": "Kiosk App User Model Id value",
  "maintenanceStartTime": "11:59:24.7240000"
}
```






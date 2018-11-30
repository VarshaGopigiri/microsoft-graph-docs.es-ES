---
title: Crear windowsIdentityProtectionConfiguration
description: Crear un nuevo objeto windowsIdentityProtectionConfiguration.
ms.openlocfilehash: 30700a08517e5762068078de46369e892218c8f0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087191"
---
# <a name="create-windowsidentityprotectionconfiguration"></a><span data-ttu-id="619ef-103">Crear windowsIdentityProtectionConfiguration</span><span class="sxs-lookup"><span data-stu-id="619ef-103">Create windowsIdentityProtectionConfiguration</span></span>

> <span data-ttu-id="619ef-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="619ef-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="619ef-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="619ef-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="619ef-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="619ef-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="619ef-107">Crear un nuevo objeto [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="619ef-107">Create a new [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="619ef-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="619ef-108">Prerequisites</span></span>
<span data-ttu-id="619ef-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="619ef-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="619ef-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="619ef-111">Permission type</span></span>|<span data-ttu-id="619ef-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="619ef-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="619ef-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="619ef-113">Delegated (work or school account)</span></span>|<span data-ttu-id="619ef-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="619ef-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="619ef-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="619ef-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="619ef-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="619ef-116">Not supported.</span></span>|
|<span data-ttu-id="619ef-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="619ef-117">Application</span></span>|<span data-ttu-id="619ef-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="619ef-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="619ef-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="619ef-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="619ef-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="619ef-120">Request headers</span></span>
|<span data-ttu-id="619ef-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="619ef-121">Header</span></span>|<span data-ttu-id="619ef-122">Valor</span><span class="sxs-lookup"><span data-stu-id="619ef-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="619ef-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="619ef-123">Authorization</span></span>|<span data-ttu-id="619ef-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="619ef-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="619ef-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="619ef-125">Accept</span></span>|<span data-ttu-id="619ef-126">application/json</span><span class="sxs-lookup"><span data-stu-id="619ef-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="619ef-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="619ef-127">Request body</span></span>
<span data-ttu-id="619ef-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windowsIdentityProtectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="619ef-128">In the request body, supply a JSON representation for the windowsIdentityProtectionConfiguration object.</span></span>

<span data-ttu-id="619ef-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windowsIdentityProtectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="619ef-129">The following table shows the properties that are required when you create the windowsIdentityProtectionConfiguration.</span></span>

|<span data-ttu-id="619ef-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="619ef-130">Property</span></span>|<span data-ttu-id="619ef-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="619ef-131">Type</span></span>|<span data-ttu-id="619ef-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="619ef-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="619ef-133">id</span><span class="sxs-lookup"><span data-stu-id="619ef-133">id</span></span>|<span data-ttu-id="619ef-134">String</span><span class="sxs-lookup"><span data-stu-id="619ef-134">String</span></span>|<span data-ttu-id="619ef-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="619ef-135">Key of the entity.</span></span> <span data-ttu-id="619ef-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="619ef-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="619ef-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="619ef-137">lastModifiedDateTime</span></span>|<span data-ttu-id="619ef-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="619ef-138">DateTimeOffset</span></span>|<span data-ttu-id="619ef-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="619ef-139">DateTime the object was last modified.</span></span> <span data-ttu-id="619ef-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="619ef-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="619ef-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="619ef-141">roleScopeTagIds</span></span>|<span data-ttu-id="619ef-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="619ef-142">String collection</span></span>|<span data-ttu-id="619ef-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="619ef-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="619ef-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="619ef-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="619ef-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="619ef-145">supportsScopeTags</span></span>|<span data-ttu-id="619ef-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="619ef-146">Boolean</span></span>|<span data-ttu-id="619ef-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="619ef-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="619ef-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="619ef-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="619ef-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="619ef-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="619ef-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="619ef-150">This property is read-only.</span></span> <span data-ttu-id="619ef-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="619ef-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="619ef-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="619ef-152">createdDateTime</span></span>|<span data-ttu-id="619ef-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="619ef-153">DateTimeOffset</span></span>|<span data-ttu-id="619ef-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="619ef-154">DateTime the object was created.</span></span> <span data-ttu-id="619ef-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="619ef-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="619ef-156">descripción</span><span class="sxs-lookup"><span data-stu-id="619ef-156">description</span></span>|<span data-ttu-id="619ef-157">String</span><span class="sxs-lookup"><span data-stu-id="619ef-157">String</span></span>|<span data-ttu-id="619ef-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="619ef-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="619ef-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="619ef-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="619ef-160">displayName</span><span class="sxs-lookup"><span data-stu-id="619ef-160">displayName</span></span>|<span data-ttu-id="619ef-161">String</span><span class="sxs-lookup"><span data-stu-id="619ef-161">String</span></span>|<span data-ttu-id="619ef-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="619ef-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="619ef-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="619ef-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="619ef-164">version</span><span class="sxs-lookup"><span data-stu-id="619ef-164">version</span></span>|<span data-ttu-id="619ef-165">Int32</span><span class="sxs-lookup"><span data-stu-id="619ef-165">Int32</span></span>|<span data-ttu-id="619ef-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="619ef-166">Version of the device configuration.</span></span> <span data-ttu-id="619ef-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="619ef-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="619ef-168">enhancedAntiSpoofingForFacialFeaturesEnabled</span><span class="sxs-lookup"><span data-stu-id="619ef-168">enhancedAntiSpoofingForFacialFeaturesEnabled</span></span>|<span data-ttu-id="619ef-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="619ef-169">Boolean</span></span>|<span data-ttu-id="619ef-170">Valor booleano que se usa para permitir mejorada contra la suplantación de reconocimiento de característica faciales acerca de la autenticación de Windows Hola cara.</span><span class="sxs-lookup"><span data-stu-id="619ef-170">Boolean value used to enable enhanced anti-spoofing for facial feature recognition on Windows Hello face authentication.</span></span>|
|<span data-ttu-id="619ef-171">pinMinimumLength</span><span class="sxs-lookup"><span data-stu-id="619ef-171">pinMinimumLength</span></span>|<span data-ttu-id="619ef-172">Int32</span><span class="sxs-lookup"><span data-stu-id="619ef-172">Int32</span></span>|<span data-ttu-id="619ef-173">Valor entero que establece el número mínimo de caracteres necesarios para el Windows Hello de PIN de negocio.</span><span class="sxs-lookup"><span data-stu-id="619ef-173">Integer value that sets the minimum number of characters required for the Windows Hello for Business PIN.</span></span> <span data-ttu-id="619ef-174">Los valores válidos son de 4 a 127 inclusive y menor o igual que el valor establecido para el PIN máximo.</span><span class="sxs-lookup"><span data-stu-id="619ef-174">Valid values are 4 to 127 inclusive and less than or equal to the value set for the maximum PIN.</span></span> <span data-ttu-id="619ef-175">Valores válidos 4 a 127</span><span class="sxs-lookup"><span data-stu-id="619ef-175">Valid values 4 to 127</span></span>|
|<span data-ttu-id="619ef-176">pinMaximumLength</span><span class="sxs-lookup"><span data-stu-id="619ef-176">pinMaximumLength</span></span>|<span data-ttu-id="619ef-177">Int32</span><span class="sxs-lookup"><span data-stu-id="619ef-177">Int32</span></span>|<span data-ttu-id="619ef-178">Valor entero que establece el número máximo de caracteres permitidos para el trabajo PIN.</span><span class="sxs-lookup"><span data-stu-id="619ef-178">Integer value that sets the maximum number of characters allowed for the work PIN.</span></span> <span data-ttu-id="619ef-179">Los valores válidos son de 4 a 127 inclusive y mayor o igual que el valor establecido para el PIN mínimo.</span><span class="sxs-lookup"><span data-stu-id="619ef-179">Valid values are 4 to 127 inclusive and greater than or equal to the value set for the minimum PIN.</span></span> <span data-ttu-id="619ef-180">Valores válidos 4 a 127</span><span class="sxs-lookup"><span data-stu-id="619ef-180">Valid values 4 to 127</span></span>|
|<span data-ttu-id="619ef-181">pinUppercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="619ef-181">pinUppercaseCharactersUsage</span></span>|[<span data-ttu-id="619ef-182">configurationUsage</span><span class="sxs-lookup"><span data-stu-id="619ef-182">configurationUsage</span></span>](../resources/intune-deviceconfig-configurationusage.md)|<span data-ttu-id="619ef-183">Este valor configura el uso de caracteres en mayúsculas en el Windows Hello para profesionales PIN.</span><span class="sxs-lookup"><span data-stu-id="619ef-183">This value configures the use of uppercase characters in the Windows Hello for Business PIN.</span></span> <span data-ttu-id="619ef-184">Los valores posibles son: `blocked`, `required` y `allowed`.</span><span class="sxs-lookup"><span data-stu-id="619ef-184">Possible values are: `blocked`, `required`, `allowed`.</span></span>|
|<span data-ttu-id="619ef-185">pinLowercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="619ef-185">pinLowercaseCharactersUsage</span></span>|[<span data-ttu-id="619ef-186">configurationUsage</span><span class="sxs-lookup"><span data-stu-id="619ef-186">configurationUsage</span></span>](../resources/intune-deviceconfig-configurationusage.md)|<span data-ttu-id="619ef-187">Este valor configura el uso de caracteres en minúsculas en el Windows Hello para profesionales PIN.</span><span class="sxs-lookup"><span data-stu-id="619ef-187">This value configures the use of lowercase characters in the Windows Hello for Business PIN.</span></span> <span data-ttu-id="619ef-188">Los valores posibles son: `blocked`, `required` y `allowed`.</span><span class="sxs-lookup"><span data-stu-id="619ef-188">Possible values are: `blocked`, `required`, `allowed`.</span></span>|
|<span data-ttu-id="619ef-189">pinSpecialCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="619ef-189">pinSpecialCharactersUsage</span></span>|[<span data-ttu-id="619ef-190">configurationUsage</span><span class="sxs-lookup"><span data-stu-id="619ef-190">configurationUsage</span></span>](../resources/intune-deviceconfig-configurationusage.md)|<span data-ttu-id="619ef-191">Controla la capacidad de usar caracteres especiales en el Windows Hello para profesionales PIN.</span><span class="sxs-lookup"><span data-stu-id="619ef-191">Controls the ability to use special characters in the Windows Hello for Business PIN.</span></span> <span data-ttu-id="619ef-192">Los valores posibles son: `blocked`, `required` y `allowed`.</span><span class="sxs-lookup"><span data-stu-id="619ef-192">Possible values are: `blocked`, `required`, `allowed`.</span></span>|
|<span data-ttu-id="619ef-193">pinExpirationInDays</span><span class="sxs-lookup"><span data-stu-id="619ef-193">pinExpirationInDays</span></span>|<span data-ttu-id="619ef-194">Int32</span><span class="sxs-lookup"><span data-stu-id="619ef-194">Int32</span></span>|<span data-ttu-id="619ef-195">Valor entero especifica el período (en días) que se puede usar un NIP antes de que el sistema requiere que el usuario que la cambie.</span><span class="sxs-lookup"><span data-stu-id="619ef-195">Integer value specifies the period (in days) that a PIN can be used before the system requires the user to change it.</span></span> <span data-ttu-id="619ef-196">Los valores válidos son 0 a 730 inclusive.</span><span class="sxs-lookup"><span data-stu-id="619ef-196">Valid values are 0 to 730 inclusive.</span></span> <span data-ttu-id="619ef-197">Valores válidos de 0 a 730.</span><span class="sxs-lookup"><span data-stu-id="619ef-197">Valid values 0 to 730</span></span>|
|<span data-ttu-id="619ef-198">pinPreviousBlockCount</span><span class="sxs-lookup"><span data-stu-id="619ef-198">pinPreviousBlockCount</span></span>|<span data-ttu-id="619ef-199">Int32</span><span class="sxs-lookup"><span data-stu-id="619ef-199">Int32</span></span>|<span data-ttu-id="619ef-200">Controla la capacidad para impedir que los usuarios utilicen más allá de los PIN.</span><span class="sxs-lookup"><span data-stu-id="619ef-200">Controls the ability to prevent users from using past PINs.</span></span> <span data-ttu-id="619ef-201">Esto se debe establecer entre 0 y 50, ambos inclusive, y el PIN del usuario actual se incluye en ese número.</span><span class="sxs-lookup"><span data-stu-id="619ef-201">This must be set between 0 and 50, inclusive, and the current PIN of the user is included in that count.</span></span> <span data-ttu-id="619ef-202">Si se establece en 0, anterior no se almacenan los PIN.</span><span class="sxs-lookup"><span data-stu-id="619ef-202">If set to 0, previous PINs are not stored.</span></span> <span data-ttu-id="619ef-203">No se conserva el historial de PIN a través de un PIN restablecer.</span><span class="sxs-lookup"><span data-stu-id="619ef-203">PIN history is not preserved through a PIN reset.</span></span> <span data-ttu-id="619ef-204">Valores válidos de 0 a 50.</span><span class="sxs-lookup"><span data-stu-id="619ef-204">Valid values 0 to 50</span></span>|
|<span data-ttu-id="619ef-205">pinRecoveryEnabled</span><span class="sxs-lookup"><span data-stu-id="619ef-205">pinRecoveryEnabled</span></span>|<span data-ttu-id="619ef-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="619ef-206">Boolean</span></span>|<span data-ttu-id="619ef-207">Valor booleano que permite a un usuario cambiar su PIN mediante el Windows Hello para servicio de recuperación de PIN de negocio.</span><span class="sxs-lookup"><span data-stu-id="619ef-207">Boolean value that enables a user to change their PIN by using the Windows Hello for Business PIN recovery service.</span></span>|
|<span data-ttu-id="619ef-208">securityDeviceRequired</span><span class="sxs-lookup"><span data-stu-id="619ef-208">securityDeviceRequired</span></span>|<span data-ttu-id="619ef-209">Booleano</span><span class="sxs-lookup"><span data-stu-id="619ef-209">Boolean</span></span>|<span data-ttu-id="619ef-210">Controla si se debe requerir un módulo de plataforma segura (TPM) para aprovisionamiento Windows Hello para la empresa.</span><span class="sxs-lookup"><span data-stu-id="619ef-210">Controls whether to require a Trusted Platform Module (TPM) for provisioning Windows Hello for Business.</span></span> <span data-ttu-id="619ef-211">Un TPM proporciona una ventaja de seguridad adicional en que los datos almacenados en él no se puede usar en otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="619ef-211">A TPM provides an additional security benefit in that data stored on it cannot be used on other devices.</span></span> <span data-ttu-id="619ef-212">Si se establece en False, todos los dispositivos pueden aprovisionar Windows Hello para la empresa, incluso si no hay un TPM utilizable.</span><span class="sxs-lookup"><span data-stu-id="619ef-212">If set to False, all devices can provision Windows Hello for Business even if there is not a usable TPM.</span></span>|
|<span data-ttu-id="619ef-213">unlockWithBiometricsEnabled</span><span class="sxs-lookup"><span data-stu-id="619ef-213">unlockWithBiometricsEnabled</span></span>|<span data-ttu-id="619ef-214">Booleano</span><span class="sxs-lookup"><span data-stu-id="619ef-214">Boolean</span></span>|<span data-ttu-id="619ef-215">Controla el uso de gestos biométricas, como cara y de huella digital, como una alternativa a la Windows Hola de PIN de negocio.</span><span class="sxs-lookup"><span data-stu-id="619ef-215">Controls the use of biometric gestures, such as face and fingerprint, as an alternative to the Windows Hello for Business PIN.</span></span>  <span data-ttu-id="619ef-216">Si se establece en False, biométricas gestos no se permite.</span><span class="sxs-lookup"><span data-stu-id="619ef-216">If set to False, biometric gestures are not allowed.</span></span> <span data-ttu-id="619ef-217">Los usuarios aún deben configurar un PIN como una copia de seguridad en caso de errores.</span><span class="sxs-lookup"><span data-stu-id="619ef-217">Users must still configure a PIN as a backup in case of failures.</span></span>|
|<span data-ttu-id="619ef-218">useCertificatesForOnPremisesAuthEnabled</span><span class="sxs-lookup"><span data-stu-id="619ef-218">useCertificatesForOnPremisesAuthEnabled</span></span>|<span data-ttu-id="619ef-219">Booleano</span><span class="sxs-lookup"><span data-stu-id="619ef-219">Boolean</span></span>|<span data-ttu-id="619ef-220">Valor booleano que permite Windows Hello para la empresa a usar certificados para autenticar los recursos locales.</span><span class="sxs-lookup"><span data-stu-id="619ef-220">Boolean value that enables Windows Hello for Business to use certificates to authenticate on-premise resources.</span></span>|
|<span data-ttu-id="619ef-221">windowsHelloForBusinessBlocked</span><span class="sxs-lookup"><span data-stu-id="619ef-221">windowsHelloForBusinessBlocked</span></span>|<span data-ttu-id="619ef-222">Booleano</span><span class="sxs-lookup"><span data-stu-id="619ef-222">Boolean</span></span>|<span data-ttu-id="619ef-223">Valor booleano que bloquea Windows Hello para la empresa como un método para iniciar sesión en Windows.</span><span class="sxs-lookup"><span data-stu-id="619ef-223">Boolean value that blocks Windows Hello for Business as a method for signing into Windows.</span></span>|



## <a name="response"></a><span data-ttu-id="619ef-224">Respuesta</span><span class="sxs-lookup"><span data-stu-id="619ef-224">Response</span></span>
<span data-ttu-id="619ef-225">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="619ef-225">If successful, this method returns a `201 Created` response code and a [windowsIdentityProtectionConfiguration](../resources/intune-deviceconfig-windowsidentityprotectionconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="619ef-226">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="619ef-226">Example</span></span>
### <a name="request"></a><span data-ttu-id="619ef-227">Solicitud</span><span class="sxs-lookup"><span data-stu-id="619ef-227">Request</span></span>
<span data-ttu-id="619ef-228">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="619ef-228">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 838

{
  "@odata.type": "#microsoft.graph.windowsIdentityProtectionConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "enhancedAntiSpoofingForFacialFeaturesEnabled": true,
  "pinMinimumLength": 0,
  "pinMaximumLength": 0,
  "pinUppercaseCharactersUsage": "required",
  "pinLowercaseCharactersUsage": "required",
  "pinSpecialCharactersUsage": "required",
  "pinExpirationInDays": 3,
  "pinPreviousBlockCount": 5,
  "pinRecoveryEnabled": true,
  "securityDeviceRequired": true,
  "unlockWithBiometricsEnabled": true,
  "useCertificatesForOnPremisesAuthEnabled": true,
  "windowsHelloForBusinessBlocked": true
}
```

### <a name="response"></a><span data-ttu-id="619ef-229">Respuesta</span><span class="sxs-lookup"><span data-stu-id="619ef-229">Response</span></span>
<span data-ttu-id="619ef-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="619ef-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 946

{
  "@odata.type": "#microsoft.graph.windowsIdentityProtectionConfiguration",
  "id": "b2e64303-4303-b2e6-0343-e6b20343e6b2",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "enhancedAntiSpoofingForFacialFeaturesEnabled": true,
  "pinMinimumLength": 0,
  "pinMaximumLength": 0,
  "pinUppercaseCharactersUsage": "required",
  "pinLowercaseCharactersUsage": "required",
  "pinSpecialCharactersUsage": "required",
  "pinExpirationInDays": 3,
  "pinPreviousBlockCount": 5,
  "pinRecoveryEnabled": true,
  "securityDeviceRequired": true,
  "unlockWithBiometricsEnabled": true,
  "useCertificatesForOnPremisesAuthEnabled": true,
  "windowsHelloForBusinessBlocked": true
}
```





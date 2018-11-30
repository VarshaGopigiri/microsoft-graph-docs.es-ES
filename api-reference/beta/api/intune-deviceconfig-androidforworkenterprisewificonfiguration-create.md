---
title: Crear androidForWorkEnterpriseWiFiConfiguration
description: Crear un nuevo objeto androidForWorkEnterpriseWiFiConfiguration.
ms.openlocfilehash: 5600d70b237cd910060db7ed0f27ae3e0dedad69
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085852"
---
# <a name="create-androidforworkenterprisewificonfiguration"></a><span data-ttu-id="ea02e-103">Crear androidForWorkEnterpriseWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea02e-103">Create androidForWorkEnterpriseWiFiConfiguration</span></span>

> <span data-ttu-id="ea02e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ea02e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ea02e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ea02e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ea02e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ea02e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ea02e-107">Crear un nuevo objeto [androidForWorkEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidforworkenterprisewificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="ea02e-107">Create a new [androidForWorkEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidforworkenterprisewificonfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ea02e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ea02e-108">Prerequisites</span></span>
<span data-ttu-id="ea02e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ea02e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ea02e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea02e-111">Permission type</span></span>|<span data-ttu-id="ea02e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea02e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ea02e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea02e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ea02e-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ea02e-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ea02e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea02e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ea02e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea02e-116">Not supported.</span></span>|
|<span data-ttu-id="ea02e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea02e-117">Application</span></span>|<span data-ttu-id="ea02e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea02e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ea02e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea02e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="ea02e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea02e-120">Request headers</span></span>
|<span data-ttu-id="ea02e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea02e-121">Header</span></span>|<span data-ttu-id="ea02e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ea02e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ea02e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="ea02e-123">Authorization</span></span>|<span data-ttu-id="ea02e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ea02e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ea02e-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ea02e-125">Accept</span></span>|<span data-ttu-id="ea02e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ea02e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ea02e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea02e-127">Request body</span></span>
<span data-ttu-id="ea02e-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidForWorkEnterpriseWiFiConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ea02e-128">In the request body, supply a JSON representation for the androidForWorkEnterpriseWiFiConfiguration object.</span></span>

<span data-ttu-id="ea02e-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidForWorkEnterpriseWiFiConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ea02e-129">The following table shows the properties that are required when you create the androidForWorkEnterpriseWiFiConfiguration.</span></span>

|<span data-ttu-id="ea02e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ea02e-130">Property</span></span>|<span data-ttu-id="ea02e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea02e-131">Type</span></span>|<span data-ttu-id="ea02e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea02e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ea02e-133">id</span><span class="sxs-lookup"><span data-stu-id="ea02e-133">id</span></span>|<span data-ttu-id="ea02e-134">String</span><span class="sxs-lookup"><span data-stu-id="ea02e-134">String</span></span>|<span data-ttu-id="ea02e-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ea02e-135">Key of the entity.</span></span> <span data-ttu-id="ea02e-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea02e-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea02e-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ea02e-137">lastModifiedDateTime</span></span>|<span data-ttu-id="ea02e-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ea02e-138">DateTimeOffset</span></span>|<span data-ttu-id="ea02e-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="ea02e-139">DateTime the object was last modified.</span></span> <span data-ttu-id="ea02e-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea02e-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea02e-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="ea02e-141">roleScopeTagIds</span></span>|<span data-ttu-id="ea02e-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="ea02e-142">String collection</span></span>|<span data-ttu-id="ea02e-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="ea02e-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="ea02e-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea02e-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea02e-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="ea02e-145">supportsScopeTags</span></span>|<span data-ttu-id="ea02e-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea02e-146">Boolean</span></span>|<span data-ttu-id="ea02e-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="ea02e-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="ea02e-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="ea02e-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="ea02e-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="ea02e-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="ea02e-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="ea02e-150">This property is read-only.</span></span> <span data-ttu-id="ea02e-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea02e-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea02e-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ea02e-152">createdDateTime</span></span>|<span data-ttu-id="ea02e-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ea02e-153">DateTimeOffset</span></span>|<span data-ttu-id="ea02e-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="ea02e-154">DateTime the object was created.</span></span> <span data-ttu-id="ea02e-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea02e-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea02e-156">descripción</span><span class="sxs-lookup"><span data-stu-id="ea02e-156">description</span></span>|<span data-ttu-id="ea02e-157">String</span><span class="sxs-lookup"><span data-stu-id="ea02e-157">String</span></span>|<span data-ttu-id="ea02e-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea02e-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="ea02e-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea02e-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea02e-160">displayName</span><span class="sxs-lookup"><span data-stu-id="ea02e-160">displayName</span></span>|<span data-ttu-id="ea02e-161">String</span><span class="sxs-lookup"><span data-stu-id="ea02e-161">String</span></span>|<span data-ttu-id="ea02e-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea02e-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="ea02e-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea02e-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea02e-164">version</span><span class="sxs-lookup"><span data-stu-id="ea02e-164">version</span></span>|<span data-ttu-id="ea02e-165">Int32</span><span class="sxs-lookup"><span data-stu-id="ea02e-165">Int32</span></span>|<span data-ttu-id="ea02e-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea02e-166">Version of the device configuration.</span></span> <span data-ttu-id="ea02e-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea02e-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea02e-168">networkName</span><span class="sxs-lookup"><span data-stu-id="ea02e-168">networkName</span></span>|<span data-ttu-id="ea02e-169">String</span><span class="sxs-lookup"><span data-stu-id="ea02e-169">String</span></span>|<span data-ttu-id="ea02e-170">Nombre de red se hereda de [androidForWorkWiFiConfiguration](../resources/intune-deviceconfig-androidforworkwificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea02e-170">Network Name Inherited from [androidForWorkWiFiConfiguration](../resources/intune-deviceconfig-androidforworkwificonfiguration.md)</span></span>|
|<span data-ttu-id="ea02e-171">SSID</span><span class="sxs-lookup"><span data-stu-id="ea02e-171">ssid</span></span>|<span data-ttu-id="ea02e-172">String</span><span class="sxs-lookup"><span data-stu-id="ea02e-172">String</span></span>|<span data-ttu-id="ea02e-173">Esto es el nombre de la red Wi-Fi que se difunde a todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ea02e-173">This is the name of the Wi-Fi network that is broadcast to all devices.</span></span> <span data-ttu-id="ea02e-174">Se hereda de [androidForWorkWiFiConfiguration](../resources/intune-deviceconfig-androidforworkwificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea02e-174">Inherited from [androidForWorkWiFiConfiguration](../resources/intune-deviceconfig-androidforworkwificonfiguration.md)</span></span>|
|<span data-ttu-id="ea02e-175">connectAutomatically</span><span class="sxs-lookup"><span data-stu-id="ea02e-175">connectAutomatically</span></span>|<span data-ttu-id="ea02e-176">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea02e-176">Boolean</span></span>|<span data-ttu-id="ea02e-177">Conectar automáticamente cuando esta red esté en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="ea02e-177">Connect automatically when this network is in range.</span></span> <span data-ttu-id="ea02e-178">Si se establece en true omitirá el símbolo del sistema del usuario y el dispositivo se conecte automáticamente a la red Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="ea02e-178">Setting this to true will skip the user prompt and automatically connect the device to Wi-Fi network.</span></span> <span data-ttu-id="ea02e-179">Se hereda de [androidForWorkWiFiConfiguration](../resources/intune-deviceconfig-androidforworkwificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea02e-179">Inherited from [androidForWorkWiFiConfiguration](../resources/intune-deviceconfig-androidforworkwificonfiguration.md)</span></span>|
|<span data-ttu-id="ea02e-180">connectWhenNetworkNameIsHidden</span><span class="sxs-lookup"><span data-stu-id="ea02e-180">connectWhenNetworkNameIsHidden</span></span>|<span data-ttu-id="ea02e-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea02e-181">Boolean</span></span>|<span data-ttu-id="ea02e-182">Cuando se establece en true, este perfil fuerza el dispositivo para conectarse a una red que no difundir su SSID para todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ea02e-182">When set to true, this profile forces the device to connect to a network that doesn't broadcast its SSID to all devices.</span></span> <span data-ttu-id="ea02e-183">Se hereda de [androidForWorkWiFiConfiguration](../resources/intune-deviceconfig-androidforworkwificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea02e-183">Inherited from [androidForWorkWiFiConfiguration](../resources/intune-deviceconfig-androidforworkwificonfiguration.md)</span></span>|
|<span data-ttu-id="ea02e-184">wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="ea02e-184">wiFiSecurityType</span></span>|[<span data-ttu-id="ea02e-185">androidWiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="ea02e-185">androidWiFiSecurityType</span></span>](../resources/intune-deviceconfig-androidwifisecuritytype.md)|<span data-ttu-id="ea02e-186">Indica si el extremo de Wi-Fi utiliza un tipo de EAP en función de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ea02e-186">Indicates whether Wi-Fi endpoint uses an EAP based security type.</span></span> <span data-ttu-id="ea02e-187">Se hereda de [androidForWorkWiFiConfiguration](../resources/intune-deviceconfig-androidforworkwificonfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ea02e-187">Inherited from [androidForWorkWiFiConfiguration](../resources/intune-deviceconfig-androidforworkwificonfiguration.md).</span></span> <span data-ttu-id="ea02e-188">Los valores posibles son: `open` y `wpaEnterprise`.</span><span class="sxs-lookup"><span data-stu-id="ea02e-188">Possible values are: `open`, `wpaEnterprise`.</span></span>|
|<span data-ttu-id="ea02e-189">eapType</span><span class="sxs-lookup"><span data-stu-id="ea02e-189">eapType</span></span>|[<span data-ttu-id="ea02e-190">androidEapType</span><span class="sxs-lookup"><span data-stu-id="ea02e-190">androidEapType</span></span>](../resources/intune-deviceconfig-androideaptype.md)|<span data-ttu-id="ea02e-191">Indica el tipo de protocolo EAP establecido en el extremo de Wi-Fi (enrutador).</span><span class="sxs-lookup"><span data-stu-id="ea02e-191">Indicates the type of EAP protocol set on the the Wi-Fi endpoint (router).</span></span> <span data-ttu-id="ea02e-192">Los valores posibles son: `eapTls`, `eapTtls` y `peap`.</span><span class="sxs-lookup"><span data-stu-id="ea02e-192">Possible values are: `eapTls`, `eapTtls`, `peap`.</span></span>|
|<span data-ttu-id="ea02e-193">authenticationMethod</span><span class="sxs-lookup"><span data-stu-id="ea02e-193">authenticationMethod</span></span>|[<span data-ttu-id="ea02e-194">wiFiAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="ea02e-194">wiFiAuthenticationMethod</span></span>](../resources/intune-deviceconfig-wifiauthenticationmethod.md)|<span data-ttu-id="ea02e-195">Indica el método de autenticación que se debe usar cuando se configura el tipo de EAP PEAP o EAP-TTLS el cliente (dispositivo).</span><span class="sxs-lookup"><span data-stu-id="ea02e-195">Indicates the Authentication Method the client (device) needs to use when the EAP Type is configured to PEAP or EAP-TTLS.</span></span> <span data-ttu-id="ea02e-196">Los valores posibles son: `certificate` y `usernameAndPassword`.</span><span class="sxs-lookup"><span data-stu-id="ea02e-196">Possible values are: `certificate`, `usernameAndPassword`.</span></span>|
|<span data-ttu-id="ea02e-197">innerAuthenticationProtocolForEapTtls</span><span class="sxs-lookup"><span data-stu-id="ea02e-197">innerAuthenticationProtocolForEapTtls</span></span>|[<span data-ttu-id="ea02e-198">nonEapAuthenticationMethodForEapTtlsType</span><span class="sxs-lookup"><span data-stu-id="ea02e-198">nonEapAuthenticationMethodForEapTtlsType</span></span>](../resources/intune-deviceconfig-noneapauthenticationmethodforeapttlstype.md)|<span data-ttu-id="ea02e-199">Método no EAP para la autenticación (Inner identidad) cuando el tipo de EAP es EAP-TTLS y Authenticationmethod es el nombre de usuario y contraseña.</span><span class="sxs-lookup"><span data-stu-id="ea02e-199">Non-EAP Method for Authentication (Inner Identity) when EAP Type is EAP-TTLS and Authenticationmethod is Username and Password.</span></span> <span data-ttu-id="ea02e-200">Los valores posibles son: `unencryptedPassword`, `challengeHandshakeAuthenticationProtocol`, `microsoftChap` y `microsoftChapVersionTwo`.</span><span class="sxs-lookup"><span data-stu-id="ea02e-200">Possible values are: `unencryptedPassword`, `challengeHandshakeAuthenticationProtocol`, `microsoftChap`, `microsoftChapVersionTwo`.</span></span>|
|<span data-ttu-id="ea02e-201">innerAuthenticationProtocolForPeap</span><span class="sxs-lookup"><span data-stu-id="ea02e-201">innerAuthenticationProtocolForPeap</span></span>|[<span data-ttu-id="ea02e-202">nonEapAuthenticationMethodForPeap</span><span class="sxs-lookup"><span data-stu-id="ea02e-202">nonEapAuthenticationMethodForPeap</span></span>](../resources/intune-deviceconfig-noneapauthenticationmethodforpeap.md)|<span data-ttu-id="ea02e-203">Método no EAP para la autenticación (Inner identidad) cuando el tipo de EAP es PEAP y Authenticationmethod es el nombre de usuario y contraseña.</span><span class="sxs-lookup"><span data-stu-id="ea02e-203">Non-EAP Method for Authentication (Inner Identity) when EAP Type is PEAP and Authenticationmethod is Username and Password.</span></span> <span data-ttu-id="ea02e-204">Los valores posibles son: `none` y `microsoftChapVersionTwo`.</span><span class="sxs-lookup"><span data-stu-id="ea02e-204">Possible values are: `none`, `microsoftChapVersionTwo`.</span></span>|
|<span data-ttu-id="ea02e-205">outerIdentityPrivacyTemporaryValue</span><span class="sxs-lookup"><span data-stu-id="ea02e-205">outerIdentityPrivacyTemporaryValue</span></span>|<span data-ttu-id="ea02e-206">String</span><span class="sxs-lookup"><span data-stu-id="ea02e-206">String</span></span>|<span data-ttu-id="ea02e-207">Habilitar privacidad de identidad (identidad externa) cuando se configura el tipo de EAP a EAP-TTLS o PEAP.</span><span class="sxs-lookup"><span data-stu-id="ea02e-207">Enable identity privacy (Outer Identity) when EAP Type is configured to EAP-TTLS or PEAP.</span></span> <span data-ttu-id="ea02e-208">La cadena proporcionada aquí se usa para el nombre de usuario de los usuarios individuales de la máscara cuando intenten conectarse a la red Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="ea02e-208">The String provided here is used to mask the username of individual users when they attempt to connect to Wi-Fi network.</span></span>|



## <a name="response"></a><span data-ttu-id="ea02e-209">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea02e-209">Response</span></span>
<span data-ttu-id="ea02e-210">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidForWorkEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidforworkenterprisewificonfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea02e-210">If successful, this method returns a `201 Created` response code and a [androidForWorkEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidforworkenterprisewificonfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ea02e-211">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea02e-211">Example</span></span>
### <a name="request"></a><span data-ttu-id="ea02e-212">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea02e-212">Request</span></span>
<span data-ttu-id="ea02e-213">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea02e-213">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 836

{
  "@odata.type": "#microsoft.graph.androidForWorkEnterpriseWiFiConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "networkName": "Network Name value",
  "ssid": "Ssid value",
  "connectAutomatically": true,
  "connectWhenNetworkNameIsHidden": true,
  "wiFiSecurityType": "wpaEnterprise",
  "eapType": "eapTtls",
  "authenticationMethod": "usernameAndPassword",
  "innerAuthenticationProtocolForEapTtls": "challengeHandshakeAuthenticationProtocol",
  "innerAuthenticationProtocolForPeap": "microsoftChapVersionTwo",
  "outerIdentityPrivacyTemporaryValue": "Outer Identity Privacy Temporary Value value"
}
```

### <a name="response"></a><span data-ttu-id="ea02e-214">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea02e-214">Response</span></span>
<span data-ttu-id="ea02e-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ea02e-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 944

{
  "@odata.type": "#microsoft.graph.androidForWorkEnterpriseWiFiConfiguration",
  "id": "742d953a-953a-742d-3a95-2d743a952d74",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "networkName": "Network Name value",
  "ssid": "Ssid value",
  "connectAutomatically": true,
  "connectWhenNetworkNameIsHidden": true,
  "wiFiSecurityType": "wpaEnterprise",
  "eapType": "eapTtls",
  "authenticationMethod": "usernameAndPassword",
  "innerAuthenticationProtocolForEapTtls": "challengeHandshakeAuthenticationProtocol",
  "innerAuthenticationProtocolForPeap": "microsoftChapVersionTwo",
  "outerIdentityPrivacyTemporaryValue": "Outer Identity Privacy Temporary Value value"
}
```






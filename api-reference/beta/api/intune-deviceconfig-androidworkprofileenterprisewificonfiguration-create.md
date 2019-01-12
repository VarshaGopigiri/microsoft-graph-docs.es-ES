---
title: Crear androidWorkProfileEnterpriseWiFiConfiguration
description: Crear un nuevo objeto androidWorkProfileEnterpriseWiFiConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 200055c11b41f437a7bcfad332a104887697848c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27929217"
---
# <a name="create-androidworkprofileenterprisewificonfiguration"></a><span data-ttu-id="cc8c1-103">Crear androidWorkProfileEnterpriseWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc8c1-103">Create androidWorkProfileEnterpriseWiFiConfiguration</span></span>

> <span data-ttu-id="cc8c1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cc8c1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cc8c1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cc8c1-107">Crear un nuevo objeto [androidWorkProfileEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofileenterprisewificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="cc8c1-107">Create a new [androidWorkProfileEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofileenterprisewificonfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cc8c1-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cc8c1-108">Prerequisites</span></span>
<span data-ttu-id="cc8c1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cc8c1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cc8c1-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cc8c1-111">Permission type</span></span>|<span data-ttu-id="cc8c1-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cc8c1-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cc8c1-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cc8c1-113">Delegated (work or school account)</span></span>|<span data-ttu-id="cc8c1-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cc8c1-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="cc8c1-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cc8c1-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cc8c1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-116">Not supported.</span></span>|
|<span data-ttu-id="cc8c1-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cc8c1-117">Application</span></span>|<span data-ttu-id="cc8c1-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cc8c1-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cc8c1-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="cc8c1-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cc8c1-120">Request headers</span></span>
|<span data-ttu-id="cc8c1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc8c1-121">Header</span></span>|<span data-ttu-id="cc8c1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cc8c1-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cc8c1-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="cc8c1-123">Authorization</span></span>|<span data-ttu-id="cc8c1-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cc8c1-125">Accept</span><span class="sxs-lookup"><span data-stu-id="cc8c1-125">Accept</span></span>|<span data-ttu-id="cc8c1-126">application/json</span><span class="sxs-lookup"><span data-stu-id="cc8c1-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cc8c1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cc8c1-127">Request body</span></span>
<span data-ttu-id="cc8c1-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidWorkProfileEnterpriseWiFiConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-128">In the request body, supply a JSON representation for the androidWorkProfileEnterpriseWiFiConfiguration object.</span></span>

<span data-ttu-id="cc8c1-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidWorkProfileEnterpriseWiFiConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-129">The following table shows the properties that are required when you create the androidWorkProfileEnterpriseWiFiConfiguration.</span></span>

|<span data-ttu-id="cc8c1-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cc8c1-130">Property</span></span>|<span data-ttu-id="cc8c1-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="cc8c1-131">Type</span></span>|<span data-ttu-id="cc8c1-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc8c1-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cc8c1-133">id</span><span class="sxs-lookup"><span data-stu-id="cc8c1-133">id</span></span>|<span data-ttu-id="cc8c1-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="cc8c1-134">String</span></span>|<span data-ttu-id="cc8c1-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-135">Key of the entity.</span></span> <span data-ttu-id="cc8c1-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc8c1-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cc8c1-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="cc8c1-137">lastModifiedDateTime</span></span>|<span data-ttu-id="cc8c1-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cc8c1-138">DateTimeOffset</span></span>|<span data-ttu-id="cc8c1-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-139">DateTime the object was last modified.</span></span> <span data-ttu-id="cc8c1-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc8c1-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cc8c1-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="cc8c1-141">roleScopeTagIds</span></span>|<span data-ttu-id="cc8c1-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="cc8c1-142">String collection</span></span>|<span data-ttu-id="cc8c1-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="cc8c1-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc8c1-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cc8c1-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="cc8c1-145">supportsScopeTags</span></span>|<span data-ttu-id="cc8c1-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc8c1-146">Boolean</span></span>|<span data-ttu-id="cc8c1-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="cc8c1-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="cc8c1-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="cc8c1-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-150">This property is read-only.</span></span> <span data-ttu-id="cc8c1-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc8c1-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cc8c1-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="cc8c1-152">createdDateTime</span></span>|<span data-ttu-id="cc8c1-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cc8c1-153">DateTimeOffset</span></span>|<span data-ttu-id="cc8c1-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-154">DateTime the object was created.</span></span> <span data-ttu-id="cc8c1-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc8c1-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cc8c1-156">descripción</span><span class="sxs-lookup"><span data-stu-id="cc8c1-156">description</span></span>|<span data-ttu-id="cc8c1-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="cc8c1-157">String</span></span>|<span data-ttu-id="cc8c1-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="cc8c1-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc8c1-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cc8c1-160">displayName</span><span class="sxs-lookup"><span data-stu-id="cc8c1-160">displayName</span></span>|<span data-ttu-id="cc8c1-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="cc8c1-161">String</span></span>|<span data-ttu-id="cc8c1-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="cc8c1-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc8c1-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cc8c1-164">version</span><span class="sxs-lookup"><span data-stu-id="cc8c1-164">version</span></span>|<span data-ttu-id="cc8c1-165">Int32</span><span class="sxs-lookup"><span data-stu-id="cc8c1-165">Int32</span></span>|<span data-ttu-id="cc8c1-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-166">Version of the device configuration.</span></span> <span data-ttu-id="cc8c1-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc8c1-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cc8c1-168">networkName</span><span class="sxs-lookup"><span data-stu-id="cc8c1-168">networkName</span></span>|<span data-ttu-id="cc8c1-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="cc8c1-169">String</span></span>|<span data-ttu-id="cc8c1-170">Nombre de red se hereda de [androidWorkProfileWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofilewificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc8c1-170">Network Name Inherited from [androidWorkProfileWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofilewificonfiguration.md)</span></span>|
|<span data-ttu-id="cc8c1-171">SSID</span><span class="sxs-lookup"><span data-stu-id="cc8c1-171">ssid</span></span>|<span data-ttu-id="cc8c1-172">Cadena</span><span class="sxs-lookup"><span data-stu-id="cc8c1-172">String</span></span>|<span data-ttu-id="cc8c1-173">Esto es el nombre de la red Wi-Fi que se difunde a todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-173">This is the name of the Wi-Fi network that is broadcast to all devices.</span></span> <span data-ttu-id="cc8c1-174">Se hereda de [androidWorkProfileWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofilewificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc8c1-174">Inherited from [androidWorkProfileWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofilewificonfiguration.md)</span></span>|
|<span data-ttu-id="cc8c1-175">connectAutomatically</span><span class="sxs-lookup"><span data-stu-id="cc8c1-175">connectAutomatically</span></span>|<span data-ttu-id="cc8c1-176">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc8c1-176">Boolean</span></span>|<span data-ttu-id="cc8c1-177">Conectar automáticamente cuando esta red esté en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-177">Connect automatically when this network is in range.</span></span> <span data-ttu-id="cc8c1-178">Si se establece en true omitirá el símbolo del sistema del usuario y el dispositivo se conecte automáticamente a la red Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-178">Setting this to true will skip the user prompt and automatically connect the device to Wi-Fi network.</span></span> <span data-ttu-id="cc8c1-179">Se hereda de [androidWorkProfileWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofilewificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc8c1-179">Inherited from [androidWorkProfileWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofilewificonfiguration.md)</span></span>|
|<span data-ttu-id="cc8c1-180">connectWhenNetworkNameIsHidden</span><span class="sxs-lookup"><span data-stu-id="cc8c1-180">connectWhenNetworkNameIsHidden</span></span>|<span data-ttu-id="cc8c1-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc8c1-181">Boolean</span></span>|<span data-ttu-id="cc8c1-182">Cuando se establece en true, este perfil fuerza el dispositivo para conectarse a una red que no difundir su SSID para todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-182">When set to true, this profile forces the device to connect to a network that doesn't broadcast its SSID to all devices.</span></span> <span data-ttu-id="cc8c1-183">Se hereda de [androidWorkProfileWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofilewificonfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc8c1-183">Inherited from [androidWorkProfileWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofilewificonfiguration.md)</span></span>|
|<span data-ttu-id="cc8c1-184">wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="cc8c1-184">wiFiSecurityType</span></span>|[<span data-ttu-id="cc8c1-185">androidWiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="cc8c1-185">androidWiFiSecurityType</span></span>](../resources/intune-deviceconfig-androidwifisecuritytype.md)|<span data-ttu-id="cc8c1-186">Indica si el extremo de Wi-Fi utiliza un tipo de EAP en función de seguridad.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-186">Indicates whether Wi-Fi endpoint uses an EAP based security type.</span></span> <span data-ttu-id="cc8c1-187">Se hereda de [androidWorkProfileWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofilewificonfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="cc8c1-187">Inherited from [androidWorkProfileWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofilewificonfiguration.md).</span></span> <span data-ttu-id="cc8c1-188">Los valores posibles son: `open` y `wpaEnterprise`.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-188">Possible values are: `open`, `wpaEnterprise`.</span></span>|
|<span data-ttu-id="cc8c1-189">eapType</span><span class="sxs-lookup"><span data-stu-id="cc8c1-189">eapType</span></span>|[<span data-ttu-id="cc8c1-190">androidEapType</span><span class="sxs-lookup"><span data-stu-id="cc8c1-190">androidEapType</span></span>](../resources/intune-deviceconfig-androideaptype.md)|<span data-ttu-id="cc8c1-191">Indica el tipo de protocolo EAP establecido en el extremo de Wi-Fi (enrutador).</span><span class="sxs-lookup"><span data-stu-id="cc8c1-191">Indicates the type of EAP protocol set on the the Wi-Fi endpoint (router).</span></span> <span data-ttu-id="cc8c1-192">Los valores posibles son: `eapTls`, `eapTtls` y `peap`.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-192">Possible values are: `eapTls`, `eapTtls`, `peap`.</span></span>|
|<span data-ttu-id="cc8c1-193">authenticationMethod</span><span class="sxs-lookup"><span data-stu-id="cc8c1-193">authenticationMethod</span></span>|[<span data-ttu-id="cc8c1-194">wiFiAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="cc8c1-194">wiFiAuthenticationMethod</span></span>](../resources/intune-deviceconfig-wifiauthenticationmethod.md)|<span data-ttu-id="cc8c1-195">Indica el método de autenticación que se debe usar cuando se configura el tipo de EAP PEAP o EAP-TTLS el cliente (dispositivo).</span><span class="sxs-lookup"><span data-stu-id="cc8c1-195">Indicates the Authentication Method the client (device) needs to use when the EAP Type is configured to PEAP or EAP-TTLS.</span></span> <span data-ttu-id="cc8c1-196">Los valores posibles son: `certificate` y `usernameAndPassword`.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-196">Possible values are: `certificate`, `usernameAndPassword`.</span></span>|
|<span data-ttu-id="cc8c1-197">innerAuthenticationProtocolForEapTtls</span><span class="sxs-lookup"><span data-stu-id="cc8c1-197">innerAuthenticationProtocolForEapTtls</span></span>|[<span data-ttu-id="cc8c1-198">nonEapAuthenticationMethodForEapTtlsType</span><span class="sxs-lookup"><span data-stu-id="cc8c1-198">nonEapAuthenticationMethodForEapTtlsType</span></span>](../resources/intune-deviceconfig-noneapauthenticationmethodforeapttlstype.md)|<span data-ttu-id="cc8c1-199">Método no EAP para la autenticación (Inner identidad) cuando el tipo de EAP es EAP-TTLS y Authenticationmethod es el nombre de usuario y contraseña.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-199">Non-EAP Method for Authentication (Inner Identity) when EAP Type is EAP-TTLS and Authenticationmethod is Username and Password.</span></span> <span data-ttu-id="cc8c1-200">Los valores posibles son: `unencryptedPassword`, `challengeHandshakeAuthenticationProtocol`, `microsoftChap` y `microsoftChapVersionTwo`.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-200">Possible values are: `unencryptedPassword`, `challengeHandshakeAuthenticationProtocol`, `microsoftChap`, `microsoftChapVersionTwo`.</span></span>|
|<span data-ttu-id="cc8c1-201">innerAuthenticationProtocolForPeap</span><span class="sxs-lookup"><span data-stu-id="cc8c1-201">innerAuthenticationProtocolForPeap</span></span>|[<span data-ttu-id="cc8c1-202">nonEapAuthenticationMethodForPeap</span><span class="sxs-lookup"><span data-stu-id="cc8c1-202">nonEapAuthenticationMethodForPeap</span></span>](../resources/intune-deviceconfig-noneapauthenticationmethodforpeap.md)|<span data-ttu-id="cc8c1-203">Método no EAP para la autenticación (Inner identidad) cuando el tipo de EAP es PEAP y Authenticationmethod es el nombre de usuario y contraseña.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-203">Non-EAP Method for Authentication (Inner Identity) when EAP Type is PEAP and Authenticationmethod is Username and Password.</span></span> <span data-ttu-id="cc8c1-204">Los valores posibles son: `none` y `microsoftChapVersionTwo`.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-204">Possible values are: `none`, `microsoftChapVersionTwo`.</span></span>|
|<span data-ttu-id="cc8c1-205">outerIdentityPrivacyTemporaryValue</span><span class="sxs-lookup"><span data-stu-id="cc8c1-205">outerIdentityPrivacyTemporaryValue</span></span>|<span data-ttu-id="cc8c1-206">Cadena</span><span class="sxs-lookup"><span data-stu-id="cc8c1-206">String</span></span>|<span data-ttu-id="cc8c1-207">Habilitar privacidad de identidad (identidad externa) cuando se configura el tipo de EAP a EAP-TTLS o PEAP.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-207">Enable identity privacy (Outer Identity) when EAP Type is configured to EAP-TTLS or PEAP.</span></span> <span data-ttu-id="cc8c1-208">La cadena proporcionada aquí se usa para el nombre de usuario de los usuarios individuales de la máscara cuando intenten conectarse a la red Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-208">The String provided here is used to mask the username of individual users when they attempt to connect to Wi-Fi network.</span></span>|



## <a name="response"></a><span data-ttu-id="cc8c1-209">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc8c1-209">Response</span></span>
<span data-ttu-id="cc8c1-210">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidWorkProfileEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofileenterprisewificonfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-210">If successful, this method returns a `201 Created` response code and a [androidWorkProfileEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofileenterprisewificonfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cc8c1-211">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cc8c1-211">Example</span></span>
### <a name="request"></a><span data-ttu-id="cc8c1-212">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cc8c1-212">Request</span></span>
<span data-ttu-id="cc8c1-213">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-213">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 840

{
  "@odata.type": "#microsoft.graph.androidWorkProfileEnterpriseWiFiConfiguration",
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

### <a name="response"></a><span data-ttu-id="cc8c1-214">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc8c1-214">Response</span></span>
<span data-ttu-id="cc8c1-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cc8c1-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 948

{
  "@odata.type": "#microsoft.graph.androidWorkProfileEnterpriseWiFiConfiguration",
  "id": "c48cd726-d726-c48c-26d7-8cc426d78cc4",
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






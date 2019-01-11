---
title: Crear androidForWorkWiFiConfiguration
description: Crear un nuevo objeto androidForWorkWiFiConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7538929270794de8b7611011867eb1381d47d00b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27863493"
---
# <a name="create-androidforworkwificonfiguration"></a><span data-ttu-id="b2714-103">Crear androidForWorkWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2714-103">Create androidForWorkWiFiConfiguration</span></span>

> <span data-ttu-id="b2714-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b2714-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b2714-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b2714-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b2714-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b2714-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b2714-107">Crear un nuevo objeto [androidForWorkWiFiConfiguration](../resources/intune-deviceconfig-androidforworkwificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="b2714-107">Create a new [androidForWorkWiFiConfiguration](../resources/intune-deviceconfig-androidforworkwificonfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b2714-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b2714-108">Prerequisites</span></span>
<span data-ttu-id="b2714-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b2714-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b2714-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b2714-111">Permission type</span></span>|<span data-ttu-id="b2714-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b2714-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b2714-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b2714-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b2714-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b2714-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="b2714-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b2714-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b2714-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b2714-116">Not supported.</span></span>|
|<span data-ttu-id="b2714-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b2714-117">Application</span></span>|<span data-ttu-id="b2714-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b2714-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b2714-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b2714-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="b2714-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b2714-120">Request headers</span></span>
|<span data-ttu-id="b2714-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2714-121">Header</span></span>|<span data-ttu-id="b2714-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b2714-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b2714-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="b2714-123">Authorization</span></span>|<span data-ttu-id="b2714-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b2714-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b2714-125">Accept</span><span class="sxs-lookup"><span data-stu-id="b2714-125">Accept</span></span>|<span data-ttu-id="b2714-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b2714-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b2714-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b2714-127">Request body</span></span>
<span data-ttu-id="b2714-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidForWorkWiFiConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b2714-128">In the request body, supply a JSON representation for the androidForWorkWiFiConfiguration object.</span></span>

<span data-ttu-id="b2714-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidForWorkWiFiConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b2714-129">The following table shows the properties that are required when you create the androidForWorkWiFiConfiguration.</span></span>

|<span data-ttu-id="b2714-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b2714-130">Property</span></span>|<span data-ttu-id="b2714-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b2714-131">Type</span></span>|<span data-ttu-id="b2714-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2714-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b2714-133">id</span><span class="sxs-lookup"><span data-stu-id="b2714-133">id</span></span>|<span data-ttu-id="b2714-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2714-134">String</span></span>|<span data-ttu-id="b2714-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b2714-135">Key of the entity.</span></span> <span data-ttu-id="b2714-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b2714-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b2714-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b2714-137">lastModifiedDateTime</span></span>|<span data-ttu-id="b2714-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b2714-138">DateTimeOffset</span></span>|<span data-ttu-id="b2714-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="b2714-139">DateTime the object was last modified.</span></span> <span data-ttu-id="b2714-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b2714-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b2714-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="b2714-141">roleScopeTagIds</span></span>|<span data-ttu-id="b2714-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="b2714-142">String collection</span></span>|<span data-ttu-id="b2714-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="b2714-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="b2714-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b2714-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b2714-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="b2714-145">supportsScopeTags</span></span>|<span data-ttu-id="b2714-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="b2714-146">Boolean</span></span>|<span data-ttu-id="b2714-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b2714-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="b2714-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="b2714-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="b2714-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="b2714-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="b2714-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="b2714-150">This property is read-only.</span></span> <span data-ttu-id="b2714-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b2714-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b2714-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b2714-152">createdDateTime</span></span>|<span data-ttu-id="b2714-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b2714-153">DateTimeOffset</span></span>|<span data-ttu-id="b2714-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="b2714-154">DateTime the object was created.</span></span> <span data-ttu-id="b2714-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b2714-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b2714-156">descripción</span><span class="sxs-lookup"><span data-stu-id="b2714-156">description</span></span>|<span data-ttu-id="b2714-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2714-157">String</span></span>|<span data-ttu-id="b2714-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2714-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="b2714-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b2714-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b2714-160">displayName</span><span class="sxs-lookup"><span data-stu-id="b2714-160">displayName</span></span>|<span data-ttu-id="b2714-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2714-161">String</span></span>|<span data-ttu-id="b2714-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2714-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="b2714-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b2714-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b2714-164">version</span><span class="sxs-lookup"><span data-stu-id="b2714-164">version</span></span>|<span data-ttu-id="b2714-165">Int32</span><span class="sxs-lookup"><span data-stu-id="b2714-165">Int32</span></span>|<span data-ttu-id="b2714-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2714-166">Version of the device configuration.</span></span> <span data-ttu-id="b2714-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b2714-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b2714-168">networkName</span><span class="sxs-lookup"><span data-stu-id="b2714-168">networkName</span></span>|<span data-ttu-id="b2714-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2714-169">String</span></span>|<span data-ttu-id="b2714-170">Nombre de red</span><span class="sxs-lookup"><span data-stu-id="b2714-170">Network Name</span></span>|
|<span data-ttu-id="b2714-171">SSID</span><span class="sxs-lookup"><span data-stu-id="b2714-171">ssid</span></span>|<span data-ttu-id="b2714-172">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2714-172">String</span></span>|<span data-ttu-id="b2714-173">Esto es el nombre de la red Wi-Fi que se difunde a todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b2714-173">This is the name of the Wi-Fi network that is broadcast to all devices.</span></span>|
|<span data-ttu-id="b2714-174">connectAutomatically</span><span class="sxs-lookup"><span data-stu-id="b2714-174">connectAutomatically</span></span>|<span data-ttu-id="b2714-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="b2714-175">Boolean</span></span>|<span data-ttu-id="b2714-176">Conectar automáticamente cuando esta red esté en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="b2714-176">Connect automatically when this network is in range.</span></span> <span data-ttu-id="b2714-177">Si se establece en true omitirá el símbolo del sistema del usuario y el dispositivo se conecte automáticamente a la red Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="b2714-177">Setting this to true will skip the user prompt and automatically connect the device to Wi-Fi network.</span></span>|
|<span data-ttu-id="b2714-178">connectWhenNetworkNameIsHidden</span><span class="sxs-lookup"><span data-stu-id="b2714-178">connectWhenNetworkNameIsHidden</span></span>|<span data-ttu-id="b2714-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="b2714-179">Boolean</span></span>|<span data-ttu-id="b2714-180">Cuando se establece en true, este perfil fuerza el dispositivo para conectarse a una red que no difundir su SSID para todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b2714-180">When set to true, this profile forces the device to connect to a network that doesn't broadcast its SSID to all devices.</span></span>|
|<span data-ttu-id="b2714-181">wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="b2714-181">wiFiSecurityType</span></span>|[<span data-ttu-id="b2714-182">androidWiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="b2714-182">androidWiFiSecurityType</span></span>](../resources/intune-deviceconfig-androidwifisecuritytype.md)|<span data-ttu-id="b2714-183">Indica si el extremo de Wi-Fi utiliza un tipo de EAP en función de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b2714-183">Indicates whether Wi-Fi endpoint uses an EAP based security type.</span></span> <span data-ttu-id="b2714-184">Los valores posibles son: `open` y `wpaEnterprise`.</span><span class="sxs-lookup"><span data-stu-id="b2714-184">Possible values are: `open`, `wpaEnterprise`.</span></span>|



## <a name="response"></a><span data-ttu-id="b2714-185">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2714-185">Response</span></span>
<span data-ttu-id="b2714-186">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidForWorkWiFiConfiguration](../resources/intune-deviceconfig-androidforworkwificonfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b2714-186">If successful, this method returns a `201 Created` response code and a [androidForWorkWiFiConfiguration](../resources/intune-deviceconfig-androidforworkwificonfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b2714-187">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b2714-187">Example</span></span>
### <a name="request"></a><span data-ttu-id="b2714-188">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b2714-188">Request</span></span>
<span data-ttu-id="b2714-189">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b2714-189">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 506

{
  "@odata.type": "#microsoft.graph.androidForWorkWiFiConfiguration",
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
  "wiFiSecurityType": "wpaEnterprise"
}
```

### <a name="response"></a><span data-ttu-id="b2714-190">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2714-190">Response</span></span>
<span data-ttu-id="b2714-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b2714-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 614

{
  "@odata.type": "#microsoft.graph.androidForWorkWiFiConfiguration",
  "id": "58bcfe05-fe05-58bc-05fe-bc5805febc58",
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
  "wiFiSecurityType": "wpaEnterprise"
}
```






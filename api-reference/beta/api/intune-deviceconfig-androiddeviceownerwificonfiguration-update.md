---
title: Actualizar androidDeviceOwnerWiFiConfiguration
description: Actualizar las propiedades de un objeto androidDeviceOwnerWiFiConfiguration.
ms.openlocfilehash: fe929e840827ca6b6e06b00663edcd5e6c0738ce
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086917"
---
# <a name="update-androiddeviceownerwificonfiguration"></a><span data-ttu-id="40a7a-103">Actualizar androidDeviceOwnerWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="40a7a-103">Update androidDeviceOwnerWiFiConfiguration</span></span>

> <span data-ttu-id="40a7a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="40a7a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="40a7a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="40a7a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="40a7a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="40a7a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="40a7a-107">Actualizar las propiedades de un objeto [androidDeviceOwnerWiFiConfiguration](../resources/intune-deviceconfig-androiddeviceownerwificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="40a7a-107">Update the properties of a [androidDeviceOwnerWiFiConfiguration](../resources/intune-deviceconfig-androiddeviceownerwificonfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="40a7a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="40a7a-108">Prerequisites</span></span>
<span data-ttu-id="40a7a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="40a7a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="40a7a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="40a7a-111">Permission type</span></span>|<span data-ttu-id="40a7a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="40a7a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="40a7a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="40a7a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="40a7a-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="40a7a-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="40a7a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="40a7a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="40a7a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="40a7a-116">Not supported.</span></span>|
|<span data-ttu-id="40a7a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="40a7a-117">Application</span></span>|<span data-ttu-id="40a7a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="40a7a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="40a7a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="40a7a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="40a7a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="40a7a-120">Request headers</span></span>
|<span data-ttu-id="40a7a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40a7a-121">Header</span></span>|<span data-ttu-id="40a7a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="40a7a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="40a7a-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="40a7a-123">Authorization</span></span>|<span data-ttu-id="40a7a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="40a7a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="40a7a-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="40a7a-125">Accept</span></span>|<span data-ttu-id="40a7a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="40a7a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="40a7a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="40a7a-127">Request body</span></span>
<span data-ttu-id="40a7a-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidDeviceOwnerWiFiConfiguration](../resources/intune-deviceconfig-androiddeviceownerwificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="40a7a-128">In the request body, supply a JSON representation for the [androidDeviceOwnerWiFiConfiguration](../resources/intune-deviceconfig-androiddeviceownerwificonfiguration.md) object.</span></span>

<span data-ttu-id="40a7a-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidDeviceOwnerWiFiConfiguration](../resources/intune-deviceconfig-androiddeviceownerwificonfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="40a7a-129">The following table shows the properties that are required when you create the [androidDeviceOwnerWiFiConfiguration](../resources/intune-deviceconfig-androiddeviceownerwificonfiguration.md).</span></span>

|<span data-ttu-id="40a7a-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="40a7a-130">Property</span></span>|<span data-ttu-id="40a7a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="40a7a-131">Type</span></span>|<span data-ttu-id="40a7a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="40a7a-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="40a7a-133">id</span><span class="sxs-lookup"><span data-stu-id="40a7a-133">id</span></span>|<span data-ttu-id="40a7a-134">String</span><span class="sxs-lookup"><span data-stu-id="40a7a-134">String</span></span>|<span data-ttu-id="40a7a-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="40a7a-135">Key of the entity.</span></span> <span data-ttu-id="40a7a-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="40a7a-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="40a7a-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="40a7a-137">lastModifiedDateTime</span></span>|<span data-ttu-id="40a7a-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="40a7a-138">DateTimeOffset</span></span>|<span data-ttu-id="40a7a-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="40a7a-139">DateTime the object was last modified.</span></span> <span data-ttu-id="40a7a-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="40a7a-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="40a7a-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="40a7a-141">roleScopeTagIds</span></span>|<span data-ttu-id="40a7a-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="40a7a-142">String collection</span></span>|<span data-ttu-id="40a7a-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="40a7a-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="40a7a-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="40a7a-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="40a7a-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="40a7a-145">supportsScopeTags</span></span>|<span data-ttu-id="40a7a-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="40a7a-146">Boolean</span></span>|<span data-ttu-id="40a7a-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="40a7a-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="40a7a-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="40a7a-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="40a7a-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="40a7a-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="40a7a-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="40a7a-150">This property is read-only.</span></span> <span data-ttu-id="40a7a-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="40a7a-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="40a7a-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="40a7a-152">createdDateTime</span></span>|<span data-ttu-id="40a7a-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="40a7a-153">DateTimeOffset</span></span>|<span data-ttu-id="40a7a-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="40a7a-154">DateTime the object was created.</span></span> <span data-ttu-id="40a7a-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="40a7a-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="40a7a-156">descripción</span><span class="sxs-lookup"><span data-stu-id="40a7a-156">description</span></span>|<span data-ttu-id="40a7a-157">String</span><span class="sxs-lookup"><span data-stu-id="40a7a-157">String</span></span>|<span data-ttu-id="40a7a-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40a7a-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="40a7a-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="40a7a-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="40a7a-160">displayName</span><span class="sxs-lookup"><span data-stu-id="40a7a-160">displayName</span></span>|<span data-ttu-id="40a7a-161">String</span><span class="sxs-lookup"><span data-stu-id="40a7a-161">String</span></span>|<span data-ttu-id="40a7a-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40a7a-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="40a7a-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="40a7a-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="40a7a-164">version</span><span class="sxs-lookup"><span data-stu-id="40a7a-164">version</span></span>|<span data-ttu-id="40a7a-165">Int32</span><span class="sxs-lookup"><span data-stu-id="40a7a-165">Int32</span></span>|<span data-ttu-id="40a7a-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40a7a-166">Version of the device configuration.</span></span> <span data-ttu-id="40a7a-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="40a7a-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="40a7a-168">networkName</span><span class="sxs-lookup"><span data-stu-id="40a7a-168">networkName</span></span>|<span data-ttu-id="40a7a-169">String</span><span class="sxs-lookup"><span data-stu-id="40a7a-169">String</span></span>|<span data-ttu-id="40a7a-170">Nombre de red</span><span class="sxs-lookup"><span data-stu-id="40a7a-170">Network Name</span></span>|
|<span data-ttu-id="40a7a-171">SSID</span><span class="sxs-lookup"><span data-stu-id="40a7a-171">ssid</span></span>|<span data-ttu-id="40a7a-172">String</span><span class="sxs-lookup"><span data-stu-id="40a7a-172">String</span></span>|<span data-ttu-id="40a7a-173">Esto es el nombre de la red Wi-Fi que se difunde a todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="40a7a-173">This is the name of the Wi-Fi network that is broadcast to all devices.</span></span>|
|<span data-ttu-id="40a7a-174">connectAutomatically</span><span class="sxs-lookup"><span data-stu-id="40a7a-174">connectAutomatically</span></span>|<span data-ttu-id="40a7a-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="40a7a-175">Boolean</span></span>|<span data-ttu-id="40a7a-176">Conectar automáticamente cuando esta red esté en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="40a7a-176">Connect automatically when this network is in range.</span></span> <span data-ttu-id="40a7a-177">Si se establece en true omitirá el símbolo del sistema del usuario y el dispositivo se conecte automáticamente a la red Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="40a7a-177">Setting this to true will skip the user prompt and automatically connect the device to Wi-Fi network.</span></span>|
|<span data-ttu-id="40a7a-178">connectWhenNetworkNameIsHidden</span><span class="sxs-lookup"><span data-stu-id="40a7a-178">connectWhenNetworkNameIsHidden</span></span>|<span data-ttu-id="40a7a-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="40a7a-179">Boolean</span></span>|<span data-ttu-id="40a7a-180">Cuando se establece en true, este perfil fuerza el dispositivo para conectarse a una red que no difundir su SSID para todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="40a7a-180">When set to true, this profile forces the device to connect to a network that doesn't broadcast its SSID to all devices.</span></span>|
|<span data-ttu-id="40a7a-181">wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="40a7a-181">wiFiSecurityType</span></span>|[<span data-ttu-id="40a7a-182">androidDeviceOwnerWiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="40a7a-182">androidDeviceOwnerWiFiSecurityType</span></span>](../resources/intune-deviceconfig-androiddeviceownerwifisecuritytype.md)|<span data-ttu-id="40a7a-183">Indica si el extremo de Wi-Fi utiliza un tipo de EAP en función de seguridad.</span><span class="sxs-lookup"><span data-stu-id="40a7a-183">Indicates whether Wi-Fi endpoint uses an EAP based security type.</span></span> <span data-ttu-id="40a7a-184">Los valores posibles son: `open`, `wep` y `wpaPersonal`.</span><span class="sxs-lookup"><span data-stu-id="40a7a-184">Possible values are: `open`, `wep`, `wpaPersonal`.</span></span>|
|<span data-ttu-id="40a7a-185">preSharedKey</span><span class="sxs-lookup"><span data-stu-id="40a7a-185">preSharedKey</span></span>|<span data-ttu-id="40a7a-186">String</span><span class="sxs-lookup"><span data-stu-id="40a7a-186">String</span></span>|<span data-ttu-id="40a7a-187">Ésta es la clave previamente compartida para la red Wi-Fi Personal WPA.</span><span class="sxs-lookup"><span data-stu-id="40a7a-187">This is the pre-shared key for WPA Personal Wi-Fi network.</span></span>|
|<span data-ttu-id="40a7a-188">preSharedKeyIsSet</span><span class="sxs-lookup"><span data-stu-id="40a7a-188">preSharedKeyIsSet</span></span>|<span data-ttu-id="40a7a-189">Booleano</span><span class="sxs-lookup"><span data-stu-id="40a7a-189">Boolean</span></span>|<span data-ttu-id="40a7a-190">Ésta es la clave previamente compartida para la red Wi-Fi Personal WPA.</span><span class="sxs-lookup"><span data-stu-id="40a7a-190">This is the pre-shared key for WPA Personal Wi-Fi network.</span></span>|



## <a name="response"></a><span data-ttu-id="40a7a-191">Respuesta</span><span class="sxs-lookup"><span data-stu-id="40a7a-191">Response</span></span>
<span data-ttu-id="40a7a-192">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidDeviceOwnerWiFiConfiguration](../resources/intune-deviceconfig-androiddeviceownerwificonfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="40a7a-192">If successful, this method returns a `200 OK` response code and an updated [androidDeviceOwnerWiFiConfiguration](../resources/intune-deviceconfig-androiddeviceownerwificonfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="40a7a-193">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="40a7a-193">Example</span></span>
### <a name="request"></a><span data-ttu-id="40a7a-194">Solicitud</span><span class="sxs-lookup"><span data-stu-id="40a7a-194">Request</span></span>
<span data-ttu-id="40a7a-195">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="40a7a-195">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 499

{
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
  "wiFiSecurityType": "wep",
  "preSharedKey": "Pre Shared Key value",
  "preSharedKeyIsSet": true
}
```

### <a name="response"></a><span data-ttu-id="40a7a-196">Respuesta</span><span class="sxs-lookup"><span data-stu-id="40a7a-196">Response</span></span>
<span data-ttu-id="40a7a-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="40a7a-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 681

{
  "@odata.type": "#microsoft.graph.androidDeviceOwnerWiFiConfiguration",
  "id": "8d25beba-beba-8d25-babe-258dbabe258d",
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
  "wiFiSecurityType": "wep",
  "preSharedKey": "Pre Shared Key value",
  "preSharedKeyIsSet": true
}
```






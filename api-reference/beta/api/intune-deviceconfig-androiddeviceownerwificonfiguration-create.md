---
title: Crear androidDeviceOwnerWiFiConfiguration
description: Crear un nuevo objeto androidDeviceOwnerWiFiConfiguration.
author: tfitzmac
ms.openlocfilehash: f3933e28bb0c47ccc104adb00358237c51920dfb
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27327331"
---
# <a name="create-androiddeviceownerwificonfiguration"></a><span data-ttu-id="41280-103">Crear androidDeviceOwnerWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="41280-103">Create androidDeviceOwnerWiFiConfiguration</span></span>

> <span data-ttu-id="41280-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="41280-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="41280-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="41280-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="41280-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="41280-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="41280-107">Crear un nuevo objeto [androidDeviceOwnerWiFiConfiguration](../resources/intune-deviceconfig-androiddeviceownerwificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="41280-107">Create a new [androidDeviceOwnerWiFiConfiguration](../resources/intune-deviceconfig-androiddeviceownerwificonfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="41280-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="41280-108">Prerequisites</span></span>
<span data-ttu-id="41280-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="41280-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="41280-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="41280-111">Permission type</span></span>|<span data-ttu-id="41280-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="41280-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="41280-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="41280-113">Delegated (work or school account)</span></span>|<span data-ttu-id="41280-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="41280-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="41280-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="41280-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="41280-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41280-116">Not supported.</span></span>|
|<span data-ttu-id="41280-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="41280-117">Application</span></span>|<span data-ttu-id="41280-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41280-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="41280-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="41280-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="41280-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="41280-120">Request headers</span></span>
|<span data-ttu-id="41280-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41280-121">Header</span></span>|<span data-ttu-id="41280-122">Valor</span><span class="sxs-lookup"><span data-stu-id="41280-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="41280-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="41280-123">Authorization</span></span>|<span data-ttu-id="41280-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="41280-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="41280-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="41280-125">Accept</span></span>|<span data-ttu-id="41280-126">application/json</span><span class="sxs-lookup"><span data-stu-id="41280-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="41280-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="41280-127">Request body</span></span>
<span data-ttu-id="41280-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidDeviceOwnerWiFiConfiguration.</span><span class="sxs-lookup"><span data-stu-id="41280-128">In the request body, supply a JSON representation for the androidDeviceOwnerWiFiConfiguration object.</span></span>

<span data-ttu-id="41280-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidDeviceOwnerWiFiConfiguration.</span><span class="sxs-lookup"><span data-stu-id="41280-129">The following table shows the properties that are required when you create the androidDeviceOwnerWiFiConfiguration.</span></span>

|<span data-ttu-id="41280-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="41280-130">Property</span></span>|<span data-ttu-id="41280-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="41280-131">Type</span></span>|<span data-ttu-id="41280-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="41280-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="41280-133">id</span><span class="sxs-lookup"><span data-stu-id="41280-133">id</span></span>|<span data-ttu-id="41280-134">String</span><span class="sxs-lookup"><span data-stu-id="41280-134">String</span></span>|<span data-ttu-id="41280-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="41280-135">Key of the entity.</span></span> <span data-ttu-id="41280-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="41280-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="41280-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="41280-137">lastModifiedDateTime</span></span>|<span data-ttu-id="41280-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="41280-138">DateTimeOffset</span></span>|<span data-ttu-id="41280-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="41280-139">DateTime the object was last modified.</span></span> <span data-ttu-id="41280-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="41280-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="41280-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="41280-141">roleScopeTagIds</span></span>|<span data-ttu-id="41280-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="41280-142">String collection</span></span>|<span data-ttu-id="41280-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="41280-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="41280-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="41280-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="41280-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="41280-145">supportsScopeTags</span></span>|<span data-ttu-id="41280-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="41280-146">Boolean</span></span>|<span data-ttu-id="41280-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="41280-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="41280-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="41280-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="41280-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="41280-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="41280-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="41280-150">This property is read-only.</span></span> <span data-ttu-id="41280-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="41280-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="41280-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="41280-152">createdDateTime</span></span>|<span data-ttu-id="41280-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="41280-153">DateTimeOffset</span></span>|<span data-ttu-id="41280-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="41280-154">DateTime the object was created.</span></span> <span data-ttu-id="41280-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="41280-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="41280-156">descripción</span><span class="sxs-lookup"><span data-stu-id="41280-156">description</span></span>|<span data-ttu-id="41280-157">String</span><span class="sxs-lookup"><span data-stu-id="41280-157">String</span></span>|<span data-ttu-id="41280-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41280-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="41280-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="41280-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="41280-160">displayName</span><span class="sxs-lookup"><span data-stu-id="41280-160">displayName</span></span>|<span data-ttu-id="41280-161">String</span><span class="sxs-lookup"><span data-stu-id="41280-161">String</span></span>|<span data-ttu-id="41280-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41280-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="41280-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="41280-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="41280-164">version</span><span class="sxs-lookup"><span data-stu-id="41280-164">version</span></span>|<span data-ttu-id="41280-165">Int32</span><span class="sxs-lookup"><span data-stu-id="41280-165">Int32</span></span>|<span data-ttu-id="41280-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41280-166">Version of the device configuration.</span></span> <span data-ttu-id="41280-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="41280-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="41280-168">networkName</span><span class="sxs-lookup"><span data-stu-id="41280-168">networkName</span></span>|<span data-ttu-id="41280-169">String</span><span class="sxs-lookup"><span data-stu-id="41280-169">String</span></span>|<span data-ttu-id="41280-170">Nombre de red</span><span class="sxs-lookup"><span data-stu-id="41280-170">Network Name</span></span>|
|<span data-ttu-id="41280-171">SSID</span><span class="sxs-lookup"><span data-stu-id="41280-171">ssid</span></span>|<span data-ttu-id="41280-172">String</span><span class="sxs-lookup"><span data-stu-id="41280-172">String</span></span>|<span data-ttu-id="41280-173">Esto es el nombre de la red Wi-Fi que se difunde a todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="41280-173">This is the name of the Wi-Fi network that is broadcast to all devices.</span></span>|
|<span data-ttu-id="41280-174">connectAutomatically</span><span class="sxs-lookup"><span data-stu-id="41280-174">connectAutomatically</span></span>|<span data-ttu-id="41280-175">Boolean</span><span class="sxs-lookup"><span data-stu-id="41280-175">Boolean</span></span>|<span data-ttu-id="41280-176">Conectar automáticamente cuando esta red esté en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="41280-176">Connect automatically when this network is in range.</span></span> <span data-ttu-id="41280-177">Si se establece en true omitirá el símbolo del sistema del usuario y el dispositivo se conecte automáticamente a la red Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="41280-177">Setting this to true will skip the user prompt and automatically connect the device to Wi-Fi network.</span></span>|
|<span data-ttu-id="41280-178">connectWhenNetworkNameIsHidden</span><span class="sxs-lookup"><span data-stu-id="41280-178">connectWhenNetworkNameIsHidden</span></span>|<span data-ttu-id="41280-179">Boolean</span><span class="sxs-lookup"><span data-stu-id="41280-179">Boolean</span></span>|<span data-ttu-id="41280-180">Cuando se establece en true, este perfil fuerza el dispositivo para conectarse a una red que no difundir su SSID para todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="41280-180">When set to true, this profile forces the device to connect to a network that doesn't broadcast its SSID to all devices.</span></span>|
|<span data-ttu-id="41280-181">wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="41280-181">wiFiSecurityType</span></span>|[<span data-ttu-id="41280-182">androidDeviceOwnerWiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="41280-182">androidDeviceOwnerWiFiSecurityType</span></span>](../resources/intune-deviceconfig-androiddeviceownerwifisecuritytype.md)|<span data-ttu-id="41280-183">Indica si el extremo de Wi-Fi utiliza un tipo de EAP en función de seguridad.</span><span class="sxs-lookup"><span data-stu-id="41280-183">Indicates whether Wi-Fi endpoint uses an EAP based security type.</span></span> <span data-ttu-id="41280-184">Los valores posibles son: `open`, `wep` y `wpaPersonal`.</span><span class="sxs-lookup"><span data-stu-id="41280-184">Possible values are: `open`, `wep`, `wpaPersonal`.</span></span>|
|<span data-ttu-id="41280-185">preSharedKey</span><span class="sxs-lookup"><span data-stu-id="41280-185">preSharedKey</span></span>|<span data-ttu-id="41280-186">String</span><span class="sxs-lookup"><span data-stu-id="41280-186">String</span></span>|<span data-ttu-id="41280-187">Ésta es la clave previamente compartida para la red Wi-Fi Personal WPA.</span><span class="sxs-lookup"><span data-stu-id="41280-187">This is the pre-shared key for WPA Personal Wi-Fi network.</span></span>|
|<span data-ttu-id="41280-188">preSharedKeyIsSet</span><span class="sxs-lookup"><span data-stu-id="41280-188">preSharedKeyIsSet</span></span>|<span data-ttu-id="41280-189">Boolean</span><span class="sxs-lookup"><span data-stu-id="41280-189">Boolean</span></span>|<span data-ttu-id="41280-190">Ésta es la clave previamente compartida para la red Wi-Fi Personal WPA.</span><span class="sxs-lookup"><span data-stu-id="41280-190">This is the pre-shared key for WPA Personal Wi-Fi network.</span></span>|



## <a name="response"></a><span data-ttu-id="41280-191">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41280-191">Response</span></span>
<span data-ttu-id="41280-192">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidDeviceOwnerWiFiConfiguration](../resources/intune-deviceconfig-androiddeviceownerwificonfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="41280-192">If successful, this method returns a `201 Created` response code and a [androidDeviceOwnerWiFiConfiguration](../resources/intune-deviceconfig-androiddeviceownerwificonfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="41280-193">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="41280-193">Example</span></span>
### <a name="request"></a><span data-ttu-id="41280-194">Solicitud</span><span class="sxs-lookup"><span data-stu-id="41280-194">Request</span></span>
<span data-ttu-id="41280-195">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="41280-195">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 573

{
  "@odata.type": "#microsoft.graph.androidDeviceOwnerWiFiConfiguration",
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

### <a name="response"></a><span data-ttu-id="41280-196">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41280-196">Response</span></span>
<span data-ttu-id="41280-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="41280-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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






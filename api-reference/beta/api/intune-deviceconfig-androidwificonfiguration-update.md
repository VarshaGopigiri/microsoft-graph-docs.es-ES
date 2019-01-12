---
title: Actualizar androidWiFiConfiguration
description: Actualizar las propiedades de un objeto androidWiFiConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 25794454f750f1d79e5d43bf866157f9761e36c3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27949440"
---
# <a name="update-androidwificonfiguration"></a><span data-ttu-id="78623-103">Actualizar androidWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="78623-103">Update androidWiFiConfiguration</span></span>

> <span data-ttu-id="78623-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="78623-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="78623-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="78623-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="78623-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="78623-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="78623-107">Actualizar las propiedades de un objeto [androidWiFiConfiguration](../resources/intune-deviceconfig-androidwificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="78623-107">Update the properties of a [androidWiFiConfiguration](../resources/intune-deviceconfig-androidwificonfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="78623-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="78623-108">Prerequisites</span></span>
<span data-ttu-id="78623-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="78623-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="78623-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="78623-111">Permission type</span></span>|<span data-ttu-id="78623-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="78623-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="78623-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="78623-113">Delegated (work or school account)</span></span>|<span data-ttu-id="78623-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="78623-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="78623-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="78623-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="78623-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="78623-116">Not supported.</span></span>|
|<span data-ttu-id="78623-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="78623-117">Application</span></span>|<span data-ttu-id="78623-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="78623-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="78623-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="78623-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="78623-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="78623-120">Request headers</span></span>
|<span data-ttu-id="78623-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78623-121">Header</span></span>|<span data-ttu-id="78623-122">Valor</span><span class="sxs-lookup"><span data-stu-id="78623-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="78623-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="78623-123">Authorization</span></span>|<span data-ttu-id="78623-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="78623-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="78623-125">Accept</span><span class="sxs-lookup"><span data-stu-id="78623-125">Accept</span></span>|<span data-ttu-id="78623-126">application/json</span><span class="sxs-lookup"><span data-stu-id="78623-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="78623-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="78623-127">Request body</span></span>
<span data-ttu-id="78623-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidWiFiConfiguration](../resources/intune-deviceconfig-androidwificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="78623-128">In the request body, supply a JSON representation for the [androidWiFiConfiguration](../resources/intune-deviceconfig-androidwificonfiguration.md) object.</span></span>

<span data-ttu-id="78623-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidWiFiConfiguration](../resources/intune-deviceconfig-androidwificonfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="78623-129">The following table shows the properties that are required when you create the [androidWiFiConfiguration](../resources/intune-deviceconfig-androidwificonfiguration.md).</span></span>

|<span data-ttu-id="78623-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="78623-130">Property</span></span>|<span data-ttu-id="78623-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="78623-131">Type</span></span>|<span data-ttu-id="78623-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="78623-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="78623-133">id</span><span class="sxs-lookup"><span data-stu-id="78623-133">id</span></span>|<span data-ttu-id="78623-134">String</span><span class="sxs-lookup"><span data-stu-id="78623-134">String</span></span>|<span data-ttu-id="78623-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="78623-135">Key of the entity.</span></span> <span data-ttu-id="78623-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="78623-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="78623-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="78623-137">lastModifiedDateTime</span></span>|<span data-ttu-id="78623-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="78623-138">DateTimeOffset</span></span>|<span data-ttu-id="78623-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="78623-139">DateTime the object was last modified.</span></span> <span data-ttu-id="78623-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="78623-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="78623-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="78623-141">roleScopeTagIds</span></span>|<span data-ttu-id="78623-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="78623-142">String collection</span></span>|<span data-ttu-id="78623-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="78623-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="78623-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="78623-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="78623-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="78623-145">supportsScopeTags</span></span>|<span data-ttu-id="78623-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="78623-146">Boolean</span></span>|<span data-ttu-id="78623-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="78623-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="78623-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="78623-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="78623-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="78623-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="78623-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="78623-150">This property is read-only.</span></span> <span data-ttu-id="78623-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="78623-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="78623-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="78623-152">createdDateTime</span></span>|<span data-ttu-id="78623-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="78623-153">DateTimeOffset</span></span>|<span data-ttu-id="78623-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="78623-154">DateTime the object was created.</span></span> <span data-ttu-id="78623-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="78623-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="78623-156">descripción</span><span class="sxs-lookup"><span data-stu-id="78623-156">description</span></span>|<span data-ttu-id="78623-157">String</span><span class="sxs-lookup"><span data-stu-id="78623-157">String</span></span>|<span data-ttu-id="78623-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78623-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="78623-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="78623-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="78623-160">displayName</span><span class="sxs-lookup"><span data-stu-id="78623-160">displayName</span></span>|<span data-ttu-id="78623-161">String</span><span class="sxs-lookup"><span data-stu-id="78623-161">String</span></span>|<span data-ttu-id="78623-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78623-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="78623-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="78623-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="78623-164">version</span><span class="sxs-lookup"><span data-stu-id="78623-164">version</span></span>|<span data-ttu-id="78623-165">Int32</span><span class="sxs-lookup"><span data-stu-id="78623-165">Int32</span></span>|<span data-ttu-id="78623-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78623-166">Version of the device configuration.</span></span> <span data-ttu-id="78623-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="78623-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="78623-168">networkName</span><span class="sxs-lookup"><span data-stu-id="78623-168">networkName</span></span>|<span data-ttu-id="78623-169">String</span><span class="sxs-lookup"><span data-stu-id="78623-169">String</span></span>|<span data-ttu-id="78623-170">Nombre de red</span><span class="sxs-lookup"><span data-stu-id="78623-170">Network Name</span></span>|
|<span data-ttu-id="78623-171">SSID</span><span class="sxs-lookup"><span data-stu-id="78623-171">ssid</span></span>|<span data-ttu-id="78623-172">String</span><span class="sxs-lookup"><span data-stu-id="78623-172">String</span></span>|<span data-ttu-id="78623-173">Esto es el nombre de la red Wi-Fi que se difunde a todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="78623-173">This is the name of the Wi-Fi network that is broadcast to all devices.</span></span>|
|<span data-ttu-id="78623-174">connectAutomatically</span><span class="sxs-lookup"><span data-stu-id="78623-174">connectAutomatically</span></span>|<span data-ttu-id="78623-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="78623-175">Boolean</span></span>|<span data-ttu-id="78623-176">Conectar automáticamente cuando esta red esté en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="78623-176">Connect automatically when this network is in range.</span></span> <span data-ttu-id="78623-177">Si se establece en true omitirá el símbolo del sistema del usuario y el dispositivo se conecte automáticamente a la red Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="78623-177">Setting this to true will skip the user prompt and automatically connect the device to Wi-Fi network.</span></span>|
|<span data-ttu-id="78623-178">connectWhenNetworkNameIsHidden</span><span class="sxs-lookup"><span data-stu-id="78623-178">connectWhenNetworkNameIsHidden</span></span>|<span data-ttu-id="78623-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="78623-179">Boolean</span></span>|<span data-ttu-id="78623-180">Cuando se establece en true, este perfil fuerza el dispositivo para conectarse a una red que no difundir su SSID para todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="78623-180">When set to true, this profile forces the device to connect to a network that doesn't broadcast its SSID to all devices.</span></span>|
|<span data-ttu-id="78623-181">wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="78623-181">wiFiSecurityType</span></span>|[<span data-ttu-id="78623-182">androidWiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="78623-182">androidWiFiSecurityType</span></span>](../resources/intune-deviceconfig-androidwifisecuritytype.md)|<span data-ttu-id="78623-183">Indica si el extremo de Wi-Fi utiliza un tipo de EAP en función de seguridad.</span><span class="sxs-lookup"><span data-stu-id="78623-183">Indicates whether Wi-Fi endpoint uses an EAP based security type.</span></span> <span data-ttu-id="78623-184">Los valores posibles son: `open` y `wpaEnterprise`.</span><span class="sxs-lookup"><span data-stu-id="78623-184">Possible values are: `open`, `wpaEnterprise`.</span></span>|



## <a name="response"></a><span data-ttu-id="78623-185">Respuesta</span><span class="sxs-lookup"><span data-stu-id="78623-185">Response</span></span>
<span data-ttu-id="78623-186">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidWiFiConfiguration](../resources/intune-deviceconfig-androidwificonfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="78623-186">If successful, this method returns a `200 OK` response code and an updated [androidWiFiConfiguration](../resources/intune-deviceconfig-androidwificonfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="78623-187">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="78623-187">Example</span></span>
### <a name="request"></a><span data-ttu-id="78623-188">Solicitud</span><span class="sxs-lookup"><span data-stu-id="78623-188">Request</span></span>
<span data-ttu-id="78623-189">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="78623-189">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 436

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
  "wiFiSecurityType": "wpaEnterprise"
}
```

### <a name="response"></a><span data-ttu-id="78623-190">Respuesta</span><span class="sxs-lookup"><span data-stu-id="78623-190">Response</span></span>
<span data-ttu-id="78623-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="78623-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 607

{
  "@odata.type": "#microsoft.graph.androidWiFiConfiguration",
  "id": "51cfd26f-d26f-51cf-6fd2-cf516fd2cf51",
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






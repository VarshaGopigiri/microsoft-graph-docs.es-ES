---
title: Crear networkIPv4ConfigurationManagementCondition
description: Crear un nuevo objeto networkIPv4ConfigurationManagementCondition.
ms.openlocfilehash: f42bd52da9175192a71ed0be2b36f8f656f6a538
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090383"
---
# <a name="create-networkipv4configurationmanagementcondition"></a><span data-ttu-id="fbc82-103">Crear networkIPv4ConfigurationManagementCondition</span><span class="sxs-lookup"><span data-stu-id="fbc82-103">Create networkIPv4ConfigurationManagementCondition</span></span>

> <span data-ttu-id="fbc82-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fbc82-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fbc82-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fbc82-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="fbc82-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fbc82-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fbc82-107">Crear un nuevo objeto [networkIPv4ConfigurationManagementCondition](../resources/intune-fencing-networkipv4configurationmanagementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="fbc82-107">Create a new [networkIPv4ConfigurationManagementCondition](../resources/intune-fencing-networkipv4configurationmanagementcondition.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fbc82-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fbc82-108">Prerequisites</span></span>
<span data-ttu-id="fbc82-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fbc82-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fbc82-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fbc82-111">Permission type</span></span>|<span data-ttu-id="fbc82-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fbc82-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fbc82-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fbc82-113">Delegated (work or school account)</span></span>|<span data-ttu-id="fbc82-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fbc82-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="fbc82-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fbc82-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fbc82-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fbc82-116">Not supported.</span></span>|
|<span data-ttu-id="fbc82-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fbc82-117">Application</span></span>|<span data-ttu-id="fbc82-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fbc82-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fbc82-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fbc82-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/managementConditions
POST /deviceManagement/managementConditions/{managementConditionId}/managementConditionStatements/{managementConditionStatementId}/managementConditions
```

## <a name="request-headers"></a><span data-ttu-id="fbc82-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fbc82-120">Request headers</span></span>
|<span data-ttu-id="fbc82-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fbc82-121">Header</span></span>|<span data-ttu-id="fbc82-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fbc82-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fbc82-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="fbc82-123">Authorization</span></span>|<span data-ttu-id="fbc82-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fbc82-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fbc82-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="fbc82-125">Accept</span></span>|<span data-ttu-id="fbc82-126">application/json</span><span class="sxs-lookup"><span data-stu-id="fbc82-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fbc82-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fbc82-127">Request body</span></span>
<span data-ttu-id="fbc82-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto networkIPv4ConfigurationManagementCondition.</span><span class="sxs-lookup"><span data-stu-id="fbc82-128">In the request body, supply a JSON representation for the networkIPv4ConfigurationManagementCondition object.</span></span>

<span data-ttu-id="fbc82-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el networkIPv4ConfigurationManagementCondition.</span><span class="sxs-lookup"><span data-stu-id="fbc82-129">The following table shows the properties that are required when you create the networkIPv4ConfigurationManagementCondition.</span></span>

|<span data-ttu-id="fbc82-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fbc82-130">Property</span></span>|<span data-ttu-id="fbc82-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="fbc82-131">Type</span></span>|<span data-ttu-id="fbc82-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbc82-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fbc82-133">id</span><span class="sxs-lookup"><span data-stu-id="fbc82-133">id</span></span>|<span data-ttu-id="fbc82-134">String</span><span class="sxs-lookup"><span data-stu-id="fbc82-134">String</span></span>|<span data-ttu-id="fbc82-135">Identificador único de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="fbc82-135">Unique identifier for the management condition.</span></span> <span data-ttu-id="fbc82-136">Valor asignado al crear generada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="fbc82-136">System generated value assigned when created.</span></span> <span data-ttu-id="fbc82-137">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="fbc82-137">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="fbc82-138">uniqueName</span><span class="sxs-lookup"><span data-stu-id="fbc82-138">uniqueName</span></span>|<span data-ttu-id="fbc82-139">String</span><span class="sxs-lookup"><span data-stu-id="fbc82-139">String</span></span>|<span data-ttu-id="fbc82-140">Nombre único para la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="fbc82-140">Unique name for the management condition.</span></span> <span data-ttu-id="fbc82-141">Se usa en expresiones de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="fbc82-141">Used in management condition expressions.</span></span> <span data-ttu-id="fbc82-142">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="fbc82-142">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="fbc82-143">displayName</span><span class="sxs-lookup"><span data-stu-id="fbc82-143">displayName</span></span>|<span data-ttu-id="fbc82-144">String</span><span class="sxs-lookup"><span data-stu-id="fbc82-144">String</span></span>|<span data-ttu-id="fbc82-145">El nombre definido de administración de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="fbc82-145">The admin defined name of the management condition.</span></span> <span data-ttu-id="fbc82-146">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="fbc82-146">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="fbc82-147">descripción</span><span class="sxs-lookup"><span data-stu-id="fbc82-147">description</span></span>|<span data-ttu-id="fbc82-148">String</span><span class="sxs-lookup"><span data-stu-id="fbc82-148">String</span></span>|<span data-ttu-id="fbc82-149">El administrador define la descripción de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="fbc82-149">The admin defined description of the management condition.</span></span> <span data-ttu-id="fbc82-150">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="fbc82-150">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="fbc82-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="fbc82-151">createdDateTime</span></span>|<span data-ttu-id="fbc82-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fbc82-152">DateTimeOffset</span></span>|<span data-ttu-id="fbc82-153">La hora en que se creó la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="fbc82-153">The time the management condition was created.</span></span> <span data-ttu-id="fbc82-154">Servicio generado al lado.</span><span class="sxs-lookup"><span data-stu-id="fbc82-154">Generated service side.</span></span> <span data-ttu-id="fbc82-155">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="fbc82-155">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="fbc82-156">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="fbc82-156">modifiedDateTime</span></span>|<span data-ttu-id="fbc82-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fbc82-157">DateTimeOffset</span></span>|<span data-ttu-id="fbc82-158">La hora en que se modificó por última vez la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="fbc82-158">The time the management condition was last modified.</span></span> <span data-ttu-id="fbc82-159">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="fbc82-159">Updated service side.</span></span> <span data-ttu-id="fbc82-160">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="fbc82-160">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="fbc82-161">eTag</span><span class="sxs-lookup"><span data-stu-id="fbc82-161">eTag</span></span>|<span data-ttu-id="fbc82-162">String</span><span class="sxs-lookup"><span data-stu-id="fbc82-162">String</span></span>|<span data-ttu-id="fbc82-163">ETag de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="fbc82-163">ETag of the management condition.</span></span> <span data-ttu-id="fbc82-164">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="fbc82-164">Updated service side.</span></span> <span data-ttu-id="fbc82-165">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="fbc82-165">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="fbc82-166">applicablePlatforms</span><span class="sxs-lookup"><span data-stu-id="fbc82-166">applicablePlatforms</span></span>|<span data-ttu-id="fbc82-167">colección de [devicePlatformType](../resources/intune-shared-deviceplatformtype.md)</span><span class="sxs-lookup"><span data-stu-id="fbc82-167">[devicePlatformType](../resources/intune-shared-deviceplatformtype.md) collection</span></span>|<span data-ttu-id="fbc82-168">Las plataformas aplicables para esta condición de administración.</span><span class="sxs-lookup"><span data-stu-id="fbc82-168">The applicable platforms for this management condition.</span></span> <span data-ttu-id="fbc82-169">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md).</span><span class="sxs-lookup"><span data-stu-id="fbc82-169">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md).</span></span> <span data-ttu-id="fbc82-170">Los valores posibles son: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater` y `androidWorkProfile`.</span><span class="sxs-lookup"><span data-stu-id="fbc82-170">Possible values are: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`.</span></span>|
|<span data-ttu-id="fbc82-171">ipV4Prefix</span><span class="sxs-lookup"><span data-stu-id="fbc82-171">ipV4Prefix</span></span>|<span data-ttu-id="fbc82-172">String</span><span class="sxs-lookup"><span data-stu-id="fbc82-172">String</span></span>|<span data-ttu-id="fbc82-173">La subred IPv4 a estar conectado a.</span><span class="sxs-lookup"><span data-stu-id="fbc82-173">The IPv4 subnet to be connected to.</span></span> <span data-ttu-id="fbc82-174">Por ejemplo, 10.0.0.0/8</span><span class="sxs-lookup"><span data-stu-id="fbc82-174">e.g. 10.0.0.0/8</span></span>|
|<span data-ttu-id="fbc82-175">ipV4Gateway</span><span class="sxs-lookup"><span data-stu-id="fbc82-175">ipV4Gateway</span></span>|<span data-ttu-id="fbc82-176">String</span><span class="sxs-lookup"><span data-stu-id="fbc82-176">String</span></span>|<span data-ttu-id="fbc82-177">La dirección IPv4 de la puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="fbc82-177">The IPv4 gateway address.</span></span> <span data-ttu-id="fbc82-178">Por ejemplo, 10.0.0.0</span><span class="sxs-lookup"><span data-stu-id="fbc82-178">e.g. 10.0.0.0</span></span>|
|<span data-ttu-id="fbc82-179">ipV4DHCPServer</span><span class="sxs-lookup"><span data-stu-id="fbc82-179">ipV4DHCPServer</span></span>|<span data-ttu-id="fbc82-180">String</span><span class="sxs-lookup"><span data-stu-id="fbc82-180">String</span></span>|<span data-ttu-id="fbc82-181">La dirección IPv4 del servidor DHCP para el adaptador.</span><span class="sxs-lookup"><span data-stu-id="fbc82-181">The IPv4 address of the DHCP server for the adapter.</span></span>|
|<span data-ttu-id="fbc82-182">ipV4DNSServerList</span><span class="sxs-lookup"><span data-stu-id="fbc82-182">ipV4DNSServerList</span></span>|<span data-ttu-id="fbc82-183">Colección String</span><span class="sxs-lookup"><span data-stu-id="fbc82-183">String collection</span></span>|<span data-ttu-id="fbc82-184">Los servidores DNS de IPv4 configurados para el adaptador.</span><span class="sxs-lookup"><span data-stu-id="fbc82-184">The IPv4 DNS servers configured for the adapter.</span></span>|
|<span data-ttu-id="fbc82-185">dnsSuffixList</span><span class="sxs-lookup"><span data-stu-id="fbc82-185">dnsSuffixList</span></span>|<span data-ttu-id="fbc82-186">Colección String</span><span class="sxs-lookup"><span data-stu-id="fbc82-186">String collection</span></span>|<span data-ttu-id="fbc82-187">Sufijos DNS válidos para la red actual.</span><span class="sxs-lookup"><span data-stu-id="fbc82-187">Valid DNS suffixes for the current network.</span></span> <span data-ttu-id="fbc82-188">Por ejemplo, seattle.contoso.com</span><span class="sxs-lookup"><span data-stu-id="fbc82-188">e.g. seattle.contoso.com</span></span>|



## <a name="response"></a><span data-ttu-id="fbc82-189">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fbc82-189">Response</span></span>
<span data-ttu-id="fbc82-190">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [networkIPv4ConfigurationManagementCondition](../resources/intune-fencing-networkipv4configurationmanagementcondition.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fbc82-190">If successful, this method returns a `201 Created` response code and a [networkIPv4ConfigurationManagementCondition](../resources/intune-fencing-networkipv4configurationmanagementcondition.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fbc82-191">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fbc82-191">Example</span></span>
### <a name="request"></a><span data-ttu-id="fbc82-192">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fbc82-192">Request</span></span>
<span data-ttu-id="fbc82-193">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fbc82-193">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/managementConditions
Content-type: application/json
Content-length: 529

{
  "@odata.type": "#microsoft.graph.networkIPv4ConfigurationManagementCondition",
  "uniqueName": "Unique Name value",
  "displayName": "Display Name value",
  "description": "Description value",
  "eTag": "ETag value",
  "applicablePlatforms": [
    "androidForWork"
  ],
  "ipV4Prefix": "Ip V4Prefix value",
  "ipV4Gateway": "Ip V4Gateway value",
  "ipV4DHCPServer": "Ip V4DHCPServer value",
  "ipV4DNSServerList": [
    "Ip V4DNSServer List value"
  ],
  "dnsSuffixList": [
    "Dns Suffix List value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="fbc82-194">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fbc82-194">Response</span></span>
<span data-ttu-id="fbc82-p114">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fbc82-p114">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 697

{
  "@odata.type": "#microsoft.graph.networkIPv4ConfigurationManagementCondition",
  "id": "5e4a8284-8284-5e4a-8482-4a5e84824a5e",
  "uniqueName": "Unique Name value",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "modifiedDateTime": "2017-01-01T00:00:22.8983556-08:00",
  "eTag": "ETag value",
  "applicablePlatforms": [
    "androidForWork"
  ],
  "ipV4Prefix": "Ip V4Prefix value",
  "ipV4Gateway": "Ip V4Gateway value",
  "ipV4DHCPServer": "Ip V4DHCPServer value",
  "ipV4DNSServerList": [
    "Ip V4DNSServer List value"
  ],
  "dnsSuffixList": [
    "Dns Suffix List value"
  ]
}
```






---
title: Crear networkIPv6ConfigurationManagementCondition
description: Crear un nuevo objeto networkIPv6ConfigurationManagementCondition.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 1495bce9e7078061baa37ee840a5efbc3b39c911
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27947928"
---
# <a name="create-networkipv6configurationmanagementcondition"></a><span data-ttu-id="7bef2-103">Crear networkIPv6ConfigurationManagementCondition</span><span class="sxs-lookup"><span data-stu-id="7bef2-103">Create networkIPv6ConfigurationManagementCondition</span></span>

> <span data-ttu-id="7bef2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7bef2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7bef2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7bef2-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7bef2-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7bef2-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7bef2-107">Crear un nuevo objeto [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="7bef2-107">Create a new [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7bef2-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7bef2-108">Prerequisites</span></span>
<span data-ttu-id="7bef2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7bef2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7bef2-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7bef2-111">Permission type</span></span>|<span data-ttu-id="7bef2-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7bef2-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7bef2-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7bef2-113">Delegated (work or school account)</span></span>|<span data-ttu-id="7bef2-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7bef2-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="7bef2-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7bef2-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7bef2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7bef2-116">Not supported.</span></span>|
|<span data-ttu-id="7bef2-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7bef2-117">Application</span></span>|<span data-ttu-id="7bef2-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7bef2-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7bef2-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7bef2-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/managementConditions
POST /deviceManagement/managementConditions/{managementConditionId}/managementConditionStatements/{managementConditionStatementId}/managementConditions
```

## <a name="request-headers"></a><span data-ttu-id="7bef2-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7bef2-120">Request headers</span></span>
|<span data-ttu-id="7bef2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7bef2-121">Header</span></span>|<span data-ttu-id="7bef2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7bef2-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7bef2-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="7bef2-123">Authorization</span></span>|<span data-ttu-id="7bef2-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7bef2-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7bef2-125">Accept</span><span class="sxs-lookup"><span data-stu-id="7bef2-125">Accept</span></span>|<span data-ttu-id="7bef2-126">application/json</span><span class="sxs-lookup"><span data-stu-id="7bef2-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7bef2-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7bef2-127">Request body</span></span>
<span data-ttu-id="7bef2-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto networkIPv6ConfigurationManagementCondition.</span><span class="sxs-lookup"><span data-stu-id="7bef2-128">In the request body, supply a JSON representation for the networkIPv6ConfigurationManagementCondition object.</span></span>

<span data-ttu-id="7bef2-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el networkIPv6ConfigurationManagementCondition.</span><span class="sxs-lookup"><span data-stu-id="7bef2-129">The following table shows the properties that are required when you create the networkIPv6ConfigurationManagementCondition.</span></span>

|<span data-ttu-id="7bef2-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7bef2-130">Property</span></span>|<span data-ttu-id="7bef2-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bef2-131">Type</span></span>|<span data-ttu-id="7bef2-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bef2-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7bef2-133">id</span><span class="sxs-lookup"><span data-stu-id="7bef2-133">id</span></span>|<span data-ttu-id="7bef2-134">String</span><span class="sxs-lookup"><span data-stu-id="7bef2-134">String</span></span>|<span data-ttu-id="7bef2-135">Identificador único de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="7bef2-135">Unique identifier for the management condition.</span></span> <span data-ttu-id="7bef2-136">Valor asignado al crear generada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="7bef2-136">System generated value assigned when created.</span></span> <span data-ttu-id="7bef2-137">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="7bef2-137">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="7bef2-138">uniqueName</span><span class="sxs-lookup"><span data-stu-id="7bef2-138">uniqueName</span></span>|<span data-ttu-id="7bef2-139">String</span><span class="sxs-lookup"><span data-stu-id="7bef2-139">String</span></span>|<span data-ttu-id="7bef2-140">Nombre único para la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="7bef2-140">Unique name for the management condition.</span></span> <span data-ttu-id="7bef2-141">Se usa en expresiones de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="7bef2-141">Used in management condition expressions.</span></span> <span data-ttu-id="7bef2-142">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="7bef2-142">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="7bef2-143">displayName</span><span class="sxs-lookup"><span data-stu-id="7bef2-143">displayName</span></span>|<span data-ttu-id="7bef2-144">String</span><span class="sxs-lookup"><span data-stu-id="7bef2-144">String</span></span>|<span data-ttu-id="7bef2-145">El nombre definido de administración de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="7bef2-145">The admin defined name of the management condition.</span></span> <span data-ttu-id="7bef2-146">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="7bef2-146">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="7bef2-147">descripción</span><span class="sxs-lookup"><span data-stu-id="7bef2-147">description</span></span>|<span data-ttu-id="7bef2-148">String</span><span class="sxs-lookup"><span data-stu-id="7bef2-148">String</span></span>|<span data-ttu-id="7bef2-149">El administrador define la descripción de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="7bef2-149">The admin defined description of the management condition.</span></span> <span data-ttu-id="7bef2-150">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="7bef2-150">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="7bef2-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="7bef2-151">createdDateTime</span></span>|<span data-ttu-id="7bef2-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7bef2-152">DateTimeOffset</span></span>|<span data-ttu-id="7bef2-153">La hora en que se creó la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="7bef2-153">The time the management condition was created.</span></span> <span data-ttu-id="7bef2-154">Servicio generado al lado.</span><span class="sxs-lookup"><span data-stu-id="7bef2-154">Generated service side.</span></span> <span data-ttu-id="7bef2-155">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="7bef2-155">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="7bef2-156">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7bef2-156">modifiedDateTime</span></span>|<span data-ttu-id="7bef2-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7bef2-157">DateTimeOffset</span></span>|<span data-ttu-id="7bef2-158">La hora en que se modificó por última vez la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="7bef2-158">The time the management condition was last modified.</span></span> <span data-ttu-id="7bef2-159">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="7bef2-159">Updated service side.</span></span> <span data-ttu-id="7bef2-160">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="7bef2-160">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="7bef2-161">eTag</span><span class="sxs-lookup"><span data-stu-id="7bef2-161">eTag</span></span>|<span data-ttu-id="7bef2-162">String</span><span class="sxs-lookup"><span data-stu-id="7bef2-162">String</span></span>|<span data-ttu-id="7bef2-163">ETag de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="7bef2-163">ETag of the management condition.</span></span> <span data-ttu-id="7bef2-164">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="7bef2-164">Updated service side.</span></span> <span data-ttu-id="7bef2-165">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="7bef2-165">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="7bef2-166">applicablePlatforms</span><span class="sxs-lookup"><span data-stu-id="7bef2-166">applicablePlatforms</span></span>|<span data-ttu-id="7bef2-167">colección de [devicePlatformType](../resources/intune-shared-deviceplatformtype.md)</span><span class="sxs-lookup"><span data-stu-id="7bef2-167">[devicePlatformType](../resources/intune-shared-deviceplatformtype.md) collection</span></span>|<span data-ttu-id="7bef2-168">Las plataformas aplicables para esta condición de administración.</span><span class="sxs-lookup"><span data-stu-id="7bef2-168">The applicable platforms for this management condition.</span></span> <span data-ttu-id="7bef2-169">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md).</span><span class="sxs-lookup"><span data-stu-id="7bef2-169">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md).</span></span> <span data-ttu-id="7bef2-170">Los valores posibles son: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater` y `androidWorkProfile`.</span><span class="sxs-lookup"><span data-stu-id="7bef2-170">Possible values are: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`.</span></span>|
|<span data-ttu-id="7bef2-171">ipV6Prefix</span><span class="sxs-lookup"><span data-stu-id="7bef2-171">ipV6Prefix</span></span>|<span data-ttu-id="7bef2-172">String</span><span class="sxs-lookup"><span data-stu-id="7bef2-172">String</span></span>|<span data-ttu-id="7bef2-173">La subred IPv6 esté conectado al.</span><span class="sxs-lookup"><span data-stu-id="7bef2-173">The IPv6 subnet to be connected to.</span></span> <span data-ttu-id="7bef2-174">Por ejemplo, 2001:db8:: / 32</span><span class="sxs-lookup"><span data-stu-id="7bef2-174">e.g. 2001:db8::/32</span></span>|
|<span data-ttu-id="7bef2-175">ipV6Gateway</span><span class="sxs-lookup"><span data-stu-id="7bef2-175">ipV6Gateway</span></span>|<span data-ttu-id="7bef2-176">String</span><span class="sxs-lookup"><span data-stu-id="7bef2-176">String</span></span>|<span data-ttu-id="7bef2-177">La dirección de puerta de enlace de IPv6 para.</span><span class="sxs-lookup"><span data-stu-id="7bef2-177">The IPv6 gateway address to.</span></span> <span data-ttu-id="7bef2-178">Por ejemplo 2001:db8::1</span><span class="sxs-lookup"><span data-stu-id="7bef2-178">e.g 2001:db8::1</span></span>|
|<span data-ttu-id="7bef2-179">ipV6DNSServerList</span><span class="sxs-lookup"><span data-stu-id="7bef2-179">ipV6DNSServerList</span></span>|<span data-ttu-id="7bef2-180">Colección String</span><span class="sxs-lookup"><span data-stu-id="7bef2-180">String collection</span></span>|<span data-ttu-id="7bef2-181">Un servidores DNS IPv6 configurada para el adaptador.</span><span class="sxs-lookup"><span data-stu-id="7bef2-181">An IPv6 DNS servers configured for the adapter.</span></span>|
|<span data-ttu-id="7bef2-182">dnsSuffixList</span><span class="sxs-lookup"><span data-stu-id="7bef2-182">dnsSuffixList</span></span>|<span data-ttu-id="7bef2-183">Colección String</span><span class="sxs-lookup"><span data-stu-id="7bef2-183">String collection</span></span>|<span data-ttu-id="7bef2-184">Sufijos DNS válidos para la red actual.</span><span class="sxs-lookup"><span data-stu-id="7bef2-184">Valid DNS suffixes for the current network.</span></span> <span data-ttu-id="7bef2-185">Por ejemplo, seattle.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7bef2-185">e.g. seattle.contoso.com</span></span>|



## <a name="response"></a><span data-ttu-id="7bef2-186">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7bef2-186">Response</span></span>
<span data-ttu-id="7bef2-187">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7bef2-187">If successful, this method returns a `201 Created` response code and a [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7bef2-188">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7bef2-188">Example</span></span>
### <a name="request"></a><span data-ttu-id="7bef2-189">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7bef2-189">Request</span></span>
<span data-ttu-id="7bef2-190">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7bef2-190">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/managementConditions
Content-type: application/json
Content-length: 483

{
  "@odata.type": "#microsoft.graph.networkIPv6ConfigurationManagementCondition",
  "uniqueName": "Unique Name value",
  "displayName": "Display Name value",
  "description": "Description value",
  "eTag": "ETag value",
  "applicablePlatforms": [
    "androidForWork"
  ],
  "ipV6Prefix": "Ip V6Prefix value",
  "ipV6Gateway": "Ip V6Gateway value",
  "ipV6DNSServerList": [
    "Ip V6DNSServer List value"
  ],
  "dnsSuffixList": [
    "Dns Suffix List value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="7bef2-191">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7bef2-191">Response</span></span>
<span data-ttu-id="7bef2-p114">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7bef2-p114">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 651

{
  "@odata.type": "#microsoft.graph.networkIPv6ConfigurationManagementCondition",
  "id": "25811206-1206-2581-0612-812506128125",
  "uniqueName": "Unique Name value",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "modifiedDateTime": "2017-01-01T00:00:22.8983556-08:00",
  "eTag": "ETag value",
  "applicablePlatforms": [
    "androidForWork"
  ],
  "ipV6Prefix": "Ip V6Prefix value",
  "ipV6Gateway": "Ip V6Gateway value",
  "ipV6DNSServerList": [
    "Ip V6DNSServer List value"
  ],
  "dnsSuffixList": [
    "Dns Suffix List value"
  ]
}
```






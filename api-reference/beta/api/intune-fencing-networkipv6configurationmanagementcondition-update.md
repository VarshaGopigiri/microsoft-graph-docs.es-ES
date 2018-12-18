---
title: Actualizar networkIPv6ConfigurationManagementCondition
description: Actualizar las propiedades de un objeto networkIPv6ConfigurationManagementCondition.
author: tfitzmac
ms.openlocfilehash: 10014f1ddde4914b97f52e92901266e06ae07c99
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27357319"
---
# <a name="update-networkipv6configurationmanagementcondition"></a><span data-ttu-id="1d943-103">Actualizar networkIPv6ConfigurationManagementCondition</span><span class="sxs-lookup"><span data-stu-id="1d943-103">Update networkIPv6ConfigurationManagementCondition</span></span>

> <span data-ttu-id="1d943-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1d943-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1d943-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1d943-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1d943-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1d943-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1d943-107">Actualizar las propiedades de un objeto [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="1d943-107">Update the properties of a [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1d943-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1d943-108">Prerequisites</span></span>
<span data-ttu-id="1d943-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1d943-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1d943-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1d943-111">Permission type</span></span>|<span data-ttu-id="1d943-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1d943-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1d943-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1d943-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1d943-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1d943-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="1d943-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1d943-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1d943-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d943-116">Not supported.</span></span>|
|<span data-ttu-id="1d943-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1d943-117">Application</span></span>|<span data-ttu-id="1d943-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d943-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1d943-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1d943-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/managementConditions/{managementConditionId}
PATCH /deviceManagement/managementConditions/{managementConditionId}/managementConditionStatements/{managementConditionStatementId}/managementConditions/{managementConditionId}
```

## <a name="request-headers"></a><span data-ttu-id="1d943-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d943-120">Request headers</span></span>
|<span data-ttu-id="1d943-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d943-121">Header</span></span>|<span data-ttu-id="1d943-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1d943-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1d943-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="1d943-123">Authorization</span></span>|<span data-ttu-id="1d943-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1d943-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1d943-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1d943-125">Accept</span></span>|<span data-ttu-id="1d943-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1d943-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1d943-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1d943-127">Request body</span></span>
<span data-ttu-id="1d943-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="1d943-128">In the request body, supply a JSON representation for the [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md) object.</span></span>

<span data-ttu-id="1d943-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md).</span><span class="sxs-lookup"><span data-stu-id="1d943-129">The following table shows the properties that are required when you create the [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md).</span></span>

|<span data-ttu-id="1d943-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1d943-130">Property</span></span>|<span data-ttu-id="1d943-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d943-131">Type</span></span>|<span data-ttu-id="1d943-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d943-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1d943-133">id</span><span class="sxs-lookup"><span data-stu-id="1d943-133">id</span></span>|<span data-ttu-id="1d943-134">String</span><span class="sxs-lookup"><span data-stu-id="1d943-134">String</span></span>|<span data-ttu-id="1d943-135">Identificador único de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1d943-135">Unique identifier for the management condition.</span></span> <span data-ttu-id="1d943-136">Valor asignado al crear generada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="1d943-136">System generated value assigned when created.</span></span> <span data-ttu-id="1d943-137">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1d943-137">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="1d943-138">uniqueName</span><span class="sxs-lookup"><span data-stu-id="1d943-138">uniqueName</span></span>|<span data-ttu-id="1d943-139">String</span><span class="sxs-lookup"><span data-stu-id="1d943-139">String</span></span>|<span data-ttu-id="1d943-140">Nombre único para la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1d943-140">Unique name for the management condition.</span></span> <span data-ttu-id="1d943-141">Se usa en expresiones de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1d943-141">Used in management condition expressions.</span></span> <span data-ttu-id="1d943-142">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1d943-142">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="1d943-143">displayName</span><span class="sxs-lookup"><span data-stu-id="1d943-143">displayName</span></span>|<span data-ttu-id="1d943-144">String</span><span class="sxs-lookup"><span data-stu-id="1d943-144">String</span></span>|<span data-ttu-id="1d943-145">El nombre definido de administración de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1d943-145">The admin defined name of the management condition.</span></span> <span data-ttu-id="1d943-146">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1d943-146">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="1d943-147">descripción</span><span class="sxs-lookup"><span data-stu-id="1d943-147">description</span></span>|<span data-ttu-id="1d943-148">String</span><span class="sxs-lookup"><span data-stu-id="1d943-148">String</span></span>|<span data-ttu-id="1d943-149">El administrador define la descripción de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1d943-149">The admin defined description of the management condition.</span></span> <span data-ttu-id="1d943-150">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1d943-150">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="1d943-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="1d943-151">createdDateTime</span></span>|<span data-ttu-id="1d943-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1d943-152">DateTimeOffset</span></span>|<span data-ttu-id="1d943-153">La hora en que se creó la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1d943-153">The time the management condition was created.</span></span> <span data-ttu-id="1d943-154">Servicio generado al lado.</span><span class="sxs-lookup"><span data-stu-id="1d943-154">Generated service side.</span></span> <span data-ttu-id="1d943-155">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1d943-155">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="1d943-156">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="1d943-156">modifiedDateTime</span></span>|<span data-ttu-id="1d943-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1d943-157">DateTimeOffset</span></span>|<span data-ttu-id="1d943-158">La hora en que se modificó por última vez la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1d943-158">The time the management condition was last modified.</span></span> <span data-ttu-id="1d943-159">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="1d943-159">Updated service side.</span></span> <span data-ttu-id="1d943-160">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1d943-160">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="1d943-161">eTag</span><span class="sxs-lookup"><span data-stu-id="1d943-161">eTag</span></span>|<span data-ttu-id="1d943-162">String</span><span class="sxs-lookup"><span data-stu-id="1d943-162">String</span></span>|<span data-ttu-id="1d943-163">ETag de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1d943-163">ETag of the management condition.</span></span> <span data-ttu-id="1d943-164">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="1d943-164">Updated service side.</span></span> <span data-ttu-id="1d943-165">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1d943-165">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="1d943-166">applicablePlatforms</span><span class="sxs-lookup"><span data-stu-id="1d943-166">applicablePlatforms</span></span>|<span data-ttu-id="1d943-167">colección de [devicePlatformType](../resources/intune-shared-deviceplatformtype.md)</span><span class="sxs-lookup"><span data-stu-id="1d943-167">[devicePlatformType](../resources/intune-shared-deviceplatformtype.md) collection</span></span>|<span data-ttu-id="1d943-168">Las plataformas aplicables para esta condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1d943-168">The applicable platforms for this management condition.</span></span> <span data-ttu-id="1d943-169">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md).</span><span class="sxs-lookup"><span data-stu-id="1d943-169">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md).</span></span> <span data-ttu-id="1d943-170">Los valores posibles son: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater` y `androidWorkProfile`.</span><span class="sxs-lookup"><span data-stu-id="1d943-170">Possible values are: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`.</span></span>|
|<span data-ttu-id="1d943-171">ipV6Prefix</span><span class="sxs-lookup"><span data-stu-id="1d943-171">ipV6Prefix</span></span>|<span data-ttu-id="1d943-172">String</span><span class="sxs-lookup"><span data-stu-id="1d943-172">String</span></span>|<span data-ttu-id="1d943-173">La subred IPv6 esté conectado al.</span><span class="sxs-lookup"><span data-stu-id="1d943-173">The IPv6 subnet to be connected to.</span></span> <span data-ttu-id="1d943-174">Por ejemplo, 2001:db8:: / 32</span><span class="sxs-lookup"><span data-stu-id="1d943-174">e.g. 2001:db8::/32</span></span>|
|<span data-ttu-id="1d943-175">ipV6Gateway</span><span class="sxs-lookup"><span data-stu-id="1d943-175">ipV6Gateway</span></span>|<span data-ttu-id="1d943-176">String</span><span class="sxs-lookup"><span data-stu-id="1d943-176">String</span></span>|<span data-ttu-id="1d943-177">La dirección de puerta de enlace de IPv6 para.</span><span class="sxs-lookup"><span data-stu-id="1d943-177">The IPv6 gateway address to.</span></span> <span data-ttu-id="1d943-178">Por ejemplo 2001:db8::1</span><span class="sxs-lookup"><span data-stu-id="1d943-178">e.g 2001:db8::1</span></span>|
|<span data-ttu-id="1d943-179">ipV6DNSServerList</span><span class="sxs-lookup"><span data-stu-id="1d943-179">ipV6DNSServerList</span></span>|<span data-ttu-id="1d943-180">Colección String</span><span class="sxs-lookup"><span data-stu-id="1d943-180">String collection</span></span>|<span data-ttu-id="1d943-181">Un servidores DNS IPv6 configurada para el adaptador.</span><span class="sxs-lookup"><span data-stu-id="1d943-181">An IPv6 DNS servers configured for the adapter.</span></span>|
|<span data-ttu-id="1d943-182">dnsSuffixList</span><span class="sxs-lookup"><span data-stu-id="1d943-182">dnsSuffixList</span></span>|<span data-ttu-id="1d943-183">Colección String</span><span class="sxs-lookup"><span data-stu-id="1d943-183">String collection</span></span>|<span data-ttu-id="1d943-184">Sufijos DNS válidos para la red actual.</span><span class="sxs-lookup"><span data-stu-id="1d943-184">Valid DNS suffixes for the current network.</span></span> <span data-ttu-id="1d943-185">Por ejemplo, seattle.contoso.com</span><span class="sxs-lookup"><span data-stu-id="1d943-185">e.g. seattle.contoso.com</span></span>|



## <a name="response"></a><span data-ttu-id="1d943-186">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d943-186">Response</span></span>
<span data-ttu-id="1d943-187">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d943-187">If successful, this method returns a `200 OK` response code and an updated [networkIPv6ConfigurationManagementCondition](../resources/intune-fencing-networkipv6configurationmanagementcondition.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1d943-188">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d943-188">Example</span></span>
### <a name="request"></a><span data-ttu-id="1d943-189">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d943-189">Request</span></span>
<span data-ttu-id="1d943-190">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d943-190">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/managementConditions/{managementConditionId}
Content-type: application/json
Content-length: 401

{
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

### <a name="response"></a><span data-ttu-id="1d943-191">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d943-191">Response</span></span>
<span data-ttu-id="1d943-p114">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1d943-p114">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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






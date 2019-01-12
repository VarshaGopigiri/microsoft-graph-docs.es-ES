---
title: Obtener windowsDomainJoinConfiguration
description: Leer las propiedades y las relaciones del objeto windowsDomainJoinConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 64a295ae105a69865e304c45d08e339eadbf7936
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950245"
---
# <a name="get-windowsdomainjoinconfiguration"></a><span data-ttu-id="37a50-103">Obtener windowsDomainJoinConfiguration</span><span class="sxs-lookup"><span data-stu-id="37a50-103">Get windowsDomainJoinConfiguration</span></span>

> <span data-ttu-id="37a50-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="37a50-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="37a50-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="37a50-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="37a50-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="37a50-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="37a50-107">Leer las propiedades y las relaciones del objeto [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="37a50-107">Read properties and relationships of the [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="37a50-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="37a50-108">Prerequisites</span></span>

<span data-ttu-id="37a50-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="37a50-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="37a50-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="37a50-111">Permission type</span></span>|<span data-ttu-id="37a50-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="37a50-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="37a50-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="37a50-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="37a50-114">&nbsp; &nbsp; **Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="37a50-114">&nbsp; &nbsp; **Device configuration**</span></span> | <span data-ttu-id="37a50-115">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="37a50-115">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
| <span data-ttu-id="37a50-116">&nbsp; &nbsp; **Inscripción**</span><span class="sxs-lookup"><span data-stu-id="37a50-116">&nbsp; &nbsp; **Enrollment**</span></span> | <span data-ttu-id="37a50-117">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="37a50-117">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
|<span data-ttu-id="37a50-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="37a50-118">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="37a50-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="37a50-119">Not supported.</span></span>|
|<span data-ttu-id="37a50-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="37a50-120">Application</span></span>|<span data-ttu-id="37a50-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="37a50-121">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="37a50-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="37a50-122">HTTP Request</span></span>
<span data-ttu-id="37a50-123">**Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="37a50-123">**Device configuration**</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

<span data-ttu-id="37a50-124">**Inscripción**</span><span class="sxs-lookup"><span data-stu-id="37a50-124">**Enrollment**</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}/deploymentProfile/microsoft.graph.activeDirectoryWindowsAutopilotDeploymentProfile/domainJoinConfiguration
```

## <a name="optional-query-parameters"></a><span data-ttu-id="37a50-125">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="37a50-125">Optional query parameters</span></span>

<span data-ttu-id="37a50-126">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37a50-126">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="37a50-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="37a50-127">Request headers</span></span>

|<span data-ttu-id="37a50-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37a50-128">Header</span></span>|<span data-ttu-id="37a50-129">Valor</span><span class="sxs-lookup"><span data-stu-id="37a50-129">Value</span></span>|
|:---|:---|
|<span data-ttu-id="37a50-130">Autorización</span><span class="sxs-lookup"><span data-stu-id="37a50-130">Authorization</span></span>|<span data-ttu-id="37a50-131">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="37a50-131">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="37a50-132">Accept</span><span class="sxs-lookup"><span data-stu-id="37a50-132">Accept</span></span>|<span data-ttu-id="37a50-133">application/json</span><span class="sxs-lookup"><span data-stu-id="37a50-133">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="37a50-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="37a50-134">Request body</span></span>

<span data-ttu-id="37a50-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="37a50-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="37a50-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37a50-136">Response</span></span>

<span data-ttu-id="37a50-137">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37a50-137">If successful, this method returns a `200 OK` response code and [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="37a50-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="37a50-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="37a50-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="37a50-139">Request</span></span>

<span data-ttu-id="37a50-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="37a50-140">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="37a50-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37a50-141">Response</span></span>

<span data-ttu-id="37a50-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37a50-142">Here is an example of the response.</span></span> <span data-ttu-id="37a50-143">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="37a50-143">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="37a50-144">Las propiedades que devuelve una llamada real dependen del contexto.</span><span class="sxs-lookup"><span data-stu-id="37a50-144">Properties returned from an actual call depend on the context.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 560

{
  "value": {
    "@odata.type": "#microsoft.graph.windowsDomainJoinConfiguration",
    "id": "40118d08-8d08-4011-088d-1140088d1140",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "computerNameStaticPrefix": "Computer Name Static Prefix value",
    "computerNameSuffixRandomCharCount": 1,
    "activeDirectoryDomainName": "Active Directory Domain Name value"
  }
}
```




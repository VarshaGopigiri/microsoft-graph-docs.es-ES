---
title: Actualizar mobileAppProvisioningConfigGroupAssignment
description: Actualizar las propiedades de un objeto mobileAppProvisioningConfigGroupAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b341de06c1bd5d504e4835ebef8fce2aa3a5aac7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27848345"
---
# <a name="update-mobileappprovisioningconfiggroupassignment"></a><span data-ttu-id="6c997-103">Actualizar mobileAppProvisioningConfigGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="6c997-103">Update mobileAppProvisioningConfigGroupAssignment</span></span>

> <span data-ttu-id="6c997-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6c997-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6c997-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6c997-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6c997-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6c997-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6c997-107">Actualizar las propiedades de un objeto [mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="6c997-107">Update the properties of a [mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6c997-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6c997-108">Prerequisites</span></span>
<span data-ttu-id="6c997-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6c997-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6c997-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6c997-111">Permission type</span></span>|<span data-ttu-id="6c997-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6c997-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6c997-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6c997-113">Delegated (work or school account)</span></span>|<span data-ttu-id="6c997-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6c997-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="6c997-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6c997-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6c997-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6c997-116">Not supported.</span></span>|
|<span data-ttu-id="6c997-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6c997-117">Application</span></span>|<span data-ttu-id="6c997-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6c997-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6c997-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6c997-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/groupAssignments/{mobileAppProvisioningConfigGroupAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="6c997-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6c997-120">Request headers</span></span>
|<span data-ttu-id="6c997-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c997-121">Header</span></span>|<span data-ttu-id="6c997-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6c997-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6c997-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="6c997-123">Authorization</span></span>|<span data-ttu-id="6c997-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6c997-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6c997-125">Accept</span><span class="sxs-lookup"><span data-stu-id="6c997-125">Accept</span></span>|<span data-ttu-id="6c997-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6c997-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6c997-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6c997-127">Request body</span></span>
<span data-ttu-id="6c997-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="6c997-128">In the request body, supply a JSON representation for the [mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md) object.</span></span>

<span data-ttu-id="6c997-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md).</span><span class="sxs-lookup"><span data-stu-id="6c997-129">The following table shows the properties that are required when you create the [mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md).</span></span>

|<span data-ttu-id="6c997-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6c997-130">Property</span></span>|<span data-ttu-id="6c997-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c997-131">Type</span></span>|<span data-ttu-id="6c997-132">Description</span><span class="sxs-lookup"><span data-stu-id="6c997-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6c997-133">targetGroupId</span><span class="sxs-lookup"><span data-stu-id="6c997-133">targetGroupId</span></span>|<span data-ttu-id="6c997-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="6c997-134">String</span></span>|<span data-ttu-id="6c997-135">El identificador del grupo AAD en la que se refiere a la aplicación de configuración de aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="6c997-135">The ID of the AAD group in which the app provisioning configuration is being targeted.</span></span>|
|<span data-ttu-id="6c997-136">id</span><span class="sxs-lookup"><span data-stu-id="6c997-136">id</span></span>|<span data-ttu-id="6c997-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="6c997-137">String</span></span>|<span data-ttu-id="6c997-138">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6c997-138">Key of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="6c997-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c997-139">Response</span></span>
<span data-ttu-id="6c997-140">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6c997-140">If successful, this method returns a `200 OK` response code and an updated [mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6c997-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6c997-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="6c997-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6c997-142">Request</span></span>
<span data-ttu-id="6c997-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6c997-143">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/groupAssignments/{mobileAppProvisioningConfigGroupAssignmentId}
Content-type: application/json
Content-length: 48

{
  "targetGroupId": "Target Group Id value"
}
```

### <a name="response"></a><span data-ttu-id="6c997-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c997-144">Response</span></span>
<span data-ttu-id="6c997-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6c997-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 178

{
  "@odata.type": "#microsoft.graph.mobileAppProvisioningConfigGroupAssignment",
  "targetGroupId": "Target Group Id value",
  "id": "fad873e3-73e3-fad8-e373-d8fae373d8fa"
}
```






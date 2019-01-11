---
title: Crear mobileAppProvisioningConfigGroupAssignment
description: Crear un nuevo objeto mobileAppProvisioningConfigGroupAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 0cc03def8a3df440c1a4d98ee60dd30554a7086d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27838041"
---
# <a name="create-mobileappprovisioningconfiggroupassignment"></a><span data-ttu-id="8a99b-103">Crear mobileAppProvisioningConfigGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="8a99b-103">Create mobileAppProvisioningConfigGroupAssignment</span></span>

> <span data-ttu-id="8a99b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8a99b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8a99b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8a99b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8a99b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8a99b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8a99b-107">Crear un nuevo objeto [mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="8a99b-107">Create a new [mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8a99b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8a99b-108">Prerequisites</span></span>
<span data-ttu-id="8a99b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8a99b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8a99b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8a99b-111">Permission type</span></span>|<span data-ttu-id="8a99b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8a99b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8a99b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8a99b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8a99b-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8a99b-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="8a99b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8a99b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8a99b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8a99b-116">Not supported.</span></span>|
|<span data-ttu-id="8a99b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8a99b-117">Application</span></span>|<span data-ttu-id="8a99b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8a99b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8a99b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8a99b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/groupAssignments
```

## <a name="request-headers"></a><span data-ttu-id="8a99b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8a99b-120">Request headers</span></span>
|<span data-ttu-id="8a99b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a99b-121">Header</span></span>|<span data-ttu-id="8a99b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8a99b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8a99b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="8a99b-123">Authorization</span></span>|<span data-ttu-id="8a99b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8a99b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8a99b-125">Accept</span><span class="sxs-lookup"><span data-stu-id="8a99b-125">Accept</span></span>|<span data-ttu-id="8a99b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8a99b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8a99b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8a99b-127">Request body</span></span>
<span data-ttu-id="8a99b-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto mobileAppProvisioningConfigGroupAssignment.</span><span class="sxs-lookup"><span data-stu-id="8a99b-128">In the request body, supply a JSON representation for the mobileAppProvisioningConfigGroupAssignment object.</span></span>

<span data-ttu-id="8a99b-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el mobileAppProvisioningConfigGroupAssignment.</span><span class="sxs-lookup"><span data-stu-id="8a99b-129">The following table shows the properties that are required when you create the mobileAppProvisioningConfigGroupAssignment.</span></span>

|<span data-ttu-id="8a99b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8a99b-130">Property</span></span>|<span data-ttu-id="8a99b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a99b-131">Type</span></span>|<span data-ttu-id="8a99b-132">Description</span><span class="sxs-lookup"><span data-stu-id="8a99b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8a99b-133">targetGroupId</span><span class="sxs-lookup"><span data-stu-id="8a99b-133">targetGroupId</span></span>|<span data-ttu-id="8a99b-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a99b-134">String</span></span>|<span data-ttu-id="8a99b-135">El identificador del grupo AAD en la que se refiere a la aplicación de configuración de aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="8a99b-135">The ID of the AAD group in which the app provisioning configuration is being targeted.</span></span>|
|<span data-ttu-id="8a99b-136">id</span><span class="sxs-lookup"><span data-stu-id="8a99b-136">id</span></span>|<span data-ttu-id="8a99b-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a99b-137">String</span></span>|<span data-ttu-id="8a99b-138">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8a99b-138">Key of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="8a99b-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a99b-139">Response</span></span>
<span data-ttu-id="8a99b-140">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a99b-140">If successful, this method returns a `201 Created` response code and a [mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8a99b-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a99b-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="8a99b-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8a99b-142">Request</span></span>
<span data-ttu-id="8a99b-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8a99b-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/groupAssignments
Content-type: application/json
Content-length: 129

{
  "@odata.type": "#microsoft.graph.mobileAppProvisioningConfigGroupAssignment",
  "targetGroupId": "Target Group Id value"
}
```

### <a name="response"></a><span data-ttu-id="8a99b-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a99b-144">Response</span></span>
<span data-ttu-id="8a99b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8a99b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 178

{
  "@odata.type": "#microsoft.graph.mobileAppProvisioningConfigGroupAssignment",
  "targetGroupId": "Target Group Id value",
  "id": "fad873e3-73e3-fad8-e373-d8fae373d8fa"
}
```






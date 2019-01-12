---
title: asignar acción
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 245530ea687c6a0ead115ff74ec8fea9f90bde90
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27964224"
---
# <a name="assign-action"></a><span data-ttu-id="21b2f-103">asignar acción</span><span class="sxs-lookup"><span data-stu-id="21b2f-103">assign action</span></span>

> <span data-ttu-id="21b2f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="21b2f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="21b2f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="21b2f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="21b2f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="21b2f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="21b2f-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="21b2f-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="21b2f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="21b2f-108">Prerequisites</span></span>
<span data-ttu-id="21b2f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="21b2f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="21b2f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="21b2f-111">Permission type</span></span>|<span data-ttu-id="21b2f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="21b2f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="21b2f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="21b2f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="21b2f-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="21b2f-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="21b2f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="21b2f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="21b2f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="21b2f-116">Not supported.</span></span>|
|<span data-ttu-id="21b2f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="21b2f-117">Application</span></span>|<span data-ttu-id="21b2f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="21b2f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="21b2f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="21b2f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="21b2f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="21b2f-120">Request headers</span></span>
|<span data-ttu-id="21b2f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21b2f-121">Header</span></span>|<span data-ttu-id="21b2f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="21b2f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="21b2f-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="21b2f-123">Authorization</span></span>|<span data-ttu-id="21b2f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="21b2f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="21b2f-125">Accept</span><span class="sxs-lookup"><span data-stu-id="21b2f-125">Accept</span></span>|<span data-ttu-id="21b2f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="21b2f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="21b2f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="21b2f-127">Request body</span></span>
<span data-ttu-id="21b2f-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="21b2f-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="21b2f-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="21b2f-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="21b2f-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="21b2f-130">Property</span></span>|<span data-ttu-id="21b2f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="21b2f-131">Type</span></span>|<span data-ttu-id="21b2f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="21b2f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="21b2f-133">appProvisioningConfigurationGroupAssignments</span><span class="sxs-lookup"><span data-stu-id="21b2f-133">appProvisioningConfigurationGroupAssignments</span></span>|<span data-ttu-id="21b2f-134">colección de [mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md)</span><span class="sxs-lookup"><span data-stu-id="21b2f-134">[mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md) collection</span></span>|<span data-ttu-id="21b2f-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="21b2f-135">Not yet documented</span></span>|
|<span data-ttu-id="21b2f-136">iOSLobAppProvisioningConfigAssignments</span><span class="sxs-lookup"><span data-stu-id="21b2f-136">iOSLobAppProvisioningConfigAssignments</span></span>|<span data-ttu-id="21b2f-137">colección de [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="21b2f-137">[iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) collection</span></span>|<span data-ttu-id="21b2f-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="21b2f-138">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="21b2f-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21b2f-139">Response</span></span>
<span data-ttu-id="21b2f-140">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="21b2f-140">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="21b2f-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="21b2f-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="21b2f-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="21b2f-142">Request</span></span>
<span data-ttu-id="21b2f-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="21b2f-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/assign

Content-type: application/json
Content-length: 578

{
  "appProvisioningConfigurationGroupAssignments": [
    {
      "@odata.type": "#microsoft.graph.mobileAppProvisioningConfigGroupAssignment",
      "targetGroupId": "Target Group Id value",
      "id": "fad873e3-73e3-fad8-e373-d8fae373d8fa"
    }
  ],
  "iOSLobAppProvisioningConfigAssignments": [
    {
      "@odata.type": "#microsoft.graph.iosLobAppProvisioningConfigurationAssignment",
      "id": "eac7008e-008e-eac7-8e00-c7ea8e00c7ea",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="21b2f-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21b2f-144">Response</span></span>
<span data-ttu-id="21b2f-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="21b2f-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```






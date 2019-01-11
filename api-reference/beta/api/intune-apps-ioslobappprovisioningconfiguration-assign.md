---
title: asignar acción
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7b7f92592a0ece8169b4f4148e71df5b6297ca7a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824413"
---
# <a name="assign-action"></a><span data-ttu-id="9c0f0-103">asignar acción</span><span class="sxs-lookup"><span data-stu-id="9c0f0-103">assign action</span></span>

> <span data-ttu-id="9c0f0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9c0f0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9c0f0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9c0f0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9c0f0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9c0f0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9c0f0-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9c0f0-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9c0f0-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9c0f0-108">Prerequisites</span></span>
<span data-ttu-id="9c0f0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9c0f0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9c0f0-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9c0f0-111">Permission type</span></span>|<span data-ttu-id="9c0f0-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9c0f0-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9c0f0-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9c0f0-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9c0f0-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9c0f0-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="9c0f0-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9c0f0-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9c0f0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9c0f0-116">Not supported.</span></span>|
|<span data-ttu-id="9c0f0-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9c0f0-117">Application</span></span>|<span data-ttu-id="9c0f0-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9c0f0-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9c0f0-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9c0f0-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="9c0f0-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9c0f0-120">Request headers</span></span>
|<span data-ttu-id="9c0f0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c0f0-121">Header</span></span>|<span data-ttu-id="9c0f0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9c0f0-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9c0f0-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="9c0f0-123">Authorization</span></span>|<span data-ttu-id="9c0f0-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9c0f0-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9c0f0-125">Accept</span><span class="sxs-lookup"><span data-stu-id="9c0f0-125">Accept</span></span>|<span data-ttu-id="9c0f0-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9c0f0-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9c0f0-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9c0f0-127">Request body</span></span>
<span data-ttu-id="9c0f0-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="9c0f0-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="9c0f0-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="9c0f0-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="9c0f0-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9c0f0-130">Property</span></span>|<span data-ttu-id="9c0f0-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c0f0-131">Type</span></span>|<span data-ttu-id="9c0f0-132">Description</span><span class="sxs-lookup"><span data-stu-id="9c0f0-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9c0f0-133">appProvisioningConfigurationGroupAssignments</span><span class="sxs-lookup"><span data-stu-id="9c0f0-133">appProvisioningConfigurationGroupAssignments</span></span>|<span data-ttu-id="9c0f0-134">colección de [mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md)</span><span class="sxs-lookup"><span data-stu-id="9c0f0-134">[mobileAppProvisioningConfigGroupAssignment](../resources/intune-apps-mobileappprovisioningconfiggroupassignment.md) collection</span></span>|<span data-ttu-id="9c0f0-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9c0f0-135">Not yet documented</span></span>|
|<span data-ttu-id="9c0f0-136">iOSLobAppProvisioningConfigAssignments</span><span class="sxs-lookup"><span data-stu-id="9c0f0-136">iOSLobAppProvisioningConfigAssignments</span></span>|<span data-ttu-id="9c0f0-137">colección de [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="9c0f0-137">[iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) collection</span></span>|<span data-ttu-id="9c0f0-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9c0f0-138">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="9c0f0-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c0f0-139">Response</span></span>
<span data-ttu-id="9c0f0-140">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="9c0f0-140">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="9c0f0-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9c0f0-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="9c0f0-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9c0f0-142">Request</span></span>
<span data-ttu-id="9c0f0-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9c0f0-143">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="9c0f0-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c0f0-144">Response</span></span>
<span data-ttu-id="9c0f0-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9c0f0-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```






---
title: Lista iosLobAppProvisioningConfigurationAssignments
description: Propiedades de la lista y relaciones de los objetos iosLobAppProvisioningConfigurationAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 41230396c73ac1682b639488da733a497381e017
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823880"
---
# <a name="list-ioslobappprovisioningconfigurationassignments"></a><span data-ttu-id="e9cf1-103">Lista iosLobAppProvisioningConfigurationAssignments</span><span class="sxs-lookup"><span data-stu-id="e9cf1-103">List iosLobAppProvisioningConfigurationAssignments</span></span>

> <span data-ttu-id="e9cf1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e9cf1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e9cf1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e9cf1-107">Propiedades de la lista y relaciones de los objetos [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="e9cf1-107">List properties and relationships of the [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e9cf1-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e9cf1-108">Prerequisites</span></span>
<span data-ttu-id="e9cf1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e9cf1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e9cf1-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e9cf1-111">Permission type</span></span>|<span data-ttu-id="e9cf1-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e9cf1-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e9cf1-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e9cf1-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e9cf1-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="e9cf1-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="e9cf1-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e9cf1-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e9cf1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-116">Not supported.</span></span>|
|<span data-ttu-id="e9cf1-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e9cf1-117">Application</span></span>|<span data-ttu-id="e9cf1-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e9cf1-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e9cf1-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="e9cf1-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9cf1-120">Request headers</span></span>
|<span data-ttu-id="e9cf1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9cf1-121">Header</span></span>|<span data-ttu-id="e9cf1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e9cf1-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e9cf1-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e9cf1-123">Authorization</span></span>|<span data-ttu-id="e9cf1-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e9cf1-125">Accept</span><span class="sxs-lookup"><span data-stu-id="e9cf1-125">Accept</span></span>|<span data-ttu-id="e9cf1-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e9cf1-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e9cf1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e9cf1-127">Request body</span></span>
<span data-ttu-id="e9cf1-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e9cf1-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9cf1-129">Response</span></span>
<span data-ttu-id="e9cf1-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-130">If successful, this method returns a `200 OK` response code and a collection of [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e9cf1-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e9cf1-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="e9cf1-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9cf1-132">Request</span></span>
<span data-ttu-id="e9cf1-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/assignments
```

### <a name="response"></a><span data-ttu-id="e9cf1-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9cf1-134">Response</span></span>
<span data-ttu-id="e9cf1-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 286

{
  "value": [
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






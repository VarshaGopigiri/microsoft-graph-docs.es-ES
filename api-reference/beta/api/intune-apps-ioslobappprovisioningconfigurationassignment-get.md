---
title: Obtener iosLobAppProvisioningConfigurationAssignment
description: Leer las propiedades y las relaciones del objeto iosLobAppProvisioningConfigurationAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 4755bab0c834c9a44a5ff1598f1b193920d5b90a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823873"
---
# <a name="get-ioslobappprovisioningconfigurationassignment"></a><span data-ttu-id="1d238-103">Obtener iosLobAppProvisioningConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="1d238-103">Get iosLobAppProvisioningConfigurationAssignment</span></span>

> <span data-ttu-id="1d238-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1d238-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1d238-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1d238-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1d238-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1d238-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1d238-107">Leer las propiedades y las relaciones del objeto [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="1d238-107">Read properties and relationships of the [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1d238-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1d238-108">Prerequisites</span></span>
<span data-ttu-id="1d238-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1d238-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1d238-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1d238-111">Permission type</span></span>|<span data-ttu-id="1d238-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1d238-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1d238-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1d238-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1d238-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="1d238-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="1d238-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1d238-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1d238-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d238-116">Not supported.</span></span>|
|<span data-ttu-id="1d238-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1d238-117">Application</span></span>|<span data-ttu-id="1d238-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d238-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1d238-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1d238-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/assignments/{iosLobAppProvisioningConfigurationAssignmentId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="1d238-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1d238-120">Optional query parameters</span></span>
<span data-ttu-id="1d238-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d238-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="1d238-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d238-122">Request headers</span></span>
|<span data-ttu-id="1d238-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d238-123">Header</span></span>|<span data-ttu-id="1d238-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1d238-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1d238-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="1d238-125">Authorization</span></span>|<span data-ttu-id="1d238-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1d238-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1d238-127">Accept</span><span class="sxs-lookup"><span data-stu-id="1d238-127">Accept</span></span>|<span data-ttu-id="1d238-128">application/json</span><span class="sxs-lookup"><span data-stu-id="1d238-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1d238-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1d238-129">Request body</span></span>
<span data-ttu-id="1d238-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1d238-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1d238-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d238-131">Response</span></span>
<span data-ttu-id="1d238-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d238-132">If successful, this method returns a `200 OK` response code and [iosLobAppProvisioningConfigurationAssignment](../resources/intune-apps-ioslobappprovisioningconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1d238-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d238-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="1d238-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d238-134">Request</span></span>
<span data-ttu-id="1d238-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d238-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/assignments/{iosLobAppProvisioningConfigurationAssignmentId}
```

### <a name="response"></a><span data-ttu-id="1d238-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d238-136">Response</span></span>
<span data-ttu-id="1d238-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1d238-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 262

{
  "value": {
    "@odata.type": "#microsoft.graph.iosLobAppProvisioningConfigurationAssignment",
    "id": "eac7008e-008e-eac7-8e00-c7ea8e00c7ea",
    "target": {
      "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
    }
  }
}
```






---
title: Obtener deviceConfigurationUserStateSummary
description: Leer las propiedades y las relaciones del objeto deviceConfigurationUserStateSummary.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ea78f50e0b957222371989ba07bea520df6546fc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933361"
---
# <a name="get-deviceconfigurationuserstatesummary"></a><span data-ttu-id="bc631-103">Obtener deviceConfigurationUserStateSummary</span><span class="sxs-lookup"><span data-stu-id="bc631-103">Get deviceConfigurationUserStateSummary</span></span>

> <span data-ttu-id="bc631-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bc631-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bc631-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bc631-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bc631-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bc631-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bc631-107">Leer las propiedades y las relaciones del objeto [deviceConfigurationUserStateSummary](../resources/intune-deviceconfig-deviceconfigurationuserstatesummary.md) .</span><span class="sxs-lookup"><span data-stu-id="bc631-107">Read properties and relationships of the [deviceConfigurationUserStateSummary](../resources/intune-deviceconfig-deviceconfigurationuserstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bc631-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bc631-108">Prerequisites</span></span>
<span data-ttu-id="bc631-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bc631-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bc631-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bc631-111">Permission type</span></span>|<span data-ttu-id="bc631-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bc631-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bc631-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bc631-113">Delegated (work or school account)</span></span>|<span data-ttu-id="bc631-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="bc631-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="bc631-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bc631-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bc631-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc631-116">Not supported.</span></span>|
|<span data-ttu-id="bc631-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bc631-117">Application</span></span>|<span data-ttu-id="bc631-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc631-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bc631-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bc631-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurationUserStateSummaries
```

## <a name="optional-query-parameters"></a><span data-ttu-id="bc631-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bc631-120">Optional query parameters</span></span>
<span data-ttu-id="bc631-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc631-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="bc631-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bc631-122">Request headers</span></span>
|<span data-ttu-id="bc631-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc631-123">Header</span></span>|<span data-ttu-id="bc631-124">Valor</span><span class="sxs-lookup"><span data-stu-id="bc631-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bc631-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="bc631-125">Authorization</span></span>|<span data-ttu-id="bc631-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bc631-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bc631-127">Accept</span><span class="sxs-lookup"><span data-stu-id="bc631-127">Accept</span></span>|<span data-ttu-id="bc631-128">application/json</span><span class="sxs-lookup"><span data-stu-id="bc631-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bc631-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bc631-129">Request body</span></span>
<span data-ttu-id="bc631-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bc631-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bc631-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc631-131">Response</span></span>
<span data-ttu-id="bc631-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [deviceConfigurationUserStateSummary](../resources/intune-deviceconfig-deviceconfigurationuserstatesummary.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc631-132">If successful, this method returns a `200 OK` response code and [deviceConfigurationUserStateSummary](../resources/intune-deviceconfig-deviceconfigurationuserstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bc631-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bc631-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="bc631-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bc631-134">Request</span></span>
<span data-ttu-id="bc631-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bc631-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurationUserStateSummaries
```

### <a name="response"></a><span data-ttu-id="bc631-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc631-136">Response</span></span>
<span data-ttu-id="bc631-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bc631-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 361

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceConfigurationUserStateSummary",
    "id": "e8957887-7887-e895-8778-95e8877895e8",
    "unknownUserCount": 0,
    "notApplicableUserCount": 6,
    "compliantUserCount": 2,
    "remediatedUserCount": 3,
    "nonCompliantUserCount": 5,
    "errorUserCount": 14,
    "conflictUserCount": 1
  }
}
```






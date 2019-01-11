---
title: Obtener deviceConfigurationDeviceStateSummary
description: Lea las propiedades y las relaciones del objeto deviceConfigurationDeviceStateSummary.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 34941c4608a2aa734ed408e0467c252a08847a24
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27827961"
---
# <a name="get-deviceconfigurationdevicestatesummary"></a><span data-ttu-id="57367-103">Obtener deviceConfigurationDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="57367-103">Get deviceConfigurationDeviceStateSummary</span></span>

> <span data-ttu-id="57367-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="57367-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="57367-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="57367-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="57367-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="57367-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="57367-107">Lea las propiedades y las relaciones del objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="57367-107">Read properties and relationships of the [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="57367-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="57367-108">Prerequisites</span></span>
<span data-ttu-id="57367-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="57367-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="57367-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="57367-111">Permission type</span></span>|<span data-ttu-id="57367-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="57367-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="57367-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="57367-113">Delegated (work or school account)</span></span>|<span data-ttu-id="57367-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="57367-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="57367-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="57367-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="57367-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="57367-116">Not supported.</span></span>|
|<span data-ttu-id="57367-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="57367-117">Application</span></span>|<span data-ttu-id="57367-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="57367-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="57367-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="57367-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurationDeviceStateSummaries
```

## <a name="optional-query-parameters"></a><span data-ttu-id="57367-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="57367-120">Optional query parameters</span></span>
<span data-ttu-id="57367-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="57367-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="57367-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="57367-122">Request headers</span></span>
|<span data-ttu-id="57367-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57367-123">Header</span></span>|<span data-ttu-id="57367-124">Valor</span><span class="sxs-lookup"><span data-stu-id="57367-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="57367-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="57367-125">Authorization</span></span>|<span data-ttu-id="57367-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="57367-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="57367-127">Accept</span><span class="sxs-lookup"><span data-stu-id="57367-127">Accept</span></span>|<span data-ttu-id="57367-128">application/json</span><span class="sxs-lookup"><span data-stu-id="57367-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="57367-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="57367-129">Request body</span></span>
<span data-ttu-id="57367-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="57367-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="57367-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="57367-131">Response</span></span>
<span data-ttu-id="57367-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="57367-132">If successful, this method returns a `200 OK` response code and [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="57367-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="57367-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="57367-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="57367-134">Request</span></span>
<span data-ttu-id="57367-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="57367-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurationDeviceStateSummaries
```

### <a name="response"></a><span data-ttu-id="57367-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="57367-136">Response</span></span>
<span data-ttu-id="57367-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="57367-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 376

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStateSummary",
    "id": "5db26f5a-6f5a-5db2-5a6f-b25d5a6fb25d",
    "unknownDeviceCount": 2,
    "notApplicableDeviceCount": 8,
    "compliantDeviceCount": 4,
    "remediatedDeviceCount": 5,
    "nonCompliantDeviceCount": 7,
    "errorDeviceCount": 0,
    "conflictDeviceCount": 3
  }
}
```






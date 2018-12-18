---
title: Obtener deviceComplianceUserOverview
description: Lea las propiedades y las relaciones del objeto deviceComplianceUserOverview.
author: tfitzmac
ms.openlocfilehash: 38eccb78c8f40e356a41de3f54a411294ac6c321
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27327520"
---
# <a name="get-devicecomplianceuseroverview"></a><span data-ttu-id="07993-103">Obtener deviceComplianceUserOverview</span><span class="sxs-lookup"><span data-stu-id="07993-103">Get deviceComplianceUserOverview</span></span>

> <span data-ttu-id="07993-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="07993-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="07993-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="07993-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="07993-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="07993-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="07993-107">Lea las propiedades y las relaciones del objeto [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md).</span><span class="sxs-lookup"><span data-stu-id="07993-107">Read properties and relationships of the [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="07993-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="07993-108">Prerequisites</span></span>
<span data-ttu-id="07993-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="07993-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="07993-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="07993-111">Permission type</span></span>|<span data-ttu-id="07993-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="07993-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="07993-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="07993-113">Delegated (work or school account)</span></span>|<span data-ttu-id="07993-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="07993-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="07993-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="07993-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="07993-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="07993-116">Not supported.</span></span>|
|<span data-ttu-id="07993-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="07993-117">Application</span></span>|<span data-ttu-id="07993-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="07993-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="07993-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="07993-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/userStatusOverview
```

## <a name="optional-query-parameters"></a><span data-ttu-id="07993-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="07993-120">Optional query parameters</span></span>
<span data-ttu-id="07993-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="07993-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="07993-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="07993-122">Request headers</span></span>
|<span data-ttu-id="07993-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07993-123">Header</span></span>|<span data-ttu-id="07993-124">Valor</span><span class="sxs-lookup"><span data-stu-id="07993-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="07993-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="07993-125">Authorization</span></span>|<span data-ttu-id="07993-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="07993-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="07993-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="07993-127">Accept</span></span>|<span data-ttu-id="07993-128">application/json</span><span class="sxs-lookup"><span data-stu-id="07993-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="07993-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="07993-129">Request body</span></span>
<span data-ttu-id="07993-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="07993-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="07993-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="07993-131">Response</span></span>
<span data-ttu-id="07993-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="07993-132">If successful, this method returns a `200 OK` response code and [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="07993-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="07993-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="07993-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="07993-134">Request</span></span>
<span data-ttu-id="07993-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="07993-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/userStatusOverview
```

### <a name="response"></a><span data-ttu-id="07993-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="07993-136">Response</span></span>
<span data-ttu-id="07993-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="07993-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 391

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceComplianceUserOverview",
    "id": "2d4f5bf4-5bf4-2d4f-f45b-4f2df45b4f2d",
    "pendingCount": 12,
    "notApplicableCount": 2,
    "successCount": 12,
    "errorCount": 10,
    "failedCount": 11,
    "conflictCount": 13,
    "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
    "configurationVersion": 4
  }
}
```






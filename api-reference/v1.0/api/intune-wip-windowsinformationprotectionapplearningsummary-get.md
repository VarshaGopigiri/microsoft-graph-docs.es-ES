---
title: Obtener windowsInformationProtectionAppLearningSummary
description: Lea las propiedades y las relaciones del objeto windowsInformationProtectionAppLearningSummary.
ms.openlocfilehash: 48031664a5a8a1351a51f32fe94f9c071e79f918
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031190"
---
# <a name="get-windowsinformationprotectionapplearningsummary"></a><span data-ttu-id="8c1ab-103">Obtener windowsInformationProtectionAppLearningSummary</span><span class="sxs-lookup"><span data-stu-id="8c1ab-103">Get windowsInformationProtectionAppLearningSummary</span></span>

> <span data-ttu-id="8c1ab-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8c1ab-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8c1ab-105">Lea las propiedades y las relaciones del objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="8c1ab-105">Read properties and relationships of the [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8c1ab-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8c1ab-106">Prerequisites</span></span>
<span data-ttu-id="8c1ab-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8c1ab-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8c1ab-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8c1ab-109">Permission type</span></span>|<span data-ttu-id="8c1ab-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8c1ab-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8c1ab-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8c1ab-111">Delegated (work or school account)</span></span>|<span data-ttu-id="8c1ab-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="8c1ab-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="8c1ab-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8c1ab-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8c1ab-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8c1ab-114">Not supported.</span></span>|
|<span data-ttu-id="8c1ab-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8c1ab-115">Application</span></span>|<span data-ttu-id="8c1ab-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8c1ab-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8c1ab-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8c1ab-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/windowsInformationProtectionAppLearningSummaries/{windowsInformationProtectionAppLearningSummaryId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="8c1ab-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="8c1ab-118">Optional query parameters</span></span>
<span data-ttu-id="8c1ab-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8c1ab-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="8c1ab-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8c1ab-120">Request headers</span></span>
|<span data-ttu-id="8c1ab-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c1ab-121">Header</span></span>|<span data-ttu-id="8c1ab-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8c1ab-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8c1ab-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="8c1ab-123">Authorization</span></span>|<span data-ttu-id="8c1ab-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8c1ab-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8c1ab-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8c1ab-125">Accept</span></span>|<span data-ttu-id="8c1ab-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8c1ab-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8c1ab-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8c1ab-127">Request body</span></span>
<span data-ttu-id="8c1ab-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8c1ab-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8c1ab-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c1ab-129">Response</span></span>
<span data-ttu-id="8c1ab-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8c1ab-130">If successful, this method returns a `200 OK` response code and [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8c1ab-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8c1ab-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="8c1ab-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8c1ab-132">Request</span></span>
<span data-ttu-id="8c1ab-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8c1ab-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/windowsInformationProtectionAppLearningSummaries/{windowsInformationProtectionAppLearningSummaryId}
```

### <a name="response"></a><span data-ttu-id="8c1ab-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c1ab-134">Response</span></span>
<span data-ttu-id="8c1ab-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8c1ab-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 269

{
  "value": {
    "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLearningSummary",
    "id": "063baf50-af50-063b-50af-3b0650af3b06",
    "applicationName": "Application Name value",
    "applicationType": "desktop",
    "deviceCount": 11
  }
}
```




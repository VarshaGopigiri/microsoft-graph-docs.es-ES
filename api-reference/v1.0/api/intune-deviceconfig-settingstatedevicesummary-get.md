---
title: Obtener settingStateDeviceSummary
description: Lea las propiedades y las relaciones del objeto settingStateDeviceSummary.
author: tfitzmac
ms.openlocfilehash: 9e05165849e52b819b154597c53fb49865e4ab72
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27359314"
---
# <a name="get-settingstatedevicesummary"></a><span data-ttu-id="0ce31-103">Obtener settingStateDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="0ce31-103">Get settingStateDeviceSummary</span></span>

> <span data-ttu-id="0ce31-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0ce31-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0ce31-105">Lea las propiedades y las relaciones del objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="0ce31-105">Read properties and relationships of the [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0ce31-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0ce31-106">Prerequisites</span></span>
<span data-ttu-id="0ce31-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0ce31-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0ce31-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0ce31-109">Permission type</span></span>|<span data-ttu-id="0ce31-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0ce31-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0ce31-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0ce31-111">Delegated (work or school account)</span></span>|<span data-ttu-id="0ce31-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="0ce31-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="0ce31-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0ce31-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0ce31-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0ce31-114">Not supported.</span></span>|
|<span data-ttu-id="0ce31-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0ce31-115">Application</span></span>|<span data-ttu-id="0ce31-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0ce31-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0ce31-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0ce31-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="0ce31-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0ce31-118">Optional query parameters</span></span>
<span data-ttu-id="0ce31-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0ce31-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="0ce31-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0ce31-120">Request headers</span></span>
|<span data-ttu-id="0ce31-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ce31-121">Header</span></span>|<span data-ttu-id="0ce31-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0ce31-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0ce31-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="0ce31-123">Authorization</span></span>|<span data-ttu-id="0ce31-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0ce31-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0ce31-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0ce31-125">Accept</span></span>|<span data-ttu-id="0ce31-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0ce31-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0ce31-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0ce31-127">Request body</span></span>
<span data-ttu-id="0ce31-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0ce31-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0ce31-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0ce31-129">Response</span></span>
<span data-ttu-id="0ce31-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0ce31-130">If successful, this method returns a `200 OK` response code and [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0ce31-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0ce31-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="0ce31-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0ce31-132">Request</span></span>
<span data-ttu-id="0ce31-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0ce31-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
```

### <a name="response"></a><span data-ttu-id="0ce31-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0ce31-134">Response</span></span>
<span data-ttu-id="0ce31-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0ce31-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 450

{
  "value": {
    "@odata.type": "#microsoft.graph.settingStateDeviceSummary",
    "id": "3e2d4526-4526-3e2d-2645-2d3e26452d3e",
    "settingName": "Setting Name value",
    "instancePath": "Instance Path value",
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




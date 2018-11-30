---
title: Obtener deviceCompliancePolicySettingStateSummary
description: Lea las propiedades y las relaciones del objeto deviceCompliancePolicySettingStateSummary.
ms.openlocfilehash: f8a4e819cdbaf1986b2f99d48a6822f4da6bf10b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028568"
---
# <a name="get-devicecompliancepolicysettingstatesummary"></a><span data-ttu-id="d2552-103">Obtener deviceCompliancePolicySettingStateSummary</span><span class="sxs-lookup"><span data-stu-id="d2552-103">Get deviceCompliancePolicySettingStateSummary</span></span>

> <span data-ttu-id="d2552-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d2552-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d2552-105">Lea las propiedades y las relaciones del objeto [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="d2552-105">Read properties and relationships of the [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d2552-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d2552-106">Prerequisites</span></span>
<span data-ttu-id="d2552-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d2552-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d2552-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2552-109">Permission type</span></span>|<span data-ttu-id="d2552-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2552-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d2552-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2552-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d2552-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="d2552-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="d2552-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2552-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d2552-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2552-114">Not supported.</span></span>|
|<span data-ttu-id="d2552-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2552-115">Application</span></span>|<span data-ttu-id="d2552-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2552-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d2552-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2552-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="d2552-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d2552-118">Optional query parameters</span></span>
<span data-ttu-id="d2552-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2552-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="d2552-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2552-120">Request headers</span></span>
|<span data-ttu-id="d2552-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2552-121">Header</span></span>|<span data-ttu-id="d2552-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d2552-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d2552-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="d2552-123">Authorization</span></span>|<span data-ttu-id="d2552-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d2552-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d2552-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d2552-125">Accept</span></span>|<span data-ttu-id="d2552-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d2552-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d2552-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2552-127">Request body</span></span>
<span data-ttu-id="d2552-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d2552-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d2552-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2552-129">Response</span></span>
<span data-ttu-id="d2552-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2552-130">If successful, this method returns a `200 OK` response code and [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d2552-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2552-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="d2552-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2552-132">Request</span></span>
<span data-ttu-id="d2552-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2552-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}
```

### <a name="response"></a><span data-ttu-id="d2552-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2552-134">Response</span></span>
<span data-ttu-id="d2552-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2552-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 483

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceCompliancePolicySettingStateSummary",
    "id": "7474d6d5-d6d5-7474-d5d6-7474d5d67474",
    "setting": "Setting value",
    "settingName": "Setting Name value",
    "platformType": "iOS",
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




---
title: Obtener deviceCompliancePolicySettingStateSummary
description: Lea las propiedades y las relaciones del objeto deviceCompliancePolicySettingStateSummary.
ms.openlocfilehash: e184d0e2890fb7fb7f7642ef56d7a6d1946b5a31
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085225"
---
# <a name="get-devicecompliancepolicysettingstatesummary"></a><span data-ttu-id="21119-103">Obtener deviceCompliancePolicySettingStateSummary</span><span class="sxs-lookup"><span data-stu-id="21119-103">Get deviceCompliancePolicySettingStateSummary</span></span>

> <span data-ttu-id="21119-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="21119-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="21119-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="21119-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="21119-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="21119-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="21119-107">Lea las propiedades y las relaciones del objeto [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="21119-107">Read properties and relationships of the [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="21119-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="21119-108">Prerequisites</span></span>
<span data-ttu-id="21119-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="21119-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="21119-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="21119-111">Permission type</span></span>|<span data-ttu-id="21119-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="21119-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="21119-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="21119-113">Delegated (work or school account)</span></span>|<span data-ttu-id="21119-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="21119-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="21119-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="21119-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="21119-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="21119-116">Not supported.</span></span>|
|<span data-ttu-id="21119-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="21119-117">Application</span></span>|<span data-ttu-id="21119-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="21119-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="21119-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="21119-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="21119-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="21119-120">Optional query parameters</span></span>
<span data-ttu-id="21119-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21119-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="21119-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="21119-122">Request headers</span></span>
|<span data-ttu-id="21119-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21119-123">Header</span></span>|<span data-ttu-id="21119-124">Valor</span><span class="sxs-lookup"><span data-stu-id="21119-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="21119-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="21119-125">Authorization</span></span>|<span data-ttu-id="21119-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="21119-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="21119-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="21119-127">Accept</span></span>|<span data-ttu-id="21119-128">application/json</span><span class="sxs-lookup"><span data-stu-id="21119-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="21119-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="21119-129">Request body</span></span>
<span data-ttu-id="21119-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="21119-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="21119-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21119-131">Response</span></span>
<span data-ttu-id="21119-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21119-132">If successful, this method returns a `200 OK` response code and [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="21119-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="21119-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="21119-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="21119-134">Request</span></span>
<span data-ttu-id="21119-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="21119-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}
```

### <a name="response"></a><span data-ttu-id="21119-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21119-136">Response</span></span>
<span data-ttu-id="21119-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="21119-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 494

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceCompliancePolicySettingStateSummary",
    "id": "7474d6d5-d6d5-7474-d5d6-7474d5d67474",
    "setting": "Setting value",
    "settingName": "Setting Name value",
    "platformType": "androidForWork",
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






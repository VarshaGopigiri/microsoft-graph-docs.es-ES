---
title: Enumerar deviceCompliancePolicySettingStateSummaries
description: Enumere las propiedades y las relaciones de los objetos deviceCompliancePolicySettingStateSummary.
author: tfitzmac
ms.openlocfilehash: 1a93aaaf6c4c1373069e0cf0459bb39e0e1fc069
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337264"
---
# <a name="list-devicecompliancepolicysettingstatesummaries"></a><span data-ttu-id="a2489-103">Enumerar deviceCompliancePolicySettingStateSummaries</span><span class="sxs-lookup"><span data-stu-id="a2489-103">List deviceCompliancePolicySettingStateSummaries</span></span>

> <span data-ttu-id="a2489-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a2489-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a2489-105">Enumere las propiedades y las relaciones de los objetos [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="a2489-105">List properties and relationships of the [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a2489-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a2489-106">Prerequisites</span></span>
<span data-ttu-id="a2489-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a2489-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a2489-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a2489-109">Permission type</span></span>|<span data-ttu-id="a2489-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a2489-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a2489-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a2489-111">Delegated (work or school account)</span></span>|<span data-ttu-id="a2489-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="a2489-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="a2489-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a2489-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a2489-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2489-114">Not supported.</span></span>|
|<span data-ttu-id="a2489-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a2489-115">Application</span></span>|<span data-ttu-id="a2489-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2489-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a2489-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a2489-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicySettingStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="a2489-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a2489-118">Request headers</span></span>
|<span data-ttu-id="a2489-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2489-119">Header</span></span>|<span data-ttu-id="a2489-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a2489-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a2489-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="a2489-121">Authorization</span></span>|<span data-ttu-id="a2489-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a2489-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a2489-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a2489-123">Accept</span></span>|<span data-ttu-id="a2489-124">application/json</span><span class="sxs-lookup"><span data-stu-id="a2489-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a2489-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a2489-125">Request body</span></span>
<span data-ttu-id="a2489-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a2489-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a2489-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2489-127">Response</span></span>
<span data-ttu-id="a2489-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2489-128">If successful, this method returns a `200 OK` response code and a collection of [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a2489-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a2489-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="a2489-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a2489-130">Request</span></span>
<span data-ttu-id="a2489-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2489-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicySettingStateSummaries
```

### <a name="response"></a><span data-ttu-id="a2489-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2489-132">Response</span></span>
<span data-ttu-id="a2489-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a2489-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 521

{
  "value": [
    {
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
  ]
}
```




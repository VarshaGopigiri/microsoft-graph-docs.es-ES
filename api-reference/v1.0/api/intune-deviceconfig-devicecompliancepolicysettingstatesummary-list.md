---
title: Enumerar deviceCompliancePolicySettingStateSummaries
description: Enumere las propiedades y las relaciones de los objetos deviceCompliancePolicySettingStateSummary.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 3125a764386890a718037387ab37508bef7f224c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888301"
---
# <a name="list-devicecompliancepolicysettingstatesummaries"></a><span data-ttu-id="41026-103">Enumerar deviceCompliancePolicySettingStateSummaries</span><span class="sxs-lookup"><span data-stu-id="41026-103">List deviceCompliancePolicySettingStateSummaries</span></span>

> <span data-ttu-id="41026-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="41026-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="41026-105">Enumere las propiedades y las relaciones de los objetos [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="41026-105">List properties and relationships of the [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="41026-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="41026-106">Prerequisites</span></span>
<span data-ttu-id="41026-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="41026-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="41026-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="41026-109">Permission type</span></span>|<span data-ttu-id="41026-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="41026-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="41026-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="41026-111">Delegated (work or school account)</span></span>|<span data-ttu-id="41026-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="41026-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="41026-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="41026-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="41026-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41026-114">Not supported.</span></span>|
|<span data-ttu-id="41026-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="41026-115">Application</span></span>|<span data-ttu-id="41026-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41026-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="41026-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="41026-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicySettingStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="41026-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="41026-118">Request headers</span></span>
|<span data-ttu-id="41026-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41026-119">Header</span></span>|<span data-ttu-id="41026-120">Valor</span><span class="sxs-lookup"><span data-stu-id="41026-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="41026-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="41026-121">Authorization</span></span>|<span data-ttu-id="41026-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="41026-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="41026-123">Accept</span><span class="sxs-lookup"><span data-stu-id="41026-123">Accept</span></span>|<span data-ttu-id="41026-124">application/json</span><span class="sxs-lookup"><span data-stu-id="41026-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="41026-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="41026-125">Request body</span></span>
<span data-ttu-id="41026-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="41026-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="41026-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41026-127">Response</span></span>
<span data-ttu-id="41026-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="41026-128">If successful, this method returns a `200 OK` response code and a collection of [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="41026-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="41026-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="41026-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="41026-130">Request</span></span>
<span data-ttu-id="41026-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="41026-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicySettingStateSummaries
```

### <a name="response"></a><span data-ttu-id="41026-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41026-132">Response</span></span>
<span data-ttu-id="41026-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="41026-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




---
title: Enumerar deviceCompliancePolicySettingStateSummaries
description: Enumere las propiedades y las relaciones de los objetos deviceCompliancePolicySettingStateSummary.
ms.openlocfilehash: 015f7dc6efd08db93cd61b674dc1f8b0ec4b701b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089927"
---
# <a name="list-devicecompliancepolicysettingstatesummaries"></a><span data-ttu-id="d757a-103">Enumerar deviceCompliancePolicySettingStateSummaries</span><span class="sxs-lookup"><span data-stu-id="d757a-103">List deviceCompliancePolicySettingStateSummaries</span></span>

> <span data-ttu-id="d757a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d757a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d757a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d757a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d757a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d757a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d757a-107">Enumere las propiedades y las relaciones de los objetos [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="d757a-107">List properties and relationships of the [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d757a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d757a-108">Prerequisites</span></span>
<span data-ttu-id="d757a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d757a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d757a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d757a-111">Permission type</span></span>|<span data-ttu-id="d757a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d757a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d757a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d757a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d757a-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="d757a-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="d757a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d757a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d757a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d757a-116">Not supported.</span></span>|
|<span data-ttu-id="d757a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d757a-117">Application</span></span>|<span data-ttu-id="d757a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d757a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d757a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d757a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicySettingStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="d757a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d757a-120">Request headers</span></span>
|<span data-ttu-id="d757a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d757a-121">Header</span></span>|<span data-ttu-id="d757a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d757a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d757a-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="d757a-123">Authorization</span></span>|<span data-ttu-id="d757a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d757a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d757a-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d757a-125">Accept</span></span>|<span data-ttu-id="d757a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d757a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d757a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d757a-127">Request body</span></span>
<span data-ttu-id="d757a-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d757a-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d757a-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d757a-129">Response</span></span>
<span data-ttu-id="d757a-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d757a-130">If successful, this method returns a `200 OK` response code and a collection of [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d757a-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d757a-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="d757a-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d757a-132">Request</span></span>
<span data-ttu-id="d757a-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d757a-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicySettingStateSummaries
```

### <a name="response"></a><span data-ttu-id="d757a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d757a-134">Response</span></span>
<span data-ttu-id="d757a-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d757a-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 532

{
  "value": [
    {
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
  ]
}
```





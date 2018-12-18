---
title: Incluir en una lista settingStateDeviceSummaries
description: Enumere las propiedades y las relaciones de los objetos settingStateDeviceSummary.
author: tfitzmac
ms.openlocfilehash: 4d2cb1153901bc934ae0b1f57c3d419a83ce2953
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27342360"
---
# <a name="list-settingstatedevicesummaries"></a><span data-ttu-id="5cb28-103">Incluir en una lista settingStateDeviceSummaries</span><span class="sxs-lookup"><span data-stu-id="5cb28-103">List settingStateDeviceSummaries</span></span>

> <span data-ttu-id="5cb28-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5cb28-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5cb28-105">Enumere las propiedades y las relaciones de los objetos [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="5cb28-105">List properties and relationships of the [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5cb28-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5cb28-106">Prerequisites</span></span>
<span data-ttu-id="5cb28-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5cb28-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5cb28-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5cb28-109">Permission type</span></span>|<span data-ttu-id="5cb28-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5cb28-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5cb28-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5cb28-111">Delegated (work or school account)</span></span>|<span data-ttu-id="5cb28-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="5cb28-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="5cb28-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5cb28-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5cb28-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5cb28-114">Not supported.</span></span>|
|<span data-ttu-id="5cb28-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5cb28-115">Application</span></span>|<span data-ttu-id="5cb28-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5cb28-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5cb28-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5cb28-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceSettingStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="5cb28-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5cb28-118">Request headers</span></span>
|<span data-ttu-id="5cb28-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5cb28-119">Header</span></span>|<span data-ttu-id="5cb28-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5cb28-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5cb28-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="5cb28-121">Authorization</span></span>|<span data-ttu-id="5cb28-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5cb28-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5cb28-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5cb28-123">Accept</span></span>|<span data-ttu-id="5cb28-124">application/json</span><span class="sxs-lookup"><span data-stu-id="5cb28-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5cb28-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5cb28-125">Request body</span></span>
<span data-ttu-id="5cb28-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5cb28-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5cb28-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5cb28-127">Response</span></span>
<span data-ttu-id="5cb28-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5cb28-128">If successful, this method returns a `200 OK` response code and a collection of [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5cb28-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5cb28-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="5cb28-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5cb28-130">Request</span></span>
<span data-ttu-id="5cb28-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5cb28-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries
```

### <a name="response"></a><span data-ttu-id="5cb28-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5cb28-132">Response</span></span>
<span data-ttu-id="5cb28-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5cb28-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 486

{
  "value": [
    {
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
  ]
}
```




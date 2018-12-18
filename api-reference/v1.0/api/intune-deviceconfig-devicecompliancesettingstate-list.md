---
title: Lista deviceComplianceSettingStates
description: Enumere las propiedades y las relaciones de los objetos deviceComplianceSettingState.
author: tfitzmac
ms.openlocfilehash: a282b306478cc1ff2ecbe7f86a063183eee0edd8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27313800"
---
# <a name="list-devicecompliancesettingstates"></a><span data-ttu-id="74665-103">Lista deviceComplianceSettingStates</span><span class="sxs-lookup"><span data-stu-id="74665-103">List deviceComplianceSettingStates</span></span>

> <span data-ttu-id="74665-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="74665-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="74665-105">Enumere las propiedades y las relaciones de los objetos [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md).</span><span class="sxs-lookup"><span data-stu-id="74665-105">List properties and relationships of the [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="74665-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="74665-106">Prerequisites</span></span>
<span data-ttu-id="74665-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="74665-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="74665-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="74665-109">Permission type</span></span>|<span data-ttu-id="74665-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="74665-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="74665-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="74665-111">Delegated (work or school account)</span></span>|<span data-ttu-id="74665-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="74665-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="74665-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="74665-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="74665-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="74665-114">Not supported.</span></span>|
|<span data-ttu-id="74665-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="74665-115">Application</span></span>|<span data-ttu-id="74665-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="74665-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="74665-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="74665-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates
```

## <a name="request-headers"></a><span data-ttu-id="74665-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="74665-118">Request headers</span></span>
|<span data-ttu-id="74665-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74665-119">Header</span></span>|<span data-ttu-id="74665-120">Valor</span><span class="sxs-lookup"><span data-stu-id="74665-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="74665-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="74665-121">Authorization</span></span>|<span data-ttu-id="74665-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="74665-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="74665-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="74665-123">Accept</span></span>|<span data-ttu-id="74665-124">application/json</span><span class="sxs-lookup"><span data-stu-id="74665-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="74665-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="74665-125">Request body</span></span>
<span data-ttu-id="74665-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="74665-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="74665-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74665-127">Response</span></span>
<span data-ttu-id="74665-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74665-128">If successful, this method returns a `200 OK` response code and a collection of [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="74665-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="74665-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="74665-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="74665-130">Request</span></span>
<span data-ttu-id="74665-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="74665-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates
```

### <a name="response"></a><span data-ttu-id="74665-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74665-132">Response</span></span>
<span data-ttu-id="74665-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="74665-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 651

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceComplianceSettingState",
      "id": "9905f955-f955-9905-55f9-059955f90599",
      "setting": "Setting value",
      "settingName": "Setting Name value",
      "deviceId": "Device Id value",
      "deviceName": "Device Name value",
      "userId": "User Id value",
      "userEmail": "User Email value",
      "userName": "User Name value",
      "userPrincipalName": "User Principal Name value",
      "deviceModel": "Device Model value",
      "state": "notApplicable",
      "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00"
    }
  ]
}
```




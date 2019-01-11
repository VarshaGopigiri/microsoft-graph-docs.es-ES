---
title: Lista deviceComplianceSettingStates
description: Enumere las propiedades y las relaciones de los objetos deviceComplianceSettingState.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8bf4734c3adc53c3cd09da1bb74607cbf50ef330
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809117"
---
# <a name="list-devicecompliancesettingstates"></a><span data-ttu-id="33c18-103">Lista deviceComplianceSettingStates</span><span class="sxs-lookup"><span data-stu-id="33c18-103">List deviceComplianceSettingStates</span></span>

> <span data-ttu-id="33c18-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="33c18-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="33c18-105">Enumere las propiedades y las relaciones de los objetos [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md).</span><span class="sxs-lookup"><span data-stu-id="33c18-105">List properties and relationships of the [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="33c18-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="33c18-106">Prerequisites</span></span>
<span data-ttu-id="33c18-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="33c18-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="33c18-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="33c18-109">Permission type</span></span>|<span data-ttu-id="33c18-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="33c18-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="33c18-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="33c18-111">Delegated (work or school account)</span></span>|<span data-ttu-id="33c18-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="33c18-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="33c18-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="33c18-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="33c18-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="33c18-114">Not supported.</span></span>|
|<span data-ttu-id="33c18-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="33c18-115">Application</span></span>|<span data-ttu-id="33c18-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="33c18-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="33c18-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="33c18-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates
```

## <a name="request-headers"></a><span data-ttu-id="33c18-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="33c18-118">Request headers</span></span>
|<span data-ttu-id="33c18-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33c18-119">Header</span></span>|<span data-ttu-id="33c18-120">Valor</span><span class="sxs-lookup"><span data-stu-id="33c18-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="33c18-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="33c18-121">Authorization</span></span>|<span data-ttu-id="33c18-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="33c18-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="33c18-123">Accept</span><span class="sxs-lookup"><span data-stu-id="33c18-123">Accept</span></span>|<span data-ttu-id="33c18-124">application/json</span><span class="sxs-lookup"><span data-stu-id="33c18-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="33c18-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="33c18-125">Request body</span></span>
<span data-ttu-id="33c18-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="33c18-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="33c18-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="33c18-127">Response</span></span>
<span data-ttu-id="33c18-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="33c18-128">If successful, this method returns a `200 OK` response code and a collection of [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="33c18-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="33c18-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="33c18-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="33c18-130">Request</span></span>
<span data-ttu-id="33c18-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="33c18-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates
```

### <a name="response"></a><span data-ttu-id="33c18-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="33c18-132">Response</span></span>
<span data-ttu-id="33c18-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="33c18-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




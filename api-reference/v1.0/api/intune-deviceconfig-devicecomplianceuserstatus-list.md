---
title: Incluir en una lista deviceComplianceUserStatuses
description: Enumere las propiedades y las relaciones de los objetos deviceComplianceUserStatus.
ms.openlocfilehash: 687db5dba1add28b5753e04b25116438ec7f5e8e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028973"
---
# <a name="list-devicecomplianceuserstatuses"></a><span data-ttu-id="43d84-103">Incluir en una lista deviceComplianceUserStatuses</span><span class="sxs-lookup"><span data-stu-id="43d84-103">List deviceComplianceUserStatuses</span></span>

> <span data-ttu-id="43d84-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="43d84-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="43d84-105">Enumere las propiedades y las relaciones de los objetos [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="43d84-105">List properties and relationships of the [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="43d84-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="43d84-106">Prerequisites</span></span>
<span data-ttu-id="43d84-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="43d84-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="43d84-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="43d84-109">Permission type</span></span>|<span data-ttu-id="43d84-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="43d84-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="43d84-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="43d84-111">Delegated (work or school account)</span></span>|<span data-ttu-id="43d84-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="43d84-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="43d84-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="43d84-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="43d84-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="43d84-114">Not supported.</span></span>|
|<span data-ttu-id="43d84-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="43d84-115">Application</span></span>|<span data-ttu-id="43d84-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="43d84-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="43d84-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="43d84-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/userStatuses
```

## <a name="request-headers"></a><span data-ttu-id="43d84-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="43d84-118">Request headers</span></span>
|<span data-ttu-id="43d84-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43d84-119">Header</span></span>|<span data-ttu-id="43d84-120">Valor</span><span class="sxs-lookup"><span data-stu-id="43d84-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="43d84-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="43d84-121">Authorization</span></span>|<span data-ttu-id="43d84-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="43d84-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="43d84-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="43d84-123">Accept</span></span>|<span data-ttu-id="43d84-124">application/json</span><span class="sxs-lookup"><span data-stu-id="43d84-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="43d84-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="43d84-125">Request body</span></span>
<span data-ttu-id="43d84-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="43d84-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="43d84-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43d84-127">Response</span></span>
<span data-ttu-id="43d84-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43d84-128">If successful, this method returns a `200 OK` response code and a collection of [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="43d84-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="43d84-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="43d84-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="43d84-130">Request</span></span>
<span data-ttu-id="43d84-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="43d84-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/userStatuses
```

### <a name="response"></a><span data-ttu-id="43d84-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43d84-132">Response</span></span>
<span data-ttu-id="43d84-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="43d84-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 397

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceComplianceUserStatus",
      "id": "a0b566cd-66cd-a0b5-cd66-b5a0cd66b5a0",
      "userDisplayName": "User Display Name value",
      "devicesCount": 12,
      "status": "notApplicable",
      "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
      "userPrincipalName": "User Principal Name value"
    }
  ]
}
```




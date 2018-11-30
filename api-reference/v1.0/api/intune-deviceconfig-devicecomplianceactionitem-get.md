---
title: Obtener deviceComplianceActionItem
description: Lea las propiedades y las relaciones de los objetos deviceComplianceActionItem.
ms.openlocfilehash: 1697c7316495751a6bea18028f6e3df6ddaa469e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030152"
---
# <a name="get-devicecomplianceactionitem"></a><span data-ttu-id="ebafd-103">Obtener deviceComplianceActionItem</span><span class="sxs-lookup"><span data-stu-id="ebafd-103">Get deviceComplianceActionItem</span></span>

> <span data-ttu-id="ebafd-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ebafd-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ebafd-105">Lea las propiedades y las relaciones de los objetos [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="ebafd-105">Read properties and relationships of the [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ebafd-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ebafd-106">Prerequisites</span></span>
<span data-ttu-id="ebafd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ebafd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ebafd-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ebafd-109">Permission type</span></span>|<span data-ttu-id="ebafd-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ebafd-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ebafd-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ebafd-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ebafd-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="ebafd-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="ebafd-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ebafd-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ebafd-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ebafd-114">Not supported.</span></span>|
|<span data-ttu-id="ebafd-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ebafd-115">Application</span></span>|<span data-ttu-id="ebafd-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ebafd-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ebafd-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ebafd-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}/scheduledActionConfigurations/{deviceComplianceActionItemId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ebafd-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ebafd-118">Optional query parameters</span></span>
<span data-ttu-id="ebafd-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ebafd-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="ebafd-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ebafd-120">Request headers</span></span>
|<span data-ttu-id="ebafd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ebafd-121">Header</span></span>|<span data-ttu-id="ebafd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ebafd-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ebafd-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="ebafd-123">Authorization</span></span>|<span data-ttu-id="ebafd-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ebafd-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ebafd-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ebafd-125">Accept</span></span>|<span data-ttu-id="ebafd-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ebafd-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ebafd-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ebafd-127">Request body</span></span>
<span data-ttu-id="ebafd-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ebafd-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ebafd-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ebafd-129">Response</span></span>
<span data-ttu-id="ebafd-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ebafd-130">If successful, this method returns a `200 OK` response code and [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ebafd-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ebafd-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="ebafd-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ebafd-132">Request</span></span>
<span data-ttu-id="ebafd-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ebafd-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}/scheduledActionConfigurations/{deviceComplianceActionItemId}
```

### <a name="response"></a><span data-ttu-id="ebafd-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ebafd-134">Response</span></span>
<span data-ttu-id="ebafd-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ebafd-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 355

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceComplianceActionItem",
    "id": "e01a1893-1893-e01a-9318-1ae093181ae0",
    "gracePeriodHours": 0,
    "actionType": "notification",
    "notificationTemplateId": "Notification Template Id value",
    "notificationMessageCCList": [
      "Notification Message CCList value"
    ]
  }
}
```




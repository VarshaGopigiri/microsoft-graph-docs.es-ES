---
title: Enumerar deviceComplianceActionItems
description: Enumere las propiedades y las relaciones de los objetos deviceComplianceActionItem.
author: tfitzmac
ms.openlocfilehash: eba2212581f1cfd1e5c753682f733fdcc83aa369
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27346833"
---
# <a name="list-devicecomplianceactionitems"></a><span data-ttu-id="e6c98-103">Enumerar deviceComplianceActionItems</span><span class="sxs-lookup"><span data-stu-id="e6c98-103">List deviceComplianceActionItems</span></span>

> <span data-ttu-id="e6c98-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e6c98-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e6c98-105">Enumere las propiedades y las relaciones de los objetos [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).</span><span class="sxs-lookup"><span data-stu-id="e6c98-105">List properties and relationships of the [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e6c98-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e6c98-106">Prerequisites</span></span>
<span data-ttu-id="e6c98-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e6c98-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e6c98-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e6c98-109">Permission type</span></span>|<span data-ttu-id="e6c98-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e6c98-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e6c98-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e6c98-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e6c98-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="e6c98-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="e6c98-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e6c98-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e6c98-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6c98-114">Not supported.</span></span>|
|<span data-ttu-id="e6c98-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e6c98-115">Application</span></span>|<span data-ttu-id="e6c98-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6c98-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e6c98-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e6c98-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}/scheduledActionConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="e6c98-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e6c98-118">Request headers</span></span>
|<span data-ttu-id="e6c98-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6c98-119">Header</span></span>|<span data-ttu-id="e6c98-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e6c98-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e6c98-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="e6c98-121">Authorization</span></span>|<span data-ttu-id="e6c98-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e6c98-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e6c98-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e6c98-123">Accept</span></span>|<span data-ttu-id="e6c98-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e6c98-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e6c98-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e6c98-125">Request body</span></span>
<span data-ttu-id="e6c98-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e6c98-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e6c98-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6c98-127">Response</span></span>
<span data-ttu-id="e6c98-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6c98-128">If successful, this method returns a `200 OK` response code and a collection of [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e6c98-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6c98-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="e6c98-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e6c98-130">Request</span></span>
<span data-ttu-id="e6c98-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e6c98-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}/scheduledActionConfigurations
```

### <a name="response"></a><span data-ttu-id="e6c98-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6c98-132">Response</span></span>
<span data-ttu-id="e6c98-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e6c98-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 385

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceComplianceActionItem",
      "id": "e01a1893-1893-e01a-9318-1ae093181ae0",
      "gracePeriodHours": 0,
      "actionType": "notification",
      "notificationTemplateId": "Notification Template Id value",
      "notificationMessageCCList": [
        "Notification Message CCList value"
      ]
    }
  ]
}
```




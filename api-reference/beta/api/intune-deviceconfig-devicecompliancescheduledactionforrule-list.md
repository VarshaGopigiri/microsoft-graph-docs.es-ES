---
title: Incluir en una lista deviceComplianceScheduledActionForRules
description: Enumere las propiedades y las relaciones de los objetos deviceComplianceScheduledActionForRule.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3d27ecf60009136a926c534c0aa84c39f0e9b851
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27967766"
---
# <a name="list-devicecompliancescheduledactionforrules"></a><span data-ttu-id="f87be-103">Incluir en una lista deviceComplianceScheduledActionForRules</span><span class="sxs-lookup"><span data-stu-id="f87be-103">List deviceComplianceScheduledActionForRules</span></span>

> <span data-ttu-id="f87be-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f87be-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f87be-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f87be-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f87be-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f87be-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f87be-107">Enumere las propiedades y las relaciones de los objetos [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="f87be-107">List properties and relationships of the [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f87be-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f87be-108">Prerequisites</span></span>
<span data-ttu-id="f87be-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f87be-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f87be-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f87be-111">Permission type</span></span>|<span data-ttu-id="f87be-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f87be-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f87be-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f87be-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f87be-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="f87be-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="f87be-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f87be-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f87be-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f87be-116">Not supported.</span></span>|
|<span data-ttu-id="f87be-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f87be-117">Application</span></span>|<span data-ttu-id="f87be-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f87be-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f87be-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f87be-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule
```

## <a name="request-headers"></a><span data-ttu-id="f87be-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f87be-120">Request headers</span></span>
|<span data-ttu-id="f87be-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f87be-121">Header</span></span>|<span data-ttu-id="f87be-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f87be-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f87be-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f87be-123">Authorization</span></span>|<span data-ttu-id="f87be-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f87be-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f87be-125">Accept</span><span class="sxs-lookup"><span data-stu-id="f87be-125">Accept</span></span>|<span data-ttu-id="f87be-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f87be-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f87be-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f87be-127">Request body</span></span>
<span data-ttu-id="f87be-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f87be-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f87be-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f87be-129">Response</span></span>
<span data-ttu-id="f87be-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f87be-130">If successful, this method returns a `200 OK` response code and a collection of [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f87be-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f87be-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="f87be-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f87be-132">Request</span></span>
<span data-ttu-id="f87be-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f87be-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule
```

### <a name="response"></a><span data-ttu-id="f87be-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f87be-134">Response</span></span>
<span data-ttu-id="f87be-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f87be-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 208

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceComplianceScheduledActionForRule",
      "id": "f0075d5e-5d5e-f007-5e5d-07f05e5d07f0",
      "ruleName": "Rule Name value"
    }
  ]
}
```






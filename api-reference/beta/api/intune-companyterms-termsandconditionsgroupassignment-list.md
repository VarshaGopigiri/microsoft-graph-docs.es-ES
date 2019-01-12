---
title: Lista termsAndConditionsGroupAssignments
description: Propiedades de la lista y relaciones de los objetos termsAndConditionsGroupAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 135c96dd8ccf9a360fdc7ad0035f16154061e53e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27973688"
---
# <a name="list-termsandconditionsgroupassignments"></a><span data-ttu-id="f0a93-103">Lista termsAndConditionsGroupAssignments</span><span class="sxs-lookup"><span data-stu-id="f0a93-103">List termsAndConditionsGroupAssignments</span></span>

> <span data-ttu-id="f0a93-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f0a93-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f0a93-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f0a93-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f0a93-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f0a93-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f0a93-107">Propiedades de la lista y relaciones de los objetos [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a93-107">List properties and relationships of the [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f0a93-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f0a93-108">Prerequisites</span></span>
<span data-ttu-id="f0a93-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f0a93-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f0a93-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f0a93-111">Permission type</span></span>|<span data-ttu-id="f0a93-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f0a93-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f0a93-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f0a93-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f0a93-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="f0a93-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="f0a93-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f0a93-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f0a93-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f0a93-116">Not supported.</span></span>|
|<span data-ttu-id="f0a93-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f0a93-117">Application</span></span>|<span data-ttu-id="f0a93-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f0a93-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f0a93-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f0a93-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/termsAndConditions/{termsAndConditionsId}/groupAssignments
```

## <a name="request-headers"></a><span data-ttu-id="f0a93-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f0a93-120">Request headers</span></span>
|<span data-ttu-id="f0a93-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0a93-121">Header</span></span>|<span data-ttu-id="f0a93-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f0a93-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f0a93-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f0a93-123">Authorization</span></span>|<span data-ttu-id="f0a93-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f0a93-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f0a93-125">Accept</span><span class="sxs-lookup"><span data-stu-id="f0a93-125">Accept</span></span>|<span data-ttu-id="f0a93-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f0a93-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f0a93-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f0a93-127">Request body</span></span>
<span data-ttu-id="f0a93-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f0a93-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f0a93-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f0a93-129">Response</span></span>
<span data-ttu-id="f0a93-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f0a93-130">If successful, this method returns a `200 OK` response code and a collection of [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f0a93-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f0a93-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="f0a93-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f0a93-132">Request</span></span>
<span data-ttu-id="f0a93-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f0a93-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/termsAndConditions/{termsAndConditionsId}/groupAssignments
```

### <a name="response"></a><span data-ttu-id="f0a93-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f0a93-134">Response</span></span>
<span data-ttu-id="f0a93-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f0a93-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 214

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.termsAndConditionsGroupAssignment",
      "id": "2eb1aab7-aab7-2eb1-b7aa-b12eb7aab12e",
      "targetGroupId": "Target Group Id value"
    }
  ]
}
```






---
title: Lista circularGeofenceManagementConditions
description: Propiedades de la lista y relaciones de los objetos circularGeofenceManagementCondition.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: df8cc05ebc9e6b608232dd9b894968ca5f8b3234
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27944617"
---
# <a name="list-circulargeofencemanagementconditions"></a><span data-ttu-id="ee074-103">Lista circularGeofenceManagementConditions</span><span class="sxs-lookup"><span data-stu-id="ee074-103">List circularGeofenceManagementConditions</span></span>

> <span data-ttu-id="ee074-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ee074-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ee074-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ee074-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ee074-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ee074-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ee074-107">Propiedades de la lista y relaciones de los objetos [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="ee074-107">List properties and relationships of the [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ee074-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ee074-108">Prerequisites</span></span>
<span data-ttu-id="ee074-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ee074-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ee074-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ee074-111">Permission type</span></span>|<span data-ttu-id="ee074-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ee074-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ee074-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ee074-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ee074-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="ee074-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="ee074-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ee074-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ee074-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ee074-116">Not supported.</span></span>|
|<span data-ttu-id="ee074-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ee074-117">Application</span></span>|<span data-ttu-id="ee074-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ee074-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ee074-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ee074-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/managementConditions
GET /deviceManagement/managementConditions/{managementConditionId}/managementConditionStatements/{managementConditionStatementId}/managementConditions
```

## <a name="request-headers"></a><span data-ttu-id="ee074-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ee074-120">Request headers</span></span>
|<span data-ttu-id="ee074-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee074-121">Header</span></span>|<span data-ttu-id="ee074-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ee074-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ee074-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ee074-123">Authorization</span></span>|<span data-ttu-id="ee074-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ee074-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ee074-125">Accept</span><span class="sxs-lookup"><span data-stu-id="ee074-125">Accept</span></span>|<span data-ttu-id="ee074-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ee074-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ee074-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ee074-127">Request body</span></span>
<span data-ttu-id="ee074-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ee074-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ee074-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee074-129">Response</span></span>
<span data-ttu-id="ee074-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee074-130">If successful, this method returns a `200 OK` response code and a collection of [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ee074-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ee074-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="ee074-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ee074-132">Request</span></span>
<span data-ttu-id="ee074-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ee074-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/managementConditions
```

### <a name="response"></a><span data-ttu-id="ee074-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee074-134">Response</span></span>
<span data-ttu-id="ee074-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ee074-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 701

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.circularGeofenceManagementCondition",
      "id": "30ee27b6-27b6-30ee-b627-ee30b627ee30",
      "uniqueName": "Unique Name value",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "modifiedDateTime": "2017-01-01T00:00:22.8983556-08:00",
      "eTag": "ETag value",
      "applicablePlatforms": [
        "androidForWork"
      ],
      "latitude": "<Unknown Primitive Type Edm.Double>",
      "longitude": "<Unknown Primitive Type Edm.Double>",
      "radiusInMeters": "<Unknown Primitive Type Edm.Single>"
    }
  ]
}
```






---
title: Lista networkManagementConditions
description: Propiedades de la lista y relaciones de los objetos networkManagementCondition.
ms.openlocfilehash: 22fe6885cfa54d74860ecb085477e6f65a153453
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089660"
---
# <a name="list-networkmanagementconditions"></a><span data-ttu-id="58d89-103">Lista networkManagementConditions</span><span class="sxs-lookup"><span data-stu-id="58d89-103">List networkManagementConditions</span></span>

> <span data-ttu-id="58d89-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="58d89-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="58d89-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="58d89-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="58d89-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="58d89-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="58d89-107">Propiedades de la lista y relaciones de los objetos [networkManagementCondition](../resources/intune-fencing-networkmanagementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="58d89-107">List properties and relationships of the [networkManagementCondition](../resources/intune-fencing-networkmanagementcondition.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="58d89-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="58d89-108">Prerequisites</span></span>
<span data-ttu-id="58d89-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="58d89-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="58d89-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="58d89-111">Permission type</span></span>|<span data-ttu-id="58d89-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="58d89-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="58d89-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="58d89-113">Delegated (work or school account)</span></span>|<span data-ttu-id="58d89-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="58d89-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="58d89-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="58d89-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="58d89-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="58d89-116">Not supported.</span></span>|
|<span data-ttu-id="58d89-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="58d89-117">Application</span></span>|<span data-ttu-id="58d89-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="58d89-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="58d89-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="58d89-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/managementConditions
GET /deviceManagement/managementConditions/{managementConditionId}/managementConditionStatements/{managementConditionStatementId}/managementConditions
```

## <a name="request-headers"></a><span data-ttu-id="58d89-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="58d89-120">Request headers</span></span>
|<span data-ttu-id="58d89-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58d89-121">Header</span></span>|<span data-ttu-id="58d89-122">Valor</span><span class="sxs-lookup"><span data-stu-id="58d89-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="58d89-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="58d89-123">Authorization</span></span>|<span data-ttu-id="58d89-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="58d89-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="58d89-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="58d89-125">Accept</span></span>|<span data-ttu-id="58d89-126">application/json</span><span class="sxs-lookup"><span data-stu-id="58d89-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="58d89-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="58d89-127">Request body</span></span>
<span data-ttu-id="58d89-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="58d89-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="58d89-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58d89-129">Response</span></span>
<span data-ttu-id="58d89-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [networkManagementCondition](../resources/intune-fencing-networkmanagementcondition.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58d89-130">If successful, this method returns a `200 OK` response code and a collection of [networkManagementCondition](../resources/intune-fencing-networkmanagementcondition.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="58d89-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="58d89-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="58d89-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="58d89-132">Request</span></span>
<span data-ttu-id="58d89-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="58d89-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/managementConditions
```

### <a name="response"></a><span data-ttu-id="58d89-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58d89-134">Response</span></span>
<span data-ttu-id="58d89-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="58d89-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 511

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.networkManagementCondition",
      "id": "c2919b8f-9b8f-c291-8f9b-91c28f9b91c2",
      "uniqueName": "Unique Name value",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "modifiedDateTime": "2017-01-01T00:00:22.8983556-08:00",
      "eTag": "ETag value",
      "applicablePlatforms": [
        "androidForWork"
      ]
    }
  ]
}
```






---
title: Enumerar termsAndConditionsAssignments
description: Enumere las propiedades y las relaciones de los objetos termsAndConditionsAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 1c9beea3297c1360ee11a1ed267a5d06e9247862
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962558"
---
# <a name="list-termsandconditionsassignments"></a><span data-ttu-id="1ccb1-103">Enumerar termsAndConditionsAssignments</span><span class="sxs-lookup"><span data-stu-id="1ccb1-103">List termsAndConditionsAssignments</span></span>

> <span data-ttu-id="1ccb1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1ccb1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1ccb1-105">Enumere las propiedades y las relaciones de los objetos [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="1ccb1-105">List properties and relationships of the [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1ccb1-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1ccb1-106">Prerequisites</span></span>
<span data-ttu-id="1ccb1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1ccb1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1ccb1-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1ccb1-109">Permission type</span></span>|<span data-ttu-id="1ccb1-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1ccb1-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1ccb1-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1ccb1-111">Delegated (work or school account)</span></span>|<span data-ttu-id="1ccb1-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="1ccb1-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="1ccb1-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1ccb1-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1ccb1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1ccb1-114">Not supported.</span></span>|
|<span data-ttu-id="1ccb1-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1ccb1-115">Application</span></span>|<span data-ttu-id="1ccb1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1ccb1-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1ccb1-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1ccb1-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="1ccb1-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1ccb1-118">Request headers</span></span>
|<span data-ttu-id="1ccb1-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ccb1-119">Header</span></span>|<span data-ttu-id="1ccb1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1ccb1-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1ccb1-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="1ccb1-121">Authorization</span></span>|<span data-ttu-id="1ccb1-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1ccb1-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1ccb1-123">Accept</span><span class="sxs-lookup"><span data-stu-id="1ccb1-123">Accept</span></span>|<span data-ttu-id="1ccb1-124">application/json</span><span class="sxs-lookup"><span data-stu-id="1ccb1-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1ccb1-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1ccb1-125">Request body</span></span>
<span data-ttu-id="1ccb1-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1ccb1-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1ccb1-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ccb1-127">Response</span></span>
<span data-ttu-id="1ccb1-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1ccb1-128">If successful, this method returns a `200 OK` response code and a collection of [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1ccb1-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1ccb1-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="1ccb1-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1ccb1-130">Request</span></span>
<span data-ttu-id="1ccb1-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1ccb1-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments
```

### <a name="response"></a><span data-ttu-id="1ccb1-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ccb1-132">Response</span></span>
<span data-ttu-id="1ccb1-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1ccb1-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 270

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.termsAndConditionsAssignment",
      "id": "64c1a196-a196-64c1-96a1-c16496a1c164",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```




---
title: Obtener plannerPlanDetails
description: Recuperar las propiedades y las relaciones del objeto **plannerplandetails**.
ms.openlocfilehash: 652ba06541562f059c7e2b690b99b595e47331c2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032078"
---
# <a name="get-plannerplandetails"></a><span data-ttu-id="dc106-103">Obtener plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="dc106-103">Get plannerPlanDetails</span></span>

<span data-ttu-id="dc106-104">Recuperar las propiedades y las relaciones del objeto **plannerplandetails**.</span><span class="sxs-lookup"><span data-stu-id="dc106-104">Retrieve the properties and relationships of **plannerplandetails** object.</span></span>
## <a name="permissions"></a><span data-ttu-id="dc106-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="dc106-105">Permissions</span></span>
<span data-ttu-id="dc106-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dc106-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dc106-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dc106-108">Permission type</span></span>      | <span data-ttu-id="dc106-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dc106-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dc106-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dc106-110">Delegated (work or school account)</span></span> | <span data-ttu-id="dc106-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dc106-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="dc106-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dc106-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dc106-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dc106-113">Not supported.</span></span>    |
|<span data-ttu-id="dc106-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dc106-114">Application</span></span> | <span data-ttu-id="dc106-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dc106-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="dc106-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dc106-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /planner/plans/{id}/details
```

## <a name="request-headers"></a><span data-ttu-id="dc106-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dc106-117">Request headers</span></span>
| <span data-ttu-id="dc106-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="dc106-118">Name</span></span>      |<span data-ttu-id="dc106-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc106-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="dc106-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="dc106-120">Authorization</span></span>  | <span data-ttu-id="dc106-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dc106-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="dc106-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dc106-123">Request body</span></span>
<span data-ttu-id="dc106-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="dc106-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="dc106-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc106-125">Response</span></span>

<span data-ttu-id="dc106-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerPlanDetails](../resources/plannerplandetails.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dc106-126">If successful, this method returns a `200 OK` response code and [plannerPlanDetails](../resources/plannerplandetails.md) object in the response body.</span></span>

<span data-ttu-id="dc106-p103">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="dc106-p103">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="dc106-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc106-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="dc106-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dc106-131">Request</span></span>
<span data-ttu-id="dc106-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dc106-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_plannerplandetails"
}-->
```http
GET https://graph.microsoft.com/v1.0/planner/plans/{plan-id}/details
```
##### <a name="response"></a><span data-ttu-id="dc106-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc106-133">Response</span></span>
<span data-ttu-id="dc106-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dc106-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerPlanDetails"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 373

{
  "sharedWith": {
    "aaa27244-1db4-476a-a5cb-004607466324" : true,
    "6463a5ce-2119-4198-9f2a-628761df4a62" : true
  },
  "categoryDescriptions": {
    "category1": "Indoors",
    "category2": "Outdoors",
    "category3": null,
    "category4": null,
    "category5": "Needs materials",
    "category6": "Needs equipment"
  },
  "id": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get plannerPlanDetails",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
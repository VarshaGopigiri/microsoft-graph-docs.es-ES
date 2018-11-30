---
title: Enumerar planes
description: Recuperar una lista de objetos **plannerplan** compartidos con un objeto user.
ms.openlocfilehash: b1aa987f1c615a17108ffb1b2d639e76a084faae
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085939"
---
# <a name="list-plans"></a><span data-ttu-id="19604-103">Enumerar planes</span><span class="sxs-lookup"><span data-stu-id="19604-103">List plans</span></span>

> <span data-ttu-id="19604-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="19604-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="19604-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="19604-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="19604-106">Recuperar una lista de objetos **plannerplan** compartidos con un objeto [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="19604-106">Retrieve a list of **plannerplan** objects shared with a [user](../resources/user.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="19604-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="19604-107">Permissions</span></span>
<span data-ttu-id="19604-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="19604-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="19604-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="19604-110">Permission type</span></span>      | <span data-ttu-id="19604-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="19604-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="19604-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="19604-112">Delegated (work or school account)</span></span> | <span data-ttu-id="19604-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="19604-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="19604-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="19604-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="19604-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="19604-115">Not supported.</span></span>    |
|<span data-ttu-id="19604-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="19604-116">Application</span></span> | <span data-ttu-id="19604-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="19604-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="19604-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="19604-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/planner/plans
GET /users/<id>/planner/plans
GET /drive/root/createdByUser/planner/plans
```

## <a name="request-headers"></a><span data-ttu-id="19604-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="19604-119">Request headers</span></span>
| <span data-ttu-id="19604-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="19604-120">Name</span></span>      |<span data-ttu-id="19604-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="19604-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="19604-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="19604-122">Authorization</span></span>  | <span data-ttu-id="19604-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="19604-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="19604-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="19604-125">Request body</span></span>
<span data-ttu-id="19604-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="19604-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="19604-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="19604-127">Response</span></span>

<span data-ttu-id="19604-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [plannerPlan](../resources/plannerplan.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="19604-128">If successful, this method returns a `200 OK` response code and collection of [plannerPlan](../resources/plannerplan.md) objects in the response body.</span></span>

<span data-ttu-id="19604-p104">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="19604-p104">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="19604-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="19604-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="19604-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="19604-133">Request</span></span>
<span data-ttu-id="19604-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="19604-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_plans"
}-->
```http
GET https://graph.microsoft.com/beta/me/planner/plans
```
##### <a name="response"></a><span data-ttu-id="19604-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="19604-135">Response</span></span>
<span data-ttu-id="19604-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="19604-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerPlan",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 438

{
  "value": [
    {
      "createdBy": {
        "application": {
          "id": "95e27074-6c4a-447a-aa24-9d718a0b86fa"
        },
        "user": {
          "id": "ebf3b108-5234-4e22-b93d-656d7dae5874"
        }
      },
      "createdDateTime": "2015-03-30T18:36:49.2407981Z",
      "owner": "ebf3b108-5234-4e22-b93d-656d7dae5874",
      "title": "title-value",
      "id": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List plans",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
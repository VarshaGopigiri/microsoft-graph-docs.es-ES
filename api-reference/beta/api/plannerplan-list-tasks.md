---
title: Enumerar tareas
description: Recuperar una lista de objetos **plannertask** asociados a un objeto plannerPlan.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: d658927db1334457d405b81ee8bf6ad2a848584c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27926088"
---
# <a name="list-tasks"></a><span data-ttu-id="c0267-103">Enumerar tareas</span><span class="sxs-lookup"><span data-stu-id="c0267-103">List tasks</span></span>

> <span data-ttu-id="c0267-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c0267-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c0267-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c0267-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c0267-106">Recuperar una lista de objetos **plannertask** asociados a un objeto [plannerPlan](../resources/plannerplan.md).</span><span class="sxs-lookup"><span data-stu-id="c0267-106">Retrieve a list of **plannertask** objects associated to a [plannerPlan](../resources/plannerplan.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="c0267-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c0267-107">Permissions</span></span>
<span data-ttu-id="c0267-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c0267-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c0267-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c0267-110">Permission type</span></span>      | <span data-ttu-id="c0267-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c0267-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c0267-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c0267-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c0267-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c0267-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="c0267-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c0267-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c0267-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c0267-115">Not supported.</span></span>    |
|<span data-ttu-id="c0267-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c0267-116">Application</span></span> | <span data-ttu-id="c0267-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c0267-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c0267-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c0267-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /planner/plans/<id>/tasks
```

## <a name="request-headers"></a><span data-ttu-id="c0267-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c0267-119">Request headers</span></span>
| <span data-ttu-id="c0267-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="c0267-120">Name</span></span>      |<span data-ttu-id="c0267-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0267-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="c0267-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c0267-122">Authorization</span></span>  | <span data-ttu-id="c0267-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c0267-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c0267-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c0267-125">Request body</span></span>
<span data-ttu-id="c0267-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c0267-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c0267-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0267-127">Response</span></span>

<span data-ttu-id="c0267-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [plannerTask](../resources/plannertask.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0267-128">If successful, this method returns a `200 OK` response code and collection of [plannerTask](../resources/plannertask.md) objects in the response body.</span></span>

<span data-ttu-id="c0267-p104">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="c0267-p104">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="c0267-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c0267-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c0267-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c0267-133">Request</span></span>
<span data-ttu-id="c0267-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c0267-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_tasks"
}-->
```http
GET https://graph.microsoft.com/beta/planner/plans/xqQg5FS2LkCp935s-FIFm2QAFkHM/tasks
```
##### <a name="response"></a><span data-ttu-id="c0267-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0267-135">Response</span></span>
<span data-ttu-id="c0267-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c0267-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerTask",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 833

{
  "value": [
    {
      "createdBy": {
        "user": {
          "id": "6463a5ce-2119-4198-9f2a-628761df4a62"
        }
      },
      "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM",
      "bucketId": "gcrYAaAkgU2EQUvpkNNXLGQAGTtu",
      "title": "title-value",
      "orderHint": "9223370609546166567W",
      "assigneePriority": "90057581\"",
      "createdDateTime": "2015-03-25T18:36:49.2407981Z",
      "assignments": {
        "fbab97d0-4932-4511-b675-204639209557": {
          "@odata.type": "#microsoft.graph.plannerAssignment",
          "assignedBy": {
            "user": {
              "id": "1e9955d2-6acd-45bf-86d3-b546fdc795eb"
            }
          },
          "assignedDateTime": "2015-03-25T18:38:21.956Z",
          "orderHint": "RWk1"
         }
      },
      "id":"01gzSlKkIUSUl6DF_EilrmQAKDhh"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List tasks",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

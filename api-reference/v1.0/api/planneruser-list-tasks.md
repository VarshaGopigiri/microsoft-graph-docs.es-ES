---
title: Enumerar tareas
description: Recuperar una lista de objetos **plannertask** asignados a un usuario.
localization_priority: Priority
ms.openlocfilehash: 4c268f666769b97aeff5fe7400b05ff5a6625810
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854988"
---
# <a name="list-tasks"></a><span data-ttu-id="f28f9-103">Enumerar tareas</span><span class="sxs-lookup"><span data-stu-id="f28f9-103">List tasks</span></span>

<span data-ttu-id="f28f9-104">Recuperar una lista de objetos **plannertask** asignados a un usuario.</span><span class="sxs-lookup"><span data-stu-id="f28f9-104">Retrieve a list of **plannertask** objects assigned to a User.</span></span>
## <a name="permissions"></a><span data-ttu-id="f28f9-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f28f9-105">Permissions</span></span>
<span data-ttu-id="f28f9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f28f9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f28f9-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f28f9-108">Permission type</span></span>      | <span data-ttu-id="f28f9-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f28f9-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f28f9-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f28f9-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f28f9-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f28f9-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="f28f9-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f28f9-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f28f9-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f28f9-113">Not supported.</span></span>    |
|<span data-ttu-id="f28f9-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f28f9-114">Application</span></span> | <span data-ttu-id="f28f9-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f28f9-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f28f9-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f28f9-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/planner/tasks
GET /users/{id}/planner/tasks
GET /drive/root/createdByUser/planner/tasks
```

## <a name="request-headers"></a><span data-ttu-id="f28f9-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f28f9-117">Request headers</span></span>
| <span data-ttu-id="f28f9-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="f28f9-118">Name</span></span>      |<span data-ttu-id="f28f9-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f28f9-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="f28f9-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="f28f9-120">Authorization</span></span>  | <span data-ttu-id="f28f9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f28f9-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f28f9-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f28f9-123">Request body</span></span>
<span data-ttu-id="f28f9-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f28f9-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f28f9-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f28f9-125">Response</span></span>

<span data-ttu-id="f28f9-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [plannerTask](../resources/plannertask.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f28f9-126">If successful, this method returns a `200 OK` response code and collection of [plannerTask](../resources/plannertask.md) objects in the response body.</span></span>

<span data-ttu-id="f28f9-p103">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="f28f9-p103">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="f28f9-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f28f9-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f28f9-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f28f9-131">Request</span></span>
<span data-ttu-id="f28f9-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f28f9-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_tasks"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/planner/tasks
```
##### <a name="response"></a><span data-ttu-id="f28f9-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f28f9-133">Response</span></span>
<span data-ttu-id="f28f9-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f28f9-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

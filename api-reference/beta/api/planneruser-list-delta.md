---
title: 'Organizador: delta'
description: Recupera los cambios realizados en los objetos que el usuario está suscrito a.
author: TarkanSevilmis
localization_priority: Normal
ms.prod: planner
ms.openlocfilehash: 0e350eb65abf08efb2ba2cb395f3b92c7b9b93e0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27915966"
---
# <a name="planner-delta"></a><span data-ttu-id="515ab-103">Organizador: delta</span><span class="sxs-lookup"><span data-stu-id="515ab-103">Planner: delta</span></span>

> <span data-ttu-id="515ab-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="515ab-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="515ab-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="515ab-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="515ab-106">Recupera los cambios realizados en los objetos que el usuario está [suscrito](../resources/planner-overview.md#track-changes-using-delta-query) a.</span><span class="sxs-lookup"><span data-stu-id="515ab-106">Retrieves changes to objects that the user is [subscribed](../resources/planner-overview.md#track-changes-using-delta-query) to.</span></span>

<span data-ttu-id="515ab-107">Este método permite que la aplicación realizar un seguimiento de los cambios a los objetos que el usuario puede obtener acceso desde dentro del organizador a través del tiempo.</span><span class="sxs-lookup"><span data-stu-id="515ab-107">This method allows your application to track changes to objects that the user can access from within Planner over time.</span></span>

<span data-ttu-id="515ab-108">El valor devuelto de este método puede contener heterogéneo tipos de objetos desde el organizador.</span><span class="sxs-lookup"><span data-stu-id="515ab-108">The return value of this method might contain hetergenous types of objects from Planner.</span></span>

<span data-ttu-id="515ab-109">Para obtener más información sobre el seguimiento de los cambios en datos de Microsoft Graph, vea [utilizar query de delta para realizar un seguimiento de los cambios en datos de Microsoft Graph](/graph/delta-query-overview).</span><span class="sxs-lookup"><span data-stu-id="515ab-109">For more information about tracking changes in Microsoft Graph data, see [Use delta query to track changes in Microsoft Graph data](/graph/delta-query-overview).</span></span>

## <a name="permissions"></a><span data-ttu-id="515ab-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="515ab-110">Permissions</span></span>

<span data-ttu-id="515ab-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="515ab-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="515ab-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="515ab-113">Permission type</span></span>      | <span data-ttu-id="515ab-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="515ab-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="515ab-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="515ab-115">Delegated (work or school account)</span></span> | <span data-ttu-id="515ab-116">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="515ab-116">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="515ab-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="515ab-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="515ab-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="515ab-118">Not supported.</span></span>    |
|<span data-ttu-id="515ab-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="515ab-119">Application</span></span> | <span data-ttu-id="515ab-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="515ab-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="515ab-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="515ab-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /me/planner/all/delta
GET /users/<id>/planner/all/delta
```

<span data-ttu-id="515ab-122">Sin parámetros adicionales de la consulta (como `$select`, `$expand`, o `$filter`) se admiten actualmente en la implementación de los planes de consultas de delta.</span><span class="sxs-lookup"><span data-stu-id="515ab-122">No additional query parameters (such as `$select`, `$expand`, or `$filter`) are currently supported on Planner's implementation of delta queries.</span></span>

## <a name="request-headers"></a><span data-ttu-id="515ab-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="515ab-123">Request headers</span></span>

| <span data-ttu-id="515ab-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="515ab-124">Name</span></span>           |<span data-ttu-id="515ab-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="515ab-125">Description</span></span>                |
|:---------------|:--------------------------|
| <span data-ttu-id="515ab-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="515ab-126">Authorization</span></span>  | <span data-ttu-id="515ab-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="515ab-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="515ab-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="515ab-129">Request body</span></span>

<span data-ttu-id="515ab-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="515ab-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="515ab-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="515ab-131">Response</span></span>

<span data-ttu-id="515ab-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de cambios se apliquen a los objetos en el cuerpo de la respuesta y un vínculo de sincronización Delta que se deben seguir.</span><span class="sxs-lookup"><span data-stu-id="515ab-132">If successful, this method returns a `200 OK` response code and a collection of changes to be applied to objects in the response body, and a Delta Sync link to follow.</span></span>

<span data-ttu-id="515ab-133">Si el `deltaLink` que usará el autor de la llamada es incorrecto, este extremo devolverá HTTP 400.</span><span class="sxs-lookup"><span data-stu-id="515ab-133">If the `deltaLink` that the caller uses is malformed, this endpoint will return HTTP 400.</span></span>

<span data-ttu-id="515ab-134">Si el `deltaLink` que usará el autor de la llamada es demasiado antigua, este extremo devolverá HTTP 410.</span><span class="sxs-lookup"><span data-stu-id="515ab-134">If the `deltaLink` that the caller uses is too old, this endpoint will return HTTP 410.</span></span>

<span data-ttu-id="515ab-p104">Este método puede devolver cualquiera de los [códigos de estado HTTP](/graph/errors). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 403 y 404. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).</span><span class="sxs-lookup"><span data-stu-id="515ab-p104">This method can return any of the [HTTP status codes](/graph/errors). The most common errors that apps should handle for this method are the 403 and 404 responses. For more information about these errors, see [Common Planner error conditions](../resources/planner-overview.md#common-planner-error-conditions).</span></span>

## <a name="example"></a><span data-ttu-id="515ab-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="515ab-138">Example</span></span>

##### <a name="request"></a><span data-ttu-id="515ab-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="515ab-139">Request</span></span>

<span data-ttu-id="515ab-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="515ab-140">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_delta"
}-->

```http
GET https://graph.microsoft.com/beta/me/planner/all/delta
```

##### <a name="response"></a><span data-ttu-id="515ab-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="515ab-141">Response</span></span>
<span data-ttu-id="515ab-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="515ab-142">Here is an example of the response.</span></span>

><span data-ttu-id="515ab-143">**Nota:** Puede que se acorte el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="515ab-143">**Note:** The response object shown might be shortened for readability.</span></span> <span data-ttu-id="515ab-144">Se devolverán todas las propiedades modificadas desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="515ab-144">All the changed properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "name": "get_delta",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.entity)",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
content-type: application/json;odata.metadata=minimal;odata.streaming=true;IEEE754Compatible=false;charset=utf-8
cache-control: private
client-request-id: 3acb384b-e2d1-4a46-a347-e03bc6428cac
request-id: 3acb384b-e2d1-4a46-a347-e03bc6428cac
preference-applied: odata.track-changes, odata.track-changes

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.plannerDelta)",
    "@odata.deltaLink": "https://graph.microsoft.com/beta/me/planner/all/delta?$deltatoken=jVztGMFnm7qLEQ69FaXzWF5sPEJZU2YxZa32QEvnZTZ4q4C10ThM5uL7bEPm9ysqrxOY0QQIb4Uqmc9DH3rn7pczamvtCipDVJ4FivXh398.J9pSVKpytlutvx03-iBmO4ZM_3qPztOq2T9VIjHoRR0",
    "value": [
        {
            "@odata.type": "#microsoft.graph.plannerTask",
            "@odata.etag": "W/\"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBASCc=\"",
            "percentComplete": 100,
            "completedDateTime": "2018-03-13T21:31:25.778Z",
            "completedBy": {
                "user": {
                    "id": "8414b634-316f-41ba-b6a6-646a2949e3a5"
                }
            },
            "id": "5pNWKnX2XUalCKa64-oiXJUAPT1v",
            "@odata.context": "https://graph.microsoft.com/beta/$metadata#planner/tasks/$entity"
        },
        {
            "@odata.type": "#microsoft.graph.plannerTask",
            "@odata.etag": "W/\"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBATCc=\"",
            "percentComplete": 0,
            "completedDateTime": null,
            "completedBy": null,
            "id": "5pNWKnX2XUalCKa64-oiXJUAPT1v",
            "@odata.context": "https://graph.microsoft.com/beta/$metadata#planner/tasks/$entity"
        },
        {
            "@odata.type": "#microsoft.graph.plannerTask",
            "@odata.etag": "W/\"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAUCc=\"",
            "title": "Title change",
            "id": "5pNWKnX2XUalCKa64-oiXJUAPT1v",
            "@odata.context": "https://graph.microsoft.com/beta/$metadata#planner/tasks/$entity"
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List changes",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

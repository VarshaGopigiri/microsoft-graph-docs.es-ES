---
title: 'usuario: findRoomLists'
description: Obtener las listas de salas definidas en un inquilino.
author: dkershaw10
localization_priority: Priority
ms.openlocfilehash: 55ff393e828d324035050e33cf194cb49d302080
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855737"
---
# <a name="user-findroomlists"></a><span data-ttu-id="43e4a-103">usuario: findRoomLists</span><span class="sxs-lookup"><span data-stu-id="43e4a-103">user: findRoomLists</span></span>

> <span data-ttu-id="43e4a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="43e4a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="43e4a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="43e4a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="43e4a-106">Obtener las listas de salas definidas en un inquilino.</span><span class="sxs-lookup"><span data-stu-id="43e4a-106">Get the room lists defined in a tenant.</span></span>

<span data-ttu-id="43e4a-107">Los inquilinos pueden organizar las salas de reuniones en listas de las salas.</span><span class="sxs-lookup"><span data-stu-id="43e4a-107">Tenants can organize meeting rooms into room lists.</span></span> <span data-ttu-id="43e4a-108">Cada sala de reuniones y la lista de salas está representada por una instancia de [emailAddress](../resources/emailaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="43e4a-108">Each meeting room and room list is represented by an [emailAddress](../resources/emailaddress.md) instance.</span></span>
<span data-ttu-id="43e4a-109">Puede obtener todas las listas de sala en el inquilino, [obtener todas las salas](user-findrooms.md) en el inquilino u [obtener todas las salas](user-findrooms.md) en una lista de salas específicas.</span><span class="sxs-lookup"><span data-stu-id="43e4a-109">You can get all the room lists in the tenant, [get all the rooms](user-findrooms.md) in the tenant, or [get all the rooms](user-findrooms.md) in a specific room list.</span></span>


## <a name="permissions"></a><span data-ttu-id="43e4a-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="43e4a-110">Permissions</span></span>
<span data-ttu-id="43e4a-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="43e4a-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="43e4a-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="43e4a-113">Permission type</span></span>      | <span data-ttu-id="43e4a-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="43e4a-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="43e4a-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="43e4a-115">Delegated (work or school account)</span></span> | <span data-ttu-id="43e4a-116">User.ReadBasic.All, User.Read.All</span><span class="sxs-lookup"><span data-stu-id="43e4a-116">User.ReadBasic.All, User.Read.All</span></span>    |
|<span data-ttu-id="43e4a-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="43e4a-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="43e4a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="43e4a-118">Not supported.</span></span>    |
|<span data-ttu-id="43e4a-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="43e4a-119">Application</span></span> | <span data-ttu-id="43e4a-120">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="43e4a-120">User.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="43e4a-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="43e4a-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/findRoomLists
GET /users/<id>/findRoomLists

```

## <a name="request-headers"></a><span data-ttu-id="43e4a-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="43e4a-122">Request headers</span></span>
| <span data-ttu-id="43e4a-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="43e4a-123">Name</span></span>       | <span data-ttu-id="43e4a-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="43e4a-124">Type</span></span> | <span data-ttu-id="43e4a-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="43e4a-125">Description</span></span> |
|:---------------|:----------|:----------|
| <span data-ttu-id="43e4a-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="43e4a-126">Authorization</span></span>  | <span data-ttu-id="43e4a-127">string</span><span class="sxs-lookup"><span data-stu-id="43e4a-127">string</span></span>  | <span data-ttu-id="43e4a-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="43e4a-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="43e4a-130">Content-Type</span><span class="sxs-lookup"><span data-stu-id="43e4a-130">Content-Type</span></span>  | <span data-ttu-id="43e4a-131">string</span><span class="sxs-lookup"><span data-stu-id="43e4a-131">string</span></span>  | <span data-ttu-id="43e4a-p105">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="43e4a-p105">application/json. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="43e4a-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="43e4a-134">Request body</span></span>
<span data-ttu-id="43e4a-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="43e4a-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="43e4a-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43e4a-136">Response</span></span>

<span data-ttu-id="43e4a-137">Si tiene éxito, este método devuelve una `200 OK` objeto de colección de respuesta [emailAddress](../resources/emailaddress.md) y de código en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43e4a-137">If successful, this method returns a `200 OK` response code and [emailAddress](../resources/emailaddress.md) collection object in the response body.</span></span>

<span data-ttu-id="43e4a-138">Si no hay listas definidas en el inquilino, se devuelve una matriz vacía.</span><span class="sxs-lookup"><span data-stu-id="43e4a-138">If no lists are defined in the tenant, then an empty array is returned.</span></span>

## <a name="example"></a><span data-ttu-id="43e4a-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="43e4a-139">Example</span></span>
##### <a name="request"></a><span data-ttu-id="43e4a-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="43e4a-140">Request</span></span>

<span data-ttu-id="43e4a-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="43e4a-141">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "user_get_room_lists"
}-->
```http
GET https://graph.microsoft.com/beta/me/findRoomLists
```

##### <a name="response"></a><span data-ttu-id="43e4a-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43e4a-142">Response</span></span>
<span data-ttu-id="43e4a-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43e4a-143">Here is an example of the response.</span></span> 

<span data-ttu-id="43e4a-p106">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="43e4a-p106">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "name": "user_get_room_lists",
  "truncated": true,
  "@odata.type": "microsoft.graph.emailAddress",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.emailAddress)",
    "value": [
        {
            "name": "Building 1 Rooms",
            "address": "Building1Rooms@contoso.onmicrosoft.com"
        },
        {
            "name": "Building 2 Rooms",
            "address": "Building2Rooms@contoso.onmicrosoft.com"
        }
    ]
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: findRoomLists",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

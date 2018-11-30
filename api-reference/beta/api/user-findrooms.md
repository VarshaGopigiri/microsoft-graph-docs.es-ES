---
title: 'usuario: findRooms'
description: 'Obtenga todas las salas de reuniones en el inquilino del usuario o en una lista de salas específicas. '
ms.openlocfilehash: 3169202f83af0696cbd2aaadd83d3beb9a3c01d8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088495"
---
# <a name="user-findrooms"></a><span data-ttu-id="573eb-103">usuario: findRooms</span><span class="sxs-lookup"><span data-stu-id="573eb-103">user: findRooms</span></span>

> <span data-ttu-id="573eb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="573eb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="573eb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="573eb-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="573eb-106">Obtenga todas las salas de reuniones en el inquilino del usuario o en una lista de salas específicas.</span><span class="sxs-lookup"><span data-stu-id="573eb-106">Get all the meeting rooms in the user's tenant or in a specific room list.</span></span> 

<span data-ttu-id="573eb-107">Los inquilinos pueden organizar las salas de reuniones en listas de las salas.</span><span class="sxs-lookup"><span data-stu-id="573eb-107">Tenants can organize meeting rooms into room lists.</span></span> <span data-ttu-id="573eb-108">Cada sala de reuniones y la lista de salas está representada por una instancia de [emailAddress](../resources/emailaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="573eb-108">Each meeting room and room list is represented by an [emailAddress](../resources/emailaddress.md) instance.</span></span> <span data-ttu-id="573eb-109">Puede [obtener todas las listas de sala](user-findroomlists.md) en el inquilino, obtener todas las salas de los inquilinos, u obtenga todos los salones de en una lista de salas específicas.</span><span class="sxs-lookup"><span data-stu-id="573eb-109">You can [get all the room lists](user-findroomlists.md) in the tenant, get all the rooms in the tenant, or get all the rooms in a specific room list.</span></span> <span data-ttu-id="573eb-110">Puede obtener una copia de seguridad a los salones de 100 en primer lugar en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="573eb-110">You can get up to the first 100 rooms in the tenant.</span></span>

## <a name="permissions"></a><span data-ttu-id="573eb-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="573eb-111">Permissions</span></span>
<span data-ttu-id="573eb-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="573eb-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="573eb-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="573eb-114">Permission type</span></span>      | <span data-ttu-id="573eb-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="573eb-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="573eb-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="573eb-116">Delegated (work or school account)</span></span> | <span data-ttu-id="573eb-117">User.ReadBasic.All, User.Read.All</span><span class="sxs-lookup"><span data-stu-id="573eb-117">User.ReadBasic.All, User.Read.All</span></span>    |
|<span data-ttu-id="573eb-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="573eb-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="573eb-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="573eb-119">Not supported.</span></span>    |
|<span data-ttu-id="573eb-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="573eb-120">Application</span></span> | <span data-ttu-id="573eb-121">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="573eb-121">User.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="573eb-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="573eb-122">HTTP request</span></span>

<span data-ttu-id="573eb-123">Para obtener todas las salas en el inquilino:</span><span class="sxs-lookup"><span data-stu-id="573eb-123">To get all the rooms in the tenant:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/findRooms
GET /users/<id>/findRooms
```

<span data-ttu-id="573eb-124">Para obtener todas las salas de una lista de salas específicas del inquilino:</span><span class="sxs-lookup"><span data-stu-id="573eb-124">To get all the rooms in a specific room list of the tenant's:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/findRooms(RoomList='{room_list}')
GET /users/<id>/findRooms(RoomList='{room_list}')
```

## <a name="query-parameters"></a><span data-ttu-id="573eb-125">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="573eb-125">Query parameters</span></span>

| <span data-ttu-id="573eb-126">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="573eb-126">Query parameter</span></span>       | <span data-ttu-id="573eb-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="573eb-127">Type</span></span> | <span data-ttu-id="573eb-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="573eb-128">Description</span></span> |
|:---------------|:----------|:----------|
| <span data-ttu-id="573eb-129">RoomList</span><span class="sxs-lookup"><span data-stu-id="573eb-129">RoomList</span></span> | <span data-ttu-id="573eb-130">string</span><span class="sxs-lookup"><span data-stu-id="573eb-130">string</span></span> | <span data-ttu-id="573eb-131">La dirección SMTP asociada con la lista de salas.</span><span class="sxs-lookup"><span data-stu-id="573eb-131">The SMTP address associated with the room list.</span></span> <span data-ttu-id="573eb-132">Cada lista de salas está representada por una instancia de [emailAddress](../resources/emailaddress.md) que incluya una dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="573eb-132">Each room list is represented by an [emailAddress](../resources/emailaddress.md) instance that includes an SMTP address.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="573eb-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="573eb-133">Request headers</span></span>
| <span data-ttu-id="573eb-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="573eb-134">Name</span></span>       | <span data-ttu-id="573eb-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="573eb-135">Type</span></span> | <span data-ttu-id="573eb-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="573eb-136">Description</span></span> |
|:---------------|:----------|:----------|
| <span data-ttu-id="573eb-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="573eb-137">Authorization</span></span>  | <span data-ttu-id="573eb-138">string</span><span class="sxs-lookup"><span data-stu-id="573eb-138">string</span></span>  | <span data-ttu-id="573eb-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="573eb-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="573eb-141">Content-Type</span><span class="sxs-lookup"><span data-stu-id="573eb-141">Content-Type</span></span>  | <span data-ttu-id="573eb-142">string</span><span class="sxs-lookup"><span data-stu-id="573eb-142">string</span></span>  | <span data-ttu-id="573eb-p106">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="573eb-p106">application/json. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="573eb-145">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="573eb-145">Request body</span></span>
<span data-ttu-id="573eb-146">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="573eb-146">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="573eb-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="573eb-147">Response</span></span>

<span data-ttu-id="573eb-148">Si tiene éxito, este método devuelve una `200 OK` objeto de colección de respuesta [emailAddress](../resources/emailaddress.md) y de código en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="573eb-148">If successful, this method returns a `200 OK` response code and [emailAddress](../resources/emailaddress.md) collection object in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="573eb-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="573eb-149">Example</span></span>

##### <a name="request-1"></a><span data-ttu-id="573eb-150">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="573eb-150">Request 1</span></span>

<span data-ttu-id="573eb-151">El primer ejemplo obtiene todos los salones de definidos en el inquilino del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="573eb-151">The first example gets all the rooms defined in the signed-in user's tenant.</span></span>

<!-- {
  "blockType": "request",
  "name": "user_get_rooms_in_tenant"
}-->
```http
GET https://graph.microsoft.com/beta/me/findRooms
```

##### <a name="response-1"></a><span data-ttu-id="573eb-152">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="573eb-152">Response 1</span></span>
<span data-ttu-id="573eb-153">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="573eb-153">Here is an example of the response.</span></span> 

<span data-ttu-id="573eb-p107">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="573eb-p107">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "name": "user_get_rooms_in_tenant",
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
            "name": "Conf Room Adams",
            "address": "Adams@contoso.onmicrosoft.com"
        },
        {
            "name": "Conf Room Baker",
            "address": "Baker@contoso.onmicrosoft.com"
        },
        {
            "name": "Conf Room Crystal",
            "address": "Crystal@contoso.onmicrosoft.com"
        },
        {
            "name": "Conf Room Hood",
            "address": "Hood@contoso.onmicrosoft.com"
        },
        {
            "name": "Conf Room Rainier",
            "address": "Rainier@contoso.onmicrosoft.com"
        },
        {
            "name": "Conf Room Stevens",
            "address": "Stevens@contoso.onmicrosoft.com"
        }
    ]
}
```

##### <a name="request-2"></a><span data-ttu-id="573eb-156">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="573eb-156">Request 2</span></span>

<span data-ttu-id="573eb-157">El segundo ejemplo obtiene las salas en la lista de salas especificado identificado por la dirección de correo electrónico Building2Rooms@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="573eb-157">The second example gets the rooms in the specified room list identified by the email address Building2Rooms@contoso.onmicrosoft.com.</span></span>

<!-- {
  "blockType": "request",
  "name": "user_get_rooms_from_specific_list"
}-->
```http
GET https://graph.microsoft.com/beta/me/findRooms(RoomList='Building2Rooms@contoso.onmicrosoft.com') 
```

##### <a name="response-2"></a><span data-ttu-id="573eb-158">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="573eb-158">Response 2</span></span>
<span data-ttu-id="573eb-159">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="573eb-159">Here is an example of the response.</span></span> 

<span data-ttu-id="573eb-p108">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="573eb-p108">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "name": "user_get_rooms_from_specific_list",
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
            "name": "Conf Room Baker",
            "address": "Baker@contoso.onmicrosoft.com"
        },
        {
            "name": "Conf Room Hood",
            "address": "Hood@contoso.onmicrosoft.com"
        },
        {
            "name": "Conf Room Rainier",
            "address": "Rainier@contoso.onmicrosoft.com"
        }
    ]
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: findRooms",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
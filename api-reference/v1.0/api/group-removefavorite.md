---
title: 'group: removeFavorite'
description: Quita el grupo de la lista de grupos favoritos del usuario actual. Solo es compatible con Grupos de Office 365.
ms.openlocfilehash: d599b0057e12acadcae7b8c74709bdad6651cdc6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030497"
---
# <a name="group-removefavorite"></a><span data-ttu-id="a92db-104">group: removeFavorite</span><span class="sxs-lookup"><span data-stu-id="a92db-104">group: removeFavorite</span></span>
<span data-ttu-id="a92db-p102">Quita el grupo de la lista de grupos favoritos del usuario actual. Solo es compatible con Grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="a92db-p102">Remove the group from the list of the current user's favorite groups. Supported for Office 365 Groups only.</span></span>

## <a name="permissions"></a><span data-ttu-id="a92db-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a92db-107">Permissions</span></span>
<span data-ttu-id="a92db-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a92db-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a92db-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a92db-110">Permission type</span></span>      | <span data-ttu-id="a92db-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a92db-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a92db-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a92db-112">Delegated (work or school account)</span></span> | <span data-ttu-id="a92db-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a92db-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="a92db-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a92db-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a92db-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a92db-115">Not supported.</span></span>    |
|<span data-ttu-id="a92db-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a92db-116">Application</span></span> | <span data-ttu-id="a92db-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a92db-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a92db-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a92db-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/removeFavorite
```
## <a name="request-headers"></a><span data-ttu-id="a92db-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a92db-119">Request headers</span></span>
| <span data-ttu-id="a92db-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a92db-120">Header</span></span>       | <span data-ttu-id="a92db-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a92db-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a92db-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="a92db-122">Authorization</span></span>  | <span data-ttu-id="a92db-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a92db-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="a92db-125">Prefer</span><span class="sxs-lookup"><span data-stu-id="a92db-125">Prefer</span></span> | <span data-ttu-id="a92db-126">return=minimal.</span><span class="sxs-lookup"><span data-stu-id="a92db-126">return=minimal.</span></span> <span data-ttu-id="a92db-127">Si el encabezado de respuesta “mínimo” se incluye en el encabezado de solicitud, una respuesta correcta devolverá un código `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="a92db-127">If minimal response header is included in the request header, then a successful response returns `204 No Content` code.</span></span> <span data-ttu-id="a92db-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a92db-128">Optional.</span></span>  | 

## <a name="request-body"></a><span data-ttu-id="a92db-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a92db-129">Request body</span></span>
<span data-ttu-id="a92db-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a92db-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a92db-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a92db-131">Response</span></span>
<span data-ttu-id="a92db-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a92db-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a92db-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a92db-134">Example</span></span>
#### <a name="request"></a><span data-ttu-id="a92db-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a92db-135">Request</span></span>
<span data-ttu-id="a92db-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a92db-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_removefavorite"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/removeFavorite
```

#### <a name="response"></a><span data-ttu-id="a92db-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a92db-137">Response</span></span>
<span data-ttu-id="a92db-138">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a92db-138">The following is an example of the response.</span></span>
<!-- {
  "blockType": "response"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: removeFavorite",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
---
title: Enumerar fotos
description: Recupere una lista de objetos profilePhoto.
author: dkershaw10
ms.openlocfilehash: fda70cc81e0a98f8527e8bd00e980a5092804f6d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27353707"
---
# <a name="list-photos"></a><span data-ttu-id="168ea-103">Enumerar fotos</span><span class="sxs-lookup"><span data-stu-id="168ea-103">List photos</span></span>
<span data-ttu-id="168ea-104">Recupere una lista de objetos [profilePhoto](../resources/profilephoto.md).</span><span class="sxs-lookup"><span data-stu-id="168ea-104">Retrieve a list of [profilePhoto](../resources/profilephoto.md) objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="168ea-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="168ea-105">Permissions</span></span>
<span data-ttu-id="168ea-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="168ea-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="168ea-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="168ea-108">Permission type</span></span>      | <span data-ttu-id="168ea-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="168ea-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="168ea-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="168ea-110">Delegated (work or school account)</span></span> | <span data-ttu-id="168ea-111">Group.ReadBasic.All, Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="168ea-111">Group.ReadBasic.All, Group.Read.All, Group.ReadWrite.All</span></span> |
|<span data-ttu-id="168ea-112">Delegado (cuenta Microsoft personal)</span><span class="sxs-lookup"><span data-stu-id="168ea-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="168ea-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="168ea-113">Not supported.</span></span>    |
|<span data-ttu-id="168ea-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="168ea-114">Application</span></span> | <span data-ttu-id="168ea-115">Group.ReadBasic.All, Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="168ea-115">Group.ReadBasic.All, Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="168ea-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="168ea-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/photos
GET /users/{id | userPrincipalName}/joinedGroups/{id}/photos
```
## <a name="optional-query-parameters"></a><span data-ttu-id="168ea-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="168ea-117">Optional query parameters</span></span>
<span data-ttu-id="168ea-118">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="168ea-118">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="168ea-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="168ea-119">Request headers</span></span>
| <span data-ttu-id="168ea-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="168ea-120">Name</span></span>       | <span data-ttu-id="168ea-121">Type</span><span class="sxs-lookup"><span data-stu-id="168ea-121">Type</span></span> | <span data-ttu-id="168ea-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="168ea-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="168ea-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="168ea-123">Authorization</span></span>  | <span data-ttu-id="168ea-124">string</span><span class="sxs-lookup"><span data-stu-id="168ea-124">string</span></span>  | <span data-ttu-id="168ea-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="168ea-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="168ea-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="168ea-127">Request body</span></span>
<span data-ttu-id="168ea-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="168ea-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="168ea-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="168ea-129">Response</span></span>
<span data-ttu-id="168ea-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [profilePhoto](../resources/profilephoto.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="168ea-130">If successful, this method returns a `200 OK` response code and collection of [profilePhoto](../resources/profilephoto.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="168ea-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="168ea-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="168ea-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="168ea-132">Request</span></span>
<span data-ttu-id="168ea-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="168ea-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_photos"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/photos
```

#### <a name="response"></a><span data-ttu-id="168ea-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="168ea-134">Response</span></span>
<span data-ttu-id="168ea-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="168ea-135">The following is an example of the response.</span></span>
><span data-ttu-id="168ea-136">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="168ea-136">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="168ea-137">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="168ea-137">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.profilePhoto",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 94

{
  "value": [
    {
      "height": 99,
      "width": 99,
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List photos",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

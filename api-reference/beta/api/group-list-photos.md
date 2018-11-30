---
title: Enumerar fotos
description: Recupere una lista de objetos profilePhoto.
ms.openlocfilehash: c6f7ea9b530e08f2a3b348396e004a9b4341e4fd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085844"
---
# <a name="list-photos"></a><span data-ttu-id="d3caf-103">Enumerar fotos</span><span class="sxs-lookup"><span data-stu-id="d3caf-103">List photos</span></span>

> <span data-ttu-id="d3caf-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d3caf-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d3caf-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d3caf-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d3caf-106">Recupere una lista de objetos [profilePhoto](../resources/profilephoto.md).</span><span class="sxs-lookup"><span data-stu-id="d3caf-106">Retrieve a list of [profilePhoto](../resources/profilephoto.md) objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="d3caf-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d3caf-107">Permissions</span></span>
<span data-ttu-id="d3caf-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d3caf-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d3caf-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d3caf-110">Permission type</span></span>      | <span data-ttu-id="d3caf-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d3caf-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d3caf-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d3caf-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d3caf-113">Group.ReadBasic.All, Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d3caf-113">Group.ReadBasic.All, Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="d3caf-114">Delegado (cuenta Microsoft personal)</span><span class="sxs-lookup"><span data-stu-id="d3caf-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d3caf-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d3caf-115">Not supported.</span></span>    |
|<span data-ttu-id="d3caf-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d3caf-116">Application</span></span> | <span data-ttu-id="d3caf-117">Group.ReadBasic.All, Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d3caf-117">Group.ReadBasic.All, Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d3caf-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d3caf-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/photos
GET /users/{id | userPrincipalName}/joinedGroups/{id}/photos
```

## <a name="optional-query-parameters"></a><span data-ttu-id="d3caf-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d3caf-119">Optional query parameters</span></span>
<span data-ttu-id="d3caf-120">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d3caf-120">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="d3caf-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d3caf-121">Request headers</span></span>
| <span data-ttu-id="d3caf-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="d3caf-122">Name</span></span>       | <span data-ttu-id="d3caf-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="d3caf-123">Type</span></span> | <span data-ttu-id="d3caf-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3caf-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="d3caf-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="d3caf-125">Authorization</span></span>  | <span data-ttu-id="d3caf-126">string</span><span class="sxs-lookup"><span data-stu-id="d3caf-126">string</span></span>  | <span data-ttu-id="d3caf-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d3caf-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d3caf-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d3caf-129">Request body</span></span>
<span data-ttu-id="d3caf-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d3caf-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d3caf-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d3caf-131">Response</span></span>
<span data-ttu-id="d3caf-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [profilePhoto](../resources/profilephoto.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d3caf-132">If successful, this method returns a `200 OK` response code and collection of [profilePhoto](../resources/profilephoto.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d3caf-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d3caf-133">Example</span></span>
#### <a name="request"></a><span data-ttu-id="d3caf-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d3caf-134">Request</span></span>
<span data-ttu-id="d3caf-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d3caf-135">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_photos"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}/photos
```

#### <a name="response"></a><span data-ttu-id="d3caf-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d3caf-136">Response</span></span>
<span data-ttu-id="d3caf-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d3caf-137">The following is an example of the response.</span></span>
><span data-ttu-id="d3caf-138">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="d3caf-138">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="d3caf-139">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d3caf-139">All the properties will be returned from an actual call.</span></span>
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
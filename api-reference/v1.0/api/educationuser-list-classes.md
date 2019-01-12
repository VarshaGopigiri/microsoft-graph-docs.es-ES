---
title: Enumerar clases
description: 'Recupere una lista de los objetos de clase. Tenga en cuenta que si se usa el token delegado, los miembros solo pueden ver información sobre sus propias clases. '
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: 1f8cc6a1dbda0f86e808d72bfc91339af58afa33
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966940"
---
# <a name="list-classes"></a><span data-ttu-id="45636-104">Enumerar clases</span><span class="sxs-lookup"><span data-stu-id="45636-104">List classes</span></span>

<span data-ttu-id="45636-105">Recupere una lista de los objetos de clase.</span><span class="sxs-lookup"><span data-stu-id="45636-105">Retrieve a list of class objects.</span></span> <span data-ttu-id="45636-106">Tenga en cuenta que si se usa el token delegado, los miembros solo pueden ver información sobre sus propias clases.</span><span class="sxs-lookup"><span data-stu-id="45636-106">Note that if the delegated token is used, members can only see information about their own classes.</span></span> 

<!-- Please verify the revision to the delegated token text. -->

## <a name="permissions"></a><span data-ttu-id="45636-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="45636-107">Permissions</span></span>
<span data-ttu-id="45636-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="45636-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="45636-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="45636-110">Permission type</span></span>      | <span data-ttu-id="45636-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="45636-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="45636-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="45636-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="45636-113">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="45636-113">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="45636-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="45636-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="45636-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="45636-115">Not supported.</span></span>  |
|<span data-ttu-id="45636-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="45636-116">Application</span></span> | <span data-ttu-id="45636-117">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="45636-117">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="45636-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="45636-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/me/classes
GET /education/users/{id}/classes
```
## <a name="optional-query-parameters"></a><span data-ttu-id="45636-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="45636-119">Optional query parameters</span></span>
<span data-ttu-id="45636-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45636-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="45636-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="45636-121">Request headers</span></span>
| <span data-ttu-id="45636-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45636-122">Header</span></span>       | <span data-ttu-id="45636-123">Valor</span><span class="sxs-lookup"><span data-stu-id="45636-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="45636-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="45636-124">Authorization</span></span>  | <span data-ttu-id="45636-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="45636-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="45636-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="45636-127">Request body</span></span>
<span data-ttu-id="45636-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="45636-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="45636-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="45636-129">Response</span></span>
<span data-ttu-id="45636-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45636-130">If successful, this method returns a `200 OK` response code and a collection of [educationClass](../resources/educationclass.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="45636-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="45636-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="45636-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="45636-132">Request</span></span>
<span data-ttu-id="45636-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="45636-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_classes"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/me/classes
```
##### <a name="response"></a><span data-ttu-id="45636-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="45636-134">Response</span></span>
<span data-ttu-id="45636-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45636-135">The following is an example of the response.</span></span> 

><span data-ttu-id="45636-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="45636-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationClass",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 277

{
  "value": [
    {
      "id": "11019",
      "description": "Health Level 1",
      "classCode": "Health 501",
      "createdBy": {
        "user": {
          "displayName": "Susana Rocha",
          "id": "14012",
        }
      },
      "displayName": "Health 1",
      "externalId": "11019",
      "externalName": "Health Level 1",
      "externalSource": "sis",
      "mailNickname": "fineartschool.net"
    } 
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List classes",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

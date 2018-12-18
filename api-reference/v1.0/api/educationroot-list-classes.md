---
title: Enumerar clases
description: 'Recupere una lista de todos los objetos de clase. '
author: mmast-msft
ms.openlocfilehash: ecc6cc0735464515da885a68213eb600a042a0dc
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27353686"
---
# <a name="list-classes"></a><span data-ttu-id="bf28e-103">Enumerar clases</span><span class="sxs-lookup"><span data-stu-id="bf28e-103">List classes</span></span>

<span data-ttu-id="bf28e-104">Recupere una lista de todos los objetos de clase.</span><span class="sxs-lookup"><span data-stu-id="bf28e-104">Retrieve a list of all class objects.</span></span> 

## <a name="permissions"></a><span data-ttu-id="bf28e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="bf28e-105">Permissions</span></span>
<span data-ttu-id="bf28e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bf28e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bf28e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bf28e-108">Permission type</span></span>      | <span data-ttu-id="bf28e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bf28e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bf28e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bf28e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="bf28e-111">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="bf28e-111">EduRoster.ReadBasic</span></span> |
|<span data-ttu-id="bf28e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bf28e-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="bf28e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf28e-113">Not supported.</span></span>  |
|<span data-ttu-id="bf28e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bf28e-114">Application</span></span> | <span data-ttu-id="bf28e-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bf28e-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="bf28e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bf28e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes
```
## <a name="optional-query-parameters"></a><span data-ttu-id="bf28e-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bf28e-117">Optional query parameters</span></span>
<span data-ttu-id="bf28e-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf28e-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="bf28e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bf28e-119">Request headers</span></span>
| <span data-ttu-id="bf28e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf28e-120">Header</span></span>       | <span data-ttu-id="bf28e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bf28e-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="bf28e-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="bf28e-122">Authorization</span></span>  | <span data-ttu-id="bf28e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bf28e-p102">Bearer {token}. Required.</span></span>  |


## <a name="request-body"></a><span data-ttu-id="bf28e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bf28e-125">Request body</span></span>
<span data-ttu-id="bf28e-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bf28e-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="bf28e-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf28e-127">Response</span></span>
<span data-ttu-id="bf28e-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf28e-128">If successful, this method returns a `200 OK` response code and a collection of [educationClass](../resources/educationclass.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bf28e-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bf28e-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bf28e-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bf28e-130">Request</span></span>
<span data-ttu-id="bf28e-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf28e-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_classes"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/classes
```
##### <a name="response"></a><span data-ttu-id="bf28e-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf28e-132">Response</span></span>
<span data-ttu-id="bf28e-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf28e-133">The following is an example of the response.</span></span> 

><span data-ttu-id="bf28e-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bf28e-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
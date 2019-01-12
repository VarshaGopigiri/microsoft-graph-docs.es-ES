---
title: Enumerar educationClasses
description: Recupere una lista de las clases de un centro educativo.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: d49e8094e28cf8c5901bfd36d9e9af02c97e2eee
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991513"
---
# <a name="list-educationclasses"></a><span data-ttu-id="a9afe-103">Enumerar educationClasses</span><span class="sxs-lookup"><span data-stu-id="a9afe-103">List educationClasses</span></span>

<span data-ttu-id="a9afe-104">Recupere una lista de las clases de un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="a9afe-104">Retrieve a list of classes owned by a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="a9afe-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="a9afe-105">Permissions</span></span>
<span data-ttu-id="a9afe-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a9afe-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a9afe-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a9afe-108">Permission type</span></span>      | <span data-ttu-id="a9afe-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a9afe-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a9afe-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a9afe-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="a9afe-111">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="a9afe-111">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="a9afe-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a9afe-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="a9afe-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a9afe-113">Not supported.</span></span>  |
|<span data-ttu-id="a9afe-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a9afe-114">Application</span></span> | <span data-ttu-id="a9afe-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a9afe-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="a9afe-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a9afe-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/schools/{id}/classes
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a9afe-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a9afe-117">Optional query parameters</span></span>
<span data-ttu-id="a9afe-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a9afe-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a9afe-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a9afe-119">Request headers</span></span>
| <span data-ttu-id="a9afe-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9afe-120">Header</span></span>       | <span data-ttu-id="a9afe-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a9afe-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a9afe-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="a9afe-122">Authorization</span></span>  | <span data-ttu-id="a9afe-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a9afe-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a9afe-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a9afe-125">Request body</span></span>
<span data-ttu-id="a9afe-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a9afe-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="a9afe-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a9afe-127">Response</span></span>
<span data-ttu-id="a9afe-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a9afe-128">If successful, this method returns a `200 OK` response code and a collection of [educationClass](../resources/educationclass.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a9afe-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a9afe-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a9afe-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a9afe-130">Request</span></span>
<span data-ttu-id="a9afe-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a9afe-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_classes"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/schools/{school-id}/classes
```
##### <a name="response"></a><span data-ttu-id="a9afe-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a9afe-132">Response</span></span>
<span data-ttu-id="a9afe-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a9afe-133">The following is an example of the response.</span></span> 

><span data-ttu-id="a9afe-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a9afe-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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

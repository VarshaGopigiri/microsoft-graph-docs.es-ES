---
title: Enumerar clases
description: 'Recupere una lista de los objetos de clase. Tenga en cuenta que si se usa el token delegado, los miembros solo pueden ver información sobre sus propias clases. '
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: fe950190ce3bd56b5f236f42a840d3d0b9f5d130
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960927"
---
# <a name="list-classes"></a><span data-ttu-id="d16bb-104">Enumerar clases</span><span class="sxs-lookup"><span data-stu-id="d16bb-104">List classes</span></span>

> <span data-ttu-id="d16bb-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d16bb-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d16bb-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d16bb-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d16bb-107">Recupere una lista de los objetos de clase.</span><span class="sxs-lookup"><span data-stu-id="d16bb-107">Retrieve a list of class objects.</span></span> <span data-ttu-id="d16bb-108">Tenga en cuenta que si se usa el token delegado, los miembros solo pueden ver información sobre sus propias clases.</span><span class="sxs-lookup"><span data-stu-id="d16bb-108">Note that if the delegated token is used, members can only see information about their own classes.</span></span> 

<!-- Please verify the revision to the delegated token text. -->

## <a name="permissions"></a><span data-ttu-id="d16bb-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="d16bb-109">Permissions</span></span>
<span data-ttu-id="d16bb-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d16bb-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d16bb-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d16bb-112">Permission type</span></span>      | <span data-ttu-id="d16bb-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d16bb-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d16bb-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d16bb-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="d16bb-115">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="d16bb-115">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="d16bb-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d16bb-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="d16bb-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d16bb-117">Not supported.</span></span>  |
|<span data-ttu-id="d16bb-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d16bb-118">Application</span></span> | <span data-ttu-id="d16bb-119">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d16bb-119">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="d16bb-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d16bb-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/me/classes
GET /education/users/{id}/classes
```
## <a name="optional-query-parameters"></a><span data-ttu-id="d16bb-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d16bb-121">Optional query parameters</span></span>
<span data-ttu-id="d16bb-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d16bb-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="d16bb-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d16bb-123">Request headers</span></span>
| <span data-ttu-id="d16bb-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d16bb-124">Header</span></span>       | <span data-ttu-id="d16bb-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d16bb-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d16bb-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="d16bb-126">Authorization</span></span>  | <span data-ttu-id="d16bb-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d16bb-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d16bb-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d16bb-129">Request body</span></span>
<span data-ttu-id="d16bb-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d16bb-130">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="d16bb-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d16bb-131">Response</span></span>
<span data-ttu-id="d16bb-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d16bb-132">If successful, this method returns a `200 OK` response code and a collection of [educationClass](../resources/educationclass.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d16bb-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d16bb-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d16bb-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d16bb-134">Request</span></span>
<span data-ttu-id="d16bb-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d16bb-135">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_classes"
}-->
```http
GET https://graph.microsoft.com/beta/education/me/classes
```
##### <a name="response"></a><span data-ttu-id="d16bb-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d16bb-136">Response</span></span>
<span data-ttu-id="d16bb-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d16bb-137">The following is an example of the response.</span></span> 

><span data-ttu-id="d16bb-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d16bb-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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

---
title: Enumerar educationClasses
description: Recupere una lista de las clases de un centro educativo.
ms.openlocfilehash: 4ae84796c903edef5215232dcd260f86a0ea5c87
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083611"
---
# <a name="list-educationclasses"></a><span data-ttu-id="1d679-103">Enumerar educationClasses</span><span class="sxs-lookup"><span data-stu-id="1d679-103">List educationClasses</span></span>

> <span data-ttu-id="1d679-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1d679-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1d679-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1d679-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1d679-106">Recupere una lista de las clases de un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="1d679-106">Retrieve a list of classes owned by a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="1d679-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1d679-107">Permissions</span></span>
<span data-ttu-id="1d679-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1d679-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1d679-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1d679-110">Permission type</span></span>      | <span data-ttu-id="1d679-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1d679-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1d679-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1d679-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="1d679-113">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="1d679-113">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="1d679-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1d679-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="1d679-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d679-115">Not supported.</span></span>  |
|<span data-ttu-id="1d679-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1d679-116">Application</span></span> | <span data-ttu-id="1d679-117">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1d679-117">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="1d679-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1d679-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/schools/{id}/classes
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1d679-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1d679-119">Optional query parameters</span></span>
<span data-ttu-id="1d679-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d679-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1d679-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d679-121">Request headers</span></span>
| <span data-ttu-id="1d679-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d679-122">Header</span></span>       | <span data-ttu-id="1d679-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1d679-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="1d679-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="1d679-124">Authorization</span></span>  | <span data-ttu-id="1d679-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1d679-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="1d679-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1d679-127">Request body</span></span>
<span data-ttu-id="1d679-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1d679-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="1d679-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d679-129">Response</span></span>
<span data-ttu-id="1d679-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d679-130">If successful, this method returns a `200 OK` response code and a collection of [educationClass](../resources/educationclass.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1d679-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d679-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1d679-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d679-132">Request</span></span>
<span data-ttu-id="1d679-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d679-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_classes"
}-->
```http
GET https://graph.microsoft.com/beta/education/schools/10002/classes
```
##### <a name="response"></a><span data-ttu-id="1d679-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d679-134">Response</span></span>
<span data-ttu-id="1d679-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d679-135">The following is an example of the response.</span></span> 

><span data-ttu-id="1d679-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1d679-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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

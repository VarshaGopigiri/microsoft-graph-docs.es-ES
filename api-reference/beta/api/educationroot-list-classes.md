---
title: Enumerar clases
description: 'Recupere una lista de todos los objetos de clase. '
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 2be32a833d407eee51f5372c3eff55e19081fc37
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27920285"
---
# <a name="list-classes"></a><span data-ttu-id="52668-103">Enumerar clases</span><span class="sxs-lookup"><span data-stu-id="52668-103">List classes</span></span>

> <span data-ttu-id="52668-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="52668-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="52668-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="52668-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="52668-106">Recupere una lista de todos los objetos de clase.</span><span class="sxs-lookup"><span data-stu-id="52668-106">Retrieve a list of all class objects.</span></span> 

## <a name="permissions"></a><span data-ttu-id="52668-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="52668-107">Permissions</span></span>
<span data-ttu-id="52668-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="52668-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="52668-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="52668-110">Permission type</span></span>      | <span data-ttu-id="52668-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="52668-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="52668-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="52668-112">Delegated (work or school account)</span></span> | <span data-ttu-id="52668-113">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="52668-113">EduRoster.ReadBasic</span></span> |
|<span data-ttu-id="52668-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="52668-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="52668-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="52668-115">Not supported.</span></span>  |
|<span data-ttu-id="52668-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="52668-116">Application</span></span> | <span data-ttu-id="52668-117">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="52668-117">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="52668-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="52668-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes
```
## <a name="optional-query-parameters"></a><span data-ttu-id="52668-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="52668-119">Optional query parameters</span></span>
<span data-ttu-id="52668-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52668-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="52668-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="52668-121">Request headers</span></span>
| <span data-ttu-id="52668-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52668-122">Header</span></span>       | <span data-ttu-id="52668-123">Valor</span><span class="sxs-lookup"><span data-stu-id="52668-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="52668-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="52668-124">Authorization</span></span>  | <span data-ttu-id="52668-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="52668-p103">Bearer {token}. Required.</span></span>  |


## <a name="request-body"></a><span data-ttu-id="52668-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="52668-127">Request body</span></span>
<span data-ttu-id="52668-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="52668-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="52668-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52668-129">Response</span></span>
<span data-ttu-id="52668-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52668-130">If successful, this method returns a `200 OK` response code and a collection of [educationClass](../resources/educationclass.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="52668-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="52668-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="52668-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="52668-132">Request</span></span>
<span data-ttu-id="52668-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="52668-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_classes"
}-->
```http
GET https://graph.microsoft.com/beta/education/classes
```
##### <a name="response"></a><span data-ttu-id="52668-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52668-134">Response</span></span>
<span data-ttu-id="52668-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52668-135">The following is an example of the response.</span></span> 

><span data-ttu-id="52668-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="52668-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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

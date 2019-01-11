---
title: List overrides
description: Obtiene los reemplazos que un usuario ha configurado para clasificar siempre los mensajes de determinados remitentes de forma específica.
localization_priority: Normal
ms.openlocfilehash: ab8324ac892df570ed0d28fabb7b31f3280adcef
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883898"
---
# <a name="list-overrides"></a><span data-ttu-id="e1ef5-103">List overrides</span><span class="sxs-lookup"><span data-stu-id="e1ef5-103">List overrides</span></span>

<span data-ttu-id="e1ef5-104">Obtiene los reemplazos que un usuario ha configurado para clasificar siempre los mensajes de determinados remitentes de forma específica.</span><span class="sxs-lookup"><span data-stu-id="e1ef5-104">Get the overrides that a user has set up to always classify messages from certain senders in specific ways.</span></span>

<span data-ttu-id="e1ef5-p101">Cada reemplazo corresponde a una dirección SMTP de un remitente. Inicialmente, un usuario no tiene ningún reemplazo.</span><span class="sxs-lookup"><span data-stu-id="e1ef5-p101">Each override corresponds to an SMTP address of a sender. Initially, a user does not have any overrides.</span></span>
## <a name="permissions"></a><span data-ttu-id="e1ef5-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e1ef5-107">Permissions</span></span>
<span data-ttu-id="e1ef5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e1ef5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e1ef5-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e1ef5-110">Permission type</span></span>      | <span data-ttu-id="e1ef5-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e1ef5-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e1ef5-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e1ef5-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e1ef5-113">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="e1ef5-113">Mail.Read</span></span>    |
|<span data-ttu-id="e1ef5-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e1ef5-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e1ef5-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="e1ef5-115">Mail.Read</span></span>    |
|<span data-ttu-id="e1ef5-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e1ef5-116">Application</span></span> | <span data-ttu-id="e1ef5-117">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="e1ef5-117">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="e1ef5-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e1ef5-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/inferenceClassification/overrides
GET /users/{id}/inferenceClassification/overrides
```

## <a name="request-headers"></a><span data-ttu-id="e1ef5-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e1ef5-119">Request headers</span></span>
| <span data-ttu-id="e1ef5-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="e1ef5-120">Name</span></span>       | <span data-ttu-id="e1ef5-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1ef5-121">Type</span></span> | <span data-ttu-id="e1ef5-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1ef5-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="e1ef5-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e1ef5-123">Authorization</span></span>  | <span data-ttu-id="e1ef5-124">string</span><span class="sxs-lookup"><span data-stu-id="e1ef5-124">string</span></span>  | <span data-ttu-id="e1ef5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e1ef5-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e1ef5-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e1ef5-127">Request body</span></span>
<span data-ttu-id="e1ef5-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e1ef5-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e1ef5-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1ef5-129">Response</span></span>

<span data-ttu-id="e1ef5-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) en el cuerpo de la respuesta. Se devuelve una colección vacía si el usuario no ha configurado ningún reemplazo.</span><span class="sxs-lookup"><span data-stu-id="e1ef5-p104">If successful, this method returns a `200 OK` response code and a collection of [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) objects in the response body. An empty collection is returned if the user doesn't have any overrides set up.</span></span>
## <a name="example"></a><span data-ttu-id="e1ef5-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e1ef5-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e1ef5-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e1ef5-133">Request</span></span>
<span data-ttu-id="e1ef5-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e1ef5-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_overrides"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/inferenceClassification/overrides
```
##### <a name="response"></a><span data-ttu-id="e1ef5-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1ef5-135">Response</span></span>
<span data-ttu-id="e1ef5-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e1ef5-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.inferenceClassificationOverride",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "classifyAs": "focused",
      "senderEmailAddress": {
        "name": "Samantha Booth",
        "address": "samanthab@adatum.onmicrosoft.com"
      },
      "id": "98f5bdef-576a-404d-a2ea-07a3cf11a9b9"
    },
    {
      "classifyAs": "other",
      "senderEmailAddress": {
        "name": "Randi Welch",
        "address": "randiw@adatum.onmicrosoft.com"
      },
      "id": "98f5bdef-576a-404d-a2ea-07a3cf34af4r"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List overrides",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

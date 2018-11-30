---
title: List overrides
description: Obtiene los reemplazos que un usuario ha configurado para clasificar siempre los mensajes de determinados remitentes de forma específica.
ms.openlocfilehash: 7953c776b60f4e63aec03245817bfcf6630bbdf8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028894"
---
# <a name="list-overrides"></a><span data-ttu-id="90b6c-103">List overrides</span><span class="sxs-lookup"><span data-stu-id="90b6c-103">List overrides</span></span>

<span data-ttu-id="90b6c-104">Obtiene los reemplazos que un usuario ha configurado para clasificar siempre los mensajes de determinados remitentes de forma específica.</span><span class="sxs-lookup"><span data-stu-id="90b6c-104">Get the overrides that a user has set up to always classify messages from certain senders in specific ways.</span></span>

<span data-ttu-id="90b6c-p101">Cada reemplazo corresponde a una dirección SMTP de un remitente. Inicialmente, un usuario no tiene ningún reemplazo.</span><span class="sxs-lookup"><span data-stu-id="90b6c-p101">Each override corresponds to an SMTP address of a sender. Initially, a user does not have any overrides.</span></span>
## <a name="permissions"></a><span data-ttu-id="90b6c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="90b6c-107">Permissions</span></span>
<span data-ttu-id="90b6c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="90b6c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="90b6c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="90b6c-110">Permission type</span></span>      | <span data-ttu-id="90b6c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="90b6c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="90b6c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="90b6c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="90b6c-113">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="90b6c-113">Mail.Read</span></span>    |
|<span data-ttu-id="90b6c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="90b6c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="90b6c-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="90b6c-115">Mail.Read</span></span>    |
|<span data-ttu-id="90b6c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="90b6c-116">Application</span></span> | <span data-ttu-id="90b6c-117">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="90b6c-117">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="90b6c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="90b6c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/inferenceClassification/overrides
GET /users/{id}/inferenceClassification/overrides
```

## <a name="request-headers"></a><span data-ttu-id="90b6c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="90b6c-119">Request headers</span></span>
| <span data-ttu-id="90b6c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="90b6c-120">Name</span></span>       | <span data-ttu-id="90b6c-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="90b6c-121">Type</span></span> | <span data-ttu-id="90b6c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="90b6c-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="90b6c-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="90b6c-123">Authorization</span></span>  | <span data-ttu-id="90b6c-124">string</span><span class="sxs-lookup"><span data-stu-id="90b6c-124">string</span></span>  | <span data-ttu-id="90b6c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90b6c-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="90b6c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="90b6c-127">Request body</span></span>
<span data-ttu-id="90b6c-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="90b6c-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="90b6c-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90b6c-129">Response</span></span>

<span data-ttu-id="90b6c-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) en el cuerpo de la respuesta. Se devuelve una colección vacía si el usuario no ha configurado ningún reemplazo.</span><span class="sxs-lookup"><span data-stu-id="90b6c-p104">If successful, this method returns a `200 OK` response code and a collection of [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) objects in the response body. An empty collection is returned if the user doesn't have any overrides set up.</span></span>
## <a name="example"></a><span data-ttu-id="90b6c-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="90b6c-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="90b6c-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="90b6c-133">Request</span></span>
<span data-ttu-id="90b6c-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="90b6c-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_overrides"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/inferenceClassification/overrides
```
##### <a name="response"></a><span data-ttu-id="90b6c-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90b6c-135">Response</span></span>
<span data-ttu-id="90b6c-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="90b6c-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
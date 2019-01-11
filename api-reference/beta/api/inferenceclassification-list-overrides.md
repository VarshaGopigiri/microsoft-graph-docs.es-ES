---
title: List overrides
description: Obtenga las invalidaciones de centrada en la Bandeja de entrada que un usuario ha configurado para clasificar siempre los mensajes de determinados remitentes de forma específica.
localization_priority: Normal
ms.openlocfilehash: 6d2d731858ad3a87cad10b4feb23378cb4dab992
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27837558"
---
# <a name="list-overrides"></a><span data-ttu-id="e2190-103">List overrides</span><span class="sxs-lookup"><span data-stu-id="e2190-103">List overrides</span></span>

> <span data-ttu-id="e2190-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e2190-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e2190-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e2190-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e2190-106">Obtenga las invalidaciones de [Centrada en la Bandeja de entrada](../resources/manage-focused-inbox.md) que un usuario ha configurado para clasificar siempre los mensajes de determinados remitentes de forma específica.</span><span class="sxs-lookup"><span data-stu-id="e2190-106">Get the [Focused Inbox](../resources/manage-focused-inbox.md) overrides that a user has set up to always classify messages from certain senders in specific ways.</span></span>

<span data-ttu-id="e2190-p102">Cada reemplazo corresponde a una dirección SMTP de un remitente. Inicialmente, un usuario no tiene ningún reemplazo.</span><span class="sxs-lookup"><span data-stu-id="e2190-p102">Each override corresponds to an SMTP address of a sender. Initially, a user does not have any overrides.</span></span>
## <a name="permissions"></a><span data-ttu-id="e2190-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="e2190-109">Permissions</span></span>
<span data-ttu-id="e2190-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e2190-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e2190-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e2190-112">Permission type</span></span>      | <span data-ttu-id="e2190-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e2190-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e2190-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e2190-114">Delegated (work or school account)</span></span> | <span data-ttu-id="e2190-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="e2190-115">Mail.Read</span></span>    |
|<span data-ttu-id="e2190-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e2190-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e2190-117">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="e2190-117">Mail.Read</span></span>    |
|<span data-ttu-id="e2190-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e2190-118">Application</span></span> | <span data-ttu-id="e2190-119">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="e2190-119">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="e2190-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e2190-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/inferenceClassification/overrides
GET /users/{id}/inferenceClassification/overrides
```

## <a name="request-headers"></a><span data-ttu-id="e2190-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e2190-121">Request headers</span></span>
| <span data-ttu-id="e2190-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="e2190-122">Name</span></span>       | <span data-ttu-id="e2190-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2190-123">Type</span></span> | <span data-ttu-id="e2190-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2190-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="e2190-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="e2190-125">Authorization</span></span>  | <span data-ttu-id="e2190-126">string</span><span class="sxs-lookup"><span data-stu-id="e2190-126">string</span></span>  | <span data-ttu-id="e2190-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e2190-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e2190-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e2190-129">Request body</span></span>
<span data-ttu-id="e2190-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e2190-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e2190-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e2190-131">Response</span></span>

<span data-ttu-id="e2190-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e2190-132">If successful, this method returns a `200 OK` response code and a collection of [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e2190-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e2190-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e2190-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e2190-134">Request</span></span>
<span data-ttu-id="e2190-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2190-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_overrides"
}-->
```http
GET https://graph.microsoft.com/beta/me/inferenceClassification/overrides
```
##### <a name="response"></a><span data-ttu-id="e2190-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e2190-136">Response</span></span>
<span data-ttu-id="e2190-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e2190-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

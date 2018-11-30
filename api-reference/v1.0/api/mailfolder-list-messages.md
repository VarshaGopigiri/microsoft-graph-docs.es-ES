---
title: List messages
description: Obtiene todos los mensajes en el buzón del usuario que inició sesión o esos mensajes en una carpeta especificada en el buzón.
ms.openlocfilehash: deb46ec472bd05c2ae038fdcfbc808ed51b48f30
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031322"
---
# <a name="list-messages"></a><span data-ttu-id="51bc7-103">List messages</span><span class="sxs-lookup"><span data-stu-id="51bc7-103">List messages</span></span>

<span data-ttu-id="51bc7-104">Obtiene todos los mensajes en el buzón del usuario que inició sesión o esos mensajes en una carpeta especificada en el buzón.</span><span class="sxs-lookup"><span data-stu-id="51bc7-104">Get all the messages in the signed-in user's mailbox, or those messages in a specified folder in the mailbox.</span></span>
## <a name="permissions"></a><span data-ttu-id="51bc7-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="51bc7-105">Permissions</span></span>
<span data-ttu-id="51bc7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="51bc7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="51bc7-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="51bc7-108">Permission type</span></span>      | <span data-ttu-id="51bc7-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="51bc7-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="51bc7-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="51bc7-110">Delegated (work or school account)</span></span> | <span data-ttu-id="51bc7-111">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="51bc7-111">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="51bc7-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="51bc7-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="51bc7-113">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="51bc7-113">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="51bc7-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="51bc7-114">Application</span></span> | <span data-ttu-id="51bc7-115">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="51bc7-115">Mail.Read, Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="51bc7-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="51bc7-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}/messages
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages
```
## <a name="optional-query-parameters"></a><span data-ttu-id="51bc7-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="51bc7-117">Optional query parameters</span></span>
<span data-ttu-id="51bc7-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="51bc7-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="51bc7-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="51bc7-119">Request headers</span></span>
| <span data-ttu-id="51bc7-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="51bc7-120">Name</span></span>       | <span data-ttu-id="51bc7-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="51bc7-121">Type</span></span> | <span data-ttu-id="51bc7-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="51bc7-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="51bc7-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="51bc7-123">Authorization</span></span>  | <span data-ttu-id="51bc7-124">string</span><span class="sxs-lookup"><span data-stu-id="51bc7-124">string</span></span>  | <span data-ttu-id="51bc7-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="51bc7-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="51bc7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="51bc7-127">Request body</span></span>
<span data-ttu-id="51bc7-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="51bc7-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="51bc7-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51bc7-129">Response</span></span>

<span data-ttu-id="51bc7-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="51bc7-130">If successful, this method returns a `200 OK` response code and collection of [Message](../resources/message.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="51bc7-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="51bc7-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="51bc7-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="51bc7-132">Request</span></span>
<span data-ttu-id="51bc7-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="51bc7-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_messages"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/{id}/messages
```
##### <a name="response"></a><span data-ttu-id="51bc7-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51bc7-134">Response</span></span>
<span data-ttu-id="51bc7-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="51bc7-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 317

{
  "value": [
    {
      "receivedDateTime": "datetime-value",
      "sentDateTime": "datetime-value",
      "hasAttachments": true,
      "subject": "subject-value",
      "body": {
        "contentType": "",
        "content": "content-value"
      },
      "bodyPreview": "bodyPreview-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List messages",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

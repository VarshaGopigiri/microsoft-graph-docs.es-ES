---
title: Eliminar messageRule
description: Eliminar el objeto messageRule especificado.
author: angelgolfer-ms
ms.openlocfilehash: 5fe208b72ddc28ca3d2ee5d2b0f1c48113e49c64
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343466"
---
# <a name="delete-messagerule"></a><span data-ttu-id="fe205-103">Eliminar messageRule</span><span class="sxs-lookup"><span data-stu-id="fe205-103">Delete messageRule</span></span>


<span data-ttu-id="fe205-104">Eliminar el objeto [messageRule](../resources/messagerule.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="fe205-104">Delete the specified [messageRule](../resources/messagerule.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="fe205-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="fe205-105">Permissions</span></span>
<span data-ttu-id="fe205-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fe205-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fe205-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fe205-108">Permission type</span></span>      | <span data-ttu-id="fe205-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fe205-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fe205-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fe205-110">Delegated (work or school account)</span></span> | <span data-ttu-id="fe205-111">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fe205-111">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="fe205-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fe205-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fe205-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fe205-113">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="fe205-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fe205-114">Application</span></span> | <span data-ttu-id="fe205-115">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fe205-115">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="fe205-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fe205-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/mailFolders/inbox/messageRules/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/inbox/messageRules/{id}
```
## <a name="request-headers"></a><span data-ttu-id="fe205-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fe205-117">Request headers</span></span>
| <span data-ttu-id="fe205-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="fe205-118">Name</span></span>       | <span data-ttu-id="fe205-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe205-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="fe205-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="fe205-120">Authorization</span></span>  | <span data-ttu-id="fe205-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fe205-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="fe205-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fe205-123">Request body</span></span>
<span data-ttu-id="fe205-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fe205-124">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="fe205-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe205-125">Response</span></span>
<span data-ttu-id="fe205-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe205-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fe205-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fe205-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fe205-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fe205-129">Request</span></span>
<span data-ttu-id="fe205-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fe205-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["inbox", "AQAAAJ5dZp8="],
  "name": "delete_messagerule"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messageRules/AQAAAJ5dZp8=

```
##### <a name="response"></a><span data-ttu-id="fe205-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe205-131">Response</span></span>
<span data-ttu-id="fe205-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe205-132">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "isEmpty": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete rule",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
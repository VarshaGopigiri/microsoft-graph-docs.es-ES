---
title: Eliminar messageRule
description: Eliminar el objeto messageRule especificado.
author: angelgolfer-ms
ms.openlocfilehash: e10cebf6b2758a21a8bf70e505edcebb7f27082c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27305379"
---
# <a name="delete-messagerule"></a><span data-ttu-id="cea39-103">Eliminar messageRule</span><span class="sxs-lookup"><span data-stu-id="cea39-103">Delete messageRule</span></span>

> <span data-ttu-id="cea39-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cea39-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cea39-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cea39-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cea39-106">Eliminar el objeto [messageRule](../resources/messagerule.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="cea39-106">Delete the specified [messageRule](../resources/messagerule.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="cea39-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="cea39-107">Permissions</span></span>
<span data-ttu-id="cea39-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cea39-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cea39-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cea39-110">Permission type</span></span>      | <span data-ttu-id="cea39-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cea39-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cea39-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cea39-112">Delegated (work or school account)</span></span> | <span data-ttu-id="cea39-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cea39-113">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="cea39-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cea39-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cea39-115">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cea39-115">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="cea39-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cea39-116">Application</span></span> | <span data-ttu-id="cea39-117">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cea39-117">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="cea39-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cea39-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/mailFolders/inbox/messagerules/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/inbox/messagerules/{id}
```
## <a name="request-headers"></a><span data-ttu-id="cea39-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cea39-119">Request headers</span></span>
| <span data-ttu-id="cea39-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="cea39-120">Name</span></span>       | <span data-ttu-id="cea39-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="cea39-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="cea39-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="cea39-122">Authorization</span></span>  | <span data-ttu-id="cea39-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cea39-p103">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="cea39-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cea39-125">Request body</span></span>
<span data-ttu-id="cea39-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cea39-126">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="cea39-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cea39-127">Response</span></span>
<span data-ttu-id="cea39-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cea39-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cea39-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cea39-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="cea39-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cea39-131">Request</span></span>
<span data-ttu-id="cea39-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cea39-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_messagerule"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/mailfolders/inbox/messagerules('AQAAAJ5dZp8=')

```
##### <a name="response"></a><span data-ttu-id="cea39-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cea39-133">Response</span></span>
<span data-ttu-id="cea39-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cea39-134">Here is an example of the response.</span></span> 
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
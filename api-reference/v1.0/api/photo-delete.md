---
title: Delete photo
description: Elimina una foto.
ms.openlocfilehash: 8d00eb3685d349efaa88981c6a725faa97896bb2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031486"
---
# <a name="delete-photo"></a><span data-ttu-id="1a819-103">Delete photo</span><span class="sxs-lookup"><span data-stu-id="1a819-103">Delete photo</span></span>

<span data-ttu-id="1a819-104">Elimina una foto.</span><span class="sxs-lookup"><span data-stu-id="1a819-104">Delete a photo.</span></span>
## <a name="permissions"></a><span data-ttu-id="1a819-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1a819-105">Permissions</span></span>
<span data-ttu-id="1a819-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1a819-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1a819-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1a819-108">Permission type</span></span>      | <span data-ttu-id="1a819-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1a819-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1a819-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1a819-110">Delegated (work or school account)</span></span> | <span data-ttu-id="1a819-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1a819-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="1a819-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1a819-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1a819-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1a819-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="1a819-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1a819-114">Application</span></span> | <span data-ttu-id="1a819-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1a819-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1a819-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1a819-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /users/{id | userPrincipalName}/photo
DELETE /groups/{id}/photo
DELETE /drive/root/createdByUser/photo

```
## <a name="request-headers"></a><span data-ttu-id="1a819-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1a819-117">Request headers</span></span>
| <span data-ttu-id="1a819-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="1a819-118">Name</span></span>       | <span data-ttu-id="1a819-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="1a819-119">Type</span></span> | <span data-ttu-id="1a819-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="1a819-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="1a819-121">if-match</span><span class="sxs-lookup"><span data-stu-id="1a819-121">if-match</span></span>  | <span data-ttu-id="1a819-122">string</span><span class="sxs-lookup"><span data-stu-id="1a819-122">string</span></span>  | <span data-ttu-id="1a819-123">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide con la etiqueta actual del archivo, se devuelve una respuesta `412 Precondition Failed` y el elemento no se borrará.</span><span class="sxs-lookup"><span data-stu-id="1a819-123">If this request header is included and the eTag (or cTag) provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span>|
| <span data-ttu-id="1a819-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="1a819-124">Authorization</span></span>  | <span data-ttu-id="1a819-125">string</span><span class="sxs-lookup"><span data-stu-id="1a819-125">string</span></span>  | <span data-ttu-id="1a819-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a819-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1a819-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1a819-128">Request body</span></span>
<span data-ttu-id="1a819-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1a819-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1a819-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1a819-130">Response</span></span>

<span data-ttu-id="1a819-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a819-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1a819-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1a819-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1a819-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1a819-134">Request</span></span>
<span data-ttu-id="1a819-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1a819-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
"name": "delete_photo"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/users/{id|userPrincipalName}/photo
```
##### <a name="response"></a><span data-ttu-id="1a819-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1a819-136">Response</span></span>
<span data-ttu-id="1a819-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a819-137">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete photo",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

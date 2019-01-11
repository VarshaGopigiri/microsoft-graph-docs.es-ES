---
title: Delete photo
description: Elimina una foto.
localization_priority: Normal
ms.openlocfilehash: 117f4acbf5a45d9db64ccc5d3fc0ccc4d1c64896
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27829263"
---
# <a name="delete-photo"></a><span data-ttu-id="50e24-103">Delete photo</span><span class="sxs-lookup"><span data-stu-id="50e24-103">Delete photo</span></span>

> <span data-ttu-id="50e24-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="50e24-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="50e24-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="50e24-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="50e24-106">Elimina una foto.</span><span class="sxs-lookup"><span data-stu-id="50e24-106">Delete a photo.</span></span>
## <a name="permissions"></a><span data-ttu-id="50e24-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="50e24-107">Permissions</span></span>
<span data-ttu-id="50e24-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="50e24-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="50e24-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="50e24-110">Permission type</span></span>      | <span data-ttu-id="50e24-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="50e24-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="50e24-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="50e24-112">Delegated (work or school account)</span></span> | <span data-ttu-id="50e24-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="50e24-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="50e24-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="50e24-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="50e24-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="50e24-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="50e24-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="50e24-116">Application</span></span> | <span data-ttu-id="50e24-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="50e24-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="50e24-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="50e24-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /users/{id | userPrincipalName}/photo
DELETE /groups/{id}/photo
DELETE /drive/root/createdByUser/photo

```
## <a name="request-headers"></a><span data-ttu-id="50e24-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="50e24-119">Request headers</span></span>
| <span data-ttu-id="50e24-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="50e24-120">Name</span></span>       | <span data-ttu-id="50e24-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="50e24-121">Type</span></span> | <span data-ttu-id="50e24-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="50e24-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="50e24-123">if-match</span><span class="sxs-lookup"><span data-stu-id="50e24-123">if-match</span></span>  | <span data-ttu-id="50e24-124">string</span><span class="sxs-lookup"><span data-stu-id="50e24-124">string</span></span>  | <span data-ttu-id="50e24-125">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide con la etiqueta actual del archivo, se devuelve una respuesta `412 Precondition Failed` y el elemento no se borrará.</span><span class="sxs-lookup"><span data-stu-id="50e24-125">If this request header is included and the eTag (or cTag) provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span>|
| <span data-ttu-id="50e24-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="50e24-126">Authorization</span></span>  | <span data-ttu-id="50e24-127">string</span><span class="sxs-lookup"><span data-stu-id="50e24-127">string</span></span>  | <span data-ttu-id="50e24-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="50e24-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="50e24-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="50e24-130">Request body</span></span>
<span data-ttu-id="50e24-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="50e24-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="50e24-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50e24-132">Response</span></span>

<span data-ttu-id="50e24-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="50e24-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="50e24-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="50e24-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="50e24-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="50e24-136">Request</span></span>
<span data-ttu-id="50e24-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="50e24-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_photo"
}-->
```http
DELETE https://graph.microsoft.com/beta/users/{id|userPrincipalName}/photo
```
##### <a name="response"></a><span data-ttu-id="50e24-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50e24-138">Response</span></span>
<span data-ttu-id="50e24-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="50e24-139">Here is an example of the response.</span></span>
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

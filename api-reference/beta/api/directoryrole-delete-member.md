---
title: Eliminar miembro del rol de directorio
description: Elimine un miembro de un directoryRole.
ms.openlocfilehash: 9ef64e3aa1833fe78e5a035f7bd8ef4692fa371b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086249"
---
# <a name="remove-directory-role-member"></a><span data-ttu-id="71c18-103">Eliminar miembro del rol de directorio</span><span class="sxs-lookup"><span data-stu-id="71c18-103">Remove directory role member</span></span>

> <span data-ttu-id="71c18-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="71c18-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="71c18-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="71c18-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="71c18-106">Elimine un miembro de un directoryRole.</span><span class="sxs-lookup"><span data-stu-id="71c18-106">Remove a member from a directoryRole.</span></span>

## <a name="permissions"></a><span data-ttu-id="71c18-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="71c18-107">Permissions</span></span>

<span data-ttu-id="71c18-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="71c18-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="71c18-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="71c18-110">Permission type</span></span>      | <span data-ttu-id="71c18-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="71c18-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="71c18-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="71c18-112">Delegated (work or school account)</span></span> | <span data-ttu-id="71c18-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="71c18-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="71c18-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="71c18-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="71c18-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71c18-115">Not supported.</span></span>    |
|<span data-ttu-id="71c18-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="71c18-116">Application</span></span> | <span data-ttu-id="71c18-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71c18-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="71c18-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71c18-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /directoryroles/{id}/members/{id}/$ref
```

## <a name="request-headers"></a><span data-ttu-id="71c18-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71c18-119">Request headers</span></span>

| <span data-ttu-id="71c18-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="71c18-120">Name</span></span>       | <span data-ttu-id="71c18-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="71c18-121">Type</span></span> | <span data-ttu-id="71c18-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="71c18-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="71c18-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="71c18-123">Authorization</span></span>  | <span data-ttu-id="71c18-124">string</span><span class="sxs-lookup"><span data-stu-id="71c18-124">string</span></span>  | <span data-ttu-id="71c18-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="71c18-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="71c18-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="71c18-127">Request body</span></span>

<span data-ttu-id="71c18-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="71c18-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="71c18-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71c18-129">Response</span></span>

<span data-ttu-id="71c18-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71c18-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="71c18-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71c18-132">Example</span></span>

##### <a name="request"></a><span data-ttu-id="71c18-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71c18-133">Request</span></span>

<span data-ttu-id="71c18-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="71c18-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_directoryobject_from_directoryrole"
}-->

```http
DELETE https://graph.microsoft.com/beta/directoryroles/{id}/members/{id}/$ref
```

##### <a name="response"></a><span data-ttu-id="71c18-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71c18-135">Response</span></span>

<span data-ttu-id="71c18-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71c18-136">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete a member",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
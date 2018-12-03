---
title: 'group: resetUnseenCount'
description: Restablecer el unseenCount de todas las entradas del blog que el usuario actual no ha visto desde la última visita. Compatible con sólo los grupos de Office 365.
ms.openlocfilehash: b6218176f097759870aad4a3a2908759862002e2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090424"
---
# <a name="group-resetunseencount"></a><span data-ttu-id="065b2-104">group: resetUnseenCount</span><span class="sxs-lookup"><span data-stu-id="065b2-104">group: resetUnseenCount</span></span>

> <span data-ttu-id="065b2-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="065b2-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="065b2-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="065b2-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="065b2-107">Restablecer el unseenCount de todas las entradas del blog que el usuario actual no ha visto desde la última visita.</span><span class="sxs-lookup"><span data-stu-id="065b2-107">Reset the unseenCount of all the posts that the current user has not seen since their last visit.</span></span> <span data-ttu-id="065b2-108">Compatible con sólo los grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="065b2-108">Supported for Office 365 Groups only.</span></span>

## <a name="permissions"></a><span data-ttu-id="065b2-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="065b2-109">Permissions</span></span>
<span data-ttu-id="065b2-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="065b2-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="065b2-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="065b2-112">Permission type</span></span>      | <span data-ttu-id="065b2-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="065b2-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="065b2-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="065b2-114">Delegated (work or school account)</span></span> | <span data-ttu-id="065b2-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="065b2-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="065b2-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="065b2-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="065b2-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="065b2-117">Not supported.</span></span>    |
|<span data-ttu-id="065b2-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="065b2-118">Application</span></span> | <span data-ttu-id="065b2-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="065b2-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="065b2-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="065b2-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/resetUnseenCount
```
## <a name="request-headers"></a><span data-ttu-id="065b2-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="065b2-121">Request headers</span></span>
| <span data-ttu-id="065b2-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="065b2-122">Header</span></span>       | <span data-ttu-id="065b2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="065b2-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="065b2-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="065b2-124">Authorization</span></span>  | <span data-ttu-id="065b2-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="065b2-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="065b2-127">Prefer</span><span class="sxs-lookup"><span data-stu-id="065b2-127">Prefer</span></span> | <span data-ttu-id="065b2-128">return=minimal.</span><span class="sxs-lookup"><span data-stu-id="065b2-128">return=minimal.</span></span> <span data-ttu-id="065b2-129">Si el encabezado de respuesta “mínimo” se incluye en el encabezado de solicitud, una respuesta correcta devolverá un código `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="065b2-129">If minimal response header is included in the request header, then a successful response returns `204 No Content` code.</span></span> <span data-ttu-id="065b2-130">Opcional.</span><span class="sxs-lookup"><span data-stu-id="065b2-130">Optional.</span></span>  | 

## <a name="request-body"></a><span data-ttu-id="065b2-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="065b2-131">Request body</span></span>
<span data-ttu-id="065b2-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="065b2-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="065b2-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="065b2-133">Response</span></span>
<span data-ttu-id="065b2-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="065b2-p107">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="065b2-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="065b2-136">Example</span></span>
#### <a name="request"></a><span data-ttu-id="065b2-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="065b2-137">Request</span></span>
<span data-ttu-id="065b2-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="065b2-138">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_resetunseencount"
}-->
```http
POST https://graph.microsoft.com/beta/groups/{id}/resetUnseenCount
```

#### <a name="response"></a><span data-ttu-id="065b2-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="065b2-139">Response</span></span>
<span data-ttu-id="065b2-140">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="065b2-140">The following is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: resetUnseenCount",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
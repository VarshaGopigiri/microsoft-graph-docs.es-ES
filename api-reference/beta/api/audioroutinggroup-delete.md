---
title: Eliminar el grupo de enrutamiento de audio
description: Eliminar el audioRoutingGroup especificado.
ms.openlocfilehash: cb4b4c2cf3f7023332acd443c63463d5251963ad
ms.sourcegitcommit: 4a46cfd112c8089fc07e4e5ccdccaf415a3a0e7f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/05/2018
ms.locfileid: "27155994"
---
# <a name="delete-audio-routing-group"></a><span data-ttu-id="203d1-103">Eliminar el grupo de enrutamiento de audio</span><span class="sxs-lookup"><span data-stu-id="203d1-103">Delete audio routing group</span></span>

> <span data-ttu-id="203d1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="203d1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="203d1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="203d1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="203d1-106">Eliminar el especificado [audioRoutingGroup](../resources/audioroutinggroup.md).</span><span class="sxs-lookup"><span data-stu-id="203d1-106">Delete the specified [audioRoutingGroup](../resources/audioroutinggroup.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="203d1-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="203d1-107">Permissions</span></span>
<span data-ttu-id="203d1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="203d1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="203d1-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="203d1-110">Permission type</span></span> | <span data-ttu-id="203d1-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="203d1-111">Permissions (from least to most privileged)</span></span>  |
| :-------------- | :------------------------------------------- |
| <span data-ttu-id="203d1-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="203d1-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="203d1-113">No se admite</span><span class="sxs-lookup"><span data-stu-id="203d1-113">Not Supported</span></span>        |
| <span data-ttu-id="203d1-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="203d1-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="203d1-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="203d1-115">Not Supported</span></span>        |
| <span data-ttu-id="203d1-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="203d1-116">Application</span></span>     | <span data-ttu-id="203d1-117">Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span><span class="sxs-lookup"><span data-stu-id="203d1-117">Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="203d1-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="203d1-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /app/calls/{id}/audioRoutingGroups/{id}
DELETE /applications/{id}/calls/{id}/audioRoutingGroups/{id}
```

## <a name="request-headers"></a><span data-ttu-id="203d1-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="203d1-119">Request headers</span></span>
| <span data-ttu-id="203d1-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="203d1-120">Name</span></span>          | <span data-ttu-id="203d1-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="203d1-121">Description</span></span>               |
|:--------------|:--------------------------|
| <span data-ttu-id="203d1-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="203d1-122">Authorization</span></span> | <span data-ttu-id="203d1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="203d1-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="203d1-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="203d1-125">Request body</span></span>
<span data-ttu-id="203d1-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="203d1-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="203d1-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="203d1-127">Response</span></span>
<span data-ttu-id="203d1-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="203d1-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="203d1-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="203d1-130">Example</span></span>

##### <a name="request"></a><span data-ttu-id="203d1-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="203d1-131">Request</span></span>
<span data-ttu-id="203d1-132">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="203d1-132">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_audioRoutingGroup"
}-->
```http
DELETE https://graph.microsoft.com/beta/app/calls/{id}/audioRoutingGroups/{id}
```

##### <a name="response"></a><span data-ttu-id="203d1-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="203d1-133">Response</span></span>

> <span data-ttu-id="203d1-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="203d1-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
  "description": "Delete audioRoutingGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

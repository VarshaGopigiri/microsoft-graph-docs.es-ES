---
title: Eliminar calendarGroup
description: Elimine un grupo de calendarios que no sea el predeterminado.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: f1dded8885f99646d48ddf309ff12e64d61988e1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27978938"
---
# <a name="delete-calendargroup"></a><span data-ttu-id="1c397-103">Eliminar calendarGroup</span><span class="sxs-lookup"><span data-stu-id="1c397-103">Delete calendarGroup</span></span>

<span data-ttu-id="1c397-104">Elimine un grupo de calendarios que no sea el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1c397-104">Delete a calendar group other than the default calendar group.</span></span>

## <a name="permissions"></a><span data-ttu-id="1c397-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1c397-105">Permissions</span></span>

<span data-ttu-id="1c397-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1c397-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="1c397-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1c397-108">Permission type</span></span>                        | <span data-ttu-id="1c397-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1c397-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="1c397-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1c397-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="1c397-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1c397-111">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="1c397-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1c397-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1c397-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1c397-113">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="1c397-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1c397-114">Application</span></span>                            | <span data-ttu-id="1c397-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1c397-115">Calendars.ReadWrite</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="1c397-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1c397-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/calendarGroups/{id}
DELETE /users/{id | userPrincipalName}/calendarGroups/{id}
```

## <a name="request-headers"></a><span data-ttu-id="1c397-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1c397-117">Request headers</span></span>

| <span data-ttu-id="1c397-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="1c397-118">Name</span></span>          | <span data-ttu-id="1c397-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c397-119">Type</span></span>   | <span data-ttu-id="1c397-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c397-120">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="1c397-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="1c397-121">Authorization</span></span> | <span data-ttu-id="1c397-122">string</span><span class="sxs-lookup"><span data-stu-id="1c397-122">string</span></span> | <span data-ttu-id="1c397-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1c397-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1c397-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1c397-125">Request body</span></span>

<span data-ttu-id="1c397-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1c397-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1c397-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c397-127">Response</span></span>

<span data-ttu-id="1c397-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1c397-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1c397-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1c397-130">Example</span></span>

##### <a name="request"></a><span data-ttu-id="1c397-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1c397-131">Request</span></span>

<span data-ttu-id="1c397-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1c397-132">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_calendargroup"
}-->

```http
DELETE https://graph.microsoft.com/v1.0/me/calendarGroups/{id}
```

##### <a name="response"></a><span data-ttu-id="1c397-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c397-133">Response</span></span>

<span data-ttu-id="1c397-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1c397-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
  "description": "Delete calendarGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

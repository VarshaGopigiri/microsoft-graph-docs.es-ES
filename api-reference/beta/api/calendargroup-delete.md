---
title: Eliminar calendarGroup
description: Elimine un grupo de calendarios que no sea el predeterminado.
ms.openlocfilehash: e71d05a8a0205b10d8735ea0e7baf32f201c7e15
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086272"
---
# <a name="delete-calendargroup"></a><span data-ttu-id="8f1d0-103">Eliminar calendarGroup</span><span class="sxs-lookup"><span data-stu-id="8f1d0-103">Delete calendarGroup</span></span>

> <span data-ttu-id="8f1d0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8f1d0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8f1d0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8f1d0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8f1d0-106">Elimine un grupo de calendarios que no sea el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8f1d0-106">Delete a calendar group other than the default calendar group.</span></span>

## <a name="permissions"></a><span data-ttu-id="8f1d0-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="8f1d0-107">Permissions</span></span>

<span data-ttu-id="8f1d0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8f1d0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="8f1d0-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8f1d0-110">Permission type</span></span>                        | <span data-ttu-id="8f1d0-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8f1d0-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="8f1d0-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8f1d0-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="8f1d0-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f1d0-113">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="8f1d0-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8f1d0-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8f1d0-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f1d0-115">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="8f1d0-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8f1d0-116">Application</span></span>                            | <span data-ttu-id="8f1d0-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f1d0-117">Calendars.ReadWrite</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="8f1d0-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8f1d0-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/calendarGroups/{id}
DELETE /users/{id | userPrincipalName}/calendarGroups/{id}
```

## <a name="request-headers"></a><span data-ttu-id="8f1d0-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8f1d0-119">Request headers</span></span>

| <span data-ttu-id="8f1d0-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f1d0-120">Name</span></span>          | <span data-ttu-id="8f1d0-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f1d0-121">Type</span></span>   | <span data-ttu-id="8f1d0-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f1d0-122">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="8f1d0-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="8f1d0-123">Authorization</span></span> | <span data-ttu-id="8f1d0-124">string</span><span class="sxs-lookup"><span data-stu-id="8f1d0-124">string</span></span> | <span data-ttu-id="8f1d0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8f1d0-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8f1d0-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8f1d0-127">Request body</span></span>

<span data-ttu-id="8f1d0-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8f1d0-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8f1d0-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f1d0-129">Response</span></span>

<span data-ttu-id="8f1d0-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f1d0-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8f1d0-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8f1d0-132">Example</span></span>

##### <a name="request"></a><span data-ttu-id="8f1d0-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8f1d0-133">Request</span></span>

<span data-ttu-id="8f1d0-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f1d0-134">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_calendargroup"
}-->

```http
DELETE https://graph.microsoft.com/beta/me/calendarGroups/{id}
```

##### <a name="response"></a><span data-ttu-id="8f1d0-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f1d0-135">Response</span></span>

<span data-ttu-id="8f1d0-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8f1d0-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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

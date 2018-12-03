---
title: Eliminar calendarGroup
description: Elimine un grupo de calendarios que no sea el predeterminado.
ms.openlocfilehash: 64fa9069ba54c7549392db4fc2d3d47b4e95ebdc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030343"
---
# <a name="delete-calendargroup"></a><span data-ttu-id="a7452-103">Eliminar calendarGroup</span><span class="sxs-lookup"><span data-stu-id="a7452-103">Delete calendarGroup</span></span>

<span data-ttu-id="a7452-104">Elimine un grupo de calendarios que no sea el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a7452-104">Delete a calendar group other than the default calendar group.</span></span>

## <a name="permissions"></a><span data-ttu-id="a7452-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="a7452-105">Permissions</span></span>

<span data-ttu-id="a7452-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a7452-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="a7452-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a7452-108">Permission type</span></span>                        | <span data-ttu-id="a7452-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a7452-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="a7452-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a7452-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="a7452-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a7452-111">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="a7452-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a7452-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a7452-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a7452-113">Calendars.ReadWrite</span></span>                         |
| <span data-ttu-id="a7452-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a7452-114">Application</span></span>                            | <span data-ttu-id="a7452-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a7452-115">Calendars.ReadWrite</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="a7452-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a7452-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/calendarGroups/{id}
DELETE /users/{id | userPrincipalName}/calendarGroups/{id}
```

## <a name="request-headers"></a><span data-ttu-id="a7452-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a7452-117">Request headers</span></span>

| <span data-ttu-id="a7452-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="a7452-118">Name</span></span>          | <span data-ttu-id="a7452-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7452-119">Type</span></span>   | <span data-ttu-id="a7452-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7452-120">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="a7452-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="a7452-121">Authorization</span></span> | <span data-ttu-id="a7452-122">string</span><span class="sxs-lookup"><span data-stu-id="a7452-122">string</span></span> | <span data-ttu-id="a7452-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a7452-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a7452-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a7452-125">Request body</span></span>

<span data-ttu-id="a7452-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a7452-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a7452-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7452-127">Response</span></span>

<span data-ttu-id="a7452-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7452-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a7452-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a7452-130">Example</span></span>

##### <a name="request"></a><span data-ttu-id="a7452-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a7452-131">Request</span></span>

<span data-ttu-id="a7452-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a7452-132">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_calendargroup"
}-->

```http
DELETE https://graph.microsoft.com/v1.0/me/calendarGroups/{id}
```

##### <a name="response"></a><span data-ttu-id="a7452-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7452-133">Response</span></span>

<span data-ttu-id="a7452-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a7452-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
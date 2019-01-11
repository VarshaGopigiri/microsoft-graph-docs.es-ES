---
title: Assign a manager
description: Use esta API para asignar un administrador de usuarios.
localization_priority: Normal
ms.openlocfilehash: 7391cef6b632df00a65f683855a5d088f69a43bb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811959"
---
# <a name="assign-a-manager"></a><span data-ttu-id="4cf66-103">Assign a manager</span><span class="sxs-lookup"><span data-stu-id="4cf66-103">Assign a manager</span></span>

> <span data-ttu-id="4cf66-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4cf66-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4cf66-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4cf66-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4cf66-106">Use esta API para asignar un administrador de usuarios.</span><span class="sxs-lookup"><span data-stu-id="4cf66-106">Use this API to assign a user's manager.</span></span>
> <span data-ttu-id="4cf66-107">Nota: No puede asignar subordinados directos; en lugar de ello, use esta API.</span><span class="sxs-lookup"><span data-stu-id="4cf66-107">Note: You cannot assign direct reports - instead use this API.</span></span>

## <a name="permissions"></a><span data-ttu-id="4cf66-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="4cf66-108">Permissions</span></span>
<span data-ttu-id="4cf66-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4cf66-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4cf66-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4cf66-111">Permission type</span></span>      | <span data-ttu-id="4cf66-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4cf66-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4cf66-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4cf66-113">Delegated (work or school account)</span></span> | <span data-ttu-id="4cf66-114">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="4cf66-114">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="4cf66-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4cf66-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4cf66-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4cf66-116">Not supported.</span></span>    |
|<span data-ttu-id="4cf66-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4cf66-117">Application</span></span> | <span data-ttu-id="4cf66-118">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4cf66-118">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4cf66-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4cf66-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PUT /users/{id}/manager/$ref
```
## <a name="request-headers"></a><span data-ttu-id="4cf66-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4cf66-120">Request headers</span></span>
| <span data-ttu-id="4cf66-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="4cf66-121">Name</span></span>       | <span data-ttu-id="4cf66-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="4cf66-122">Type</span></span> | <span data-ttu-id="4cf66-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="4cf66-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="4cf66-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="4cf66-124">Authorization</span></span>  | <span data-ttu-id="4cf66-125">string</span><span class="sxs-lookup"><span data-stu-id="4cf66-125">string</span></span>  | <span data-ttu-id="4cf66-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4cf66-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4cf66-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4cf66-128">Request body</span></span>
<span data-ttu-id="4cf66-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md) o [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="4cf66-129">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) or [user](../resources/user.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="4cf66-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4cf66-130">Response</span></span>

<span data-ttu-id="4cf66-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4cf66-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4cf66-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4cf66-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4cf66-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4cf66-134">Request</span></span>
<span data-ttu-id="4cf66-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4cf66-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
PUT https://graph.microsoft.com/v1.0/users/{id}/manager/$ref
Content-type: application/json
Content-length: xxx

{
  "@odata.id": "https://graph.microsoft.com/v1.0/users/{id}"
}
```
<span data-ttu-id="4cf66-136">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="4cf66-136">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>
##### <a name="response"></a><span data-ttu-id="4cf66-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4cf66-137">Response</span></span>
<span data-ttu-id="4cf66-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4cf66-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create member",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

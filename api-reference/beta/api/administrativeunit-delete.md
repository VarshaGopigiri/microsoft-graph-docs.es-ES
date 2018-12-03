---
title: Eliminar administrativeUnit
description: Eliminar un administrativeUnit.
ms.openlocfilehash: 6cb1885193e03da027d8d7680c0e5f33ec7f7d2b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084349"
---
# <a name="delete-administrativeunit"></a><span data-ttu-id="d1dfb-103">Eliminar administrativeUnit</span><span class="sxs-lookup"><span data-stu-id="d1dfb-103">Delete administrativeUnit</span></span>

> <span data-ttu-id="d1dfb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d1dfb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d1dfb-106">Eliminar un [administrativeUnit](../resources/administrativeunit.md).</span><span class="sxs-lookup"><span data-stu-id="d1dfb-106">Delete an [administrativeUnit](../resources/administrativeunit.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="d1dfb-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d1dfb-107">Permissions</span></span>
<span data-ttu-id="d1dfb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d1dfb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="d1dfb-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d1dfb-110">Permission type</span></span>      | <span data-ttu-id="d1dfb-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d1dfb-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d1dfb-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d1dfb-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d1dfb-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="d1dfb-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="d1dfb-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d1dfb-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d1dfb-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-115">Not supported.</span></span>    |
|<span data-ttu-id="d1dfb-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d1dfb-116">Application</span></span> | <span data-ttu-id="d1dfb-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d1dfb-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d1dfb-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /administrativeUnits/{id}

```
## <a name="request-headers"></a><span data-ttu-id="d1dfb-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d1dfb-119">Request headers</span></span>
| <span data-ttu-id="d1dfb-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="d1dfb-120">Name</span></span>       | <span data-ttu-id="d1dfb-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1dfb-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d1dfb-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="d1dfb-122">Authorization</span></span>  | <span data-ttu-id="d1dfb-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d1dfb-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d1dfb-125">Request body</span></span>
<span data-ttu-id="d1dfb-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d1dfb-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d1dfb-127">Response</span></span>

<span data-ttu-id="d1dfb-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d1dfb-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d1dfb-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d1dfb-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d1dfb-131">Request</span></span>
<span data-ttu-id="d1dfb-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_administrativeunit"
}-->
```http
DELETE https://graph.microsoft.com/beta/administrativeUnits/{id}
```
##### <a name="response"></a><span data-ttu-id="d1dfb-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d1dfb-133">Response</span></span>
<span data-ttu-id="d1dfb-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Delete administrativeUnit",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
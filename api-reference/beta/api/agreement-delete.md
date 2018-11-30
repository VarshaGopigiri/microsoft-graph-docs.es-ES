---
title: Eliminar contrato
description: Eliminación de un objeto de contrato.
ms.openlocfilehash: 919fc628e5f8ff9b6c016e085671f47ed6d56a5c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085956"
---
# <a name="delete-agreement"></a><span data-ttu-id="78d37-103">Eliminar contrato</span><span class="sxs-lookup"><span data-stu-id="78d37-103">Delete agreement</span></span>

> <span data-ttu-id="78d37-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="78d37-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="78d37-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="78d37-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="78d37-106">Eliminación de un objeto de [contrato](../resources/agreement.md) .</span><span class="sxs-lookup"><span data-stu-id="78d37-106">Delete an [agreement](../resources/agreement.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="78d37-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="78d37-107">Permissions</span></span>
<span data-ttu-id="78d37-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="78d37-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="78d37-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="78d37-110">Permission type</span></span>                        | <span data-ttu-id="78d37-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="78d37-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="78d37-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="78d37-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="78d37-113">Agreement.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="78d37-113">Agreement.ReadWrite.All</span></span> |
|<span data-ttu-id="78d37-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="78d37-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="78d37-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="78d37-115">Not supported.</span></span> |
|<span data-ttu-id="78d37-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="78d37-116">Application</span></span>                            | <span data-ttu-id="78d37-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="78d37-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="78d37-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="78d37-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /agreements/<id>
```
## <a name="request-headers"></a><span data-ttu-id="78d37-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="78d37-119">Request headers</span></span>
| <span data-ttu-id="78d37-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="78d37-120">Name</span></span>         | <span data-ttu-id="78d37-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="78d37-121">Type</span></span>        | <span data-ttu-id="78d37-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="78d37-122">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="78d37-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="78d37-123">Authorization</span></span> | <span data-ttu-id="78d37-124">string</span><span class="sxs-lookup"><span data-stu-id="78d37-124">string</span></span> | <span data-ttu-id="78d37-125">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="78d37-125">Bearer \{token\}.</span></span> <span data-ttu-id="78d37-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="78d37-126">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="78d37-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="78d37-127">Request body</span></span>
<span data-ttu-id="78d37-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="78d37-128">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="78d37-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="78d37-129">Response</span></span>
<span data-ttu-id="78d37-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="78d37-p104">If successful, this method returns a `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="78d37-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="78d37-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="78d37-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="78d37-133">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_agreement"
}-->
```http
DELETE https://graph.microsoft.com/beta/agreements/<id>
```
##### <a name="response"></a><span data-ttu-id="78d37-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="78d37-134">Response</span></span>
><span data-ttu-id="78d37-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="78d37-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
  "description": "Delete agreement",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

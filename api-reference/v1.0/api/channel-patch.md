---
title: Canal de revisión
description: Actualizar las propiedades del canal especificado.
ms.openlocfilehash: 981de62dcedb42b98016aa99ccaaa8b5cd27ba9c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032703"
---
# <a name="patch-channel"></a><span data-ttu-id="eb756-103">Canal de revisión</span><span class="sxs-lookup"><span data-stu-id="eb756-103">Patch channel</span></span>



<span data-ttu-id="eb756-104">Actualizar las propiedades del [canal](../resources/channel.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="eb756-104">Update the properties of the specified [channel](../resources/channel.md).</span></span>

> <span data-ttu-id="eb756-105">**Nota**: hay un problema conocido con permisos de la aplicación y esta API.</span><span class="sxs-lookup"><span data-stu-id="eb756-105">**Note**: There is a known issue with application permissions and this API.</span></span> <span data-ttu-id="eb756-106">Para obtener información detallada, vea el [conocido lista de problemas](/graph/known-issues#application-permissions).</span><span class="sxs-lookup"><span data-stu-id="eb756-106">For details, see the [known issues list](/graph/known-issues#application-permissions).</span></span>

## <a name="permissions"></a><span data-ttu-id="eb756-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="eb756-107">Permissions</span></span>
<span data-ttu-id="eb756-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eb756-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eb756-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eb756-110">Permission type</span></span>      | <span data-ttu-id="eb756-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eb756-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eb756-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eb756-112">Delegated (work or school account)</span></span> | <span data-ttu-id="eb756-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eb756-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="eb756-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eb756-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eb756-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eb756-115">Not supported.</span></span>    |
|<span data-ttu-id="eb756-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eb756-116">Application</span></span> | <span data-ttu-id="eb756-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eb756-117">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="eb756-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eb756-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /teams/{id}/channels/{id}
```
## <a name="request-headers"></a><span data-ttu-id="eb756-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eb756-119">Request headers</span></span>
| <span data-ttu-id="eb756-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb756-120">Header</span></span>       | <span data-ttu-id="eb756-121">Valor</span><span class="sxs-lookup"><span data-stu-id="eb756-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="eb756-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="eb756-122">Authorization</span></span>  | <span data-ttu-id="eb756-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eb756-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="eb756-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="eb756-125">Content-Type</span></span>  | <span data-ttu-id="eb756-126">application/json</span><span class="sxs-lookup"><span data-stu-id="eb756-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="eb756-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eb756-127">Request body</span></span>
<span data-ttu-id="eb756-128">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [canal](../resources/channel.md) .</span><span class="sxs-lookup"><span data-stu-id="eb756-128">In the request body, supply a JSON representation of [channel](../resources/channel.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="eb756-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb756-129">Response</span></span>

<span data-ttu-id="eb756-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="eb756-130">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="eb756-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eb756-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="eb756-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eb756-132">Request</span></span>
<span data-ttu-id="eb756-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eb756-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "patch_channel"
}-->
```http
PATCH https://graph.microsoft.com/beta/teams/{id}/channels/{id}
```
##### <a name="response"></a><span data-ttu-id="eb756-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb756-134">Response</span></span>
<span data-ttu-id="eb756-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eb756-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.channel"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 201

{
    "description": "description-value",
    "displayName": "display-name-value",
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Patch channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

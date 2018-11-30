---
title: Canal de revisión
description: Actualizar las propiedades del canal especificado.
ms.openlocfilehash: 833b5cf4999f43e9de799691a9f6d7a98318d4fe
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083319"
---
# <a name="patch-channel"></a><span data-ttu-id="adca1-103">Canal de revisión</span><span class="sxs-lookup"><span data-stu-id="adca1-103">Patch channel</span></span>

> <span data-ttu-id="adca1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="adca1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="adca1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="adca1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="adca1-106">Actualizar las propiedades del [canal](../resources/channel.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="adca1-106">Update the properties of the specified [channel](../resources/channel.md).</span></span>

> <span data-ttu-id="adca1-107">**Nota**: hay un problema conocido con permisos de la aplicación y esta API.</span><span class="sxs-lookup"><span data-stu-id="adca1-107">**Note**: There is a known issue with application permissions and this API.</span></span> <span data-ttu-id="adca1-108">Para obtener información detallada, vea el [conocido lista de problemas](/graph/known-issues#application-permissions).</span><span class="sxs-lookup"><span data-stu-id="adca1-108">For details, see the [known issues list](/graph/known-issues#application-permissions).</span></span>

## <a name="permissions"></a><span data-ttu-id="adca1-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="adca1-109">Permissions</span></span>
<span data-ttu-id="adca1-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="adca1-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="adca1-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="adca1-112">Permission type</span></span>      | <span data-ttu-id="adca1-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="adca1-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="adca1-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="adca1-114">Delegated (work or school account)</span></span> | <span data-ttu-id="adca1-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="adca1-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="adca1-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="adca1-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="adca1-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="adca1-117">Not supported.</span></span>    |
|<span data-ttu-id="adca1-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="adca1-118">Application</span></span> | <span data-ttu-id="adca1-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="adca1-119">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="adca1-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="adca1-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /teams/{id}/channels/{id}
```
## <a name="request-headers"></a><span data-ttu-id="adca1-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="adca1-121">Request headers</span></span>
| <span data-ttu-id="adca1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="adca1-122">Header</span></span>       | <span data-ttu-id="adca1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="adca1-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="adca1-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="adca1-124">Authorization</span></span>  | <span data-ttu-id="adca1-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="adca1-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="adca1-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="adca1-127">Content-Type</span></span>  | <span data-ttu-id="adca1-128">application/json</span><span class="sxs-lookup"><span data-stu-id="adca1-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="adca1-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="adca1-129">Request body</span></span>
<span data-ttu-id="adca1-130">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [canal](../resources/channel.md) .</span><span class="sxs-lookup"><span data-stu-id="adca1-130">In the request body, supply a JSON representation of [channel](../resources/channel.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="adca1-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="adca1-131">Response</span></span>

<span data-ttu-id="adca1-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="adca1-132">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="adca1-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="adca1-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="adca1-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="adca1-134">Request</span></span>
<span data-ttu-id="adca1-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="adca1-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "patch_channel"
}-->
```http
PATCH https://graph.microsoft.com/beta/teams/{id}/channels/{id}
```
##### <a name="response"></a><span data-ttu-id="adca1-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="adca1-136">Response</span></span>
<span data-ttu-id="adca1-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="adca1-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

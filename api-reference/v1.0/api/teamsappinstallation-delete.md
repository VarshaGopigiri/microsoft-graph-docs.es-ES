---
title: Eliminar aplicación de equipo
description: Desinstala una aplicación desde el equipo especificado.
ms.openlocfilehash: a1ba2ce7234796e3a2df508d40432a15690b1a63
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029571"
---
# <a name="delete-app-from-team"></a><span data-ttu-id="dfccf-103">Eliminar aplicación de equipo</span><span class="sxs-lookup"><span data-stu-id="dfccf-103">Delete app from team</span></span>



<span data-ttu-id="dfccf-104">Desinstala una [aplicación](../resources/teamsappinstallation.md) desde el [equipo](../resources/team.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="dfccf-104">Uninstalls an [app](../resources/teamsappinstallation.md) from the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="dfccf-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="dfccf-105">Permissions</span></span>
<span data-ttu-id="dfccf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dfccf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dfccf-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dfccf-108">Permission type</span></span>      | <span data-ttu-id="dfccf-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dfccf-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dfccf-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dfccf-110">Delegated (work or school account)</span></span> | <span data-ttu-id="dfccf-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dfccf-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="dfccf-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dfccf-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dfccf-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dfccf-113">Not supported.</span></span>    |
|<span data-ttu-id="dfccf-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dfccf-114">Application</span></span> | <span data-ttu-id="dfccf-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dfccf-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="dfccf-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dfccf-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /teams/{id}/installedApps/{id}
```

## <a name="request-headers"></a><span data-ttu-id="dfccf-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dfccf-117">Request headers</span></span>
| <span data-ttu-id="dfccf-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dfccf-118">Header</span></span>       | <span data-ttu-id="dfccf-119">Valor</span><span class="sxs-lookup"><span data-stu-id="dfccf-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="dfccf-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="dfccf-120">Authorization</span></span>  | <span data-ttu-id="dfccf-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dfccf-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="dfccf-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dfccf-123">Request body</span></span>
<span data-ttu-id="dfccf-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="dfccf-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="dfccf-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dfccf-125">Response</span></span>

<span data-ttu-id="dfccf-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dfccf-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dfccf-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dfccf-128">Example</span></span>
#### <a name="request"></a><span data-ttu-id="dfccf-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dfccf-129">Request</span></span>
<span data-ttu-id="dfccf-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dfccf-130">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->
```http
DELETE https://graph.microsoft.com/beta/teams/{id}/installedApps/{id}
```
#### <a name="response"></a><span data-ttu-id="dfccf-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dfccf-131">Response</span></span>
<span data-ttu-id="dfccf-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dfccf-132">The following is an example of the response.</span></span> <span data-ttu-id="dfccf-133">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="dfccf-133">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="dfccf-134">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dfccf-134">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
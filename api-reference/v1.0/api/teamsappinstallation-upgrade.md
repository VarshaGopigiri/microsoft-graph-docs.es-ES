---
title: Actualización de una aplicación en un equipo
description: Actualiza una instalación de la aplicación en un equipo
ms.openlocfilehash: 37f42a307b2f86e7a447e3df05030e94495eaa6b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029241"
---
# <a name="upgrade-an-app-in-a-team"></a><span data-ttu-id="e71f6-103">Actualización de una aplicación en un equipo</span><span class="sxs-lookup"><span data-stu-id="e71f6-103">Upgrade an app in a team</span></span>



<span data-ttu-id="e71f6-104">Actualiza una [instalación de la aplicación](../resources/teamsappinstallation.md) en un [equipo](../resources/team.md) a la versión más reciente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e71f6-104">Upgrades an [app installation](../resources/teamsappinstallation.md) in a [team](../resources/team.md) to the latest version of the app.</span></span>

## <a name="permissions"></a><span data-ttu-id="e71f6-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="e71f6-105">Permissions</span></span>

<span data-ttu-id="e71f6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e71f6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e71f6-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e71f6-108">Permission type</span></span>      | <span data-ttu-id="e71f6-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e71f6-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e71f6-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e71f6-110">Delegated (work or school account)</span></span> | <span data-ttu-id="e71f6-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e71f6-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="e71f6-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e71f6-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e71f6-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e71f6-113">Not supported.</span></span>    |
|<span data-ttu-id="e71f6-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e71f6-114">Application</span></span> | <span data-ttu-id="e71f6-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e71f6-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e71f6-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e71f6-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/installedApps/{id}/upgrade
```

## <a name="request-headers"></a><span data-ttu-id="e71f6-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e71f6-117">Request headers</span></span>
| <span data-ttu-id="e71f6-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e71f6-118">Header</span></span>       | <span data-ttu-id="e71f6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e71f6-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e71f6-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="e71f6-120">Authorization</span></span>  | <span data-ttu-id="e71f6-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e71f6-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e71f6-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e71f6-123">Request body</span></span>
<span data-ttu-id="e71f6-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e71f6-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e71f6-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e71f6-125">Response</span></span>

<span data-ttu-id="e71f6-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e71f6-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e71f6-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e71f6-128">Example</span></span>

#### <a name="request"></a><span data-ttu-id="e71f6-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e71f6-129">Request</span></span>
<span data-ttu-id="e71f6-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e71f6-130">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->

```http
POST /teams/{id}/installedApps/{id}/upgrade
```
#### <a name="response"></a><span data-ttu-id="e71f6-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e71f6-131">Response</span></span>
<span data-ttu-id="e71f6-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e71f6-132">The following is an example of the response.</span></span> 

><span data-ttu-id="e71f6-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e71f6-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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

---
title: Actualización de una aplicación en un equipo
description: Actualiza una instalación de la aplicación en un equipo
ms.openlocfilehash: 90cec9dcb41b27a239661f3ed1850e073775be71
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087840"
---
# <a name="upgrade-an-app-in-a-team"></a><span data-ttu-id="df2b1-103">Actualización de una aplicación en un equipo</span><span class="sxs-lookup"><span data-stu-id="df2b1-103">Upgrade an app in a team</span></span>

> <span data-ttu-id="df2b1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="df2b1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="df2b1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="df2b1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="df2b1-106">Actualiza una [instalación de la aplicación](../resources/teamsappinstallation.md) en un [equipo](../resources/team.md) a la versión más reciente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="df2b1-106">Upgrades an [app installation](../resources/teamsappinstallation.md) in a [team](../resources/team.md) to the latest version of the app.</span></span>

## <a name="permissions"></a><span data-ttu-id="df2b1-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="df2b1-107">Permissions</span></span>

<span data-ttu-id="df2b1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="df2b1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="df2b1-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="df2b1-110">Permission type</span></span>      | <span data-ttu-id="df2b1-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="df2b1-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="df2b1-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="df2b1-112">Delegated (work or school account)</span></span> | <span data-ttu-id="df2b1-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="df2b1-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="df2b1-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="df2b1-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="df2b1-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="df2b1-115">Not supported.</span></span>    |
|<span data-ttu-id="df2b1-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="df2b1-116">Application</span></span> | <span data-ttu-id="df2b1-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="df2b1-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="df2b1-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="df2b1-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/installedApps/{id}/upgrade
```

## <a name="request-headers"></a><span data-ttu-id="df2b1-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="df2b1-119">Request headers</span></span>
| <span data-ttu-id="df2b1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df2b1-120">Header</span></span>       | <span data-ttu-id="df2b1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="df2b1-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="df2b1-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="df2b1-122">Authorization</span></span>  | <span data-ttu-id="df2b1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="df2b1-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="df2b1-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="df2b1-125">Request body</span></span>
<span data-ttu-id="df2b1-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="df2b1-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="df2b1-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="df2b1-127">Response</span></span>

<span data-ttu-id="df2b1-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="df2b1-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="df2b1-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="df2b1-130">Example</span></span>

#### <a name="request"></a><span data-ttu-id="df2b1-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="df2b1-131">Request</span></span>
<span data-ttu-id="df2b1-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="df2b1-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->

```http
POST /teams/{id}/installedApps/{id}/upgrade
```
#### <a name="response"></a><span data-ttu-id="df2b1-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="df2b1-133">Response</span></span>
<span data-ttu-id="df2b1-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="df2b1-134">The following is an example of the response.</span></span> 

><span data-ttu-id="df2b1-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="df2b1-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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

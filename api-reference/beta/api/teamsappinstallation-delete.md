---
title: Eliminar aplicación de equipo
description: Desinstala una aplicación desde el equipo especificado.
author: nkramer
localization_priority: Normal
ms.openlocfilehash: b0d1c7d8344218d6eba4165e94b09158d60846ec
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27852496"
---
# <a name="delete-app-from-team"></a><span data-ttu-id="63bf9-103">Eliminar aplicación de equipo</span><span class="sxs-lookup"><span data-stu-id="63bf9-103">Delete app from team</span></span>

> <span data-ttu-id="63bf9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="63bf9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="63bf9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="63bf9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="63bf9-106">Desinstala una [aplicación](../resources/teamsappinstallation.md) desde el [equipo](../resources/team.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="63bf9-106">Uninstalls an [app](../resources/teamsappinstallation.md) from the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="63bf9-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="63bf9-107">Permissions</span></span>
<span data-ttu-id="63bf9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="63bf9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="63bf9-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="63bf9-110">Permission type</span></span>      | <span data-ttu-id="63bf9-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="63bf9-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="63bf9-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="63bf9-112">Delegated (work or school account)</span></span> | <span data-ttu-id="63bf9-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="63bf9-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="63bf9-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="63bf9-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="63bf9-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63bf9-115">Not supported.</span></span>    |
|<span data-ttu-id="63bf9-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="63bf9-116">Application</span></span> | <span data-ttu-id="63bf9-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63bf9-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="63bf9-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="63bf9-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /teams/{id}/installedApps/{id}
```

## <a name="request-headers"></a><span data-ttu-id="63bf9-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="63bf9-119">Request headers</span></span>
| <span data-ttu-id="63bf9-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63bf9-120">Header</span></span>       | <span data-ttu-id="63bf9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="63bf9-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="63bf9-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="63bf9-122">Authorization</span></span>  | <span data-ttu-id="63bf9-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="63bf9-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="63bf9-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="63bf9-125">Request body</span></span>
<span data-ttu-id="63bf9-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="63bf9-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="63bf9-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63bf9-127">Response</span></span>

<span data-ttu-id="63bf9-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63bf9-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="63bf9-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63bf9-130">Example</span></span>
#### <a name="request"></a><span data-ttu-id="63bf9-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="63bf9-131">Request</span></span>
<span data-ttu-id="63bf9-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63bf9-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->
```http
DELETE https://graph.microsoft.com/beta/teams/{id}/installedApps/{id}
```
#### <a name="response"></a><span data-ttu-id="63bf9-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63bf9-133">Response</span></span>
<span data-ttu-id="63bf9-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63bf9-134">The following is an example of the response.</span></span> <span data-ttu-id="63bf9-135">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="63bf9-135">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="63bf9-136">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="63bf9-136">All of the properties will be returned from an actual call.</span></span>
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

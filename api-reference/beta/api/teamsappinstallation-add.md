---
title: Agregar la aplicación al equipo
description: Instala una aplicación en el equipo especificado.
author: nkramer
ms.openlocfilehash: ed38f809c784c4178f7be2b028dc4c71a6206b1b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27349171"
---
# <a name="add-app-to-team"></a><span data-ttu-id="5d90c-103">Agregar la aplicación al equipo</span><span class="sxs-lookup"><span data-stu-id="5d90c-103">Add app to team</span></span>

> <span data-ttu-id="5d90c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5d90c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5d90c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5d90c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5d90c-106">Instala una [aplicación](../resources/teamsapp.md) en el [equipo](../resources/team.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="5d90c-106">Installs an [app](../resources/teamsapp.md) to the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="5d90c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5d90c-107">Permissions</span></span>
<span data-ttu-id="5d90c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5d90c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5d90c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5d90c-110">Permission type</span></span>      | <span data-ttu-id="5d90c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5d90c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5d90c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5d90c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5d90c-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5d90c-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="5d90c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5d90c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5d90c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5d90c-115">Not supported.</span></span>    |
|<span data-ttu-id="5d90c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5d90c-116">Application</span></span> | <span data-ttu-id="5d90c-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5d90c-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5d90c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5d90c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/installedApps
```

## <a name="request-headers"></a><span data-ttu-id="5d90c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5d90c-119">Request headers</span></span>
| <span data-ttu-id="5d90c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d90c-120">Header</span></span>       | <span data-ttu-id="5d90c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5d90c-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="5d90c-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="5d90c-122">Authorization</span></span>  | <span data-ttu-id="5d90c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5d90c-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="5d90c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5d90c-125">Request body</span></span>

| <span data-ttu-id="5d90c-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5d90c-126">Property</span></span>     | <span data-ttu-id="5d90c-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="5d90c-127">Type</span></span>   |<span data-ttu-id="5d90c-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d90c-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5d90c-129">teamsApp</span><span class="sxs-lookup"><span data-stu-id="5d90c-129">teamsApp</span></span>|<span data-ttu-id="5d90c-130">String</span><span class="sxs-lookup"><span data-stu-id="5d90c-130">String</span></span>|<span data-ttu-id="5d90c-131">El identificador de la aplicación para agregar.</span><span class="sxs-lookup"><span data-stu-id="5d90c-131">The id of the app to add.</span></span>|


## <a name="response"></a><span data-ttu-id="5d90c-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d90c-132">Response</span></span>

<span data-ttu-id="5d90c-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="5d90c-133">If successful, this method returns a `200 OK` response code.</span></span>
## <a name="example"></a><span data-ttu-id="5d90c-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5d90c-134">Example</span></span>
#### <a name="request"></a><span data-ttu-id="5d90c-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5d90c-135">Request</span></span>
<span data-ttu-id="5d90c-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5d90c-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->
```http
POST https://graph.microsoft.com/beta/teams/{id}/installedApps
{
   "teamsApp@odata.bind":"https://graph.microsoft.com/beta/appCatalogs/teamsApps/12345678-9abc-def0-123456789a"
}
```
#### <a name="response"></a><span data-ttu-id="5d90c-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d90c-137">Response</span></span>
<span data-ttu-id="5d90c-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5d90c-138">The following is an example of the response.</span></span> <span data-ttu-id="5d90c-139">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="5d90c-139">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="5d90c-140">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5d90c-140">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 401

{
}
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

## <a name="see-also"></a><span data-ttu-id="5d90c-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="5d90c-141">See also</span></span>


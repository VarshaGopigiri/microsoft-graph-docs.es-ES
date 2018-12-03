---
title: Agregar la aplicación al equipo
description: Instala una aplicación en el equipo especificado.
ms.openlocfilehash: de5817f243b02462817d23d0e2b3864d5644b1d4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030101"
---
# <a name="add-app-to-team"></a><span data-ttu-id="d21da-103">Agregar la aplicación al equipo</span><span class="sxs-lookup"><span data-stu-id="d21da-103">Add app to team</span></span>



<span data-ttu-id="d21da-104">Instala una [aplicación](../resources/teamsapp.md) en el [equipo](../resources/team.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="d21da-104">Installs an [app](../resources/teamsapp.md) to the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="d21da-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="d21da-105">Permissions</span></span>
<span data-ttu-id="d21da-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d21da-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d21da-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d21da-108">Permission type</span></span>      | <span data-ttu-id="d21da-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d21da-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d21da-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d21da-110">Delegated (work or school account)</span></span> | <span data-ttu-id="d21da-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d21da-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="d21da-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d21da-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d21da-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d21da-113">Not supported.</span></span>    |
|<span data-ttu-id="d21da-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d21da-114">Application</span></span> | <span data-ttu-id="d21da-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d21da-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d21da-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d21da-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/installedApps
```

## <a name="request-headers"></a><span data-ttu-id="d21da-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d21da-117">Request headers</span></span>
| <span data-ttu-id="d21da-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d21da-118">Header</span></span>       | <span data-ttu-id="d21da-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d21da-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d21da-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="d21da-120">Authorization</span></span>  | <span data-ttu-id="d21da-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d21da-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d21da-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d21da-123">Request body</span></span>

| <span data-ttu-id="d21da-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d21da-124">Property</span></span>     | <span data-ttu-id="d21da-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="d21da-125">Type</span></span>   |<span data-ttu-id="d21da-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="d21da-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d21da-127">teamsApp</span><span class="sxs-lookup"><span data-stu-id="d21da-127">teamsApp</span></span>| [<span data-ttu-id="d21da-128">teamsApp</span><span class="sxs-lookup"><span data-stu-id="d21da-128">teamsApp</span></span>](../resources/teamsapp.md) |<span data-ttu-id="d21da-129">Para agregar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d21da-129">The app to add.</span></span>|


## <a name="response"></a><span data-ttu-id="d21da-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d21da-130">Response</span></span>

<span data-ttu-id="d21da-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="d21da-131">If successful, this method returns a `200 OK` response code.</span></span>

## <a name="example"></a><span data-ttu-id="d21da-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d21da-132">Example</span></span>
#### <a name="request"></a><span data-ttu-id="d21da-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d21da-133">Request</span></span>
<span data-ttu-id="d21da-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d21da-134">The following is an example of the request.</span></span>
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
#### <a name="response"></a><span data-ttu-id="d21da-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d21da-135">Response</span></span>
<span data-ttu-id="d21da-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d21da-136">The following is an example of the response.</span></span> <span data-ttu-id="d21da-137">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="d21da-137">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="d21da-138">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d21da-138">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: xxx

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

## <a name="see-also"></a><span data-ttu-id="d21da-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="d21da-139">See also</span></span>

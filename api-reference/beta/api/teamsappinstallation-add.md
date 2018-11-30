---
title: Agregar la aplicación al equipo
description: Instala una aplicación en el equipo especificado.
ms.openlocfilehash: f3cf62163747bd1a288b59a39e5ff1fc9d82783b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088306"
---
# <a name="add-app-to-team"></a><span data-ttu-id="644f6-103">Agregar la aplicación al equipo</span><span class="sxs-lookup"><span data-stu-id="644f6-103">Add app to team</span></span>

> <span data-ttu-id="644f6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="644f6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="644f6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="644f6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="644f6-106">Instala una [aplicación](../resources/teamsapp.md) en el [equipo](../resources/team.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="644f6-106">Installs an [app](../resources/teamsapp.md) to the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="644f6-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="644f6-107">Permissions</span></span>
<span data-ttu-id="644f6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="644f6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="644f6-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="644f6-110">Permission type</span></span>      | <span data-ttu-id="644f6-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="644f6-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="644f6-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="644f6-112">Delegated (work or school account)</span></span> | <span data-ttu-id="644f6-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="644f6-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="644f6-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="644f6-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="644f6-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="644f6-115">Not supported.</span></span>    |
|<span data-ttu-id="644f6-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="644f6-116">Application</span></span> | <span data-ttu-id="644f6-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="644f6-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="644f6-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="644f6-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/installedApps
```

## <a name="request-headers"></a><span data-ttu-id="644f6-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="644f6-119">Request headers</span></span>
| <span data-ttu-id="644f6-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="644f6-120">Header</span></span>       | <span data-ttu-id="644f6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="644f6-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="644f6-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="644f6-122">Authorization</span></span>  | <span data-ttu-id="644f6-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="644f6-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="644f6-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="644f6-125">Request body</span></span>

| <span data-ttu-id="644f6-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="644f6-126">Property</span></span>     | <span data-ttu-id="644f6-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="644f6-127">Type</span></span>   |<span data-ttu-id="644f6-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="644f6-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="644f6-129">teamsApp</span><span class="sxs-lookup"><span data-stu-id="644f6-129">teamsApp</span></span>|<span data-ttu-id="644f6-130">String</span><span class="sxs-lookup"><span data-stu-id="644f6-130">String</span></span>|<span data-ttu-id="644f6-131">El identificador de la aplicación para agregar.</span><span class="sxs-lookup"><span data-stu-id="644f6-131">The id of the app to add.</span></span>|


## <a name="response"></a><span data-ttu-id="644f6-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="644f6-132">Response</span></span>

<span data-ttu-id="644f6-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="644f6-133">If successful, this method returns a `200 OK` response code.</span></span>
## <a name="example"></a><span data-ttu-id="644f6-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="644f6-134">Example</span></span>
#### <a name="request"></a><span data-ttu-id="644f6-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="644f6-135">Request</span></span>
<span data-ttu-id="644f6-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="644f6-136">The following is an example of the request.</span></span>
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
#### <a name="response"></a><span data-ttu-id="644f6-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="644f6-137">Response</span></span>
<span data-ttu-id="644f6-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="644f6-138">The following is an example of the response.</span></span> <span data-ttu-id="644f6-139">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="644f6-139">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="644f6-140">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="644f6-140">All of the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="644f6-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="644f6-141">See also</span></span>


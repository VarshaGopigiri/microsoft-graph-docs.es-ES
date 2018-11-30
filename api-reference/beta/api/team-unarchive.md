---
title: Unarchive equipo
description: Restaurar un equipo archivado. Esto restaura la capacidad de los usuarios enviar mensajes y editar el equipo, respetando por la configuración de inquilino y del equipo. Los equipos se archivan con la API de archivo.
ms.openlocfilehash: 6016529f20781a66aa8c36771a56942cb471ee7f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088311"
---
# <a name="unarchive-team"></a><span data-ttu-id="ec24c-105">Unarchive equipo</span><span class="sxs-lookup"><span data-stu-id="ec24c-105">Unarchive team</span></span>

> <span data-ttu-id="ec24c-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ec24c-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ec24c-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ec24c-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ec24c-108">Restauración de un [equipo](../resources/team.md)de archivado.</span><span class="sxs-lookup"><span data-stu-id="ec24c-108">Restore an archived [team](../resources/team.md).</span></span> <span data-ttu-id="ec24c-109">Esto restaura la capacidad de los usuarios enviar mensajes y editar el equipo, respetando por la configuración de inquilino y del equipo.</span><span class="sxs-lookup"><span data-stu-id="ec24c-109">This restores users' ability to send messages and edit the team, abiding by tenant and team settings.</span></span> <span data-ttu-id="ec24c-110">Los equipos se archivan con el [archivo](team-archive.md) API.</span><span class="sxs-lookup"><span data-stu-id="ec24c-110">Teams are archived using the [archive](team-archive.md) API.</span></span>

<span data-ttu-id="ec24c-111">Unarchiving es una operación asíncrona.</span><span class="sxs-lookup"><span data-stu-id="ec24c-111">Unarchiving is an async operation.</span></span> <span data-ttu-id="ec24c-112">Un equipo es sin archivar una vez que la operación asincrónica se completa correctamente, lo que puede producirse con posterioridad a una respuesta desde esta API.</span><span class="sxs-lookup"><span data-stu-id="ec24c-112">A team is unarchived once the async operation completes successfully, which may occur subsequent to a response from this API.</span></span>

## <a name="permissions"></a><span data-ttu-id="ec24c-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="ec24c-113">Permissions</span></span>
<span data-ttu-id="ec24c-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ec24c-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ec24c-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ec24c-116">Permission type</span></span>      | <span data-ttu-id="ec24c-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ec24c-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ec24c-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ec24c-118">Delegated (work or school account)</span></span> | <span data-ttu-id="ec24c-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ec24c-119">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ec24c-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ec24c-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ec24c-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ec24c-121">Not supported.</span></span>    |
|<span data-ttu-id="ec24c-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ec24c-122">Application</span></span> | <span data-ttu-id="ec24c-123">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ec24c-123">Group.ReadWrite.All</span></span>    |

## <a name="http-request"></a><span data-ttu-id="ec24c-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ec24c-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/unarchive
```

## <a name="request-headers"></a><span data-ttu-id="ec24c-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ec24c-125">Request headers</span></span>
| <span data-ttu-id="ec24c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec24c-126">Header</span></span>       | <span data-ttu-id="ec24c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="ec24c-127">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ec24c-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="ec24c-128">Authorization</span></span>  | <span data-ttu-id="ec24c-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ec24c-p106">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ec24c-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ec24c-131">Request body</span></span>
<span data-ttu-id="ec24c-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ec24c-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ec24c-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec24c-133">Response</span></span>

<span data-ttu-id="ec24c-134">Si unarchiving se ha iniciado correctamente, este método devuelve una `202 Accepted` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="ec24c-134">If unarchiving is started successfully, this method returns a `202 Accepted` response code.</span></span> <span data-ttu-id="ec24c-135">La respuesta contendrá también un `Location` encabezado, que contiene la ubicación de la [teamsAsyncOperation](../resources/teamsasyncoperation.md) que se creó para controlar unarchiving del equipo.</span><span class="sxs-lookup"><span data-stu-id="ec24c-135">The response will also contain a `Location` header, which contains the location of the [teamsAsyncOperation](../resources/teamsasyncoperation.md) that was created to handle unarchiving of the team.</span></span> <span data-ttu-id="ec24c-136">Comprobar el estado de la operación unarchiving mediante la realización de una solicitud GET en esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="ec24c-136">Check the status of the unarchiving operation by making a GET request to this location.</span></span>

## <a name="example"></a><span data-ttu-id="ec24c-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ec24c-137">Example</span></span>
#### <a name="request"></a><span data-ttu-id="ec24c-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ec24c-138">Request</span></span>
<span data-ttu-id="ec24c-139">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ec24c-139">The following is an example of a request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "unarchive_team"
}-->
```http
POST https://graph.microsoft.com/beta/teams/{id}/unarchive
```

#### <a name="response"></a><span data-ttu-id="ec24c-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec24c-140">Response</span></span>
<span data-ttu-id="ec24c-141">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="ec24c-141">The following is an example of a response.</span></span>
```http
HTTP/1.1 202 Accepted
Location: /teams{id}/operations({opId})
Content-Type: text/plain
Content-Length: 0
```

<!-- uuid: 9a9bb83f-6f35-4426-bb04-73ca43ad6cc8
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Unarchive team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

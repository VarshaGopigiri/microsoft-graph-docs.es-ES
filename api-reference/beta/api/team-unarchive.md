---
title: Unarchive equipo
description: Restaurar un equipo archivado. Esto restaura la capacidad de los usuarios enviar mensajes y editar el equipo, respetando por la configuración de inquilino y del equipo. Los equipos se archivan con la API de archivo.
localization_priority: Normal
author: nkramer
ms.prod: microsoft-teams
ms.openlocfilehash: b5c64c9c04c7c3cc3549721747c27361680bd03a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977671"
---
# <a name="unarchive-team"></a><span data-ttu-id="14736-105">Unarchive equipo</span><span class="sxs-lookup"><span data-stu-id="14736-105">Unarchive team</span></span>

> <span data-ttu-id="14736-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="14736-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="14736-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="14736-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="14736-108">Restauración de un [equipo](../resources/team.md)de archivado.</span><span class="sxs-lookup"><span data-stu-id="14736-108">Restore an archived [team](../resources/team.md).</span></span> <span data-ttu-id="14736-109">Esto restaura la capacidad de los usuarios enviar mensajes y editar el equipo, respetando por la configuración de inquilino y del equipo.</span><span class="sxs-lookup"><span data-stu-id="14736-109">This restores users' ability to send messages and edit the team, abiding by tenant and team settings.</span></span> <span data-ttu-id="14736-110">Los equipos se archivan con el [archivo](team-archive.md) API.</span><span class="sxs-lookup"><span data-stu-id="14736-110">Teams are archived using the [archive](team-archive.md) API.</span></span>

<span data-ttu-id="14736-111">Unarchiving es una operación asíncrona.</span><span class="sxs-lookup"><span data-stu-id="14736-111">Unarchiving is an async operation.</span></span> <span data-ttu-id="14736-112">Un equipo es sin archivar una vez que la operación asincrónica se completa correctamente, lo que puede producirse con posterioridad a una respuesta desde esta API.</span><span class="sxs-lookup"><span data-stu-id="14736-112">A team is unarchived once the async operation completes successfully, which may occur subsequent to a response from this API.</span></span>

## <a name="permissions"></a><span data-ttu-id="14736-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="14736-113">Permissions</span></span>
<span data-ttu-id="14736-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="14736-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="14736-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="14736-116">Permission type</span></span>      | <span data-ttu-id="14736-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="14736-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="14736-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="14736-118">Delegated (work or school account)</span></span> | <span data-ttu-id="14736-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="14736-119">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="14736-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="14736-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="14736-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="14736-121">Not supported.</span></span>    |
|<span data-ttu-id="14736-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="14736-122">Application</span></span> | <span data-ttu-id="14736-123">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="14736-123">Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="14736-124">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="14736-124">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="14736-125">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="14736-125">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="14736-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="14736-126">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/unarchive
```

## <a name="request-headers"></a><span data-ttu-id="14736-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="14736-127">Request headers</span></span>
| <span data-ttu-id="14736-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14736-128">Header</span></span>       | <span data-ttu-id="14736-129">Valor</span><span class="sxs-lookup"><span data-stu-id="14736-129">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="14736-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="14736-130">Authorization</span></span>  | <span data-ttu-id="14736-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="14736-p107">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="14736-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="14736-133">Request body</span></span>
<span data-ttu-id="14736-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="14736-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="14736-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="14736-135">Response</span></span>

<span data-ttu-id="14736-136">Si unarchiving se ha iniciado correctamente, este método devuelve una `202 Accepted` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="14736-136">If unarchiving is started successfully, this method returns a `202 Accepted` response code.</span></span> <span data-ttu-id="14736-137">La respuesta contendrá también un `Location` encabezado, que contiene la ubicación de la [teamsAsyncOperation](../resources/teamsasyncoperation.md) que se creó para controlar unarchiving del equipo.</span><span class="sxs-lookup"><span data-stu-id="14736-137">The response will also contain a `Location` header, which contains the location of the [teamsAsyncOperation](../resources/teamsasyncoperation.md) that was created to handle unarchiving of the team.</span></span> <span data-ttu-id="14736-138">Comprobar el estado de la operación unarchiving mediante la realización de una solicitud GET en esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="14736-138">Check the status of the unarchiving operation by making a GET request to this location.</span></span>

## <a name="example"></a><span data-ttu-id="14736-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="14736-139">Example</span></span>
#### <a name="request"></a><span data-ttu-id="14736-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="14736-140">Request</span></span>
<span data-ttu-id="14736-141">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="14736-141">The following is an example of a request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "unarchive_team"
}-->
```http
POST https://graph.microsoft.com/beta/teams/{id}/unarchive
```

#### <a name="response"></a><span data-ttu-id="14736-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="14736-142">Response</span></span>
<span data-ttu-id="14736-143">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="14736-143">The following is an example of a response.</span></span>
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

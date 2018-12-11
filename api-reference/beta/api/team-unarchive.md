---
title: Unarchive equipo
description: Restaurar un equipo archivado. Esto restaura la capacidad de los usuarios enviar mensajes y editar el equipo, respetando por la configuración de inquilino y del equipo. Los equipos se archivan con la API de archivo.
ms.openlocfilehash: 7ea400e93efceed7b8a35de24339739bcaa9d74f
ms.sourcegitcommit: 72d4da2a6bfaf99fa4edaf6ce3b97b1a6d96d874
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2018
ms.locfileid: "27222461"
---
# <a name="unarchive-team"></a><span data-ttu-id="7555d-105">Unarchive equipo</span><span class="sxs-lookup"><span data-stu-id="7555d-105">Unarchive team</span></span>

> <span data-ttu-id="7555d-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7555d-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7555d-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7555d-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7555d-108">Restauración de un [equipo](../resources/team.md)de archivado.</span><span class="sxs-lookup"><span data-stu-id="7555d-108">Restore an archived [team](../resources/team.md).</span></span> <span data-ttu-id="7555d-109">Esto restaura la capacidad de los usuarios enviar mensajes y editar el equipo, respetando por la configuración de inquilino y del equipo.</span><span class="sxs-lookup"><span data-stu-id="7555d-109">This restores users' ability to send messages and edit the team, abiding by tenant and team settings.</span></span> <span data-ttu-id="7555d-110">Los equipos se archivan con el [archivo](team-archive.md) API.</span><span class="sxs-lookup"><span data-stu-id="7555d-110">Teams are archived using the [archive](team-archive.md) API.</span></span>

<span data-ttu-id="7555d-111">Unarchiving es una operación asíncrona.</span><span class="sxs-lookup"><span data-stu-id="7555d-111">Unarchiving is an async operation.</span></span> <span data-ttu-id="7555d-112">Un equipo es sin archivar una vez que la operación asincrónica se completa correctamente, lo que puede producirse con posterioridad a una respuesta desde esta API.</span><span class="sxs-lookup"><span data-stu-id="7555d-112">A team is unarchived once the async operation completes successfully, which may occur subsequent to a response from this API.</span></span>

## <a name="permissions"></a><span data-ttu-id="7555d-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="7555d-113">Permissions</span></span>
<span data-ttu-id="7555d-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7555d-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7555d-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7555d-116">Permission type</span></span>      | <span data-ttu-id="7555d-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7555d-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7555d-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7555d-118">Delegated (work or school account)</span></span> | <span data-ttu-id="7555d-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7555d-119">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="7555d-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7555d-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7555d-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7555d-121">Not supported.</span></span>    |
|<span data-ttu-id="7555d-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7555d-122">Application</span></span> | <span data-ttu-id="7555d-123">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7555d-123">Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="7555d-124">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="7555d-124">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="7555d-125">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="7555d-125">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="7555d-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7555d-126">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/unarchive
```

## <a name="request-headers"></a><span data-ttu-id="7555d-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7555d-127">Request headers</span></span>
| <span data-ttu-id="7555d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7555d-128">Header</span></span>       | <span data-ttu-id="7555d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="7555d-129">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="7555d-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="7555d-130">Authorization</span></span>  | <span data-ttu-id="7555d-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7555d-p107">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="7555d-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7555d-133">Request body</span></span>
<span data-ttu-id="7555d-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7555d-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7555d-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7555d-135">Response</span></span>

<span data-ttu-id="7555d-136">Si unarchiving se ha iniciado correctamente, este método devuelve una `202 Accepted` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="7555d-136">If unarchiving is started successfully, this method returns a `202 Accepted` response code.</span></span> <span data-ttu-id="7555d-137">La respuesta contendrá también un `Location` encabezado, que contiene la ubicación de la [teamsAsyncOperation](../resources/teamsasyncoperation.md) que se creó para controlar unarchiving del equipo.</span><span class="sxs-lookup"><span data-stu-id="7555d-137">The response will also contain a `Location` header, which contains the location of the [teamsAsyncOperation](../resources/teamsasyncoperation.md) that was created to handle unarchiving of the team.</span></span> <span data-ttu-id="7555d-138">Comprobar el estado de la operación unarchiving mediante la realización de una solicitud GET en esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="7555d-138">Check the status of the unarchiving operation by making a GET request to this location.</span></span>

## <a name="example"></a><span data-ttu-id="7555d-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7555d-139">Example</span></span>
#### <a name="request"></a><span data-ttu-id="7555d-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7555d-140">Request</span></span>
<span data-ttu-id="7555d-141">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="7555d-141">The following is an example of a request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "unarchive_team"
}-->
```http
POST https://graph.microsoft.com/beta/teams/{id}/unarchive
```

#### <a name="response"></a><span data-ttu-id="7555d-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7555d-142">Response</span></span>
<span data-ttu-id="7555d-143">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="7555d-143">The following is an example of a response.</span></span>
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

---
title: Equipo de archivo
description: 'Archivar el equipo especificado. '
ms.openlocfilehash: 3e25a6b5cf5475eeacfb7b01e52775e0b483b2be
ms.sourcegitcommit: 72d4da2a6bfaf99fa4edaf6ce3b97b1a6d96d874
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2018
ms.locfileid: "27222558"
---
# <a name="archive-team"></a><span data-ttu-id="eee48-103">Equipo de archivo</span><span class="sxs-lookup"><span data-stu-id="eee48-103">Archive team</span></span>

> <span data-ttu-id="eee48-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eee48-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eee48-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eee48-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="eee48-106">Archivar el [equipo](../resources/team.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="eee48-106">Archive the specified [team](../resources/team.md).</span></span> <span data-ttu-id="eee48-107">Cuando un equipo se archiva, los usuarios pueden enviar ya no o como mensajes en cualquier canal en el equipo, modificar otras opciones de configuración, descripción o nombre del grupo o en general realizar mayoría de los cambios en el equipo.</span><span class="sxs-lookup"><span data-stu-id="eee48-107">When a team is archived, users can no longer send or like messages on any channel in the team, edit the team's name, description, or other settings, or in general make most changes to the team.</span></span>
<span data-ttu-id="eee48-108">Continuarán con los cambios de pertenencia en el equipo que se permitirán.</span><span class="sxs-lookup"><span data-stu-id="eee48-108">Membership changes to the team continue to be allowed.</span></span>

<span data-ttu-id="eee48-109">El archivado es una operación asíncrona.</span><span class="sxs-lookup"><span data-stu-id="eee48-109">Archiving is an async operation.</span></span> <span data-ttu-id="eee48-110">Un equipo se archiva una vez que la operación asincrónica se completa correctamente, lo que puede producirse con posterioridad a una respuesta desde esta API.</span><span class="sxs-lookup"><span data-stu-id="eee48-110">A team is archived once the async operation completes successfully, which may occur subsequent to a response from this API.</span></span>

<span data-ttu-id="eee48-111">Para poder archivar el equipo, el equipo y el [grupo](../resources/group.md) deben tener un propietario.</span><span class="sxs-lookup"><span data-stu-id="eee48-111">In order to archive team, the team and [group](../resources/group.md) must have an owner.</span></span>

<span data-ttu-id="eee48-112">Para restaurar un equipo de su estado archivado, use la API de [unarchive](team-unarchive.md).</span><span class="sxs-lookup"><span data-stu-id="eee48-112">To restore a team from its archived state, use the API to [unarchive](team-unarchive.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="eee48-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="eee48-113">Permissions</span></span>
<span data-ttu-id="eee48-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eee48-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eee48-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eee48-116">Permission type</span></span>      | <span data-ttu-id="eee48-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eee48-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eee48-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eee48-118">Delegated (work or school account)</span></span> | <span data-ttu-id="eee48-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eee48-119">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="eee48-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eee48-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eee48-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eee48-121">Not supported.</span></span>    |
|<span data-ttu-id="eee48-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eee48-122">Application</span></span> | <span data-ttu-id="eee48-123">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eee48-123">Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="eee48-124">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="eee48-124">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="eee48-125">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="eee48-125">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="eee48-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eee48-126">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/archive
```
## <a name="request-headers"></a><span data-ttu-id="eee48-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eee48-127">Request headers</span></span>
| <span data-ttu-id="eee48-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eee48-128">Header</span></span>       | <span data-ttu-id="eee48-129">Valor</span><span class="sxs-lookup"><span data-stu-id="eee48-129">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="eee48-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="eee48-130">Authorization</span></span>  | <span data-ttu-id="eee48-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eee48-p106">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="eee48-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eee48-133">Request body</span></span>
<span data-ttu-id="eee48-134">En la solicitud, _opcionalmente_ puede incluir la `shouldSetSpoSiteReadOnlyForMembers` parámetro en un JSON body, como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="eee48-134">In the request, you may _optionally_ include the `shouldSetSpoSiteReadOnlyForMembers` parameter in a JSON body, as follows.</span></span>
```JSON
{
    "shouldSetSpoSiteReadOnlyForMembers": true
}
```
<span data-ttu-id="eee48-135">Este parámetro opcional define si se va a establecer permisos para los miembros del equipo de solo lectura en el sitio de Sharepoint Online asociado con el equipo.</span><span class="sxs-lookup"><span data-stu-id="eee48-135">This optional parameter defines whether to set permissions for team members to read-only on the Sharepoint Online site associated with the team.</span></span> <span data-ttu-id="eee48-136">Si se establece en false o se omite el cuerpo por completo, se producirá este paso se omitirá.</span><span class="sxs-lookup"><span data-stu-id="eee48-136">Setting it to false or omitting the body altogether will result in this step being skipped.</span></span>

## <a name="response"></a><span data-ttu-id="eee48-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eee48-137">Response</span></span>

<span data-ttu-id="eee48-138">Si el archivado se ha iniciado correctamente, este método devuelve una `202 Accepted` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="eee48-138">If archiving is started successfully, this method returns a `202 Accepted` response code.</span></span> <span data-ttu-id="eee48-139">La respuesta contendrá también un `Location` encabezado, que contiene la ubicación de la [teamsAsyncOperation](../resources/teamsasyncoperation.md) que se creó para controlar el archivado del equipo.</span><span class="sxs-lookup"><span data-stu-id="eee48-139">The response will also contain a `Location` header, which contains the location of the [teamsAsyncOperation](../resources/teamsasyncoperation.md) that was created to handle archiving of the team.</span></span> <span data-ttu-id="eee48-140">Comprobar el estado de la operación de archivado mediante la realización de una solicitud GET en esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="eee48-140">Check the status of the archiving operation by making a GET request to this location.</span></span>

## <a name="example"></a><span data-ttu-id="eee48-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eee48-141">Example</span></span>
#### <a name="request"></a><span data-ttu-id="eee48-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eee48-142">Request</span></span>
<span data-ttu-id="eee48-143">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="eee48-143">The following is an example of a request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "archive_team"
}-->
```http
POST https://graph.microsoft.com/beta/teams/{id}/archive
```
#### <a name="response"></a><span data-ttu-id="eee48-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eee48-144">Response</span></span>
<span data-ttu-id="eee48-145">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="eee48-145">The following is an example of a response.</span></span>
```http
HTTP/1.1 202 Accepted
Location: /teams{id}/operations({opId})
Content-Type: text/plain
Content-Length: 0
```
<!-- uuid: e848414b-4669-4484-ac36-1504c58a3fb8
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Archive team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

---
title: Equipo de archivo
description: 'Archivar el equipo especificado. '
author: nkramer
localization_priority: Priority
ms.openlocfilehash: 5a364fe025688bf082de187940e40acdee22d6a2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27882855"
---
# <a name="archive-team"></a><span data-ttu-id="b999e-103">Equipo de archivo</span><span class="sxs-lookup"><span data-stu-id="b999e-103">Archive team</span></span>



<span data-ttu-id="b999e-104">Archivar el [equipo](../resources/team.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="b999e-104">Archive the specified [team](../resources/team.md).</span></span> <span data-ttu-id="b999e-105">Cuando un equipo se archiva, los usuarios pueden enviar ya no o como mensajes en cualquier canal en el equipo, modificar otras opciones de configuración, descripción o nombre del grupo o en general realizar mayoría de los cambios en el equipo.</span><span class="sxs-lookup"><span data-stu-id="b999e-105">When a team is archived, users can no longer send or like messages on any channel in the team, edit the team's name, description, or other settings, or in general make most changes to the team.</span></span>
<span data-ttu-id="b999e-106">Continuarán con los cambios de pertenencia en el equipo que se permitirán.</span><span class="sxs-lookup"><span data-stu-id="b999e-106">Membership changes to the team continue to be allowed.</span></span>

<span data-ttu-id="b999e-107">El archivado es una operación asíncrona.</span><span class="sxs-lookup"><span data-stu-id="b999e-107">Archiving is an async operation.</span></span> <span data-ttu-id="b999e-108">Un equipo se archiva una vez que la operación asincrónica se completa correctamente, lo que puede producirse con posterioridad a una respuesta desde esta API.</span><span class="sxs-lookup"><span data-stu-id="b999e-108">A team is archived once the async operation completes successfully, which may occur subsequent to a response from this API.</span></span>

<span data-ttu-id="b999e-109">Para poder archivar el equipo, el equipo y el [grupo](../resources/group.md) deben tener un propietario.</span><span class="sxs-lookup"><span data-stu-id="b999e-109">In order to archive team, the team and [group](../resources/group.md) must have an owner.</span></span>

<span data-ttu-id="b999e-110">Para restaurar un equipo de su estado archivado, use la API de [unarchive](team-unarchive.md).</span><span class="sxs-lookup"><span data-stu-id="b999e-110">To restore a team from its archived state, use the API to [unarchive](team-unarchive.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="b999e-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="b999e-111">Permissions</span></span>
<span data-ttu-id="b999e-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b999e-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b999e-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b999e-114">Permission type</span></span>      | <span data-ttu-id="b999e-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b999e-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b999e-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b999e-116">Delegated (work or school account)</span></span> | <span data-ttu-id="b999e-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b999e-117">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="b999e-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b999e-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b999e-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b999e-119">Not supported.</span></span>    |
|<span data-ttu-id="b999e-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b999e-120">Application</span></span> | <span data-ttu-id="b999e-121">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b999e-121">Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="b999e-122">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="b999e-122">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="b999e-123">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="b999e-123">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="b999e-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b999e-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/archive
```
## <a name="request-headers"></a><span data-ttu-id="b999e-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b999e-125">Request headers</span></span>
| <span data-ttu-id="b999e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b999e-126">Header</span></span>       | <span data-ttu-id="b999e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b999e-127">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b999e-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="b999e-128">Authorization</span></span>  | <span data-ttu-id="b999e-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b999e-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b999e-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b999e-131">Request body</span></span>
<span data-ttu-id="b999e-132">En la solicitud, _opcionalmente_ puede incluir la `shouldSetSpoSiteReadOnlyForMembers` parámetro en un JSON body, como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="b999e-132">In the request, you may _optionally_ include the `shouldSetSpoSiteReadOnlyForMembers` parameter in a JSON body, as follows.</span></span>
```JSON
{
    "shouldSetSpoSiteReadOnlyForMembers": true
}
```
<span data-ttu-id="b999e-133">Este parámetro opcional define si se va a establecer permisos para los miembros del equipo de solo lectura en el sitio de Sharepoint Online asociado con el equipo.</span><span class="sxs-lookup"><span data-stu-id="b999e-133">This optional parameter defines whether to set permissions for team members to read-only on the Sharepoint Online site associated with the team.</span></span> <span data-ttu-id="b999e-134">Si se establece en false o se omite el cuerpo por completo, se producirá este paso se omitirá.</span><span class="sxs-lookup"><span data-stu-id="b999e-134">Setting it to false or omitting the body altogether will result in this step being skipped.</span></span>

## <a name="response"></a><span data-ttu-id="b999e-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b999e-135">Response</span></span>

<span data-ttu-id="b999e-136">Si el archivado se ha iniciado correctamente, este método devuelve una `202 Accepted` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="b999e-136">If archiving is started successfully, this method returns a `202 Accepted` response code.</span></span> <span data-ttu-id="b999e-137">La respuesta contendrá también un `Location` encabezado, que contiene la ubicación de la [teamsAsyncOperation](../resources/teamsasyncoperation.md) que se creó para controlar el archivado del equipo.</span><span class="sxs-lookup"><span data-stu-id="b999e-137">The response will also contain a `Location` header, which contains the location of the [teamsAsyncOperation](../resources/teamsasyncoperation.md) that was created to handle archiving of the team.</span></span> <span data-ttu-id="b999e-138">Comprobar el estado de la operación de archivado mediante la realización de una solicitud GET en esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="b999e-138">Check the status of the archiving operation by making a GET request to this location.</span></span>

## <a name="example"></a><span data-ttu-id="b999e-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b999e-139">Example</span></span>
#### <a name="request"></a><span data-ttu-id="b999e-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b999e-140">Request</span></span>
<span data-ttu-id="b999e-141">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="b999e-141">The following is an example of a request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "archive_team"
}-->
```http
POST https://graph.microsoft.com/beta/teams/{id}/archive
```
#### <a name="response"></a><span data-ttu-id="b999e-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b999e-142">Response</span></span>
<span data-ttu-id="b999e-143">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="b999e-143">The following is an example of a response.</span></span>
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

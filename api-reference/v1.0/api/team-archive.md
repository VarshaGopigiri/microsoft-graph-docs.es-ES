---
title: Equipo de archivo
description: 'Archivar el equipo especificado. '
ms.openlocfilehash: 414b45a3dd2f03aba29b3393db3ef547472a8950
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030791"
---
# <a name="archive-team"></a><span data-ttu-id="ed36c-103">Equipo de archivo</span><span class="sxs-lookup"><span data-stu-id="ed36c-103">Archive team</span></span>



<span data-ttu-id="ed36c-104">Archivar el [equipo](../resources/team.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="ed36c-104">Archive the specified [team](../resources/team.md).</span></span> <span data-ttu-id="ed36c-105">Cuando un equipo se archiva, los usuarios pueden enviar ya no o como mensajes en cualquier canal en el equipo, modificar otras opciones de configuración, descripción o nombre del grupo o en general realizar mayoría de los cambios en el equipo.</span><span class="sxs-lookup"><span data-stu-id="ed36c-105">When a team is archived, users can no longer send or like messages on any channel in the team, edit the team's name, description, or other settings, or in general make most changes to the team.</span></span>
<span data-ttu-id="ed36c-106">Continuarán con los cambios de pertenencia en el equipo que se permitirán.</span><span class="sxs-lookup"><span data-stu-id="ed36c-106">Membership changes to the team continue to be allowed.</span></span>

<span data-ttu-id="ed36c-107">El archivado es una operación asíncrona.</span><span class="sxs-lookup"><span data-stu-id="ed36c-107">Archiving is an async operation.</span></span> <span data-ttu-id="ed36c-108">Un equipo se archiva una vez que la operación asincrónica se completa correctamente, lo que puede producirse con posterioridad a una respuesta desde esta API.</span><span class="sxs-lookup"><span data-stu-id="ed36c-108">A team is archived once the async operation completes successfully, which may occur subsequent to a response from this API.</span></span>

<span data-ttu-id="ed36c-109">Para poder archivar el equipo, el equipo y el [grupo](../resources/group.md) deben tener un propietario.</span><span class="sxs-lookup"><span data-stu-id="ed36c-109">In order to archive team, the team and [group](../resources/group.md) must have an owner.</span></span>

<span data-ttu-id="ed36c-110">Para restaurar un equipo de su estado archivado, use la API de [unarchive](team-unarchive.md).</span><span class="sxs-lookup"><span data-stu-id="ed36c-110">To restore a team from its archived state, use the API to [unarchive](team-unarchive.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="ed36c-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="ed36c-111">Permissions</span></span>
<span data-ttu-id="ed36c-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ed36c-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ed36c-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ed36c-114">Permission type</span></span>      | <span data-ttu-id="ed36c-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ed36c-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ed36c-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ed36c-116">Delegated (work or school account)</span></span> | <span data-ttu-id="ed36c-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed36c-117">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ed36c-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ed36c-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ed36c-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ed36c-119">Not supported.</span></span>    |
|<span data-ttu-id="ed36c-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ed36c-120">Application</span></span> | <span data-ttu-id="ed36c-121">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed36c-121">Group.ReadWrite.All</span></span>    |

## <a name="http-request"></a><span data-ttu-id="ed36c-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ed36c-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/archive
```
## <a name="request-headers"></a><span data-ttu-id="ed36c-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ed36c-123">Request headers</span></span>
| <span data-ttu-id="ed36c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed36c-124">Header</span></span>       | <span data-ttu-id="ed36c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ed36c-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ed36c-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="ed36c-126">Authorization</span></span>  | <span data-ttu-id="ed36c-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ed36c-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ed36c-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ed36c-129">Request body</span></span>
<span data-ttu-id="ed36c-130">En la solicitud, _opcionalmente_ puede incluir la `shouldSetSpoSiteReadOnlyForMembers` parámetro en un JSON body, como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="ed36c-130">In the request, you may _optionally_ include the `shouldSetSpoSiteReadOnlyForMembers` parameter in a JSON body, as follows.</span></span>
```JSON
{
    "shouldSetSpoSiteReadOnlyForMembers": true
}
```
<span data-ttu-id="ed36c-131">Este parámetro opcional define si se va a establecer permisos para los miembros del equipo de solo lectura en el sitio de Sharepoint Online asociado con el equipo.</span><span class="sxs-lookup"><span data-stu-id="ed36c-131">This optional parameter defines whether to set permissions for team members to read-only on the Sharepoint Online site associated with the team.</span></span> <span data-ttu-id="ed36c-132">Si se establece en false o se omite el cuerpo por completo, se producirá este paso se omitirá.</span><span class="sxs-lookup"><span data-stu-id="ed36c-132">Setting it to false or omitting the body altogether will result in this step being skipped.</span></span>

## <a name="response"></a><span data-ttu-id="ed36c-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed36c-133">Response</span></span>

<span data-ttu-id="ed36c-134">Si el archivado se ha iniciado correctamente, este método devuelve una `202 Accepted` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed36c-134">If archiving is started successfully, this method returns a `202 Accepted` response code.</span></span> <span data-ttu-id="ed36c-135">La respuesta contendrá también un `Location` encabezado, que contiene la ubicación de la [teamsAsyncOperation](../resources/teamsasyncoperation.md) que se creó para controlar el archivado del equipo.</span><span class="sxs-lookup"><span data-stu-id="ed36c-135">The response will also contain a `Location` header, which contains the location of the [teamsAsyncOperation](../resources/teamsasyncoperation.md) that was created to handle archiving of the team.</span></span> <span data-ttu-id="ed36c-136">Comprobar el estado de la operación de archivado mediante la realización de una solicitud GET en esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="ed36c-136">Check the status of the archiving operation by making a GET request to this location.</span></span>

## <a name="example"></a><span data-ttu-id="ed36c-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ed36c-137">Example</span></span>
#### <a name="request"></a><span data-ttu-id="ed36c-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ed36c-138">Request</span></span>
<span data-ttu-id="ed36c-139">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ed36c-139">The following is an example of a request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "archive_team"
}-->
```http
POST https://graph.microsoft.com/beta/teams/{id}/archive
```
#### <a name="response"></a><span data-ttu-id="ed36c-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed36c-140">Response</span></span>
<span data-ttu-id="ed36c-141">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed36c-141">The following is an example of a response.</span></span>
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

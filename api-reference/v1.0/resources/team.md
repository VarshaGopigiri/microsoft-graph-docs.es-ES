---
title: tipo de recurso de equipo
description: 'Un equipo en Microsoft Teams es una colección de canales. '
ms.openlocfilehash: 62a20629dc3e62da730a3821395af5cc2417d56f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029798"
---
# <a name="team-resource-type"></a><span data-ttu-id="34ace-103">tipo de recurso de equipo</span><span class="sxs-lookup"><span data-stu-id="34ace-103">team resource type</span></span>



<span data-ttu-id="34ace-104">Un equipo en Microsoft Teams es una colección de [canales](channel.md).</span><span class="sxs-lookup"><span data-stu-id="34ace-104">A team in Microsoft Teams is a collection of [channels](channel.md).</span></span> <span data-ttu-id="34ace-105">Un canal representa un tema y, por lo tanto, un aislamiento lógico de discusión, dentro de un equipo.</span><span class="sxs-lookup"><span data-stu-id="34ace-105">A channel represents a topic, and therefore a logical isolation of discussion, within a team.</span></span>

<span data-ttu-id="34ace-106">Cada equipo está asociado con un [grupo](../resources/group.md).</span><span class="sxs-lookup"><span data-stu-id="34ace-106">Every team is associated with a [group](../resources/group.md).</span></span>
<span data-ttu-id="34ace-107">El grupo tiene el mismo identificador que el equipo - /groups/ por ejemplo, {identificador} / equipo es el mismo que /teams/ {identificador}.</span><span class="sxs-lookup"><span data-stu-id="34ace-107">The group has the same ID as the team - for example, /groups/{id}/team is the same as /teams/{id}.</span></span>
<span data-ttu-id="34ace-108">Para obtener más información sobre cómo trabajar con los miembros de los equipos y grupos, vea [uso de la API de REST de Microsoft Graph para que funcione con los equipos de Microsoft](teams-api-overview.md).</span><span class="sxs-lookup"><span data-stu-id="34ace-108">For more information about working with groups and members in teams, see [Use the Microsoft Graph REST API to work with Microsoft Teams](teams-api-overview.md).</span></span>

## <a name="methods"></a><span data-ttu-id="34ace-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="34ace-109">Methods</span></span>

| <span data-ttu-id="34ace-110">Método</span><span class="sxs-lookup"><span data-stu-id="34ace-110">Method</span></span>       | <span data-ttu-id="34ace-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34ace-111">Return Type</span></span>  |<span data-ttu-id="34ace-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="34ace-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="34ace-113">Crear equipo</span><span class="sxs-lookup"><span data-stu-id="34ace-113">Create team</span></span>](../api/team-put-teams.md) | [<span data-ttu-id="34ace-114">equipo</span><span class="sxs-lookup"><span data-stu-id="34ace-114">team</span></span>](team.md) | <span data-ttu-id="34ace-115">Crear un nuevo equipo o agregar un equipo a un grupo existente.</span><span class="sxs-lookup"><span data-stu-id="34ace-115">Create a new team, or add a team to an existing group.</span></span>|
|[<span data-ttu-id="34ace-116">Obtener el equipo</span><span class="sxs-lookup"><span data-stu-id="34ace-116">Get team</span></span>](../api/team-get.md) | [<span data-ttu-id="34ace-117">equipo</span><span class="sxs-lookup"><span data-stu-id="34ace-117">team</span></span>](team.md) | <span data-ttu-id="34ace-118">Recuperar las propiedades y relaciones del equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="34ace-118">Retrieve the properties and relationships of the specified team.</span></span>|
|[<span data-ttu-id="34ace-119">Equipo de actualización</span><span class="sxs-lookup"><span data-stu-id="34ace-119">Update team</span></span>](../api/team-update.md) | [<span data-ttu-id="34ace-120">equipo</span><span class="sxs-lookup"><span data-stu-id="34ace-120">team</span></span>](team.md) |<span data-ttu-id="34ace-121">Actualizar las propiedades del equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="34ace-121">Update the properties of the specified team.</span></span> |
|[<span data-ttu-id="34ace-122">Eliminar grupo</span><span class="sxs-lookup"><span data-stu-id="34ace-122">Delete team</span></span>](/graph/api/group-delete?view=graph-rest-1.0) | <span data-ttu-id="34ace-123">Ninguno</span><span class="sxs-lookup"><span data-stu-id="34ace-123">None</span></span> |<span data-ttu-id="34ace-124">Eliminar el equipo y el grupo asociado.</span><span class="sxs-lookup"><span data-stu-id="34ace-124">Delete the team and its associated group.</span></span> |
|[<span data-ttu-id="34ace-125">Clonación de equipo</span><span class="sxs-lookup"><span data-stu-id="34ace-125">Clone team</span></span>](../api/team-clone.md) | [<span data-ttu-id="34ace-126">teamsAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="34ace-126">teamsAsyncOperation</span></span>](../resources/teamsasyncoperation.md) |<span data-ttu-id="34ace-127">Copie el equipo y el grupo asociado.</span><span class="sxs-lookup"><span data-stu-id="34ace-127">Copy the team and its associated group.</span></span> |
|[<span data-ttu-id="34ace-128">Equipo de archivo</span><span class="sxs-lookup"><span data-stu-id="34ace-128">Archive team</span></span>](../api/team-archive.md) | [<span data-ttu-id="34ace-129">teamsAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="34ace-129">teamsAsyncOperation</span></span>](../resources/teamsasyncoperation.md) |<span data-ttu-id="34ace-130">Poner el equipo en un estado de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="34ace-130">Put the team in a read-only state.</span></span> |
|[<span data-ttu-id="34ace-131">Unarchive equipo</span><span class="sxs-lookup"><span data-stu-id="34ace-131">Unarchive team</span></span>](../api/team-unarchive.md) | [<span data-ttu-id="34ace-132">teamsAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="34ace-132">teamsAsyncOperation</span></span>](../resources/teamsasyncoperation.md) |<span data-ttu-id="34ace-133">Restaure el equipo a un estado de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="34ace-133">Restore the team to a read-write state.</span></span> |
|[<span data-ttu-id="34ace-134">Lista de los equipos</span><span class="sxs-lookup"><span data-stu-id="34ace-134">List your teams</span></span>](../api/user-list-joinedteams.md) | <span data-ttu-id="34ace-135">colección de [equipo](team.md)</span><span class="sxs-lookup"><span data-stu-id="34ace-135">[team](team.md) collection</span></span> | <span data-ttu-id="34ace-136">Lista de los equipos de que es un miembro.</span><span class="sxs-lookup"><span data-stu-id="34ace-136">List the teams you are a member of.</span></span> |
|[<span data-ttu-id="34ace-137">Lista de todos los equipos</span><span class="sxs-lookup"><span data-stu-id="34ace-137">List all teams</span></span>](/graph/teams-list-all-teams) | <span data-ttu-id="34ace-138">Colección [group](group.md)</span><span class="sxs-lookup"><span data-stu-id="34ace-138">[group](group.md) collection</span></span> | <span data-ttu-id="34ace-139">Lista de todos los grupos que tienen los equipos.</span><span class="sxs-lookup"><span data-stu-id="34ace-139">List all groups that have teams.</span></span> |
|[<span data-ttu-id="34ace-140">Publicar aplicaciones en la organización</span><span class="sxs-lookup"><span data-stu-id="34ace-140">Publish apps to your organization</span></span>](../resources/teamsapp.md)| [<span data-ttu-id="34ace-141">teamsApp</span><span class="sxs-lookup"><span data-stu-id="34ace-141">teamsApp</span></span>](../resources/teamsapp.md) | <span data-ttu-id="34ace-142">Crear aplicaciones de los equipos sólo es visible para su organización.</span><span class="sxs-lookup"><span data-stu-id="34ace-142">Create Teams apps visible only to your organization.</span></span> |
|[<span data-ttu-id="34ace-143">Agregar la aplicación al equipo</span><span class="sxs-lookup"><span data-stu-id="34ace-143">Add app to team</span></span>](../api/teamsappinstallation-add.md) | [<span data-ttu-id="34ace-144">teamsappinstallation</span><span class="sxs-lookup"><span data-stu-id="34ace-144">teamsappinstallation</span></span>](teamsappinstallation.md) | <span data-ttu-id="34ace-145">Agrega (se instala) una aplicación a un equipo.</span><span class="sxs-lookup"><span data-stu-id="34ace-145">Adds (installs) an app to a team.</span></span>|
|[<span data-ttu-id="34ace-146">Agregar una ficha a canal</span><span class="sxs-lookup"><span data-stu-id="34ace-146">Add tab to channel</span></span>](../api/teamstab-add.md) | [<span data-ttu-id="34ace-147">teamsTab</span><span class="sxs-lookup"><span data-stu-id="34ace-147">teamsTab</span></span>](../resources/teamstab.md) | <span data-ttu-id="34ace-148">(Se instala) se agrega una ficha a canal de un equipo.</span><span class="sxs-lookup"><span data-stu-id="34ace-148">Adds (installs) a tab to a team's channel.</span></span>|

## <a name="properties"></a><span data-ttu-id="34ace-149">Propiedades</span><span class="sxs-lookup"><span data-stu-id="34ace-149">Properties</span></span>

| <span data-ttu-id="34ace-150">Propiedad</span><span class="sxs-lookup"><span data-stu-id="34ace-150">Property</span></span> | <span data-ttu-id="34ace-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="34ace-151">Type</span></span>   | <span data-ttu-id="34ace-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="34ace-152">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="34ace-153">funSettings</span><span class="sxs-lookup"><span data-stu-id="34ace-153">funSettings</span></span>|[<span data-ttu-id="34ace-154">teamFunSettings</span><span class="sxs-lookup"><span data-stu-id="34ace-154">teamFunSettings</span></span>](teamfunsettings.md) |<span data-ttu-id="34ace-155">Opciones para configurar el uso de Giphy, memes y pegatinas en el equipo.</span><span class="sxs-lookup"><span data-stu-id="34ace-155">Settings to configure use of Giphy, memes, and stickers in the team.</span></span>|
|<span data-ttu-id="34ace-156">guestSettings</span><span class="sxs-lookup"><span data-stu-id="34ace-156">guestSettings</span></span>|[<span data-ttu-id="34ace-157">teamGuestSettings</span><span class="sxs-lookup"><span data-stu-id="34ace-157">teamGuestSettings</span></span>](teamguestsettings.md) |<span data-ttu-id="34ace-158">Configuración para configurar si los invitados pueden crear, actualizar o eliminar los canales en el equipo.</span><span class="sxs-lookup"><span data-stu-id="34ace-158">Settings to configure whether guests can create, update, or delete channels in the team.</span></span>|
|<span data-ttu-id="34ace-159">isArchived</span><span class="sxs-lookup"><span data-stu-id="34ace-159">isArchived</span></span>|<span data-ttu-id="34ace-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="34ace-160">Boolean</span></span>|<span data-ttu-id="34ace-161">Si este equipo está en modo de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="34ace-161">Whether this team is in read-only mode.</span></span> |
|<span data-ttu-id="34ace-162">memberSettings</span><span class="sxs-lookup"><span data-stu-id="34ace-162">memberSettings</span></span>|[<span data-ttu-id="34ace-163">teamMemberSettings</span><span class="sxs-lookup"><span data-stu-id="34ace-163">teamMemberSettings</span></span>](teammembersettings.md) |<span data-ttu-id="34ace-164">Configuración para configurar si los miembros pueden realizar determinadas acciones, por ejemplo, creación de canales y agrega bots, en el equipo.</span><span class="sxs-lookup"><span data-stu-id="34ace-164">Settings to configure whether members can perform certain actions, for example, create channels and add bots, in the team.</span></span>|
|<span data-ttu-id="34ace-165">messagingSettings</span><span class="sxs-lookup"><span data-stu-id="34ace-165">messagingSettings</span></span>|[<span data-ttu-id="34ace-166">teamMessagingSettings</span><span class="sxs-lookup"><span data-stu-id="34ace-166">teamMessagingSettings</span></span>](teammessagingsettings.md) |<span data-ttu-id="34ace-167">La configuración de mensajería y menciones en el equipo.</span><span class="sxs-lookup"><span data-stu-id="34ace-167">Settings to configure messaging and mentions in the team.</span></span>|
|<span data-ttu-id="34ace-168">webUrl</span><span class="sxs-lookup"><span data-stu-id="34ace-168">webUrl</span></span>|<span data-ttu-id="34ace-169">cadena (sólo lectura)</span><span class="sxs-lookup"><span data-stu-id="34ace-169">string (readonly)</span></span> | <span data-ttu-id="34ace-170">Un hipervínculo que se vaya al equipo en el cliente de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="34ace-170">A hyperlink that will go to the team in the Microsoft Teams client.</span></span> <span data-ttu-id="34ace-171">Esta es la URL que se obtiene cuando haga clic en un equipo en el cliente de Microsoft Teams y seleccione **obtener el vínculo al equipo**.</span><span class="sxs-lookup"><span data-stu-id="34ace-171">This is the URL that you get when you right-click a team in the Microsoft Teams client and select **Get link to team**.</span></span> <span data-ttu-id="34ace-172">Esta dirección URL debe se trata como un objeto binario opaco y no puede analizar.</span><span class="sxs-lookup"><span data-stu-id="34ace-172">This URL should be treated as an opaque blob, and not parsed.</span></span> |

## <a name="relationships"></a><span data-ttu-id="34ace-173">Relaciones</span><span class="sxs-lookup"><span data-stu-id="34ace-173">Relationships</span></span>

| <span data-ttu-id="34ace-174">Relación</span><span class="sxs-lookup"><span data-stu-id="34ace-174">Relationship</span></span> | <span data-ttu-id="34ace-175">Tipo</span><span class="sxs-lookup"><span data-stu-id="34ace-175">Type</span></span>   | <span data-ttu-id="34ace-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="34ace-176">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="34ace-177">canales</span><span class="sxs-lookup"><span data-stu-id="34ace-177">channels</span></span>|<span data-ttu-id="34ace-178">colección de [canal](channel.md)</span><span class="sxs-lookup"><span data-stu-id="34ace-178">[channel](channel.md) collection</span></span>|<span data-ttu-id="34ace-179">La colección de canales de & mensajes asociados con el equipo.</span><span class="sxs-lookup"><span data-stu-id="34ace-179">The collection of channels & messages associated with the team.</span></span>|
|<span data-ttu-id="34ace-180">installedApps</span><span class="sxs-lookup"><span data-stu-id="34ace-180">installedApps</span></span>|<span data-ttu-id="34ace-181">colección de [teamsAppInstallation](teamsappinstallation.md)</span><span class="sxs-lookup"><span data-stu-id="34ace-181">[teamsAppInstallation](teamsappinstallation.md) collection</span></span>|<span data-ttu-id="34ace-182">Las aplicaciones instaladas en este equipo.</span><span class="sxs-lookup"><span data-stu-id="34ace-182">The apps installed in this team.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="34ace-183">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="34ace-183">JSON representation</span></span>

<span data-ttu-id="34ace-184">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="34ace-184">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.team",
  "baseType": "microsoft.graph.entity"
}-->

```json
{  
  "guestSettings": {"@odata.type": "microsoft.graph.teamGuestSettings"},
  "memberSettings": {"@odata.type": "microsoft.graph.teamMemberSettings"},
  "messagingSettings": {"@odata.type": "microsoft.graph.teamMessagingSettings"},
  "funSettings": {"@odata.type": "microsoft.graph.teamFunSettings"},
  "isArchived": false,
  "webUrl": "https://...longUrl..."
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "team resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

## <a name="see-also"></a><span data-ttu-id="34ace-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="34ace-185">See Also</span></span>
- [<span data-ttu-id="34ace-186">Creación de un grupo con un equipo</span><span class="sxs-lookup"><span data-stu-id="34ace-186">Creating a group with a team</span></span>](/graph/teams-create-group-and-team)
- [<span data-ttu-id="34ace-187">Uso de las API de los equipos</span><span class="sxs-lookup"><span data-stu-id="34ace-187">Using Teams APIs</span></span>](teams-api-overview.md)

---
title: Clonación de un equipo
description: Crear una copia de un equipo. Esta operación también crea una copia del grupo correspondiente.
ms.openlocfilehash: 8cd6c580db9aa77f87a31bdb9b2878ed9e580e61
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029064"
---
# <a name="clone-a-team"></a><span data-ttu-id="d2692-104">Clonación de un equipo</span><span class="sxs-lookup"><span data-stu-id="d2692-104">Clone a team</span></span>



<span data-ttu-id="d2692-105">Crear una copia de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="d2692-105">Create a copy of a [team](../resources/team.md).</span></span> <span data-ttu-id="d2692-106">Esta operación también crea una copia del [grupo](../resources/group.md)correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d2692-106">This operation also creates a copy of the corresponding [group](../resources/group.md).</span></span>
<span data-ttu-id="d2692-107">Puede especificar qué elementos del equipo que se debe clonar:</span><span class="sxs-lookup"><span data-stu-id="d2692-107">You can specify which parts of the team to clone:</span></span>

- <span data-ttu-id="d2692-108">**aplicaciones** : aplicaciones de los equipos de Microsoft de copias que se instalan en el equipo.</span><span class="sxs-lookup"><span data-stu-id="d2692-108">**apps** - Copies Microsoft Teams apps that are installed in the team.</span></span> 
- <span data-ttu-id="d2692-109">**canales de** – copia la estructura de canal (pero no los mensajes en el canal).</span><span class="sxs-lookup"><span data-stu-id="d2692-109">**channels** – Copies the channel structure (but not the messages in the channel).</span></span>
- <span data-ttu-id="d2692-110">**miembros** : copias de los miembros y propietarios del grupo.</span><span class="sxs-lookup"><span data-stu-id="d2692-110">**members** – Copies the members and owners of the group.</span></span>
- <span data-ttu-id="d2692-111">**configuración** – copia toda la configuración en el equipo, junto con la configuración de grupo de claves.</span><span class="sxs-lookup"><span data-stu-id="d2692-111">**settings** – Copies all settings within the team, along with key group settings.</span></span>
- <span data-ttu-id="d2692-112">**las fichas** – copias de las fichas dentro de los canales.</span><span class="sxs-lookup"><span data-stu-id="d2692-112">**tabs** – Copies the tabs within channels.</span></span>

<span data-ttu-id="d2692-113">Cuando se clonarán las fichas, se ponen en un estado no configurado: se muestran en la barra de pestañas en Microsoft Teams, y la primera vez que se abren, se le dirigirá a través de la pantalla de configuración.</span><span class="sxs-lookup"><span data-stu-id="d2692-113">When tabs are cloned, they are put into an unconfigured state -- they are displayed on the tab bar in Microsoft Teams, and the first time you open them, you'll go through the configuration screen.</span></span> <span data-ttu-id="d2692-114">(Si la persona que abre la ficha no tiene permiso para configurar aplicaciones, verán un mensaje que explica que no se ha configurado la ficha.)</span><span class="sxs-lookup"><span data-stu-id="d2692-114">(If the person opening the tab does not have permission to configure apps, they will see a message explaining that the tab hasn't been configured.)</span></span>

<span data-ttu-id="d2692-115">La clonación es una operación de larga duración.</span><span class="sxs-lookup"><span data-stu-id="d2692-115">Cloning is a long-running operation.</span></span>
<span data-ttu-id="d2692-116">Después de que se devuelve el clon POST, debe obtener la [operación](../resources/teamsasyncoperation.md) para ver si es "que se está ejecutando" o "correcto" o "error".</span><span class="sxs-lookup"><span data-stu-id="d2692-116">After the POST clone returns, you need to GET the [operation](../resources/teamsasyncoperation.md) to see if it's "running" or "succeeded" or "failed".</span></span> <span data-ttu-id="d2692-117">Se debe seguir GET hasta que el estado es no "en ejecución".</span><span class="sxs-lookup"><span data-stu-id="d2692-117">You should continue to GET until the status is not "running".</span></span> <span data-ttu-id="d2692-118">El retraso entre obtiene recomendado es de 5 segundos.</span><span class="sxs-lookup"><span data-stu-id="d2692-118">The recommended delay between GETs is 5 seconds.</span></span>

## <a name="permissions"></a><span data-ttu-id="d2692-119">Permisos</span><span class="sxs-lookup"><span data-stu-id="d2692-119">Permissions</span></span>

<span data-ttu-id="d2692-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d2692-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d2692-122">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2692-122">Permission type</span></span>      | <span data-ttu-id="d2692-123">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2692-123">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d2692-124">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2692-124">Delegated (work or school account)</span></span>     | <span data-ttu-id="d2692-125">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d2692-125">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="d2692-126">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2692-126">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d2692-127">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2692-127">Not supported.</span></span>    |
|<span data-ttu-id="d2692-128">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2692-128">Application</span></span>                            | <span data-ttu-id="d2692-129">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d2692-129">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d2692-130">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2692-130">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/clone
```

## <a name="request-headers"></a><span data-ttu-id="d2692-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2692-131">Request headers</span></span>
| <span data-ttu-id="d2692-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2692-132">Header</span></span>       | <span data-ttu-id="d2692-133">Valor</span><span class="sxs-lookup"><span data-stu-id="d2692-133">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d2692-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="d2692-134">Authorization</span></span>  | <span data-ttu-id="d2692-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d2692-p106">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="d2692-137">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d2692-137">Content-Type</span></span>  | <span data-ttu-id="d2692-138">application/json</span><span class="sxs-lookup"><span data-stu-id="d2692-138">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d2692-139">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2692-139">Request body</span></span>

| <span data-ttu-id="d2692-140">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2692-140">Property</span></span>     | <span data-ttu-id="d2692-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2692-141">Type</span></span>   |<span data-ttu-id="d2692-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2692-142">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d2692-143">classification</span><span class="sxs-lookup"><span data-stu-id="d2692-143">classification</span></span>|<span data-ttu-id="d2692-144">Cadena (opcional)</span><span class="sxs-lookup"><span data-stu-id="d2692-144">String (optional)</span></span>|<span data-ttu-id="d2692-145">Describe una clasificación para el grupo (por ejemplo, el impacto de negocio bajo, medio o alto).</span><span class="sxs-lookup"><span data-stu-id="d2692-145">Describes a classification for the group (such as low, medium or high business impact).</span></span> <span data-ttu-id="d2692-146">Si no se especifica la clasificación, la clasificación se copiarán desde el equipo original o grupo.</span><span class="sxs-lookup"><span data-stu-id="d2692-146">If classification is not specified, the classification will be copied from the original team/group.</span></span>|
|<span data-ttu-id="d2692-147">descripción</span><span class="sxs-lookup"><span data-stu-id="d2692-147">description</span></span>|<span data-ttu-id="d2692-148">Cadena (opcional)</span><span class="sxs-lookup"><span data-stu-id="d2692-148">String (optional)</span></span>|<span data-ttu-id="d2692-149">Una descripción opcional del grupo.</span><span class="sxs-lookup"><span data-stu-id="d2692-149">An optional description for the group.</span></span> <span data-ttu-id="d2692-150">Si no se especifica esta propiedad, se va a dejar en blanco.</span><span class="sxs-lookup"><span data-stu-id="d2692-150">If this property is not specified, it will be left blank.</span></span>|
|<span data-ttu-id="d2692-151">displayName</span><span class="sxs-lookup"><span data-stu-id="d2692-151">displayName</span></span>|<span data-ttu-id="d2692-152">String</span><span class="sxs-lookup"><span data-stu-id="d2692-152">String</span></span>|<span data-ttu-id="d2692-p109">El nombre para mostrar del grupo. Esta propiedad es necesaria cuando se crea un grupo y no se puede borrar durante las actualizaciones. Es compatible con $filter y $orderby.</span><span class="sxs-lookup"><span data-stu-id="d2692-p109">The display name for the group. This property is required when a group is created and it cannot be cleared during updates. Supports $filter and $orderby.</span></span>|
|<span data-ttu-id="d2692-156">mailNickname</span><span class="sxs-lookup"><span data-stu-id="d2692-156">mailNickname</span></span>|<span data-ttu-id="d2692-157">String</span><span class="sxs-lookup"><span data-stu-id="d2692-157">String</span></span>|<span data-ttu-id="d2692-158">El alias de correo para el grupo, único en la organización.</span><span class="sxs-lookup"><span data-stu-id="d2692-158">The mail alias for the group, unique in the organization.</span></span> <span data-ttu-id="d2692-159">Esta propiedad debe especificarse cuando se crea un grupo.</span><span class="sxs-lookup"><span data-stu-id="d2692-159">This property must be specified when a group is created.</span></span> <span data-ttu-id="d2692-160">Es compatible con $filter.</span><span class="sxs-lookup"><span data-stu-id="d2692-160">Supports $filter.</span></span> <span data-ttu-id="d2692-161">Si no se especifica esta propiedad, se calculará de la propiedad displayName.</span><span class="sxs-lookup"><span data-stu-id="d2692-161">If this property is not specified, it will be computed from the displayName.</span></span> <span data-ttu-id="d2692-162">Problema conocido: esta propiedad se omite actualmente.</span><span class="sxs-lookup"><span data-stu-id="d2692-162">Known issue: this property is currently ignored.</span></span>|
|<span data-ttu-id="d2692-163">partsToClone</span><span class="sxs-lookup"><span data-stu-id="d2692-163">partsToClone</span></span>| [<span data-ttu-id="d2692-164">clonableTeamParts</span><span class="sxs-lookup"><span data-stu-id="d2692-164">clonableTeamParts</span></span>](../resources/clonableteamparts.md) |<span data-ttu-id="d2692-165">Una lista separados por comas de los elementos que se debe clonar.</span><span class="sxs-lookup"><span data-stu-id="d2692-165">A comma-seperated list of the parts to clone.</span></span> <span data-ttu-id="d2692-166">Los elementos legales son "aplicaciones, las fichas, configuración, canales, los miembros".</span><span class="sxs-lookup"><span data-stu-id="d2692-166">Legal parts are "apps, tabs, settings, channels, members".</span></span>|
|<span data-ttu-id="d2692-167">visibility</span><span class="sxs-lookup"><span data-stu-id="d2692-167">visibility</span></span>|<span data-ttu-id="d2692-168">[teamVisibilityType](../resources/teamvisibilitytype.md) (opcional)</span><span class="sxs-lookup"><span data-stu-id="d2692-168">[teamVisibilityType](../resources/teamvisibilitytype.md) (optional)</span></span>| <span data-ttu-id="d2692-169">Especifica la visibilidad del grupo.</span><span class="sxs-lookup"><span data-stu-id="d2692-169">Specifies the visibility of the group.</span></span> <span data-ttu-id="d2692-170">Los valores posibles son: **privada**, **pública**.</span><span class="sxs-lookup"><span data-stu-id="d2692-170">Possible values are: **Private**, **Public**.</span></span> <span data-ttu-id="d2692-171">Si no se especifica la visibilidad, la visibilidad se copiarán desde el equipo original o grupo.</span><span class="sxs-lookup"><span data-stu-id="d2692-171">If visibility is not specified, the visibility will be copied from the original team/group.</span></span> <span data-ttu-id="d2692-172">Si el equipo que se está clonando es un equipo de **educationClass** , se omite el parámetro visibilidad y visibilidad del nuevo grupo se establecerá en HiddenMembership.</span><span class="sxs-lookup"><span data-stu-id="d2692-172">If the team being cloned is an **educationClass** team, the visibility parameter is ignored, and the new group's visibility will be set to HiddenMembership.</span></span>|

## <a name="response"></a><span data-ttu-id="d2692-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2692-173">Response</span></span>

<span data-ttu-id="d2692-174">Si tiene éxito, este método devolverá un `202 Accepted` código de respuesta con una ubicación: encabezado que señala hacia el recurso de la [operación](../resources/teamsasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="d2692-174">If successful, this method will return a `202 Accepted` response code with a Location: header pointing to the [operation](../resources/teamsasyncoperation.md) resource.</span></span>
<span data-ttu-id="d2692-175">Una vez finalizada la operación, el recurso de la operación le indicará el identificador del equipo de creada.</span><span class="sxs-lookup"><span data-stu-id="d2692-175">When the operation is complete, the operation resource will tell you the id of the created team.</span></span>

## <a name="example"></a><span data-ttu-id="d2692-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2692-176">Example</span></span>
#### <a name="request"></a><span data-ttu-id="d2692-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2692-177">Request</span></span>
<span data-ttu-id="d2692-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2692-178">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "create_team"
}-->
```http
POST /teams/{id}/clone
Content-Type: application/json

{  
     "displayName": "Library Assist",
     "description": "Self help community for library",
     "mailNickname": "libassist",
     "partsToClone": "apps,tabs,settings,channels,members",
     "visibility": "public"
}
```

#### <a name="response"></a><span data-ttu-id="d2692-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2692-179">Response</span></span>
<span data-ttu-id="d2692-180">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2692-180">The following is an example of the response.</span></span> <span data-ttu-id="d2692-181">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="d2692-181">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="d2692-182">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2692-182">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->
```http
HTTP/1.1 202 Accepted
Location: /teams{id}/operations({opId})
Content-Type: text/plain
Content-Length: 0
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
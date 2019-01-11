---
title: Clonación de un equipo
description: Crear una copia de un equipo. Esta operación también crea una copia del grupo correspondiente.
author: nkramer
localization_priority: Normal
ms.openlocfilehash: 262cbe4bd17cc1ab3abded49b65868d0b8039e70
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854596"
---
# <a name="clone-a-team"></a><span data-ttu-id="651d5-104">Clonación de un equipo</span><span class="sxs-lookup"><span data-stu-id="651d5-104">Clone a team</span></span>

> <span data-ttu-id="651d5-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="651d5-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="651d5-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="651d5-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="651d5-107">Crear una copia de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="651d5-107">Create a copy of a [team](../resources/team.md).</span></span> <span data-ttu-id="651d5-108">Esta operación también crea una copia del [grupo](../resources/group.md)correspondiente.</span><span class="sxs-lookup"><span data-stu-id="651d5-108">This operation also creates a copy of the corresponding [group](../resources/group.md).</span></span>
<span data-ttu-id="651d5-109">Puede especificar qué elementos del equipo que se debe clonar:</span><span class="sxs-lookup"><span data-stu-id="651d5-109">You can specify which parts of the team to clone:</span></span>

- <span data-ttu-id="651d5-110">**aplicaciones** : aplicaciones de los equipos de Microsoft de copias que se instalan en el equipo.</span><span class="sxs-lookup"><span data-stu-id="651d5-110">**apps** - Copies Microsoft Teams apps that are installed in the team.</span></span> 
- <span data-ttu-id="651d5-111">**canales de** – copia la estructura de canal (pero no los mensajes en el canal).</span><span class="sxs-lookup"><span data-stu-id="651d5-111">**channels** – Copies the channel structure (but not the messages in the channel).</span></span>
- <span data-ttu-id="651d5-112">**miembros** : copias de los miembros y propietarios del grupo.</span><span class="sxs-lookup"><span data-stu-id="651d5-112">**members** – Copies the members and owners of the group.</span></span>
- <span data-ttu-id="651d5-113">**configuración** – copia toda la configuración en el equipo, junto con la configuración de grupo de claves.</span><span class="sxs-lookup"><span data-stu-id="651d5-113">**settings** – Copies all settings within the team, along with key group settings.</span></span>
- <span data-ttu-id="651d5-114">**las fichas** – copias de las fichas dentro de los canales.</span><span class="sxs-lookup"><span data-stu-id="651d5-114">**tabs** – Copies the tabs within channels.</span></span>

<span data-ttu-id="651d5-115">Cuando se clonarán las fichas, se ponen en un estado no configurado: se muestran en la barra de pestañas en Microsoft Teams, y la primera vez que se abren, se le dirigirá a través de la pantalla de configuración.</span><span class="sxs-lookup"><span data-stu-id="651d5-115">When tabs are cloned, they are put into an unconfigured state -- they are displayed on the tab bar in Microsoft Teams, and the first time you open them, you'll go through the configuration screen.</span></span> <span data-ttu-id="651d5-116">(Si la persona que abre la ficha no tiene permiso para configurar aplicaciones, verán un mensaje que explica que no se ha configurado la ficha.)</span><span class="sxs-lookup"><span data-stu-id="651d5-116">(If the person opening the tab does not have permission to configure apps, they will see a message explaining that the tab hasn't been configured.)</span></span>

<span data-ttu-id="651d5-117">La clonación es una operación de larga duración.</span><span class="sxs-lookup"><span data-stu-id="651d5-117">Cloning is a long-running operation.</span></span>
<span data-ttu-id="651d5-118">Después de que se devuelve el clon POST, debe obtener la [operación](../resources/teamsasyncoperation.md) para ver si es "que se está ejecutando" o "correcto" o "error".</span><span class="sxs-lookup"><span data-stu-id="651d5-118">After the POST clone returns, you need to GET the [operation](../resources/teamsasyncoperation.md) to see if it's "running" or "succeeded" or "failed".</span></span> <span data-ttu-id="651d5-119">Se debe seguir GET hasta que el estado es no "en ejecución".</span><span class="sxs-lookup"><span data-stu-id="651d5-119">You should continue to GET until the status is not "running".</span></span> <span data-ttu-id="651d5-120">El retraso entre obtiene recomendado es de 5 segundos.</span><span class="sxs-lookup"><span data-stu-id="651d5-120">The recommended delay between GETs is 5 seconds.</span></span>

## <a name="permissions"></a><span data-ttu-id="651d5-121">Permisos</span><span class="sxs-lookup"><span data-stu-id="651d5-121">Permissions</span></span>

<span data-ttu-id="651d5-p106">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="651d5-p106">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="651d5-124">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="651d5-124">Permission type</span></span>      | <span data-ttu-id="651d5-125">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="651d5-125">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="651d5-126">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="651d5-126">Delegated (work or school account)</span></span>     | <span data-ttu-id="651d5-127">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="651d5-127">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="651d5-128">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="651d5-128">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="651d5-129">No admitida.</span><span class="sxs-lookup"><span data-stu-id="651d5-129">Not supported.</span></span>    |
|<span data-ttu-id="651d5-130">Aplicación</span><span class="sxs-lookup"><span data-stu-id="651d5-130">Application</span></span>                            | <span data-ttu-id="651d5-131">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="651d5-131">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="651d5-132">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="651d5-132">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/clone
```

## <a name="request-headers"></a><span data-ttu-id="651d5-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="651d5-133">Request headers</span></span>
| <span data-ttu-id="651d5-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="651d5-134">Header</span></span>       | <span data-ttu-id="651d5-135">Valor</span><span class="sxs-lookup"><span data-stu-id="651d5-135">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="651d5-136">Authorization</span><span class="sxs-lookup"><span data-stu-id="651d5-136">Authorization</span></span>  | <span data-ttu-id="651d5-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="651d5-p107">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="651d5-139">Content-Type</span><span class="sxs-lookup"><span data-stu-id="651d5-139">Content-Type</span></span>  | <span data-ttu-id="651d5-140">application/json</span><span class="sxs-lookup"><span data-stu-id="651d5-140">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="651d5-141">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="651d5-141">Request body</span></span>

| <span data-ttu-id="651d5-142">Propiedad</span><span class="sxs-lookup"><span data-stu-id="651d5-142">Property</span></span>     | <span data-ttu-id="651d5-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="651d5-143">Type</span></span>   |<span data-ttu-id="651d5-144">Description</span><span class="sxs-lookup"><span data-stu-id="651d5-144">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="651d5-145">classification</span><span class="sxs-lookup"><span data-stu-id="651d5-145">classification</span></span>|<span data-ttu-id="651d5-146">Cadena (opcional)</span><span class="sxs-lookup"><span data-stu-id="651d5-146">String (optional)</span></span>|<span data-ttu-id="651d5-147">Describe una clasificación para el grupo (por ejemplo, el impacto de negocio bajo, medio o alto).</span><span class="sxs-lookup"><span data-stu-id="651d5-147">Describes a classification for the group (such as low, medium or high business impact).</span></span> <span data-ttu-id="651d5-148">Los valores válidos para esta propiedad se definen mediante la creación de un valor de [configuración](../resources/directorysetting.md) ClassificationList, basado en la [definición de plantilla](../resources/directorysettingtemplate.md).</span><span class="sxs-lookup"><span data-stu-id="651d5-148">Valid values for this property are defined by creating a ClassificationList [setting](../resources/directorysetting.md) value, based on the [template definition](../resources/directorysettingtemplate.md).</span></span> <span data-ttu-id="651d5-149">Si no se especifica la clasificación, la clasificación se copiarán desde el equipo original o grupo.</span><span class="sxs-lookup"><span data-stu-id="651d5-149">If classification is not specified, the classification will be copied from the original team/group.</span></span>|
|<span data-ttu-id="651d5-150">descripción</span><span class="sxs-lookup"><span data-stu-id="651d5-150">description</span></span>|<span data-ttu-id="651d5-151">Cadena (opcional)</span><span class="sxs-lookup"><span data-stu-id="651d5-151">String (optional)</span></span>|<span data-ttu-id="651d5-152">Una descripción opcional del grupo.</span><span class="sxs-lookup"><span data-stu-id="651d5-152">An optional description for the group.</span></span> <span data-ttu-id="651d5-153">Si no se especifica esta propiedad, se va a dejar en blanco.</span><span class="sxs-lookup"><span data-stu-id="651d5-153">If this property is not specified, it will be left blank.</span></span>|
|<span data-ttu-id="651d5-154">displayName</span><span class="sxs-lookup"><span data-stu-id="651d5-154">displayName</span></span>|<span data-ttu-id="651d5-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="651d5-155">String</span></span>|<span data-ttu-id="651d5-p110">El nombre para mostrar del grupo. Esta propiedad es necesaria cuando se crea un grupo y no se puede borrar durante las actualizaciones. Es compatible con $filter y $orderby.</span><span class="sxs-lookup"><span data-stu-id="651d5-p110">The display name for the group. This property is required when a group is created and it cannot be cleared during updates. Supports $filter and $orderby.</span></span>|
|<span data-ttu-id="651d5-159">mailNickname</span><span class="sxs-lookup"><span data-stu-id="651d5-159">mailNickname</span></span>|<span data-ttu-id="651d5-160">Cadena</span><span class="sxs-lookup"><span data-stu-id="651d5-160">String</span></span>|<span data-ttu-id="651d5-161">El alias de correo para el grupo, único en la organización.</span><span class="sxs-lookup"><span data-stu-id="651d5-161">The mail alias for the group, unique in the organization.</span></span> <span data-ttu-id="651d5-162">Esta propiedad debe especificarse cuando se crea un grupo.</span><span class="sxs-lookup"><span data-stu-id="651d5-162">This property must be specified when a group is created.</span></span> <span data-ttu-id="651d5-163">Es compatible con $filter.</span><span class="sxs-lookup"><span data-stu-id="651d5-163">Supports $filter.</span></span> <span data-ttu-id="651d5-164">Si no se especifica esta propiedad, se calculará de la propiedad displayName.</span><span class="sxs-lookup"><span data-stu-id="651d5-164">If this property is not specified, it will be computed from the displayName.</span></span> <span data-ttu-id="651d5-165">Problema conocido: esta propiedad se omite actualmente.</span><span class="sxs-lookup"><span data-stu-id="651d5-165">Known issue: this property is currently ignored.</span></span>|
|<span data-ttu-id="651d5-166">partsToClone</span><span class="sxs-lookup"><span data-stu-id="651d5-166">partsToClone</span></span>| [<span data-ttu-id="651d5-167">clonableTeamParts</span><span class="sxs-lookup"><span data-stu-id="651d5-167">clonableTeamParts</span></span>](../resources/clonableteamparts.md) |<span data-ttu-id="651d5-168">Una lista separados por comas de los elementos que se debe clonar.</span><span class="sxs-lookup"><span data-stu-id="651d5-168">A comma-seperated list of the parts to clone.</span></span> <span data-ttu-id="651d5-169">Los elementos legales son "aplicaciones, las fichas, configuración, canales, los miembros".</span><span class="sxs-lookup"><span data-stu-id="651d5-169">Legal parts are "apps, tabs, settings, channels, members".</span></span>|
|<span data-ttu-id="651d5-170">visibility</span><span class="sxs-lookup"><span data-stu-id="651d5-170">visibility</span></span>|<span data-ttu-id="651d5-171">[teamVisibilityType](../resources/teamvisibilitytype.md) (opcional)</span><span class="sxs-lookup"><span data-stu-id="651d5-171">[teamVisibilityType](../resources/teamvisibilitytype.md) (optional)</span></span>| <span data-ttu-id="651d5-172">Especifica la visibilidad del grupo.</span><span class="sxs-lookup"><span data-stu-id="651d5-172">Specifies the visibility of the group.</span></span> <span data-ttu-id="651d5-173">Los valores posibles son: **privada**, **pública**.</span><span class="sxs-lookup"><span data-stu-id="651d5-173">Possible values are: **Private**, **Public**.</span></span> <span data-ttu-id="651d5-174">Si no se especifica la visibilidad, la visibilidad se copiarán desde el equipo original o grupo.</span><span class="sxs-lookup"><span data-stu-id="651d5-174">If visibility is not specified, the visibility will be copied from the original team/group.</span></span> <span data-ttu-id="651d5-175">Si el equipo que se está clonando es un equipo de **educationClass** , se omite el parámetro visibilidad y visibilidad del nuevo grupo se establecerá en HiddenMembership.</span><span class="sxs-lookup"><span data-stu-id="651d5-175">If the team being cloned is an **educationClass** team, the visibility parameter is ignored, and the new group's visibility will be set to HiddenMembership.</span></span>|

## <a name="response"></a><span data-ttu-id="651d5-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="651d5-176">Response</span></span>

<span data-ttu-id="651d5-177">Si tiene éxito, este método devolverá un `202 Accepted` código de respuesta con una ubicación: encabezado que señala hacia el recurso de la [operación](../resources/teamsasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="651d5-177">If successful, this method will return a `202 Accepted` response code with a Location: header pointing to the [operation](../resources/teamsasyncoperation.md) resource.</span></span>
<span data-ttu-id="651d5-178">Una vez finalizada la operación, el recurso de la operación le indicará el identificador del equipo de creada.</span><span class="sxs-lookup"><span data-stu-id="651d5-178">When the operation is complete, the operation resource will tell you the id of the created team.</span></span>

## <a name="example"></a><span data-ttu-id="651d5-179">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="651d5-179">Example</span></span>
#### <a name="request"></a><span data-ttu-id="651d5-180">Solicitud</span><span class="sxs-lookup"><span data-stu-id="651d5-180">Request</span></span>
<span data-ttu-id="651d5-181">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="651d5-181">The following is an example of the request.</span></span>
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

#### <a name="response"></a><span data-ttu-id="651d5-182">Respuesta</span><span class="sxs-lookup"><span data-stu-id="651d5-182">Response</span></span>
<span data-ttu-id="651d5-183">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="651d5-183">The following is an example of the response.</span></span> <span data-ttu-id="651d5-184">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="651d5-184">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="651d5-185">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="651d5-185">All of the properties will be returned from an actual call.</span></span>
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

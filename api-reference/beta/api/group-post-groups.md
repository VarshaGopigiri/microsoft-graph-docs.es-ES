---
title: Crear grupo
description: 'Use esta API para crear un grupo como se especifica en el cuerpo de la solicitud. Puede crear uno de los tres tipos de grupos:'
author: dkershaw10
ms.openlocfilehash: 1c77b3a33b19e9f0254642ef89e3d7fddc224b9a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27320772"
---
# <a name="create-group"></a><span data-ttu-id="aac34-104">Crear grupo</span><span class="sxs-lookup"><span data-stu-id="aac34-104">Create group</span></span>

> <span data-ttu-id="aac34-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="aac34-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="aac34-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="aac34-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="aac34-107">Utilice esta API para crear un nuevo [grupo](../resources/group.md) , tal como se especifica en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="aac34-107">Use this API to create a new [group](../resources/group.md) as specified in the request body.</span></span> <span data-ttu-id="aac34-108">Puede crear uno de los tres tipos de grupos:</span><span class="sxs-lookup"><span data-stu-id="aac34-108">You can create one of three types of groups:</span></span>

* <span data-ttu-id="aac34-109">Grupo de Office 365 (grupo unificado)</span><span class="sxs-lookup"><span data-stu-id="aac34-109">Office 365 Group (unified group)</span></span>
* <span data-ttu-id="aac34-110">Grupo dinámico</span><span class="sxs-lookup"><span data-stu-id="aac34-110">Dynamic group</span></span>
* <span data-ttu-id="aac34-111">Grupo de seguridad</span><span class="sxs-lookup"><span data-stu-id="aac34-111">Security group</span></span>

> <span data-ttu-id="aac34-112">**Nota**: para crear un [equipo](../resources/team.md), primero cree un grupo, a continuación, agregar un equipo a ella, vea [Crear equipo](../api/team-put-teams.md).</span><span class="sxs-lookup"><span data-stu-id="aac34-112">**Note**: To create a [team](../resources/team.md), first create a group then add a team to it, see [create team](../api/team-put-teams.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="aac34-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="aac34-113">Permissions</span></span>
<span data-ttu-id="aac34-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="aac34-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="aac34-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="aac34-116">Permission type</span></span>      | <span data-ttu-id="aac34-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="aac34-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="aac34-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="aac34-118">Delegated (work or school account)</span></span> | <span data-ttu-id="aac34-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="aac34-119">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="aac34-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="aac34-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="aac34-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aac34-121">Not supported.</span></span>    |
|<span data-ttu-id="aac34-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="aac34-122">Application</span></span> | <span data-ttu-id="aac34-123">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="aac34-123">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="aac34-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aac34-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups
```

## <a name="request-headers"></a><span data-ttu-id="aac34-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="aac34-125">Request headers</span></span>
| <span data-ttu-id="aac34-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="aac34-126">Name</span></span>       | <span data-ttu-id="aac34-127">Type</span><span class="sxs-lookup"><span data-stu-id="aac34-127">Type</span></span> | <span data-ttu-id="aac34-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="aac34-128">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="aac34-129">Autorización</span><span class="sxs-lookup"><span data-stu-id="aac34-129">Authorization</span></span>  | <span data-ttu-id="aac34-130">string</span><span class="sxs-lookup"><span data-stu-id="aac34-130">string</span></span>  | <span data-ttu-id="aac34-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aac34-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="aac34-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="aac34-133">Request body</span></span>
<span data-ttu-id="aac34-134">En la siguiente tabla se muestra las propiedades del recurso de [grupo](../resources/group.md) para especificar cuando se crea un grupo.</span><span class="sxs-lookup"><span data-stu-id="aac34-134">The following table shows the properties of the [group](../resources/group.md) resource to specify when you create a group.</span></span> 

| <span data-ttu-id="aac34-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aac34-135">Property</span></span> | <span data-ttu-id="aac34-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="aac34-136">Type</span></span> | <span data-ttu-id="aac34-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="aac34-137">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="aac34-138">displayName</span><span class="sxs-lookup"><span data-stu-id="aac34-138">displayName</span></span> | <span data-ttu-id="aac34-139">string</span><span class="sxs-lookup"><span data-stu-id="aac34-139">string</span></span> | <span data-ttu-id="aac34-140">El nombre para mostrar en la libreta de direcciones del grupo.</span><span class="sxs-lookup"><span data-stu-id="aac34-140">The name to display in the address book for the group.</span></span> <span data-ttu-id="aac34-141">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aac34-141">Required.</span></span> |
| <span data-ttu-id="aac34-142">mailEnabled</span><span class="sxs-lookup"><span data-stu-id="aac34-142">mailEnabled</span></span> | <span data-ttu-id="aac34-143">boolean</span><span class="sxs-lookup"><span data-stu-id="aac34-143">boolean</span></span> | <span data-ttu-id="aac34-144">Establézcalo en **true** para grupos habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="aac34-144">Set to **true** for mail-enabled groups.</span></span> <span data-ttu-id="aac34-145">Debe establecer en **true** si la creación de un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="aac34-145">Set this to **true** if creating an Office 365 Group.</span></span> <span data-ttu-id="aac34-146">Debe establecer en **false** si crear dinámico o grupo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="aac34-146">Set this to **false** if creating dynamic or security group.</span></span> <span data-ttu-id="aac34-147">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aac34-147">Required.</span></span> |
| <span data-ttu-id="aac34-148">mailNickname</span><span class="sxs-lookup"><span data-stu-id="aac34-148">mailNickname</span></span> | <span data-ttu-id="aac34-149">string</span><span class="sxs-lookup"><span data-stu-id="aac34-149">string</span></span> | <span data-ttu-id="aac34-150">El alias de correo del grupo.</span><span class="sxs-lookup"><span data-stu-id="aac34-150">The mail alias for the group.</span></span> <span data-ttu-id="aac34-151">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aac34-151">Required.</span></span> |
| <span data-ttu-id="aac34-152">securityEnabled</span><span class="sxs-lookup"><span data-stu-id="aac34-152">securityEnabled</span></span> | <span data-ttu-id="aac34-153">boolean</span><span class="sxs-lookup"><span data-stu-id="aac34-153">boolean</span></span> | <span data-ttu-id="aac34-154">Establecer en **true** para grupos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="aac34-154">Set to **true** for security-enabled groups.</span></span> <span data-ttu-id="aac34-155">Debe establecer en **true** si la creación de un grupo de seguridad o dinámicos.</span><span class="sxs-lookup"><span data-stu-id="aac34-155">Set this to **true** if creating a dynamic or security group.</span></span> <span data-ttu-id="aac34-156">Debe establecer en **false** si la creación de un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="aac34-156">Set this to **false** if creating an Office 365 Group.</span></span> <span data-ttu-id="aac34-157">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aac34-157">Required.</span></span> |
| <span data-ttu-id="aac34-158">owners</span><span class="sxs-lookup"><span data-stu-id="aac34-158">owners</span></span> | <span data-ttu-id="aac34-159">colección string</span><span class="sxs-lookup"><span data-stu-id="aac34-159">string collection</span></span> | <span data-ttu-id="aac34-160">Esta propiedad representa los propietarios para el grupo en tiempo de creación.</span><span class="sxs-lookup"><span data-stu-id="aac34-160">This property represents the owners for the group at creation time.</span></span> <span data-ttu-id="aac34-161">Opcional.</span><span class="sxs-lookup"><span data-stu-id="aac34-161">Optional.</span></span> |
| <span data-ttu-id="aac34-162">members</span><span class="sxs-lookup"><span data-stu-id="aac34-162">members</span></span> | <span data-ttu-id="aac34-163">colección string</span><span class="sxs-lookup"><span data-stu-id="aac34-163">string collection</span></span> | <span data-ttu-id="aac34-164">Esta propiedad representa a los miembros para el grupo en tiempo de creación.</span><span class="sxs-lookup"><span data-stu-id="aac34-164">This property represents the members for the group at creation time.</span></span> <span data-ttu-id="aac34-165">Opcional.</span><span class="sxs-lookup"><span data-stu-id="aac34-165">Optional.</span></span> |

<span data-ttu-id="aac34-166">Especificar la propiedad **groupTypes** si está creando un grupo de Office 365 o dinámico, como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="aac34-166">Specify the **groupTypes** property if you're creating an Office 365 or dynamic group, as stated below.</span></span>

| <span data-ttu-id="aac34-167">Tipo de grupo</span><span class="sxs-lookup"><span data-stu-id="aac34-167">Type of group</span></span> | <span data-ttu-id="aac34-168">Propiedad **groupTypes**</span><span class="sxs-lookup"><span data-stu-id="aac34-168">**groupTypes** property</span></span> |
|:--------------|:------------------------|
| <span data-ttu-id="aac34-169">Office 365 (también conocido como grupo unificado)</span><span class="sxs-lookup"><span data-stu-id="aac34-169">Office 365 (aka unified group)</span></span>| <span data-ttu-id="aac34-170">"Unificado"</span><span class="sxs-lookup"><span data-stu-id="aac34-170">"Unified"</span></span> |
| <span data-ttu-id="aac34-171">Dinámico</span><span class="sxs-lookup"><span data-stu-id="aac34-171">Dynamic</span></span> | <span data-ttu-id="aac34-172">"DynamicMembership"</span><span class="sxs-lookup"><span data-stu-id="aac34-172">"DynamicMembership"</span></span> |
| <span data-ttu-id="aac34-173">Seguridad</span><span class="sxs-lookup"><span data-stu-id="aac34-173">Security</span></span> | <span data-ttu-id="aac34-174">Sin establecer.</span><span class="sxs-lookup"><span data-stu-id="aac34-174">Do not set.</span></span> |

<span data-ttu-id="aac34-175">Puesto que el recurso de **grupo** admite [extensiones](/graph/extensibility-overview), puede usar el `POST` operación y agregar propiedades personalizadas con sus propios datos al grupo al crearla.</span><span class="sxs-lookup"><span data-stu-id="aac34-175">Since the **group** resource supports [extensions](/graph/extensibility-overview), you can use the `POST` operation and add custom properties with your own data to the group while creating it.</span></span>

><span data-ttu-id="aac34-176">**Nota:** Creación de un grupo de Office 365 mediante programación sin un contexto de usuario y sin especificar los propietarios va a crear el grupo de forma anónima.</span><span class="sxs-lookup"><span data-stu-id="aac34-176">**Note:** Creating an Office 365 Group programmatically without a user context and  without specifying owners will create the group anonymously.</span></span>  <span data-ttu-id="aac34-177">Al hacerlo, se puede producir en el sitio de SharePoint Online asociado, no se crean automáticamente hasta que más se lleva a cabo la acción manual.</span><span class="sxs-lookup"><span data-stu-id="aac34-177">Doing so can result in the associated SharePoint Online site not being created automatically until further manual action is taken.</span></span>  

<span data-ttu-id="aac34-p113">Especifique otras propiedades modificables según sea necesario para su grupo. Para más información, vea las propiedades del recurso [grupo](../resources/group.md).</span><span class="sxs-lookup"><span data-stu-id="aac34-p113">Specify other writable properties as necessary for your group. For more information, see the properties of the [group](../resources/group.md) resource.</span></span>

## <a name="response"></a><span data-ttu-id="aac34-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aac34-180">Response</span></span>
<span data-ttu-id="aac34-181">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aac34-181">If successful, this method returns `201 Created` response code and [group](../resources/group.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="aac34-182">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aac34-182">Example</span></span>
#### <a name="request-1"></a><span data-ttu-id="aac34-183">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="aac34-183">Request 1</span></span>
<span data-ttu-id="aac34-184">La primera solicitud en el ejemplo crea un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="aac34-184">The first example request creates an Office 365 Group.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_group"
}-->
```http
POST https://graph.microsoft.com/beta/groups
Content-type: application/json
Content-length: 244

{
  "description": "Self help community for library",
  "displayName": "Library Assist",
  "groupTypes": [
    "Unified"
  ],
  "mailEnabled": true,
  "mailNickname": "library",
  "securityEnabled": false
}
```

#### <a name="response"></a><span data-ttu-id="aac34-185">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aac34-185">Response</span></span>
<span data-ttu-id="aac34-186">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aac34-186">The following is an example of the response.</span></span>
><span data-ttu-id="aac34-187">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="aac34-187">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="aac34-188">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aac34-188">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 244

{
  "description": "Self help community for library",
  "displayName": "Library Assist",
  "groupTypes": [
    "Unified"
  ],
  "mail": "library@contoso.onmicrosoft.com",
  "mailEnabled": true,
  "mailNickname": "library",
  "securityEnabled": false
}
```

#### <a name="request-2"></a><span data-ttu-id="aac34-189">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="aac34-189">Request 2</span></span>
<span data-ttu-id="aac34-190">La segunda solicitud de ejemplo crea un grupo de Office 365 con los propietarios de especificado.</span><span class="sxs-lookup"><span data-stu-id="aac34-190">The second example request creates an Office 365 Group with owners specified.</span></span>
<!-- {
  "blockType": "request"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups
Content-Type: application/json
 {
  "description": "Group with owners",
  "displayName": "Group1",
  "groupTypes": [
    "Unified"
  ],
  "mailEnabled": true,
  "mailNickname": "group1",
  "securityEnabled": false,
  "owners@odata.bind": [
    "https://graph.microsoft.com/v1.0/users/26be1845-4119-4801-a799-aea79d09f1a2"
  ]
}
```

 #### <a name="response-2"></a><span data-ttu-id="aac34-191">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="aac34-191">Response 2</span></span>
<span data-ttu-id="aac34-192">El siguiente es un ejemplo de la respuesta correcta.</span><span class="sxs-lookup"><span data-stu-id="aac34-192">The following is an example of the successful response.</span></span>
><span data-ttu-id="aac34-p115">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aac34-p115">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
 {
    "description": "Group with owners",
    "displayName": "Group1",
    "groupTypes": [
        "Unified"
    ],
    "mail": "group1@contoso.onmicrosoft.com",
    "mailEnabled": true,
    "mailNickname": "group1",
    "securityEnabled": false
}
```

## <a name="see-also"></a><span data-ttu-id="aac34-195">Vea también</span><span class="sxs-lookup"><span data-stu-id="aac34-195">See also</span></span>

- [<span data-ttu-id="aac34-196">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="aac34-196">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="aac34-197">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="aac34-197">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="aac34-198">Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="aac34-198">Add custom data to groups using schema extensions (preview)</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

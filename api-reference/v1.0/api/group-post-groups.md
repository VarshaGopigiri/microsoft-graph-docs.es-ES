---
title: Crear grupo
description: 'Use esta API para crear un grupo como se especifica en el cuerpo de la solicitud. Puede crear uno de los tres tipos de grupos:'
author: dkershaw10
ms.openlocfilehash: 2fff86d3bc86a8e78c295b1a4553006ac416ddd1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27322963"
---
# <a name="create-group"></a><span data-ttu-id="7c890-104">Crear grupo</span><span class="sxs-lookup"><span data-stu-id="7c890-104">Create group</span></span>
<span data-ttu-id="7c890-p102">Use esta API para crear un grupo como se especifica en el cuerpo de la solicitud. Puede crear uno de los tres tipos de grupos:</span><span class="sxs-lookup"><span data-stu-id="7c890-p102">Use this API to create a new group as specified in the request body. You can create one of three types of groups:</span></span>

* <span data-ttu-id="7c890-107">Grupo de Office 365 (grupo unificado)</span><span class="sxs-lookup"><span data-stu-id="7c890-107">Office 365 Group (unified group)</span></span>
* <span data-ttu-id="7c890-108">Grupo dinámico</span><span class="sxs-lookup"><span data-stu-id="7c890-108">Dynamic group</span></span>
* <span data-ttu-id="7c890-109">Grupo de seguridad</span><span class="sxs-lookup"><span data-stu-id="7c890-109">Security group</span></span>

> <span data-ttu-id="7c890-p103">**Nota**: Aunque Microsoft Teams se basa en Grupos de Office 365, actualmente no puede crear un equipo mediante esta API. Puede usar las otras API de grupo para administrar un equipo que se ha creado en la interfaz de usuario de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7c890-p103">**Note**: Although Microsoft Teams is built on Office 365 Groups, you can't currently create a team via this API. You can use the other group APIs to manage a team that has been created in the Microsoft Teams UI.</span></span>

## <a name="permissions"></a><span data-ttu-id="7c890-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="7c890-112">Permissions</span></span>
<span data-ttu-id="7c890-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7c890-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7c890-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7c890-115">Permission type</span></span>      | <span data-ttu-id="7c890-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7c890-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7c890-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7c890-117">Delegated (work or school account)</span></span> | <span data-ttu-id="7c890-118">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7c890-118">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="7c890-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7c890-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7c890-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7c890-120">Not supported.</span></span>    |
|<span data-ttu-id="7c890-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7c890-121">Application</span></span> | <span data-ttu-id="7c890-122">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7c890-122">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7c890-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7c890-123">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups
```

## <a name="request-headers"></a><span data-ttu-id="7c890-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7c890-124">Request headers</span></span>
| <span data-ttu-id="7c890-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="7c890-125">Name</span></span>       | <span data-ttu-id="7c890-126">Type</span><span class="sxs-lookup"><span data-stu-id="7c890-126">Type</span></span> | <span data-ttu-id="7c890-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c890-127">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="7c890-128">Autorización</span><span class="sxs-lookup"><span data-stu-id="7c890-128">Authorization</span></span>  | <span data-ttu-id="7c890-129">string</span><span class="sxs-lookup"><span data-stu-id="7c890-129">string</span></span>  | <span data-ttu-id="7c890-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7c890-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7c890-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7c890-132">Request body</span></span>
<span data-ttu-id="7c890-133">En la siguiente tabla se muestra las propiedades del recurso de [grupo](../resources/group.md) para especificar cuando se crea un grupo.</span><span class="sxs-lookup"><span data-stu-id="7c890-133">The following table shows the properties of the [group](../resources/group.md) resource to specify when you create a group.</span></span> 

| <span data-ttu-id="7c890-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7c890-134">Property</span></span> | <span data-ttu-id="7c890-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c890-135">Type</span></span> | <span data-ttu-id="7c890-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c890-136">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="7c890-137">displayName</span><span class="sxs-lookup"><span data-stu-id="7c890-137">displayName</span></span> | <span data-ttu-id="7c890-138">string</span><span class="sxs-lookup"><span data-stu-id="7c890-138">string</span></span> | <span data-ttu-id="7c890-139">El nombre para mostrar en la libreta de direcciones del grupo.</span><span class="sxs-lookup"><span data-stu-id="7c890-139">The name to display in the address book for the group.</span></span> <span data-ttu-id="7c890-140">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7c890-140">Required.</span></span> |
| <span data-ttu-id="7c890-141">mailEnabled</span><span class="sxs-lookup"><span data-stu-id="7c890-141">mailEnabled</span></span> | <span data-ttu-id="7c890-142">boolean</span><span class="sxs-lookup"><span data-stu-id="7c890-142">boolean</span></span> | <span data-ttu-id="7c890-143">Establézcalo en **true** para grupos habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="7c890-143">Set to **true** for mail-enabled groups.</span></span> <span data-ttu-id="7c890-144">Debe establecer en **true** si la creación de un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="7c890-144">Set this to **true** if creating an Office 365 Group.</span></span> <span data-ttu-id="7c890-145">Debe establecer en **false** si crear dinámico o grupo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7c890-145">Set this to **false** if creating dynamic or security group.</span></span> <span data-ttu-id="7c890-146">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7c890-146">Required.</span></span> |
| <span data-ttu-id="7c890-147">mailNickname</span><span class="sxs-lookup"><span data-stu-id="7c890-147">mailNickname</span></span> | <span data-ttu-id="7c890-148">string</span><span class="sxs-lookup"><span data-stu-id="7c890-148">string</span></span> | <span data-ttu-id="7c890-149">El alias de correo del grupo.</span><span class="sxs-lookup"><span data-stu-id="7c890-149">The mail alias for the group.</span></span> <span data-ttu-id="7c890-150">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7c890-150">Required.</span></span> |
| <span data-ttu-id="7c890-151">securityEnabled</span><span class="sxs-lookup"><span data-stu-id="7c890-151">securityEnabled</span></span> | <span data-ttu-id="7c890-152">boolean</span><span class="sxs-lookup"><span data-stu-id="7c890-152">boolean</span></span> | <span data-ttu-id="7c890-153">Establecer en **true** para grupos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7c890-153">Set to **true** for security-enabled groups.</span></span> <span data-ttu-id="7c890-154">Debe establecer en **true** si la creación de un grupo de seguridad o dinámicos.</span><span class="sxs-lookup"><span data-stu-id="7c890-154">Set this to **true** if creating a dynamic or security group.</span></span> <span data-ttu-id="7c890-155">Debe establecer en **false** si la creación de un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="7c890-155">Set this to **false** if creating an Office 365 group.</span></span> <span data-ttu-id="7c890-156">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7c890-156">Required.</span></span> |
| <span data-ttu-id="7c890-157">owners</span><span class="sxs-lookup"><span data-stu-id="7c890-157">owners</span></span> | <span data-ttu-id="7c890-158">colección string</span><span class="sxs-lookup"><span data-stu-id="7c890-158">string collection</span></span> | <span data-ttu-id="7c890-159">Esta propiedad representa los propietarios para el grupo en tiempo de creación.</span><span class="sxs-lookup"><span data-stu-id="7c890-159">This property represents the owners for the group at creation time.</span></span> <span data-ttu-id="7c890-160">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7c890-160">Optional.</span></span> |
| <span data-ttu-id="7c890-161">members</span><span class="sxs-lookup"><span data-stu-id="7c890-161">members</span></span> | <span data-ttu-id="7c890-162">colección string</span><span class="sxs-lookup"><span data-stu-id="7c890-162">string collection</span></span> | <span data-ttu-id="7c890-163">Esta propiedad representa a los miembros para el grupo en tiempo de creación.</span><span class="sxs-lookup"><span data-stu-id="7c890-163">This property represents the members for the group at creation time.</span></span> <span data-ttu-id="7c890-164">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7c890-164">Optional.</span></span> |


<span data-ttu-id="7c890-165">Especificar la propiedad **groupTypes** si está creando un grupo de Office 365 o dinámico, como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="7c890-165">Specify the **groupTypes** property if you're creating an Office 365 or dynamic group, as stated below.</span></span>

### <a name="grouptypes-options"></a><span data-ttu-id="7c890-166">Opciones de groupTypes</span><span class="sxs-lookup"><span data-stu-id="7c890-166">groupTypes options</span></span>

| <span data-ttu-id="7c890-167">Tipo de grupo</span><span class="sxs-lookup"><span data-stu-id="7c890-167">Type of group</span></span> | <span data-ttu-id="7c890-168">Propiedad **groupTypes**</span><span class="sxs-lookup"><span data-stu-id="7c890-168">**groupTypes** property</span></span> |
|:--------------|:------------------------|
| <span data-ttu-id="7c890-169">Office 365 (también conocido como grupo unificado)</span><span class="sxs-lookup"><span data-stu-id="7c890-169">Office 365 (aka unified group)</span></span>| <span data-ttu-id="7c890-170">"Unificado"</span><span class="sxs-lookup"><span data-stu-id="7c890-170">"Unified"</span></span> |
| <span data-ttu-id="7c890-171">Dinámico</span><span class="sxs-lookup"><span data-stu-id="7c890-171">Dynamic</span></span> | <span data-ttu-id="7c890-172">"DynamicMembership"</span><span class="sxs-lookup"><span data-stu-id="7c890-172">"DynamicMembership"</span></span> |
| <span data-ttu-id="7c890-173">Seguridad</span><span class="sxs-lookup"><span data-stu-id="7c890-173">Security</span></span> | <span data-ttu-id="7c890-174">Sin establecer.</span><span class="sxs-lookup"><span data-stu-id="7c890-174">Do not set.</span></span> |


><span data-ttu-id="7c890-175">**Nota:** creación de un grupo de Office 365 mediante programación sin un contexto de usuario y sin especificar propietarios va a crear el grupo de forma anónima.</span><span class="sxs-lookup"><span data-stu-id="7c890-175">**Note:** Creating an Office 365 Group programmatically without a user context and  without specifying owners will create the group anonymously.</span></span>  <span data-ttu-id="7c890-176">Al hacerlo, se puede producir en el sitio de SharePoint Online asociado, no se crean automáticamente hasta que más se lleva a cabo la acción manual.</span><span class="sxs-lookup"><span data-stu-id="7c890-176">Doing so can result in the associated SharePoint Online site not being created automatically until further manual action is taken.</span></span>  

<span data-ttu-id="7c890-p113">Especifique otras propiedades modificables según sea necesario para su grupo. Para más información, vea las propiedades del recurso [grupo](../resources/group.md).</span><span class="sxs-lookup"><span data-stu-id="7c890-p113">Specify other writable properties as necessary for your group. For more information, see the properties of the [group](../resources/group.md) resource.</span></span>

## <a name="response"></a><span data-ttu-id="7c890-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7c890-179">Response</span></span>
<span data-ttu-id="7c890-180">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7c890-180">If successful, this method returns `201 Created` response code and [group](../resources/group.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7c890-181">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7c890-181">Example</span></span>
#### <a name="request-1"></a><span data-ttu-id="7c890-182">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="7c890-182">Request 1</span></span>
<span data-ttu-id="7c890-183">La primera solicitud en el ejemplo crea un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="7c890-183">The first example request creates an Office 365 Group.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups
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

#### <a name="response-1"></a><span data-ttu-id="7c890-184">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="7c890-184">Response 1</span></span>
<span data-ttu-id="7c890-185">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7c890-185">The following is an example of the response.</span></span>
><span data-ttu-id="7c890-186">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="7c890-186">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="7c890-187">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7c890-187">All the properties will be returned from an actual call.</span></span>
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

#### <a name="request-2"></a><span data-ttu-id="7c890-188">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="7c890-188">Request 2</span></span>
<span data-ttu-id="7c890-189">La segunda solicitud de ejemplo crea un grupo de Office 365 con los propietarios de especificado.</span><span class="sxs-lookup"><span data-stu-id="7c890-189">The second example request creates an Office 365 Group with owners specified.</span></span>
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

#### <a name="response-2"></a><span data-ttu-id="7c890-190">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="7c890-190">Response 2</span></span>
<span data-ttu-id="7c890-191">El siguiente es un ejemplo de la respuesta correcta.</span><span class="sxs-lookup"><span data-stu-id="7c890-191">The following is an example of the successful response.</span></span>
><span data-ttu-id="7c890-192">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="7c890-192">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="7c890-193">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7c890-193">All the properties will be returned from an actual call.</span></span>
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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

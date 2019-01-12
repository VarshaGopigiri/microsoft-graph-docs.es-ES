---
title: Trabajar con grupos en Microsoft Graph
description: Los grupos son colecciones de usuarios y otras entidades de seguridad que comparten el acceso a recursos de servicios de Microsoft o de la aplicación. Microsoft Graph proporciona API que se pueden usar para crear y administrar diversos tipos de grupos y funcionalidades de grupo según la situación. Todas las operaciones relacionadas con grupos de Microsoft Graph requieren permisos de administrador.
author: dkershaw10
localization_priority: Priority
ms.prod: groups
ms.openlocfilehash: 031d67db4f0ad151175fc244aefdfd31615b221c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27961690"
---
# <a name="working-with-groups-in-microsoft-graph"></a><span data-ttu-id="b6ea5-105">Trabajar con grupos en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="b6ea5-105">Working with groups in Microsoft Graph</span></span>

<span data-ttu-id="b6ea5-106">Los grupos son colecciones de [usuarios](user.md) y otras entidades de seguridad que comparten el acceso a recursos de servicios de Microsoft o de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-106">Groups are collections of [users](user.md) and other principals who share access to resources in Microsoft services or in your app.</span></span> <span data-ttu-id="b6ea5-107">Microsoft Graph proporciona API que se pueden usar para crear y administrar diversos tipos de grupos y funcionalidades de grupo según la situación.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-107">Microsoft Graph provides APIs that you can use to create and manage different types of groups and group functionality according to your scenario.</span></span> <span data-ttu-id="b6ea5-108">Todas las operaciones relacionadas con grupos de Microsoft Graph requieren permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-108">All group-related operations in Microsoft Graph require administrator consent.</span></span>

> <span data-ttu-id="b6ea5-109">**Nota**: Solo se pueden crear grupos mediante cuentas profesionales o educativas.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-109">**Note**: Groups can only be created through work or school accounts.</span></span> <span data-ttu-id="b6ea5-110">Las cuentas personales de Microsoft no admiten grupos.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-110">Personal Microsoft accounts don't support groups.</span></span>

| <span data-ttu-id="b6ea5-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6ea5-111">Type</span></span>              | <span data-ttu-id="b6ea5-112">Caso de uso</span><span class="sxs-lookup"><span data-stu-id="b6ea5-112">Use case</span></span> | <span data-ttu-id="b6ea5-113">groupType</span><span class="sxs-lookup"><span data-stu-id="b6ea5-113">groupType</span></span> | <span data-ttu-id="b6ea5-114">Con correo habilitado</span><span class="sxs-lookup"><span data-stu-id="b6ea5-114">mail-enabled</span></span> | <span data-ttu-id="b6ea5-115">Con seguridad habilitada</span><span class="sxs-lookup"><span data-stu-id="b6ea5-115">security-enabled</span></span> | <span data-ttu-id="b6ea5-116">¿Se puede crear mediante API?</span><span class="sxs-lookup"><span data-stu-id="b6ea5-116">Can be created via API?</span></span> |
|-------------------|----------|-----------|--------------|------------------|--------------------------------|
| [<span data-ttu-id="b6ea5-117">Grupos de Office 365</span><span class="sxs-lookup"><span data-stu-id="b6ea5-117">Office 365 groups</span></span>](#office-365-groups) | <span data-ttu-id="b6ea5-118">Facilitar la colaboración de usuarios con recursos compartidos en línea de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-118">Facilitating user collaboration with shared Microsoft online resources.</span></span> | `["Unified"]` | `true` | `false` | <span data-ttu-id="b6ea5-119">Sí</span><span class="sxs-lookup"><span data-stu-id="b6ea5-119">Yes</span></span> |
| [<span data-ttu-id="b6ea5-120">Grupos de seguridad</span><span class="sxs-lookup"><span data-stu-id="b6ea5-120">Security groups</span></span>](#security-groups-and-mail-enabled-security-groups) | <span data-ttu-id="b6ea5-121">Controlar el acceso de los usuarios a recursos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-121">Controlling user access to in-app resources.</span></span> | `[]` | `false` | `true` | <span data-ttu-id="b6ea5-122">Sí</span><span class="sxs-lookup"><span data-stu-id="b6ea5-122">Yes</span></span> |
| [<span data-ttu-id="b6ea5-123">Grupos de seguridad habilitados para correo</span><span class="sxs-lookup"><span data-stu-id="b6ea5-123">Mail-enabled security groups</span></span>](#security-groups-and-mail-enabled-security-groups) | <span data-ttu-id="b6ea5-124">Controlar el acceso de los usuarios a recursos de la aplicación, con un buzón de grupo compartido.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-124">Controlling user access to in-app resources, with a shared group mailbox.</span></span> | `[]` | `true` | `true` | <span data-ttu-id="b6ea5-125">No</span><span class="sxs-lookup"><span data-stu-id="b6ea5-125">No</span></span> |
| <span data-ttu-id="b6ea5-126">Grupos de distribución</span><span class="sxs-lookup"><span data-stu-id="b6ea5-126">Distribution groups</span></span> | <span data-ttu-id="b6ea5-127">Distribuir correo a los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-127">Distributing mail to the members of the group.</span></span> <span data-ttu-id="b6ea5-128">Se recomienda usar Grupos de Office 365 debido al variado conjunto de recursos que proporcionan.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-128">It is recommended to use Office 365 groups due to the richer set of resources it provides.</span></span> | `[]` | `true` | `false` | <span data-ttu-id="b6ea5-129">No</span><span class="sxs-lookup"><span data-stu-id="b6ea5-129">No</span></span> |

## <a name="office-365-groups"></a><span data-ttu-id="b6ea5-130">Grupos de Office 365</span><span class="sxs-lookup"><span data-stu-id="b6ea5-130">Office 365 groups</span></span>
<span data-ttu-id="b6ea5-131">La utilidad de Grupos de Office 365 reside en su naturaleza colaborativa, ideal para personas que trabajan juntas en un proyecto o equipo.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-131">The power of Office 365 groups is in its collaborative nature, perfect for people who work together on a project or a team.</span></span> <span data-ttu-id="b6ea5-132">Se crean con los recursos que comparten los miembros del grupo, incluidos los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b6ea5-132">They are created with resources that members of the group share, including:</span></span>

- <span data-ttu-id="b6ea5-133">Conversaciones de Outlook</span><span class="sxs-lookup"><span data-stu-id="b6ea5-133">Outlook conversations</span></span>
- <span data-ttu-id="b6ea5-134">Calendario de Outlook</span><span class="sxs-lookup"><span data-stu-id="b6ea5-134">Outlook calendar</span></span>
- <span data-ttu-id="b6ea5-135">Archivos de SharePoint</span><span class="sxs-lookup"><span data-stu-id="b6ea5-135">SharePoint files</span></span>
- <span data-ttu-id="b6ea5-136">Bloc de notas de OneNote</span><span class="sxs-lookup"><span data-stu-id="b6ea5-136">OneNote notebook</span></span>
- <span data-ttu-id="b6ea5-137">Sitio de grupo de SharePoint</span><span class="sxs-lookup"><span data-stu-id="b6ea5-137">SharePoint team site</span></span>
- <span data-ttu-id="b6ea5-138">Planes de Planner</span><span class="sxs-lookup"><span data-stu-id="b6ea5-138">Planner plans</span></span>
- <span data-ttu-id="b6ea5-139">Administración de dispositivos de Intune</span><span class="sxs-lookup"><span data-stu-id="b6ea5-139">Intune device management</span></span>

### <a name="group-in-outlook-example"></a><span data-ttu-id="b6ea5-140">Ejemplo de grupo de Outlook</span><span class="sxs-lookup"><span data-stu-id="b6ea5-140">Group in Outlook example</span></span>

<span data-ttu-id="b6ea5-141">Esta es una representación JSON de grupos en Outlook.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-141">The following is a JSON representation of groups in Outlook.</span></span> 

```http

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#groups/$entity",
    "id": "4c5ee71b-e6a5-4343-9e2c-4244bc7e0938",
    "deletedDateTime": null,
    "classification": "MBI",
    "createdDateTime": "2016-08-23T14:46:56Z",
    "description": "This is a group in Outlook",
    "displayName": "OutlookGroup101",
    "groupTypes": [
        "Unified"
    ],
    "mail": "outlookgroup101@service.microsoft.com",
    "mailEnabled": true,
    "mailNickname": "outlookgroup101",
    "preferredLanguage": null,
    "proxyAddresses": [
        "smtp:outlookgroup101@microsoft.onmicrosoft.com",
        "SMTP:outlookgroup101@service.microsoft.com"
    ],
    "securityEnabled": false,
    "theme": null,
    "visibility": "Public"
}
```
<span data-ttu-id="b6ea5-142">Para más información sobre Grupos de Office 365 y las experiencias de administrador, vea [Obtenga más información sobre los grupos de Office 365](https://support.office.com/en-us/article/Learn-about-Office-365-groups-b565caa1-5c40-40ef-9915-60fdb2d97fa2).</span><span class="sxs-lookup"><span data-stu-id="b6ea5-142">To learn more about Office 365 groups and the administrator experiences, see [Learn about Office 365 Groups](https://support.office.com/en-us/article/Learn-about-Office-365-groups-b565caa1-5c40-40ef-9915-60fdb2d97fa2).</span></span>

## <a name="security-groups-and-mail-enabled-security-groups"></a><span data-ttu-id="b6ea5-143">Grupos de seguridad y grupos de seguridad con correo habilitado</span><span class="sxs-lookup"><span data-stu-id="b6ea5-143">Security groups and mail-enabled security groups</span></span>

<span data-ttu-id="b6ea5-144">Los grupos de seguridad están diseñados para controlar el acceso de los usuarios a los recursos.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-144">Security groups are for controlling user access to resources.</span></span> <span data-ttu-id="b6ea5-145">Al comprobar si un usuario es miembro de un grupo de seguridad, la aplicación puede tomar decisiones de autorización cuando el usuario intenta obtener acceso a algunos recursos seguros de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-145">By checking whether a user is a member of a security group, your app can make authorization decisions when that user is trying to access some secure resources in your app.</span></span> <span data-ttu-id="b6ea5-146">Los grupos de seguridad pueden tener como miembros usuarios y otros grupos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-146">Security groups can have users and other security groups as members.</span></span>

<span data-ttu-id="b6ea5-147">Los grupos de seguridad con correo habilitado se usan de la misma manera que los grupos de seguridad, pero incluyen la función de buzón compartido para los grupos.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-147">Mail-enabled security groups are used in the same way that security groups are, but with the added feature of a shared mailbox for the groups.</span></span> <span data-ttu-id="b6ea5-148">No es posible crear grupos de seguridad habilitados para correo electrónico mediante la API, pero funcionan otras operaciones de grupo.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-148">Mail-enabled security groups can't be created through the API, but other group operations work.</span></span>  <span data-ttu-id="b6ea5-149">Los grupos de seguridad habilitados para correo electrónico son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-149">Mail-enabled security groups are read only.</span></span> <span data-ttu-id="b6ea5-150">Obtenga más información en el artículo [Administrar grupos de seguridad de correo en Exchange](https://technet.microsoft.com/en-us/library/bb123521%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b6ea5-150">Learn more in the [Manage mail-enabled security groups Exchange article](https://technet.microsoft.com/en-us/library/bb123521%28v=exchg.160%29.aspx).</span></span>

### <a name="security-group-example"></a><span data-ttu-id="b6ea5-151">Ejemplo de grupo de seguridad</span><span class="sxs-lookup"><span data-stu-id="b6ea5-151">Security group example</span></span>

<span data-ttu-id="b6ea5-152">Esta es una representación JSON de un grupo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-152">The following is a JSON representation of a security group.</span></span> 

```http
{
    "@odata.type": "#microsoft.graph.group",
    "id": "f87faa71-57a8-4c14-91f0-517f54645106",
    "deletedDateTime": null,
    "classification": null,
    "createdDateTime": "2016-07-20T09:21:23Z",
    "description": "This group is a Security Group",
    "displayName": "SecurityGroup101",
    "groupTypes": [],
    "mail": null,
    "mailEnabled": false,
    "mailNickname": "",
    "preferredLanguage": null,
    "proxyAddresses": [],
    "securityEnabled": true
}
```
## <a name="dynamic-membership"></a><span data-ttu-id="b6ea5-153">Pertenencia dinámica</span><span class="sxs-lookup"><span data-stu-id="b6ea5-153">Dynamic membership</span></span> 

<span data-ttu-id="b6ea5-154">Todos los tipos de grupos pueden tener reglas de pertenencia dinámica que agregan o quitan miembros automáticamente del grupo según las propiedades del usuario.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-154">All types of groups can have dynamic membership rules that automatically add or remove members from the group based on user properties.</span></span> <span data-ttu-id="b6ea5-155">Por ejemplo, el grupo "Empleados de marketing" incluirá a todos los usuarios con la propiedad department establecida en "marketing", de modo que los nuevos empleados de marketing se agreguen automáticamente al grupo y los empleados que dejen el departamento se eliminen automáticamente del grupo.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-155">For example, a "Marketing employees" group would include every user with the department property set to "Marketing", so that new marketing employees are automatically added to the group and employees who leave the department are automatically removed from the group.</span></span> <span data-ttu-id="b6ea5-156">Esta regla se puede especificar en un campo "membershipRule" durante la creación de grupos como `"membershipRule": 'user.department -eq "Marketing"'`.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-156">This rule can be specified in a "membershipRule" field during group creation as `"membershipRule": 'user.department -eq "Marketing"'`.</span></span> <span data-ttu-id="b6ea5-157">GroupType también debe incluir `"DynamicMembership"`.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-157">GroupType must also include `"DynamicMembership"`.</span></span> <span data-ttu-id="b6ea5-158">Mediante la solicitud siguiente se crea un grupo de Office 365 para los empleados de marketing:</span><span class="sxs-lookup"><span data-stu-id="b6ea5-158">The following request creates a new Office 365 group for the marketing employees:</span></span> 

```http
POST https://graph.microsoft.com/beta/groups
{
    "description": "Marketing department folks",
    "displayName": "Marketing department",
    "groupTypes": [
        "Unified",
        "DynamicMembership"
    ],
    "mailEnabled": true,
    "mailNickname": "marketing",
    "securityEnabled": false,
    "membershipRule": 'user.department -eq "Marketing"',
    "membershipRuleProcessingState": "on"
}
```

<span data-ttu-id="b6ea5-159">Para más información sobre la formulación de propiedades membershipRule, vea [Creación de reglas de pertenencia dinámica a grupos basadas en atributos en Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="b6ea5-159">To learn more about formulating membershipRules, see [Create attribute-based rules for dynamic group membership in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal).</span></span>

> <span data-ttu-id="b6ea5-160">**Nota**: Las reglas de pertenencia dinámica requieren que el inquilino tenga una licencia de nivel [Azure Active Directory Premium P1](https://azure.microsoft.com/en-us/pricing/details/active-directory/) o superior.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-160">**Note**: Dynamic membership rules requires the tenant to have a license at tier [Azure Active Directory Premium P1](https://azure.microsoft.com/en-us/pricing/details/active-directory/) or greater.</span></span>

## <a name="other-types-of-groups"></a><span data-ttu-id="b6ea5-161">Otros tipos de grupos</span><span class="sxs-lookup"><span data-stu-id="b6ea5-161">Other types of groups</span></span>

<span data-ttu-id="b6ea5-162">Los Grupos de Office 365 en Yammer se usan para facilitar la colaboración de usuarios a través de publicaciones de Yammer.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-162">Office 365 groups in Yammer are used to facilitate user collaboration through Yammer posts.</span></span> <span data-ttu-id="b6ea5-163">Este tipo de grupo se puede devolver a través de una solicitud de lectura, pero no se puede obtener acceso a sus publicaciones mediante la API.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-163">This type of group can be returned through a read request, but their posts can't be accessed through the API.</span></span> <span data-ttu-id="b6ea5-164">Cuando las publicaciones y las fuentes de conversaciones de Yammer están habilitadas en un grupo, se deshabilitan las conversaciones del grupo de Office 365 predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-164">When Yammer posts and conversation feeds are enabled on a group, default Office 365 group conversations are disabled.</span></span> <span data-ttu-id="b6ea5-165">Para más información, vea los [documentos de la API para desarrolladores de Yammer](https://developer.yammer.com/docs).</span><span class="sxs-lookup"><span data-stu-id="b6ea5-165">To learn more, see [Yammer developer API docs](https://developer.yammer.com/docs).</span></span>

## <a name="common-use-cases"></a><span data-ttu-id="b6ea5-166">Casos de uso común</span><span class="sxs-lookup"><span data-stu-id="b6ea5-166">Common use cases</span></span>

<span data-ttu-id="b6ea5-167">Con Microsoft Graph, puede llevar a cabo las siguientes operaciones comunes.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-167">Using Microsoft Graph, you can perform the following common operations.</span></span>

| <span data-ttu-id="b6ea5-168">**Casos de uso**</span><span class="sxs-lookup"><span data-stu-id="b6ea5-168">**Use cases**</span></span>  | <span data-ttu-id="b6ea5-169">**Recursos de REST**</span><span class="sxs-lookup"><span data-stu-id="b6ea5-169">**REST resources**</span></span> | <span data-ttu-id="b6ea5-170">**Ver también**</span><span class="sxs-lookup"><span data-stu-id="b6ea5-170">**See also**</span></span> |
|:---------------|:--------|:----------|
| <span data-ttu-id="b6ea5-171">**Métodos de objeto de grupo**</span><span class="sxs-lookup"><span data-stu-id="b6ea5-171">**Group object and methods**</span></span> | | |
| <span data-ttu-id="b6ea5-172">Crear grupos, obtener grupos existentes, actualizar las propiedades de los grupos y eliminar grupos.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-172">Create new groups, get existing groups, update the properties on groups, and delete groups.</span></span> <span data-ttu-id="b6ea5-173">Actualmente, solo se pueden crear mediante la API grupos de seguridad y grupos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-173">Currently, only security groups and groups in Outlook can be created through the API.</span></span> | [<span data-ttu-id="b6ea5-174">group</span><span class="sxs-lookup"><span data-stu-id="b6ea5-174">group</span></span>](group.md) | [<span data-ttu-id="b6ea5-175">Crear grupos</span><span class="sxs-lookup"><span data-stu-id="b6ea5-175">Create new groups</span></span>](../api/group-post-groups.md) <br/> [<span data-ttu-id="b6ea5-176">Enumerar grupos</span><span class="sxs-lookup"><span data-stu-id="b6ea5-176">List groups</span></span>](../api/group-list.md) <br/> [<span data-ttu-id="b6ea5-177">Actualizar grupos</span><span class="sxs-lookup"><span data-stu-id="b6ea5-177">Update groups</span></span>](../api/group-update.md) <br/> [<span data-ttu-id="b6ea5-178">Eliminar grupos</span><span class="sxs-lookup"><span data-stu-id="b6ea5-178">Delete groups</span></span>](../api/group-delete.md) |
| <span data-ttu-id="b6ea5-179">**Métodos de pertenencia a grupos**</span><span class="sxs-lookup"><span data-stu-id="b6ea5-179">**Group membership methods**</span></span> | | |
| <span data-ttu-id="b6ea5-180">Enumerar los miembros de un grupo y agregar o quitar miembros.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-180">List the members of a group, and add or remove members.</span></span> | [<span data-ttu-id="b6ea5-181">user</span><span class="sxs-lookup"><span data-stu-id="b6ea5-181">user</span></span>](user.md) <br/> [<span data-ttu-id="b6ea5-182">group</span><span class="sxs-lookup"><span data-stu-id="b6ea5-182">group</span></span>](group.md)| [<span data-ttu-id="b6ea5-183">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="b6ea5-183">List members</span></span>](../api/group-list-members.md) <br/> [<span data-ttu-id="b6ea5-184">Agregar miembro</span><span class="sxs-lookup"><span data-stu-id="b6ea5-184">Add member</span></span>](../api/group-post-members.md) <br/> [<span data-ttu-id="b6ea5-185">Eliminar miembro</span><span class="sxs-lookup"><span data-stu-id="b6ea5-185">Remove member</span></span>](../api/group-delete-members.md)|
| <span data-ttu-id="b6ea5-186">Determinar si un usuario es miembro de un grupo y obtener todos los grupos a los que pertenece el usuario.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-186">Determine whether a user is a member of a group, get all the groups the user is a member of.</span></span> | [<span data-ttu-id="b6ea5-187">user</span><span class="sxs-lookup"><span data-stu-id="b6ea5-187">user</span></span>](user.md) <br/> [<span data-ttu-id="b6ea5-188">group</span><span class="sxs-lookup"><span data-stu-id="b6ea5-188">group</span></span>](group.md)| [<span data-ttu-id="b6ea5-189">Comprobar grupos de miembro</span><span class="sxs-lookup"><span data-stu-id="b6ea5-189">Check member groups</span></span>](../api/group-checkmembergroups.md) <br/> [<span data-ttu-id="b6ea5-190">Obtener grupos de miembro</span><span class="sxs-lookup"><span data-stu-id="b6ea5-190">Get member groups</span></span>](../api/group-getmembergroups.md)|
| <span data-ttu-id="b6ea5-191">Enumerar los propietarios de un grupo y agregar o quitar propietarios.</span><span class="sxs-lookup"><span data-stu-id="b6ea5-191">List the owners of a group, and add or remove owners.</span></span> | [<span data-ttu-id="b6ea5-192">user</span><span class="sxs-lookup"><span data-stu-id="b6ea5-192">user</span></span>](user.md) <br/> [<span data-ttu-id="b6ea5-193">group</span><span class="sxs-lookup"><span data-stu-id="b6ea5-193">group</span></span>](group.md)| [<span data-ttu-id="b6ea5-194">Enumerar propietarios</span><span class="sxs-lookup"><span data-stu-id="b6ea5-194">List owners</span></span>](../api/group-list-members.md) <br/> [<span data-ttu-id="b6ea5-195">Agregar miembro</span><span class="sxs-lookup"><span data-stu-id="b6ea5-195">Add member</span></span>](../api/group-post-members.md) <br/> [<span data-ttu-id="b6ea5-196">Eliminar miembro</span><span class="sxs-lookup"><span data-stu-id="b6ea5-196">Remove member</span></span>](../api/group-delete-members.md)|

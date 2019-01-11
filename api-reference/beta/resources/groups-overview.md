---
title: Trabajar con grupos en Microsoft Graph
description: Los grupos son colecciones de usuarios y otras entidades de seguridad que comparten el acceso a recursos de servicios de Microsoft o de la aplicación. Microsoft Graph proporciona API que se pueden usar para crear y administrar diversos tipos de grupos y funcionalidades de grupo según la situación. Todas las operaciones relacionadas con grupos de Microsoft Graph requieren permisos de administrador.
author: dkershaw10
localization_priority: Priority
ms.openlocfilehash: c244a372dffda1913cab71d63046caeb64186655
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27873804"
---
# <a name="working-with-groups-in-microsoft-graph"></a><span data-ttu-id="8a9c6-105">Trabajar con grupos en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="8a9c6-105">Working with groups in Microsoft Graph</span></span>

<span data-ttu-id="8a9c6-106">Los grupos son colecciones de [usuarios](user.md) y otras entidades de seguridad que comparten el acceso a recursos de servicios de Microsoft o de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-106">Groups are collections of [users](user.md) and other principals who share access to resources in Microsoft services or in your app.</span></span> <span data-ttu-id="8a9c6-107">Microsoft Graph proporciona API que se pueden usar para crear y administrar diversos tipos de grupos y funcionalidades de grupo según la situación.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-107">Microsoft Graph provides APIs that you can use to create and manage different types of groups and group functionality according to your scenario.</span></span> <span data-ttu-id="8a9c6-108">Todas las operaciones relacionadas con grupos de Microsoft Graph requieren permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-108">All group-related operations in Microsoft Graph require administrator consent.</span></span>

> <span data-ttu-id="8a9c6-109">**Nota**: Solo se pueden crear grupos mediante cuentas profesionales o educativas.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-109">**Note**: Groups can only be created through work or school accounts.</span></span> <span data-ttu-id="8a9c6-110">Las cuentas personales de Microsoft no admiten grupos.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-110">Personal Microsoft accounts don't support groups.</span></span>

| <span data-ttu-id="8a9c6-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a9c6-111">Type</span></span>              | <span data-ttu-id="8a9c6-112">Caso de uso</span><span class="sxs-lookup"><span data-stu-id="8a9c6-112">Use case</span></span> | <span data-ttu-id="8a9c6-113">groupType</span><span class="sxs-lookup"><span data-stu-id="8a9c6-113">groupType</span></span> | <span data-ttu-id="8a9c6-114">Con correo habilitado</span><span class="sxs-lookup"><span data-stu-id="8a9c6-114">mail-enabled</span></span> | <span data-ttu-id="8a9c6-115">Con seguridad habilitada</span><span class="sxs-lookup"><span data-stu-id="8a9c6-115">security-enabled</span></span> | <span data-ttu-id="8a9c6-116">¿Se puede crear mediante API?</span><span class="sxs-lookup"><span data-stu-id="8a9c6-116">Can be created via API?</span></span> |
|-------------------|----------|-----------|--------------|------------------|--------------------------------|
| [<span data-ttu-id="8a9c6-117">Grupos de Office 365</span><span class="sxs-lookup"><span data-stu-id="8a9c6-117">Office 365 groups</span></span>](#office-365-groups) | <span data-ttu-id="8a9c6-118">Facilitar la colaboración de usuarios con recursos compartidos en línea de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-118">Facilitating user collaboration with shared Microsoft online resources.</span></span> | `["Unified"]` | `true` | `false` | <span data-ttu-id="8a9c6-119">Sí</span><span class="sxs-lookup"><span data-stu-id="8a9c6-119">Yes</span></span> |
| [<span data-ttu-id="8a9c6-120">Grupos de seguridad</span><span class="sxs-lookup"><span data-stu-id="8a9c6-120">Security groups</span></span>](#security-groups-and-mail-enabled-security-groups) | <span data-ttu-id="8a9c6-121">Controlar el acceso de los usuarios a recursos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-121">Controlling user access to in-app resources.</span></span> | `[]` | `false` | `true` | <span data-ttu-id="8a9c6-122">Sí</span><span class="sxs-lookup"><span data-stu-id="8a9c6-122">Yes</span></span> |
| [<span data-ttu-id="8a9c6-123">Grupos de seguridad habilitados para correo</span><span class="sxs-lookup"><span data-stu-id="8a9c6-123">Mail-enabled security groups</span></span>](#security-groups-and-mail-enabled-security-groups) | <span data-ttu-id="8a9c6-124">Controlar el acceso de los usuarios a recursos de la aplicación, con un buzón de grupo compartido.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-124">Controlling user access to in-app resources, with a shared group mailbox.</span></span> | `[]` | `true` | `true` | <span data-ttu-id="8a9c6-125">No</span><span class="sxs-lookup"><span data-stu-id="8a9c6-125">No</span></span> |
| <span data-ttu-id="8a9c6-126">Grupos de distribución</span><span class="sxs-lookup"><span data-stu-id="8a9c6-126">Distribution groups</span></span> | <span data-ttu-id="8a9c6-127">Distribuir correo a los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-127">Distributing mail to the members of the group.</span></span> <span data-ttu-id="8a9c6-128">Se recomienda usar Grupos de Office 365 debido al variado conjunto de recursos que proporcionan.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-128">It is recommended to use Office 365 groups due to the richer set of resources it provides.</span></span> | `[]` | `true` | `false` | <span data-ttu-id="8a9c6-129">No</span><span class="sxs-lookup"><span data-stu-id="8a9c6-129">No</span></span> |

## <a name="office-365-groups"></a><span data-ttu-id="8a9c6-130">Grupos de Office 365</span><span class="sxs-lookup"><span data-stu-id="8a9c6-130">Office 365 groups</span></span>
<span data-ttu-id="8a9c6-131">La utilidad de Grupos de Office 365 reside en su naturaleza colaborativa, ideal para personas que trabajan juntas en un proyecto o equipo.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-131">The power of Office 365 groups is in its collaborative nature, perfect for people who work together on a project or a team.</span></span> <span data-ttu-id="8a9c6-132">Se crean con los recursos que comparten los miembros del grupo, incluidos los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8a9c6-132">They are created with resources that members of the group share, including:</span></span>

- <span data-ttu-id="8a9c6-133">Conversaciones de Outlook</span><span class="sxs-lookup"><span data-stu-id="8a9c6-133">Outlook conversations</span></span>
- <span data-ttu-id="8a9c6-134">Calendario de Outlook</span><span class="sxs-lookup"><span data-stu-id="8a9c6-134">Outlook calendar</span></span>
- <span data-ttu-id="8a9c6-135">Archivos de SharePoint</span><span class="sxs-lookup"><span data-stu-id="8a9c6-135">SharePoint files</span></span>
- <span data-ttu-id="8a9c6-136">Bloc de notas de OneNote</span><span class="sxs-lookup"><span data-stu-id="8a9c6-136">OneNote notebook</span></span>
- <span data-ttu-id="8a9c6-137">Sitio de grupo de SharePoint</span><span class="sxs-lookup"><span data-stu-id="8a9c6-137">SharePoint team site</span></span>
- <span data-ttu-id="8a9c6-138">Planes de Planner</span><span class="sxs-lookup"><span data-stu-id="8a9c6-138">Planner plans</span></span>
- <span data-ttu-id="8a9c6-139">Administración de dispositivos de Intune</span><span class="sxs-lookup"><span data-stu-id="8a9c6-139">Intune device management</span></span>

### <a name="group-in-outlook-example"></a><span data-ttu-id="8a9c6-140">Ejemplo de grupo de Outlook</span><span class="sxs-lookup"><span data-stu-id="8a9c6-140">Group in Outlook example</span></span>

<span data-ttu-id="8a9c6-141">Esta es una representación JSON de grupos en Outlook.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-141">The following is a JSON representation of groups in Outlook.</span></span> 

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
<span data-ttu-id="8a9c6-142">Para más información sobre Grupos de Office 365 y las experiencias de administrador, vea [Obtenga más información sobre los grupos de Office 365](https://support.office.com/en-us/article/Learn-about-Office-365-groups-b565caa1-5c40-40ef-9915-60fdb2d97fa2).</span><span class="sxs-lookup"><span data-stu-id="8a9c6-142">To learn more about Office 365 groups and the administrator experiences, see [Learn about Office 365 Groups](https://support.office.com/en-us/article/Learn-about-Office-365-groups-b565caa1-5c40-40ef-9915-60fdb2d97fa2).</span></span>

## <a name="security-groups-and-mail-enabled-security-groups"></a><span data-ttu-id="8a9c6-143">Grupos de seguridad y grupos de seguridad con correo habilitado</span><span class="sxs-lookup"><span data-stu-id="8a9c6-143">Security groups and mail-enabled security groups</span></span>

<span data-ttu-id="8a9c6-144">Los grupos de seguridad están diseñados para controlar el acceso de los usuarios a los recursos.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-144">Security groups are for controlling user access to resources.</span></span> <span data-ttu-id="8a9c6-145">Al comprobar si un usuario es miembro de un grupo de seguridad, la aplicación puede tomar decisiones de autorización cuando el usuario intenta obtener acceso a algunos recursos seguros de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-145">By checking whether a user is a member of a security group, your app can make authorization decisions when that user is trying to access some secure resources in your app.</span></span> <span data-ttu-id="8a9c6-146">Los grupos de seguridad pueden tener como miembros usuarios y otros grupos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-146">Security groups can have users and other security groups as members.</span></span>

<span data-ttu-id="8a9c6-147">Los grupos de seguridad con correo habilitado se usan de la misma manera que los grupos de seguridad, pero incluyen la función de buzón compartido para los grupos.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-147">Mail-enabled security groups are used in the same way that security groups are, but with the added feature of a shared mailbox for the groups.</span></span> <span data-ttu-id="8a9c6-148">No es posible crear grupos de seguridad habilitados para correo electrónico mediante la API, pero funcionan otras operaciones de grupo.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-148">Mail-enabled security groups can't be created through the API, but other group operations work.</span></span> <span data-ttu-id="8a9c6-149">Los grupos de seguridad habilitados para correo electrónico son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-149">Mail-enabled security groups are read only.</span></span> <span data-ttu-id="8a9c6-150">Obtenga más información en el artículo [Administrar grupos de seguridad de correo en Exchange](https://technet.microsoft.com/en-us/library/bb123521%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8a9c6-150">Learn more in the [Manage mail-enabled security groups Exchange article](https://technet.microsoft.com/en-us/library/bb123521%28v=exchg.160%29.aspx).</span></span>

### <a name="security-group-example"></a><span data-ttu-id="8a9c6-151">Ejemplo de grupo de seguridad</span><span class="sxs-lookup"><span data-stu-id="8a9c6-151">Security group example</span></span>

<span data-ttu-id="8a9c6-152">Esta es una representación JSON de un grupo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-152">The following is a JSON representation of a security group.</span></span> 

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
## <a name="dynamic-membership"></a><span data-ttu-id="8a9c6-153">Pertenencia dinámica</span><span class="sxs-lookup"><span data-stu-id="8a9c6-153">Dynamic membership</span></span> 

<span data-ttu-id="8a9c6-154">Todos los tipos de grupos pueden tener reglas de pertenencia dinámica que agregan o quitan miembros automáticamente del grupo según las propiedades del usuario.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-154">All types of groups can have dynamic membership rules that automatically add or remove members from the group based on user properties.</span></span> <span data-ttu-id="8a9c6-155">Por ejemplo, el grupo "Empleados de marketing" incluirá a todos los usuarios con la propiedad department establecida en "marketing", de modo que los nuevos empleados de marketing se agreguen automáticamente al grupo y los empleados que dejen el departamento se eliminen automáticamente del grupo.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-155">For example, a "Marketing employees" group would include every user with the department property set to "Marketing", so that new marketing employees are automatically added to the group and employees who leave the department are automatically removed from the group.</span></span> <span data-ttu-id="8a9c6-156">Esta regla se puede especificar en un campo "membershipRule" durante la creación de grupos como `"membershipRule": 'user.department -eq "Marketing"'`.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-156">This rule can be specified in a "membershipRule" field during group creation as `"membershipRule": 'user.department -eq "Marketing"'`.</span></span> <span data-ttu-id="8a9c6-157">GroupType también debe incluir `"DynamicMembership"`.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-157">GroupType must also include `"DynamicMembership"`.</span></span> <span data-ttu-id="8a9c6-158">Mediante la solicitud siguiente se crea un grupo de Office 365 para los empleados de marketing:</span><span class="sxs-lookup"><span data-stu-id="8a9c6-158">The following request creates a new Office 365 group for the marketing employees:</span></span> 

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

<span data-ttu-id="8a9c6-159">Para más información sobre la formulación de propiedades membershipRule, vea [Creación de reglas de pertenencia dinámica a grupos basadas en atributos en Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="8a9c6-159">To learn more about formulating membershipRules, see [Create attribute-based rules for dynamic group membership in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal).</span></span>

> <span data-ttu-id="8a9c6-160">**Nota**: Las reglas de pertenencia dinámica requieren que el inquilino tenga una licencia de nivel [Azure Active Directory Premium P1](https://azure.microsoft.com/en-us/pricing/details/active-directory/) o superior.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-160">**Note**: Dynamic membership rules requires the tenant to have a license at tier [Azure Active Directory Premium P1](https://azure.microsoft.com/en-us/pricing/details/active-directory/) or greater.</span></span>

## <a name="other-types-of-groups"></a><span data-ttu-id="8a9c6-161">Otros tipos de grupos</span><span class="sxs-lookup"><span data-stu-id="8a9c6-161">Other types of groups</span></span>

<span data-ttu-id="8a9c6-162">Los Grupos de Office 365 en Yammer se usan para facilitar la colaboración de usuarios a través de publicaciones de Yammer.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-162">Office 365 groups in Yammer are used to facilitate user collaboration through Yammer posts.</span></span> <span data-ttu-id="8a9c6-163">Este tipo de grupo se puede devolver a través de una solicitud de lectura, pero no se puede obtener acceso a sus publicaciones mediante la API.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-163">This type of group can be returned through a read request, but their posts can't be accessed through the API.</span></span> <span data-ttu-id="8a9c6-164">Cuando las publicaciones y las fuentes de conversaciones de Yammer están habilitadas en un grupo, se deshabilitan las conversaciones del grupo de Office 365 predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-164">When Yammer posts and conversation feeds are enabled on a group, default Office 365 group conversations are disabled.</span></span> <span data-ttu-id="8a9c6-165">Para más información, vea los [documentos de la API para desarrolladores de Yammer](https://developer.yammer.com/docs).</span><span class="sxs-lookup"><span data-stu-id="8a9c6-165">To learn more, see [Yammer developer API docs](https://developer.yammer.com/docs).</span></span>

## <a name="group-based-licensing"></a><span data-ttu-id="8a9c6-166">Concesión de licencias por grupo</span><span class="sxs-lookup"><span data-stu-id="8a9c6-166">Group-based licensing</span></span> 

<span data-ttu-id="8a9c6-167">Capacidad de licencia basadas en grupos puede usarse para asignar una o varias licencias del producto a un grupo de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-167">Group-based licensing capability can be used to assign one or more product licenses to an Azure AD group.</span></span> <span data-ttu-id="8a9c6-168">Azure AD se asegura de que las licencias se asignan a todos los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-168">Azure AD ensures that the licenses are assigned to all members of the group.</span></span> <span data-ttu-id="8a9c6-169">Los nuevos miembros que se unen al grupo se asignan las licencias adecuadas.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-169">Any new members who join the group are assigned the appropriate licenses.</span></span> <span data-ttu-id="8a9c6-170">Cuando deja el grupo, se quitan las licencias.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-170">When they leave the group, those licenses are removed.</span></span> <span data-ttu-id="8a9c6-171">La característica sólo puede utilizarse con grupos de seguridad y los grupos de Office 365 que tienen securityEnabled = TRUE.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-171">The feature can only be used with security groups, and Office 365 groups that have securityEnabled=TRUE.</span></span> <span data-ttu-id="8a9c6-172">Para obtener más información acerca de licencias, consulte basadas en grupos [aquí](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="8a9c6-172">To learn more about group-based licensing see [here](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal).</span></span>

## <a name="common-use-cases"></a><span data-ttu-id="8a9c6-173">Casos de uso común</span><span class="sxs-lookup"><span data-stu-id="8a9c6-173">Common use cases</span></span>

<span data-ttu-id="8a9c6-174">Con Microsoft Graph, puede llevar a cabo las siguientes operaciones comunes.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-174">Using Microsoft Graph, you can perform the following common operations.</span></span>

| <span data-ttu-id="8a9c6-175">**Casos de uso**</span><span class="sxs-lookup"><span data-stu-id="8a9c6-175">**Use cases**</span></span>  | <span data-ttu-id="8a9c6-176">**Recursos de REST**</span><span class="sxs-lookup"><span data-stu-id="8a9c6-176">**REST resources**</span></span> | <span data-ttu-id="8a9c6-177">**Ver también**</span><span class="sxs-lookup"><span data-stu-id="8a9c6-177">**See also**</span></span> |
|:---------------|:--------|:----------|
| <span data-ttu-id="8a9c6-178">**Métodos de objeto de grupo**</span><span class="sxs-lookup"><span data-stu-id="8a9c6-178">**Group object and methods**</span></span> | | |
| <span data-ttu-id="8a9c6-179">Crear grupos, obtener grupos existentes, actualizar las propiedades de los grupos y eliminar grupos.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-179">Create new groups, get existing groups, update the properties on groups, and delete groups.</span></span> <span data-ttu-id="8a9c6-180">Actualmente, solo se pueden crear mediante la API grupos de seguridad y grupos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-180">Currently, only security groups and groups in Outlook can be created through the API.</span></span> | [<span data-ttu-id="8a9c6-181">group</span><span class="sxs-lookup"><span data-stu-id="8a9c6-181">group</span></span>](group.md) | [<span data-ttu-id="8a9c6-182">Crear grupos</span><span class="sxs-lookup"><span data-stu-id="8a9c6-182">Create new groups</span></span>](../api/group-post-groups.md) <br/> [<span data-ttu-id="8a9c6-183">Enumerar grupos</span><span class="sxs-lookup"><span data-stu-id="8a9c6-183">List groups</span></span>](../api/group-list.md) <br/> [<span data-ttu-id="8a9c6-184">Actualizar grupos</span><span class="sxs-lookup"><span data-stu-id="8a9c6-184">Update groups</span></span>](../api/group-update.md) <br/> [<span data-ttu-id="8a9c6-185">Eliminar grupos</span><span class="sxs-lookup"><span data-stu-id="8a9c6-185">Delete groups</span></span>](../api/group-delete.md) |
| <span data-ttu-id="8a9c6-186">**Métodos de pertenencia a grupos**</span><span class="sxs-lookup"><span data-stu-id="8a9c6-186">**Group membership methods**</span></span> | | |
| <span data-ttu-id="8a9c6-187">Enumerar los miembros de un grupo y agregar o quitar miembros.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-187">List the members of a group, and add or remove members.</span></span> | [<span data-ttu-id="8a9c6-188">user</span><span class="sxs-lookup"><span data-stu-id="8a9c6-188">user</span></span>](user.md) <br/> [<span data-ttu-id="8a9c6-189">group</span><span class="sxs-lookup"><span data-stu-id="8a9c6-189">group</span></span>](group.md)| [<span data-ttu-id="8a9c6-190">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="8a9c6-190">List members</span></span>](../api/group-list-members.md) <br/> [<span data-ttu-id="8a9c6-191">Agregar miembro</span><span class="sxs-lookup"><span data-stu-id="8a9c6-191">Add member</span></span>](../api/group-post-members.md) <br/> [<span data-ttu-id="8a9c6-192">Eliminar miembro</span><span class="sxs-lookup"><span data-stu-id="8a9c6-192">Remove member</span></span>](../api/group-delete-members.md)|
| <span data-ttu-id="8a9c6-193">Determinar si un usuario es miembro de un grupo y obtener todos los grupos a los que pertenece el usuario.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-193">Determine whether a user is a member of a group, get all the groups the user is a member of.</span></span> | [<span data-ttu-id="8a9c6-194">user</span><span class="sxs-lookup"><span data-stu-id="8a9c6-194">user</span></span>](user.md) <br/> [<span data-ttu-id="8a9c6-195">group</span><span class="sxs-lookup"><span data-stu-id="8a9c6-195">group</span></span>](group.md)| [<span data-ttu-id="8a9c6-196">Comprobar grupos de miembro</span><span class="sxs-lookup"><span data-stu-id="8a9c6-196">Check member groups</span></span>](../api/group-checkmembergroups.md) <br/> [<span data-ttu-id="8a9c6-197">Obtener grupos de miembro</span><span class="sxs-lookup"><span data-stu-id="8a9c6-197">Get member groups</span></span>](../api/group-getmembergroups.md)|
| <span data-ttu-id="8a9c6-198">Enumerar los propietarios de un grupo y agregar o quitar propietarios.</span><span class="sxs-lookup"><span data-stu-id="8a9c6-198">List the owners of a group, and add or remove owners.</span></span> | [<span data-ttu-id="8a9c6-199">user</span><span class="sxs-lookup"><span data-stu-id="8a9c6-199">user</span></span>](user.md) <br/> [<span data-ttu-id="8a9c6-200">group</span><span class="sxs-lookup"><span data-stu-id="8a9c6-200">group</span></span>](group.md)| [<span data-ttu-id="8a9c6-201">Enumerar propietarios</span><span class="sxs-lookup"><span data-stu-id="8a9c6-201">List owners</span></span>](../api/group-list-members.md) <br/> [<span data-ttu-id="8a9c6-202">Agregar miembro</span><span class="sxs-lookup"><span data-stu-id="8a9c6-202">Add member</span></span>](../api/group-post-members.md) <br/> [<span data-ttu-id="8a9c6-203">Eliminar miembro</span><span class="sxs-lookup"><span data-stu-id="8a9c6-203">Remove member</span></span>](../api/group-delete-members.md)|

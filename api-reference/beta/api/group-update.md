---
title: Actualizar grupo
description: Actualiza las propiedades de un objeto de grupo.
ms.openlocfilehash: 1a87bc3e6599d37cab25e3e98c9dcf63d7d078e9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085658"
---
# <a name="update-group"></a><span data-ttu-id="c3551-103">Actualizar grupo</span><span class="sxs-lookup"><span data-stu-id="c3551-103">Update group</span></span>

> <span data-ttu-id="c3551-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c3551-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c3551-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c3551-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c3551-106">Actualizar las propiedades de un objeto de [grupo](../resources/group.md) .</span><span class="sxs-lookup"><span data-stu-id="c3551-106">Update the properties of a [group](../resources/group.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="c3551-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c3551-107">Permissions</span></span>

<span data-ttu-id="c3551-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c3551-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c3551-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c3551-110">Permission type</span></span>      | <span data-ttu-id="c3551-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c3551-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c3551-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c3551-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c3551-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c3551-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="c3551-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c3551-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c3551-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c3551-115">Not supported.</span></span>    |
|<span data-ttu-id="c3551-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c3551-116">Application</span></span> | <span data-ttu-id="c3551-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c3551-117">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c3551-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c3551-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /groups/{id}
```

## <a name="request-headers"></a><span data-ttu-id="c3551-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c3551-119">Request headers</span></span>

| <span data-ttu-id="c3551-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="c3551-120">Name</span></span>       | <span data-ttu-id="c3551-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="c3551-121">Type</span></span> | <span data-ttu-id="c3551-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3551-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="c3551-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="c3551-123">Authorization</span></span>  | <span data-ttu-id="c3551-124">string</span><span class="sxs-lookup"><span data-stu-id="c3551-124">string</span></span>  | <span data-ttu-id="c3551-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c3551-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c3551-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c3551-127">Request body</span></span>

<span data-ttu-id="c3551-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="c3551-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="c3551-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c3551-131">Property</span></span>   | <span data-ttu-id="c3551-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="c3551-132">Type</span></span> |<span data-ttu-id="c3551-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3551-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c3551-134">allowExternalSenders</span><span class="sxs-lookup"><span data-stu-id="c3551-134">allowExternalSenders</span></span>|<span data-ttu-id="c3551-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="c3551-135">Boolean</span></span>|<span data-ttu-id="c3551-p105">El valor predeterminado es **false**. Indica si los usuarios externos a la organización pueden enviar mensajes al grupo.</span><span class="sxs-lookup"><span data-stu-id="c3551-p105">Default is **false**. Indicates if people external to the organization can send messages to the group.</span></span>|
|<span data-ttu-id="c3551-138">autoSubscribeNewMembers</span><span class="sxs-lookup"><span data-stu-id="c3551-138">autoSubscribeNewMembers</span></span>|<span data-ttu-id="c3551-139">Booleano</span><span class="sxs-lookup"><span data-stu-id="c3551-139">Boolean</span></span>|<span data-ttu-id="c3551-p106">El valor predeterminado es **false**. Indica si los miembros agregados al grupo se suscribirán de forma automática para recibir notificaciones por correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c3551-p106">Default is **false**. Indicates if new members added to the group will be auto-subscribed to receive email notifications.</span></span>|
|<span data-ttu-id="c3551-142">descripción</span><span class="sxs-lookup"><span data-stu-id="c3551-142">description</span></span>|<span data-ttu-id="c3551-143">String</span><span class="sxs-lookup"><span data-stu-id="c3551-143">String</span></span>|<span data-ttu-id="c3551-144">Una descripción opcional del grupo.</span><span class="sxs-lookup"><span data-stu-id="c3551-144">An optional description for the group.</span></span> |
|<span data-ttu-id="c3551-145">displayName</span><span class="sxs-lookup"><span data-stu-id="c3551-145">displayName</span></span>|<span data-ttu-id="c3551-146">String</span><span class="sxs-lookup"><span data-stu-id="c3551-146">String</span></span>|<span data-ttu-id="c3551-p107">El nombre para mostrar del grupo. Esta propiedad es necesaria cuando se crea un grupo y no se puede borrar durante las actualizaciones. Es compatible con $filter y $orderby.</span><span class="sxs-lookup"><span data-stu-id="c3551-p107">The display name for the group. This property is required when a group is created and it cannot be cleared during updates. Supports $filter and $orderby.</span></span>|
|<span data-ttu-id="c3551-150">groupTypes</span><span class="sxs-lookup"><span data-stu-id="c3551-150">groupTypes</span></span>|<span data-ttu-id="c3551-151">Colección string</span><span class="sxs-lookup"><span data-stu-id="c3551-151">String collection</span></span>|<span data-ttu-id="c3551-p108">Especifica el tipo de grupo que se va a crear. Los valores posibles son **Unified** para crear un grupo de Office 365 o **DynamicMembership** para grupos dinámicos.  Para los demás tipos de grupos, como los grupos con seguridad habilitada y los grupos de seguridad habilitados para correo electrónico, no establezca esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c3551-p108">Specifies the type of group to create. Possible values are **Unified** to create an Office 365 group, or **DynamicMembership** for dynamic groups.  For all other group types, like security-enabled groups and email-enabled security groups, do not set this property.</span></span>|
|<span data-ttu-id="c3551-155">mailEnabled</span><span class="sxs-lookup"><span data-stu-id="c3551-155">mailEnabled</span></span>|<span data-ttu-id="c3551-156">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3551-156">Boolean</span></span>|<span data-ttu-id="c3551-p109">Especifica si el grupo está habilitado para correo. Si la propiedad **securityEnabled** también es **true**, el grupo es un grupo de seguridad habilitado para correo electrónico; en caso contrario, el grupo es un grupo de distribución de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="c3551-p109">Specifies whether the group is mail-enabled. If the **securityEnabled** property is also **true**, the group is a mail-enabled security group; otherwise, the group is a Microsoft Exchange distribution group.</span></span>|
|<span data-ttu-id="c3551-159">mailNickname</span><span class="sxs-lookup"><span data-stu-id="c3551-159">mailNickname</span></span>|<span data-ttu-id="c3551-160">String</span><span class="sxs-lookup"><span data-stu-id="c3551-160">String</span></span>|<span data-ttu-id="c3551-p110">El alias de correo del grupo. Esta propiedad debe especificarse al crear un grupo. Es compatible con $filter.</span><span class="sxs-lookup"><span data-stu-id="c3551-p110">The mail alias for the group. This property must be specified when a group is created. Supports $filter.</span></span>|
|<span data-ttu-id="c3551-164">securityEnabled</span><span class="sxs-lookup"><span data-stu-id="c3551-164">securityEnabled</span></span>|<span data-ttu-id="c3551-165">Boolean</span><span class="sxs-lookup"><span data-stu-id="c3551-165">Boolean</span></span>|<span data-ttu-id="c3551-p111">Especifica si el grupo es un grupo de seguridad. Si la propiedad **mailEnabled** también es true, el grupo es un grupo de seguridad habilitado para correo electrónico; de lo contrario, es un grupo de seguridad. Debe ser **false** para grupos de Office 365. Es compatible con $filter.</span><span class="sxs-lookup"><span data-stu-id="c3551-p111">Specifies whether the group is a security group. If the **mailEnabled** property is also true, the group is a mail-enabled security group; otherwise it is a security group. Must be **false** for Office 365 groups. Supports $filter..</span></span>|
|<span data-ttu-id="c3551-170">visibility</span><span class="sxs-lookup"><span data-stu-id="c3551-170">visibility</span></span>|<span data-ttu-id="c3551-171">String</span><span class="sxs-lookup"><span data-stu-id="c3551-171">String</span></span>|<span data-ttu-id="c3551-p112">Especifica la visibilidad de un grupo de Office 365. Los valores posibles son: **Private**, **Public** o vacío (que se interpreta como **Public**).</span><span class="sxs-lookup"><span data-stu-id="c3551-p112">Specifies the visibility of an Office 365 group. Possible values are: **Private**, **Public**, or empty (which is interpreted as **Public**).</span></span>|

<span data-ttu-id="c3551-174">Puesto que el recurso de **grupo** admite [extensiones](/graph/extensibility-overview), puede usar el `PATCH` operación para agregar, actualizar o eliminar sus propios datos específicas de la aplicación en las propiedades personalizadas de una extensión en una instancia de **grupo** existente.</span><span class="sxs-lookup"><span data-stu-id="c3551-174">Since the **group** resource supports [extensions](/graph/extensibility-overview), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **group** instance.</span></span>

> <span data-ttu-id="c3551-175">**Nota**:</span><span class="sxs-lookup"><span data-stu-id="c3551-175">**Note:**</span></span>
>
> - <span data-ttu-id="c3551-176">Puede actualizar **autoSubscribeNewMembers** especificándolo en su propia solicitud PATCH sin incluir el resto de propiedades de la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="c3551-176">You can update **autoSubscribeNewMembers** by specifying it in its own PATCH request, without including the other properties in the table above.</span></span>
> - <span data-ttu-id="c3551-p113">Solo un subconjunto de la API de grupo relativa a la administración de grupos básicos admite permisos delegados y de aplicación. Todos los demás miembros de la API de grupo, incluida la actualización **autoSubscribeNewMembers**, son compatible solo con los permisos delegados. Vea [problemas conocidos](https://developer.microsoft.com/graph/docs/overview/release_notes#group-permission-scopes) para obtener ejemplos.</span><span class="sxs-lookup"><span data-stu-id="c3551-p113">Only a subset of the group API pertaining to core group administration and management support application and delegated permissions. All other members of the group API, including updating  **autoSubscribeNewMembers**, support only delegated permissions. See [known issues](https://developer.microsoft.com/graph/docs/overview/release_notes#group-permission-scopes) for examples.</span></span>

## <a name="response"></a><span data-ttu-id="c3551-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c3551-180">Response</span></span>

<span data-ttu-id="c3551-181">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="c3551-181">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="c3551-182">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c3551-182">Example</span></span>

#### <a name="request"></a><span data-ttu-id="c3551-183">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c3551-183">Request</span></span>

<span data-ttu-id="c3551-184">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c3551-184">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_group"
}-->

```http
PATCH https://graph.microsoft.com/beta/groups/{id}
Content-type: application/json
Content-length: 211

{
  "description": "description-value",
  "displayName": "displayName-value",
  "groupTypes": [
    "groupTypes-value"
  ],
  "mail": "mail-value",
  "mailEnabled": true,
  "mailNickname": "mailNickname-value"
}
```

#### <a name="response"></a><span data-ttu-id="c3551-185">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c3551-185">Response</span></span>

<span data-ttu-id="c3551-186">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c3551-186">The following is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->

```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a><span data-ttu-id="c3551-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3551-187">See also</span></span>

- [<span data-ttu-id="c3551-188">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="c3551-188">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="c3551-189">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="c3551-189">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="c3551-190">Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="c3551-190">Add custom data to groups using schema extensions (preview)</span></span>](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

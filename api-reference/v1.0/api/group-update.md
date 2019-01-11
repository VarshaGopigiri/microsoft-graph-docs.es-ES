---
title: Actualizar grupo
description: Actualiza las propiedades de un objeto de grupo.
author: dkershaw10
localization_priority: Priority
ms.openlocfilehash: 92ba1110f0b92a8042e3e3a982d385ded4fdc68a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27879698"
---
# <a name="update-group"></a><span data-ttu-id="554a1-103">Actualizar grupo</span><span class="sxs-lookup"><span data-stu-id="554a1-103">Update group</span></span>

<span data-ttu-id="554a1-104">Actualiza las propiedades de un objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="554a1-104">Update the properties of a group object.</span></span>

## <a name="permissions"></a><span data-ttu-id="554a1-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="554a1-105">Permissions</span></span>

<span data-ttu-id="554a1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="554a1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="554a1-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="554a1-108">Permission type</span></span>      | <span data-ttu-id="554a1-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="554a1-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="554a1-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="554a1-110">Delegated (work or school account)</span></span> | <span data-ttu-id="554a1-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="554a1-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="554a1-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="554a1-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="554a1-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="554a1-113">Not supported.</span></span>    |
|<span data-ttu-id="554a1-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="554a1-114">Application</span></span> | <span data-ttu-id="554a1-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="554a1-115">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="554a1-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="554a1-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /groups/{id}
```

## <a name="request-headers"></a><span data-ttu-id="554a1-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="554a1-117">Request headers</span></span>

| <span data-ttu-id="554a1-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="554a1-118">Name</span></span>       | <span data-ttu-id="554a1-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="554a1-119">Type</span></span> | <span data-ttu-id="554a1-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="554a1-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="554a1-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="554a1-121">Authorization</span></span>  | <span data-ttu-id="554a1-122">string</span><span class="sxs-lookup"><span data-stu-id="554a1-122">string</span></span>  | <span data-ttu-id="554a1-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="554a1-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="554a1-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="554a1-125">Request body</span></span>

<span data-ttu-id="554a1-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="554a1-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="554a1-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="554a1-129">Property</span></span>   | <span data-ttu-id="554a1-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="554a1-130">Type</span></span> |<span data-ttu-id="554a1-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="554a1-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="554a1-132">allowExternalSenders</span><span class="sxs-lookup"><span data-stu-id="554a1-132">allowExternalSenders</span></span>|<span data-ttu-id="554a1-133">Booleano</span><span class="sxs-lookup"><span data-stu-id="554a1-133">Boolean</span></span>|<span data-ttu-id="554a1-p104">El valor predeterminado es **false**. Indica si los usuarios externos a la organización pueden enviar mensajes al grupo.</span><span class="sxs-lookup"><span data-stu-id="554a1-p104">Default is **false**. Indicates if people external to the organization can send messages to the group.</span></span>|
|<span data-ttu-id="554a1-136">autoSubscribeNewMembers</span><span class="sxs-lookup"><span data-stu-id="554a1-136">autoSubscribeNewMembers</span></span>|<span data-ttu-id="554a1-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="554a1-137">Boolean</span></span>|<span data-ttu-id="554a1-p105">El valor predeterminado es **false**. Indica si los miembros agregados al grupo se suscribirán de forma automática para recibir notificaciones por correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="554a1-p105">Default is **false**. Indicates if new members added to the group will be auto-subscribed to receive email notifications.</span></span>|
|<span data-ttu-id="554a1-140">descripción</span><span class="sxs-lookup"><span data-stu-id="554a1-140">description</span></span>|<span data-ttu-id="554a1-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="554a1-141">String</span></span>|<span data-ttu-id="554a1-142">Una descripción opcional del grupo.</span><span class="sxs-lookup"><span data-stu-id="554a1-142">An optional description for the group.</span></span> |
|<span data-ttu-id="554a1-143">displayName</span><span class="sxs-lookup"><span data-stu-id="554a1-143">displayName</span></span>|<span data-ttu-id="554a1-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="554a1-144">String</span></span>|<span data-ttu-id="554a1-p106">El nombre para mostrar del grupo. Esta propiedad es necesaria cuando se crea un grupo y no se puede borrar durante las actualizaciones. Es compatible con $filter y $orderby.</span><span class="sxs-lookup"><span data-stu-id="554a1-p106">The display name for the group. This property is required when a group is created and it cannot be cleared during updates. Supports $filter and $orderby.</span></span>|
|<span data-ttu-id="554a1-148">groupTypes</span><span class="sxs-lookup"><span data-stu-id="554a1-148">groupTypes</span></span>|<span data-ttu-id="554a1-149">Colección string</span><span class="sxs-lookup"><span data-stu-id="554a1-149">String collection</span></span>|<span data-ttu-id="554a1-p107">Especifica el tipo de grupo que se va a crear. Los valores posibles son **Unified** para crear un grupo de Office 365 o **DynamicMembership** para grupos dinámicos.  Para los demás tipos de grupos, como los grupos con seguridad habilitada y los grupos de seguridad habilitados para correo electrónico, no establezca esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="554a1-p107">Specifies the type of group to create. Possible values are **Unified** to create an Office 365 group, or **DynamicMembership** for dynamic groups.  For all other group types, like security-enabled groups and email-enabled security groups, do not set this property.</span></span>|
|<span data-ttu-id="554a1-153">mailEnabled</span><span class="sxs-lookup"><span data-stu-id="554a1-153">mailEnabled</span></span>|<span data-ttu-id="554a1-154">Boolean</span><span class="sxs-lookup"><span data-stu-id="554a1-154">Boolean</span></span>|<span data-ttu-id="554a1-p108">Especifica si el grupo está habilitado para correo. Si la propiedad **securityEnabled** también es **true**, el grupo es un grupo de seguridad habilitado para correo electrónico; en caso contrario, el grupo es un grupo de distribución de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="554a1-p108">Specifies whether the group is mail-enabled. If the **securityEnabled** property is also **true**, the group is a mail-enabled security group; otherwise, the group is a Microsoft Exchange distribution group.</span></span>|
|<span data-ttu-id="554a1-157">mailNickname</span><span class="sxs-lookup"><span data-stu-id="554a1-157">mailNickname</span></span>|<span data-ttu-id="554a1-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="554a1-158">String</span></span>|<span data-ttu-id="554a1-p109">El alias de correo del grupo. Esta propiedad debe especificarse al crear un grupo. Es compatible con $filter.</span><span class="sxs-lookup"><span data-stu-id="554a1-p109">The mail alias for the group. This property must be specified when a group is created. Supports $filter.</span></span>|
|<span data-ttu-id="554a1-162">securityEnabled</span><span class="sxs-lookup"><span data-stu-id="554a1-162">securityEnabled</span></span>|<span data-ttu-id="554a1-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="554a1-163">Boolean</span></span>|<span data-ttu-id="554a1-p110">Especifica si el grupo es un grupo de seguridad. Si la propiedad **mailEnabled** también es true, el grupo es un grupo de seguridad habilitado para correo electrónico; de lo contrario, es un grupo de seguridad. Debe ser **false** para grupos de Office 365. Es compatible con $filter.</span><span class="sxs-lookup"><span data-stu-id="554a1-p110">Specifies whether the group is a security group. If the **mailEnabled** property is also true, the group is a mail-enabled security group; otherwise it is a security group. Must be **false** for Office 365 groups. Supports $filter..</span></span>|
|<span data-ttu-id="554a1-168">visibility</span><span class="sxs-lookup"><span data-stu-id="554a1-168">visibility</span></span>|<span data-ttu-id="554a1-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="554a1-169">String</span></span>|<span data-ttu-id="554a1-170">Especifica la visibilidad de un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="554a1-170">Specifies the visibility of an Office 365 group.</span></span> <span data-ttu-id="554a1-171">Los valores posibles son: **Private**, **Public**o empty (que se interpreta como **pública**).</span><span class="sxs-lookup"><span data-stu-id="554a1-171">The possible values are: **Private**, **Public**, or empty (which is interpreted as **Public**).</span></span>|

> <span data-ttu-id="554a1-172">**Nota**:</span><span class="sxs-lookup"><span data-stu-id="554a1-172">**Note:**</span></span>
>
> - <span data-ttu-id="554a1-173">Puede actualizar **autoSubscribeNewMembers** mediante la especificación en su propia solicitud de revisión, sin incluir las demás propiedades en la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="554a1-173">You can update **autoSubscribeNewMembers** by specifying it in its own PATCH request,without including the other properties in the table above.</span></span>
> - <span data-ttu-id="554a1-p112">Solo un subconjunto de la API de grupo relativa a la administración de grupos básicos admite permisos delegados y de aplicación. Todos los demás miembros de la API de grupo, incluida la actualización **autoSubscribeNewMembers**, son compatible solo con los permisos delegados. Vea [problemas conocidos](https://developer.microsoft.com/graph/docs/overview/release_notes#group-permission-scopes) para obtener ejemplos.</span><span class="sxs-lookup"><span data-stu-id="554a1-p112">Only a subset of the group API pertaining to core group administration and management support application and delegated permissions. All other members of the group API, including updating  **autoSubscribeNewMembers**, support only delegated permissions. See [known issues](https://developer.microsoft.com/graph/docs/overview/release_notes#group-permission-scopes) for examples.</span></span>

## <a name="response"></a><span data-ttu-id="554a1-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="554a1-177">Response</span></span>

<span data-ttu-id="554a1-178">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="554a1-178">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="554a1-179">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="554a1-179">Example</span></span>

#### <a name="request"></a><span data-ttu-id="554a1-180">Solicitud</span><span class="sxs-lookup"><span data-stu-id="554a1-180">Request</span></span>

<span data-ttu-id="554a1-181">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="554a1-181">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_group"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/groups/{id}
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

#### <a name="response"></a><span data-ttu-id="554a1-182">Respuesta</span><span class="sxs-lookup"><span data-stu-id="554a1-182">Response</span></span>

<span data-ttu-id="554a1-183">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="554a1-183">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

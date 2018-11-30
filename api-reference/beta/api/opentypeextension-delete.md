---
title: Eliminar extensión abierta
description: 'Elimina una extensión abierta (objeto openTypeExtension) de la instancia especificada de un recurso. '
ms.openlocfilehash: 852573241e65e1a68ecbb308a67f79ee4ec14ab8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085027"
---
# <a name="delete-open-extension"></a><span data-ttu-id="8447d-103">Eliminar extensión abierta</span><span class="sxs-lookup"><span data-stu-id="8447d-103">Delete open extension</span></span>

> <span data-ttu-id="8447d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8447d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8447d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8447d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8447d-106">Elimina una extensión abierta (objeto [openTypeExtension](../resources/opentypeextension.md)) de la instancia especificada de un recurso.</span><span class="sxs-lookup"><span data-stu-id="8447d-106">Delete an open extension ([openTypeExtension](../resources/opentypeextension.md) object) from the specified instance of a resource.</span></span> 

## <a name="permissions"></a><span data-ttu-id="8447d-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="8447d-107">Permissions</span></span>

<span data-ttu-id="8447d-108">Según el recurso que está eliminando la extensión de y el permiso solicitado tipo (delegada o de la aplicación), el permiso especificado en la tabla siguiente es la con privilegios mínimos necesarios para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="8447d-108">Depending on the resource you're deleting the extension from and the permission type (delegated or application) requested, the permission specified in the following table is the least privileged required to call this API.</span></span> <span data-ttu-id="8447d-109">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8447d-109">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="8447d-110">Recurso admitido</span><span class="sxs-lookup"><span data-stu-id="8447d-110">Supported resource</span></span> | <span data-ttu-id="8447d-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8447d-111">Delegated (work or school account)</span></span> | <span data-ttu-id="8447d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8447d-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8447d-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8447d-113">Application</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="8447d-114">device</span><span class="sxs-lookup"><span data-stu-id="8447d-114">device</span></span>](../resources/device.md) | <span data-ttu-id="8447d-115">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="8447d-115">Directory.AccessAsUser.All</span></span> | <span data-ttu-id="8447d-116">No admitido</span><span class="sxs-lookup"><span data-stu-id="8447d-116">Not supported</span></span> | <span data-ttu-id="8447d-117">Device.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8447d-117">Device.ReadWrite.All</span></span> |
| [<span data-ttu-id="8447d-118">evento</span><span class="sxs-lookup"><span data-stu-id="8447d-118">event</span></span>](../resources/event.md) | <span data-ttu-id="8447d-119">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8447d-119">Calendars.ReadWrite</span></span> | <span data-ttu-id="8447d-120">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8447d-120">Calendars.ReadWrite</span></span> | <span data-ttu-id="8447d-121">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8447d-121">Calendars.ReadWrite</span></span> |
| [<span data-ttu-id="8447d-122">grupo</span><span class="sxs-lookup"><span data-stu-id="8447d-122">group</span></span>](../resources/group.md) | <span data-ttu-id="8447d-123">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8447d-123">Group.ReadWrite.All</span></span> | <span data-ttu-id="8447d-124">No admitido</span><span class="sxs-lookup"><span data-stu-id="8447d-124">Not supported</span></span> | <span data-ttu-id="8447d-125">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8447d-125">Group.ReadWrite.All</span></span> |
| [<span data-ttu-id="8447d-126">evento de grupo</span><span class="sxs-lookup"><span data-stu-id="8447d-126">group event</span></span>](../resources/event.md) | <span data-ttu-id="8447d-127">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8447d-127">Group.ReadWrite.All</span></span> | <span data-ttu-id="8447d-128">No admitido</span><span class="sxs-lookup"><span data-stu-id="8447d-128">Not supported</span></span> | <span data-ttu-id="8447d-129">No admitido</span><span class="sxs-lookup"><span data-stu-id="8447d-129">Not supported</span></span> |
| [<span data-ttu-id="8447d-130">publicación de grupo</span><span class="sxs-lookup"><span data-stu-id="8447d-130">group post</span></span>](../resources/post.md) | <span data-ttu-id="8447d-131">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8447d-131">Group.ReadWrite.All</span></span> | <span data-ttu-id="8447d-132">No admitido</span><span class="sxs-lookup"><span data-stu-id="8447d-132">Not supported</span></span> | <span data-ttu-id="8447d-133">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8447d-133">Group.ReadWrite.All</span></span> |
| [<span data-ttu-id="8447d-134">mensaje</span><span class="sxs-lookup"><span data-stu-id="8447d-134">message</span></span>](../resources/message.md) | <span data-ttu-id="8447d-135">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8447d-135">Mail.ReadWrite</span></span> | <span data-ttu-id="8447d-136">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8447d-136">Mail.ReadWrite</span></span> | <span data-ttu-id="8447d-137">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8447d-137">Mail.ReadWrite</span></span> | 
| [<span data-ttu-id="8447d-138">organización</span><span class="sxs-lookup"><span data-stu-id="8447d-138">organization</span></span>](../resources/organization.md) | <span data-ttu-id="8447d-139">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="8447d-139">Directory.AccessAsUser.All</span></span> | <span data-ttu-id="8447d-140">No admitido</span><span class="sxs-lookup"><span data-stu-id="8447d-140">Not supported</span></span> | <span data-ttu-id="8447d-141">No admitido</span><span class="sxs-lookup"><span data-stu-id="8447d-141">Not supported</span></span> |
| [<span data-ttu-id="8447d-142">contacto personal</span><span class="sxs-lookup"><span data-stu-id="8447d-142">personal contact</span></span>](../resources/contact.md) | <span data-ttu-id="8447d-143">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8447d-143">Contacts.ReadWrite</span></span> | <span data-ttu-id="8447d-144">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8447d-144">Contacts.ReadWrite</span></span> | <span data-ttu-id="8447d-145">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8447d-145">Contacts.ReadWrite</span></span> |
| [<span data-ttu-id="8447d-146">usuario</span><span class="sxs-lookup"><span data-stu-id="8447d-146">user</span></span>](../resources/user.md) | <span data-ttu-id="8447d-147">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8447d-147">User.ReadWrite.All</span></span> | <span data-ttu-id="8447d-148">User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8447d-148">User.ReadWrite</span></span> | <span data-ttu-id="8447d-149">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8447d-149">User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="8447d-150">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8447d-150">HTTP request</span></span>

<span data-ttu-id="8447d-151">En la solicitud, identifique la instancia de recurso, utilice la propiedad de navegación **extensiones** de esa instancia para identificar y realizar un `DELETE` en esa instancia de extensión.</span><span class="sxs-lookup"><span data-stu-id="8447d-151">In the request, identify the resource instance, use the **extensions** navigation property of that instance to identify the extension, and do a `DELETE` on that extension instance.</span></span>

<!-- { "blockType": "ignored" } -->
```http
DELETE /administrativeUnits/{Id}/extensions/{extensionId}
DELETE /devices/{Id}/extensions/{extensionId}
DELETE /users/{id|userPrincipalName}/events/{id}/extensions/{extensionId}
DELETE /groups/{id}/extensions/{extensionId}
DELETE /groups/{id}/events/{id}/extensions/{extensionId}
DELETE /groups/{id}/threads/{id}/posts/{id}/extensions/{extensionId}
DELETE /users/{id|userPrincipalName}/messages/{id}/extensions/{extensionId}
DELETE /organization/{Id}/extensions/{extensionId}
DELETE /users/{id|userPrincipalName}/contacts/{id}/extensions/{extensionId}
DELETE /users/{id|userPrincipalName}/extensions/{extensionId}
```

><span data-ttu-id="8447d-p103">**Nota:** La sintaxis anterior muestra algunas formas comunes para identificar una instancia del recurso, con el fin de eliminar una extensión de él. Todas las otras formas de sintaxis que le permiten identificar estas instancias de recursos admiten la eliminación de extensiones abiertas de ellas de una manera similar.</span><span class="sxs-lookup"><span data-stu-id="8447d-p103">**Note:** The above syntax shows some common ways to identify a resource instance, in order to delete an extension from it. All other syntax that allows you to identify these resource instances supports deleting open extensions from them in a similar way.</span></span>

## <a name="path-parameters"></a><span data-ttu-id="8447d-154">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="8447d-154">Path parameters</span></span>
|<span data-ttu-id="8447d-155">**Parámetro**</span><span class="sxs-lookup"><span data-stu-id="8447d-155">**Parameter**</span></span>|<span data-ttu-id="8447d-156">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8447d-156">**Type**</span></span>|<span data-ttu-id="8447d-157">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8447d-157">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8447d-158">id</span><span class="sxs-lookup"><span data-stu-id="8447d-158">id</span></span>|<span data-ttu-id="8447d-159">string</span><span class="sxs-lookup"><span data-stu-id="8447d-159">string</span></span>|<span data-ttu-id="8447d-p104">Un identificador único para una instancia en la colección correspondiente. Necesario.</span><span class="sxs-lookup"><span data-stu-id="8447d-p104">A unique identifier for an instance in the corresponding collection. Required.</span></span>|
|<span data-ttu-id="8447d-162">extensionId</span><span class="sxs-lookup"><span data-stu-id="8447d-162">extensionId</span></span>|<span data-ttu-id="8447d-163">string</span><span class="sxs-lookup"><span data-stu-id="8447d-163">string</span></span>|<span data-ttu-id="8447d-p105">Puede ser un nombre de extensión, que es un identificador de texto único de la extensión, o un nombre completo que concatena el tipo de extensión y un identificador de texto único. Se devuelve el nombre completo de la propiedad `id` al crear la extensión. Necesario.</span><span class="sxs-lookup"><span data-stu-id="8447d-p105">This can be an extension name which is a unique text identifier for the extension, or a fully qualified name which concatenates the extension type and unique text identifier. The fully qualified name is returned in the `id` property when you create the extension. Required.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="8447d-167">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8447d-167">Request headers</span></span>
| <span data-ttu-id="8447d-168">Nombre</span><span class="sxs-lookup"><span data-stu-id="8447d-168">Name</span></span>       | <span data-ttu-id="8447d-169">Valor</span><span class="sxs-lookup"><span data-stu-id="8447d-169">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="8447d-170">Authorization</span><span class="sxs-lookup"><span data-stu-id="8447d-170">Authorization</span></span> | <span data-ttu-id="8447d-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8447d-p106">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8447d-173">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8447d-173">Request body</span></span>
<span data-ttu-id="8447d-174">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8447d-174">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8447d-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8447d-175">Response</span></span>

<span data-ttu-id="8447d-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8447d-p107">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8447d-178">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8447d-178">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8447d-179">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8447d-179">Request</span></span>
<span data-ttu-id="8447d-180">El primer ejemplo hace referencia a una extensión por su nombre y elimina la extensión en el mensaje especificado.</span><span class="sxs-lookup"><span data-stu-id="8447d-180">The first example references an extension by its name and deletes the extension in the specified message.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_opentypeextension"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions('Com.Contoso.Referral')
```

<span data-ttu-id="8447d-181">El segundo ejemplo elimina una extensión en el evento de grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="8447d-181">The second example deletes an extension in the specified group event.</span></span>

<!-- { "blockType": "ignored" } -->
```http
DELETE https://graph.microsoft.com/beta/groups('f5480dfd-7d77-4d0b-ba2e-3391953cc74a')/events('AAMkADVlN17IsAAA=')/extensions('Com.Contoso.Referral')
```

 

##### <a name="response"></a><span data-ttu-id="8447d-182">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8447d-182">Response</span></span>
<span data-ttu-id="8447d-183">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8447d-183">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete opentypeextension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
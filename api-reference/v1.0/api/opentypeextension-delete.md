---
title: Eliminar extensión abierta
description: 'Elimina una extensión abierta (objeto openTypeExtension) de la instancia especificada de un recurso. '
ms.openlocfilehash: 9906b0b68711f1bb78d220252366b0c4a56592fc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032519"
---
# <a name="delete-open-extension"></a><span data-ttu-id="d9b8c-103">Eliminar extensión abierta</span><span class="sxs-lookup"><span data-stu-id="d9b8c-103">Delete open extension</span></span>

<span data-ttu-id="d9b8c-104">Elimina una extensión abierta (objeto [openTypeExtension](../resources/opentypeextension.md)) de la instancia especificada de un recurso.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-104">Delete an open extension ([openTypeExtension](../resources/opentypeextension.md) object) from the specified instance of a resource.</span></span> 

## <a name="permissions"></a><span data-ttu-id="d9b8c-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="d9b8c-105">Permissions</span></span>

<span data-ttu-id="d9b8c-106">Según el recurso que está eliminando la extensión de y el permiso solicitado tipo (delegada o de la aplicación), el permiso especificado en la tabla siguiente es la con privilegios mínimos necesarios para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-106">Depending on the resource you're deleting the extension from and the permission type (delegated or application) requested, the permission specified in the following table is the least privileged required to call this API.</span></span> <span data-ttu-id="d9b8c-107">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d9b8c-107">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="d9b8c-108">Recurso admitido</span><span class="sxs-lookup"><span data-stu-id="d9b8c-108">Supported resource</span></span> | <span data-ttu-id="d9b8c-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d9b8c-109">Delegated (work or school account)</span></span> | <span data-ttu-id="d9b8c-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d9b8c-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d9b8c-111">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d9b8c-111">Application</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="d9b8c-112">device</span><span class="sxs-lookup"><span data-stu-id="d9b8c-112">device</span></span>](../resources/device.md) | <span data-ttu-id="d9b8c-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="d9b8c-113">Directory.AccessAsUser.All</span></span> | <span data-ttu-id="d9b8c-114">No admitido</span><span class="sxs-lookup"><span data-stu-id="d9b8c-114">Not supported</span></span> | <span data-ttu-id="d9b8c-115">Device.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d9b8c-115">Device.ReadWrite.All</span></span> |
| [<span data-ttu-id="d9b8c-116">evento</span><span class="sxs-lookup"><span data-stu-id="d9b8c-116">event</span></span>](../resources/event.md) | <span data-ttu-id="d9b8c-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d9b8c-117">Calendars.ReadWrite</span></span> | <span data-ttu-id="d9b8c-118">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d9b8c-118">Calendars.ReadWrite</span></span> | <span data-ttu-id="d9b8c-119">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d9b8c-119">Calendars.ReadWrite</span></span> |
| [<span data-ttu-id="d9b8c-120">grupo</span><span class="sxs-lookup"><span data-stu-id="d9b8c-120">group</span></span>](../resources/group.md) | <span data-ttu-id="d9b8c-121">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d9b8c-121">Group.ReadWrite.All</span></span> | <span data-ttu-id="d9b8c-122">No admitido</span><span class="sxs-lookup"><span data-stu-id="d9b8c-122">Not supported</span></span> | <span data-ttu-id="d9b8c-123">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d9b8c-123">Group.ReadWrite.All</span></span> |
| [<span data-ttu-id="d9b8c-124">evento de grupo</span><span class="sxs-lookup"><span data-stu-id="d9b8c-124">group event</span></span>](../resources/event.md) | <span data-ttu-id="d9b8c-125">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d9b8c-125">Group.ReadWrite.All</span></span> | <span data-ttu-id="d9b8c-126">No admitido</span><span class="sxs-lookup"><span data-stu-id="d9b8c-126">Not supported</span></span> | <span data-ttu-id="d9b8c-127">No admitido</span><span class="sxs-lookup"><span data-stu-id="d9b8c-127">Not supported</span></span> |
| [<span data-ttu-id="d9b8c-128">publicación de grupo</span><span class="sxs-lookup"><span data-stu-id="d9b8c-128">group post</span></span>](../resources/post.md) | <span data-ttu-id="d9b8c-129">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d9b8c-129">Group.ReadWrite.All</span></span> | <span data-ttu-id="d9b8c-130">No admitido</span><span class="sxs-lookup"><span data-stu-id="d9b8c-130">Not supported</span></span> | <span data-ttu-id="d9b8c-131">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d9b8c-131">Group.ReadWrite.All</span></span> |
| [<span data-ttu-id="d9b8c-132">mensaje</span><span class="sxs-lookup"><span data-stu-id="d9b8c-132">message</span></span>](../resources/message.md) | <span data-ttu-id="d9b8c-133">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d9b8c-133">Mail.ReadWrite</span></span> | <span data-ttu-id="d9b8c-134">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d9b8c-134">Mail.ReadWrite</span></span> | <span data-ttu-id="d9b8c-135">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d9b8c-135">Mail.ReadWrite</span></span> | 
| [<span data-ttu-id="d9b8c-136">organización</span><span class="sxs-lookup"><span data-stu-id="d9b8c-136">organization</span></span>](../resources/organization.md) | <span data-ttu-id="d9b8c-137">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="d9b8c-137">Directory.AccessAsUser.All</span></span> | <span data-ttu-id="d9b8c-138">No admitido</span><span class="sxs-lookup"><span data-stu-id="d9b8c-138">Not supported</span></span> | <span data-ttu-id="d9b8c-139">No admitido</span><span class="sxs-lookup"><span data-stu-id="d9b8c-139">Not supported</span></span> |
| [<span data-ttu-id="d9b8c-140">contacto personal</span><span class="sxs-lookup"><span data-stu-id="d9b8c-140">personal contact</span></span>](../resources/contact.md) | <span data-ttu-id="d9b8c-141">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d9b8c-141">Contacts.ReadWrite</span></span> | <span data-ttu-id="d9b8c-142">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d9b8c-142">Contacts.ReadWrite</span></span> | <span data-ttu-id="d9b8c-143">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d9b8c-143">Contacts.ReadWrite</span></span> |
| [<span data-ttu-id="d9b8c-144">usuario</span><span class="sxs-lookup"><span data-stu-id="d9b8c-144">user</span></span>](../resources/user.md) | <span data-ttu-id="d9b8c-145">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d9b8c-145">User.ReadWrite.All</span></span> | <span data-ttu-id="d9b8c-146">User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d9b8c-146">User.ReadWrite</span></span> | <span data-ttu-id="d9b8c-147">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d9b8c-147">User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d9b8c-148">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d9b8c-148">HTTP request</span></span>
<span data-ttu-id="d9b8c-149">En la solicitud, identifique la instancia de recurso, utilice la propiedad de navegación **extensiones** de esa instancia para identificar y realizar un `DELETE` en esa instancia de extensión.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-149">In the request, identify the resource instance, use the **extensions** navigation property of that instance to identify the extension, and do a `DELETE` on that extension instance.</span></span>

<!-- { "blockType": "ignored" } -->
```http
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

><span data-ttu-id="d9b8c-p102">**Nota:** La sintaxis anterior muestra algunas formas comunes para identificar una instancia del recurso, con el fin de eliminar una extensión de él. Todas las otras formas de sintaxis que le permiten identificar estas instancias de recursos admiten la eliminación de extensiones abiertas de ellas de una manera similar.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-p102">**Note:** The above syntax shows some common ways to identify a resource instance, in order to delete an extension from it. All other syntax that allows you to identify these resource instances supports deleting open extensions from them in a similar way.</span></span>

## <a name="path-parameters"></a><span data-ttu-id="d9b8c-152">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="d9b8c-152">Path parameters</span></span>
|<span data-ttu-id="d9b8c-153">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d9b8c-153">Parameter</span></span>|<span data-ttu-id="d9b8c-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9b8c-154">Type</span></span>|<span data-ttu-id="d9b8c-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9b8c-155">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d9b8c-156">id</span><span class="sxs-lookup"><span data-stu-id="d9b8c-156">id</span></span>|<span data-ttu-id="d9b8c-157">string</span><span class="sxs-lookup"><span data-stu-id="d9b8c-157">string</span></span>|<span data-ttu-id="d9b8c-p103">Un identificador único para una instancia en la colección correspondiente. Necesario.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-p103">A unique identifier for an instance in the corresponding collection. Required.</span></span>|
|<span data-ttu-id="d9b8c-160">extensionId</span><span class="sxs-lookup"><span data-stu-id="d9b8c-160">extensionId</span></span>|<span data-ttu-id="d9b8c-161">string</span><span class="sxs-lookup"><span data-stu-id="d9b8c-161">string</span></span>|<span data-ttu-id="d9b8c-p104">Puede ser un nombre de extensión, que es un identificador de texto único de la extensión, o un nombre completo que concatena el tipo de extensión y un identificador de texto único. Se devuelve el nombre completo de la propiedad `id` al crear la extensión. Necesario.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-p104">This can be an extension name which is a unique text identifier for the extension, or a fully qualified name which concatenates the extension type and unique text identifier. The fully qualified name is returned in the `id` property when you create the extension. Required.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="d9b8c-165">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d9b8c-165">Request headers</span></span>
| <span data-ttu-id="d9b8c-166">Nombre</span><span class="sxs-lookup"><span data-stu-id="d9b8c-166">Name</span></span>       | <span data-ttu-id="d9b8c-167">Valor</span><span class="sxs-lookup"><span data-stu-id="d9b8c-167">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="d9b8c-168">Authorization</span><span class="sxs-lookup"><span data-stu-id="d9b8c-168">Authorization</span></span> | <span data-ttu-id="d9b8c-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d9b8c-171">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d9b8c-171">Request body</span></span>
<span data-ttu-id="d9b8c-172">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-172">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d9b8c-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9b8c-173">Response</span></span>

<span data-ttu-id="d9b8c-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-p106">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d9b8c-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d9b8c-176">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d9b8c-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d9b8c-177">Request</span></span>
<span data-ttu-id="d9b8c-178">El primer ejemplo hace referencia a una extensión por su nombre y elimina la extensión en el mensaje especificado.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-178">The first example references an extension by its name and deletes the extension in the specified message.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["Com.Contoso.Referral", "AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl==="],
  "name": "delete_opentypeextension"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/messages/AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===/extensions/Com.Contoso.Referral
```

<span data-ttu-id="d9b8c-179">El segundo ejemplo elimina una extensión en el evento de grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-179">The second example deletes an extension in the specified group event.</span></span>

<!-- { "blockType": "ignored" } -->
```http
DELETE https://graph.microsoft.com/v1.0/groups/f5480dfd-7d77-4d0b-ba2e-3391953cc74a/events/AAMkADVlN17IsAAA=/extensions/Com.Contoso.Referral
```

 

##### <a name="response"></a><span data-ttu-id="d9b8c-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9b8c-180">Response</span></span>
<span data-ttu-id="d9b8c-181">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-181">Here is an example of the response.</span></span>
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
# <a name="delete-open-extension"></a><span data-ttu-id="afce1-101">Eliminar extensión abierta</span><span class="sxs-lookup"><span data-stu-id="afce1-101">Delete open extension</span></span>

<span data-ttu-id="afce1-102">Elimina una extensión abierta (objeto [openTypeExtension](../resources/openTypeExtension.md)) de la instancia especificada de un recurso.</span><span class="sxs-lookup"><span data-stu-id="afce1-102">Delete an open extension ([openTypeExtension](../resources/openTypeExtension.md) object) from the specified instance of a resource.</span></span> 

## <a name="permissions"></a><span data-ttu-id="afce1-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="afce1-103">Permissions</span></span>

<span data-ttu-id="afce1-104">Según el recurso que está eliminando la extensión de y el permiso solicitado tipo (delegada o de la aplicación), el permiso especificado en la tabla siguiente es la con privilegios mínimos necesarios para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="afce1-104">Depending on the resource you're deleting the extension from and the permission type (delegated or application) requested, the permission specified in the following table is the least privileged required to call this API.</span></span> <span data-ttu-id="afce1-105">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="afce1-105">To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="afce1-106">Recurso admitido</span><span class="sxs-lookup"><span data-stu-id="afce1-106">Supported resource</span></span> | <span data-ttu-id="afce1-107">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="afce1-107">Delegated (work or school account)</span></span> | <span data-ttu-id="afce1-108">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="afce1-108">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="afce1-109">Aplicación</span><span class="sxs-lookup"><span data-stu-id="afce1-109">Application</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="afce1-110">dispositivo</span><span class="sxs-lookup"><span data-stu-id="afce1-110">device</span></span>](../resources/device.md) | <span data-ttu-id="afce1-111">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="afce1-111">Directory.AccessAsUser.All</span></span> | <span data-ttu-id="afce1-112">No admitido</span><span class="sxs-lookup"><span data-stu-id="afce1-112">Not supported</span></span> | <span data-ttu-id="afce1-113">Device.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="afce1-113">Device.ReadWrite.All</span></span> |
| [<span data-ttu-id="afce1-114">evento</span><span class="sxs-lookup"><span data-stu-id="afce1-114">event</span></span>](../resources/event.md) | <span data-ttu-id="afce1-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="afce1-115">Calendars.ReadWrite</span></span> | <span data-ttu-id="afce1-116">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="afce1-116">Calendars.ReadWrite</span></span> | <span data-ttu-id="afce1-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="afce1-117">Calendars.ReadWrite</span></span> |
| [<span data-ttu-id="afce1-118">grupo</span><span class="sxs-lookup"><span data-stu-id="afce1-118">group</span></span>](../resources/group.md) | <span data-ttu-id="afce1-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="afce1-119">Group.ReadWrite.All</span></span> | <span data-ttu-id="afce1-120">No admitido</span><span class="sxs-lookup"><span data-stu-id="afce1-120">Not supported</span></span> | <span data-ttu-id="afce1-121">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="afce1-121">Group.ReadWrite.All</span></span> |
| [<span data-ttu-id="afce1-122">evento de grupo</span><span class="sxs-lookup"><span data-stu-id="afce1-122">group event</span></span>](../resources/event.md) | <span data-ttu-id="afce1-123">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="afce1-123">Group.ReadWrite.All</span></span> | <span data-ttu-id="afce1-124">No admitido</span><span class="sxs-lookup"><span data-stu-id="afce1-124">Not supported</span></span> | <span data-ttu-id="afce1-125">No admitido</span><span class="sxs-lookup"><span data-stu-id="afce1-125">Not supported</span></span> |
| [<span data-ttu-id="afce1-126">publicación de grupo</span><span class="sxs-lookup"><span data-stu-id="afce1-126">group post</span></span>](../resources/post.md) | <span data-ttu-id="afce1-127">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="afce1-127">Group.ReadWrite.All</span></span> | <span data-ttu-id="afce1-128">No admitido</span><span class="sxs-lookup"><span data-stu-id="afce1-128">Not supported</span></span> | <span data-ttu-id="afce1-129">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="afce1-129">Group.ReadWrite.All</span></span> |
| [<span data-ttu-id="afce1-130">mensaje</span><span class="sxs-lookup"><span data-stu-id="afce1-130">message</span></span>](../resources/message.md) | <span data-ttu-id="afce1-131">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="afce1-131">Mail.ReadWrite</span></span> | <span data-ttu-id="afce1-132">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="afce1-132">Mail.ReadWrite</span></span> | <span data-ttu-id="afce1-133">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="afce1-133">Mail.ReadWrite</span></span> | 
| [<span data-ttu-id="afce1-134">organización</span><span class="sxs-lookup"><span data-stu-id="afce1-134">organization</span></span>](../resources/organization.md) | <span data-ttu-id="afce1-135">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="afce1-135">Directory.AccessAsUser.All</span></span> | <span data-ttu-id="afce1-136">No admitido</span><span class="sxs-lookup"><span data-stu-id="afce1-136">Not supported</span></span> | <span data-ttu-id="afce1-137">No admitido</span><span class="sxs-lookup"><span data-stu-id="afce1-137">Not supported</span></span> |
| [<span data-ttu-id="afce1-138">contacto personal</span><span class="sxs-lookup"><span data-stu-id="afce1-138">personal contact</span></span>](../resources/contact.md) | <span data-ttu-id="afce1-139">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="afce1-139">Contacts.ReadWrite</span></span> | <span data-ttu-id="afce1-140">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="afce1-140">Contacts.ReadWrite</span></span> | <span data-ttu-id="afce1-141">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="afce1-141">Contacts.ReadWrite</span></span> |
| [<span data-ttu-id="afce1-142">usuario</span><span class="sxs-lookup"><span data-stu-id="afce1-142">user</span></span>](../resources/user.md) | <span data-ttu-id="afce1-143">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="afce1-143">User.ReadWrite.All</span></span> | <span data-ttu-id="afce1-144">User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="afce1-144">User.ReadWrite</span></span> | <span data-ttu-id="afce1-145">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="afce1-145">User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="afce1-146">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="afce1-146">HTTP request</span></span>
<span data-ttu-id="afce1-147">En la solicitud, identifique la instancia de recurso, utilice la propiedad de navegación **extensiones** de esa instancia para identificar y realizar un `DELETE` en esa instancia de extensión.</span><span class="sxs-lookup"><span data-stu-id="afce1-147">In the request, identify the resource instance, use the **extensions** navigation property of that instance to identify the extension, and do a `DELETE` on that extension instance.</span></span>

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

><span data-ttu-id="afce1-p102">**Nota:** La sintaxis anterior muestra algunas formas comunes para identificar una instancia del recurso, con el fin de eliminar una extensión de él. Todas las otras formas de sintaxis que le permiten identificar estas instancias de recursos admiten la eliminación de extensiones abiertas de ellas de una manera similar.</span><span class="sxs-lookup"><span data-stu-id="afce1-p102">**Note:** The above syntax shows some common ways to identify a resource instance, in order to delete an extension from it. All other syntax that allows you to identify these resource instances supports deleting open extensions from them in a similar way.</span></span>

## <a name="path-parameters"></a><span data-ttu-id="afce1-150">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="afce1-150">Path parameters</span></span>
|<span data-ttu-id="afce1-151">Parámetro</span><span class="sxs-lookup"><span data-stu-id="afce1-151">Parameter</span></span>|<span data-ttu-id="afce1-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="afce1-152">Type</span></span>|<span data-ttu-id="afce1-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="afce1-153">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="afce1-154">id</span><span class="sxs-lookup"><span data-stu-id="afce1-154">id</span></span>|<span data-ttu-id="afce1-155">string</span><span class="sxs-lookup"><span data-stu-id="afce1-155">string</span></span>|<span data-ttu-id="afce1-p103">Un identificador único para una instancia en la colección correspondiente. Necesario.</span><span class="sxs-lookup"><span data-stu-id="afce1-p103">A unique identifier for an instance in the corresponding collection. Required.</span></span>|
|<span data-ttu-id="afce1-158">extensionId</span><span class="sxs-lookup"><span data-stu-id="afce1-158">extensionId</span></span>|<span data-ttu-id="afce1-159">string</span><span class="sxs-lookup"><span data-stu-id="afce1-159">string</span></span>|<span data-ttu-id="afce1-p104">Puede ser un nombre de extensión, que es un identificador de texto único de la extensión, o un nombre completo que concatena el tipo de extensión y un identificador de texto único. Se devuelve el nombre completo de la propiedad `id` al crear la extensión. Necesario.</span><span class="sxs-lookup"><span data-stu-id="afce1-p104">This can be an extension name which is a unique text identifier for the extension, or a fully qualified name which concatenates the extension type and unique text identifier. The fully qualified name is returned in the `id` property when you create the extension. Required.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="afce1-163">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="afce1-163">Request headers</span></span>
| <span data-ttu-id="afce1-164">Nombre</span><span class="sxs-lookup"><span data-stu-id="afce1-164">Name</span></span>       | <span data-ttu-id="afce1-165">Valor</span><span class="sxs-lookup"><span data-stu-id="afce1-165">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="afce1-166">Authorization</span><span class="sxs-lookup"><span data-stu-id="afce1-166">Authorization</span></span> | <span data-ttu-id="afce1-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="afce1-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="afce1-169">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="afce1-169">Request body</span></span>
<span data-ttu-id="afce1-170">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="afce1-170">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="afce1-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="afce1-171">Response</span></span>

<span data-ttu-id="afce1-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="afce1-p106">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="afce1-174">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="afce1-174">Example</span></span>
##### <a name="request"></a><span data-ttu-id="afce1-175">Solicitud</span><span class="sxs-lookup"><span data-stu-id="afce1-175">Request</span></span>
<span data-ttu-id="afce1-176">El primer ejemplo hace referencia a una extensión por su nombre y elimina la extensión en el mensaje especificado.</span><span class="sxs-lookup"><span data-stu-id="afce1-176">The first example references an extension by its name and deletes the extension in the specified message.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["Com.Contoso.Referral", "AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl==="],
  "name": "delete_opentypeextension"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/messages/AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===/extensions/Com.Contoso.Referral
```

<span data-ttu-id="afce1-177">El segundo ejemplo elimina una extensión en el evento de grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="afce1-177">The second example deletes an extension in the specified group event.</span></span>

<!-- { "blockType": "ignored" } -->
```http
DELETE https://graph.microsoft.com/v1.0/groups/f5480dfd-7d77-4d0b-ba2e-3391953cc74a/events/AAMkADVlN17IsAAA=/extensions/Com.Contoso.Referral
```

 

##### <a name="response"></a><span data-ttu-id="afce1-178">Respuesta</span><span class="sxs-lookup"><span data-stu-id="afce1-178">Response</span></span>
<span data-ttu-id="afce1-179">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="afce1-179">Here is an example of the response.</span></span>
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
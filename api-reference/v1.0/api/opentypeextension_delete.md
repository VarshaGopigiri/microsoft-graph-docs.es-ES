# <a name="delete-open-extension"></a><span data-ttu-id="5f110-101">Eliminar extensión abierta</span><span class="sxs-lookup"><span data-stu-id="5f110-101">Delete open extension</span></span>

<span data-ttu-id="5f110-102">Elimina una extensión abierta (objeto [openTypeExtension](../resources/openTypeExtension.md)) de la instancia especificada de un recurso.</span><span class="sxs-lookup"><span data-stu-id="5f110-102">Delete an open extension ([openTypeExtension](../resources/openTypeExtension.md) object) from the specified instance of a resource.</span></span> 

## <a name="permissions"></a><span data-ttu-id="5f110-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="5f110-103">Permissions</span></span>

<span data-ttu-id="5f110-p101">Según el recurso desde el que elimine la extensión, se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5f110-p101">One of the following permissions is required to call this API, depending on the resource you're deleting the extension from. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5f110-106">**Recurso admitido**</span><span class="sxs-lookup"><span data-stu-id="5f110-106">**Supported resource**</span></span>|<span data-ttu-id="5f110-107">**Permiso**</span><span class="sxs-lookup"><span data-stu-id="5f110-107">**Permission**</span></span>|<span data-ttu-id="5f110-108">**Recurso admitido**</span><span class="sxs-lookup"><span data-stu-id="5f110-108">**Supported resource**</span></span>|<span data-ttu-id="5f110-109">**Permiso**</span><span class="sxs-lookup"><span data-stu-id="5f110-109">**Permission**</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="5f110-110">dispositivo</span><span class="sxs-lookup"><span data-stu-id="5f110-110">device</span></span>](../resources/device.md) | <span data-ttu-id="5f110-111">Device.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5f110-111">Device.ReadWrite.All</span></span> | [<span data-ttu-id="5f110-112">evento</span><span class="sxs-lookup"><span data-stu-id="5f110-112">event</span></span>](../resources/event.md) | <span data-ttu-id="5f110-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5f110-113">Calendars.ReadWrite</span></span> |
| [<span data-ttu-id="5f110-114">grupo</span><span class="sxs-lookup"><span data-stu-id="5f110-114">group</span></span>](../resources/group.md) | <span data-ttu-id="5f110-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5f110-115">Group.ReadWrite.All</span></span> | [<span data-ttu-id="5f110-116">evento de grupo</span><span class="sxs-lookup"><span data-stu-id="5f110-116">group event</span></span>](../resources/event.md) | <span data-ttu-id="5f110-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5f110-117">Group.ReadWrite.All</span></span> |
| [<span data-ttu-id="5f110-118">publicación de grupo</span><span class="sxs-lookup"><span data-stu-id="5f110-118">group post</span></span>](../resources/post.md) | <span data-ttu-id="5f110-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5f110-119">Group.ReadWrite.All</span></span> | [<span data-ttu-id="5f110-120">mensaje</span><span class="sxs-lookup"><span data-stu-id="5f110-120">message</span></span>](../resources/message.md) | <span data-ttu-id="5f110-121">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5f110-121">Mail.ReadWrite</span></span> |
| [<span data-ttu-id="5f110-122">organización</span><span class="sxs-lookup"><span data-stu-id="5f110-122">organization</span></span>](../resources/organization.md) | <span data-ttu-id="5f110-123">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="5f110-123">Directory.AccessAsUser.All</span></span> | [<span data-ttu-id="5f110-124">contacto personal</span><span class="sxs-lookup"><span data-stu-id="5f110-124">personal contact</span></span>](../resources/contact.md) | <span data-ttu-id="5f110-125">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5f110-125">Contacts.ReadWrite</span></span> |
| [<span data-ttu-id="5f110-126">usuario</span><span class="sxs-lookup"><span data-stu-id="5f110-126">user</span></span>](../resources/user.md) | <span data-ttu-id="5f110-127">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="5f110-127">Directory.AccessAsUser.All</span></span> | | |

## <a name="http-request"></a><span data-ttu-id="5f110-128">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5f110-128">HTTP request</span></span>
<span data-ttu-id="5f110-129">En la solicitud, identifique la instancia de recurso, utilice la propiedad de navegación **extensiones** de esa instancia para identificar y realizar un `DELETE` en esa instancia de extensión.</span><span class="sxs-lookup"><span data-stu-id="5f110-129">In the request, identify the resource instance, use the **extensions** navigation property of that instance to identify the extension, and do a `DELETE` on that extension instance.</span></span>

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

><span data-ttu-id="5f110-p102">**Nota:** La sintaxis anterior muestra algunas formas comunes para identificar una instancia del recurso, con el fin de eliminar una extensión de él. Todas las otras formas de sintaxis que le permiten identificar estas instancias de recursos admiten la eliminación de extensiones abiertas de ellas de una manera similar.</span><span class="sxs-lookup"><span data-stu-id="5f110-p102">**Note:** The above syntax shows some common ways to identify a resource instance, in order to delete an extension from it. All other syntax that allows you to identify these resource instances supports deleting open extensions from them in a similar way.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f110-132">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f110-132">Parameters</span></span>
|<span data-ttu-id="5f110-133">**Parámetro**</span><span class="sxs-lookup"><span data-stu-id="5f110-133">**Parameter**</span></span>|<span data-ttu-id="5f110-134">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5f110-134">**Type**</span></span>|<span data-ttu-id="5f110-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f110-135">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5f110-136">_Parámetros de dirección URL_</span><span class="sxs-lookup"><span data-stu-id="5f110-136">_URL parameters_</span></span>|
|<span data-ttu-id="5f110-137">id</span><span class="sxs-lookup"><span data-stu-id="5f110-137">id</span></span>|<span data-ttu-id="5f110-138">string</span><span class="sxs-lookup"><span data-stu-id="5f110-138">string</span></span>|<span data-ttu-id="5f110-p103">Un identificador único para una instancia en la colección correspondiente. Necesario.</span><span class="sxs-lookup"><span data-stu-id="5f110-p103">A unique identifier for an instance in the corresponding collection. Required.</span></span>|
|<span data-ttu-id="5f110-141">extensionId</span><span class="sxs-lookup"><span data-stu-id="5f110-141">extensionId</span></span>|<span data-ttu-id="5f110-142">string</span><span class="sxs-lookup"><span data-stu-id="5f110-142">string</span></span>|<span data-ttu-id="5f110-p104">Puede ser un nombre de extensión, que es un identificador de texto único de la extensión, o un nombre completo que concatena el tipo de extensión y un identificador de texto único. Se devuelve el nombre completo de la propiedad `id` al crear la extensión. Necesario.</span><span class="sxs-lookup"><span data-stu-id="5f110-p104">This can be an extension name which is a unique text identifier for the extension, or a fully qualified name which concatenates the extension type and unique text identifier. The fully qualified name is returned in the `id` property when you create the extension. Required.</span></span>|


## <a name="request-headers"></a><span data-ttu-id="5f110-146">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5f110-146">Request headers</span></span>
| <span data-ttu-id="5f110-147">Nombre</span><span class="sxs-lookup"><span data-stu-id="5f110-147">Name</span></span>       | <span data-ttu-id="5f110-148">Valor</span><span class="sxs-lookup"><span data-stu-id="5f110-148">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="5f110-149">Authorization</span><span class="sxs-lookup"><span data-stu-id="5f110-149">Authorization</span></span> | <span data-ttu-id="5f110-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5f110-p105">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="5f110-152">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5f110-152">Request body</span></span>
<span data-ttu-id="5f110-153">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5f110-153">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5f110-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f110-154">Response</span></span>

<span data-ttu-id="5f110-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f110-p106">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5f110-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5f110-157">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5f110-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5f110-158">Request</span></span>
<span data-ttu-id="5f110-159">El primer ejemplo hace referencia a una extensión por su nombre y elimina la extensión en el mensaje especificado.</span><span class="sxs-lookup"><span data-stu-id="5f110-159">The first example references an extension by its name and deletes the extension in the specified message.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_opentypeextension"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions('Com.Contoso.Referral')
```

<span data-ttu-id="5f110-160">El segundo ejemplo elimina una extensión en el evento de grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="5f110-160">The second example deletes an extension in the specified group event.</span></span>

<!-- { "blockType": "ignored" } -->
```http
DELETE https://graph.microsoft.com/v1.0/groups('f5480dfd-7d77-4d0b-ba2e-3391953cc74a')/events('AAMkADVlN17IsAAA=')/extensions('Com.Contoso.Referral')
```

 

##### <a name="response"></a><span data-ttu-id="5f110-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f110-161">Response</span></span>
<span data-ttu-id="5f110-162">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f110-162">Here is an example of the response.</span></span>
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
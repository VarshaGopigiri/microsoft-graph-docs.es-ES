# <a name="delete-open-extension"></a><span data-ttu-id="f9dfd-101">Eliminar extensión abierta</span><span class="sxs-lookup"><span data-stu-id="f9dfd-101">Delete open extension</span></span>

<span data-ttu-id="f9dfd-102">Elimine una extensión abierta (objeto [openTypeExtension](../resources/openTypeExtension.md)) de la instancia especificada de un recurso.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-102">Delete an open extension ([openTypeExtension](../resources/openTypeExtension.md) object) from the specified instance of a resource.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="f9dfd-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f9dfd-103">Prerequisites</span></span>

<span data-ttu-id="f9dfd-104">Según el recurso desde el que elimine la extensión, se requiere uno de los siguientes **permisos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="f9dfd-104">One of the following **permissions** is required to execute this API, depending on the resource you're deleting the extension from:</span></span>

|<span data-ttu-id="f9dfd-105">**Recurso admitido**</span><span class="sxs-lookup"><span data-stu-id="f9dfd-105">**Supported resource**</span></span>|<span data-ttu-id="f9dfd-106">**Permiso**</span><span class="sxs-lookup"><span data-stu-id="f9dfd-106">**Permission**</span></span>|<span data-ttu-id="f9dfd-107">**Recurso admitido**</span><span class="sxs-lookup"><span data-stu-id="f9dfd-107">**Supported resource**</span></span>|<span data-ttu-id="f9dfd-108">**Permiso**</span><span class="sxs-lookup"><span data-stu-id="f9dfd-108">**Permission**</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="f9dfd-109">device</span><span class="sxs-lookup"><span data-stu-id="f9dfd-109">device</span></span>](../resources/device.md) | <span data-ttu-id="f9dfd-110">_Device.ReadWrite.All_</span><span class="sxs-lookup"><span data-stu-id="f9dfd-110">_Device.ReadWrite.All_</span></span> | [<span data-ttu-id="f9dfd-111">event</span><span class="sxs-lookup"><span data-stu-id="f9dfd-111">Event</span></span>](../resources/event.md) | <span data-ttu-id="f9dfd-112">_Calendars.ReadWrite_</span><span class="sxs-lookup"><span data-stu-id="f9dfd-112">_Calendars.ReadWrite_</span></span> |
| [<span data-ttu-id="f9dfd-113">group</span><span class="sxs-lookup"><span data-stu-id="f9dfd-113">group</span></span>](../resources/group.md) | <span data-ttu-id="f9dfd-114">_Group.ReadWrite.All_</span><span class="sxs-lookup"><span data-stu-id="f9dfd-114">_Group.ReadWrite.All_</span></span> | [<span data-ttu-id="f9dfd-115">group event</span><span class="sxs-lookup"><span data-stu-id="f9dfd-115">group event</span></span>](../resources/event.md) | <span data-ttu-id="f9dfd-116">_Group.ReadWrite.All_</span><span class="sxs-lookup"><span data-stu-id="f9dfd-116">_Group.ReadWrite.All_</span></span> |
| [<span data-ttu-id="f9dfd-117">group post</span><span class="sxs-lookup"><span data-stu-id="f9dfd-117">group post</span></span>](../resources/post.md) | <span data-ttu-id="f9dfd-118">_Group.ReadWrite.All_</span><span class="sxs-lookup"><span data-stu-id="f9dfd-118">_Group.ReadWrite.All_</span></span> | [<span data-ttu-id="f9dfd-119">mensaje</span><span class="sxs-lookup"><span data-stu-id="f9dfd-119">message</span></span>](../resources/message.md) | <span data-ttu-id="f9dfd-120">_Mail.ReadWrite_</span><span class="sxs-lookup"><span data-stu-id="f9dfd-120">_Mail.ReadWrite_</span></span> |
| [<span data-ttu-id="f9dfd-121">organization</span><span class="sxs-lookup"><span data-stu-id="f9dfd-121">organization</span></span>](../resources/organization.md) | <span data-ttu-id="f9dfd-122">_Directory.AccessAsUser.All_</span><span class="sxs-lookup"><span data-stu-id="f9dfd-122">_Directory.AccessAsUser.All_</span></span> | [<span data-ttu-id="f9dfd-123">personal contact</span><span class="sxs-lookup"><span data-stu-id="f9dfd-123">personal contact</span></span>](../resources/contact.md) | <span data-ttu-id="f9dfd-124">_Contacts.ReadWrite_</span><span class="sxs-lookup"><span data-stu-id="f9dfd-124">_Contacts.ReadWrite_</span></span> |
| [<span data-ttu-id="f9dfd-125">user</span><span class="sxs-lookup"><span data-stu-id="f9dfd-125">User</span></span>](../resources/user.md) | <span data-ttu-id="f9dfd-126">_Directory.AccessAsUser.All_</span><span class="sxs-lookup"><span data-stu-id="f9dfd-126">_Directory.AccessAsUser.All_</span></span> | | |

 
## <a name="http-request"></a><span data-ttu-id="f9dfd-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f9dfd-127">HTTP request</span></span>
<span data-ttu-id="f9dfd-128">En la solicitud, identifique la instancia de recurso, utilice la propiedad de navegación **extensiones** de esa instancia para identificar y realizar un `DELETE` en esa instancia de extensión.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-128">In the request, identify the resource instance, use the **extensions** navigation property of that instance to identify the extension, and do a `DELETE` on that extension instance.</span></span>

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

><span data-ttu-id="f9dfd-p101">**Nota:** La sintaxis anterior muestra algunas formas comunes para identificar una instancia del recurso, con el fin de eliminar una extensión de él. Todas las otras formas de sintaxis que le permiten identificar estas instancias de recursos admiten la eliminación de extensiones abiertas de ellas de una manera similar.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-p101">**Note:** The above syntax shows some common ways to identify a resource instance, in order to delete an extension from it. All other syntax that allows you to identify these resource instances supports deleting open extensions from them in a similar way.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9dfd-131">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9dfd-131">Parameters</span></span>
|<span data-ttu-id="f9dfd-132">**Parámetro**</span><span class="sxs-lookup"><span data-stu-id="f9dfd-132">**Parameter**</span></span>|<span data-ttu-id="f9dfd-133">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f9dfd-133">**Type**</span></span>|<span data-ttu-id="f9dfd-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f9dfd-134">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f9dfd-135">_Parámetros de dirección URL_</span><span class="sxs-lookup"><span data-stu-id="f9dfd-135">_URL parameters_</span></span>|
|<span data-ttu-id="f9dfd-136">id</span><span class="sxs-lookup"><span data-stu-id="f9dfd-136">id</span></span>|<span data-ttu-id="f9dfd-137">string</span><span class="sxs-lookup"><span data-stu-id="f9dfd-137">string</span></span>|<span data-ttu-id="f9dfd-p102">Un identificador único para una instancia en la colección correspondiente. Necesario.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-p102">A unique identifier for an instance in the corresponding collection. Required.</span></span>|
|<span data-ttu-id="f9dfd-140">extensionId</span><span class="sxs-lookup"><span data-stu-id="f9dfd-140">extensionId</span></span>|<span data-ttu-id="f9dfd-141">string</span><span class="sxs-lookup"><span data-stu-id="f9dfd-141">string</span></span>|<span data-ttu-id="f9dfd-p103">Puede ser un nombre de extensión, que es un identificador de texto único de la extensión, o un nombre completo que concatena el tipo de extensión y un identificador de texto único. Se devuelve el nombre completo de la propiedad `id` al crear la extensión. Necesario.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-p103">This can be an extension name which is a unique text identifier for the extension, or a fully qualified name which concatenates the extension type and unique text identifier. The fully qualified name is returned in the `id` property when you create the extension. Required.</span></span>|


## <a name="request-headers"></a><span data-ttu-id="f9dfd-145">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f9dfd-145">Request headers</span></span>
| <span data-ttu-id="f9dfd-146">Nombre</span><span class="sxs-lookup"><span data-stu-id="f9dfd-146">Name</span></span>       | <span data-ttu-id="f9dfd-147">Valor</span><span class="sxs-lookup"><span data-stu-id="f9dfd-147">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="f9dfd-148">Authorization</span><span class="sxs-lookup"><span data-stu-id="f9dfd-148">Authorization</span></span> | <span data-ttu-id="f9dfd-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-p104">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="f9dfd-151">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f9dfd-151">Request body</span></span>
<span data-ttu-id="f9dfd-152">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-152">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f9dfd-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9dfd-153">Response</span></span>

<span data-ttu-id="f9dfd-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-p105">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f9dfd-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9dfd-156">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f9dfd-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f9dfd-157">Request</span></span>
<span data-ttu-id="f9dfd-158">El primer ejemplo hace referencia a una extensión por su nombre y elimina la extensión en el mensaje especificado.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-158">The first example references an extension by its name and deletes the extension in the specified message.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_opentypeextension"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions('Com.Contoso.Referral')
```

<span data-ttu-id="f9dfd-159">El segundo ejemplo elimina una extensión en el evento de grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-159">The second example deletes an extension in the specified group event.</span></span>

<!-- { "blockType": "ignored" } -->
```http
DELETE https://graph.microsoft.com/v1.0/groups('f5480dfd-7d77-4d0b-ba2e-3391953cc74a')/events('AAMkADVlN17IsAAA=')/extensions('Com.Contoso.Referral')
```

 

##### <a name="response"></a><span data-ttu-id="f9dfd-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9dfd-160">Response</span></span>
<span data-ttu-id="f9dfd-161">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-161">Here is an example of the response.</span></span>
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
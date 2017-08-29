# <a name="delete-contact"></a><span data-ttu-id="60ec8-101">Eliminar contact</span><span class="sxs-lookup"><span data-stu-id="60ec8-101">Delete contact</span></span>

<span data-ttu-id="60ec8-102">Elimina un contacto.</span><span class="sxs-lookup"><span data-stu-id="60ec8-102">Delete a contact.</span></span>
## <a name="permissions"></a><span data-ttu-id="60ec8-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="60ec8-103">Permissions</span></span>
<span data-ttu-id="60ec8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="60ec8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="60ec8-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="60ec8-106">Permission type</span></span>      | <span data-ttu-id="60ec8-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="60ec8-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="60ec8-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="60ec8-108">Delegated (work or school account)</span></span> | <span data-ttu-id="60ec8-109">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="60ec8-109">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="60ec8-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="60ec8-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="60ec8-111">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="60ec8-111">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="60ec8-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="60ec8-112">Application</span></span> | <span data-ttu-id="60ec8-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="60ec8-113">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="60ec8-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="60ec8-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="60ec8-115">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="60ec8-115">A [contact](../resources/contact.md) from a user's default [contactFolder](../resources/contactfolder.md).</span></span>
```http
DELETE /me/contacts/{id}
DELETE /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="60ec8-116">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.</span><span class="sxs-lookup"><span data-stu-id="60ec8-116">A [contact](../resources/contact.md) from a user's top level [contactFolder](../resources/contactfolder.md).</span></span>
```http
DELETE /me/contactFolders/{id}/contacts/{id}
DELETE /users/{id | userPrincipalName}/contactFolders/{id}/contacts/{id}
```
<span data-ttu-id="60ec8-p102">Un [contact](../resources/contact.md) contenido en una carpeta secundaria de una [contactFolder](../resources/mailfolder.md). En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="60ec8-p102">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md). The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
DELETE /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
DELETE /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="request-headers"></a><span data-ttu-id="60ec8-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="60ec8-119">Request headers</span></span>
| <span data-ttu-id="60ec8-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60ec8-120">Header</span></span>       | <span data-ttu-id="60ec8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="60ec8-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="60ec8-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="60ec8-122">Authorization</span></span>  | <span data-ttu-id="60ec8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="60ec8-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="60ec8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="60ec8-125">Request body</span></span>
<span data-ttu-id="60ec8-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="60ec8-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="60ec8-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60ec8-127">Response</span></span>

<span data-ttu-id="60ec8-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="60ec8-p104">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="60ec8-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="60ec8-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="60ec8-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="60ec8-131">Request</span></span>
<span data-ttu-id="60ec8-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="60ec8-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_contact"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/contacts/{id}
```
##### <a name="response"></a><span data-ttu-id="60ec8-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60ec8-133">Response</span></span>
<span data-ttu-id="60ec8-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="60ec8-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete contact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

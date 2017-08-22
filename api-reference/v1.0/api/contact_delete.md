# <a name="delete-contact"></a><span data-ttu-id="0265d-101">Eliminar contact</span><span class="sxs-lookup"><span data-stu-id="0265d-101">Delete contact</span></span>

<span data-ttu-id="0265d-102">Elimina un contacto.</span><span class="sxs-lookup"><span data-stu-id="0265d-102">Delete a contact.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0265d-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0265d-103">Prerequisites</span></span>
<span data-ttu-id="0265d-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Contacts.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="0265d-104">One of the following **scopes** is required to execute this API: *Contacts.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="0265d-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0265d-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="0265d-106">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="0265d-106">A [contact](../resources/contact.md) from a user's default [contactFolder](../resources/contactfolder.md).</span></span>
```http
DELETE /me/contacts/{id}
DELETE /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="0265d-107">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.</span><span class="sxs-lookup"><span data-stu-id="0265d-107">A [contact](../resources/contact.md) from a user's top level [contactFolder](../resources/contactfolder.md).</span></span>
```http
DELETE /me/contactFolders/{id}/contacts/{id}
DELETE /users/{id | userPrincipalName}/contactFolders/{id}/contacts/{id}
```
<span data-ttu-id="0265d-p101">Un [contact](../resources/contact.md) contenido en una carpeta secundaria de una [contactFolder](../resources/mailfolder.md). En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="0265d-p101">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md). The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
DELETE /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
DELETE /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="request-headers"></a><span data-ttu-id="0265d-110">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0265d-110">Request headers</span></span>
| <span data-ttu-id="0265d-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0265d-111">Header</span></span>       | <span data-ttu-id="0265d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="0265d-112">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="0265d-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="0265d-113">Authorization</span></span>  | <span data-ttu-id="0265d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0265d-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="0265d-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0265d-116">Request body</span></span>
<span data-ttu-id="0265d-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0265d-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0265d-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0265d-118">Response</span></span>

<span data-ttu-id="0265d-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0265d-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0265d-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0265d-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0265d-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0265d-122">Request</span></span>
<span data-ttu-id="0265d-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0265d-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_contact"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/contacts/{id}
```
##### <a name="response"></a><span data-ttu-id="0265d-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0265d-124">Response</span></span>
<span data-ttu-id="0265d-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0265d-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

# <a name="create-contact"></a><span data-ttu-id="68473-101">Create Contact</span><span class="sxs-lookup"><span data-stu-id="68473-101">Create Contact</span></span>

<span data-ttu-id="68473-102">Agrega un contacto a la carpeta de contactos raíz o al extremo de `contacts` de otra carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="68473-102">Add a contact to the root Contacts folder or to the `contacts` endpoint of another contact folder.</span></span>
## <a name="permissions"></a><span data-ttu-id="68473-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="68473-103">Permissions</span></span>
<span data-ttu-id="68473-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="68473-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="68473-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="68473-106">Permission type</span></span>      | <span data-ttu-id="68473-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="68473-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="68473-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="68473-108">Delegated (work or school account)</span></span> | <span data-ttu-id="68473-109">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="68473-109">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="68473-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="68473-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="68473-111">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="68473-111">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="68473-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="68473-112">Application</span></span> | <span data-ttu-id="68473-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="68473-113">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="68473-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="68473-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/contacts
POST /users/{id | userPrincipalName}/contacts

POST /me/contactFolders/{id}/contacts
POST /users/{id | userPrincipalName}/contactFolders/{id}/contacts
```
## <a name="request-headers"></a><span data-ttu-id="68473-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="68473-115">Request headers</span></span>
## <a name="request-headers"></a><span data-ttu-id="68473-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="68473-116">Request headers</span></span>
| <span data-ttu-id="68473-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68473-117">Header</span></span>       | <span data-ttu-id="68473-118">Valor</span><span class="sxs-lookup"><span data-stu-id="68473-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="68473-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="68473-119">Authorization</span></span>  | <span data-ttu-id="68473-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="68473-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="68473-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="68473-122">Content-Type</span></span>  | <span data-ttu-id="68473-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="68473-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="68473-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="68473-125">Request body</span></span>
<span data-ttu-id="68473-126">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Contact](../resources/contact.md).</span><span class="sxs-lookup"><span data-stu-id="68473-126">In the request body, supply a JSON representation of [Contact](../resources/contact.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="68473-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68473-127">Response</span></span>

<span data-ttu-id="68473-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [Contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68473-128">If successful, this method returns `201, Created` response code and [Contact](../resources/contact.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="68473-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="68473-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="68473-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="68473-130">Request</span></span>
<span data-ttu-id="68473-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="68473-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_contact_from_contactfolder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/contactFolders/{id}/contacts
Content-type: application/json
Content-length: 210

{
  "parentFolderId": "parentFolderId-value",
  "birthday": "datetime-value",
  "fileAs": "fileAs-value",
  "displayName": "displayName-value",
  "givenName": "givenName-value",
  "initials": "initials-value"
}
```
<span data-ttu-id="68473-132">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [contact](../resources/contact.md).</span><span class="sxs-lookup"><span data-stu-id="68473-132">In the request body, supply a JSON representation of [contact](../resources/contact.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="68473-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68473-133">Response</span></span>
<span data-ttu-id="68473-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="68473-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 210

{
  "parentFolderId": "parentFolderId-value",
  "birthday": "datetime-value",
  "fileAs": "fileAs-value",
  "displayName": "displayName-value",
  "givenName": "givenName-value",
  "initials": "initials-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Contact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
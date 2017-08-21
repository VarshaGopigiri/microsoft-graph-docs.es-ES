# <a name="delete-directoryobject"></a><span data-ttu-id="51926-101">Delete directoryObject</span><span class="sxs-lookup"><span data-stu-id="51926-101">Delete directoryObject</span></span>

<span data-ttu-id="51926-102">Eliminar un directoryObject.</span><span class="sxs-lookup"><span data-stu-id="51926-102">Deletes a directoryObject.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="51926-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="51926-103">Prerequisites</span></span>
<span data-ttu-id="51926-104">Se requieren los siguientes **ámbitos** para ejecutar esta API: _Directory.AccessAsUser.All_</span><span class="sxs-lookup"><span data-stu-id="51926-104">The following **scopes** is required to execute this API: _Directory.AccessAsUser.All_</span></span>

<span data-ttu-id="51926-p101">**NOTA:** Los usuarios, grupos y contactos son tipos de objeto de Active Directory. Por tanto, si tiene que eliminar usuarios, puede y debe usarse el siguiente **ámbito**: _User.ReadWrite.All_</span><span class="sxs-lookup"><span data-stu-id="51926-p101">**NOTE:** Users, groups, and contacts are types of directory object. As a result,if you need to delete users, the following **scope** can and should be used: _User.ReadWrite.All_</span></span>
## <a name="http-request"></a><span data-ttu-id="51926-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="51926-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /directoryObjects/{id}

```
## <a name="request-headers"></a><span data-ttu-id="51926-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="51926-108">Request headers</span></span>
| <span data-ttu-id="51926-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="51926-109">Name</span></span>       | <span data-ttu-id="51926-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="51926-110">Type</span></span> | <span data-ttu-id="51926-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="51926-111">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="51926-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="51926-112">Authorization</span></span>  | <span data-ttu-id="51926-113">string</span><span class="sxs-lookup"><span data-stu-id="51926-113">string</span></span>  | <span data-ttu-id="51926-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="51926-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="51926-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="51926-116">Request body</span></span>
<span data-ttu-id="51926-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="51926-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="51926-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51926-118">Response</span></span>

<span data-ttu-id="51926-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="51926-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="51926-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="51926-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="51926-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="51926-122">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_directoryobject"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/directoryObject/{id}
```
##### <a name="response"></a><span data-ttu-id="51926-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51926-123">Response</span></span>

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
  "description": "Delete directoryObject",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
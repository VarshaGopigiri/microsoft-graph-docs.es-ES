# <a name="delete-messagerule"></a><span data-ttu-id="9b8cb-101">Eliminar messageRule</span><span class="sxs-lookup"><span data-stu-id="9b8cb-101">Delete messageRule</span></span>


<span data-ttu-id="9b8cb-102">Eliminar el objeto [messageRule](../resources/messagerule.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-102">Delete the specified [messageRule](../resources/messagerule.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="9b8cb-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="9b8cb-103">Permissions</span></span>
<span data-ttu-id="9b8cb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9b8cb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9b8cb-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b8cb-106">Permission type</span></span>      | <span data-ttu-id="9b8cb-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b8cb-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9b8cb-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b8cb-108">Delegated (work or school account)</span></span> | <span data-ttu-id="9b8cb-109">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9b8cb-109">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="9b8cb-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b8cb-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9b8cb-111">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9b8cb-111">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="9b8cb-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b8cb-112">Application</span></span> | <span data-ttu-id="9b8cb-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9b8cb-113">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="9b8cb-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b8cb-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/mailFolders/inbox/messagerules/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/inbox/messagerules/{id}
```
## <a name="request-headers"></a><span data-ttu-id="9b8cb-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b8cb-115">Request headers</span></span>
| <span data-ttu-id="9b8cb-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="9b8cb-116">Name</span></span>       | <span data-ttu-id="9b8cb-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b8cb-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="9b8cb-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="9b8cb-118">Authorization</span></span>  | <span data-ttu-id="9b8cb-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="9b8cb-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b8cb-121">Request body</span></span>
<span data-ttu-id="9b8cb-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-122">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="9b8cb-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b8cb-123">Response</span></span>
<span data-ttu-id="9b8cb-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9b8cb-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b8cb-126">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9b8cb-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b8cb-127">Request</span></span>
<span data-ttu-id="9b8cb-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_messagerule"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/mailfolders/inbox/messagerules('AQAAAJ5dZp8=')

```
##### <a name="response"></a><span data-ttu-id="9b8cb-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b8cb-129">Response</span></span>
<span data-ttu-id="9b8cb-130">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-130">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "isEmpty": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete rule",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
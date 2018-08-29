# <a name="delete-messagerule"></a><span data-ttu-id="e3549-101">Eliminar messageRule</span><span class="sxs-lookup"><span data-stu-id="e3549-101">Delete messageRule</span></span>


<span data-ttu-id="e3549-102">Eliminar el objeto [messageRule](../resources/messagerule.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="e3549-102">Delete the specified [messageRule](../resources/messagerule.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="e3549-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="e3549-103">Permissions</span></span>
<span data-ttu-id="e3549-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e3549-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e3549-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e3549-106">Permission type</span></span>      | <span data-ttu-id="e3549-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e3549-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e3549-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e3549-108">Delegated (work or school account)</span></span> | <span data-ttu-id="e3549-109">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e3549-109">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="e3549-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e3549-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e3549-111">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e3549-111">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="e3549-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e3549-112">Application</span></span> | <span data-ttu-id="e3549-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e3549-113">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="e3549-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e3549-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/mailFolders/inbox/messageRules/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/inbox/messageRules/{id}
```
## <a name="request-headers"></a><span data-ttu-id="e3549-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e3549-115">Request headers</span></span>
| <span data-ttu-id="e3549-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="e3549-116">Name</span></span>       | <span data-ttu-id="e3549-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3549-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e3549-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="e3549-118">Authorization</span></span>  | <span data-ttu-id="e3549-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e3549-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="e3549-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e3549-121">Request body</span></span>
<span data-ttu-id="e3549-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e3549-122">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="e3549-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3549-123">Response</span></span>
<span data-ttu-id="e3549-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e3549-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e3549-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e3549-126">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e3549-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e3549-127">Request</span></span>
<span data-ttu-id="e3549-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e3549-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["inbox", "AQAAAJ5dZp8="],
  "name": "delete_messagerule"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messageRules/AQAAAJ5dZp8=

```
##### <a name="response"></a><span data-ttu-id="e3549-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3549-129">Response</span></span>
<span data-ttu-id="e3549-130">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e3549-130">Here is an example of the response.</span></span> 
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
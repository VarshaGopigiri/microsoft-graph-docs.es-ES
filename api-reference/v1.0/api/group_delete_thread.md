# <a name="delete-conversation-thread"></a><span data-ttu-id="79ee4-101">Eliminar hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="79ee4-101">Delete conversation thread</span></span>
<span data-ttu-id="79ee4-102">Elimina un objeto de [conversación](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="79ee4-102">Delete a [thread](../resources/conversationthread.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="79ee4-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="79ee4-103">Permissions</span></span>
<span data-ttu-id="79ee4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="79ee4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="79ee4-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="79ee4-106">Permission type</span></span>      | <span data-ttu-id="79ee4-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="79ee4-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="79ee4-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="79ee4-108">Delegated (work or school account)</span></span> | <span data-ttu-id="79ee4-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="79ee4-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="79ee4-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="79ee4-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="79ee4-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="79ee4-111">Not supported.</span></span>    |
|<span data-ttu-id="79ee4-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="79ee4-112">Application</span></span> | <span data-ttu-id="79ee4-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="79ee4-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="79ee4-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="79ee4-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/threads/{id}
```

## <a name="request-headers"></a><span data-ttu-id="79ee4-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="79ee4-115">Request headers</span></span>
| <span data-ttu-id="79ee4-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="79ee4-116">Name</span></span>       | <span data-ttu-id="79ee4-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="79ee4-117">Type</span></span> | <span data-ttu-id="79ee4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="79ee4-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="79ee4-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="79ee4-119">Authorization</span></span>  | <span data-ttu-id="79ee4-120">string</span><span class="sxs-lookup"><span data-stu-id="79ee4-120">string</span></span>  | <span data-ttu-id="79ee4-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="79ee4-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="79ee4-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="79ee4-123">Request body</span></span>
<span data-ttu-id="79ee4-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="79ee4-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="79ee4-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79ee4-125">Response</span></span>
<span data-ttu-id="79ee4-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79ee4-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="79ee4-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="79ee4-128">Example</span></span>
#### <a name="request"></a><span data-ttu-id="79ee4-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="79ee4-129">Request</span></span>
<span data-ttu-id="79ee4-130">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="79ee4-130">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_group_thread"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/threads/AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q==
```

#### <a name="response"></a><span data-ttu-id="79ee4-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79ee4-131">Response</span></span>
<span data-ttu-id="79ee4-132">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79ee4-132">Here is an example of the response.</span></span> 
><span data-ttu-id="79ee4-133">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="79ee4-133">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="79ee4-134">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="79ee4-134">All the properties will be returned from an actual call.</span></span>
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
  "description": "Delete conversation thread",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
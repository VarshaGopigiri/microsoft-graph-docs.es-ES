# <a name="delete-conversation-thread"></a><span data-ttu-id="8aa85-101">Eliminar hilo de conversación</span><span class="sxs-lookup"><span data-stu-id="8aa85-101">Delete conversation thread</span></span>
<span data-ttu-id="8aa85-102">Elimina un objeto de [conversación](../resources/conversationthread.md).</span><span class="sxs-lookup"><span data-stu-id="8aa85-102">Delete a [thread](../resources/conversationthread.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="8aa85-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="8aa85-103">Permissions</span></span>
<span data-ttu-id="8aa85-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8aa85-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8aa85-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8aa85-106">Permission type</span></span>      | <span data-ttu-id="8aa85-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8aa85-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8aa85-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8aa85-108">Delegated (work or school account)</span></span> | <span data-ttu-id="8aa85-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8aa85-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="8aa85-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8aa85-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8aa85-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8aa85-111">Not supported.</span></span>    |
|<span data-ttu-id="8aa85-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8aa85-112">Application</span></span> | <span data-ttu-id="8aa85-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8aa85-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="8aa85-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8aa85-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/threads/{id}
```

## <a name="request-headers"></a><span data-ttu-id="8aa85-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8aa85-115">Request headers</span></span>
| <span data-ttu-id="8aa85-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="8aa85-116">Name</span></span>       | <span data-ttu-id="8aa85-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="8aa85-117">Type</span></span> | <span data-ttu-id="8aa85-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="8aa85-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="8aa85-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="8aa85-119">Authorization</span></span>  | <span data-ttu-id="8aa85-120">cadena</span><span class="sxs-lookup"><span data-stu-id="8aa85-120">string</span></span>  | <span data-ttu-id="8aa85-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8aa85-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8aa85-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8aa85-123">Request body</span></span>
<span data-ttu-id="8aa85-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8aa85-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8aa85-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8aa85-125">Response</span></span>
<span data-ttu-id="8aa85-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8aa85-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8aa85-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8aa85-128">Example</span></span>
#### <a name="request"></a><span data-ttu-id="8aa85-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8aa85-129">Request</span></span>
<span data-ttu-id="8aa85-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8aa85-130">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["02bd9fd6-8f93-4758-87c3-1fb73740a315", "AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q=="],
  "name": "delete_group_thread"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/threads/AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q==
```

#### <a name="response"></a><span data-ttu-id="8aa85-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8aa85-131">Response</span></span>
<span data-ttu-id="8aa85-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8aa85-132">The following is an example of the response.</span></span> 
><span data-ttu-id="8aa85-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8aa85-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
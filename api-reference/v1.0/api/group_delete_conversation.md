# <a name="delete-conversation"></a><span data-ttu-id="ca353-101">Eliminar conversación</span><span class="sxs-lookup"><span data-stu-id="ca353-101">Delete conversation</span></span>
<span data-ttu-id="ca353-102">Elimina un objeto de [conversación](../resources/conversation.md).</span><span class="sxs-lookup"><span data-stu-id="ca353-102">Delete a [conversation](../resources/conversation.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="ca353-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="ca353-103">Permissions</span></span>
<span data-ttu-id="ca353-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ca353-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ca353-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ca353-106">Permission type</span></span>      | <span data-ttu-id="ca353-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ca353-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ca353-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ca353-108">Delegated (work or school account)</span></span> | <span data-ttu-id="ca353-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ca353-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ca353-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ca353-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ca353-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ca353-111">Not supported.</span></span>    |
|<span data-ttu-id="ca353-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ca353-112">Application</span></span> | <span data-ttu-id="ca353-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ca353-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ca353-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ca353-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/conversations/{id}
```

## <a name="request-headers"></a><span data-ttu-id="ca353-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ca353-115">Request headers</span></span>
| <span data-ttu-id="ca353-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="ca353-116">Name</span></span>       | <span data-ttu-id="ca353-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="ca353-117">Type</span></span> | <span data-ttu-id="ca353-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca353-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="ca353-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="ca353-119">Authorization</span></span>  | <span data-ttu-id="ca353-120">cadena</span><span class="sxs-lookup"><span data-stu-id="ca353-120">string</span></span>  | <span data-ttu-id="ca353-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ca353-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ca353-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ca353-123">Request body</span></span>
<span data-ttu-id="ca353-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ca353-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ca353-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ca353-125">Response</span></span>
<span data-ttu-id="ca353-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ca353-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ca353-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ca353-128">Example</span></span>
#### <a name="request"></a><span data-ttu-id="ca353-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ca353-129">Request</span></span>
<span data-ttu-id="ca353-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ca353-130">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["02bd9fd6-8f93-4758-87c3-1fb73740a315", "AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgAQABuXO3guDWBMpyKF7LsVwfU="],
  "name": "delete_group_conversation"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/conversations/AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgAQABuXO3guDWBMpyKF7LsVwfU=
```

#### <a name="response"></a><span data-ttu-id="ca353-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ca353-131">Response</span></span>
<span data-ttu-id="ca353-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ca353-132">The following is an example of the response.</span></span> 
><span data-ttu-id="ca353-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ca353-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
  "description": "Delete conversation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
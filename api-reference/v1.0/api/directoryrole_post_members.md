<span data-ttu-id="52bbb-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="52bbb-p101">Bearer {token}. Required.</span></span>  | {token} de portador. Obligatorio. |
| <span data-ttu-id="52bbb-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="52bbb-114">Content-Type</span></span>  | <span data-ttu-id="52bbb-115">application/json</span><span class="sxs-lookup"><span data-stu-id="52bbb-115">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="52bbb-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="52bbb-116">Request body</span></span>
<span data-ttu-id="52bbb-117">En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [directoryObject](../resources/directoryobject.md) o [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="52bbb-117">In the request body, supply a JSON representation of a [directoryObject](../resources/directoryobject.md) or [user](../resources/user.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="52bbb-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52bbb-118">Response</span></span>

<span data-ttu-id="52bbb-119">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`.</span><span class="sxs-lookup"><span data-stu-id="52bbb-119">If successful, this method returns `204, No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="52bbb-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="52bbb-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="52bbb-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="52bbb-121">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_directoryrole"
}-->
```http
POST https://graph.microsoft.com/v1.0/directoryRoles/{id}/members
Content-type: application/json

{
  "@odata.id": "https://graph.microsoft.com/v1.0/directoryObjects/{id}"
}
```

##### <a name="response"></a><span data-ttu-id="52bbb-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52bbb-122">Response</span></span>
<span data-ttu-id="52bbb-123">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="52bbb-123">Note: The response object shown here may be truncated for brevity.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 204 No Content
Content-type: text/plain

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create member",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
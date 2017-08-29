# <a name="get-message"></a><span data-ttu-id="7a5bf-101">Obtener mensaje</span><span class="sxs-lookup"><span data-stu-id="7a5bf-101">Get message</span></span>

<span data-ttu-id="7a5bf-102">Recupere las propiedades y las relaciones de un objeto [message](../resources/message.md).</span><span class="sxs-lookup"><span data-stu-id="7a5bf-102">Retrieve the properties and relationships of a [message](../resources/message.md) object.</span></span>

<span data-ttu-id="7a5bf-103">Dado que el recurso **message** admite [extensiones](../../../concepts/extensibility_overview.md), también puede utilizar la operación `GET` para obtener propiedades personalizadas y datos de extensión en una instancia **message**.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-103">Since the **message** resource supports [extensions](../../../concepts/extensibility_overview.md), you can also use the `GET` operation to get custom properties and extension data in a **message** instance.</span></span>

<span data-ttu-id="7a5bf-104">Actualmente, esta operación devuelve los cuerpos de los mensajes solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-104">Currently, this operation returns message bodies in only HTML format.</span></span>

## <a name="permissions"></a><span data-ttu-id="7a5bf-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="7a5bf-105">Permissions</span></span>
<span data-ttu-id="7a5bf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7a5bf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7a5bf-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7a5bf-108">Permission type</span></span>      | <span data-ttu-id="7a5bf-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7a5bf-109">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="7a5bf-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7a5bf-110">Delegated (work or school account)</span></span> | <span data-ttu-id="7a5bf-111">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="7a5bf-111">Mail.Read</span></span>    | 
|<span data-ttu-id="7a5bf-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7a5bf-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7a5bf-113">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="7a5bf-113">Mail.Read</span></span>    | 
|<span data-ttu-id="7a5bf-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7a5bf-114">Application</span></span> | <span data-ttu-id="7a5bf-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="7a5bf-115">Mail.Read</span></span> | 

## <a name="http-request"></a><span data-ttu-id="7a5bf-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7a5bf-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}
GET /users/{id | userPrincipalName}/messages/{id}
GET /me/mailFolders/{id}/messages/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="7a5bf-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7a5bf-117">Optional query parameters</span></span>
<span data-ttu-id="7a5bf-118">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-118">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="7a5bf-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7a5bf-119">Request headers</span></span>
| <span data-ttu-id="7a5bf-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="7a5bf-120">Name</span></span>       | <span data-ttu-id="7a5bf-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a5bf-121">Type</span></span> | <span data-ttu-id="7a5bf-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a5bf-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="7a5bf-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="7a5bf-123">Authorization</span></span>  | <span data-ttu-id="7a5bf-124">string</span><span class="sxs-lookup"><span data-stu-id="7a5bf-124">string</span></span>  | <span data-ttu-id="7a5bf-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7a5bf-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7a5bf-127">Request body</span></span>
<span data-ttu-id="7a5bf-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7a5bf-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7a5bf-129">Response</span></span>

<span data-ttu-id="7a5bf-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-130">If successful, this method returns a `200 OK` response code and [message](../resources/message.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7a5bf-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7a5bf-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7a5bf-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7a5bf-132">Request</span></span>
<span data-ttu-id="7a5bf-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_message"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/{id}
```
##### <a name="response"></a><span data-ttu-id="7a5bf-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7a5bf-134">Response</span></span>
<span data-ttu-id="7a5bf-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "datetime-value",
  "sentDateTime": "datetime-value",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": "html",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value"
}
```

## <a name="see-also"></a><span data-ttu-id="7a5bf-138">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="7a5bf-138">See also</span></span>

- [<span data-ttu-id="7a5bf-139">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="7a5bf-139">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="7a5bf-140">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="7a5bf-140">Add custom data to users using open extensions (preview)</span></span>](../../../concepts/extensibility_open_users.md)
<!--
- [Add custom data to groups using schema extensions (preview)](../../../concepts/extensibility_schema_groups.md)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get message",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

# <a name="update-mailfolder"></a><span data-ttu-id="2d7d1-101">Update mailfolder</span><span class="sxs-lookup"><span data-stu-id="2d7d1-101">Update mailfolder</span></span>

<span data-ttu-id="2d7d1-102">Actualiza las propiedades del objeto mailfolder.</span><span class="sxs-lookup"><span data-stu-id="2d7d1-102">Update the properties of mailfolder object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2d7d1-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2d7d1-103">Prerequisites</span></span>
<span data-ttu-id="2d7d1-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="2d7d1-104">One of the following **scopes** is required to execute this API: *Mail.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="2d7d1-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2d7d1-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/mailFolders/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="2d7d1-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2d7d1-106">Request headers</span></span>
| <span data-ttu-id="2d7d1-107">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d7d1-107">Header</span></span>       | <span data-ttu-id="2d7d1-108">Valor</span><span class="sxs-lookup"><span data-stu-id="2d7d1-108">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="2d7d1-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="2d7d1-109">Authorization</span></span>  | <span data-ttu-id="2d7d1-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2d7d1-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="2d7d1-112">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2d7d1-112">Content-Type</span></span>  | <span data-ttu-id="2d7d1-p102">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2d7d1-p102">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="2d7d1-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2d7d1-115">Request body</span></span>
<span data-ttu-id="2d7d1-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="2d7d1-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="2d7d1-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2d7d1-119">Property</span></span>     | <span data-ttu-id="2d7d1-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d7d1-120">Type</span></span>   |<span data-ttu-id="2d7d1-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d7d1-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2d7d1-122">displayName</span><span class="sxs-lookup"><span data-stu-id="2d7d1-122">displayName</span></span>|<span data-ttu-id="2d7d1-123">String</span><span class="sxs-lookup"><span data-stu-id="2d7d1-123">String</span></span>|<span data-ttu-id="2d7d1-124">Nombre para mostrar del objeto mailFolder.</span><span class="sxs-lookup"><span data-stu-id="2d7d1-124">The mailFolder's display name.</span></span>|

## <a name="response"></a><span data-ttu-id="2d7d1-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d7d1-125">Response</span></span>

<span data-ttu-id="2d7d1-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [mailFolder](../resources/mailfolder.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2d7d1-126">If successful, this method returns a `200 OK` response code and updated [mailFolder](../resources/mailfolder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2d7d1-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2d7d1-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2d7d1-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2d7d1-128">Request</span></span>
<span data-ttu-id="2d7d1-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2d7d1-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_mailfolder"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/mailFolders/{id}
Content-type: application/json
Content-length: 159

{
  "displayName": "displayName-value",
}
```
##### <a name="response"></a><span data-ttu-id="2d7d1-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d7d1-130">Response</span></span>
<span data-ttu-id="2d7d1-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2d7d1-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailFolder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 179

{
  "displayName": "displayName-value",
  "parentFolderId": "parentFolderId-value",
  "childFolderCount": 99,
  "unreadItemCount": 99,
  "totalItemCount": 99,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update mailfolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

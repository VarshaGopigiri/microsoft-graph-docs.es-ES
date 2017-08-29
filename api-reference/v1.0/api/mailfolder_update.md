# <a name="update-mailfolder"></a><span data-ttu-id="c2df6-101">Update mailfolder</span><span class="sxs-lookup"><span data-stu-id="c2df6-101">Update mailfolder</span></span>

<span data-ttu-id="c2df6-102">Actualiza las propiedades del objeto mailfolder.</span><span class="sxs-lookup"><span data-stu-id="c2df6-102">Update the properties of mailfolder object.</span></span>
## <a name="permissions"></a><span data-ttu-id="c2df6-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="c2df6-103">Permissions</span></span>
<span data-ttu-id="c2df6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c2df6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c2df6-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c2df6-106">Permission type</span></span>      | <span data-ttu-id="c2df6-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c2df6-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c2df6-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c2df6-108">Delegated (work or school account)</span></span> | <span data-ttu-id="c2df6-109">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c2df6-109">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="c2df6-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c2df6-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c2df6-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c2df6-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="c2df6-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c2df6-112">Application</span></span> | <span data-ttu-id="c2df6-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c2df6-113">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="c2df6-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c2df6-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/mailFolders/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="c2df6-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c2df6-115">Request headers</span></span>
| <span data-ttu-id="c2df6-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2df6-116">Header</span></span>       | <span data-ttu-id="c2df6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c2df6-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c2df6-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="c2df6-118">Authorization</span></span>  | <span data-ttu-id="c2df6-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c2df6-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="c2df6-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c2df6-121">Content-Type</span></span>  | <span data-ttu-id="c2df6-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c2df6-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c2df6-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c2df6-124">Request body</span></span>
<span data-ttu-id="c2df6-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="c2df6-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="c2df6-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c2df6-128">Property</span></span>     | <span data-ttu-id="c2df6-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="c2df6-129">Type</span></span>   |<span data-ttu-id="c2df6-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2df6-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c2df6-131">displayName</span><span class="sxs-lookup"><span data-stu-id="c2df6-131">displayName</span></span>|<span data-ttu-id="c2df6-132">String</span><span class="sxs-lookup"><span data-stu-id="c2df6-132">String</span></span>|<span data-ttu-id="c2df6-133">Nombre para mostrar del objeto mailFolder.</span><span class="sxs-lookup"><span data-stu-id="c2df6-133">The mailFolder's display name.</span></span>|

## <a name="response"></a><span data-ttu-id="c2df6-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2df6-134">Response</span></span>

<span data-ttu-id="c2df6-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [mailFolder](../resources/mailfolder.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c2df6-135">If successful, this method returns a `200 OK` response code and updated [mailFolder](../resources/mailfolder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c2df6-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2df6-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c2df6-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2df6-137">Request</span></span>
<span data-ttu-id="c2df6-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c2df6-138">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="c2df6-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2df6-139">Response</span></span>
<span data-ttu-id="c2df6-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c2df6-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

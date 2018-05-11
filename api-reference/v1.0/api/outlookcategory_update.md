# <a name="update-outlook-category"></a><span data-ttu-id="a6d55-101">Actualizar categoría de Outlook</span><span class="sxs-lookup"><span data-stu-id="a6d55-101">Update Outlook category</span></span>


<span data-ttu-id="a6d55-102">Actualizar la propiedad modificable **color** del objeto [outlookCategory](../resources/outlookCategory.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="a6d55-102">Update the writable property, **color**, of the specified [outlookCategory](../resources/outlookCategory.md) object.</span></span> <span data-ttu-id="a6d55-103">No puede modificar la propiedad **displayName** después de haber creado la categoría.</span><span class="sxs-lookup"><span data-stu-id="a6d55-103">You cannot modify the **displayName** property once you have created the category.</span></span>

## <a name="permissions"></a><span data-ttu-id="a6d55-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="a6d55-104">Permissions</span></span>
<span data-ttu-id="a6d55-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a6d55-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a6d55-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a6d55-107">Permission type</span></span>      | <span data-ttu-id="a6d55-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a6d55-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a6d55-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a6d55-109">Delegated (work or school account)</span></span> | <span data-ttu-id="a6d55-110">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a6d55-110">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="a6d55-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a6d55-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a6d55-112">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a6d55-112">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="a6d55-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a6d55-113">Application</span></span> | <span data-ttu-id="a6d55-114">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a6d55-114">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="a6d55-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a6d55-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/outlook/masterCategories/{id}
PATCH /users/{id|userPrincipalName}/outlook/masterCategories/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a6d55-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a6d55-116">Optional query parameters</span></span>
<span data-ttu-id="a6d55-117">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a6d55-117">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a6d55-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a6d55-118">Request headers</span></span>
| <span data-ttu-id="a6d55-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="a6d55-119">Name</span></span>      |<span data-ttu-id="a6d55-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6d55-120">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="a6d55-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="a6d55-121">Authorization</span></span>  | <span data-ttu-id="a6d55-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a6d55-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a6d55-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a6d55-124">Request body</span></span>
<span data-ttu-id="a6d55-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="a6d55-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="a6d55-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a6d55-128">Property</span></span>     | <span data-ttu-id="a6d55-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="a6d55-129">Type</span></span>   |<span data-ttu-id="a6d55-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6d55-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a6d55-131">color</span><span class="sxs-lookup"><span data-stu-id="a6d55-131">color</span></span>|<span data-ttu-id="a6d55-132">String</span><span class="sxs-lookup"><span data-stu-id="a6d55-132">String</span></span>|<span data-ttu-id="a6d55-133">Constante de color preestablecida que caracteriza a una categoría y a la que se asigna uno de los 25 colores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="a6d55-133">A pre-set color constant that characterizes a category, and that is mapped to one of 25 predefined colors.</span></span> |

## <a name="response"></a><span data-ttu-id="a6d55-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6d55-134">Response</span></span>

<span data-ttu-id="a6d55-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [outlookCategory](../resources/outlookCategory.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a6d55-135">If successful, this method returns a `200 OK` response code and updated [contactFolder](../resources/outlookCategory.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a6d55-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a6d55-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a6d55-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a6d55-137">Request</span></span>
<span data-ttu-id="a6d55-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a6d55-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_outlookcategory"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/outlook/masterCategories('bac262b7-485d-4739-b436-e31467d64fac')
Content-type: application/json
Content-length: 30

{
  "color":"preset15"
}
```
##### <a name="response"></a><span data-ttu-id="a6d55-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6d55-139">Response</span></span>
<span data-ttu-id="a6d55-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a6d55-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookCategory"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 251

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('8ae6f565-0d7f-4ead-853e-7db94c912a1f')/outlook/masterCategories/$entity",
  "id":"bac262b7-485d-4739-b436-e31467d64fac",
  "displayName":"Project expenses",
  "color":"preset15"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update outlookCategory",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
# <a name="get-onenoteoperation"></a><span data-ttu-id="2a927-101">Obtener onenoteOperation</span><span class="sxs-lookup"><span data-stu-id="2a927-101">Get onenoteOperation</span></span>

<span data-ttu-id="2a927-p101">Obtenga el estado de una operación de larga duración de OneNote. Esto se aplica a las operaciones que devuelvan el encabezado **Operation-Location** en la respuesta, como `CopyNotebook`, `CopyToNotebook`, `CopyToSectionGroup` y `and CopyToSection`.</span><span class="sxs-lookup"><span data-stu-id="2a927-p101">Get the status of a long-running OneNote operation. This applies to operations that return the **Operation-Location** header in the response, such as `CopyNotebook`, `CopyToNotebook`, `CopyToSectionGroup`, `and CopyToSection`.</span></span>   

<span data-ttu-id="2a927-104">Puede sondear el extremo de Operation-Location hasta que la propiedad de `status` devuelva `completed` o `failed`.</span><span class="sxs-lookup"><span data-stu-id="2a927-104">You can poll the Operation-Location endpoint until the `status` property returns `completed` or `failed`.</span></span> 

<span data-ttu-id="2a927-105">Si el estado es `completed`, la propiedad de `resourceLocation` contiene el URI del extremo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2a927-105">If the status is `completed`, the `resourceLocation` property contains the resource endpoint URI.</span></span> 

<span data-ttu-id="2a927-106">Si el estado es `failed`, el error y las propiedades de `@api.diagnostics` facilitan información del error.</span><span class="sxs-lookup"><span data-stu-id="2a927-106">If the status is `failed`, the error and `@api.diagnostics` properties provide error information.</span></span>

## <a name="permissions"></a><span data-ttu-id="2a927-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="2a927-107">Permissions</span></span>
<span data-ttu-id="2a927-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2a927-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2a927-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2a927-110">Permission type</span></span>      | <span data-ttu-id="2a927-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2a927-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2a927-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2a927-112">Delegated (work or school account)</span></span> | <span data-ttu-id="2a927-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2a927-113">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="2a927-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2a927-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2a927-115">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2a927-115">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="2a927-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2a927-116">Application</span></span> | <span data-ttu-id="2a927-117">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2a927-117">Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2a927-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2a927-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/operations/{id}
GET /users/{id | userPrincipalName}/onenote/operations/{id}
GET /groups/{id}/onenote/operations/{id}
GET /sites/{id}/onenote/operations/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="2a927-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2a927-119">Optional query parameters</span></span>
<span data-ttu-id="2a927-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2a927-120">None.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2a927-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2a927-121">Request headers</span></span>
| <span data-ttu-id="2a927-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="2a927-122">Name</span></span>       | <span data-ttu-id="2a927-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a927-123">Type</span></span> | <span data-ttu-id="2a927-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a927-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="2a927-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="2a927-125">Authorization</span></span>  | <span data-ttu-id="2a927-126">string</span><span class="sxs-lookup"><span data-stu-id="2a927-126">string</span></span>  | <span data-ttu-id="2a927-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a927-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2a927-129">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2a927-129">Accept</span></span> | <span data-ttu-id="2a927-130">string</span><span class="sxs-lookup"><span data-stu-id="2a927-130">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="2a927-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2a927-131">Request body</span></span>
<span data-ttu-id="2a927-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2a927-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2a927-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2a927-133">Response</span></span>

<span data-ttu-id="2a927-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [onenoteOperation](../resources/onenoteoperation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a927-134">If successful, this method returns a `200 OK` response code and [onenoteOperation](../resources/onenoteoperation.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2a927-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2a927-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2a927-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2a927-136">Request</span></span>
<span data-ttu-id="2a927-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2a927-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_onenoteoperation"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/operations/{id}
```
##### <a name="response"></a><span data-ttu-id="2a927-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2a927-138">Response</span></span>
<span data-ttu-id="2a927-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2a927-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onenoteOperation"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 215

{
  "id": "id-value",
  "status": "status-value",
  "createdDateTime": "2016-10-19T10:37:00Z",
  "lastActionDateTime": "2016-10-19T10:37:00Z",
  "resourceLocation": "resourceLocation-value",
  "resourceId": "resourceId-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get onenoteOperation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

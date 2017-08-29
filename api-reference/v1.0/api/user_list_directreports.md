# <a name="list-directreports"></a><span data-ttu-id="caa20-101">List directReports</span><span class="sxs-lookup"><span data-stu-id="caa20-101">List directReports</span></span>

<span data-ttu-id="caa20-p101">Obtiene los subordinados directos del usuario. Devuelve los usuarios y los contactos para los que se asigna este usuario como administrador.</span><span class="sxs-lookup"><span data-stu-id="caa20-p101">Get user's direct reports. Returns the users and contacts for whom this user is assigned as manager.</span></span>
## <a name="permissions"></a><span data-ttu-id="caa20-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="caa20-104">Permissions</span></span>
<span data-ttu-id="caa20-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="caa20-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="caa20-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="caa20-107">Permission type</span></span>      | <span data-ttu-id="caa20-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="caa20-108">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="caa20-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="caa20-109">Delegated (work or school account)</span></span> | <span data-ttu-id="caa20-110">User.Read, User.ReadWrite, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="caa20-110">One of the following scopes is required to execute this API: User.Read; User.ReadWrite; User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All</span></span>    | 
|<span data-ttu-id="caa20-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="caa20-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="caa20-112">User.Read, User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="caa20-112">User.Read, User.ReadWrite</span></span>    | 
|<span data-ttu-id="caa20-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="caa20-113">Application</span></span> | <span data-ttu-id="caa20-114">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="caa20-114">One of the following scopes is required to execute this API: User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="caa20-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="caa20-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/directReports
```
## <a name="optional-query-parameters"></a><span data-ttu-id="caa20-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="caa20-116">Optional query parameters</span></span>
<span data-ttu-id="caa20-117">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="caa20-117">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="caa20-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="caa20-118">Request headers</span></span>
| <span data-ttu-id="caa20-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="caa20-119">Header</span></span>       | <span data-ttu-id="caa20-120">Valor</span><span class="sxs-lookup"><span data-stu-id="caa20-120">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="caa20-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="caa20-121">Authorization</span></span>  | <span data-ttu-id="caa20-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="caa20-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="caa20-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="caa20-124">Content-Type</span></span>   | <span data-ttu-id="caa20-125">application/json</span><span class="sxs-lookup"><span data-stu-id="caa20-125">application/json</span></span>  | 

## <a name="request-body"></a><span data-ttu-id="caa20-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="caa20-126">Request body</span></span>
<span data-ttu-id="caa20-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="caa20-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="caa20-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="caa20-128">Response</span></span>

<span data-ttu-id="caa20-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="caa20-129">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="caa20-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="caa20-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="caa20-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="caa20-131">Request</span></span>
<span data-ttu-id="caa20-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="caa20-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_directreports"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/directReports
```
##### <a name="response"></a><span data-ttu-id="caa20-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="caa20-133">Response</span></span>
<span data-ttu-id="caa20-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="caa20-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List directReports",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
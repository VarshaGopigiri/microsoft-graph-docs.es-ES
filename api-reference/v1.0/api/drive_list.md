# <a name="list-available-drives"></a><span data-ttu-id="e179e-101">List available drives</span><span class="sxs-lookup"><span data-stu-id="e179e-101">List available drives</span></span>

<span data-ttu-id="e179e-p101">Recupera la lista de recursos [Drive](../resources/drive.md) disponibles para un [User](../resources/user.md) o [Group](../resources/group.md) de destino. La aplicación también puede solicitar el conjunto de bibliotecas de documentos en el sitio de raíz de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e179e-p101">Retrieve the list of [Drive](../resources/drive.md) resources available for a target [User](../resources/user.md) or [Group](../resources/group.md). Your app can also request the set of document libraries on the SharePoint root site.</span></span>

## <a name="permissions"></a><span data-ttu-id="e179e-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="e179e-104">Permissions</span></span>

<span data-ttu-id="e179e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e179e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e179e-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e179e-107">Permission type</span></span>      | <span data-ttu-id="e179e-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e179e-108">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="e179e-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e179e-109">Delegated (work or school account)</span></span> | <span data-ttu-id="e179e-110">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e179e-110">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    | 
|<span data-ttu-id="e179e-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e179e-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e179e-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e179e-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    | 
|<span data-ttu-id="e179e-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e179e-113">Application</span></span> | <span data-ttu-id="e179e-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e179e-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="e179e-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e179e-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives
GET /me/drives
GET /sites/{site-id}/drives
```

## <a name="optional-query-parameters"></a><span data-ttu-id="e179e-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e179e-116">Optional query parameters</span></span>

<span data-ttu-id="e179e-117">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e179e-117">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-body"></a><span data-ttu-id="e179e-118">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="e179e-118">Request body</span></span>

<span data-ttu-id="e179e-119">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e179e-119">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e179e-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e179e-120">Response</span></span>

<span data-ttu-id="e179e-121">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Drive](../resources/drive.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e179e-121">If successful, this method returns a `200 OK` response code and collection of [Drive](../resources/drive.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e179e-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e179e-122">Example</span></span>

##### <a name="request"></a><span data-ttu-id="e179e-123">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e179e-123">Request</span></span>

<span data-ttu-id="e179e-124">Aquí tiene un ejemplo de la solicitud de las unidades del usuario.</span><span class="sxs-lookup"><span data-stu-id="e179e-124">Here is an example of the request for the user's drives.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_drives"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/drives
```

##### <a name="response"></a><span data-ttu-id="e179e-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e179e-125">Response</span></span>

<span data-ttu-id="e179e-126">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e179e-126">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.drive",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 579

{
  "value": [
    {
      "id": "b!t18F8ybsHUq1z3LTz8xvZqP8zaSWjkFNhsME-Fepo75dTf9vQKfeRblBZjoSQrd7",
      "driveType": "business",
      "owner": {
          "user": {
              "id": "efee1b77-fb3b-4f65-99d6-274c11914d12",
              "displayName": "Ryan Gregg"
          }
      },
      "quota": {
          "deleted": 256938,
          "remaining": 1099447353539,
          "state": "normal",
          "total": 1099511627776
      }
    }
  ]
}
```

## <a name="remarks"></a><span data-ttu-id="e179e-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e179e-127">Remarks</span></span>

<span data-ttu-id="e179e-p103">La mayoría de los usuarios solo tendrán un único recurso Drive. Puede que los grupos y algunos usuarios tengan varias unidades disponibles.</span><span class="sxs-lookup"><span data-stu-id="e179e-p103">Most users will only have a single Drive resource. Groups and some users may have multiple drive available.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List drives",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Drive/List Drives"
}-->

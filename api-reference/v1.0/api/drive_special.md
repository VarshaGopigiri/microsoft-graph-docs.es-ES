# <a name="get-a-special-folder-by-name"></a><span data-ttu-id="a494d-101">Obtener una carpeta especial por su nombre</span><span class="sxs-lookup"><span data-stu-id="a494d-101">Get a special folder by name</span></span>

<span data-ttu-id="a494d-102">Use la colección especial para acceder a una carpeta especial por su nombre.</span><span class="sxs-lookup"><span data-stu-id="a494d-102">Use the special collection to access a special folder by name.</span></span>

<span data-ttu-id="a494d-p101">Las carpetas especiales proporcionan alias simples para acceder a carpetas conocidas en OneDrive sin necesidad de buscar la carpeta por su ruta (que requeriría localización) o hacer referencia a la carpeta con un identificador. Si una carpeta especial cambia de nombre o se mueve a otra ubicación de la unidad, esta sintaxis seguirá encontrando esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="a494d-p101">Special folders provide simple aliases to access well-known folders in OneDrive without the need to look up the folder by path (which would require localization), or reference the folder with an ID. If a special folder is renamed or moved to another location within the drive, this syntax will continue to find that folder.</span></span>

<span data-ttu-id="a494d-p102">Las carpetas especiales se crean de forma automática la primera vez que una aplicación intenta escribir en una, si aún no existe. Si un usuario elimina una, se vuelve a crear al volver a escribir en ella.</span><span class="sxs-lookup"><span data-stu-id="a494d-p102">Special folders are automatically created the first time an application attempts to write to one, if it doesn't already exist. If a user deletes one, it is recreated when written to again.</span></span>

<span data-ttu-id="a494d-107">**Nota:**  Si tiene permisos de solo lectura y solicita una carpeta especial que no existe, recibirá un error `403 Forbidden`.</span><span class="sxs-lookup"><span data-stu-id="a494d-107">**Note:**  If you have read-only permissions and request a special folder that doesn't exist, you'll receive a `403 Forbidden` error.</span></span>

## <a name="permissions"></a><span data-ttu-id="a494d-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="a494d-108">Permissions</span></span>
<span data-ttu-id="a494d-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a494d-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a494d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a494d-111">Permission type</span></span>      | <span data-ttu-id="a494d-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a494d-112">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="a494d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a494d-113">Delegated (work or school account)</span></span> | <span data-ttu-id="a494d-114">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a494d-114">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    | 
|<span data-ttu-id="a494d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a494d-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a494d-116">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Files.ReadWrite.AppFolder</span><span class="sxs-lookup"><span data-stu-id="a494d-116">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Files.ReadWrite.AppFolder</span></span>    | 
|<span data-ttu-id="a494d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a494d-117">Application</span></span> | <span data-ttu-id="a494d-118">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a494d-118">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="a494d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a494d-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/special/{name}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a494d-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a494d-120">Optional query parameters</span></span>
<span data-ttu-id="a494d-121">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a494d-121">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a494d-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a494d-122">Request headers</span></span>

| <span data-ttu-id="a494d-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="a494d-123">Name</span></span>          | <span data-ttu-id="a494d-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="a494d-124">Type</span></span>   | <span data-ttu-id="a494d-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="a494d-125">Description</span></span>               |
|:--------------|:-------|:--------------------------|
| <span data-ttu-id="a494d-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="a494d-126">Authorization</span></span> | <span data-ttu-id="a494d-127">string</span><span class="sxs-lookup"><span data-stu-id="a494d-127">string</span></span> | <span data-ttu-id="a494d-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a494d-p104">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="a494d-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a494d-130">Request body</span></span>
<span data-ttu-id="a494d-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a494d-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a494d-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a494d-132">Response</span></span>

<span data-ttu-id="a494d-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [driveItem](../resources/driveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a494d-133">If successful, this method returns a `200 OK` response code and a [driveItem](../resources/driveitem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a494d-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a494d-134">Example</span></span>

##### <a name="request"></a><span data-ttu-id="a494d-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a494d-135">Request</span></span>
<span data-ttu-id="a494d-136">Aquí tiene un ejemplo de la solicitud de las unidades del usuario.</span><span class="sxs-lookup"><span data-stu-id="a494d-136">Here is an example of the request for the user's drives.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_drive_special"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/special/{name}
```

##### <a name="response"></a><span data-ttu-id="a494d-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a494d-137">Response</span></span>
<span data-ttu-id="a494d-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a494d-138">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.driveItem"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "folder": { },
  "id": "s!lkjqwlkj124912049an",
  "name": "Photos",
  "specialFolder": { "name": "photos" },
  "webUrl": "https://contoso-my.sharepoint.com/personal/rgregg_contoso_com/Documents/Photos",
}
```

## <a name="remarks"></a><span data-ttu-id="a494d-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a494d-139">Remarks</span></span>

<span data-ttu-id="a494d-140">Para solicitar los elementos secundarios de una carpeta especial, puede solicitar la colección `children` o usar la opción [expand](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) para expandir la colección de elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="a494d-140">To request the children of a special folder, you can request the `children` collection or use the [expand](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) option to expand the children collection.</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "List drives",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Drive/Get special folder"
}-->

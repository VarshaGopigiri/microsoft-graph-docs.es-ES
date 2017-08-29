# <a name="accessing-shared-driveitems"></a><span data-ttu-id="1b425-101">Acceder a objetos DriveItem compartidos</span><span class="sxs-lookup"><span data-stu-id="1b425-101">Accessing shared DriveItems</span></span>

<span data-ttu-id="1b425-102">Acceda a un objeto [DriveItem](../resources/driveitem.md) compartido o a una colección de elementos compartidos mediante el uso de un **shareId** o una dirección URL para compartir.</span><span class="sxs-lookup"><span data-stu-id="1b425-102">Access a shared [DriveItem](../resources/driveitem.md) or a collection of shared items by using a **shareId** or sharing URL.</span></span>

<span data-ttu-id="1b425-103">Para usar una dirección URL para compartir con esta API, la aplicación debe [transformar la dirección URL en un token para compartir](#transform-a-sharing-url).</span><span class="sxs-lookup"><span data-stu-id="1b425-103">To use a sharing URL with this API, your app needs to [transform the URL into a sharing token](#transform-a-sharing-url).</span></span>

## <a name="permissions"></a><span data-ttu-id="1b425-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="1b425-104">Permissions</span></span>

<span data-ttu-id="1b425-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1b425-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1b425-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1b425-107">Permission type</span></span>      | <span data-ttu-id="1b425-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1b425-108">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="1b425-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1b425-109">Delegated (work or school account)</span></span> | <span data-ttu-id="1b425-110">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1b425-110">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    | 
|<span data-ttu-id="1b425-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1b425-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1b425-112">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1b425-112">Files.ReadWrite, Files.ReadWrite.All</span></span>    | 
|<span data-ttu-id="1b425-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1b425-113">Application</span></span> | <span data-ttu-id="1b425-114">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1b425-114">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="1b425-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1b425-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /shares/{sharingIdOrUrl}
```

## <a name="request-body"></a><span data-ttu-id="1b425-116">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="1b425-116">Request body</span></span>
<span data-ttu-id="1b425-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1b425-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1b425-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b425-118">Response</span></span>

<span data-ttu-id="1b425-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un recurso [sharedDriveItem](../resources/shareddriveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1b425-119">If successful, this method returns a `200 OK` response code and a [sharedDriveItem](../resources/shareddriveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1b425-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1b425-120">Example</span></span>

##### <a name="request"></a><span data-ttu-id="1b425-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1b425-121">Request</span></span>

<span data-ttu-id="1b425-122">Este es un ejemplo de la solicitud para recuperar un elemento compartido:</span><span class="sxs-lookup"><span data-stu-id="1b425-122">Here is an example of the request to retrieve a shared item:</span></span>

<!-- {
  "blockType": "request",
  "name": "get_shares_by_url"
}-->
```http
GET https://graph.microsoft.com/v1.0/shares/{shareIdOrUrl}
```
##### <a name="response"></a><span data-ttu-id="1b425-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b425-123">Response</span></span>

<span data-ttu-id="1b425-124">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1b425-124">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.sharedDriveItem"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "B64397C8-07AE-43E4-920E-32BFB4331A5B",
  "name": "contoso project.docx",
  "owner": {
    "user": {
      "id": "98E88F1C-F8DC-47CC-A406-C090248B30E5",
      "displayName": "Ryan Gregg"
    }
  }
}
```

## <a name="access-the-shared-item-directly"></a><span data-ttu-id="1b425-125">Acceder directamente al elemento compartido</span><span class="sxs-lookup"><span data-stu-id="1b425-125">Access the shared item directly</span></span>

<span data-ttu-id="1b425-p102">Mientras que [**SharedDriveItem**](../resources/shareddriveitem.md) contiene alguna información útil, la mayoría de las aplicaciones querrán acceder directamente al objeto [DriveItem](../resources/driveitem.md) compartido. El recurso **SharedDriveItem** incluye un **root** y relaciones de **items** que pueden acceder al contenido del ámbito del elemento compartido.</span><span class="sxs-lookup"><span data-stu-id="1b425-p102">While the [**SharedDriveItem**](../resources/shareddriveitem.md) contains some useful information, most apps will want to directly access the shared [DriveItem](../resources/driveitem.md). The **SharedDriveItem** resource includes a **root** and **items** relationships which can access content within the scope of the shared item.</span></span>

## <a name="example-single-file"></a><span data-ttu-id="1b425-128">Ejemplo (archivo único)</span><span class="sxs-lookup"><span data-stu-id="1b425-128">Example (single file)</span></span>

##### <a name="request"></a><span data-ttu-id="1b425-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1b425-129">Request</span></span>

<span data-ttu-id="1b425-130">Al solicitar la relación **root**, se devolverá el objeto **DriveItem** compartido.</span><span class="sxs-lookup"><span data-stu-id="1b425-130">By requesting the **root** relationship, the **DriveItem** that was shared will be returned.</span></span>

```http
GET https://graph.microsoft.com/v1.0/shares/{shareIdOrUrl}/root
```

##### <a name="response"></a><span data-ttu-id="1b425-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b425-131">Response</span></span>

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": "9FFFDB3C-5B87-4062-9606-1B008CA88E44",
  "name": "contoso project.docx",
  "eTag": "2246BD2D-7811-4660-BD0F-1CF36133677B,1",
  "file": {},
  "size": 109112
}
```

## <a name="example-shared-folder"></a><span data-ttu-id="1b425-132">Ejemplo (carpeta compartida)</span><span class="sxs-lookup"><span data-stu-id="1b425-132">Example (shared folder)</span></span>

##### <a name="request"></a><span data-ttu-id="1b425-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1b425-133">Request</span></span>

<span data-ttu-id="1b425-134">Al solicitar la relación **root** y expandir la colección **children**, se devolverá el objeto **DriveItem** compartido junto con los archivos de la carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="1b425-134">By requesting the **root** relationship and expanding the **children** collection, the **DriveItem** that was shared will be returned along with the files within the shared folder.</span></span>

```http
GET https://graph.microsoft.com/v1.0/shares/{shareIdOrUrl}/root?$expand=children
```

##### <a name="response"></a><span data-ttu-id="1b425-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b425-135">Response</span></span>

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": "9FFFDB3C-5B87-4062-9606-1B008CA88E44",
  "name": "Contoso Project",
  "eTag": "2246BD2D-7811-4660-BD0F-1CF36133677B,1",
  "folder": {}
  "size": 10911212,
  "children": [
    {
      "id": "AFBBDD79-868E-452D-AD4D-24697D4A4044",
      "name": "Propsoal.docx",
      "file": {},
      "size": 19001
    },
    {
      "id": "A91FE90A-2F2C-4EE6-B412-C4FFBA3F71A6",
      "name": "Update to Proposal.docx",
      "file": {},
      "size": 91001
    }
  ]
}
```

## <a name="transform-a-sharing-url"></a><span data-ttu-id="1b425-136">Transformar una dirección URL para compartir</span><span class="sxs-lookup"><span data-stu-id="1b425-136">Transform a sharing URL</span></span>

<span data-ttu-id="1b425-137">Para acceder a una dirección URL para compartir mediante la API **shares**, la dirección URL debe transformarse en un token para compartir.</span><span class="sxs-lookup"><span data-stu-id="1b425-137">To access a sharing URL using the **shares** API, the URL needs to be transformed into a sharing token.</span></span>

<span data-ttu-id="1b425-138">Para transformar una dirección URL en un token para compartir:</span><span class="sxs-lookup"><span data-stu-id="1b425-138">To transform a URL into a sharing token:</span></span>

1. <span data-ttu-id="1b425-139">Codifique en base64 la dirección URL para compartir.</span><span class="sxs-lookup"><span data-stu-id="1b425-139">Base64 encode the sharing URL.</span></span>
2. <span data-ttu-id="1b425-140">Convierta los datos codificados en base64 en [formato base64url sin rellenar](https://en.wikipedia.org/wiki/Base64); para ello:</span><span class="sxs-lookup"><span data-stu-id="1b425-140">Convert the base64 encoded data to [unpadded base64url format](https://en.wikipedia.org/wiki/Base64) by:</span></span>
  1. <span data-ttu-id="1b425-141">Quite los caracteres `=` finales de la cadena</span><span class="sxs-lookup"><span data-stu-id="1b425-141">Trim trailing `=` characters from the string</span></span>
  2. <span data-ttu-id="1b425-142">Reemplace los caracteres inseguros de dirección URL por un carácter equivalente; reemplace `/` por `_` y `+` por `-`.</span><span class="sxs-lookup"><span data-stu-id="1b425-142">Replace unsafe URL characters with an equivalent character; replace `/` with `_` and `+` with `-`.</span></span>
3. <span data-ttu-id="1b425-143">Anexe `u!` al principio de la cadena.</span><span class="sxs-lookup"><span data-stu-id="1b425-143">Append `u!` to the beginning of the string.</span></span>

<span data-ttu-id="1b425-144">Por ejemplo, el siguiente método C# transforma una cadena de entrada en un token para compartir:</span><span class="sxs-lookup"><span data-stu-id="1b425-144">For example, the following C# method transforms an input string into a sharing token:</span></span>

```csharp
string UrlToSharingToken(string inputUrl) {
  var base64Value = System.Convert.ToBase64String(System.Text.Encoding.UTF8.GetBytes(inputUrl));
  return "u!" + base64Value.TrimEnd('=').Replace('/','_').Replace('+','-');
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update permission",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Update permission"
}-->

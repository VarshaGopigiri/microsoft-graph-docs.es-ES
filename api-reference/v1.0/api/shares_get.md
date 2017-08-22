# <a name="accessing-shared-driveitems"></a><span data-ttu-id="e37d7-101">Acceder a objetos DriveItem compartidos</span><span class="sxs-lookup"><span data-stu-id="e37d7-101">Accessing shared DriveItems</span></span>

<span data-ttu-id="e37d7-102">Acceda a un objeto [DriveItem](../resources/driveitem.md) compartido o a una colección de elementos compartidos mediante el uso de un **shareId** o una dirección URL para compartir.</span><span class="sxs-lookup"><span data-stu-id="e37d7-102">Access a shared [DriveItem](../resources/driveitem.md) or a collection of shared items by using a **shareId** or sharing URL.</span></span>

<span data-ttu-id="e37d7-103">Para usar una dirección URL para compartir con esta API, la aplicación debe [transformar la dirección URL en un token para compartir](#transform-a-sharing-url).</span><span class="sxs-lookup"><span data-stu-id="e37d7-103">To use a sharing URL with this API, your app needs to [transform the URL into a sharing token](#transform-a-sharing-url).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e37d7-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e37d7-104">Prerequisites</span></span>

<span data-ttu-id="e37d7-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="e37d7-105">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="e37d7-106">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e37d7-106">Files.ReadWrite</span></span>
* <span data-ttu-id="e37d7-107">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e37d7-107">Files.ReadWrite.All</span></span>
* <span data-ttu-id="e37d7-108">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e37d7-108">Sites.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="e37d7-109">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e37d7-109">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /shares/{sharingIdOrUrl}
```

## <a name="request-body"></a><span data-ttu-id="e37d7-110">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="e37d7-110">Request body</span></span>
<span data-ttu-id="e37d7-111">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e37d7-111">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e37d7-112">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e37d7-112">Response</span></span>

<span data-ttu-id="e37d7-113">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un recurso [sharedDriveItem](../resources/shareddriveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e37d7-113">If successful, this method returns a `200 OK` response code and a [sharedDriveItem](../resources/shareddriveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e37d7-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e37d7-114">Example</span></span>

##### <a name="request"></a><span data-ttu-id="e37d7-115">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e37d7-115">Request</span></span>

<span data-ttu-id="e37d7-116">Este es un ejemplo de la solicitud para recuperar un elemento compartido:</span><span class="sxs-lookup"><span data-stu-id="e37d7-116">Here is an example of the request to retrieve a shared item:</span></span>

<!-- {
  "blockType": "request",
  "name": "get_shares_by_url"
}-->
```http
GET https://graph.microsoft.com/v1.0/shares/{shareIdOrUrl}
```
##### <a name="response"></a><span data-ttu-id="e37d7-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e37d7-117">Response</span></span>

<span data-ttu-id="e37d7-118">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e37d7-118">Here is an example of the response.</span></span>
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

## <a name="access-the-shared-item-directly"></a><span data-ttu-id="e37d7-119">Acceder directamente al elemento compartido</span><span class="sxs-lookup"><span data-stu-id="e37d7-119">Access the shared item directly</span></span>

<span data-ttu-id="e37d7-p101">Mientras que [**SharedDriveItem**](../resources/shareddriveitem.md) contiene alguna información útil, la mayoría de las aplicaciones querrán acceder directamente al objeto [DriveItem](../resources/driveitem.md) compartido. El recurso **SharedDriveItem** incluye un **root** y relaciones de **items** que pueden acceder al contenido del ámbito del elemento compartido.</span><span class="sxs-lookup"><span data-stu-id="e37d7-p101">While the [**SharedDriveItem**](../resources/shareddriveitem.md) contains some useful information, most apps will want to directly access the shared [DriveItem](../resources/driveitem.md). The **SharedDriveItem** resource includes a **root** and **items** relationships which can access content within the scope of the shared item.</span></span>

## <a name="example-single-file"></a><span data-ttu-id="e37d7-122">Ejemplo (archivo único)</span><span class="sxs-lookup"><span data-stu-id="e37d7-122">Example (single file)</span></span>

##### <a name="request"></a><span data-ttu-id="e37d7-123">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e37d7-123">Request</span></span>

<span data-ttu-id="e37d7-124">Al solicitar la relación **root**, se devolverá el objeto **DriveItem** compartido.</span><span class="sxs-lookup"><span data-stu-id="e37d7-124">By requesting the **root** relationship, the **DriveItem** that was shared will be returned.</span></span>

```http
GET https://graph.microsoft.com/v1.0/shares/{shareIdOrUrl}/root
```

##### <a name="response"></a><span data-ttu-id="e37d7-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e37d7-125">Response</span></span>

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

## <a name="example-shared-folder"></a><span data-ttu-id="e37d7-126">Ejemplo (carpeta compartida)</span><span class="sxs-lookup"><span data-stu-id="e37d7-126">Example (shared folder)</span></span>

##### <a name="request"></a><span data-ttu-id="e37d7-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e37d7-127">Request</span></span>

<span data-ttu-id="e37d7-128">Al solicitar la relación **root** y expandir la colección **children**, se devolverá el objeto **DriveItem** compartido junto con los archivos de la carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="e37d7-128">By requesting the **root** relationship and expanding the **children** collection, the **DriveItem** that was shared will be returned along with the files within the shared folder.</span></span>

```http
GET https://graph.microsoft.com/v1.0/shares/{shareIdOrUrl}/root?$expand=children
```

##### <a name="response"></a><span data-ttu-id="e37d7-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e37d7-129">Response</span></span>

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

## <a name="transform-a-sharing-url"></a><span data-ttu-id="e37d7-130">Transformar una dirección URL para compartir</span><span class="sxs-lookup"><span data-stu-id="e37d7-130">Transform a sharing URL</span></span>

<span data-ttu-id="e37d7-131">Para acceder a una dirección URL para compartir mediante la API **shares**, la dirección URL debe transformarse en un token para compartir.</span><span class="sxs-lookup"><span data-stu-id="e37d7-131">To access a sharing URL using the **shares** API, the URL needs to be transformed into a sharing token.</span></span>

<span data-ttu-id="e37d7-132">Para transformar una dirección URL en un token para compartir:</span><span class="sxs-lookup"><span data-stu-id="e37d7-132">To transform a URL into a sharing token:</span></span>

1. <span data-ttu-id="e37d7-133">Codifique en base64 la dirección URL para compartir.</span><span class="sxs-lookup"><span data-stu-id="e37d7-133">Base64 encode the sharing URL.</span></span>
2. <span data-ttu-id="e37d7-134">Convierta los datos codificados en base64 en [formato base64url sin rellenar](https://en.wikipedia.org/wiki/Base64); para ello:</span><span class="sxs-lookup"><span data-stu-id="e37d7-134">Convert the base64 encoded data to [unpadded base64url format](https://en.wikipedia.org/wiki/Base64) by:</span></span>
  1. <span data-ttu-id="e37d7-135">Quite los caracteres `=` finales de la cadena</span><span class="sxs-lookup"><span data-stu-id="e37d7-135">Trim trailing `=` characters from the string</span></span>
  2. <span data-ttu-id="e37d7-136">Reemplace los caracteres inseguros de dirección URL por un carácter equivalente; reemplace `/` por `_` y `+` por `-`.</span><span class="sxs-lookup"><span data-stu-id="e37d7-136">Replace unsafe URL characters with an equivalent character; replace `/` with `_` and `+` with `-`.</span></span>
3. <span data-ttu-id="e37d7-137">Anexe `u!` al principio de la cadena.</span><span class="sxs-lookup"><span data-stu-id="e37d7-137">Append `u!` to the beginning of the string.</span></span>

<span data-ttu-id="e37d7-138">Por ejemplo, el siguiente método C# transforma una cadena de entrada en un token para compartir:</span><span class="sxs-lookup"><span data-stu-id="e37d7-138">For example, the following C# method transforms an input string into a sharing token:</span></span>

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

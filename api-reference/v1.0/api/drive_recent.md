# <a name="list-recent-files"></a><span data-ttu-id="5695c-101">Enumerar archivos recientes</span><span class="sxs-lookup"><span data-stu-id="5695c-101">List recent files</span></span>

<span data-ttu-id="5695c-p101">Enumere un conjunto de elementos que ha usado recientemente el usuario que ha iniciado sesión. Esta colección incluye elementos que están en la unidad del usuario, así como elementos de otras unidades a los que tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="5695c-p101">List a set of items that have been recently used by the signed in user. This collection includes items that are in the user's drive as well as items they have access to from other drives.</span></span>

## <a name="permissions"></a><span data-ttu-id="5695c-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="5695c-104">Permissions</span></span>
<span data-ttu-id="5695c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5695c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5695c-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5695c-107">Permission type</span></span>      | <span data-ttu-id="5695c-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5695c-108">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="5695c-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5695c-109">Delegated (work or school account)</span></span> | <span data-ttu-id="5695c-110">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5695c-110">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    | 
|<span data-ttu-id="5695c-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5695c-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5695c-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5695c-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    | 
|<span data-ttu-id="5695c-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5695c-113">Application</span></span> | <span data-ttu-id="5695c-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5695c-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="5695c-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5695c-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```
GET /me/drive/recent
```

## <a name="request-body"></a><span data-ttu-id="5695c-116">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="5695c-116">Request body</span></span>
<span data-ttu-id="5695c-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5695c-117">Do not supply a request body for this method.</span></span>

## <a name="example"></a><span data-ttu-id="5695c-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5695c-118">Example</span></span>

<!-- { "blockType": "request", "name": "drive-recent", "scopes": "files.read" } -->
```http
GET https://graph.microsoft.com/v1.0/me/drive/recent
```

## <a name="response"></a><span data-ttu-id="5695c-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5695c-119">Response</span></span>

<span data-ttu-id="5695c-p103">Devuelve una colección de recursos [DriveItem](../resources/driveitem.md) para los elementos a los que ha accedido recientemente el propietario de la unidad. Los elementos fuera de la unidad del usuario incluirán la faceta [RemoteItem](../resources/remoteitem.md), que ofrece información para acceder al elemento compartido.</span><span class="sxs-lookup"><span data-stu-id="5695c-p103">This returns a collection of [DriveItem](../resources/driveitem.md) resources for items which the owner of the drive has recently accessed. Items outside of the user's drive will include the [RemoteItem](../resources/remoteitem.md) facet, which provides information to access the shared item.</span></span>


<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "isCollection": true, "truncated": true } -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "1312abc!1231",
      "remoteItem":
      {
        "id": "1991210caf!192",
        "name": "March Proposal.docx",
        "file": { },
        "size": 19121,
        "parentReference": {
          "driveId": "1991210caf",
          "id": "1991210caf!104"
        }
      }
    },
    {
      "id": "1312def!9943",
      "name": "Vacation.jpg",
      "file": { },
      "size": 37810,
      "parentReference": {
        "driveId": "1312def",
        "id": "1312def!123"
      }
    }
  ]
}
```

## <a name="remarks"></a><span data-ttu-id="5695c-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5695c-122">Remarks</span></span>

<span data-ttu-id="5695c-p104">Algunos recursos driveItem devueltos de la acción **recent** incluirán la faceta **remoteItem**, que indica que son elementos de otra unidad. Para acceder al objeto driveItem original, deberá realizar una solicitud con la información proporcionada en **remoteItem** en el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="5695c-p104">Some driveItems returned from the **recent** action will include the **remoteItem** facet which indicates they are items from another drive. To access the original driveItem object, you will need to make a request using the information provided in **remoteItem** in the following format:</span></span>

<!-- {"blockType": "ignored"} -->
```http
GET https://graph.microsoft.com/v1.0/drives/{remoteItem.driveId}/items/{remoteItem.id}
```

<!-- {
  "type": "#page.annotation",
  "description": "Retrieve a list of files shared with the signed-in user.",
  "keywords": "sharedWithMe onedrive shared files",
  "section": "documentation",
  "tocPath": "OneDrive/Drive/Shared with me"
} -->

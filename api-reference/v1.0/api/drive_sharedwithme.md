# <a name="list-items-shared-with-the-signed-in-user"></a><span data-ttu-id="df645-101">Enumerar elementos compartidos con el usuario que ha iniciado sesión</span><span class="sxs-lookup"><span data-stu-id="df645-101">List items shared with the signed-in user</span></span>

<span data-ttu-id="df645-102">Recupere una colección de recursos [DriveItem](../resources/driveitem.md) que se han compartido con el propietario del [Drive](../resources/drive.md).</span><span class="sxs-lookup"><span data-stu-id="df645-102">Retrieve a collection of [DriveItem](../resources/driveitem.md) resources that have been shared with the owner of the [Drive](../resources/drive.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="df645-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="df645-103">Permissions</span></span>
<span data-ttu-id="df645-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="df645-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="df645-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="df645-106">Permission type</span></span>      | <span data-ttu-id="df645-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="df645-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="df645-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="df645-108">Delegated (work or school account)</span></span> | <span data-ttu-id="df645-109">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="df645-109">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="df645-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="df645-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="df645-111">Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="df645-111">Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="df645-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="df645-112">Application</span></span> | <span data-ttu-id="df645-113">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="df645-113">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

<span data-ttu-id="df645-114">Además, sin uno de los permisos **Todo**, los elementos compartidos devueltos desde esta API no serán accesibles.</span><span class="sxs-lookup"><span data-stu-id="df645-114">Additionally, without one of the  **All** scopes, shared items returned from this API will not be accessible.</span></span>

## <a name="http-request"></a><span data-ttu-id="df645-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="df645-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```
GET /me/drive/sharedWithMe
```

## <a name="request-body"></a><span data-ttu-id="df645-116">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="df645-116">Request body</span></span>
<span data-ttu-id="df645-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="df645-117">Do not supply a request body for this method.</span></span>

## <a name="example"></a><span data-ttu-id="df645-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="df645-118">Example</span></span>

<!-- { "blockType": "request", "name": "drive-sharedwithme", "scopes": "files.read" } -->
```http
GET https://graph.microsoft.com/v1.0/me/drive/sharedWithMe
```

## <a name="response"></a><span data-ttu-id="df645-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="df645-119">Response</span></span>

<span data-ttu-id="df645-p102">Devuelve una colección de recursos [DriveItem](../resources/driveitem.md) que contiene los recursos DriveItem compartidos con el propietario de la unidad. En este ejemplo, ya que la unidad es la unidad predeterminada del usuario, devuelve elementos compartidos con el usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="df645-p102">This returns a collection of [DriveItem](../resources/driveitem.md) resources which contain the DriveItem resources shared with the owner of the drive. In this example, since the drive is the user's default drive, this returns items shared with the signed in user.</span></span>


<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "isCollection": true, "truncated": true } -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "1312abc",
      "remoteItem": {
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
      "id": "1312def",
      "remoteItem": {
        "id": "1991210caf!1991",
        "name": "Team Roster.xlsx",
        "file": { },
        "size": 37619,
        "parentReference": {
          "driveId": "1991210caf",
          "id": "1991210caf!104"
        }
      }
    }
  ]
}
```

## <a name="remarks"></a><span data-ttu-id="df645-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="df645-122">Remarks</span></span>

<span data-ttu-id="df645-p103">Los recursos driveItem devueltos de la acción **sharedWithMe** incluirán siempre la faceta [**remoteItem**](../resources/remoteitem.md) que indica que son elementos de otra unidad. Para acceder al recurso driveItem compartido, deberá realizar una solicitud con la información proporcionada en **remoteItem** en el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="df645-p103">DriveItems returned from the **sharedWithMe** action will always include the [**remoteItem**](../resources/remoteitem.md) facet which indicates they are items from a different drive. To access the shared DriveItem resource, you will need to make a request using the information provided in **remoteItem** in the following format:</span></span>

<!-- {"blockType": "ignored"} -->
```http
GET https://graph.microsoft.com/v1.0/drives/{remoteItem.parentReference.driveId}/items/{remoteItem.id}
```

<!-- {
  "type": "#page.annotation",
  "description": "Retrieve a list of files shared with the signed-in user.",
  "keywords": "sharedWithMe onedrive shared files",
  "section": "documentation",
  "tocPath": "OneDrive/Drive/Shared with me"
} -->

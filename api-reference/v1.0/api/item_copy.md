# <a name="copy-a-driveitem"></a><span data-ttu-id="b27c9-101">Copiar un objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="b27c9-101">Copy a DriveItem</span></span>

<span data-ttu-id="b27c9-102">Crea una copia de un objeto [driveItem](../resources/driveitem.md) (incluidos los elementos secundarios) en un nuevo elemento primario o con un nombre nuevo.</span><span class="sxs-lookup"><span data-stu-id="b27c9-102">Creates a copy of a [driveItem](../resources/driveitem.md) (including any children) under a new parent or with a new name.</span></span>

## <a name="permissions"></a><span data-ttu-id="b27c9-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="b27c9-103">Permissions</span></span>
<span data-ttu-id="b27c9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b27c9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b27c9-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b27c9-106">Permission type</span></span>      | <span data-ttu-id="b27c9-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b27c9-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b27c9-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b27c9-108">Delegated (work or school account)</span></span> | <span data-ttu-id="b27c9-109">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b27c9-109">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="b27c9-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b27c9-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b27c9-111">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b27c9-111">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="b27c9-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b27c9-112">Application</span></span> | <span data-ttu-id="b27c9-113">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b27c9-113">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b27c9-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b27c9-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```
POST /me/drive/items/{item-id}/copy
POST /me/drive/root:/{path}:/copy
POST /groups/{group-id}/drive/items/{item-id}/copy
```

## <a name="request-body"></a><span data-ttu-id="b27c9-115">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="b27c9-115">Request body</span></span>
<span data-ttu-id="b27c9-116">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="b27c9-116">In the request body, provide a JSON object with the following parameters.</span></span>


| <span data-ttu-id="b27c9-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="b27c9-117">Name</span></span>            | <span data-ttu-id="b27c9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b27c9-118">Value</span></span>                                          | <span data-ttu-id="b27c9-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b27c9-119">Description</span></span>                                                                                                 |
|:----------------|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b27c9-120">parentReference</span><span class="sxs-lookup"><span data-stu-id="b27c9-120">parentReference</span></span> | [<span data-ttu-id="b27c9-121">ItemReference</span><span class="sxs-lookup"><span data-stu-id="b27c9-121">ItemReference</span></span>](../resources/itemreference.md) | <span data-ttu-id="b27c9-p102">Opcional. Referencia al elemento primario en que se creará la copia.</span><span class="sxs-lookup"><span data-stu-id="b27c9-p102">Optional. Reference to the parent item the copy will be created in.</span></span>                                         |
| <span data-ttu-id="b27c9-124">name</span><span class="sxs-lookup"><span data-stu-id="b27c9-124">name</span></span>            | <span data-ttu-id="b27c9-125">string</span><span class="sxs-lookup"><span data-stu-id="b27c9-125">string</span></span>                                         | <span data-ttu-id="b27c9-p103">Opcional. El nuevo nombre de la copia. Si no se proporciona, se usará el mismo nombre que el original.</span><span class="sxs-lookup"><span data-stu-id="b27c9-p103">Optional. The new name for the copy. If this isn't provided, the same name will be used as the original.</span></span>    |

<span data-ttu-id="b27c9-p104">**Nota:** _parentReference_ debe incluir un `id` o `path`, pero no ambos. Si se incluyen ambos, tienen que hacer referencia al mismo elemento o se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="b27c9-p104">**Note:** The _parentReference_ should include either an `id` or `path` but not both. If both are included, they need to reference the same item or an error will occur.</span></span>

## <a name="example"></a><span data-ttu-id="b27c9-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b27c9-131">Example</span></span>

<!-- { "blockType": "request", "name": "copy-item", "scopes": "files.readwrite" } -->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{item-id}/copy
Content-Type: application/json

{
  "parentReference": {
    "path": "/drive/root:/Documents"
  },
  "name": "contoso plan.docx"
}
```

## <a name="response"></a><span data-ttu-id="b27c9-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b27c9-132">Response</span></span>

<span data-ttu-id="b27c9-133">Devuelve detalles sobre cómo supervisar el progreso de la copia tras aceptar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b27c9-133">Returns details about how to monitor the progress of the copy, upon accepting the request.</span></span>

<!-- { "blockType": "response" } -->
```http
HTTP/1.1 202 Accepted
```

## <a name="remarks"></a><span data-ttu-id="b27c9-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b27c9-134">Remarks</span></span>

<span data-ttu-id="b27c9-p105">En muchos casos, la operación de copia se realiza de forma asincrónica. La respuesta de la API solo indicará que la operación de copia se ha aceptado o rechazado, debido a que el nombre de archivo de destino ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="b27c9-p105">In many cases the copy action is performed asynchronously. The response from the API will only indicate that the copy operation was accepted or rejected, say due to the destination filename already being in use.</span></span>

<span data-ttu-id="b27c9-137">**Nota:** La API no proporciona un método para saber si la copia fue correcta.</span><span class="sxs-lookup"><span data-stu-id="b27c9-137">**Note:** The API does not provide a method to know if the copy was successful.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "Create a copy of an existing item.",
  "keywords": "copy existing item",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Copy"
} -->

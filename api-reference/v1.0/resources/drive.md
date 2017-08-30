# <a name="drive-resource-type"></a><span data-ttu-id="84875-101">Tipo de recurso Drive</span><span class="sxs-lookup"><span data-stu-id="84875-101">Drive resource type</span></span>

<span data-ttu-id="84875-102">El recurso de unidad es el objeto de nivel superior que representa el OneDrive de un usuario o una biblioteca de documentos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="84875-102">The drive resource is the top level object representing a user's OneDrive or a document library in SharePoint.</span></span>

<span data-ttu-id="84875-p101">Los usuarios de OneDrive siempre tendrán al menos una unidad disponible, la unidad predeterminada. Es posible que los usuarios sin licencia de OneDrive no tengan una unidad predeterminada disponible.</span><span class="sxs-lookup"><span data-stu-id="84875-p101">OneDrive users will always have at least one drive available, their default drive. Users without a OneDrive license may not have a default drive available.</span></span>

## <a name="json-representation"></a><span data-ttu-id="84875-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="84875-105">JSON representation</span></span>

<span data-ttu-id="84875-106">A continuación se incluye una representación JSON del recurso **drive**.</span><span class="sxs-lookup"><span data-stu-id="84875-106">Here is a JSON representation of a Drive resource.</span></span>

<span data-ttu-id="84875-107">El recurso **drive** deriva de [**baseItem**](baseitem.md) y hereda las propiedades de ese recurso.</span><span class="sxs-lookup"><span data-stu-id="84875-107">The **drive** resource is derived from [**baseItem**](baseitem.md) and inherits properties from that resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "items", "root", "special", "owner", "description" ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.drive"
}-->

```json
{
  "id": "string (identifier)",
  "driveType": "string",
  "owner": {"@odata.type": "microsoft.graph.identitySet"},
  "quota": {"@odata.type": "microsoft.graph.quota"},
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" },

  /* relationships */
  "root": {"@odata.type": "microsoft.graph.driveItem" },
  "items": [ {"@odata.type": "microsoft.graph.driveItem" }],
  "special": [ {"@odata.type": "microsoft.graph.driveItem" }],

  /* inherited from baseItem */
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "createdDateTime": "datetime",
  "description": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "datetime",
  "name": "string",
  "webUrl": "url"
}
```

## <a name="properties"></a><span data-ttu-id="84875-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="84875-108">Properties</span></span>

| <span data-ttu-id="84875-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="84875-109">Property</span></span>             | <span data-ttu-id="84875-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="84875-110">Type</span></span>                          | <span data-ttu-id="84875-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="84875-111">Description</span></span>                                                                                                                                                                                                                      |
| :------------------- | :---------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="84875-112">id</span><span class="sxs-lookup"><span data-stu-id="84875-112">id</span></span>                   | <span data-ttu-id="84875-113">String</span><span class="sxs-lookup"><span data-stu-id="84875-113">String</span></span>                        | <span data-ttu-id="84875-p102">El identificador único de la unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="84875-p102">The unique identifier of the drive. Read-only.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="84875-116">createdBy</span><span class="sxs-lookup"><span data-stu-id="84875-116">createdBy</span></span>            | <span data-ttu-id="84875-117">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="84875-117">[identitySet][]</span></span>               | <span data-ttu-id="84875-p103">Identidad del usuario, del dispositivo o de la aplicación que ha creado el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="84875-p103">Identity of the user, device, or application which created the item. Read-only.</span></span>                                                                                                                                                  |
| <span data-ttu-id="84875-120">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="84875-120">createdDateTime</span></span>      | <span data-ttu-id="84875-121">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="84875-121">dateTimeOffset</span></span>                | <span data-ttu-id="84875-p104">Fecha y hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="84875-p104">Date and time of item creation. Read-only.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="84875-124">driveType</span><span class="sxs-lookup"><span data-stu-id="84875-124">driveType</span></span>            | <span data-ttu-id="84875-125">String</span><span class="sxs-lookup"><span data-stu-id="84875-125">String</span></span>                        | <span data-ttu-id="84875-p105">Describe el tipo de unidad que representa este recurso. Las unidades personales de OneDrive devolverán `personal`. OneDrive para la Empresa devolverá `business`. Las bibliotecas de documentos de SharePoint devolverán `documentLibrary`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="84875-p105">Describes the type of drive represented by this resource. OneDrive personal drives will return `personal`. OneDrive for Business will return `business`. SharePoint document libraries will return `documentLibrary`. Read-only.</span></span> |
| <span data-ttu-id="84875-131">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="84875-131">lastModifiedBy</span></span>       | <span data-ttu-id="84875-132">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="84875-132">[identitySet][]</span></span>               | <span data-ttu-id="84875-p106">Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="84875-p106">Identity of the user, device, and application which last modified the item. Read-only.</span></span>                                                                                                                                           |
| <span data-ttu-id="84875-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="84875-135">lastModifiedDateTime</span></span> | <span data-ttu-id="84875-136">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="84875-136">dateTimeOffset</span></span>                | <span data-ttu-id="84875-p107">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="84875-p107">Date and time the item was last modified. Read-only.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="84875-139">name</span><span class="sxs-lookup"><span data-stu-id="84875-139">name</span></span>                 | <span data-ttu-id="84875-140">string</span><span class="sxs-lookup"><span data-stu-id="84875-140">string</span></span>                        | <span data-ttu-id="84875-p108">Nombre del elemento. Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="84875-p108">The name of the item. Read-write.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="84875-143">owner</span><span class="sxs-lookup"><span data-stu-id="84875-143">owner</span></span>                | [<span data-ttu-id="84875-144">identitySet</span><span class="sxs-lookup"><span data-stu-id="84875-144">identitySet</span></span>](identityset.md) | <span data-ttu-id="84875-p109">Opcional. La cuenta de usuario propietaria de la unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="84875-p109">Optional. The user account that owns the drive. Read-only.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="84875-148">quota</span><span class="sxs-lookup"><span data-stu-id="84875-148">quota</span></span>                | [<span data-ttu-id="84875-149">quota</span><span class="sxs-lookup"><span data-stu-id="84875-149">quota</span></span>](quota.md)             | <span data-ttu-id="84875-p110">Opcional. Información sobre la cuota de espacio de almacenamiento de la unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="84875-p110">Optional. Information about the drive's storage space quota. Read-only.</span></span>                                                                                                                                                          |
| <span data-ttu-id="84875-153">sharepointIds</span><span class="sxs-lookup"><span data-stu-id="84875-153">sharepointIds</span></span>        | <span data-ttu-id="84875-154">[sharepointIds][]</span><span class="sxs-lookup"><span data-stu-id="84875-154">[sharepointIds][]</span></span>             | <span data-ttu-id="84875-p111">Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="84875-p111">Returns identifiers useful for SharePoint REST compatibility. Read-only.</span></span>                                                                                                                                                         |
| <span data-ttu-id="84875-157">webUrl</span><span class="sxs-lookup"><span data-stu-id="84875-157">webUrl</span></span>               | <span data-ttu-id="84875-158">string (url)</span><span class="sxs-lookup"><span data-stu-id="84875-158">string (url)</span></span>                  | <span data-ttu-id="84875-p112">Dirección URL que muestra el recurso en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="84875-p112">URL that displays the resource in the browser. Read-only.</span></span>                                                                                                                                                                        |

<span data-ttu-id="84875-161">[identitySet]: identityset.md</span><span class="sxs-lookup"><span data-stu-id="84875-161">[identitySet]: identityset.md</span></span>
<span data-ttu-id="84875-162">[sharepointIds]: sharepointids.md</span><span class="sxs-lookup"><span data-stu-id="84875-162">[sharepointIds]: sharepointids.md</span></span>

## <a name="relationships"></a><span data-ttu-id="84875-163">Relaciones</span><span class="sxs-lookup"><span data-stu-id="84875-163">Relationships</span></span>

| <span data-ttu-id="84875-164">Relación</span><span class="sxs-lookup"><span data-stu-id="84875-164">Relationship</span></span> | <span data-ttu-id="84875-165">Tipo</span><span class="sxs-lookup"><span data-stu-id="84875-165">Type</span></span>                                 | <span data-ttu-id="84875-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="84875-166">Description</span></span>                                                              |
| :----------- | :----------------------------------- | :----------------------------------------------------------------------- |
| <span data-ttu-id="84875-167">items</span><span class="sxs-lookup"><span data-stu-id="84875-167">items</span></span>        | <span data-ttu-id="84875-168">Colección [driveitem](driveitem.md)</span><span class="sxs-lookup"><span data-stu-id="84875-168">[driveitem](driveitem.md) collection</span></span> | <span data-ttu-id="84875-p113">Todos los elementos contenidos en la unidad. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="84875-p113">All items contained in the drive. Read-only. Nullable.</span></span>                   |
| <span data-ttu-id="84875-172">root</span><span class="sxs-lookup"><span data-stu-id="84875-172">root</span></span>         | [<span data-ttu-id="84875-173">driveitem</span><span class="sxs-lookup"><span data-stu-id="84875-173">driveitem</span></span>](driveitem.md)            | <span data-ttu-id="84875-p114">La carpeta raíz de la unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="84875-p114">The root folder of the drive. Read-only.</span></span>                                 |
| <span data-ttu-id="84875-176">special</span><span class="sxs-lookup"><span data-stu-id="84875-176">special</span></span>      | <span data-ttu-id="84875-177">Colección [driveitem](driveitem.md)</span><span class="sxs-lookup"><span data-stu-id="84875-177">[driveitem](driveitem.md) collection</span></span> | <span data-ttu-id="84875-p115">Colección de carpetas comunes disponibles en OneDrive. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="84875-p115">Collection of common folders available in OneDrive. Read-only. Nullable.</span></span> |

## <a name="methods"></a><span data-ttu-id="84875-181">Métodos</span><span class="sxs-lookup"><span data-stu-id="84875-181">Methods</span></span>

<span data-ttu-id="84875-182">Los métodos siguientes están disponibles para los recursos de la unidad.</span><span class="sxs-lookup"><span data-stu-id="84875-182">The following methods are available for drive resources.</span></span>

| <span data-ttu-id="84875-183">Método</span><span class="sxs-lookup"><span data-stu-id="84875-183">Method</span></span>                                                | <span data-ttu-id="84875-184">Ruta de acceso a REST</span><span class="sxs-lookup"><span data-stu-id="84875-184">REST Path</span></span>                        |
| :---------------------------------------------------- | :------------------------------- |
| [<span data-ttu-id="84875-185">Obtener unidad predeterminado del usuario</span><span class="sxs-lookup"><span data-stu-id="84875-185">Get user's default drive</span></span>](../api/drive_get.md)       | `GET /me/drive`                  |
| [<span data-ttu-id="84875-186">Obtener unidad de otro usuario</span><span class="sxs-lookup"><span data-stu-id="84875-186">Get another user's drive</span></span>](../api/drive_get.md)       | `GET /users/{user-id}/drive`     |
| [<span data-ttu-id="84875-187">Obtener la carpeta raíz de una unidad</span><span class="sxs-lookup"><span data-stu-id="84875-187">Get root folder for a drive</span></span>](../api/item_get.md)     | `GET /drives/{drive-id}/root`    |
| [<span data-ttu-id="84875-188">Enumerar elementos en una unidad</span><span class="sxs-lookup"><span data-stu-id="84875-188">List items in a drive</span></span>](../api/item_list_children.md) | `GET /me/drive/root/children`    |
| [<span data-ttu-id="84875-189">Enumerar cambios en una unidad</span><span class="sxs-lookup"><span data-stu-id="84875-189">List changes in a drive</span></span>](../api/item_delta.md)       | `GET /me/drive/root/delta`       |
| [<span data-ttu-id="84875-190">Buscar elementos en una unidad</span><span class="sxs-lookup"><span data-stu-id="84875-190">Search items in a drive</span></span>](../api/item_search.md)      | `GET /me/drive/search(q='text')` |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "drive resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Drive"
}-->

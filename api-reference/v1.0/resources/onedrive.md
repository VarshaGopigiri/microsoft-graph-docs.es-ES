# <a name="working-with-files-in-microsoft-graph"></a><span data-ttu-id="df411-101">Trabajar con archivos en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="df411-101">Working with files in Microsoft Graph</span></span>

<span data-ttu-id="df411-p101">Puede utilizar Microsoft Graph para crear una aplicación que se conecte con archivos a través de las bibliotecas de documentos de OneDrive, OneDrive para la Empresa y SharePoint. Con Microsoft Graph puede crear una variedad de experiencias con archivos almacenados en Office 365, desde simplemente almacenar documentos de usuario a escenarios complejos de uso compartido de archivos.</span><span class="sxs-lookup"><span data-stu-id="df411-p101">You can use Microsoft Graph to create an app that connects with files across OneDrive, OneDrive for Business, and SharePoint document libraries. With Microsoft Graph, you can build a variety of experiences with files stored in Office 365, from simply storing user documents to complex file sharing scenarios.</span></span>

<span data-ttu-id="df411-104">Microsoft Graph expone dos tipos de recursos para trabajar con archivos:</span><span class="sxs-lookup"><span data-stu-id="df411-104">Microsoft Graph exposes two resource types for working with files:</span></span>

* <span data-ttu-id="df411-105">[Drive](drive.md) - Representa un contenedor lógico de archivos, como una biblioteca de documentos o OneDrive de un usuario.</span><span class="sxs-lookup"><span data-stu-id="df411-105">[Drive](drive.md) - Represents a logical container of files, like a document library or a user's OneDrive.</span></span>
* <span data-ttu-id="df411-106">[DriveItem](driveitem.md) - Representa un elemento dentro de una unidad, como un documento, una foto, un vídeo o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="df411-106">[DriveItem](driveitem.md) - Represents an item within a drive, like a document, photo, video, or folder.</span></span>

<span data-ttu-id="df411-107">La mayor parte de la interacción con archivos se produce mediante la interacción con recursos **DriveItem**.</span><span class="sxs-lookup"><span data-stu-id="df411-107">Most of the interaction with files occurs through interaction with **DriveItem** resources. The following is an example of a DriveItem resource:</span></span> <span data-ttu-id="df411-108">A continuación se muestra un ejemplo de un recurso DriveItem:</span><span class="sxs-lookup"><span data-stu-id="df411-108">The following is an example of a driveItem resource.</span></span>

```json
{
  "@content.downloadUrl":"http://public-sn3302.files.1drv.com/y2pcT7OaUEExF7EHOlpTjCE55mIUoiX7H3sx1ff6I-nP35XUTBqZlnkh9FJhWb_pf9sZ7LEpEchvDznIbQig0hWBeidpwFkOqSKCwQylisarN6T0ecAeMvantizBUzM2PA1",
  "createdDateTime": "2016-09-16T03:37:04.72Z",
  "cTag": "aYzpENDY0OEYwNkM5MUQ5RDNEITU0OTI3LjI1Ng",
  "eTag": "aRDQ2NDhGMDZDOTFEOUQzRCE1NDkyNy4w",
  "id":"D4648F06C91D9D3D!54927",
  "lastModifiedBy": {
    "user": {
      "displayName": "Daron Spektor",
      "id": "d4648f06c91d9d3d"
    }
  },
  "name":"BritishShorthair.jpg",
  "size":35212,
  "image":{
    "height":398,
    "width":273
  },
  "file": {
    "hashes":{
      "sha1Hash":"wmgPQ6jrSeMX7JP1XmstQEGM2fc="
    }
  }
}
```

<span data-ttu-id="df411-109">Los recursos **Drive** y **DriveItem** exponen los datos de tres maneras diferentes:</span><span class="sxs-lookup"><span data-stu-id="df411-109">**Drive** and **DriveItem** resources expose data in three different ways:</span></span>

* <span data-ttu-id="df411-110">Las _propiedades_ (como **id** y **name**) exponen valores simples (cadenas, números y booleanos).</span><span class="sxs-lookup"><span data-stu-id="df411-110">_Properties_ (like **id** and **name**) expose simple values (strings, numbers, Booleans).</span></span>
* <span data-ttu-id="df411-111">_Facetas_ (como **file** y **photo**) exponen valores complejos.</span><span class="sxs-lookup"><span data-stu-id="df411-111">_Facets_ (like **file** and **photo**) expose complex values.</span></span> <span data-ttu-id="df411-112">La presencia de facetas **file** o **folder** indica comportamientos y propiedades de un **DriveItem**.</span><span class="sxs-lookup"><span data-stu-id="df411-112">Facets (like file and photo) expose complex values. The presence of **file** or **folder** facets indicates behaviors and properties of a **DriveItem**.</span></span>
* <span data-ttu-id="df411-113">Las _referencias_ (como **children** y **thumbnails**) indican colecciones de otros recursos.</span><span class="sxs-lookup"><span data-stu-id="df411-113">_References_ (like **children** and **thumbnails**) point to collections of other resources.</span></span>

## <a name="commonly-accessed-resources"></a><span data-ttu-id="df411-114">Recursos de acceso frecuente</span><span class="sxs-lookup"><span data-stu-id="df411-114">Commonly accessed resources</span></span>

<span data-ttu-id="df411-115">La mayoría de las solicitudes de API para las interacciones de archivo utilizarán uno de estos recursos base para acceder a un recurso **Drive** o **DriveItem**.</span><span class="sxs-lookup"><span data-stu-id="df411-115">Most API requests for file interactions will use one of these base resources to access a **Drive** or **DriveItem**.</span></span>

| <span data-ttu-id="df411-116">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="df411-116">Path</span></span>    | <span data-ttu-id="df411-117">Recurso</span><span class="sxs-lookup"><span data-stu-id="df411-117">Resource</span></span>    |
|---------|-------------|
| `/me/drive` | <span data-ttu-id="df411-118">OneDrive del usuario</span><span class="sxs-lookup"><span data-stu-id="df411-118">User's OneDrive</span></span> |
| `/me/drives` | <span data-ttu-id="df411-119">Enumera los recursos de OneDrive disponibles para el usuario.</span><span class="sxs-lookup"><span data-stu-id="df411-119">Enumerate OneDrive resources available to the user.</span></span> |
| `/drives/{drive-id}` | <span data-ttu-id="df411-120">Accede a un **Drive** específico mediante el identificador de la unidad.</span><span class="sxs-lookup"><span data-stu-id="df411-120">Access a specific **Drive** by the drive's ID.</span></span> |
| `/drives/{drive-id}/root/children` | <span data-ttu-id="df411-121">Enumera los recursos **DriveItem** en la raíz de un **Drive** específico.</span><span class="sxs-lookup"><span data-stu-id="df411-121">Enumerate the **DriveItem** resources in the root of a specific **Drive**.</span></span> |
| `/me/drive/items/{item-id}` | <span data-ttu-id="df411-122">Accede a un **DriveItem** en el OneDrive del usuario mediante su identificador único.</span><span class="sxs-lookup"><span data-stu-id="df411-122">Access a **DriveItem** in the user's OneDrive by its unique ID.</span></span> |
| `/me/drive/special/{special-id}` | <span data-ttu-id="df411-123">Accede a una carpeta con nombre especial en el OneDrive del usuario mediante su nombre conocido.</span><span class="sxs-lookup"><span data-stu-id="df411-123">Access a special (named) folder in the user's OneDrive by its known name.</span></span> |
| `/users/{user-id}/drive` | <span data-ttu-id="df411-124">Accede al OneDrive de otro usuario mediante el identificador del usuario.</span><span class="sxs-lookup"><span data-stu-id="df411-124">Access another user's OneDrive by using the user's unique ID.</span></span> |
| `/groups/{group-id}/drive` | <span data-ttu-id="df411-125">Accede a la biblioteca de documentos predeterminada de un grupo mediante el identificador único del grupo.</span><span class="sxs-lookup"><span data-stu-id="df411-125">Access the default document library for a group by the group's unique ID.</span></span> |
| `/shares/{share-id}` | <span data-ttu-id="df411-126">Accede a un **DriveItem** mediante su **sharedId** o su dirección URL compartida.</span><span class="sxs-lookup"><span data-stu-id="df411-126">Access a **DriveItem** by its **sharedId** or sharing URL.</span></span> |

<span data-ttu-id="df411-127">Además de dirigirse a un **DriveItem** dentro de un **Drive** mediante el identificador único, su aplicación también puede dirigirse a un **DriveItem** mediante la ruta de acceso relativa de un recurso conocido.</span><span class="sxs-lookup"><span data-stu-id="df411-127">In addition to addressing a **DriveItem** within a **Drive** by unique ID, your app can also address a **DriveItem** by relative path from a known resource. To address using a path, the colon () character is used to escape the relative path. This table provides an example of different ways to use the colon character to address an item by path.</span></span>
<span data-ttu-id="df411-128">Para acceder mediante una ruta de acceso, se utiliza el carácter de los dos puntos (`:`) para salir de la ruta de acceso relativa.</span><span class="sxs-lookup"><span data-stu-id="df411-128">To address using a path, the colon (`:`) character is used to escape the relative path.</span></span>
<span data-ttu-id="df411-129">Esta tabla proporciona un ejemplo de las diferentes maneras de utilizar el carácter de los dos puntos para dirigirse a un elemento mediante la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="df411-129">This table provides an example of different ways to use the colon character to address an item by path.</span></span>

| <span data-ttu-id="df411-130">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="df411-130">Path</span></span> | <span data-ttu-id="df411-131">Recurso</span><span class="sxs-lookup"><span data-stu-id="df411-131">Resource</span></span> |
|---|---|
| `/me/drive/root:/path/to/file` | <span data-ttu-id="df411-132">Accede a un **DriveItem** mediante la ruta de acceso relativa a la carpeta raíz del OneDrive del usuario.</span><span class="sxs-lookup"><span data-stu-id="df411-132">Access a **DriveItem** by path relative to the user's OneDrive root folder.</span></span> |
| `/me/drive/items/{item-id}:/path/to/file` | <span data-ttu-id="df411-133">Accede a un **DriveItem** mediante la ruta de acceso relativa a otro elemento (un **DriveItem** con una faceta **folder**).</span><span class="sxs-lookup"><span data-stu-id="df411-133">Access a **DriveItem** by path relative to another item (a **DriveItem** with a **folder** facet).</span></span> |
| `/me/drive/root:/path/to/folder:/children` | <span data-ttu-id="df411-134">Enumera los elementos secundarios de un **DriveItem** mediante la ruta de acceso relativa a la raíz del OneDrive del usuario.</span><span class="sxs-lookup"><span data-stu-id="df411-134">List the children of a **DriveItem** by path relative to the root of the user's OneDrive.</span></span> |
| `/me/drive/items/{item-id}:/path/to/folder:/children` | <span data-ttu-id="df411-135">Enumera los elementos secundarios de un **DriveItem** mediante la ruta de acceso relativa a otro elemento.</span><span class="sxs-lookup"><span data-stu-id="df411-135">List the children of a **DriveItem** by path relative to another item.</span></span> |

## <a name="drive-resource"></a><span data-ttu-id="df411-136">Recurso Drive</span><span class="sxs-lookup"><span data-stu-id="df411-136">Drive resource</span></span>

<span data-ttu-id="df411-137">El [recurso Drive](drive.md) es el objeto de nivel superior dentro del OneDrive de un usuario o de una biblioteca de documentos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="df411-137">The [Drive resource](drive.md) is the top-level object within a user's OneDrive or a SharePoint document library. Nearly all files operations will start by addressing a specific drive resource.</span></span>
<span data-ttu-id="df411-138">Casi todas las operaciones de archivos comienzan con el direccionamiento a un recurso de unidad específico.</span><span class="sxs-lookup"><span data-stu-id="df411-138">The Drive resource is the top-level object within a user's OneDrive or a SharePoint document library. Nearly all files operations will start by addressing a specific drive resource.</span></span>

<span data-ttu-id="df411-139">Un recurso Drive puede tratarse mediante el identificador único de la unidad o mediante la unidad predeterminada de un [usuario](user.md), [grupo](group.md) u organización.</span><span class="sxs-lookup"><span data-stu-id="df411-139">A drive resource can be addressed either by the drive's unique ID or by the default drive for a [User](user.md), [Group](group.md), or organization.</span></span> 

## <a name="driveitem-resource"></a><span data-ttu-id="df411-140">Recurso DriveItem</span><span class="sxs-lookup"><span data-stu-id="df411-140">DriveItem resource</span></span>

<span data-ttu-id="df411-141">Los [DriveItems](driveitem.md) son los objetos que hay en el sistema de archivos de una unidad.</span><span class="sxs-lookup"><span data-stu-id="df411-141">[DriveItems](driveitem.md) are the objects inside a drive's file system.</span></span>
<span data-ttu-id="df411-142">Se puede acceder a ellos a través de su **identificador**, mediante la sintaxis `/items/{item-id}`, o a través de su ruta de acceso al sistema de archivos, mediante la sintaxis `/root:/path/to/item/`.</span><span class="sxs-lookup"><span data-stu-id="df411-142">DriveItems are the objects inside a drive's file system. They can be accessed by their **id** by using `/items/{item-id}` syntax, or by their file system path using the `/root:/path/to/item/` syntax.</span></span>

<span data-ttu-id="df411-143">Los DriveItems tienen _facetas_ que proporcionan datos sobre la identidad y las capacidades del elemento.</span><span class="sxs-lookup"><span data-stu-id="df411-143">DriveItems have _facets_ that provide data about the item's identity and capabilities.</span></span>

<span data-ttu-id="df411-144">Los DriveItems con una faceta **folder** actúan como contenedores de elementos y tienen una referencia **children** que indica una colección de elementos dentro de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="df411-144">DriveItems with a **folder** facet act as containers of items, and have a **children** reference, which points to a collection of items under the folder.</span></span>

## <a name="shared-folders-and-remote-items"></a><span data-ttu-id="df411-145">Carpetas compartidas y elementos remotos</span><span class="sxs-lookup"><span data-stu-id="df411-145">Shared folders and remote items</span></span>

<span data-ttu-id="df411-146">Los usuarios con cuenta personal de OneDrive pueden agregar uno o más elementos compartidos desde otra unidad a su propio OneDrive.</span><span class="sxs-lookup"><span data-stu-id="df411-146">OneDrive personal users can add one or more shared items from another drive to their own OneDrive. These shared items appear as a DriveItem in the children collection with a remoteItem facet.</span></span>
<span data-ttu-id="df411-147">Estos elementos compartidos aparecen como un **DriveItem** en la colección **children** con una faceta [remoteItem](remoteitem.md).</span><span class="sxs-lookup"><span data-stu-id="df411-147">OneDrive personal users can add one or more shared items from another drive to their own OneDrive. These shared items appear as a **DriveItem** in the **children** collection with a [remoteItem](remoteitem.md) facet.</span></span>

<span data-ttu-id="df411-148">Para obtener más información acerca de cómo trabajar con carpetas compartidas y objetos remotos, consulte [Elementos remotos y carpetas compartidas](remoteitem.md).</span><span class="sxs-lookup"><span data-stu-id="df411-148">For more information about working with shared folders and remote items, see [Remote items and shared folders](remoteitem.md).</span></span>   

## <a name="sharing-and-permissions"></a><span data-ttu-id="df411-149">Uso compartido y permisos</span><span class="sxs-lookup"><span data-stu-id="df411-149">Sharing and permissions</span></span>

<span data-ttu-id="df411-150">Una de las acciones más comunes en las bibliotecas de documentos de OneDrive y SharePoint es compartir contenido con otras personas.</span><span class="sxs-lookup"><span data-stu-id="df411-150">One of the most common actions for OneDrive and SharePoint document libraries is sharing content with other people. Microsoft Graph allows your app to create sharing links, add permissions and send invitations to items in a drive.</span></span>
<span data-ttu-id="df411-151">Microsoft Graph permite que su aplicación pueda crear [vínculos para compartir](../api/driveitem_createlink.md), [agregar permisos y enviar invitaciones](../api/driveitem_invite.md) a los elementos de una unidad.</span><span class="sxs-lookup"><span data-stu-id="df411-151">One of the most common actions for OneDrive and SharePoint document libraries is sharing content with other people. Microsoft Graph allows your app to create [sharing links](../api/driveitem_createlink.md), [add permissions and send invitations](../api/driveitem_invite.md) to items in a drive.</span></span>

<span data-ttu-id="df411-152">Microsoft Graph también permite que su aplicación pueda [acceder a contenido compartido](../api/shares_get.md) directamente desde un vínculo para compartir.</span><span class="sxs-lookup"><span data-stu-id="df411-152">Microsoft Graph also provides a way for your app to [access shared content](../api/shares_get.md) directly from a sharing link.</span></span>

 

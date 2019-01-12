---
title: Trabajar con archivos en Microsoft Graph
description: Puede utilizar Microsoft Graph para crear una aplicación que se conecte con archivos a través de las bibliotecas de documentos de OneDrive, OneDrive para la Empresa y SharePoint. Con Microsoft Graph puede crear una variedad de experiencias con archivos almacenados en Office 365, desde simplemente almacenar documentos de usuario a escenarios complejos de uso compartido de archivos.
localization_priority: Priority
ms.prod: sharepoint
ms.openlocfilehash: 7d791f983573f56744a47952aff282f822568785
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27965897"
---
# <a name="working-with-files-in-microsoft-graph"></a><span data-ttu-id="fbbbc-104">Trabajar con archivos en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="fbbbc-104">Working with files in Microsoft Graph</span></span>

> <span data-ttu-id="fbbbc-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fbbbc-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fbbbc-p103">Puede utilizar Microsoft Graph para crear una aplicación que se conecte con archivos a través de las bibliotecas de documentos de OneDrive, OneDrive para la Empresa y SharePoint. Con Microsoft Graph puede crear una variedad de experiencias con archivos almacenados en Office 365, desde simplemente almacenar documentos de usuario a escenarios complejos de uso compartido de archivos.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-p103">You can use Microsoft Graph to create an app that connects with files across OneDrive, OneDrive for Business, and SharePoint document libraries. With Microsoft Graph, you can build a variety of experiences with files stored in Office 365, from simply storing user documents to complex file sharing scenarios.</span></span>

<span data-ttu-id="fbbbc-109">Microsoft Graph expone dos tipos de recursos para trabajar con archivos:</span><span class="sxs-lookup"><span data-stu-id="fbbbc-109">Microsoft Graph exposes two resource types for working with files:</span></span>

* <span data-ttu-id="fbbbc-110">[Drive](drive.md) - Representa un contenedor lógico de archivos, como una biblioteca de documentos o OneDrive de un usuario.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-110">[Drive](drive.md) - Represents a logical container of files, like a document library or a user's OneDrive.</span></span>
* <span data-ttu-id="fbbbc-111">[DriveItem](driveitem.md) - Representa un elemento dentro de una unidad, como un documento, una foto, un vídeo o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-111">[DriveItem](driveitem.md) - Represents an item within a drive, like a document, photo, video, or folder.</span></span>

<span data-ttu-id="fbbbc-p104">La mayor parte de la interacción con archivos se produce mediante la interacción con recursos **DriveItem**. A continuación se muestra un ejemplo de un recurso DriveItem:</span><span class="sxs-lookup"><span data-stu-id="fbbbc-p104">Most of the interaction with files occurs through interaction with **DriveItem** resources. The following is an example of a DriveItem resource:</span></span>

```json
{
  "@content.downloadUrl":"https://public-sn3302.files.1drv.com/y2pcT7OaUEExF7EHOlpTjCE55mIUoiX7H3sx1ff6I-nP35XUTBqZlnkh9FJhWb_pf9sZ7LEpEchvDznIbQig0hWBeidpwFkOqSKCwQylisarN6T0ecAeMvantizBUzM2PA1",
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

<span data-ttu-id="fbbbc-114">Los recursos **Drive** y **DriveItem** exponen los datos de tres maneras diferentes:</span><span class="sxs-lookup"><span data-stu-id="fbbbc-114">**Drive** and **DriveItem** resources expose data in three different ways:</span></span>

* <span data-ttu-id="fbbbc-115">Las _propiedades_ (como **id** y **name**) exponen valores simples (cadenas, números y booleanos).</span><span class="sxs-lookup"><span data-stu-id="fbbbc-115">_Properties_ (like **id** and **name**) expose simple values (strings, numbers, Booleans).</span></span>
* <span data-ttu-id="fbbbc-p105">Las _facetas_ (como **file** y **photo**) exponen valores complejos. La presencia de facetas **file** o **folder** indica comportamientos y propiedades de un **DriveItem**.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-p105">_Facets_ (like **file** and **photo**) expose complex values. The presence of **file** or **folder** facets indicates behaviors and properties of a **DriveItem**.</span></span>
* <span data-ttu-id="fbbbc-118">Las _referencias_ (como **children** y **thumbnails**) indican colecciones de otros recursos.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-118">_References_ (like **children** and **thumbnails**) point to collections of other resources.</span></span>

## <a name="commonly-accessed-resources"></a><span data-ttu-id="fbbbc-119">Recursos de acceso frecuente</span><span class="sxs-lookup"><span data-stu-id="fbbbc-119">Commonly accessed resources</span></span>

<span data-ttu-id="fbbbc-120">La mayoría de las solicitudes de API para las interacciones de archivo utilizarán uno de estos recursos base para acceder a un recurso **Drive** o **DriveItem**.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-120">Most API requests for file interactions will use one of these base resources to access a **Drive** or **DriveItem**.</span></span>

| <span data-ttu-id="fbbbc-121">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="fbbbc-121">Path</span></span>    | <span data-ttu-id="fbbbc-122">Recurso</span><span class="sxs-lookup"><span data-stu-id="fbbbc-122">Resource</span></span>    |
|---------|-------------|
| `/me/drive` | <span data-ttu-id="fbbbc-123">OneDrive del usuario</span><span class="sxs-lookup"><span data-stu-id="fbbbc-123">User's OneDrive</span></span> |
| `/me/drives` | <span data-ttu-id="fbbbc-124">Enumera los recursos de OneDrive disponibles para el usuario.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-124">Enumerate OneDrive resources available to the user.</span></span> |
| `/drives/{drive-id}` | <span data-ttu-id="fbbbc-125">Accede a un **Drive** específico mediante el identificador de la unidad.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-125">Access a specific **Drive** by the drive's ID.</span></span> |
| `/drives/{drive-id}/root/children` | <span data-ttu-id="fbbbc-126">Enumera los recursos **DriveItem** en la raíz de un **Drive** específico.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-126">Enumerate the **DriveItem** resources in the root of a specific **Drive**.</span></span> |
| `/me/drive/items/{item-id}` | <span data-ttu-id="fbbbc-127">Accede a un **DriveItem** en el OneDrive del usuario mediante su identificador único.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-127">Access a **DriveItem** in the user's OneDrive by its unique ID.</span></span> |
| `/me/drive/special/{special-id}` | <span data-ttu-id="fbbbc-128">Accede a una carpeta con nombre especial en el OneDrive del usuario mediante su nombre conocido.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-128">Access a special (named) folder in the user's OneDrive by its known name.</span></span> |
| `/users/{user-id}/drive` | <span data-ttu-id="fbbbc-129">Accede al OneDrive de otro usuario mediante el identificador del usuario.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-129">Access another user's OneDrive by using the user's unique ID.</span></span> |
| `/groups/{group-id}/drive` | <span data-ttu-id="fbbbc-130">Accede a la biblioteca de documentos predeterminada de un grupo mediante el identificador único del grupo.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-130">Access the default document library for a group by the group's unique ID.</span></span> |
| `/shares/{share-id}` | <span data-ttu-id="fbbbc-131">Accede a un **DriveItem** mediante su **sharedId** o su dirección URL compartida.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-131">Access a **DriveItem** by its **sharedId** or sharing URL.</span></span> |

<span data-ttu-id="fbbbc-p106">Además de dirigirse a un **DriveItem** dentro de un **Drive** mediante el identificador único, su aplicación también puede dirigirse a un **DriveItem** mediante la ruta de acceso relativa de un recurso conocido. Para acceder mediante una ruta de acceso, se utiliza el carácter de los dos puntos (`:`) para salir de la ruta de acceso relativa. Esta tabla proporciona un ejemplo de las diferentes maneras de utilizar el carácter de los dos puntos para dirigirse a un elemento mediante la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-p106">In addition to addressing a **DriveItem** within a **Drive** by unique ID, your app can also address a **DriveItem** by relative path from a known resource. To address using a path, the colon (`:`) character is used to escape the relative path. This table provides an example of different ways to use the colon character to address an item by path.</span></span>

| <span data-ttu-id="fbbbc-135">Path</span><span class="sxs-lookup"><span data-stu-id="fbbbc-135">Path</span></span> | <span data-ttu-id="fbbbc-136">Recurso</span><span class="sxs-lookup"><span data-stu-id="fbbbc-136">Resource</span></span> |
|---|---|
| `/me/drive/root:/path/to/file` | <span data-ttu-id="fbbbc-137">Accede a un **DriveItem** mediante la ruta de acceso relativa a la carpeta raíz del OneDrive del usuario.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-137">Access a **DriveItem** by path relative to the user's OneDrive root folder.</span></span> |
| `/me/drive/items/{item-id}:/path/to/file` | <span data-ttu-id="fbbbc-138">Accede a un **DriveItem** mediante la ruta de acceso relativa a otro elemento (un **DriveItem** con una faceta **folder**).</span><span class="sxs-lookup"><span data-stu-id="fbbbc-138">Access a **DriveItem** by path relative to another item (a **DriveItem** with a **folder** facet).</span></span> |
| `/me/drive/root:/path/to/folder:/children` | <span data-ttu-id="fbbbc-139">Enumera los elementos secundarios de un **DriveItem** mediante la ruta de acceso relativa a la raíz del OneDrive del usuario.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-139">List the children of a **DriveItem** by path relative to the root of the user's OneDrive.</span></span> |
| `/me/drive/items/{item-id}:/path/to/folder:/children` | <span data-ttu-id="fbbbc-140">Enumera los elementos secundarios de un **DriveItem** mediante la ruta de acceso relativa a otro elemento.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-140">List the children of a **DriveItem** by path relative to another item.</span></span> |

## <a name="drive-resource"></a><span data-ttu-id="fbbbc-141">Recurso Drive</span><span class="sxs-lookup"><span data-stu-id="fbbbc-141">Drive resource</span></span>

<span data-ttu-id="fbbbc-p107">El [recurso Drive](drive.md) es el objeto de nivel superior dentro del OneDrive de un usuario o de una biblioteca de documentos de SharePoint. Casi todas las operaciones de archivos comienzan con el direccionamiento a un recurso de unidad específico.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-p107">The [Drive resource](drive.md) is the top-level object within a user's OneDrive or a SharePoint document library. Nearly all files operations will start by addressing a specific drive resource.</span></span>

<span data-ttu-id="fbbbc-144">Un recurso Drive puede tratarse mediante el identificador único de la unidad o mediante la unidad predeterminada de un [usuario](user.md), [grupo](group.md) u organización.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-144">A drive resource can be addressed either by the drive's unique ID or by the default drive for a [User](user.md), [Group](group.md), or organization.</span></span> 

## <a name="driveitem-resource"></a><span data-ttu-id="fbbbc-145">Recurso DriveItem</span><span class="sxs-lookup"><span data-stu-id="fbbbc-145">DriveItem resource</span></span>

<span data-ttu-id="fbbbc-p108">Los [DriveItems](driveitem.md) son los objetos que hay en el sistema de archivos de una unidad. Se puede acceder a ellos a través de su **identificador**, mediante la sintaxis `/items/{item-id}`, o a través de su ruta de acceso al sistema de archivos, mediante la sintaxis `/root:/path/to/item/`. </span><span class="sxs-lookup"><span data-stu-id="fbbbc-p108">[DriveItems](driveitem.md) are the objects inside a drive's file system. They can be accessed by their **id** by using `/items/{item-id}` syntax, or by their file system path using the `/root:/path/to/item/` syntax.</span></span>

<span data-ttu-id="fbbbc-148">Los DriveItems tienen _facetas_ que proporcionan datos sobre la identidad y las capacidades del elemento.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-148">DriveItems have _facets_ that provide data about the item's identity and capabilities.</span></span>

<span data-ttu-id="fbbbc-149">Los DriveItems con una faceta **folder** actúan como contenedores de elementos y tienen una referencia **children** que indica una colección de elementos dentro de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-149">DriveItems with a **folder** facet act as containers of items, and have a **children** reference, which points to a collection of items under the folder.</span></span>

## <a name="shared-folders-and-remote-items"></a><span data-ttu-id="fbbbc-150">Carpetas compartidas y elementos remotos</span><span class="sxs-lookup"><span data-stu-id="fbbbc-150">Shared folders and remote items</span></span>

<span data-ttu-id="fbbbc-p109">Los usuarios con cuenta personal de OneDrive pueden agregar uno o más elementos compartidos desde otra unidad a su propio OneDrive. Estos elementos compartidos aparecen como un **DriveItem** en la colección **children** con una faceta [remoteItem](remoteitem.md).</span><span class="sxs-lookup"><span data-stu-id="fbbbc-p109">OneDrive personal users can add one or more shared items from another drive to their own OneDrive. These shared items appear as a **DriveItem** in the **children** collection with a [remoteItem](remoteitem.md) facet.</span></span>

<span data-ttu-id="fbbbc-153">Para obtener más información acerca de cómo trabajar con carpetas compartidas y objetos remotos, consulte [Elementos remotos y carpetas compartidas](remoteitem.md).</span><span class="sxs-lookup"><span data-stu-id="fbbbc-153">For more information about working with shared folders and remote items, see [Remote items and shared folders](remoteitem.md).</span></span>   

## <a name="sharing-and-permissions"></a><span data-ttu-id="fbbbc-154">Uso compartido y permisos</span><span class="sxs-lookup"><span data-stu-id="fbbbc-154">Sharing and permissions</span></span>

<span data-ttu-id="fbbbc-p110">Una de las acciones más comunes en las bibliotecas de documentos de OneDrive y SharePoint es compartir contenido con otras personas. Microsoft Graph permite que su aplicación pueda crear [vínculos para compartir](../api/driveitem-createlink.md), [agregar permisos y enviar invitaciones](../api/driveitem-invite.md) a los elementos de una unidad.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-p110">One of the most common actions for OneDrive and SharePoint document libraries is sharing content with other people. Microsoft Graph allows your app to create [sharing links](../api/driveitem-createlink.md), [add permissions and send invitations](../api/driveitem-invite.md) to items in a drive.</span></span>

<span data-ttu-id="fbbbc-157">Microsoft Graph también permite que su aplicación pueda [acceder a contenido compartido](../api/shares-get.md) directamente desde un vínculo para compartir.</span><span class="sxs-lookup"><span data-stu-id="fbbbc-157">Microsoft Graph also provides a way for your app to [access shared content](../api/shares-get.md) directly from a sharing link.</span></span>

 

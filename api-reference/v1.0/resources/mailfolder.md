---
title: Tipo de recurso mailFolder
description: Carpeta de recurso en el buzón de un usuario, como Bandeja de entrada y Borradores. Las carpetas de correo pueden contener mensajes, otros elementos de Outlook y carpetas de correo secundarias.
localization_priority: Priority
ms.openlocfilehash: 32af125f57e02394c4d01913aaf783df11809242
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888161"
---
# <a name="mailfolder-resource-type"></a><span data-ttu-id="76e31-104">Tipo de recurso mailFolder</span><span class="sxs-lookup"><span data-stu-id="76e31-104">mailFolder resource type</span></span>

<span data-ttu-id="76e31-105">Carpeta de recurso en el buzón de un usuario, como Bandeja de entrada y Borradores.</span><span class="sxs-lookup"><span data-stu-id="76e31-105">A mail folder in a user's mailbox, such as Inbox and Drafts.</span></span> <span data-ttu-id="76e31-106">Las carpetas de correo pueden contener mensajes, otros elementos de Outlook y carpetas de correo secundarias.</span><span class="sxs-lookup"><span data-stu-id="76e31-106">Mail folders can contain messages, other Outlook items, and child mail folders.</span></span>

<span data-ttu-id="76e31-107">Este recurso es compatible con el uso de una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de las adiciones incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/mailfolder-delta.md).</span><span class="sxs-lookup"><span data-stu-id="76e31-107">This resource supports using [delta query](/graph/delta-query-overview) to track incremental additions, deletions, and updates, by providing a [delta](../api/mailfolder-delta.md) function.</span></span>

<span data-ttu-id="76e31-108">**Nombres de carpeta conocidos**</span><span class="sxs-lookup"><span data-stu-id="76e31-108">**Well-known folder names**</span></span>

<span data-ttu-id="76e31-109">Outlook crea determinadas carpetas para los usuarios de manera predeterminada.</span><span class="sxs-lookup"><span data-stu-id="76e31-109">Outlook creates certain folders for users by default.</span></span> <span data-ttu-id="76e31-110">En lugar de usar el valor de **identificador de** carpeta correspondiente, para su comodidad, puede usar los nombres de carpeta conocidas de la siguiente tabla al obtener acceso a estas carpetas.</span><span class="sxs-lookup"><span data-stu-id="76e31-110">Instead of using the corresponding folder **id** value, for convenience, you can use the well-known folder names from the table below when accessing these folders.</span></span> <span data-ttu-id="76e31-111">Por ejemplo, puede obtener la carpeta Borradores utilizando su nombre Well-known con la siguiente consulta.</span><span class="sxs-lookup"><span data-stu-id="76e31-111">For example, you can get the Drafts folder using its well-known name with the following query.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/drafts
```

<span data-ttu-id="76e31-112">Nombres conocidos trabajar independientemente de la configuración regional del buzón de correo del usuario, por lo que la consulta anterior devolverá siempre carpeta de borradores del usuario, independientemente de cómo se denomina.</span><span class="sxs-lookup"><span data-stu-id="76e31-112">Well-known names work regardless of the locale of the user's mailbox, so the above query will always return the user's Drafts folder regardless of how it is named.</span></span>

| <span data-ttu-id="76e31-113">Nombre de la carpeta conocidos</span><span class="sxs-lookup"><span data-stu-id="76e31-113">Well-known folder name</span></span> | <span data-ttu-id="76e31-114">Description</span><span class="sxs-lookup"><span data-stu-id="76e31-114">Description</span></span> |
|:-----------------------|:------------|
| <span data-ttu-id="76e31-115">archivo</span><span class="sxs-lookup"><span data-stu-id="76e31-115">archive</span></span> | <span data-ttu-id="76e31-116">Los mensajes de la carpeta de archivo se envían a cuando se usa la característica de archivo de One_Click en los clientes de Outlook que lo admitan.</span><span class="sxs-lookup"><span data-stu-id="76e31-116">The archive folder messages are sent to when using the One_Click Archive feature in Outlook clients that support it.</span></span> <span data-ttu-id="76e31-117">**Nota:** no es el mismo que la característica de buzón de archivo de Exchange online.</span><span class="sxs-lookup"><span data-stu-id="76e31-117">**Note:** this is not the same as the Archive Mailbox feature of Exchange online.</span></span> |
| <span data-ttu-id="76e31-118">desorden</span><span class="sxs-lookup"><span data-stu-id="76e31-118">clutter</span></span> | <span data-ttu-id="76e31-119">Los mensajes con prioridad baja desorden carpeta se mueven a cuando se usa la característica de desorden.</span><span class="sxs-lookup"><span data-stu-id="76e31-119">The clutter folder low-priority messages are moved to when using the Clutter feature.</span></span> |
| <span data-ttu-id="76e31-120">conflictos</span><span class="sxs-lookup"><span data-stu-id="76e31-120">conflicts</span></span> | <span data-ttu-id="76e31-121">La carpeta que contiene los elementos en conflicto en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="76e31-121">The folder that contains conflicting items in the mailbox.</span></span> |
| <span data-ttu-id="76e31-122">conversationhistory</span><span class="sxs-lookup"><span data-stu-id="76e31-122">conversationhistory</span></span> | <span data-ttu-id="76e31-123">La carpeta donde Skype guarda las conversaciones de mensajería instantánea (si está configurada Skype para ello).</span><span class="sxs-lookup"><span data-stu-id="76e31-123">The folder where Skype saves IM conversations (if Skype is configured to do so).</span></span> |
| <span data-ttu-id="76e31-124">deleteditems</span><span class="sxs-lookup"><span data-stu-id="76e31-124">deleteditems</span></span> | <span data-ttu-id="76e31-125">Cuando se eliminan, se mueven los elementos de carpeta a.</span><span class="sxs-lookup"><span data-stu-id="76e31-125">The folder items are moved to when they are deleted.</span></span> |
| <span data-ttu-id="76e31-126">borradores</span><span class="sxs-lookup"><span data-stu-id="76e31-126">drafts</span></span> | <span data-ttu-id="76e31-127">La carpeta que contiene los mensajes no enviados.</span><span class="sxs-lookup"><span data-stu-id="76e31-127">The folder that contains unsent messages.</span></span> |
| <span data-ttu-id="76e31-128">Bandeja de entrada</span><span class="sxs-lookup"><span data-stu-id="76e31-128">inbox</span></span> | <span data-ttu-id="76e31-129">La carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="76e31-129">The inbox folder.</span></span> |
| <span data-ttu-id="76e31-130">junkemail</span><span class="sxs-lookup"><span data-stu-id="76e31-130">junkemail</span></span> | <span data-ttu-id="76e31-131">La carpeta correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="76e31-131">The junk email folder.</span></span> |
| <span data-ttu-id="76e31-132">localfailures</span><span class="sxs-lookup"><span data-stu-id="76e31-132">localfailures</span></span> | <span data-ttu-id="76e31-133">La carpeta que contiene los elementos que existen en el cliente local pero no se podrían cargar en el servidor.</span><span class="sxs-lookup"><span data-stu-id="76e31-133">The folder that contains items that exist on the local client but could not be uploaded to the server.</span></span> |
| <span data-ttu-id="76e31-134">msgfolderroot</span><span class="sxs-lookup"><span data-stu-id="76e31-134">msgfolderroot</span></span> | <span data-ttu-id="76e31-135">La carpeta "Parte superior del almacén de información".</span><span class="sxs-lookup"><span data-stu-id="76e31-135">The "Top of Information Store" folder.</span></span> <span data-ttu-id="76e31-136">Esta carpeta es la carpeta principal para las carpetas que se muestran en los clientes de correo normal, como la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="76e31-136">This folder is the parent folder for folders that are displayed in normal mail clients, such as the inbox.</span></span> |
| <span data-ttu-id="76e31-137">Bandeja de salida</span><span class="sxs-lookup"><span data-stu-id="76e31-137">outbox</span></span> | <span data-ttu-id="76e31-138">La carpeta Bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="76e31-138">The outbox folder.</span></span> |
| <span data-ttu-id="76e31-139">recoverableitemsdeletions</span><span class="sxs-lookup"><span data-stu-id="76e31-139">recoverableitemsdeletions</span></span> | <span data-ttu-id="76e31-140">La carpeta que contiene elementos eliminados temporalmente: eliminado desde la carpeta Elementos eliminados, o al presionar MAYÚS + SUPR en Outlook.</span><span class="sxs-lookup"><span data-stu-id="76e31-140">The folder that contains soft-deleted items: deleted either from the Deleted Items folder, or by pressing shift+delete in Outlook.</span></span> <span data-ttu-id="76e31-141">Esta carpeta no está visible en cualquier cliente de correo electrónico de Outlook, pero los usuarios finales pueden interactuar con él a través de la característica **Recuperar elementos eliminados del servidor** en Outlook o Outlook en el web.</span><span class="sxs-lookup"><span data-stu-id="76e31-141">This folder is not visible in any Outlook email client, but end users can interact with it through the **Recover Deleted Items from Server** feature in Outlook or Outlook on the web.</span></span> |
| <span data-ttu-id="76e31-142">programado</span><span class="sxs-lookup"><span data-stu-id="76e31-142">scheduled</span></span> | <span data-ttu-id="76e31-143">La carpeta que contiene los mensajes que están programados para volver a aparecer en la Bandeja de entrada mediante la característica de programación de Outlook para iOS.</span><span class="sxs-lookup"><span data-stu-id="76e31-143">The folder that contains messages that are scheduled to reappear in the inbox using the Schedule feature in Outlook for iOS.</span></span> |
| <span data-ttu-id="76e31-144">SearchFolders</span><span class="sxs-lookup"><span data-stu-id="76e31-144">searchfolders</span></span> | <span data-ttu-id="76e31-145">La carpeta principal para todas las carpetas de búsqueda definidas en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="76e31-145">The parent folder for all search folders defined in the user's mailbox.</span></span> |
| <span data-ttu-id="76e31-146">elementos enviados</span><span class="sxs-lookup"><span data-stu-id="76e31-146">sentitems</span></span> | <span data-ttu-id="76e31-147">La carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="76e31-147">The sent items folder.</span></span> |
| <span data-ttu-id="76e31-148">serverfailures</span><span class="sxs-lookup"><span data-stu-id="76e31-148">serverfailures</span></span> | <span data-ttu-id="76e31-149">La carpeta que contiene los elementos que existen en el servidor, pero no se pudieron sincronizar para el cliente local.</span><span class="sxs-lookup"><span data-stu-id="76e31-149">The folder that contains items that exist on the server but could not be synchronized to the local client.</span></span> |
| <span data-ttu-id="76e31-150">syncissues</span><span class="sxs-lookup"><span data-stu-id="76e31-150">syncissues</span></span> | <span data-ttu-id="76e31-151">La carpeta que contiene los registros de sincronización creados por Outlook.</span><span class="sxs-lookup"><span data-stu-id="76e31-151">The folder that contains synchronization logs created by Outlook.</span></span> |

## <a name="methods"></a><span data-ttu-id="76e31-152">Métodos</span><span class="sxs-lookup"><span data-stu-id="76e31-152">Methods</span></span>

| <span data-ttu-id="76e31-153">Método</span><span class="sxs-lookup"><span data-stu-id="76e31-153">Method</span></span> | <span data-ttu-id="76e31-154">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76e31-154">Return Type</span></span> | <span data-ttu-id="76e31-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="76e31-155">Description</span></span> |
|:-------|:------------|:------------|
|[<span data-ttu-id="76e31-156">Obtener mailFolder</span><span class="sxs-lookup"><span data-stu-id="76e31-156">Get mailFolder</span></span>](../api/mailfolder-get.md) | [<span data-ttu-id="76e31-157">mailFolder</span><span class="sxs-lookup"><span data-stu-id="76e31-157">mailFolder</span></span>](mailfolder.md) |<span data-ttu-id="76e31-158">Lea las propiedades y las relaciones del objeto mailFolder.</span><span class="sxs-lookup"><span data-stu-id="76e31-158">Read properties and relationships of mailFolder object.</span></span>|
|[<span data-ttu-id="76e31-159">Crear MailFolder</span><span class="sxs-lookup"><span data-stu-id="76e31-159">Create MailFolder</span></span>](../api/mailfolder-post-childfolders.md) |[<span data-ttu-id="76e31-160">MailFolder</span><span class="sxs-lookup"><span data-stu-id="76e31-160">MailFolder</span></span>](mailfolder.md)| <span data-ttu-id="76e31-161">Cree un nuevo recurso mailFolder en el actual; para ello, publique en la colección childFolders.</span><span class="sxs-lookup"><span data-stu-id="76e31-161">Create a new mailFolder under the current one by posting to the childFolders collection.</span></span>|
|[<span data-ttu-id="76e31-162">Enumerar childFolders</span><span class="sxs-lookup"><span data-stu-id="76e31-162">List childFolders</span></span>](../api/mailfolder-list-childfolders.md) |<span data-ttu-id="76e31-163">Colección [MailFolder](mailfolder.md)</span><span class="sxs-lookup"><span data-stu-id="76e31-163">[MailFolder](mailfolder.md) collection</span></span>| <span data-ttu-id="76e31-p107">Obtenga la colección de carpetas en la carpeta especificada. Puede usar el acceso directo `.../me/MailFolders` para obtener la colección de carpetas de nivel superior y navegar a otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="76e31-p107">Get the folder collection under the specified folder. You can use the `.../me/MailFolders` shortcut to get the top-level folder collection and navigate to another folder.</span></span>|
|[<span data-ttu-id="76e31-166">Crear mensaje</span><span class="sxs-lookup"><span data-stu-id="76e31-166">Create Message</span></span>](../api/mailfolder-post-messages.md) |[<span data-ttu-id="76e31-167">Message</span><span class="sxs-lookup"><span data-stu-id="76e31-167">Message</span></span>](message.md)| <span data-ttu-id="76e31-168">Cree un nuevo mensaje en el recurso mailFolder actual; para ello, publique en la colección de mensajes.</span><span class="sxs-lookup"><span data-stu-id="76e31-168">Create a new message in the current mailFolder by posting to the messages collection.</span></span>|
|[<span data-ttu-id="76e31-169">Enumerar mensajes</span><span class="sxs-lookup"><span data-stu-id="76e31-169">List messages</span></span>](../api/mailfolder-list-messages.md) |<span data-ttu-id="76e31-170">Colección [Message](message.md)</span><span class="sxs-lookup"><span data-stu-id="76e31-170">[Message](message.md) collection</span></span>| <span data-ttu-id="76e31-171">Obtenga todos los mensajes del buzón del usuario que ha iniciado sesión o esos mensajes en una carpeta especificada del buzón.</span><span class="sxs-lookup"><span data-stu-id="76e31-171">Get all the messages in the signed-in user's mailbox, or those messages in a specified folder in the mailbox.</span></span>|
|[<span data-ttu-id="76e31-172">Actualizar</span><span class="sxs-lookup"><span data-stu-id="76e31-172">Update</span></span>](../api/mailfolder-update.md) | [<span data-ttu-id="76e31-173">mailFolder</span><span class="sxs-lookup"><span data-stu-id="76e31-173">mailFolder</span></span>](mailfolder.md)|<span data-ttu-id="76e31-174">Actualice el objeto mailFolder especificado.</span><span class="sxs-lookup"><span data-stu-id="76e31-174">Update the specified mailFolder object.</span></span> |
|[<span data-ttu-id="76e31-175">Eliminar</span><span class="sxs-lookup"><span data-stu-id="76e31-175">Delete</span></span>](../api/mailfolder-delete.md) | <span data-ttu-id="76e31-176">Ninguno</span><span class="sxs-lookup"><span data-stu-id="76e31-176">None</span></span> |<span data-ttu-id="76e31-177">Elimine el objeto mailFolder especificado.</span><span class="sxs-lookup"><span data-stu-id="76e31-177">Delete the specified mailFolder object.</span></span> |
|[<span data-ttu-id="76e31-178">copy</span><span class="sxs-lookup"><span data-stu-id="76e31-178">copy</span></span>](../api/mailfolder-copy.md)|[<span data-ttu-id="76e31-179">MailFolder</span><span class="sxs-lookup"><span data-stu-id="76e31-179">MailFolder</span></span>](mailfolder.md)|<span data-ttu-id="76e31-180">Copie un objeto mailFolder y su contenido en otro objeto mailFolder.</span><span class="sxs-lookup"><span data-stu-id="76e31-180">Copy a mailFolder and its contents to another mailFolder.</span></span>|
|[<span data-ttu-id="76e31-181">delta</span><span class="sxs-lookup"><span data-stu-id="76e31-181">delta</span></span>](../api/mailfolder-delta.md)|<span data-ttu-id="76e31-182">Colección [mailFolder](mailfolder.md)</span><span class="sxs-lookup"><span data-stu-id="76e31-182">[mailFolder](mailfolder.md) collection</span></span>|<span data-ttu-id="76e31-183">Obtenga un conjunto de carpetas de correo que se hayan agregado, eliminado o quitado del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="76e31-183">Get a set of mail folders that have been added, deleted, or removed from the user's mailbox.</span></span>|
|[<span data-ttu-id="76e31-184">move</span><span class="sxs-lookup"><span data-stu-id="76e31-184">move</span></span>](../api/mailfolder-move.md)|[<span data-ttu-id="76e31-185">MailFolder</span><span class="sxs-lookup"><span data-stu-id="76e31-185">MailFolder</span></span>](mailfolder.md)|<span data-ttu-id="76e31-186">Mueva un objeto mailFolder y su contenido a otro objeto mailFolder.</span><span class="sxs-lookup"><span data-stu-id="76e31-186">Move a mailFolder and its contents to another mailFolder.</span></span>|
|<span data-ttu-id="76e31-187">**Propiedades extendidas**</span><span class="sxs-lookup"><span data-stu-id="76e31-187">**Extended properties**</span></span>| | |
|[<span data-ttu-id="76e31-188">Crear propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="76e31-188">Create single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[<span data-ttu-id="76e31-189">mailFolder</span><span class="sxs-lookup"><span data-stu-id="76e31-189">mailFolder</span></span>](mailfolder.md)  |<span data-ttu-id="76e31-190">Cree una o varias propiedades extendidas de valor único en un objeto mailFolder nuevo o existente.</span><span class="sxs-lookup"><span data-stu-id="76e31-190">Create one or more single-value extended properties in a new or existing mailFolder.</span></span>   |
|[<span data-ttu-id="76e31-191">Obtener mailFolder con propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="76e31-191">Get mailFolder with single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty-get.md)  | [<span data-ttu-id="76e31-192">mailFolder</span><span class="sxs-lookup"><span data-stu-id="76e31-192">mailFolder</span></span>](mailfolder.md) | <span data-ttu-id="76e31-193">Obtenga objetos mailFolder que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`.</span><span class="sxs-lookup"><span data-stu-id="76e31-193">Get mailFolders that contain a single-value extended property by using `$expand` or `$filter`.</span></span> |
|[<span data-ttu-id="76e31-194">Crear propiedad extendida de varios valores</span><span class="sxs-lookup"><span data-stu-id="76e31-194">Create multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [<span data-ttu-id="76e31-195">mailFolder</span><span class="sxs-lookup"><span data-stu-id="76e31-195">mailFolder</span></span>](mailfolder.md) | <span data-ttu-id="76e31-196">Cree una o varias propiedades extendidas de varios valores en un objeto mailFolder nuevo o existente.</span><span class="sxs-lookup"><span data-stu-id="76e31-196">Create one or more multi-value extended properties in a new or existing mailFolder.</span></span>  |
|[<span data-ttu-id="76e31-197">Obtener mailFolder con propiedad extendida de varios valores</span><span class="sxs-lookup"><span data-stu-id="76e31-197">Get mailFolder with multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty-get.md)  | [<span data-ttu-id="76e31-198">mailFolder</span><span class="sxs-lookup"><span data-stu-id="76e31-198">mailFolder</span></span>](mailfolder.md) | <span data-ttu-id="76e31-199">Obtenga un objeto mailFolder que contiene una propiedad extendida de varios valores mediante el uso de `$expand`.</span><span class="sxs-lookup"><span data-stu-id="76e31-199">Get a mailFolder that contains a multi-value extended property by using `$expand`.</span></span> |

## <a name="properties"></a><span data-ttu-id="76e31-200">Propiedades</span><span class="sxs-lookup"><span data-stu-id="76e31-200">Properties</span></span>

| <span data-ttu-id="76e31-201">Propiedad</span><span class="sxs-lookup"><span data-stu-id="76e31-201">Property</span></span> | <span data-ttu-id="76e31-202">Tipo</span><span class="sxs-lookup"><span data-stu-id="76e31-202">Type</span></span> | <span data-ttu-id="76e31-203">Descripción</span><span class="sxs-lookup"><span data-stu-id="76e31-203">Description</span></span> |
|:---------|:-----|:------------|
|<span data-ttu-id="76e31-204">childFolderCount</span><span class="sxs-lookup"><span data-stu-id="76e31-204">childFolderCount</span></span>|<span data-ttu-id="76e31-205">Int32</span><span class="sxs-lookup"><span data-stu-id="76e31-205">Int32</span></span>|<span data-ttu-id="76e31-206">El número de objetos mailFolder secundarios inmediatos en el objeto mailFolder actual.</span><span class="sxs-lookup"><span data-stu-id="76e31-206">The number of immediate child mailFolders in the current mailFolder.</span></span>|
|<span data-ttu-id="76e31-207">displayName</span><span class="sxs-lookup"><span data-stu-id="76e31-207">displayName</span></span>|<span data-ttu-id="76e31-208">String</span><span class="sxs-lookup"><span data-stu-id="76e31-208">String</span></span>|<span data-ttu-id="76e31-209">El nombre para mostrar del objeto mailFolder.</span><span class="sxs-lookup"><span data-stu-id="76e31-209">The mailFolder's display name.</span></span>|
|<span data-ttu-id="76e31-210">id</span><span class="sxs-lookup"><span data-stu-id="76e31-210">id</span></span>|<span data-ttu-id="76e31-211">Cadena</span><span class="sxs-lookup"><span data-stu-id="76e31-211">String</span></span>|<span data-ttu-id="76e31-212">Identificador único del mailFolder.</span><span class="sxs-lookup"><span data-stu-id="76e31-212">The mailFolder's unique identifier.</span></span>|
|<span data-ttu-id="76e31-213">parentFolderId</span><span class="sxs-lookup"><span data-stu-id="76e31-213">parentFolderId</span></span>|<span data-ttu-id="76e31-214">String</span><span class="sxs-lookup"><span data-stu-id="76e31-214">String</span></span>|<span data-ttu-id="76e31-215">El identificador único del objeto mailFolder principal del objeto mailFolder.</span><span class="sxs-lookup"><span data-stu-id="76e31-215">The unique identifier for the mailFolder's parent mailFolder.</span></span>|
|<span data-ttu-id="76e31-216">totalItemCount</span><span class="sxs-lookup"><span data-stu-id="76e31-216">totalItemCount</span></span>|<span data-ttu-id="76e31-217">Int32</span><span class="sxs-lookup"><span data-stu-id="76e31-217">Int32</span></span>|<span data-ttu-id="76e31-218">El número de elementos en el objeto mailFolder.</span><span class="sxs-lookup"><span data-stu-id="76e31-218">The number of items in the mailFolder.</span></span>|
|<span data-ttu-id="76e31-219">unreadItemCount</span><span class="sxs-lookup"><span data-stu-id="76e31-219">unreadItemCount</span></span>|<span data-ttu-id="76e31-220">Int32</span><span class="sxs-lookup"><span data-stu-id="76e31-220">Int32</span></span>|<span data-ttu-id="76e31-221">El número de elementos en el objeto mailFolder marcados como no leídos.</span><span class="sxs-lookup"><span data-stu-id="76e31-221">The number of items in the mailFolder marked as unread.</span></span>|

<span data-ttu-id="76e31-222">**Acceder a recuentos de elementos de forma eficaz**</span><span class="sxs-lookup"><span data-stu-id="76e31-222">**Access item counts efficiently**</span></span>

<span data-ttu-id="76e31-223">El `TotalItemCount` y `UnreadItemCount` las propiedades de una carpeta permiten calcular fácilmente el número de elementos de lectura en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="76e31-223">The `TotalItemCount` and `UnreadItemCount` properties of a folder allow you to conveniently compute the number of read items in the folder.</span></span>
<span data-ttu-id="76e31-224">Le permiten evitar las consultas como el siguiente que puede provocar una latencia elevada:</span><span class="sxs-lookup"><span data-stu-id="76e31-224">They let you avoid queries like the following that can incur significant latency:</span></span>

```http
https://outlook.office.com/api/v1.0/me/folders/inbox/messages?$count=true&$filter=isread%20eq%20false
```

<span data-ttu-id="76e31-225">Las carpetas de correo en Outlook pueden contener más de un tipo de elementos, por ejemplo, puede contener la Bandeja de entrada los elementos de solicitud que son distintos de los elementos de correo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="76e31-225">Mail folders in Outlook can contain more than one type of items, for example, the Inbox can contain meeting request items which are distinct from mail items.</span></span> <span data-ttu-id="76e31-226">`TotalItemCount`y `UnreadItemCount` incluir elementos de una carpeta de correo con independencia de su tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="76e31-226">`TotalItemCount` and `UnreadItemCount` include items in a mail folder irrespective of their item types.</span></span>

## <a name="relationships"></a><span data-ttu-id="76e31-227">Relaciones</span><span class="sxs-lookup"><span data-stu-id="76e31-227">Relationships</span></span>

| <span data-ttu-id="76e31-228">Relación</span><span class="sxs-lookup"><span data-stu-id="76e31-228">Relationship</span></span> | <span data-ttu-id="76e31-229">Tipo</span><span class="sxs-lookup"><span data-stu-id="76e31-229">Type</span></span> | <span data-ttu-id="76e31-230">Descripción</span><span class="sxs-lookup"><span data-stu-id="76e31-230">Description</span></span> |
|:-------------|:-----|:------------|
|<span data-ttu-id="76e31-231">childFolders</span><span class="sxs-lookup"><span data-stu-id="76e31-231">childFolders</span></span>|<span data-ttu-id="76e31-232">Colección [MailFolder](mailfolder.md)</span><span class="sxs-lookup"><span data-stu-id="76e31-232">[MailFolder](mailfolder.md) collection</span></span>|<span data-ttu-id="76e31-233">La colección de carpetas secundarias del objeto mailFolder.</span><span class="sxs-lookup"><span data-stu-id="76e31-233">The collection of child folders in the mailFolder.</span></span>|
|<span data-ttu-id="76e31-234">messageRules</span><span class="sxs-lookup"><span data-stu-id="76e31-234">messageRules</span></span> | <span data-ttu-id="76e31-235">Colección [messageRule](messagerule.md)</span><span class="sxs-lookup"><span data-stu-id="76e31-235">[messageRule](messagerule.md) collection</span></span> | <span data-ttu-id="76e31-236">Conjunto de reglas que se aplican a la Bandeja de entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="76e31-236">The collection of rules that apply to the user's Inbox folder.</span></span> |
|<span data-ttu-id="76e31-237">messages</span><span class="sxs-lookup"><span data-stu-id="76e31-237">messages</span></span>|<span data-ttu-id="76e31-238">Colección [Message](message.md)</span><span class="sxs-lookup"><span data-stu-id="76e31-238">[Message](message.md) collection</span></span>|<span data-ttu-id="76e31-239">La colección de mensajes del objeto mailFolder.</span><span class="sxs-lookup"><span data-stu-id="76e31-239">The collection of messages in the mailFolder.</span></span>|
|<span data-ttu-id="76e31-240">multiValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="76e31-240">multiValueExtendedProperties</span></span>|<span data-ttu-id="76e31-241">Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="76e31-241">[multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="76e31-p110">La colección de propiedades extendidas de varios valores definidas para el objeto mailFolder. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="76e31-p110">The collection of multi-value extended properties defined for the mailFolder. Read-only. Nullable.</span></span>|
|<span data-ttu-id="76e31-245">singleValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="76e31-245">singleValueExtendedProperties</span></span>|<span data-ttu-id="76e31-246">Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="76e31-246">[singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="76e31-p111">La colección de propiedades extendidas de valor único definidas para el objeto mailFolder. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="76e31-p111">The collection of single-value extended properties defined for the mailFolder. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="76e31-250">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="76e31-250">JSON representation</span></span>

<span data-ttu-id="76e31-251">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="76e31-251">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "childFolders",
    "messageRules",
    "messages",
    "multiValueExtendedProperties",
    "singleValueExtendedProperties"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.mailFolder",
  "@odata.annotations": [
    {
      "property": "childFolders",
      "capabilities": {
        "changeTracking": false,
        "navigability": "single",
        "searchable": false
      }
    },
    {
      "property": "messageRules",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "searchable": false
      }
    },
    {
      "property": "messages",
      "capabilities": {
        "changeTracking": true,
        "navigability": "single"
      }
    }
  ]
}-->

```json
{
  "childFolderCount": 1024,
  "displayName": "string",
  "id": "string (identifier)",
  "parentFolderId": "string",
  "totalItemCount": 1024,
  "unreadItemCount": 1024,
  "childFolders": [ { "@odata.type": "microsoft.graph.mailFolder" } ],
  "messageRules": [ { "@odata.type": "microsoft.graph.messageRule" } ],
  "messages": [ { "@odata.type": "microsoft.graph.message" } ],
  "multiValueExtendedProperties": [ { "@odata.type": "microsoft.graph.multiValueLegacyExtendedProperty" }],
  "singleValueExtendedProperties": [ { "@odata.type": "microsoft.graph.singleValueLegacyExtendedProperty" }]
}
```

## <a name="see-also"></a><span data-ttu-id="76e31-252">Consulte también</span><span class="sxs-lookup"><span data-stu-id="76e31-252">See also</span></span>

- [<span data-ttu-id="76e31-253">Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="76e31-253">Use delta query to track changes in Microsoft Graph data</span></span>](/graph/delta-query-overview)
- [<span data-ttu-id="76e31-254">Obtener los cambios incrementales en los mensajes de una carpeta</span><span class="sxs-lookup"><span data-stu-id="76e31-254">Get incremental changes to messages in a folder</span></span>](/graph/delta-query-messages)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailFolder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

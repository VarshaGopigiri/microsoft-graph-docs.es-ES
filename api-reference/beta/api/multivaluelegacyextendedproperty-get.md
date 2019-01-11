---
title: Obtener multiValueLegacyExtendedProperty
description: Expanda '.
localization_priority: Normal
ms.openlocfilehash: 2dd97797fb15641e772d27d6ffb9652fabe3c04b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27837747"
---
# <a name="get-multivaluelegacyextendedproperty"></a><span data-ttu-id="a3ac0-103">Obtener multiValueLegacyExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="a3ac0-103">Get multiValueLegacyExtendedProperty</span></span>

> <span data-ttu-id="a3ac0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a3ac0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a3ac0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a3ac0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a3ac0-106">Obtenga una instancia de recursos que contiene una propiedad extendida de varios valores mediante el uso de `$expand`.</span><span class="sxs-lookup"><span data-stu-id="a3ac0-106">Get a resource instance that contains a multi-value extended property by using `$expand`.</span></span>

<span data-ttu-id="a3ac0-107">El uso del parámetro de consulta `$expand` le permite expandir la instancia especificada con la propiedad extendida indicada.</span><span class="sxs-lookup"><span data-stu-id="a3ac0-107">Using the query parameter `$expand` allows you to get the specified instance expanded with the indicated extended property.</span></span> <span data-ttu-id="a3ac0-108">Actualmente, esta es la única forma de obtener el objeto [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) que representa una propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="a3ac0-108">This is currently the only way to get the [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) object that represents an extended property.</span></span>

<span data-ttu-id="a3ac0-109">Se admiten los siguientes recursos de usuario:</span><span class="sxs-lookup"><span data-stu-id="a3ac0-109">The following user resources are supported:</span></span>

- [<span data-ttu-id="a3ac0-110">calendar</span><span class="sxs-lookup"><span data-stu-id="a3ac0-110">calendar</span></span>](../resources/calendar.md)
- [<span data-ttu-id="a3ac0-111">contact</span><span class="sxs-lookup"><span data-stu-id="a3ac0-111">contact</span></span>](../resources/contact.md)
- [<span data-ttu-id="a3ac0-112">contactFolder</span><span class="sxs-lookup"><span data-stu-id="a3ac0-112">contactFolder</span></span>](../resources/contactfolder.md) 
- [<span data-ttu-id="a3ac0-113">event</span><span class="sxs-lookup"><span data-stu-id="a3ac0-113">event</span></span>](../resources/event.md)
- [<span data-ttu-id="a3ac0-114">mailFolder</span><span class="sxs-lookup"><span data-stu-id="a3ac0-114">mailFolder</span></span>](../resources/mailfolder.md)
- [<span data-ttu-id="a3ac0-115">message</span><span class="sxs-lookup"><span data-stu-id="a3ac0-115">message</span></span>](../resources/message.md) 
- [<span data-ttu-id="a3ac0-116">Tarea de Outlook</span><span class="sxs-lookup"><span data-stu-id="a3ac0-116">Outlook task</span></span>](../resources/outlooktask.md)
- [<span data-ttu-id="a3ac0-117">Carpeta de tareas de Outlook</span><span class="sxs-lookup"><span data-stu-id="a3ac0-117">Outlook task folder</span></span>](../resources/outlooktaskfolder.md)

<span data-ttu-id="a3ac0-118">También los siguientes recursos de grupo:</span><span class="sxs-lookup"><span data-stu-id="a3ac0-118">As well as the following group resources:</span></span>

- <span data-ttu-id="a3ac0-119">[calendar](../resources/calendar.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a3ac0-119">group [calendar](../resources/calendar.md)</span></span>
- <span data-ttu-id="a3ac0-120">[event](../resources/event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a3ac0-120">group [event](../resources/event.md)</span></span>
- <span data-ttu-id="a3ac0-121">[post](../resources/post.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a3ac0-121">group [post](../resources/post.md)</span></span> 

<span data-ttu-id="a3ac0-122">Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="a3ac0-122">See [Extended properties overview](../resources/extended-properties-overview.md) for more information about when to use open extensions or extended properties, and how to specify extended properties.</span></span>

## <a name="permissions"></a><span data-ttu-id="a3ac0-123">Permisos</span><span class="sxs-lookup"><span data-stu-id="a3ac0-123">Permissions</span></span>
<span data-ttu-id="a3ac0-124">Dependiendo del recurso está obteniendo la propiedad extendida desde y el permiso escriba (delegada o de la aplicación) se solicitud, el permiso especificado en la tabla siguiente es el requisito mínimo para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a3ac0-124">Depending on the resource you're getting the extended property from and the permission type (delegated or application) you request, the permission specified in the following table is the minimum required to call this API.</span></span> <span data-ttu-id="a3ac0-125">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a3ac0-125">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="a3ac0-126">Recurso admitido</span><span class="sxs-lookup"><span data-stu-id="a3ac0-126">Supported resource</span></span> | <span data-ttu-id="a3ac0-127">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a3ac0-127">Delegated (work or school account)</span></span> | <span data-ttu-id="a3ac0-128">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a3ac0-128">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a3ac0-129">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a3ac0-129">Application</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="a3ac0-130">calendario</span><span class="sxs-lookup"><span data-stu-id="a3ac0-130">calendar</span></span>](../resources/calendar.md) | <span data-ttu-id="a3ac0-131">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-131">Calendars.Read</span></span> | <span data-ttu-id="a3ac0-132">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-132">Calendars.Read</span></span> | <span data-ttu-id="a3ac0-133">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-133">Calendars.Read</span></span> |
| [<span data-ttu-id="a3ac0-134">contact</span><span class="sxs-lookup"><span data-stu-id="a3ac0-134">contact</span></span>](../resources/contact.md) | <span data-ttu-id="a3ac0-135">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-135">Contacts.Read</span></span> | <span data-ttu-id="a3ac0-136">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-136">Contacts.Read</span></span> | <span data-ttu-id="a3ac0-137">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-137">Contacts.Read</span></span> |
| [<span data-ttu-id="a3ac0-138">contactFolder</span><span class="sxs-lookup"><span data-stu-id="a3ac0-138">contactFolder</span></span>](../resources/contactfolder.md) | <span data-ttu-id="a3ac0-139">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-139">Contacts.Read</span></span> | <span data-ttu-id="a3ac0-140">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-140">Contacts.Read</span></span> | <span data-ttu-id="a3ac0-141">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-141">Contacts.Read</span></span> |
| [<span data-ttu-id="a3ac0-142">event</span><span class="sxs-lookup"><span data-stu-id="a3ac0-142">event</span></span>](../resources/event.md) | <span data-ttu-id="a3ac0-143">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-143">Calendars.Read</span></span> | <span data-ttu-id="a3ac0-144">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-144">Calendars.Read</span></span> |  <span data-ttu-id="a3ac0-145">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-145">Calendars.Read</span></span>|
| <span data-ttu-id="a3ac0-146">[calendar](../resources/calendar.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a3ac0-146">group [calendar](../resources/calendar.md)</span></span> | <span data-ttu-id="a3ac0-147">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a3ac0-147">Group.Read.All</span></span> | <span data-ttu-id="a3ac0-148">No admitido</span><span class="sxs-lookup"><span data-stu-id="a3ac0-148">Not supported</span></span> | <span data-ttu-id="a3ac0-149">No admitido</span><span class="sxs-lookup"><span data-stu-id="a3ac0-149">Not supported</span></span> |
| <span data-ttu-id="a3ac0-150">[event](../resources/event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a3ac0-150">group [event](../resources/event.md)</span></span> | <span data-ttu-id="a3ac0-151">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a3ac0-151">Group.Read.All</span></span> | <span data-ttu-id="a3ac0-152">No admitido</span><span class="sxs-lookup"><span data-stu-id="a3ac0-152">Not supported</span></span> | <span data-ttu-id="a3ac0-153">No admitido</span><span class="sxs-lookup"><span data-stu-id="a3ac0-153">Not supported</span></span> |
| <span data-ttu-id="a3ac0-154">[post](../resources/post.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a3ac0-154">group [post](../resources/post.md)</span></span> | <span data-ttu-id="a3ac0-155">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a3ac0-155">Group.Read.All</span></span> | <span data-ttu-id="a3ac0-156">No admitido</span><span class="sxs-lookup"><span data-stu-id="a3ac0-156">Not supported</span></span> | <span data-ttu-id="a3ac0-157">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a3ac0-157">Group.Read.All</span></span> |
| [<span data-ttu-id="a3ac0-158">mailFolder</span><span class="sxs-lookup"><span data-stu-id="a3ac0-158">mailFolder</span></span>](../resources/mailfolder.md) | <span data-ttu-id="a3ac0-159">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-159">Mail.Read</span></span> | <span data-ttu-id="a3ac0-160">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-160">Mail.Read</span></span> | <span data-ttu-id="a3ac0-161">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-161">Mail.Read</span></span> |
| [<span data-ttu-id="a3ac0-162">message</span><span class="sxs-lookup"><span data-stu-id="a3ac0-162">message</span></span>](../resources/message.md) | <span data-ttu-id="a3ac0-163">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-163">Mail.Read</span></span> | <span data-ttu-id="a3ac0-164">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-164">Mail.Read</span></span> | <span data-ttu-id="a3ac0-165">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-165">Mail.Read</span></span> |
| [<span data-ttu-id="a3ac0-166">Tarea de Outlook</span><span class="sxs-lookup"><span data-stu-id="a3ac0-166">Outlook task</span></span>](../resources/outlooktask.md) | <span data-ttu-id="a3ac0-167">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-167">Tasks.Read</span></span> | <span data-ttu-id="a3ac0-168">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-168">Tasks.Read</span></span> | <span data-ttu-id="a3ac0-169">No admitido</span><span class="sxs-lookup"><span data-stu-id="a3ac0-169">Not supported</span></span> |
| [<span data-ttu-id="a3ac0-170">Carpeta de tareas de Outlook</span><span class="sxs-lookup"><span data-stu-id="a3ac0-170">Outlook task folder</span></span>](../resources/outlooktaskfolder.md) | <span data-ttu-id="a3ac0-171">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-171">Tasks.Read</span></span> | <span data-ttu-id="a3ac0-172">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="a3ac0-172">Tasks.Read</span></span> | <span data-ttu-id="a3ac0-173">No se admite</span><span class="sxs-lookup"><span data-stu-id="a3ac0-173">Not supported</span></span> |
 
## <a name="http-request"></a><span data-ttu-id="a3ac0-174">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a3ac0-174">HTTP request</span></span>

<span data-ttu-id="a3ac0-p104">Expanda una instancia de recurso con la propiedad extendida que coincida con un filtro en la propiedad **id**. Asegúrese de aplicar la [codificación de direcciones URL](https://www.w3schools.com/tags/ref_urlencode.asp) a los caracteres de espacio de la cadena de filtro.</span><span class="sxs-lookup"><span data-stu-id="a3ac0-p104">Get a resource instance expanded with the extended property which matches a filter on the **id** property. Make sure you apply [URL encoding](https://www.w3schools.com/tags/ref_urlencode.asp) to the space characters in the filter string.</span></span>

<span data-ttu-id="a3ac0-177">Obtener una instancia de **mensaje** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a3ac0-177">Get a **message** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/messages/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/messages/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /me/mailFolders/{id}/messages/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="a3ac0-178">Obtener una instancia de **mailFolder** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a3ac0-178">Get a **mailFolder** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/mailFolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/mailFolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="a3ac0-179">Obtener una instancia de **evento** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a3ac0-179">Get an **event** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/events/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/events/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="a3ac0-180">Obtener una instancia de **calendario** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a3ac0-180">Get a **calendar** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/calendars/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/calendars/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="a3ac0-181">Obtener una instancia de **ponerse en contacto con** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a3ac0-181">Get a **contact** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/contacts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contacts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /me/contactFolders/{id}/contacts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}/contacts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="a3ac0-182">Obtener una instancia de **contactFolder** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a3ac0-182">Get a **contactFolder** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/contactfolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="a3ac0-183">Obtener una instancia de **outlookTask** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a3ac0-183">Get an **outlookTask** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/outlook/tasks/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/outlook/tasks/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /me/outlook/taskFolders/{id}/tasks/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/outlook/taskFolders/{id}/tasks/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /me/outlook/taskGroups/{id}/taskFolders/{id}/tasks/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}/tasks/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="a3ac0-184">Obtener una instancia de **outlookTaskFolder** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a3ac0-184">Get an **outlookTaskFolder** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/outlook/taskFolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/outlook/taskFolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /me/outlook/taskGroups/{id}/taskFolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="a3ac0-185">Obtener una instancia de **evento** de grupo:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a3ac0-185">Get a group **event** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /groups/{id}/events/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="a3ac0-186">Obtener una instancia de **entrada** de grupo:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a3ac0-186">Get a group **post** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /groups/{id}/threads/{id}/posts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```

## <a name="path-parameters"></a><span data-ttu-id="a3ac0-187">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="a3ac0-187">Path parameters</span></span>
|<span data-ttu-id="a3ac0-188">**Parámetro**</span><span class="sxs-lookup"><span data-stu-id="a3ac0-188">**Parameter**</span></span>|<span data-ttu-id="a3ac0-189">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a3ac0-189">**Type**</span></span>|<span data-ttu-id="a3ac0-190">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3ac0-190">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a3ac0-191">id_value</span><span class="sxs-lookup"><span data-stu-id="a3ac0-191">id_value</span></span>|<span data-ttu-id="a3ac0-192">String</span><span class="sxs-lookup"><span data-stu-id="a3ac0-192">String</span></span>|<span data-ttu-id="a3ac0-p105">El identificador de la propiedad extendida que debe coincidir. Debe tener uno de los formatos compatibles. Consulte la [Información general de las propiedades extendidas de Outlook](../resources/extended-properties-overview.md) para obtener más información. Necesario.</span><span class="sxs-lookup"><span data-stu-id="a3ac0-p105">The ID of the extended property to match. It must follow one of the supported formats. See [Outlook extended properties overview](../resources/extended-properties-overview.md) for more information. Required.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="a3ac0-197">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a3ac0-197">Request headers</span></span>
| <span data-ttu-id="a3ac0-198">Nombre</span><span class="sxs-lookup"><span data-stu-id="a3ac0-198">Name</span></span>      |<span data-ttu-id="a3ac0-199">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3ac0-199">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="a3ac0-200">Authorization</span><span class="sxs-lookup"><span data-stu-id="a3ac0-200">Authorization</span></span>  | <span data-ttu-id="a3ac0-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a3ac0-p106">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a3ac0-203">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a3ac0-203">Request body</span></span>
<span data-ttu-id="a3ac0-204">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a3ac0-204">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a3ac0-205">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a3ac0-205">Response</span></span>

<span data-ttu-id="a3ac0-206">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="a3ac0-206">If successful, this method returns a `200 OK` response code.</span></span> 

<span data-ttu-id="a3ac0-207">El cuerpo de la respuesta incluye un objeto que representa la instancia de recurso solicitada y expandida con el objeto coincidente [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="a3ac0-207">The response body includes an object representing the requested resource instance, expanded with the matching [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) object.</span></span>

## <a name="example"></a><span data-ttu-id="a3ac0-208">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a3ac0-208">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a3ac0-209">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a3ac0-209">Request</span></span>
<span data-ttu-id="a3ac0-p107">Este ejemplo obtiene y expande el evento especificado al incluir una propiedad extendida de varios valores. El filtro devuelve la propiedad extendida con un **id** que coincide con la cadena `StringArray {66f5a359-4659-4830-9070-00050ec6ac6e} Name Recreation` (la codificación de dirección URL se ha eliminado aquí para facilitar la lectura).</span><span class="sxs-lookup"><span data-stu-id="a3ac0-p107">This example gets and expands the specified event by including a multi-value extended property. The filter returns the extended property that has its **id** matching the string `StringArray {66f5a359-4659-4830-9070-00050ec6ac6e} Name Recreation` (with URL encoding removed here for ease of reading).</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/me/events('AAMkAGE1M2_bs88AACbuFiiAAA=')?$expand=multiValueExtendedProperties($filter=id%20eq%20'StringArray%20{66f5a359-4659-4830-9070-00050ec6ac6e}%20Name%20Recreation')
```
##### <a name="response"></a><span data-ttu-id="a3ac0-212">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a3ac0-212">Response</span></span>

<span data-ttu-id="a3ac0-213">El cuerpo de la respuesta incluye todas las propiedades del evento especificado y devuelve la propiedad extendida del filtro.</span><span class="sxs-lookup"><span data-stu-id="a3ac0-213">The response body includes all the properties of the specified event and extended property returned from the filter.</span></span>

<span data-ttu-id="a3ac0-p108">Nota: El objeto **event** que aparece aquí está truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a3ac0-p108">Note: The **event** object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
Content-type: application/json
{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/events/$entity",
    "@odata.id": "https://graph.microsoft.com/beta/users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/events('AAMkAGE1M2_bs88AACbuFiiAAA=')",
    "@odata.etag": "W/\"mODEKWhc/Um6lA3uPm7PPAAAm8k15A==\"",
    "id": "AAMkAGE1M2_bs88AACbuFiiAAA=",
    "start": {
        "dateTime": "2015-11-26T17:00:00.0000000",
        "timeZone": "UTC"
    },
    "end": {
        "dateTime": "2015-11-30T05:00:00.0000000",
        "timeZone": "UTC"
    },
    "organizer": {
        "emailAddress": {
            "name": "Christine Irwin",
            "address": "christine@contoso.com"
        }
    },
    "multiValueExtendedProperties@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/events('AAMkAGE1M2_bs88AACbuFiiAAA%3D')/multiValueExtendedProperties",
    "multiValueExtendedProperties": [
        {
            "id": "StringArray {66f5a359-4659-4830-9070-00050ec6ac6e} Name Recreation",
            "value": [
                "Food",
                "Hiking",
                "Swimming"
            ]
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get multiValueLegacyExtendedProperty",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

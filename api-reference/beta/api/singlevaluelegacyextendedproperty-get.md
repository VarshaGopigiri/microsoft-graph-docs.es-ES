---
title: Obtener singleValueLegacyExtendedProperty
description: Puede obtener una instancia de un solo recurso expandida con una propiedad extendida específica o una colección de instancias de recursos
localization_priority: Normal
ms.openlocfilehash: ee9d51f945650c8051badd27f1b934d03f47cc7b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27873188"
---
# <a name="get-singlevaluelegacyextendedproperty"></a><span data-ttu-id="a7eb5-103">Obtener singleValueLegacyExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="a7eb5-103">Get singleValueLegacyExtendedProperty</span></span>

> <span data-ttu-id="a7eb5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a7eb5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a7eb5-106">Puede expandir una única instancia de recursos con una propiedad extendida determinada o una colección de instancias de recursos que incluya propiedades extendidas que coinciden con un filtro.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-106">You can get a single resource instance expanded with a specific extended property, or a collection of resource instances that include extended properties matching a filter.</span></span>

<span data-ttu-id="a7eb5-107">El uso del parámetro de consulta `$expand` le permite expandir la instancia de recursos especificada con una propiedad extendida específica.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-107">Using the query parameter `$expand` allows you to get the specified resource instance expanded with a specific extended property.</span></span> <span data-ttu-id="a7eb5-108">Use un operador `$filter` y `eq` en la propiedad **id** para especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-108">Use a `$filter` and `eq` operator on the **id** property to specify the extended property.</span></span> <span data-ttu-id="a7eb5-109">Actualmente, esta es la única forma de obtener el objeto [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md) que representa una propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-109">This is currently the only way to get the [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md) object that represents an extended property.</span></span> 

<span data-ttu-id="a7eb5-110">Para obtener las instancias de recursos que tengan ciertas propiedades extendidas, use el parámetro de consulta `$filter` y aplique un operador `eq` en la propiedad **id**.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-110">To get resource instances that have certain extended properties, use the `$filter` query parameter and apply an `eq` operator on the **id** property.</span></span> <span data-ttu-id="a7eb5-111">Además, para las propiedades extendidas numéricas, aplique uno de los siguientes operadores en la propiedad **value**: `eq`, `ne`,`ge`, `gt`, `le` o `lt`.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-111">In addition, for numeric extended properties, apply one of the following operators on the **value** property: `eq`, `ne`,`ge`, `gt`, `le`, or `lt`.</span></span> <span data-ttu-id="a7eb5-112">Para las propiedades extendidas de tipo cadena, aplique un operador `contains`, `startswith`, `eq` o `ne` en **value**.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-112">For string-typed extended properties, apply a `contains`, `startswith`, `eq`, or `ne` operator on **value**.</span></span> 

<span data-ttu-id="a7eb5-113">El filtrado del nombre de la cadena (`Name`) en el **id** de una propiedad extendida distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-113">Filtering the string name (`Name`) in the **id** of an extended property is case-sensitive.</span></span> <span data-ttu-id="a7eb5-114">El filtrado de la propiedad **value** de una propiedad extendida no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-114">Filtering the **value** property of an extended property is case-insensitive.</span></span>

<span data-ttu-id="a7eb5-115">Se admiten los siguientes recursos de usuario:</span><span class="sxs-lookup"><span data-stu-id="a7eb5-115">The following user resources are supported:</span></span>

- [<span data-ttu-id="a7eb5-116">calendar</span><span class="sxs-lookup"><span data-stu-id="a7eb5-116">calendar</span></span>](../resources/calendar.md)
- [<span data-ttu-id="a7eb5-117">contact</span><span class="sxs-lookup"><span data-stu-id="a7eb5-117">contact</span></span>](../resources/contact.md)
- [<span data-ttu-id="a7eb5-118">contactFolder</span><span class="sxs-lookup"><span data-stu-id="a7eb5-118">contactFolder</span></span>](../resources/contactfolder.md) 
- [<span data-ttu-id="a7eb5-119">event</span><span class="sxs-lookup"><span data-stu-id="a7eb5-119">event</span></span>](../resources/event.md)
- [<span data-ttu-id="a7eb5-120">mailFolder</span><span class="sxs-lookup"><span data-stu-id="a7eb5-120">mailFolder</span></span>](../resources/mailfolder.md)
- [<span data-ttu-id="a7eb5-121">message</span><span class="sxs-lookup"><span data-stu-id="a7eb5-121">message</span></span>](../resources/message.md) 
- [<span data-ttu-id="a7eb5-122">Tarea de Outlook</span><span class="sxs-lookup"><span data-stu-id="a7eb5-122">Outlook task</span></span>](../resources/outlooktask.md)
- [<span data-ttu-id="a7eb5-123">Carpeta de tareas de Outlook</span><span class="sxs-lookup"><span data-stu-id="a7eb5-123">Outlook task folder</span></span>](../resources/outlooktaskfolder.md)

<span data-ttu-id="a7eb5-124">También los siguientes recursos de grupo:</span><span class="sxs-lookup"><span data-stu-id="a7eb5-124">As well as the following group resources:</span></span>

- <span data-ttu-id="a7eb5-125">[calendar](../resources/calendar.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a7eb5-125">group [calendar](../resources/calendar.md)</span></span>
- <span data-ttu-id="a7eb5-126">[event](../resources/event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a7eb5-126">group [event](../resources/event.md)</span></span>
- <span data-ttu-id="a7eb5-127">[post](../resources/post.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a7eb5-127">group [post](../resources/post.md)</span></span> 

<span data-ttu-id="a7eb5-128">Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-128">See [Extended properties overview](../resources/extended-properties-overview.md) for more information about when to use open extensions or extended properties, and how to specify extended properties.</span></span>

## <a name="permissions"></a><span data-ttu-id="a7eb5-129">Permisos</span><span class="sxs-lookup"><span data-stu-id="a7eb5-129">Permissions</span></span>
<span data-ttu-id="a7eb5-130">Dependiendo del recurso está obteniendo la propiedad extendida desde y el permiso escriba (delegada o de la aplicación) se solicitud, el permiso especificado en la tabla siguiente es el requisito mínimo para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-130">Depending on the resource you're getting the extended property from and the permission type (delegated or application) you request, the permission specified in the following table is the minimum required to call this API.</span></span> <span data-ttu-id="a7eb5-131">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a7eb5-131">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="a7eb5-132">Recurso admitido</span><span class="sxs-lookup"><span data-stu-id="a7eb5-132">Supported resource</span></span> | <span data-ttu-id="a7eb5-133">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a7eb5-133">Delegated (work or school account)</span></span> | <span data-ttu-id="a7eb5-134">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a7eb5-134">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a7eb5-135">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a7eb5-135">Application</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="a7eb5-136">calendario</span><span class="sxs-lookup"><span data-stu-id="a7eb5-136">calendar</span></span>](../resources/calendar.md) | <span data-ttu-id="a7eb5-137">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-137">Calendars.Read</span></span> | <span data-ttu-id="a7eb5-138">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-138">Calendars.Read</span></span> | <span data-ttu-id="a7eb5-139">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-139">Calendars.Read</span></span> |
| [<span data-ttu-id="a7eb5-140">contact</span><span class="sxs-lookup"><span data-stu-id="a7eb5-140">contact</span></span>](../resources/contact.md) | <span data-ttu-id="a7eb5-141">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-141">Contacts.Read</span></span> | <span data-ttu-id="a7eb5-142">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-142">Contacts.Read</span></span> | <span data-ttu-id="a7eb5-143">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-143">Contacts.Read</span></span> |
| [<span data-ttu-id="a7eb5-144">contactFolder</span><span class="sxs-lookup"><span data-stu-id="a7eb5-144">contactFolder</span></span>](../resources/contactfolder.md) | <span data-ttu-id="a7eb5-145">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-145">Contacts.Read</span></span> | <span data-ttu-id="a7eb5-146">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-146">Contacts.Read</span></span> | <span data-ttu-id="a7eb5-147">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-147">Contacts.Read</span></span> |
| [<span data-ttu-id="a7eb5-148">event</span><span class="sxs-lookup"><span data-stu-id="a7eb5-148">event</span></span>](../resources/event.md) | <span data-ttu-id="a7eb5-149">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-149">Calendars.Read</span></span> | <span data-ttu-id="a7eb5-150">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-150">Calendars.Read</span></span> |  <span data-ttu-id="a7eb5-151">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-151">Calendars.Read</span></span>|
| <span data-ttu-id="a7eb5-152">[calendar](../resources/calendar.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a7eb5-152">group [calendar](../resources/calendar.md)</span></span> | <span data-ttu-id="a7eb5-153">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a7eb5-153">Group.Read.All</span></span> | <span data-ttu-id="a7eb5-154">No admitido</span><span class="sxs-lookup"><span data-stu-id="a7eb5-154">Not supported</span></span> | <span data-ttu-id="a7eb5-155">No admitido</span><span class="sxs-lookup"><span data-stu-id="a7eb5-155">Not supported</span></span> |
| <span data-ttu-id="a7eb5-156">[event](../resources/event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a7eb5-156">group [event](../resources/event.md)</span></span> | <span data-ttu-id="a7eb5-157">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a7eb5-157">Group.Read.All</span></span> | <span data-ttu-id="a7eb5-158">No admitido</span><span class="sxs-lookup"><span data-stu-id="a7eb5-158">Not supported</span></span> | <span data-ttu-id="a7eb5-159">No admitido</span><span class="sxs-lookup"><span data-stu-id="a7eb5-159">Not supported</span></span> |
| <span data-ttu-id="a7eb5-160">[post](../resources/post.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a7eb5-160">group [post](../resources/post.md)</span></span> | <span data-ttu-id="a7eb5-161">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a7eb5-161">Group.Read.All</span></span> | <span data-ttu-id="a7eb5-162">No admitido</span><span class="sxs-lookup"><span data-stu-id="a7eb5-162">Not supported</span></span> | <span data-ttu-id="a7eb5-163">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a7eb5-163">Group.Read.All</span></span> |
| [<span data-ttu-id="a7eb5-164">mailFolder</span><span class="sxs-lookup"><span data-stu-id="a7eb5-164">mailFolder</span></span>](../resources/mailfolder.md) | <span data-ttu-id="a7eb5-165">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-165">Mail.Read</span></span> | <span data-ttu-id="a7eb5-166">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-166">Mail.Read</span></span> | <span data-ttu-id="a7eb5-167">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-167">Mail.Read</span></span> |
| [<span data-ttu-id="a7eb5-168">message</span><span class="sxs-lookup"><span data-stu-id="a7eb5-168">message</span></span>](../resources/message.md) | <span data-ttu-id="a7eb5-169">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-169">Mail.Read</span></span> | <span data-ttu-id="a7eb5-170">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-170">Mail.Read</span></span> | <span data-ttu-id="a7eb5-171">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-171">Mail.Read</span></span> |
| [<span data-ttu-id="a7eb5-172">Tarea de Outlook</span><span class="sxs-lookup"><span data-stu-id="a7eb5-172">Outlook task</span></span>](../resources/outlooktask.md) | <span data-ttu-id="a7eb5-173">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-173">Tasks.Read</span></span> | <span data-ttu-id="a7eb5-174">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-174">Tasks.Read</span></span> | <span data-ttu-id="a7eb5-175">No admitido</span><span class="sxs-lookup"><span data-stu-id="a7eb5-175">Not supported</span></span> |
| [<span data-ttu-id="a7eb5-176">Carpeta de tareas de Outlook</span><span class="sxs-lookup"><span data-stu-id="a7eb5-176">Outlook task folder</span></span>](../resources/outlooktaskfolder.md) | <span data-ttu-id="a7eb5-177">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-177">Tasks.Read</span></span> | <span data-ttu-id="a7eb5-178">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="a7eb5-178">Tasks.Read</span></span> | <span data-ttu-id="a7eb5-179">No se admite</span><span class="sxs-lookup"><span data-stu-id="a7eb5-179">Not supported</span></span> |


## <a name="http-request"></a><span data-ttu-id="a7eb5-180">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a7eb5-180">HTTP request</span></span>

#### <a name="get-a-resource-instance-expanded-with-an-extended-property-that-matches-a-filter"></a><span data-ttu-id="a7eb5-181">Expandir una instancia de recurso con una propiedad extendida que coincide con un filtro</span><span class="sxs-lookup"><span data-stu-id="a7eb5-181">GET a resource instance expanded with an extended property that matches a filter</span></span>
<span data-ttu-id="a7eb5-p106">Expanda una instancia de recurso con la propiedad extendida que coincida con un filtro en la propiedad **id**. Asegúrese de aplicar [la codificación de direcciones URL](https://www.w3schools.com/tags/ref_urlencode.asp) a los caracteres de espacio de la cadena de filtro.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-p106">Get a resource instance expanded with the extended property which matches a filter on the **id** property. Make sure you apply [URL encoding](https://www.w3schools.com/tags/ref_urlencode.asp) to the space characters in the filter string.</span></span>

<span data-ttu-id="a7eb5-184">Obtener una instancia de **mensaje** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-184">Get a **message** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/messages/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/messages/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /me/mailFolders/{id}/messages/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="a7eb5-185">Obtener una instancia de **mailFolder** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-185">Get a **mailFolder** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/mailFolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/mailFolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="a7eb5-186">Obtener una instancia de **evento** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-186">Get an **event** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/events/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/events/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="a7eb5-187">Obtener una instancia de **calendario** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-187">Get a **calendar** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/calendars/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/calendars/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="a7eb5-188">Obtener una instancia de **ponerse en contacto con** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-188">Get a **contact** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/contacts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contacts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /me/contactFolders/{id}/contacts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}/contacts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="a7eb5-189">Obtener una instancia de **contactFolder** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-189">Get a **contactFolder** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/contactfolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="a7eb5-190">Obtener una instancia de **outlookTask** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-190">Get an **outlookTask** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/outlook/tasks/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/outlook/tasks/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /me/outlook/taskFolders/{id}/tasks/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/outlook/taskFolders/{id}/tasks/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /me/outlook/taskGroups/{id}/taskFolders/{id}/tasks/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}/tasks/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="a7eb5-191">Obtener una instancia de **outlookTaskFolder** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-191">Get an **outlookTaskFolder** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/outlook/taskFolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/outlook/taskFolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /me/outlook/taskGroups/{id}/taskFolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="a7eb5-192">Obtener una instancia de **evento** de grupo:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-192">Get a group **event** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /groups/{id}/events/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="a7eb5-193">Obtener una instancia de **entrada** de grupo:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-193">Get a group **post** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /groups/{id}/threads/{id}/posts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```

#### <a name="get-resource-instances-that-include-numeric-extended-properties-matching-a-filter"></a><span data-ttu-id="a7eb5-194">Obtener instancias de recursos que incluyan propiedades extendidas numéricas que coinciden con un filtro</span><span class="sxs-lookup"><span data-stu-id="a7eb5-194">GET resource instances that include numeric extended properties matching a filter</span></span>

<span data-ttu-id="a7eb5-195">Obtenga instancias de un recurso compatible que tenga una propiedad extendida numérica que coincide con un filtro.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-195">Get instances of a supported resource that have a numeric extended property matching a filter.</span></span> <span data-ttu-id="a7eb5-196">El filtro usa un operador `eq` en la propiedad **id** y uno de los siguientes operadores en la propiedad **value**: `eq`, `ne`,`ge`, `gt` , `le` o `lt`.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-196">The filter uses an `eq` operator on the **id** property, and one of the following operators on the **value** property: `eq`, `ne`,`ge`, `gt`, `le`, or `lt`.</span></span> <span data-ttu-id="a7eb5-197">Asegúrese de aplicar Asegúrese de que confirme aplica [codificación de dirección URL](https://www.w3schools.com/tags/ref_urlencode.asp) a los siguientes caracteres en la cadena de filtro - punto y coma, barra diagonal y espacio.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-197">Make sure you apply Make sure you apply [URL encoding](https://www.w3schools.com/tags/ref_urlencode.asp) to the following characters in the filter string - colon, forward slash, and space.</span></span>

<span data-ttu-id="a7eb5-198">Las líneas de sintaxis siguientes muestran un filtro que usa un operador `eq` en el Id. y otro operador `eq` en el valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-198">The following syntax lines show a filter that uses an `eq` operator on the id, and another `eq` operator on the property value.</span></span> <span data-ttu-id="a7eb5-199">Puede sustituir el operador `eq` en el **valor** por alguno de los otros operadores (`ne`, `ge`, `gt`, `le` o `lt`) que se aplican a los valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-199">You can substitute the `eq` operator on the **value** by any one of the other operators (`ne`,`ge`, `gt`, `le`, or `lt`) that apply to numeric values.</span></span>

<span data-ttu-id="a7eb5-200">Obtener instancias de **mensaje** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-200">Get **message** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /me/mailFolders/{id}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
<span data-ttu-id="a7eb5-201">Obtener instancias de **mailFolder** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-201">Get **mailFolder** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/mailFolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/mailFolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```

<span data-ttu-id="a7eb5-202">Obtener instancias de **eventos** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-202">Get **event** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
<span data-ttu-id="a7eb5-203">Obtener instancias de **calendario** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-203">Get **calendar** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/calendars?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/calendars?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
<span data-ttu-id="a7eb5-204">Obtener instancias **póngase en contacto con** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-204">Get **contact** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/contacts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/contacts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /me/contactFolders/{id}/contacts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}/contacts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
<span data-ttu-id="a7eb5-205">Obtener instancias de **contactFolder** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-205">Get **contactFolder** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/contactfolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/contactFolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```

<span data-ttu-id="a7eb5-206">Obtener una instancia de **outlookTask** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-206">Get an **outlookTask** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/outlook/tasks?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/outlook/tasks?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /me/outlook/taskFolders/{id}/tasks?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/outlook/taskFolders/{id}/tasks?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /me/outlook/taskGroups/{id}/taskFolders/{id}/tasks?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}/tasks?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
<span data-ttu-id="a7eb5-207">Obtener una instancia de **outlookTaskFolder** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-207">Get an **outlookTaskFolder** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/outlook/taskFolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/outlook/taskFolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /me/outlook/taskGroups/{id}/taskFolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```

<span data-ttu-id="a7eb5-208">Obtener instancias de **eventos** de grupo:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-208">Get group **event** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /groups/{id}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```

<span data-ttu-id="a7eb5-209">Obtener instancias de **entrada** de grupo:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-209">Get group **post** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /groups/{id}/threads/{id}/posts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /groups/{id}/conversations/{id}/threads/{id}/posts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```

#### <a name="get-resource-instances-with-string-typed-extended-properties-matching-a-filter"></a><span data-ttu-id="a7eb5-210">Obtener instancias de recursos con propiedades extendidas de tipo cadena que coinciden con un filtro</span><span class="sxs-lookup"><span data-stu-id="a7eb5-210">GET resource instances with string-typed extended properties matching a filter</span></span>

<span data-ttu-id="a7eb5-211">Obtenga instancias del recurso **mensaje** o **evento** recursos que tienen una propiedad extendida de tipo cadena que coincide con un filtro.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-211">Get instances of the **message** or **event** resource that have a string-typed extended property matching a filter.</span></span> <span data-ttu-id="a7eb5-212">El filtro usa un operador `eq` en la propiedad **id** y uno de los siguientes operadores en la propiedad **value**: `contains`, `startswith`,`eq` o `ne`.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-212">The filter uses an `eq` operator on the **id** property, and one of the following operators on the **value** property: `contains`, `startswith`, `eq`, or `ne`.</span></span> <span data-ttu-id="a7eb5-213">Asegúrese de aplicar [la codificación de direcciones URL](https://www.w3schools.com/tags/ref_urlencode.asp) a los siguientes caracteres de la cadena de filtro: dos puntos, barra diagonal y espacio.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-213">Make sure you apply [URL encoding](https://www.w3schools.com/tags/ref_urlencode.asp) to the following characters in the filter string - colon, forward slash, and space.</span></span>


<span data-ttu-id="a7eb5-214">Obtener instancias de **mensaje** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-214">Get **message** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))
GET /users/{id|userPrincipalName}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))
GET /me/mailFolders/{id}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))

GET /me/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))
GET /users/{id|userPrincipalName}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))
GET /me/mailFolders/{id}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))

GET /me/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /me/mailFolders/{id}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')

GET /me/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
GET /users/{id|userPrincipalName}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
GET /me/mailFolders/{id}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
```

<span data-ttu-id="a7eb5-215">Obtener instancias de **eventos** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-215">Get **event** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))
GET /users/{id|userPrincipalName}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))

GET /me/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))
GET /users/{id|userPrincipalName}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))

GET /me/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')

GET /me/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
GET /users/{id|userPrincipalName}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
```

<span data-ttu-id="a7eb5-216">Obtener instancias de **eventos** de grupo:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a7eb5-216">Get group **event** instances: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /groups/{id}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))
GET /groups/{id}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))
GET /groups/{id}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /groups/{id}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
```

## <a name="path-parameters"></a><span data-ttu-id="a7eb5-217">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="a7eb5-217">Path parameters</span></span>
|<span data-ttu-id="a7eb5-218">**Parámetro**</span><span class="sxs-lookup"><span data-stu-id="a7eb5-218">**Parameter**</span></span>|<span data-ttu-id="a7eb5-219">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a7eb5-219">**Type**</span></span>|<span data-ttu-id="a7eb5-220">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a7eb5-220">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a7eb5-221">id_value</span><span class="sxs-lookup"><span data-stu-id="a7eb5-221">id_value</span></span>|<span data-ttu-id="a7eb5-222">String</span><span class="sxs-lookup"><span data-stu-id="a7eb5-222">String</span></span>|<span data-ttu-id="a7eb5-p110">El identificador de la propiedad extendida que debe coincidir. Debe tener uno de los formatos compatibles. Consulte la [Información general de las propiedades extendidas de Outlook](../resources/extended-properties-overview.md) para obtener más información. Necesario.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-p110">The ID of the extended property to match. It must follow one of the supported formats. See [Outlook extended properties overview](../resources/extended-properties-overview.md) for more information. Required.</span></span>|
|<span data-ttu-id="a7eb5-227">property_value</span><span class="sxs-lookup"><span data-stu-id="a7eb5-227">property_value</span></span> |<span data-ttu-id="a7eb5-228">Cadena</span><span class="sxs-lookup"><span data-stu-id="a7eb5-228">String</span></span>|<span data-ttu-id="a7eb5-229">El valor de la propiedad extendida que debe coincidir.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-229">The value of the extended property to match.</span></span> <span data-ttu-id="a7eb5-230">Es necesario donde aparece en la sección anterior **Solicitud HTTP**.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-230">Required where listed in the **HTTP request** section above.</span></span> <span data-ttu-id="a7eb5-231">Si {property_value} no es una cadena, asegúrese de convertir explícitamente `ep/value` en el tipo de datos Edm apropiado cuando se compare con {property_value}.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-231">If {property_value} is not a string, make sure you explicitly cast `ep/value` to the appropriate Edm data type when comparing it with {property_value}.</span></span> <span data-ttu-id="a7eb5-232">Vea la [solicitud 4](#request-4) a continuación para obtener ejemplos.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-232">See [request 4](#request-4) below for examples.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="a7eb5-233">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a7eb5-233">Request headers</span></span>
| <span data-ttu-id="a7eb5-234">Nombre</span><span class="sxs-lookup"><span data-stu-id="a7eb5-234">Name</span></span>      |<span data-ttu-id="a7eb5-235">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7eb5-235">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="a7eb5-236">Authorization</span><span class="sxs-lookup"><span data-stu-id="a7eb5-236">Authorization</span></span>  | <span data-ttu-id="a7eb5-p112">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-p112">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a7eb5-239">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a7eb5-239">Request body</span></span>
<span data-ttu-id="a7eb5-240">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-240">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a7eb5-241">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7eb5-241">Response</span></span>

<span data-ttu-id="a7eb5-242">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-242">If successful, this method returns a `200 OK` response code.</span></span>

#### <a name="get-resource-instance-using-expand"></a><span data-ttu-id="a7eb5-243">GET (OBTENER) una instancia de recurso mediante el uso de `$expand`</span><span class="sxs-lookup"><span data-stu-id="a7eb5-243">GET resource instance using `$expand`</span></span>
<span data-ttu-id="a7eb5-244">El cuerpo de la respuesta incluye un objeto que representa la instancia de recurso solicitada y expandida con el objeto coincidente [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="a7eb5-244">The response body includes an object representing the requested resource instance, expanded with the matching [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md) object.</span></span>
  
#### <a name="get-resource-instances-that-contain-an-extended-property-matching-a-filter"></a><span data-ttu-id="a7eb5-245">Obtener instancias de recurso que contienen una propiedad extendida que coincide con un filtro</span><span class="sxs-lookup"><span data-stu-id="a7eb5-245">GET resource instances that contain an extended property matching a filter</span></span>
<span data-ttu-id="a7eb5-246">El cuerpo de la respuesta incluye uno o varios objetos que representan las instancias de recurso que contienen una propiedad extendida coincidente.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-246">The response body includes one or more objects representing the resource instances that contain a matching extended property.</span></span> <span data-ttu-id="a7eb5-247">El cuerpo de la respuesta no incluye la propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-247">The response body does not include the extended property.</span></span>

## <a name="example"></a><span data-ttu-id="a7eb5-248">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a7eb5-248">Example</span></span>
#### <a name="request-1"></a><span data-ttu-id="a7eb5-249">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="a7eb5-249">Request 1</span></span>

<span data-ttu-id="a7eb5-p114">El primer ejemplo obtiene y expande el mensaje especificado al incluir una propiedad extendida de valor único. El filtro devuelve la propiedad extendida cuyo **identificador** coincide con la cadena `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (la codificación de dirección URL se ha eliminado aquí para facilitar la lectura).</span><span class="sxs-lookup"><span data-stu-id="a7eb5-p114">The first example gets and expands the specified message by including a single-value extended property. The filter returns the extended property that has its **id** matching the string `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (with URL encoding removed here for ease of reading).</span></span>

<!-- {
  "blockType": "request",
  "name": "get_singlevaluelegacyextendedproperty_1"
}-->
```http
GET https://graph.microsoft.com/beta/me/messages('AAMkAGE1M2_bs88AACHsLqWAAA=')?$expand=singleValueExtendedProperties($filter=id%20eq%20'String%20{66f5a359-4659-4830-9070-00047ec6ac6e}%20Name%20Color')
```
#### <a name="response-1"></a><span data-ttu-id="a7eb5-252">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="a7eb5-252">Response 1</span></span>
<span data-ttu-id="a7eb5-253">El cuerpo de la respuesta incluye todas las propiedades del mensaje especificado y devuelve la propiedad extendida del filtro.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-253">The response body includes all the properties of the specified message and extended property returned from the filter.</span></span>

<span data-ttu-id="a7eb5-p115">Nota: El objeto del **mensaje** que aparece aquí está truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-p115">Note: The **message** object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/messages/$entity",
    "@odata.id": "https://graph.microsoft.com/beta/users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/messages('AAMkAGE1M2_bs88AACHsLqWAAA=')",
    "@odata.etag": "W/\"CQAAABYAAACY4MQpaFz9SbqUDe4+bs88AACbyS4H\"",
    "id": "AAMkAGE1M2_bs88AACHsLqWAAA=",
    "subject": "RE: Talk about emergency prep",
    "sender": {
        "emailAddress": {
            "name": "Christine Irwin",
            "address": "christine@contoso.com"
        }
    },
    "from": null,
    "toRecipients": [
        {
            "emailAddress": {
                "name": "Christine Irwin",
                "address": "christine@contoso.com"
            }
        }
    ],
    "singleValueExtendedProperties@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/messages('AAMkAGE1M2_bs88AACHsLqWAAA%3D')/singleValueExtendedProperties",
    "singleValueExtendedProperties": [
        {
            "id": "String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color",
            "value": "Green"
        }
    ]
}
```

#### <a name="request-2"></a><span data-ttu-id="a7eb5-256">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="a7eb5-256">Request 2</span></span>

<span data-ttu-id="a7eb5-257">En el segundo ejemplo, se obtienen mensajes con la propiedad extendida de valor único de tipo cadena especificada en el filtro.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-257">The second example gets messages that have the string-typed single-value extended property specified in the filter.</span></span> <span data-ttu-id="a7eb5-258">El filtro busca una propiedad extendida que tenga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a7eb5-258">The filter looks for the extended property that has:</span></span>

- <span data-ttu-id="a7eb5-259">Un **id.** igual a la cadena `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (con la codificación de direcciones URL quitada aquí para facilitar la lectura).</span><span class="sxs-lookup"><span data-stu-id="a7eb5-259">Its **id** equal to the string `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (with URL encoding removed here for ease of reading).</span></span>

- <span data-ttu-id="a7eb5-260">Un **valor** igual a la cadena `Green`.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-260">Its **value** equal to the string `Green`.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/Me/messages?$filter=singleValueExtendedProperties%2FAny(ep%3A%20ep%2Fid%20eq%20'String%20{66f5a359-4659-4830-9070-00047ec6ac6e}%20Name%20Color'%20and%20ep%2Fvalue%20eq%20'Green')
```

#### <a name="response-2"></a><span data-ttu-id="a7eb5-261">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="a7eb5-261">Response 2</span></span>

<span data-ttu-id="a7eb5-p117">Un código de respuesta `HTTP 200 OK` indica una respuesta correcta y el cuerpo de la respuesta incluye todas las propiedades de los mensajes cuya propiedad extendida coincide con el filtro. El cuerpo de la respuesta es similar a la respuesta al [obtener una colección de mensajes](../api/user-list-messages.md). El cuerpo de la respuesta no incluye la propiedad extendida coincidente.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-p117">A successful response is indicated by an `HTTP 200 OK` response code, and the response body includes all the properties of the messages that have the extended property matching the filter. The response body is similar to the response from [getting a message collection](../api/user-list-messages.md). The response does not include the matching extended property.</span></span>


#### <a name="request-3"></a><span data-ttu-id="a7eb5-265">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="a7eb5-265">Request 3</span></span>

<span data-ttu-id="a7eb5-266">En el tercer ejemplo, se obtienen mensajes con la propiedad extendida de valor único de tipo cadena especificada en el filtro.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-266">The third example gets messages that have the string-typed single-value extended property specified in the filter.</span></span> <span data-ttu-id="a7eb5-267">El filtro busca una propiedad extendida que tenga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a7eb5-267">The filter looks for the extended property that has:</span></span>

- <span data-ttu-id="a7eb5-268">Un **id.** igual a la cadena `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (con la codificación de direcciones URL quitada aquí para facilitar la lectura).</span><span class="sxs-lookup"><span data-stu-id="a7eb5-268">Its **id** equal to the string `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (with URL encoding removed here for ease of reading).</span></span>

- <span data-ttu-id="a7eb5-269">Su **valor** que contiene la cadena `green`.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-269">Its **value** containing the string `green`.</span></span> 

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/Me/messages?$filter=singleValueExtendedProperties/any(ep:ep/Id eq 'String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color' and contains(ep/Value, 'green'))
```

#### <a name="response-3"></a><span data-ttu-id="a7eb5-270">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="a7eb5-270">Response 3</span></span>

<span data-ttu-id="a7eb5-271">Un código de respuesta `HTTP 200 OK` indica una respuesta correcta y el cuerpo de la respuesta incluye todas las propiedades de los mensajes cuya propiedad extendida coincide con el filtro.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-271">A successful response is indicated by an `HTTP 200 OK` response code, and the response body includes all the properties of the messages that have the extended property matching the filter.</span></span> <span data-ttu-id="a7eb5-272">Por ejemplo, un mensaje que tiene una propiedad extendida de valor único con el **id** igual a la cadena `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` y el **valor** `Light green`, debería coincidir con el filtro y se incluye en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-272">For example, a message that has a single-value extended property with the **id** equal to the string `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color`, and the **value** `Light green`, would match the filter and be included in the response.</span></span>

<span data-ttu-id="a7eb5-273">El cuerpo de la respuesta es similar a la respuesta de la [obtención de una colección de mensajes](../api/user-list-messages.md).</span><span class="sxs-lookup"><span data-stu-id="a7eb5-273">The response body is similar to the response from [getting a message collection](../api/user-list-messages.md).</span></span> <span data-ttu-id="a7eb5-274">El cuerpo de la respuesta no incluye la propiedad extendida coincidente.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-274">The response does not include the matching extended property.</span></span>


#### <a name="request-4"></a><span data-ttu-id="a7eb5-275">Solicitud 4</span><span class="sxs-lookup"><span data-stu-id="a7eb5-275">Request 4</span></span>

<span data-ttu-id="a7eb5-276">En los siguientes dos ejemplos, se muestra cómo obtener mensajes que tengan propiedades extendidas de valor único que no sean de tipo cadena.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-276">The next 2 examples show how to get messages that have non-string typed single-value extended properties.</span></span> <span data-ttu-id="a7eb5-277">Para facilitar la lectura, no incluyen la codificación de direcciones URL necesaria.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-277">For ease of reading, they do not include the necessary URL encoding.</span></span>

<span data-ttu-id="a7eb5-278">En el siguiente ejemplo, se muestra un filtro que busca una propiedad extendida que tenga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a7eb5-278">The following example shows a filter that looks for the extended property that has:</span></span>

- <span data-ttu-id="a7eb5-279">Un **id.** coincidente con la cadena `CLSID {00062008-0000-0000-C000-000000000046} Name ConnectorSenderGuid`.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-279">Its **id** matching the string `CLSID {00062008-0000-0000-C000-000000000046} Name ConnectorSenderGuid`.</span></span>

- <span data-ttu-id="a7eb5-280">El GUID `b9cf8971-7d55-4b73-9ffa-a584611b600b` como **valor**.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-280">Its **value** being the GUID `b9cf8971-7d55-4b73-9ffa-a584611b600b`.</span></span> <span data-ttu-id="a7eb5-281">Para comparar el valor de propiedad con un GUID, convierta `ep/value` en `Edm.Guid`.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-281">To compare the property value with a GUID, cast `ep/value` to `Edm.Guid`.</span></span>


<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/me/messages?$filter=singleValueExtendedProperties/any(ep:ep/id eq 'CLSID {00062008-0000-0000-C000-000000000046} Name ConnectorSenderGuid' and cast(ep/value, Edm.Guid) eq (b9cf8971-7d55-4b73-9ffa-a584611b600b))
```

<span data-ttu-id="a7eb5-282">En el siguiente ejemplo, se muestra un filtro que busca una propiedad extendida que tenga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a7eb5-282">The next example shows a filter that looks for the extended property that has:</span></span>

- <span data-ttu-id="a7eb5-283">Un **id.** coincidente con la cadena `Integer {66f5a359-4659-4830-9070-00047ec6ac6e} Name Pallete`.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-283">Its **id** matching the string `Integer {66f5a359-4659-4830-9070-00047ec6ac6e} Name Pallete`.</span></span>

- <span data-ttu-id="a7eb5-284">Un **valor** igual que el número entero 12.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-284">Its **value** equal to the integer 12.</span></span> <span data-ttu-id="a7eb5-285">Para comparar el valor de propiedad con un número entero, convierta `ep/value` en `Edm.Int32`.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-285">To compare the property value with an integer, cast `ep/value` to `Edm.Int32`.</span></span>


<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/me/messages?$filter=singleValueExtendedProperties/any(ep:ep/id eq 'Integer {66f5a359-4659-4830-9070-00047ec6ac6e} Name Pallete' and cast(ep/value, Edm.Int32) eq 12)
```


#### <a name="response-4"></a><span data-ttu-id="a7eb5-286">Respuesta 4</span><span class="sxs-lookup"><span data-stu-id="a7eb5-286">Response 4</span></span>

<span data-ttu-id="a7eb5-287">Para cada uno de los dos ejemplos anteriores, un código de respuesta `HTTP 200 OK` indica una respuesta correcta y el cuerpo de la respuesta incluye todas las propiedades de los mensajes cuya propiedad extendida coincide con el filtro correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-287">For each of the preceding 2 examples, a successful response is indicated by an `HTTP 200 OK` response code, and the response body includes all the properties of the messages that have the extended property matching the corresponding filter.</span></span> <span data-ttu-id="a7eb5-288">El cuerpo de la respuesta es similar a la respuesta de la [obtención de una colección de mensajes](../api/user-list-messages.md).</span><span class="sxs-lookup"><span data-stu-id="a7eb5-288">The response body is similar to the response from [getting a message collection](../api/user-list-messages.md).</span></span> <span data-ttu-id="a7eb5-289">El cuerpo de la respuesta no incluye la propiedad extendida coincidente.</span><span class="sxs-lookup"><span data-stu-id="a7eb5-289">The response does not include the matching extended property.</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get singleValueLegacyExtendedProperty",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

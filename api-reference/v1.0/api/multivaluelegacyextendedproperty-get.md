---
title: Obtener multiValueLegacyExtendedProperty
description: Expanda '.
localization_priority: Normal
ms.openlocfilehash: c1d95e319637df17f04e706055245d5e19762a87
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866328"
---
# <a name="get-multivaluelegacyextendedproperty"></a><span data-ttu-id="35a36-103">Obtener multiValueLegacyExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="35a36-103">Get multiValueLegacyExtendedProperty</span></span>

<span data-ttu-id="35a36-104">Obtenga una instancia de recursos que contiene una propiedad extendida de varios valores mediante el uso de `$expand`.</span><span class="sxs-lookup"><span data-stu-id="35a36-104">Get a resource instance that contains a multi-value extended property by using `$expand`.</span></span>

<span data-ttu-id="35a36-105">El uso del parámetro de consulta `$expand` le permite expandir la instancia especificada con la propiedad extendida indicada.</span><span class="sxs-lookup"><span data-stu-id="35a36-105">Using the query parameter `$expand` allows you to get the specified instance expanded with the indicated extended property.</span></span> <span data-ttu-id="35a36-106">Actualmente, esta es la única forma de obtener el objeto [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) que representa una propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="35a36-106">This is currently the only way to get the [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) object that represents an extended property.</span></span>

<span data-ttu-id="35a36-107">Se admiten los siguientes recursos de usuario:</span><span class="sxs-lookup"><span data-stu-id="35a36-107">The following user resources are supported:</span></span>

- [<span data-ttu-id="35a36-108">calendar</span><span class="sxs-lookup"><span data-stu-id="35a36-108">calendar</span></span>](../resources/calendar.md)
- [<span data-ttu-id="35a36-109">contact</span><span class="sxs-lookup"><span data-stu-id="35a36-109">contact</span></span>](../resources/contact.md)
- [<span data-ttu-id="35a36-110">contactFolder</span><span class="sxs-lookup"><span data-stu-id="35a36-110">contactFolder</span></span>](../resources/contactfolder.md) 
- [<span data-ttu-id="35a36-111">event</span><span class="sxs-lookup"><span data-stu-id="35a36-111">event</span></span>](../resources/event.md)
- [<span data-ttu-id="35a36-112">mailFolder</span><span class="sxs-lookup"><span data-stu-id="35a36-112">mailFolder</span></span>](../resources/mailfolder.md)
- [<span data-ttu-id="35a36-113">message</span><span class="sxs-lookup"><span data-stu-id="35a36-113">message</span></span>](../resources/message.md) 

<span data-ttu-id="35a36-114">También los siguientes recursos de grupo:</span><span class="sxs-lookup"><span data-stu-id="35a36-114">As well as the following group resources:</span></span>

- <span data-ttu-id="35a36-115">[calendar](../resources/calendar.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="35a36-115">group [calendar](../resources/calendar.md)</span></span>
- <span data-ttu-id="35a36-116">[event](../resources/event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="35a36-116">group [event](../resources/event.md)</span></span>
- <span data-ttu-id="35a36-117">[post](../resources/post.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="35a36-117">group [post](../resources/post.md)</span></span>

<span data-ttu-id="35a36-118">Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="35a36-118">See [Extended properties overview](../resources/extended-properties-overview.md) for more information about when to use open extensions or extended properties, and how to specify extended properties.</span></span>

## <a name="permissions"></a><span data-ttu-id="35a36-119">Permisos</span><span class="sxs-lookup"><span data-stu-id="35a36-119">Permissions</span></span>
<span data-ttu-id="35a36-120">Dependiendo del recurso está obteniendo la propiedad extendida desde y el permiso escriba (delegada o de la aplicación) se solicitud, el permiso especificado en la tabla siguiente es el requisito mínimo para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="35a36-120">Depending on the resource you're getting the extended property from and the permission type (delegated or application) you request, the permission specified in the following table is the minimum required to call this API.</span></span> <span data-ttu-id="35a36-121">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="35a36-121">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="35a36-122">Recurso admitido</span><span class="sxs-lookup"><span data-stu-id="35a36-122">Supported resource</span></span> | <span data-ttu-id="35a36-123">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="35a36-123">Delegated (work or school account)</span></span> | <span data-ttu-id="35a36-124">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="35a36-124">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="35a36-125">Aplicación</span><span class="sxs-lookup"><span data-stu-id="35a36-125">Application</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="35a36-126">calendario</span><span class="sxs-lookup"><span data-stu-id="35a36-126">calendar</span></span>](../resources/calendar.md) | <span data-ttu-id="35a36-127">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-127">Calendars.Read</span></span> | <span data-ttu-id="35a36-128">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-128">Calendars.Read</span></span> | <span data-ttu-id="35a36-129">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-129">Calendars.Read</span></span> |
| [<span data-ttu-id="35a36-130">contact</span><span class="sxs-lookup"><span data-stu-id="35a36-130">contact</span></span>](../resources/contact.md) | <span data-ttu-id="35a36-131">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-131">Contacts.Read</span></span> | <span data-ttu-id="35a36-132">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-132">Contacts.Read</span></span> | <span data-ttu-id="35a36-133">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-133">Contacts.Read</span></span> |
| [<span data-ttu-id="35a36-134">contactFolder</span><span class="sxs-lookup"><span data-stu-id="35a36-134">contactFolder</span></span>](../resources/contactfolder.md) | <span data-ttu-id="35a36-135">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-135">Contacts.Read</span></span> | <span data-ttu-id="35a36-136">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-136">Contacts.Read</span></span> | <span data-ttu-id="35a36-137">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-137">Contacts.Read</span></span> |
| [<span data-ttu-id="35a36-138">event</span><span class="sxs-lookup"><span data-stu-id="35a36-138">event</span></span>](../resources/event.md) | <span data-ttu-id="35a36-139">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-139">Calendars.Read</span></span> | <span data-ttu-id="35a36-140">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-140">Calendars.Read</span></span> |  <span data-ttu-id="35a36-141">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-141">Calendars.Read</span></span>|
| <span data-ttu-id="35a36-142">[calendar](../resources/calendar.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="35a36-142">group [calendar](../resources/calendar.md)</span></span> | <span data-ttu-id="35a36-143">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="35a36-143">Group.Read.All</span></span> | <span data-ttu-id="35a36-144">No admitido</span><span class="sxs-lookup"><span data-stu-id="35a36-144">Not supported</span></span> | <span data-ttu-id="35a36-145">No admitido</span><span class="sxs-lookup"><span data-stu-id="35a36-145">Not supported</span></span> |
| <span data-ttu-id="35a36-146">[event](../resources/event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="35a36-146">group [event](../resources/event.md)</span></span> | <span data-ttu-id="35a36-147">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="35a36-147">Group.Read.All</span></span> | <span data-ttu-id="35a36-148">No admitido</span><span class="sxs-lookup"><span data-stu-id="35a36-148">Not supported</span></span> | <span data-ttu-id="35a36-149">No admitido</span><span class="sxs-lookup"><span data-stu-id="35a36-149">Not supported</span></span> |
| <span data-ttu-id="35a36-150">[post](../resources/post.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="35a36-150">group [post](../resources/post.md)</span></span> | <span data-ttu-id="35a36-151">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="35a36-151">Group.Read.All</span></span> | <span data-ttu-id="35a36-152">No admitido</span><span class="sxs-lookup"><span data-stu-id="35a36-152">Not supported</span></span> | <span data-ttu-id="35a36-153">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="35a36-153">Group.Read.All</span></span> |
| [<span data-ttu-id="35a36-154">mailFolder</span><span class="sxs-lookup"><span data-stu-id="35a36-154">mailFolder</span></span>](../resources/mailfolder.md) | <span data-ttu-id="35a36-155">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-155">Mail.Read</span></span> | <span data-ttu-id="35a36-156">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-156">Mail.Read</span></span> | <span data-ttu-id="35a36-157">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-157">Mail.Read</span></span> |
| [<span data-ttu-id="35a36-158">message</span><span class="sxs-lookup"><span data-stu-id="35a36-158">message</span></span>](../resources/message.md) | <span data-ttu-id="35a36-159">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-159">Mail.Read</span></span> | <span data-ttu-id="35a36-160">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-160">Mail.Read</span></span> | <span data-ttu-id="35a36-161">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="35a36-161">Mail.Read</span></span> |
 
## <a name="http-request"></a><span data-ttu-id="35a36-162">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="35a36-162">HTTP request</span></span>

<span data-ttu-id="35a36-p103">Expanda una instancia de recurso con la propiedad extendida que coincida con un filtro en la propiedad **id**. Asegúrese de aplicar la [codificación de direcciones URL](https://www.w3schools.com/tags/ref_urlencode.asp) a los caracteres de espacio de la cadena de filtro.</span><span class="sxs-lookup"><span data-stu-id="35a36-p103">Get a resource instance expanded with the extended property which matches a filter on the **id** property. Make sure you apply [URL encoding](https://www.w3schools.com/tags/ref_urlencode.asp) to the space characters in the filter string.</span></span>

<span data-ttu-id="35a36-165">Obtener una instancia de **mensaje** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="35a36-165">Get a **message** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/messages/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/messages/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /me/mailFolders/{id}/messages/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="35a36-166">Obtener una instancia de **mailFolder** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="35a36-166">Get a **mailFolder** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/mailFolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/mailFolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="35a36-167">Obtener una instancia de **evento** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="35a36-167">Get an **event** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/events/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/events/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="35a36-168">Obtener una instancia de **calendario** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="35a36-168">Get a **calendar** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/calendars/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/calendars/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="35a36-169">Obtener una instancia de **ponerse en contacto con** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="35a36-169">Get a **contact** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/contacts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contacts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /me/contactFolders/{id}/contacts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}/contacts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="35a36-170">Obtener una instancia de **contactFolder** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="35a36-170">Get a **contactFolder** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/contactfolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="35a36-171">Obtener una instancia de **evento** de grupo:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="35a36-171">Get a group **event** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /groups/{id}/events/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="35a36-172">Obtener una instancia de **entrada** de grupo:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="35a36-172">Get a group **post** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /groups/{id}/threads/{id}/posts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```

## <a name="path-parameters"></a><span data-ttu-id="35a36-173">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="35a36-173">Path parameters</span></span>
|<span data-ttu-id="35a36-174">Parámetro</span><span class="sxs-lookup"><span data-stu-id="35a36-174">Parameter</span></span>|<span data-ttu-id="35a36-175">Tipo</span><span class="sxs-lookup"><span data-stu-id="35a36-175">Type</span></span>|<span data-ttu-id="35a36-176">Description</span><span class="sxs-lookup"><span data-stu-id="35a36-176">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="35a36-177">id_value</span><span class="sxs-lookup"><span data-stu-id="35a36-177">id_value</span></span>|<span data-ttu-id="35a36-178">String</span><span class="sxs-lookup"><span data-stu-id="35a36-178">String</span></span>|<span data-ttu-id="35a36-p104">El identificador de la propiedad extendida que debe coincidir. Debe tener uno de los formatos compatibles. Consulte la [Información general de las propiedades extendidas de Outlook](../resources/extended-properties-overview.md) para obtener más información. Necesario.</span><span class="sxs-lookup"><span data-stu-id="35a36-p104">The ID of the extended property to match. It must follow one of the supported formats. See [Outlook extended properties overview](../resources/extended-properties-overview.md) for more information. Required.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="35a36-183">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="35a36-183">Request headers</span></span>
| <span data-ttu-id="35a36-184">Nombre</span><span class="sxs-lookup"><span data-stu-id="35a36-184">Name</span></span>      |<span data-ttu-id="35a36-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="35a36-185">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="35a36-186">Authorization</span><span class="sxs-lookup"><span data-stu-id="35a36-186">Authorization</span></span>  | <span data-ttu-id="35a36-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="35a36-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="35a36-189">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="35a36-189">Request body</span></span>
<span data-ttu-id="35a36-190">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="35a36-190">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="35a36-191">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35a36-191">Response</span></span>

<span data-ttu-id="35a36-192">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="35a36-192">If successful, this method returns a `200 OK` response code.</span></span> 

<span data-ttu-id="35a36-193">El cuerpo de la respuesta incluye un objeto que representa la instancia de recurso solicitada y expandida con el objeto coincidente [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="35a36-193">The response body includes an object representing the requested resource instance, expanded with the matching [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) object.</span></span>

## <a name="example"></a><span data-ttu-id="35a36-194">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="35a36-194">Example</span></span>
##### <a name="request"></a><span data-ttu-id="35a36-195">Solicitud</span><span class="sxs-lookup"><span data-stu-id="35a36-195">Request</span></span>
<span data-ttu-id="35a36-p106">Este ejemplo obtiene y expande el evento especificado al incluir una propiedad extendida de varios valores. El filtro devuelve la propiedad extendida con un **id** que coincide con la cadena `StringArray {66f5a359-4659-4830-9070-00050ec6ac6e} Name Recreation` (la codificación de dirección URL se ha eliminado aquí para facilitar la lectura).</span><span class="sxs-lookup"><span data-stu-id="35a36-p106">This example gets and expands the specified event by including a multi-value extended property. The filter returns the extended property that has its **id** matching the string `StringArray {66f5a359-4659-4830-9070-00050ec6ac6e} Name Recreation` (with URL encoding removed here for ease of reading).</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/me/events('AAMkAGE1M2_bs88AACbuFiiAAA=')?$expand=multiValueExtendedProperties($filter=id%20eq%20'StringArray%20{66f5a359-4659-4830-9070-00050ec6ac6e}%20Name%20Recreation')
```
##### <a name="response"></a><span data-ttu-id="35a36-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35a36-198">Response</span></span>

<span data-ttu-id="35a36-199">El cuerpo de la respuesta incluye todas las propiedades del evento especificado y devuelve la propiedad extendida del filtro.</span><span class="sxs-lookup"><span data-stu-id="35a36-199">The response body includes all the properties of the specified event and extended property returned from the filter.</span></span>

<span data-ttu-id="35a36-p107">Nota: El objeto **event** que aparece aquí está truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="35a36-p107">Note: The **event** object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
Content-type: application/json
{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/events/$entity",
    "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/events('AAMkAGE1M2_bs88AACbuFiiAAA=')",
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
    "multiValueExtendedProperties@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/events('AAMkAGE1M2_bs88AACbuFiiAAA%3D')/multiValueExtendedProperties",
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

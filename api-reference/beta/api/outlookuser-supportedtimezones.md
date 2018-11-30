---
title: 'outlookUser: supportedTimeZones'
description: Obtener la lista de zonas horarias compatibles con el usuario, según la configuración del servidor de buzones del usuario.
ms.openlocfilehash: c5886cc435b482a0acfcd99c65f356efe3a99d59
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083770"
---
# <a name="outlookuser-supportedtimezones"></a><span data-ttu-id="88043-103">outlookUser: supportedTimeZones</span><span class="sxs-lookup"><span data-stu-id="88043-103">outlookUser: supportedTimeZones</span></span>

> <span data-ttu-id="88043-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="88043-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="88043-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="88043-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="88043-106">Obtener la lista de zonas horarias compatibles con el usuario, según la configuración del servidor de buzones del usuario.</span><span class="sxs-lookup"><span data-stu-id="88043-106">Get the list of time zones that are supported for the user, as configured on the user's mailbox server.</span></span>

<span data-ttu-id="88043-107">Puede especificarse explícitamente que las zonas horarias se devuelvan en el formato de zona horaria de Windows o el formato de [zona horaria Internet Assigned Numbers Authority (IANA)](https://www.iana.org/time-zones) (también conocida como "zona horaria Olson").</span><span class="sxs-lookup"><span data-stu-id="88043-107">You can explicitly specify to have time zones returned in the Windows time zone format or  [Internet Assigned Numbers Authority (IANA) time zone](https://www.iana.org/time-zones) (also known as Olson time zone) format.</span></span> <span data-ttu-id="88043-108">El formato Windows es el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="88043-108">The Windows format is the default.</span></span>

<span data-ttu-id="88043-109">Al configurar un cliente de Outlook, el usuario selecciona la zona horaria preferida de esta lista admitida.</span><span class="sxs-lookup"><span data-stu-id="88043-109">When setting up an Outlook client, the user selects the preferred time zone from this supported list.</span></span> <span data-ttu-id="88043-110">Posteriormente, puede obtener la zona horaria preferida [obteniendo la configuración del buzón del usuario](user-get-mailboxsettings.md).</span><span class="sxs-lookup"><span data-stu-id="88043-110">You can subsequently get the preferred time zone by [getting the user's mailbox settings](user-get-mailboxsettings.md).</span></span>


## <a name="permissions"></a><span data-ttu-id="88043-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="88043-111">Permissions</span></span>
<span data-ttu-id="88043-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="88043-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="88043-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="88043-114">Permission type</span></span>      | <span data-ttu-id="88043-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="88043-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="88043-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="88043-116">Delegated (work or school account)</span></span> | <span data-ttu-id="88043-117">User.Read, User.ReadBasic.All</span><span class="sxs-lookup"><span data-stu-id="88043-117">User.Read, User.ReadBasic.All</span></span>    |
|<span data-ttu-id="88043-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="88043-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="88043-119">User.Read</span><span class="sxs-lookup"><span data-stu-id="88043-119">User.Read</span></span>    |
|<span data-ttu-id="88043-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="88043-120">Application</span></span> | <span data-ttu-id="88043-121">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="88043-121">User.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="88043-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="88043-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/outlook/supportedTimeZones
GET /users/{id|userPrincipalName}/outlook/supportedTimeZones

GET /me/outlook/supportedTimeZones(TimeZoneStandard=microsoft.graph.timeZoneStandard'{timezone_format}')
GET /users/{id|userPrincipalName}/outlook/supportedTimeZones(TimeZoneStandard=microsoft.graph.timeZoneStandard'{timezone_format}')
```

## <a name="function-parameters"></a><span data-ttu-id="88043-123">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="88043-123">Function parameters</span></span>
| <span data-ttu-id="88043-124">Parámetro de la función</span><span class="sxs-lookup"><span data-stu-id="88043-124">Function parameter</span></span>       | <span data-ttu-id="88043-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="88043-125">Type</span></span> | <span data-ttu-id="88043-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="88043-126">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="88043-127">TimeZoneStandard</span><span class="sxs-lookup"><span data-stu-id="88043-127">TimeZoneStandard</span></span>  | <span data-ttu-id="88043-128">String</span><span class="sxs-lookup"><span data-stu-id="88043-128">String</span></span>  | <span data-ttu-id="88043-129">Formato de una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="88043-129">A time zone format.</span></span> <span data-ttu-id="88043-130">Los valores admitidos son: `Windows` y `Iana`.</span><span class="sxs-lookup"><span data-stu-id="88043-130">Supported values are: `Windows`, and `Iana`.</span></span> <span data-ttu-id="88043-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="88043-131">Optional.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="88043-132">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="88043-132">Request headers</span></span>
| <span data-ttu-id="88043-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="88043-133">Name</span></span>       | <span data-ttu-id="88043-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="88043-134">Type</span></span> | <span data-ttu-id="88043-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="88043-135">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="88043-136">Authorization</span><span class="sxs-lookup"><span data-stu-id="88043-136">Authorization</span></span>  | <span data-ttu-id="88043-137">string</span><span class="sxs-lookup"><span data-stu-id="88043-137">string</span></span>  | <span data-ttu-id="88043-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="88043-p106">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="88043-140">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="88043-140">Request body</span></span>
<span data-ttu-id="88043-141">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="88043-141">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="88043-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88043-142">Response</span></span>
<span data-ttu-id="88043-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [timeZoneInformation](../resources/timezoneinformation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88043-143">If successful, this method returns `200 OK` response code and a collection of [timeZoneInformation](../resources/timezoneinformation.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="88043-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="88043-144">Example</span></span>

##### <a name="request-1"></a><span data-ttu-id="88043-145">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="88043-145">Request 1</span></span>
<span data-ttu-id="88043-146">En el ejemplo siguiente no se especifica el parámetro `timeZoneStandard` y se obtiene la lista de zonas horarias admitidas representadas en el formato de zona horaria de Windows.</span><span class="sxs-lookup"><span data-stu-id="88043-146">The following example does not specify the `timeZoneStandard` parameter, and gets the list of supported time zones represented in the Windows time zone format.</span></span> 
<!-- {
  "blockType": "request",
  "name": "user_supportedtimezones_default"
}-->
```http
GET https://graph.microsoft.com/beta/me/outlook/supportedTimeZones
```

##### <a name="response-1"></a><span data-ttu-id="88043-147">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="88043-147">Response 1</span></span>
<span data-ttu-id="88043-148">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88043-148">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "name": "user_supportedtimezones_default",
  "truncated": true,
  "@odata.type": "microsoft.graph.timeZoneInformation",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.timeZoneInformation)",
  "value":[
    {
      "alias":"Dateline Standard Time",
      "displayName":"(UTC-12:00) International Date Line West"
    },
    {
      "alias":"Samoa Standard Time",
      "displayName":"(UTC+13:00) Samoa"
    },
    {
       "alias":"UTC-11",
       "displayName":"(UTC-11:00) Coordinated Universal Time-11"
    },
    {
      "alias":"Aleutian Standard Time",
      "displayName":"(UTC-10:00) Aleutian Islands"
    }
  ]
}
```

##### <a name="request-2"></a><span data-ttu-id="88043-149">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="88043-149">Request 2</span></span>
<span data-ttu-id="88043-150">En el ejemplo siguiente se especifica el `Iana` para el parámetro `TimeZoneStandard` y se obtiene la lista de zonas horarias admitidas representadas en el formato IANA.</span><span class="sxs-lookup"><span data-stu-id="88043-150">The following example specifies `Iana` for the `TimeZoneStandard` parameter, and gets the list of supported time zones represented in IANA format.</span></span> 

<!-- {
  "blockType": "request",
  "name": "user_supportedtimezones_iana"
} -->

```http
GET https://graph.microsoft.com/beta/me/outlook/supportedTimeZones(TimeZoneStandard=microsoft.graph.timeZoneStandard'Iana')
```

##### <a name="response-2"></a><span data-ttu-id="88043-151">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="88043-151">Response 2</span></span>
<span data-ttu-id="88043-152">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88043-152">Here is an example of the response.</span></span> 

<!-- {
  "blockType": "response",
  "name": "user_supportedtimezones_iana",
  "truncated": true,
  "@odata.type": "microsoft.graph.timeZoneInformation",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.timeZoneInformation)",
  "value":[
    {
      "alias":"Etc/GMT+12",
      "displayName":"Etc/GMT+12"
    },
    {
      "alias":"US/Samoa",
      "displayName":"US/Samoa"
    },
    {
      "alias":"Etc/GMT+11",
      "displayName":"Etc/GMT+11"
    },
    {
      "alias":"US/Aleutian",
      "displayName":"US/Aleutian"
    }
  ]
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: supportedTimeZones",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
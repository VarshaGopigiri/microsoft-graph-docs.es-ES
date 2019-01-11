---
title: 'outlookUser: supportedTimeZones'
description: Obtener la lista de zonas horarias compatibles con el usuario, según la configuración del servidor de buzones del usuario.
localization_priority: Normal
ms.openlocfilehash: 01ee7d7df928e68bd34793ced3b6d3e2a8cc5502
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27848205"
---
# <a name="outlookuser-supportedtimezones"></a><span data-ttu-id="09a2e-103">outlookUser: supportedTimeZones</span><span class="sxs-lookup"><span data-stu-id="09a2e-103">outlookUser: supportedTimeZones</span></span>

<span data-ttu-id="09a2e-104">Obtener la lista de zonas horarias compatibles con el usuario, según la configuración del servidor de buzones del usuario.</span><span class="sxs-lookup"><span data-stu-id="09a2e-104">Get the list of time zones that are supported for the user, as configured on the user's mailbox server.</span></span>

<span data-ttu-id="09a2e-105">Puede especificarse explícitamente que las zonas horarias se devuelvan en el formato de zona horaria de Windows o el formato de [zona horaria Internet Assigned Numbers Authority (IANA)](https://www.iana.org/time-zones) (también conocida como "zona horaria Olson").</span><span class="sxs-lookup"><span data-stu-id="09a2e-105">You can explicitly specify to have time zones returned in the Windows time zone format or  [Internet Assigned Numbers Authority (IANA) time zone](https://www.iana.org/time-zones) (also known as Olson time zone) format.</span></span> <span data-ttu-id="09a2e-106">El formato Windows es el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="09a2e-106">The Windows format is the default.</span></span>

<span data-ttu-id="09a2e-107">Al configurar un cliente de Outlook, el usuario selecciona la zona horaria preferida de esta lista admitida.</span><span class="sxs-lookup"><span data-stu-id="09a2e-107">When setting up an Outlook client, the user selects the preferred time zone from this supported list.</span></span> <span data-ttu-id="09a2e-108">Posteriormente, puede obtener la zona horaria preferida [obteniendo la configuración del buzón del usuario](user-get-mailboxsettings.md).</span><span class="sxs-lookup"><span data-stu-id="09a2e-108">You can subsequently get the preferred time zone by [getting the user's mailbox settings](user-get-mailboxsettings.md).</span></span>


## <a name="permissions"></a><span data-ttu-id="09a2e-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="09a2e-109">Permissions</span></span>
<span data-ttu-id="09a2e-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="09a2e-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="09a2e-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="09a2e-112">Permission type</span></span>      | <span data-ttu-id="09a2e-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="09a2e-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="09a2e-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="09a2e-114">Delegated (work or school account)</span></span> | <span data-ttu-id="09a2e-115">User.Read, User.ReadBasic.All</span><span class="sxs-lookup"><span data-stu-id="09a2e-115">User.Read, User.ReadBasic.All</span></span>    |
|<span data-ttu-id="09a2e-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="09a2e-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="09a2e-117">User.Read</span><span class="sxs-lookup"><span data-stu-id="09a2e-117">User.Read</span></span>    |
|<span data-ttu-id="09a2e-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="09a2e-118">Application</span></span> | <span data-ttu-id="09a2e-119">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="09a2e-119">User.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="09a2e-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="09a2e-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/outlook/supportedTimeZones
GET /users/{id|userPrincipalName}/outlook/supportedTimeZones

GET /me/outlook/supportedTimeZones(TimeZoneStandard=microsoft.graph.timeZoneStandard'{timezone_format}')
GET /users/{id|userPrincipalName}/outlook/supportedTimeZones(TimeZoneStandard=microsoft.graph.timeZoneStandard'{timezone_format}')
```

## <a name="function-parameters"></a><span data-ttu-id="09a2e-121">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="09a2e-121">Function parameters</span></span>
| <span data-ttu-id="09a2e-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="09a2e-122">Parameter</span></span>       | <span data-ttu-id="09a2e-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="09a2e-123">Type</span></span> | <span data-ttu-id="09a2e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="09a2e-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="09a2e-125">TimeZoneStandard</span><span class="sxs-lookup"><span data-stu-id="09a2e-125">TimeZoneStandard</span></span>  | <span data-ttu-id="09a2e-126">timeZoneStandard</span><span class="sxs-lookup"><span data-stu-id="09a2e-126">timeZoneStandard</span></span>  | <span data-ttu-id="09a2e-127">Formato de una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="09a2e-127">A time zone format.</span></span> <span data-ttu-id="09a2e-128">Los valores admitidos son: `Windows` y `Iana`.</span><span class="sxs-lookup"><span data-stu-id="09a2e-128">Supported values are: `Windows`, and `Iana`.</span></span> <span data-ttu-id="09a2e-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="09a2e-129">Optional.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="09a2e-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="09a2e-130">Request headers</span></span>
| <span data-ttu-id="09a2e-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="09a2e-131">Name</span></span>       | <span data-ttu-id="09a2e-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="09a2e-132">Type</span></span> | <span data-ttu-id="09a2e-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="09a2e-133">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="09a2e-134">Autorización</span><span class="sxs-lookup"><span data-stu-id="09a2e-134">Authorization</span></span>  | <span data-ttu-id="09a2e-135">string</span><span class="sxs-lookup"><span data-stu-id="09a2e-135">string</span></span>  | <span data-ttu-id="09a2e-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="09a2e-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="09a2e-138">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="09a2e-138">Request body</span></span>
<span data-ttu-id="09a2e-139">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="09a2e-139">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="09a2e-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="09a2e-140">Response</span></span>
<span data-ttu-id="09a2e-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [timeZoneInformation](../resources/timezoneinformation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="09a2e-141">If successful, this method returns `200 OK` response code and a collection of [timeZoneInformation](../resources/timezoneinformation.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="09a2e-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="09a2e-142">Example</span></span>

##### <a name="request-1"></a><span data-ttu-id="09a2e-143">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="09a2e-143">Request 1</span></span>
<span data-ttu-id="09a2e-144">En el ejemplo siguiente no se especifica el parámetro `timeZoneStandard` y se obtiene la lista de zonas horarias admitidas representadas en el formato de zona horaria de Windows.</span><span class="sxs-lookup"><span data-stu-id="09a2e-144">The following example does not specify the `timeZoneStandard` parameter, and gets the list of supported time zones represented in the Windows time zone format.</span></span> 
<!-- {
  "blockType": "request",
  "name": "user_supportedtimezones_default"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/outlook/supportedTimeZones
```

##### <a name="response-1"></a><span data-ttu-id="09a2e-145">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="09a2e-145">Response 1</span></span>
<span data-ttu-id="09a2e-146">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="09a2e-146">Here is an example of the response.</span></span> 
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
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#Collection(microsoft.graph.timeZoneInformation)",
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

##### <a name="request-2"></a><span data-ttu-id="09a2e-147">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="09a2e-147">Request 2</span></span>
<span data-ttu-id="09a2e-148">En el ejemplo siguiente se especifica el `Iana` para el parámetro `TimeZoneStandard` y se obtiene la lista de zonas horarias admitidas representadas en el formato IANA.</span><span class="sxs-lookup"><span data-stu-id="09a2e-148">The following example specifies `Iana` for the `TimeZoneStandard` parameter, and gets the list of supported time zones represented in IANA format.</span></span> 

<!-- {
  "blockType": "request",
  "name": "user_supportedtimezones_iana"
} -->

```http
GET https://graph.microsoft.com/v1.0/me/outlook/supportedTimeZones(TimeZoneStandard=microsoft.graph.timeZoneStandard'Iana')
```

##### <a name="response-2"></a><span data-ttu-id="09a2e-149">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="09a2e-149">Response 2</span></span>
<span data-ttu-id="09a2e-150">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="09a2e-150">Here is an example of the response.</span></span> 

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
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#Collection(microsoft.graph.timeZoneInformation)",
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

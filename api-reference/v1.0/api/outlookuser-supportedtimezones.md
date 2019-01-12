---
title: 'outlookUser: supportedTimeZones'
description: Obtener la lista de zonas horarias compatibles con el usuario, según la configuración del servidor de buzones del usuario.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: c9c90ea56b1c0924ec91436733c99c67333b99d5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981717"
---
# <a name="outlookuser-supportedtimezones"></a><span data-ttu-id="d6443-103">outlookUser: supportedTimeZones</span><span class="sxs-lookup"><span data-stu-id="d6443-103">outlookUser: supportedTimeZones</span></span>

<span data-ttu-id="d6443-104">Obtener la lista de zonas horarias compatibles con el usuario, según la configuración del servidor de buzones del usuario.</span><span class="sxs-lookup"><span data-stu-id="d6443-104">Get the list of time zones that are supported for the user, as configured on the user's mailbox server.</span></span>

<span data-ttu-id="d6443-105">Puede especificarse explícitamente que las zonas horarias se devuelvan en el formato de zona horaria de Windows o el formato de [zona horaria Internet Assigned Numbers Authority (IANA)](https://www.iana.org/time-zones) (también conocida como "zona horaria Olson").</span><span class="sxs-lookup"><span data-stu-id="d6443-105">You can explicitly specify to have time zones returned in the Windows time zone format or  [Internet Assigned Numbers Authority (IANA) time zone](https://www.iana.org/time-zones) (also known as Olson time zone) format.</span></span> <span data-ttu-id="d6443-106">El formato Windows es el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d6443-106">The Windows format is the default.</span></span>

<span data-ttu-id="d6443-107">Al configurar un cliente de Outlook, el usuario selecciona la zona horaria preferida de esta lista admitida.</span><span class="sxs-lookup"><span data-stu-id="d6443-107">When setting up an Outlook client, the user selects the preferred time zone from this supported list.</span></span> <span data-ttu-id="d6443-108">Posteriormente, puede obtener la zona horaria preferida [obteniendo la configuración del buzón del usuario](user-get-mailboxsettings.md).</span><span class="sxs-lookup"><span data-stu-id="d6443-108">You can subsequently get the preferred time zone by [getting the user's mailbox settings](user-get-mailboxsettings.md).</span></span>


## <a name="permissions"></a><span data-ttu-id="d6443-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="d6443-109">Permissions</span></span>
<span data-ttu-id="d6443-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d6443-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d6443-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d6443-112">Permission type</span></span>      | <span data-ttu-id="d6443-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d6443-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d6443-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d6443-114">Delegated (work or school account)</span></span> | <span data-ttu-id="d6443-115">User.Read, User.ReadBasic.All</span><span class="sxs-lookup"><span data-stu-id="d6443-115">User.Read, User.ReadBasic.All</span></span>    |
|<span data-ttu-id="d6443-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d6443-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d6443-117">User.Read</span><span class="sxs-lookup"><span data-stu-id="d6443-117">User.Read</span></span>    |
|<span data-ttu-id="d6443-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d6443-118">Application</span></span> | <span data-ttu-id="d6443-119">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="d6443-119">User.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d6443-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d6443-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/outlook/supportedTimeZones
GET /users/{id|userPrincipalName}/outlook/supportedTimeZones

GET /me/outlook/supportedTimeZones(TimeZoneStandard=microsoft.graph.timeZoneStandard'{timezone_format}')
GET /users/{id|userPrincipalName}/outlook/supportedTimeZones(TimeZoneStandard=microsoft.graph.timeZoneStandard'{timezone_format}')
```

## <a name="function-parameters"></a><span data-ttu-id="d6443-121">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="d6443-121">Function parameters</span></span>
| <span data-ttu-id="d6443-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d6443-122">Parameter</span></span>       | <span data-ttu-id="d6443-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6443-123">Type</span></span> | <span data-ttu-id="d6443-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6443-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="d6443-125">TimeZoneStandard</span><span class="sxs-lookup"><span data-stu-id="d6443-125">TimeZoneStandard</span></span>  | <span data-ttu-id="d6443-126">timeZoneStandard</span><span class="sxs-lookup"><span data-stu-id="d6443-126">timeZoneStandard</span></span>  | <span data-ttu-id="d6443-127">Formato de una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="d6443-127">A time zone format.</span></span> <span data-ttu-id="d6443-128">Los valores admitidos son: `Windows` y `Iana`.</span><span class="sxs-lookup"><span data-stu-id="d6443-128">Supported values are: `Windows`, and `Iana`.</span></span> <span data-ttu-id="d6443-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d6443-129">Optional.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="d6443-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d6443-130">Request headers</span></span>
| <span data-ttu-id="d6443-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="d6443-131">Name</span></span>       | <span data-ttu-id="d6443-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6443-132">Type</span></span> | <span data-ttu-id="d6443-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6443-133">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="d6443-134">Autorización</span><span class="sxs-lookup"><span data-stu-id="d6443-134">Authorization</span></span>  | <span data-ttu-id="d6443-135">string</span><span class="sxs-lookup"><span data-stu-id="d6443-135">string</span></span>  | <span data-ttu-id="d6443-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d6443-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d6443-138">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d6443-138">Request body</span></span>
<span data-ttu-id="d6443-139">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d6443-139">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d6443-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6443-140">Response</span></span>
<span data-ttu-id="d6443-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [timeZoneInformation](../resources/timezoneinformation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6443-141">If successful, this method returns `200 OK` response code and a collection of [timeZoneInformation](../resources/timezoneinformation.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d6443-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d6443-142">Example</span></span>

##### <a name="request-1"></a><span data-ttu-id="d6443-143">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="d6443-143">Request 1</span></span>
<span data-ttu-id="d6443-144">En el ejemplo siguiente no se especifica el parámetro `timeZoneStandard` y se obtiene la lista de zonas horarias admitidas representadas en el formato de zona horaria de Windows.</span><span class="sxs-lookup"><span data-stu-id="d6443-144">The following example does not specify the `timeZoneStandard` parameter, and gets the list of supported time zones represented in the Windows time zone format.</span></span> 
<!-- {
  "blockType": "request",
  "name": "user_supportedtimezones_default"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/outlook/supportedTimeZones
```

##### <a name="response-1"></a><span data-ttu-id="d6443-145">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="d6443-145">Response 1</span></span>
<span data-ttu-id="d6443-146">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6443-146">Here is an example of the response.</span></span> 
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

##### <a name="request-2"></a><span data-ttu-id="d6443-147">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="d6443-147">Request 2</span></span>
<span data-ttu-id="d6443-148">En el ejemplo siguiente se especifica el `Iana` para el parámetro `TimeZoneStandard` y se obtiene la lista de zonas horarias admitidas representadas en el formato IANA.</span><span class="sxs-lookup"><span data-stu-id="d6443-148">The following example specifies `Iana` for the `TimeZoneStandard` parameter, and gets the list of supported time zones represented in IANA format.</span></span> 

<!-- {
  "blockType": "request",
  "name": "user_supportedtimezones_iana"
} -->

```http
GET https://graph.microsoft.com/v1.0/me/outlook/supportedTimeZones(TimeZoneStandard=microsoft.graph.timeZoneStandard'Iana')
```

##### <a name="response-2"></a><span data-ttu-id="d6443-149">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="d6443-149">Response 2</span></span>
<span data-ttu-id="d6443-150">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6443-150">Here is an example of the response.</span></span> 

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

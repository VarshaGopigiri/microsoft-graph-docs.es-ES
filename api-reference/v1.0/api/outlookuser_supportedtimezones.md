# <a name="outlookuser-supportedtimezones"></a><span data-ttu-id="3a3ae-101">outlookUser: supportedTimeZones</span><span class="sxs-lookup"><span data-stu-id="3a3ae-101">outlookUser: supportedTimeZones</span></span>

<span data-ttu-id="3a3ae-102">Obtener la lista de zonas horarias compatibles con el usuario, según la configuración del servidor de buzones del usuario.</span><span class="sxs-lookup"><span data-stu-id="3a3ae-102">Get the list of time zones that are supported for the user, as configured on the user's mailbox server.</span></span>

<span data-ttu-id="3a3ae-103">Puede especificarse explícitamente que las zonas horarias se devuelvan en el formato de zona horaria de Windows o el formato de [zona horaria Internet Assigned Numbers Authority (IANA)](http://www.iana.org/time-zones) (también conocida como "zona horaria Olson").</span><span class="sxs-lookup"><span data-stu-id="3a3ae-103">You can explicitly specify to have time zones returned in the Windows time zone format or  [Internet Assigned Numbers Authority (IANA) time zone](http://www.iana.org/time-zones) (also known as Olson time zone) format.</span></span> <span data-ttu-id="3a3ae-104">El formato Windows es el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3a3ae-104">The Windows format is the default.</span></span>

<span data-ttu-id="3a3ae-105">Al configurar un cliente de Outlook, el usuario selecciona la zona horaria preferida de esta lista admitida.</span><span class="sxs-lookup"><span data-stu-id="3a3ae-105">When setting up an Outlook client, the user selects the preferred time zone from this supported list.</span></span> <span data-ttu-id="3a3ae-106">Posteriormente, puede obtener la zona horaria preferida [obteniendo la configuración del buzón del usuario](user_get_mailboxsettings.md).</span><span class="sxs-lookup"><span data-stu-id="3a3ae-106">You can subsequently get the preferred time zone by [getting the user's mailbox settings](user_get_mailboxsettings.md).</span></span>


## <a name="permissions"></a><span data-ttu-id="3a3ae-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="3a3ae-107">Permissions</span></span>
<span data-ttu-id="3a3ae-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3a3ae-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="3a3ae-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3a3ae-110">Permission type</span></span>      | <span data-ttu-id="3a3ae-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3a3ae-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3a3ae-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3a3ae-112">Delegated (work or school account)</span></span> | <span data-ttu-id="3a3ae-113">User.Read, User.ReadBasic.All</span><span class="sxs-lookup"><span data-stu-id="3a3ae-113">User.Read, User.ReadBasic.All</span></span>    |
|<span data-ttu-id="3a3ae-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3a3ae-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3a3ae-115">User.Read</span><span class="sxs-lookup"><span data-stu-id="3a3ae-115">User.Read</span></span>    |
|<span data-ttu-id="3a3ae-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3a3ae-116">Application</span></span> | <span data-ttu-id="3a3ae-117">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="3a3ae-117">User.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="3a3ae-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3a3ae-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/outlook/supportedTimeZones
GET /users/{id|userPrincipalName}/outlook/supportedTimeZones

GET /me/outlook/supportedTimeZones(TimeZoneStandard=microsoft.graph.timeZoneStandard'{timezone_format}')
GET /users/{id|userPrincipalName}/outlook/supportedTimeZones(TimeZoneStandard=microsoft.graph.timeZoneStandard'{timezone_format}')
```

## <a name="function-parameters"></a><span data-ttu-id="3a3ae-119">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="3a3ae-119">Function parameters</span></span>
| <span data-ttu-id="3a3ae-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3a3ae-120">Parameter</span></span>       | <span data-ttu-id="3a3ae-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a3ae-121">Type</span></span> | <span data-ttu-id="3a3ae-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a3ae-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="3a3ae-123">TimeZoneStandard</span><span class="sxs-lookup"><span data-stu-id="3a3ae-123">TimeZoneStandard</span></span>  | <span data-ttu-id="3a3ae-124">timeZoneStandard</span><span class="sxs-lookup"><span data-stu-id="3a3ae-124">TimeZoneStandard</span></span>  | <span data-ttu-id="3a3ae-125">Formato de una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="3a3ae-125">A time zone format.</span></span> <span data-ttu-id="3a3ae-126">Los valores admitidos son: `Windows` y `Iana`.</span><span class="sxs-lookup"><span data-stu-id="3a3ae-126">Supported values are: `Windows`, and `Iana`.</span></span> <span data-ttu-id="3a3ae-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3a3ae-127">Optional.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="3a3ae-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3a3ae-128">Request headers</span></span>
| <span data-ttu-id="3a3ae-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="3a3ae-129">Name</span></span>       | <span data-ttu-id="3a3ae-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a3ae-130">Type</span></span> | <span data-ttu-id="3a3ae-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a3ae-131">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="3a3ae-132">Autorización</span><span class="sxs-lookup"><span data-stu-id="3a3ae-132">Authorization</span></span>  | <span data-ttu-id="3a3ae-133">cadena</span><span class="sxs-lookup"><span data-stu-id="3a3ae-133">string</span></span>  | <span data-ttu-id="3a3ae-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3a3ae-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3a3ae-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3a3ae-136">Request body</span></span>
<span data-ttu-id="3a3ae-137">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3a3ae-137">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3a3ae-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a3ae-138">Response</span></span>
<span data-ttu-id="3a3ae-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [timeZoneInformation](../resources/timezoneinformation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a3ae-139">If successful, this method returns `200 OK` response code and a collection of [timeZoneInformation](../resources/timezoneinformation.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3a3ae-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a3ae-140">Example</span></span>

##### <a name="request-1"></a><span data-ttu-id="3a3ae-141">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="3a3ae-141">Request 1</span></span>
<span data-ttu-id="3a3ae-142">En el ejemplo siguiente no se especifica el parámetro `timeZoneStandard` y se obtiene la lista de zonas horarias admitidas representadas en el formato de zona horaria de Windows.</span><span class="sxs-lookup"><span data-stu-id="3a3ae-142">The following example does not specify the `timeZoneStandard` parameter, and gets the list of supported time zones represented in the Windows time zone format.</span></span> 
<!-- {
  "blockType": "request",
  "name": "user_supportedtimezones_default"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/outlook/supportedTimeZones
```

##### <a name="response-1"></a><span data-ttu-id="3a3ae-143">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="3a3ae-143">Response 1</span></span>
<span data-ttu-id="3a3ae-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a3ae-144">Here is an example of the response.</span></span> 
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

##### <a name="request-2"></a><span data-ttu-id="3a3ae-145">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="3a3ae-145">Request 2</span></span>
<span data-ttu-id="3a3ae-146">En el ejemplo siguiente se especifica el `Iana` para el parámetro `TimeZoneStandard` y se obtiene la lista de zonas horarias admitidas representadas en el formato IANA.</span><span class="sxs-lookup"><span data-stu-id="3a3ae-146">The following example specifies `Iana` for the `TimeZoneStandard` parameter, and gets the list of supported time zones represented in IANA format.</span></span> 

<!-- {
  "blockType": "request",
  "name": "user_supportedtimezones_iana"
} -->

```http
GET https://graph.microsoft.com/v1.0/me/outlook/supportedTimeZones(TimeZoneStandard=microsoft.graph.timeZoneStandard'Iana')
```

##### <a name="response-2"></a><span data-ttu-id="3a3ae-147">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="3a3ae-147">Response 2</span></span>
<span data-ttu-id="3a3ae-148">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a3ae-148">Here is an example of the response.</span></span> 

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
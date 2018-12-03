---
title: 'orgContact: el Administrador de Get'
description: Obtener el administrador del contacto
ms.openlocfilehash: 7fe4c61422eb83bb4501fbb521f301ec6f9afaa5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084299"
---
# <a name="orgcontact-get-manager"></a><span data-ttu-id="11b5f-103">orgContact: el Administrador de Get</span><span class="sxs-lookup"><span data-stu-id="11b5f-103">orgContact: Get manager</span></span>

> <span data-ttu-id="11b5f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="11b5f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="11b5f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="11b5f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="11b5f-106">Obtener el administrador del contacto</span><span class="sxs-lookup"><span data-stu-id="11b5f-106">Get the contact's manager</span></span>

## <a name="permissions"></a><span data-ttu-id="11b5f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="11b5f-107">Permissions</span></span>
<span data-ttu-id="11b5f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="11b5f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="11b5f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="11b5f-110">Permission type</span></span>      | <span data-ttu-id="11b5f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="11b5f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="11b5f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="11b5f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="11b5f-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="11b5f-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="11b5f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="11b5f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="11b5f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="11b5f-115">Not supported.</span></span>    |
|<span data-ttu-id="11b5f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="11b5f-116">Application</span></span> | <span data-ttu-id="11b5f-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="11b5f-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="11b5f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="11b5f-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /contacts/{id}/manager
```

## <a name="optional-query-parameters"></a><span data-ttu-id="11b5f-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="11b5f-119">Optional query parameters</span></span>
<span data-ttu-id="11b5f-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="11b5f-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="11b5f-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="11b5f-121">Request headers</span></span>
| <span data-ttu-id="11b5f-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="11b5f-122">Name</span></span>       | <span data-ttu-id="11b5f-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="11b5f-123">Type</span></span> | <span data-ttu-id="11b5f-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="11b5f-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="11b5f-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="11b5f-125">Authorization</span></span>  | <span data-ttu-id="11b5f-126">string</span><span class="sxs-lookup"><span data-stu-id="11b5f-126">string</span></span>  | <span data-ttu-id="11b5f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="11b5f-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="11b5f-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="11b5f-129">Request body</span></span>
<span data-ttu-id="11b5f-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="11b5f-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="11b5f-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11b5f-131">Response</span></span>

<span data-ttu-id="11b5f-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="11b5f-132">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="11b5f-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="11b5f-133">Example</span></span>

#### <a name="request"></a><span data-ttu-id="11b5f-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="11b5f-134">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_manager"
}-->

```http
GET https://graph.microsoft.com/beta/contacts/{id}/manager
```

#### <a name="response"></a><span data-ttu-id="11b5f-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11b5f-135">Response</span></span>

<span data-ttu-id="11b5f-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="11b5f-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": false
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 455

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#directoryObjects/$entity",
    "@odata.type": "#microsoft.graph.user",
    "id": "24fcbca3-c3e2-48bf-9ffc-c7f81b81483d",
    "businessPhones": [
        "+1 205 555 0108"
    ],
    "displayName": "Diego Siciliani",
    "givenName": "Diego",
    "jobTitle": "CVP Finance",
    "mail": "DiegoS@contoso.com",
    "mobilePhone": null,
    "officeLocation": "14/1108",
    "preferredLanguage": "en-US",
    "surname": "Siciliani",
    "userPrincipalName": "DiegoS@contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get manager",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
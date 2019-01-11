---
title: 'orgContact: miembro de lista'
description: Recuperar la lista de grupos y unidades administrativas de que el contacto es un miembro.
localization_priority: Normal
ms.openlocfilehash: 318936a49c4eeb56f05c685fc1a1ddd1eaad1a62
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27862691"
---
# <a name="orgcontact-list-memberof"></a><span data-ttu-id="dabc7-103">orgContact: miembro de lista</span><span class="sxs-lookup"><span data-stu-id="dabc7-103">orgContact: List memberOf</span></span>

> <span data-ttu-id="dabc7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dabc7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dabc7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dabc7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dabc7-106">Recuperar la lista de grupos y unidades administrativas de que el contacto es un miembro.</span><span class="sxs-lookup"><span data-stu-id="dabc7-106">Retrieve the list of groups and adminstrative units the contact is a member of.</span></span>

## <a name="permissions"></a><span data-ttu-id="dabc7-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="dabc7-107">Permissions</span></span>
<span data-ttu-id="dabc7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dabc7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dabc7-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dabc7-110">Permission type</span></span>      | <span data-ttu-id="dabc7-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dabc7-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dabc7-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dabc7-112">Delegated (work or school account)</span></span> | <span data-ttu-id="dabc7-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="dabc7-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="dabc7-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dabc7-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dabc7-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dabc7-115">Not supported.</span></span>    |
|<span data-ttu-id="dabc7-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dabc7-116">Application</span></span> | <span data-ttu-id="dabc7-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dabc7-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="dabc7-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dabc7-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /contacts/{id}/memberOf
```
## <a name="optional-query-parameters"></a><span data-ttu-id="dabc7-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="dabc7-119">Optional query parameters</span></span>
<span data-ttu-id="dabc7-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dabc7-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="dabc7-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dabc7-121">Request headers</span></span>
| <span data-ttu-id="dabc7-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="dabc7-122">Name</span></span>       | <span data-ttu-id="dabc7-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="dabc7-123">Type</span></span> | <span data-ttu-id="dabc7-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="dabc7-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="dabc7-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="dabc7-125">Authorization</span></span>  | <span data-ttu-id="dabc7-126">string</span><span class="sxs-lookup"><span data-stu-id="dabc7-126">string</span></span>  | <span data-ttu-id="dabc7-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dabc7-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="dabc7-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dabc7-129">Request body</span></span>
<span data-ttu-id="dabc7-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="dabc7-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="dabc7-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dabc7-131">Response</span></span>

<span data-ttu-id="dabc7-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dabc7-132">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="dabc7-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dabc7-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="dabc7-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dabc7-134">Request</span></span>
<span data-ttu-id="dabc7-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dabc7-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_memberof"
}-->
```http
GET https://graph.microsoft.com/beta/contacts/{id}/memberOf
```
##### <a name="response"></a><span data-ttu-id="dabc7-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dabc7-136">Response</span></span>
<span data-ttu-id="dabc7-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dabc7-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List memberOf",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

---
title: 'group: getMemberObjects'
description: 'Devolver todos los grupos y unidades administrativas que el grupo es un miembro de. La comprobación es transitiva. Nota: Los grupos no pueden ser miembros de los roles de Active directory, por lo que no se devolverá ninguna función de Active directory.'
localization_priority: Normal
ms.openlocfilehash: 72d9bc23fa5499ebf1f43d8baee9c9562a57c645
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27838111"
---
# <a name="group-getmemberobjects"></a><span data-ttu-id="22ebf-105">group: getMemberObjects</span><span class="sxs-lookup"><span data-stu-id="22ebf-105">group: getMemberObjects</span></span>

> <span data-ttu-id="22ebf-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="22ebf-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="22ebf-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="22ebf-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="22ebf-108">Devolver todos los grupos y unidades administrativas que el grupo es un miembro de.</span><span class="sxs-lookup"><span data-stu-id="22ebf-108">Return all of the groups and administrative units that the group is a member of.</span></span> <span data-ttu-id="22ebf-109">La comprobación es transitiva.</span><span class="sxs-lookup"><span data-stu-id="22ebf-109">The check is transitive.</span></span> <span data-ttu-id="22ebf-110">Nota: Los grupos no pueden ser miembros de los roles de Active directory, por lo que no se devolverá ninguna función de Active directory.</span><span class="sxs-lookup"><span data-stu-id="22ebf-110">Note: Groups cannot be members of directory roles, so no directory roles will be returned.</span></span>

## <a name="permissions"></a><span data-ttu-id="22ebf-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="22ebf-111">Permissions</span></span>
<span data-ttu-id="22ebf-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="22ebf-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="22ebf-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="22ebf-114">Permission type</span></span>      | <span data-ttu-id="22ebf-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="22ebf-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="22ebf-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="22ebf-116">Delegated (work or school account)</span></span> | <span data-ttu-id="22ebf-117">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="22ebf-117">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="22ebf-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="22ebf-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="22ebf-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="22ebf-119">Not supported.</span></span>    |
|<span data-ttu-id="22ebf-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="22ebf-120">Application</span></span> | <span data-ttu-id="22ebf-121">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="22ebf-121">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="22ebf-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="22ebf-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/getMemberObjects
```

## <a name="request-headers"></a><span data-ttu-id="22ebf-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="22ebf-123">Request headers</span></span>
| <span data-ttu-id="22ebf-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="22ebf-124">Name</span></span>       | <span data-ttu-id="22ebf-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="22ebf-125">Type</span></span> | <span data-ttu-id="22ebf-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="22ebf-126">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="22ebf-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="22ebf-127">Authorization</span></span>  | <span data-ttu-id="22ebf-128">string</span><span class="sxs-lookup"><span data-stu-id="22ebf-128">string</span></span>  | <span data-ttu-id="22ebf-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="22ebf-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="22ebf-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="22ebf-131">Request body</span></span>
<span data-ttu-id="22ebf-132">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="22ebf-132">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="22ebf-133">Parámetro</span><span class="sxs-lookup"><span data-stu-id="22ebf-133">Parameter</span></span>    | <span data-ttu-id="22ebf-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="22ebf-134">Type</span></span>   |<span data-ttu-id="22ebf-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="22ebf-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="22ebf-136">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="22ebf-136">securityEnabledOnly</span></span>|<span data-ttu-id="22ebf-137">Boolean</span><span class="sxs-lookup"><span data-stu-id="22ebf-137">Boolean</span></span>|<span data-ttu-id="22ebf-p106">Establecer en **false**. La devolución solo de grupos con la seguridad activada solo es compatible para usuarios.</span><span class="sxs-lookup"><span data-stu-id="22ebf-p106">Set to **false**. Returning only security-enabled groups is supported for users only.</span></span>|

## <a name="response"></a><span data-ttu-id="22ebf-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="22ebf-140">Response</span></span>
<span data-ttu-id="22ebf-141">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la colección String en el cuerpo de la respuesta que contiene los identificadores de los grupos de los que el grupo sea miembro.</span><span class="sxs-lookup"><span data-stu-id="22ebf-141">If successful, this method returns `200 OK` response code and String collection in the response body that contains the IDs of the groups that the group is a member of.</span></span>

## <a name="example"></a><span data-ttu-id="22ebf-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="22ebf-142">Example</span></span>
#### <a name="request"></a><span data-ttu-id="22ebf-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="22ebf-143">Request</span></span>
<span data-ttu-id="22ebf-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="22ebf-144">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_getmemberobjects"
}-->
```http
POST https://graph.microsoft.com/beta/groups/{id}/getMemberObjects
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": false
}
```

#### <a name="response"></a><span data-ttu-id="22ebf-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="22ebf-145">Response</span></span>
<span data-ttu-id="22ebf-146">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="22ebf-146">The following is an example of the response.</span></span>
><span data-ttu-id="22ebf-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="22ebf-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "string",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "value": [
    "string-value"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: getMemberObjects",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

---
title: Lista scopedAdministratorOf
description: Recuperar una lista de scopedRoleMembership para el usuario.
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 71e58dfb1195fdbbddf3b658d2aaab6f28e7e21c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939612"
---
# <a name="list-scopedadministratorof"></a><span data-ttu-id="825e8-103">Lista scopedAdministratorOf</span><span class="sxs-lookup"><span data-stu-id="825e8-103">List scopedAdministratorOf</span></span>

> <span data-ttu-id="825e8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="825e8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="825e8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="825e8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="825e8-106">Recuperar una lista de [scopedRoleMembership](../resources/scopedrolemembership.md) para el usuario.</span><span class="sxs-lookup"><span data-stu-id="825e8-106">Retrieve a list of [scopedRoleMembership](../resources/scopedrolemembership.md) for the user.</span></span>
## <a name="permissions"></a><span data-ttu-id="825e8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="825e8-107">Permissions</span></span>
<span data-ttu-id="825e8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="825e8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="825e8-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="825e8-110">Permission type</span></span>      | <span data-ttu-id="825e8-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="825e8-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="825e8-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="825e8-112">Delegated (work or school account)</span></span> | <span data-ttu-id="825e8-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="825e8-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="825e8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="825e8-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="825e8-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="825e8-115">Not supported.</span></span>    |
|<span data-ttu-id="825e8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="825e8-116">Application</span></span> | <span data-ttu-id="825e8-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="825e8-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="825e8-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="825e8-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/scopedAdministratorOf
GET /users/{id}/scopedAdministratorOf

```
## <a name="optional-query-parameters"></a><span data-ttu-id="825e8-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="825e8-119">Optional query parameters</span></span>
<span data-ttu-id="825e8-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="825e8-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="825e8-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="825e8-121">Request headers</span></span>
| <span data-ttu-id="825e8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="825e8-122">Header</span></span>       | <span data-ttu-id="825e8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="825e8-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="825e8-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="825e8-124">Authorization</span></span>  | <span data-ttu-id="825e8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="825e8-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="825e8-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="825e8-127">Request body</span></span>
<span data-ttu-id="825e8-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="825e8-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="825e8-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="825e8-129">Response</span></span>

<span data-ttu-id="825e8-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [scopedRoleMembership](../resources/scopedrolemembership.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="825e8-130">If successful, this method returns a `200 OK` response code and collection of [scopedRoleMembership](../resources/scopedrolemembership.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="825e8-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="825e8-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="825e8-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="825e8-132">Request</span></span>
<span data-ttu-id="825e8-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="825e8-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_scopedadministratorof"
}-->
```http
GET https://graph.microsoft.com/beta/me/scopedAdministratorOf
```
##### <a name="response"></a><span data-ttu-id="825e8-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="825e8-134">Response</span></span>
<span data-ttu-id="825e8-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="825e8-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.scopedrolemembership",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 307

{
  "value": [
    {
      "roleId": "roleId-value",
      "administrativeUnitId": "administrativeUnitId-value",
      "roleMemberInfo": {
        "id": "id-value",
        "displayName": "displayName-value",
        "userPrincipalName": "userPrincipalName-value"
      },
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List scopedAdministratorOf",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

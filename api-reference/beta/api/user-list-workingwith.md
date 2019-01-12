---
title: Lista workingWith
description: Introducción a la lista de usuarios que un usuario ha trabajado con calculado.
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 5f9445dcee294f20f5eadf18cdd648805142c53d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953570"
---
# <a name="list-workingwith"></a><span data-ttu-id="09dce-103">Lista workingWith</span><span class="sxs-lookup"><span data-stu-id="09dce-103">List workingWith</span></span>

> <span data-ttu-id="09dce-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="09dce-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="09dce-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="09dce-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="09dce-106">Introducción a la lista de usuarios que un usuario ha trabajado con calculado.</span><span class="sxs-lookup"><span data-stu-id="09dce-106">Calculated insight for the list of users that a user has been working with.</span></span>

## <a name="permissions"></a><span data-ttu-id="09dce-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="09dce-107">Permissions</span></span>
<span data-ttu-id="09dce-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="09dce-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="09dce-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="09dce-110">Permission type</span></span>      | <span data-ttu-id="09dce-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="09dce-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="09dce-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="09dce-112">Delegated (work or school account)</span></span> | <span data-ttu-id="09dce-113">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="09dce-113">User.Read.All</span></span>    |
|<span data-ttu-id="09dce-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="09dce-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="09dce-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="09dce-115">Not supported.</span></span>    |
|<span data-ttu-id="09dce-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="09dce-116">Application</span></span> | <span data-ttu-id="09dce-117">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="09dce-117">User.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="09dce-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="09dce-118">HTTP request</span></span>
```http
GET /me/workingWith
GET /users/{id | userPrincipalName}/workingWith
GET /drive/root/createdByUser/workingWith
GET /drive/root/lastModifiedByUser/workingWith
```
## <a name="optional-query-parameters"></a><span data-ttu-id="09dce-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="09dce-119">Optional query parameters</span></span>
<span data-ttu-id="09dce-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="09dce-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="09dce-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="09dce-121">Request headers</span></span>
| <span data-ttu-id="09dce-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09dce-122">Header</span></span>         | <span data-ttu-id="09dce-123">Valor</span><span class="sxs-lookup"><span data-stu-id="09dce-123">Value</span></span>                      |
|:---------------|:---------------------------|
| <span data-ttu-id="09dce-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="09dce-124">Authorization</span></span>  | <span data-ttu-id="09dce-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="09dce-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="09dce-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="09dce-127">Content-Type</span></span>   | <span data-ttu-id="09dce-128">application/json</span><span class="sxs-lookup"><span data-stu-id="09dce-128">application/json</span></span>           |

## <a name="request-body"></a><span data-ttu-id="09dce-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="09dce-129">Request body</span></span>
<span data-ttu-id="09dce-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="09dce-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="09dce-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="09dce-131">Response</span></span>

<span data-ttu-id="09dce-132">Si se realiza correctamente, este método devuelve un código de respuesta OK 200 y una colección de objetos de [usuario](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="09dce-132">If successful, this method returns a 200 OK response code and collection of [User](../resources/user.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="09dce-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="09dce-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="09dce-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="09dce-134">Request</span></span>
```http
GET https://graph.microsoft.com/beta/me/workingWith
```
##### <a name="response"></a><span data-ttu-id="09dce-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="09dce-135">Response</span></span>
<span data-ttu-id="09dce-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="09dce-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 98

{
  "id": "id-value",
  "preferredName": "preferredName-value",
  "Email": "Email-value",
}
```

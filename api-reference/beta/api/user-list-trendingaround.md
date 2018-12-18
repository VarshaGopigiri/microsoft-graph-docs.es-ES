---
title: Lista trendingAround
description: Insight calculado que devuelve la lista de elementos tendencias alrededor de un usuario.
author: dkershaw10
ms.openlocfilehash: 2f2595cbaacc74053b23d6b26b64fb9a17e2924a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27333834"
---
# <a name="list-trendingaround"></a><span data-ttu-id="65d49-103">Lista trendingAround</span><span class="sxs-lookup"><span data-stu-id="65d49-103">List trendingAround</span></span>

> <span data-ttu-id="65d49-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="65d49-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="65d49-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="65d49-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="65d49-106">Insight calculado que devuelve la lista de elementos tendencias alrededor de un usuario.</span><span class="sxs-lookup"><span data-stu-id="65d49-106">Calculated insight that returns the list of items trending around a user.</span></span>

<span data-ttu-id="65d49-107">**Nota:** Esta API se en desuso y se ha reemplazado por la [API de tendencias](../resources/insights-trending.md).</span><span class="sxs-lookup"><span data-stu-id="65d49-107">**Note:** This API will be deprecated and replaced by the [Trending API](../resources/insights-trending.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="65d49-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="65d49-108">Permissions</span></span>
<span data-ttu-id="65d49-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="65d49-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="65d49-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="65d49-111">Permission type</span></span>      | <span data-ttu-id="65d49-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="65d49-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="65d49-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="65d49-113">Delegated (work or school account)</span></span> | <span data-ttu-id="65d49-114">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="65d49-114">Sites.Read.All</span></span>    |
|<span data-ttu-id="65d49-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="65d49-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="65d49-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="65d49-116">Not supported.</span></span>    |
|<span data-ttu-id="65d49-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="65d49-117">Application</span></span> | <span data-ttu-id="65d49-118">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="65d49-118">Sites.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="65d49-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="65d49-119">HTTP request</span></span>
```http
GET /me/trendingAround
GET /users/{id | userPrincipalName}/trendingAround
GET /drive/root/createdByUser/trendingAround
GET /drive/root/lastModifiedByUser/trendingAround
```
## <a name="optional-query-parameters"></a><span data-ttu-id="65d49-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="65d49-120">Optional query parameters</span></span>
<span data-ttu-id="65d49-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="65d49-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="65d49-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="65d49-122">Request headers</span></span>
| <span data-ttu-id="65d49-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65d49-123">Header</span></span>         | <span data-ttu-id="65d49-124">Valor</span><span class="sxs-lookup"><span data-stu-id="65d49-124">Value</span></span>                      |
|:---------------|:---------------------------|
| <span data-ttu-id="65d49-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="65d49-125">Authorization</span></span>  | <span data-ttu-id="65d49-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="65d49-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="65d49-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="65d49-128">Content-Type</span></span>   | <span data-ttu-id="65d49-129">application/json</span><span class="sxs-lookup"><span data-stu-id="65d49-129">application/json</span></span>           |

## <a name="request-body"></a><span data-ttu-id="65d49-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="65d49-130">Request body</span></span>
<span data-ttu-id="65d49-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="65d49-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="65d49-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65d49-132">Response</span></span>

<span data-ttu-id="65d49-133">Si se realiza correctamente, este método devuelve un código de respuesta OK 200 y una colección de objetos [driveItem](../resources/driveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="65d49-133">If successful, this method returns a 200 OK response code and collection of [driveItem](../resources/driveitem.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="65d49-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="65d49-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="65d49-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="65d49-135">Request</span></span>
```http
GET https://graph.microsoft.com/beta/me/trendingAround
```
##### <a name="response"></a><span data-ttu-id="65d49-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65d49-136">Response</span></span>
<span data-ttu-id="65d49-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="65d49-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 226

{
  "id": "id-value",
  "name": "name-value",
  "DateTimeCreated": "DateTimeCreated-value",
  "DateTimeLastModified": "DateTimeLastModified-value",
  "webUrl": "webUrl-value",
}
```
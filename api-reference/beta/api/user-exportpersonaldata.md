---
title: 'usuario: exportPersonalData'
description: Envía una solicitud de operación de la directiva de datos, realizada por un administrador de la compañía para exportar datos de un usuario organizativa.
localization_priority: Normal
ms.openlocfilehash: d660994868e331fb8c1813bb9ff90aebe4790e9d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845342"
---
# <a name="user-exportpersonaldata"></a><span data-ttu-id="f7978-103">usuario: exportPersonalData</span><span class="sxs-lookup"><span data-stu-id="f7978-103">user: exportPersonalData</span></span>

<span data-ttu-id="f7978-104">Envía una solicitud de operación de la directiva de datos, realizada por un administrador de la compañía para exportar datos de un usuario organizativa.</span><span class="sxs-lookup"><span data-stu-id="f7978-104">Submits a data policy operation request, made by a company administrator to export an organizational user's data.</span></span>

## <a name="permissions"></a><span data-ttu-id="f7978-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f7978-105">Permissions</span></span>
<span data-ttu-id="f7978-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f7978-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f7978-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f7978-108">Permission type</span></span>      | <span data-ttu-id="f7978-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f7978-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f7978-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f7978-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="f7978-111">User.Export.All y User.Read.All</span><span class="sxs-lookup"><span data-stu-id="f7978-111">User.Export.All and User.Read.All</span></span>  |
|<span data-ttu-id="f7978-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f7978-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="f7978-113">No aplicable</span><span class="sxs-lookup"><span data-stu-id="f7978-113">Not applicable</span></span>  |
|<span data-ttu-id="f7978-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f7978-114">Application</span></span> | <span data-ttu-id="f7978-115">User.Export.All y User.Read.All</span><span class="sxs-lookup"><span data-stu-id="f7978-115">User.Export.All and User.Read.All</span></span> |

><span data-ttu-id="f7978-116">**Nota:** Cuando se usa el permiso delegado exportación sólo puede realizarse por un administrador de la compañía.</span><span class="sxs-lookup"><span data-stu-id="f7978-116">**Note:** Export can only be performed by a company administrator when the delegated permission is used.</span></span>

## <a name="http-request"></a><span data-ttu-id="f7978-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f7978-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/<id>/exportPersonalData

```
## <a name="request-headers"></a><span data-ttu-id="f7978-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f7978-118">Request headers</span></span>
| <span data-ttu-id="f7978-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7978-119">Name</span></span>       | <span data-ttu-id="f7978-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7978-120">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="f7978-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="f7978-121">Authorization</span></span>  | <span data-ttu-id="f7978-122">Bearer {token}</span><span class="sxs-lookup"><span data-stu-id="f7978-122">Bearer {token}</span></span>|

## <a name="request-body"></a><span data-ttu-id="f7978-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f7978-123">Request body</span></span>
<span data-ttu-id="f7978-124">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="f7978-124">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f7978-125">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f7978-125">Parameter</span></span>    | <span data-ttu-id="f7978-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="f7978-126">Type</span></span>   |<span data-ttu-id="f7978-127">Description</span><span class="sxs-lookup"><span data-stu-id="f7978-127">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="f7978-128">storageLocation</span><span class="sxs-lookup"><span data-stu-id="f7978-128">storageLocation</span></span>|<span data-ttu-id="f7978-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="f7978-129">String</span></span>|<span data-ttu-id="f7978-130">Esto es una dirección URL de firma (SAS) de acceso compartido a una cuenta de almacenamiento de Azure, para que se deben exportar los datos.</span><span class="sxs-lookup"><span data-stu-id="f7978-130">This is a shared access signature (SAS) URL to an Azure Storage account, to where data should be exported.</span></span>|

## <a name="response"></a><span data-ttu-id="f7978-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7978-131">Response</span></span>
<span data-ttu-id="f7978-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted`.</span><span class="sxs-lookup"><span data-stu-id="f7978-132">If successful, this method returns a `202 Accepted` response code.</span></span> <span data-ttu-id="f7978-133">No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f7978-133">It does not return anything in the response body.</span></span> <span data-ttu-id="f7978-134">La respuesta contiene los siguientes encabezados.</span><span class="sxs-lookup"><span data-stu-id="f7978-134">The response contains the following headers.</span></span>

| <span data-ttu-id="f7978-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7978-135">Name</span></span>       | <span data-ttu-id="f7978-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7978-136">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="f7978-137">Location</span><span class="sxs-lookup"><span data-stu-id="f7978-137">Location</span></span>  | <span data-ttu-id="f7978-138">Dirección URL para comprobar el estado de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f7978-138">URL to check on the status of the Request.</span></span> |
| <span data-ttu-id="f7978-139">Retry-After</span><span class="sxs-lookup"><span data-stu-id="f7978-139">Retry-After</span></span>  | <span data-ttu-id="f7978-140">Período de tiempo en segundos.</span><span class="sxs-lookup"><span data-stu-id="f7978-140">Time period in seconds.</span></span> <span data-ttu-id="f7978-141">Maker solicitud debe esperar a que esto durante cuánto tiempo después de enviar una solicitud para comprobar el estado.</span><span class="sxs-lookup"><span data-stu-id="f7978-141">Request maker should wait this long after submitting a request to check for the status.</span></span> |


## <a name="example"></a><span data-ttu-id="f7978-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7978-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f7978-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f7978-143">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "user_exportpersonaldata"
}-->
```http
POST https://graph.microsoft.com/beta/users/{id}/exportPersonalData
Content-type: application/json
Content-length: 48

{
  "storageLocation": "storageLocation-value"
}
```
##### <a name="response"></a><span data-ttu-id="f7978-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7978-144">Response</span></span>

```
{
  Location: https://graph.microsoft.com/beta/dataPolicyOperations/d007e3da-cd9b-4b02-8d66-422403c53e3f
  Retry-After: 60
}
```

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: exportPersonalData",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

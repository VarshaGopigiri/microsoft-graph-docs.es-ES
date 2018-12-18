---
title: 'usuario: exportPersonalData'
description: Envía una solicitud de operación de la directiva de datos, realizada por un administrador de la compañía para exportar datos de un usuario organizativa.
ms.openlocfilehash: 27a299a4cfa6ccc3016a1f706b452840aa5dc396
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27329130"
---
# <a name="user-exportpersonaldata"></a><span data-ttu-id="17f46-103">usuario: exportPersonalData</span><span class="sxs-lookup"><span data-stu-id="17f46-103">user: exportPersonalData</span></span>

<span data-ttu-id="17f46-104">Envía una solicitud de operación de la directiva de datos, realizada por un administrador de la compañía para exportar datos de un usuario organizativa.</span><span class="sxs-lookup"><span data-stu-id="17f46-104">Submits a data policy operation request, made by a Company Administrator to export an organizational user's data.</span></span>

## <a name="permissions"></a><span data-ttu-id="17f46-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="17f46-105">Permissions</span></span>
<span data-ttu-id="17f46-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="17f46-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="17f46-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="17f46-108">Permission type</span></span>      | <span data-ttu-id="17f46-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="17f46-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="17f46-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="17f46-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="17f46-111">User.Export.All y User.Read.All</span><span class="sxs-lookup"><span data-stu-id="17f46-111">User.Export.All and User.Read.All</span></span>  |
|<span data-ttu-id="17f46-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="17f46-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="17f46-113">No aplicable</span><span class="sxs-lookup"><span data-stu-id="17f46-113">Not applicable</span></span>  |
|<span data-ttu-id="17f46-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="17f46-114">Application</span></span> | <span data-ttu-id="17f46-115">User.Export.All y User.Read.All</span><span class="sxs-lookup"><span data-stu-id="17f46-115">User.Export.All and User.Read.All</span></span> |

><span data-ttu-id="17f46-116">Nota: Exportación sólo puede realizarse por un administrador de la compañía cuando se usa el permiso delegado.</span><span class="sxs-lookup"><span data-stu-id="17f46-116">Note: Export can only be performed by a Company Administrator when using the delegated permission.</span></span>

## <a name="http-request"></a><span data-ttu-id="17f46-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="17f46-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/<id>/exportPersonalData

```
## <a name="request-headers"></a><span data-ttu-id="17f46-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="17f46-118">Request headers</span></span>
| <span data-ttu-id="17f46-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="17f46-119">Name</span></span>       | <span data-ttu-id="17f46-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="17f46-120">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="17f46-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="17f46-121">Authorization</span></span>  | <span data-ttu-id="17f46-122">Bearer {token}</span><span class="sxs-lookup"><span data-stu-id="17f46-122">Bearer {token}</span></span>|

## <a name="request-body"></a><span data-ttu-id="17f46-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="17f46-123">Request body</span></span>
<span data-ttu-id="17f46-124">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="17f46-124">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="17f46-125">Parámetro</span><span class="sxs-lookup"><span data-stu-id="17f46-125">Parameter</span></span>    | <span data-ttu-id="17f46-126">Type</span><span class="sxs-lookup"><span data-stu-id="17f46-126">Type</span></span>   |<span data-ttu-id="17f46-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="17f46-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="17f46-128">storageLocation</span><span class="sxs-lookup"><span data-stu-id="17f46-128">storageLocation</span></span>|<span data-ttu-id="17f46-129">String</span><span class="sxs-lookup"><span data-stu-id="17f46-129">String</span></span>|<span data-ttu-id="17f46-130">Esto es una dirección URL de firma (SAS) de acceso compartido a una cuenta de almacenamiento de Azure, para que se deben exportar los datos.</span><span class="sxs-lookup"><span data-stu-id="17f46-130">This is a shared access signature (SAS) URL to an Azure Storage account, to where data should be exported.</span></span>|

## <a name="response"></a><span data-ttu-id="17f46-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17f46-131">Response</span></span>
<span data-ttu-id="17f46-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="17f46-p102">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="17f46-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="17f46-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="17f46-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="17f46-135">Request</span></span>
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

##### <a name="response"></a><span data-ttu-id="17f46-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17f46-136">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
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

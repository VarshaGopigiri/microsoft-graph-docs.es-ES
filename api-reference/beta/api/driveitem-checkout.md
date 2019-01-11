---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Desproteger archivos
localization_priority: Normal
ms.openlocfilehash: 4201f9a075947182cdcd2b69b222896e3c60f93d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27870004"
---
# <a name="check-out-a-driveitem-resource"></a><span data-ttu-id="6471e-102">Extraer un recurso DriveItem del repositorio</span><span class="sxs-lookup"><span data-stu-id="6471e-102">Check-out a DriveItem resource</span></span>

> <span data-ttu-id="6471e-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6471e-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6471e-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6471e-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6471e-105">Extraiga un recurso driveItem del repositorio para evitar que otros usuarios editen el documento y que sus cambios estén visibles hasta que el documento se [inserte en el repositorio](driveitem-checkin.md).</span><span class="sxs-lookup"><span data-stu-id="6471e-105">Check-out a driveItem resource to prevent others from editing the document, and your changes from being visible until the documented is [checked-in](driveitem-checkin.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="6471e-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="6471e-106">Permissions</span></span>

<span data-ttu-id="6471e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6471e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6471e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6471e-109">Permission type</span></span>      | <span data-ttu-id="6471e-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6471e-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6471e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6471e-111">Delegated (work or school account)</span></span> | <span data-ttu-id="6471e-112">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6471e-112">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="6471e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6471e-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6471e-114">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6471e-114">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="6471e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6471e-115">Application</span></span> | <span data-ttu-id="6471e-116">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6471e-116">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6471e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6471e-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/checkout
POST /groups/{groupId}/drive/items/{itemId}/checkout
POST /me/drive/items/{item-id}/checkout
POST /sites/{siteId}/drive/items/{itemId}/checkout
POST /users/{userId}/drive/items/{itemId}/checkout
```

### <a name="request-body"></a><span data-ttu-id="6471e-118">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="6471e-118">Request body</span></span>

<span data-ttu-id="6471e-119">No es necesario ningún cuerpo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="6471e-119">No request body is required.</span></span>

## <a name="example"></a><span data-ttu-id="6471e-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6471e-120">Example</span></span>

<span data-ttu-id="6471e-121">Este ejemplo extrae un archivo identificado por `{item-id}` del repositorio.</span><span class="sxs-lookup"><span data-stu-id="6471e-121">This example checks out a file identified by `{item-id}`.</span></span>

<!-- { "blockType": "request", "name": "checkout-item", "scopes": "files.readwrite", "target": "action" } -->

```http
POST /drives/{drive-id}/items/{item-id}/checkout
```

## <a name="response"></a><span data-ttu-id="6471e-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6471e-122">Response</span></span>

<span data-ttu-id="6471e-123">Si se realiza correctamente, la llamada API devuelve `204 No content`.</span><span class="sxs-lookup"><span data-stu-id="6471e-123">If successful, the API call returns a `204 No content`.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No content
```

### <a name="remarks"></a><span data-ttu-id="6471e-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6471e-124">Remarks</span></span>


[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Create a copy of an existing item.",
  "keywords": "copy existing item",
  "section": "documentation",
  "tocPath": "Items/Copy"
} -->

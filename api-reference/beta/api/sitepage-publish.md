---
author: rahmit
ms.author: rahmit
ms.date: 09/10/2018
title: Publicar la página
ms.openlocfilehash: d932b1d37b5ab81f86f6e87aab43aa1cf9dc3eae
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084736"
---
# <a name="sitepage-publish"></a><span data-ttu-id="7d60b-102">sitePage: publicar</span><span class="sxs-lookup"><span data-stu-id="7d60b-102">sitePage: publish</span></span>

> <span data-ttu-id="7d60b-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7d60b-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7d60b-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7d60b-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7d60b-105">Publicar la versión más reciente de un recurso [sitePage][] , que hace que la versión de la página esté disponible para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="7d60b-105">Publish the latest version of a [sitePage][] resource, which makes the version of the page available to all users.</span></span> <span data-ttu-id="7d60b-106">Si la página se desprotege, compruebe en la página y publicarlo.</span><span class="sxs-lookup"><span data-stu-id="7d60b-106">If the page is checked out, check in the page and publish it.</span></span> <span data-ttu-id="7d60b-107">Si la página está desprotegida por el autor de la llamada de esta API, la página se registra automáticamente y, a continuación, se ha publicado.</span><span class="sxs-lookup"><span data-stu-id="7d60b-107">If the page is checked out to the caller of this API, the page is automatically checked in and then published.</span></span>

[sitePage]: ../resources/sitepage.md

## <a name="permissions"></a><span data-ttu-id="7d60b-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="7d60b-109">Permissions</span></span>

<span data-ttu-id="7d60b-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7d60b-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7d60b-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7d60b-112">Permission type</span></span>      | <span data-ttu-id="7d60b-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7d60b-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7d60b-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7d60b-114">Delegated (work or school account)</span></span> | <span data-ttu-id="7d60b-115">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7d60b-115">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="7d60b-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7d60b-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7d60b-117">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7d60b-117">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="7d60b-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7d60b-118">Application</span></span> | <span data-ttu-id="7d60b-119">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7d60b-119">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7d60b-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7d60b-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /sites/{siteId}/pages/{pageId}/publish
```

## <a name="request-body"></a><span data-ttu-id="7d60b-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7d60b-121">Request body</span></span>

<span data-ttu-id="7d60b-122">Este mensaje no tiene un cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7d60b-122">This message does not have a request body.</span></span> <span data-ttu-id="7d60b-123">Se omitirá el cuerpo de la solicitud que se envían.</span><span class="sxs-lookup"><span data-stu-id="7d60b-123">Any request body sent will be ignored.</span></span>

## <a name="response"></a><span data-ttu-id="7d60b-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d60b-124">Response</span></span>

<span data-ttu-id="7d60b-125">Si se realiza correctamente, la llamada API devuelve `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="7d60b-125">If successful, the API call returns a `204 No Content`.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```


<!-- {
  "type": "#page.annotation",
  "description": "Publish a page.",
  "keywords": "publish page",
  "section": "documentation",
  "tocPath": "Pages/Publish"
} -->

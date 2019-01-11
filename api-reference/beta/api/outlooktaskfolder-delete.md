---
title: Eliminar outlookTaskFolder
description: Elimine la carpeta de tareas de Outlook especificada.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: c8fd5a62113ee9ad66a7ca080f5b4d2593834c2d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27836361"
---
# <a name="delete-outlooktaskfolder"></a><span data-ttu-id="f4315-103">Eliminar outlookTaskFolder</span><span class="sxs-lookup"><span data-stu-id="f4315-103">Delete outlookTaskFolder</span></span>

> <span data-ttu-id="f4315-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f4315-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f4315-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f4315-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f4315-106">Elimine la carpeta de tareas de Outlook especificada.</span><span class="sxs-lookup"><span data-stu-id="f4315-106">Delete the specified Outlook task folder.</span></span>
## <a name="permissions"></a><span data-ttu-id="f4315-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="f4315-107">Permissions</span></span>
<span data-ttu-id="f4315-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f4315-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f4315-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f4315-110">Permission type</span></span>      | <span data-ttu-id="f4315-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f4315-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f4315-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f4315-112">Delegated (work or school account)</span></span> | <span data-ttu-id="f4315-113">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f4315-113">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="f4315-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f4315-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f4315-115">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f4315-115">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="f4315-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f4315-116">Application</span></span> | <span data-ttu-id="f4315-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f4315-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f4315-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f4315-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /users/{id|userPrincipalName}/outlook/taskFolders/{id}
DELETE /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}

```
## <a name="request-headers"></a><span data-ttu-id="f4315-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f4315-119">Request headers</span></span>
| <span data-ttu-id="f4315-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4315-120">Name</span></span>       | <span data-ttu-id="f4315-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4315-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="f4315-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="f4315-122">Authorization</span></span>  | <span data-ttu-id="f4315-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f4315-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f4315-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f4315-125">Request body</span></span>
<span data-ttu-id="f4315-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f4315-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f4315-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4315-127">Response</span></span>

<span data-ttu-id="f4315-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f4315-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f4315-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f4315-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f4315-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f4315-131">Request</span></span>
<span data-ttu-id="f4315-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f4315-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_outlooktaskfolder"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/outlook/taskFolders('AAMkADIyAAAhrbPXAAA=')
```
##### <a name="response"></a><span data-ttu-id="f4315-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4315-133">Response</span></span>
<span data-ttu-id="f4315-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f4315-134">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete outlookTaskFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

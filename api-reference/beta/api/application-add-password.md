---
title: Agregar la contraseña de la aplicación
description: Agrega una contraseña segura a una aplicación.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: 03e3e712f621856634c931202904db3300d6166b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27829403"
---
# <a name="add-application-password"></a><span data-ttu-id="b2281-103">Agregar la contraseña de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b2281-103">Add application password</span></span>

> <span data-ttu-id="b2281-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b2281-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b2281-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b2281-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b2281-106">Agrega una contraseña segura a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2281-106">Adds a strong password to an application.</span></span>

## <a name="permissions"></a><span data-ttu-id="b2281-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b2281-107">Permissions</span></span>
<span data-ttu-id="b2281-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b2281-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b2281-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b2281-110">Permission type</span></span>      | <span data-ttu-id="b2281-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b2281-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b2281-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b2281-112">Delegated (work or school account)</span></span> | <span data-ttu-id="b2281-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="b2281-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="b2281-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b2281-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b2281-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b2281-115">Not supported.</span></span>    |
|<span data-ttu-id="b2281-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b2281-116">Application</span></span> | <span data-ttu-id="b2281-117">Application.ReadWrite.OwnedBy, Application.ReadWrite.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="b2281-117">Application.ReadWrite.OwnedBy, Application.ReadWrite.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b2281-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b2281-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /applications/{id}/addPassword
```

## <a name="request-headers"></a><span data-ttu-id="b2281-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b2281-119">Request headers</span></span>
| <span data-ttu-id="b2281-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="b2281-120">Name</span></span>       | <span data-ttu-id="b2281-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="b2281-121">Type</span></span> | <span data-ttu-id="b2281-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2281-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="b2281-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="b2281-123">Authorization</span></span>  | <span data-ttu-id="b2281-124">string</span><span class="sxs-lookup"><span data-stu-id="b2281-124">string</span></span>  | <span data-ttu-id="b2281-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b2281-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b2281-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b2281-127">Request body</span></span>
<span data-ttu-id="b2281-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b2281-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b2281-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2281-129">Response</span></span>

<span data-ttu-id="b2281-130">Si tiene éxito, este método devuelve una `200 OK` objeto de código y la contraseña de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b2281-130">If successful, this method returns a `200 OK` response code and password object in the response body.</span></span> <span data-ttu-id="b2281-131">Azure AD genera una contraseña segura que se devuelve a través de la `secretText` (propiedad).</span><span class="sxs-lookup"><span data-stu-id="b2281-131">Azure AD generates a strong password which is returned via the `secretText` property.</span></span> <span data-ttu-id="b2281-132">No hay ninguna forma de recuperar esta contraseña en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b2281-132">There is no way to retrieve this password in the future.</span></span>

## <a name="example"></a><span data-ttu-id="b2281-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b2281-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b2281-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b2281-134">Request</span></span>
<span data-ttu-id="b2281-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b2281-135">Here is an example of the request.</span></span>

```http
POST https://graph.microsoft.com/beta/applications/{id}/addPassword
```
##### <a name="response"></a><span data-ttu-id="b2281-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2281-136">Response</span></span>
<span data-ttu-id="b2281-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b2281-137">Here is an example of the response.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1044

{
    "customKeyIdentifier": "Binary",
    "endDateTime": "String (timestamp)",
    "keyId": "String (identifier)",
    "startDateTime": "String (timestamp)",
    "secretText": "String",
    "hint": "String"
}
```

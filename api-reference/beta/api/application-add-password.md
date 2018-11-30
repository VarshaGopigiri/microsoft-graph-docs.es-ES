---
title: Agregar la contraseña de la aplicación
description: Agrega una contraseña segura a una aplicación.
ms.openlocfilehash: 78ccb6cced055ca7f2d2ab201e844a9f50f36939
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083695"
---
# <a name="add-application-password"></a><span data-ttu-id="e8dec-103">Agregar la contraseña de la aplicación</span><span class="sxs-lookup"><span data-stu-id="e8dec-103">Add application password</span></span>

> <span data-ttu-id="e8dec-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e8dec-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e8dec-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e8dec-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e8dec-106">Agrega una contraseña segura a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e8dec-106">Adds a strong password to an application.</span></span>

## <a name="permissions"></a><span data-ttu-id="e8dec-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e8dec-107">Permissions</span></span>
<span data-ttu-id="e8dec-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e8dec-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e8dec-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e8dec-110">Permission type</span></span>      | <span data-ttu-id="e8dec-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e8dec-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e8dec-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e8dec-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e8dec-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="e8dec-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="e8dec-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e8dec-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e8dec-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e8dec-115">Not supported.</span></span>    |
|<span data-ttu-id="e8dec-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e8dec-116">Application</span></span> | <span data-ttu-id="e8dec-117">Application.ReadWrite.OwnedBy, Application.ReadWrite.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="e8dec-117">Application.ReadWrite.OwnedBy, Application.ReadWrite.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e8dec-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e8dec-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /applications/{id}/addPassword
```

## <a name="request-headers"></a><span data-ttu-id="e8dec-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e8dec-119">Request headers</span></span>
| <span data-ttu-id="e8dec-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="e8dec-120">Name</span></span>       | <span data-ttu-id="e8dec-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="e8dec-121">Type</span></span> | <span data-ttu-id="e8dec-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8dec-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="e8dec-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="e8dec-123">Authorization</span></span>  | <span data-ttu-id="e8dec-124">string</span><span class="sxs-lookup"><span data-stu-id="e8dec-124">string</span></span>  | <span data-ttu-id="e8dec-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e8dec-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e8dec-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e8dec-127">Request body</span></span>
<span data-ttu-id="e8dec-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e8dec-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e8dec-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8dec-129">Response</span></span>

<span data-ttu-id="e8dec-130">Si tiene éxito, este método devuelve una `200 OK` objeto de código y la contraseña de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e8dec-130">If successful, this method returns a `200 OK` response code and password object in the response body.</span></span> <span data-ttu-id="e8dec-131">Azure AD genera una contraseña segura que se devuelve a través de la `secretText` (propiedad).</span><span class="sxs-lookup"><span data-stu-id="e8dec-131">Azure AD generates a strong password which is returned via the `secretText` property.</span></span> <span data-ttu-id="e8dec-132">No hay ninguna forma de recuperar esta contraseña en el futuro.</span><span class="sxs-lookup"><span data-stu-id="e8dec-132">There is no way to retrieve this password in the future.</span></span>

## <a name="example"></a><span data-ttu-id="e8dec-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8dec-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e8dec-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e8dec-134">Request</span></span>
<span data-ttu-id="e8dec-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e8dec-135">Here is an example of the request.</span></span>

```http
POST https://graph.microsoft.com/beta/applications/{id}/addPassword
```
##### <a name="response"></a><span data-ttu-id="e8dec-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8dec-136">Response</span></span>
<span data-ttu-id="e8dec-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e8dec-137">Here is an example of the response.</span></span>

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

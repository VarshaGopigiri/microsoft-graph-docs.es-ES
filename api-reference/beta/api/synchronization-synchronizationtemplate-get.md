---
title: Obtener synchronizationTemplate
description: Recuperar una plantilla de sincronización mediante su identificador.
localization_priority: Normal
ms.openlocfilehash: 9754b1fbc8c86f05d22f0ada57b8b97e0b1efbed
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27863815"
---
# <a name="get-synchronizationtemplate"></a><span data-ttu-id="b6a74-103">Obtener synchronizationTemplate</span><span class="sxs-lookup"><span data-stu-id="b6a74-103">Get synchronizationTemplate</span></span>

> <span data-ttu-id="b6a74-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b6a74-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b6a74-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b6a74-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b6a74-106">Recuperar una plantilla de sincronización mediante su identificador.</span><span class="sxs-lookup"><span data-stu-id="b6a74-106">Retrieve a synchronization template by its identifier.</span></span>

## <a name="permissions"></a><span data-ttu-id="b6a74-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b6a74-107">Permissions</span></span>
<span data-ttu-id="b6a74-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b6a74-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b6a74-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b6a74-110">Permission type</span></span>                        | <span data-ttu-id="b6a74-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b6a74-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="b6a74-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b6a74-112">Delegated (work or school account)</span></span>     |<span data-ttu-id="b6a74-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b6a74-113">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="b6a74-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b6a74-114">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="b6a74-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6a74-115">Not supported.</span></span>|
|<span data-ttu-id="b6a74-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b6a74-116">Application</span></span>                            |<span data-ttu-id="b6a74-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6a74-117">Not supported.</span></span>| 

### <a name="http-request"></a><span data-ttu-id="b6a74-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b6a74-118">HTTP Request</span></span>

```http
GET applications/{id}/synchronization/templates/{templateId}
GET servicePrincipals/{id}/synchronization/templates/{templateId}
```

## <a name="request-headers"></a><span data-ttu-id="b6a74-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b6a74-119">Request headers</span></span>

| <span data-ttu-id="b6a74-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="b6a74-120">Name</span></span>           | <span data-ttu-id="b6a74-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6a74-121">Type</span></span>    | <span data-ttu-id="b6a74-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6a74-122">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="b6a74-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="b6a74-123">Authorization</span></span>  | <span data-ttu-id="b6a74-124">string</span><span class="sxs-lookup"><span data-stu-id="b6a74-124">string</span></span>  | <span data-ttu-id="b6a74-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b6a74-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b6a74-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b6a74-127">Request body</span></span>

<span data-ttu-id="b6a74-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b6a74-128">Do not supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="b6a74-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6a74-129">Response</span></span>

<span data-ttu-id="b6a74-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6a74-130">If successful, this method returns a `200 OK` response code and a [synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) object in the response body.</span></span>

### <a name="example"></a><span data-ttu-id="b6a74-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6a74-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="b6a74-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b6a74-132">Request</span></span>
<span data-ttu-id="b6a74-133">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6a74-133">The following is an example of a request.</span></span>

```http
GET https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/templates/Slack
```

##### <a name="response"></a><span data-ttu-id="b6a74-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6a74-134">Response</span></span>
<span data-ttu-id="b6a74-135">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6a74-135">The following is an example of a response.</span></span>
><span data-ttu-id="b6a74-136">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="b6a74-136">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="b6a74-137">Se devolverán todas las propiedades en una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b6a74-137">All the properties will be returned in an actual call.</span></span>

```http
HTTP/1.1 200 OK
{
    "id": "Slack",
    "factoryTag": "CustomSCIM",
    "schema": {
        "directories": [],
        "synchronizationRules": []
        }
}
```

---
title: Obtener un miembro
description: Utilice esta API para obtener a un miembro específico (usuario o grupo) en una unidad administrativa.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: bbceccf30fdc3a9bd43fd25b8eda4cabdb4f7514
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932003"
---
# <a name="get-a-member"></a><span data-ttu-id="c3bcb-103">Obtener un miembro</span><span class="sxs-lookup"><span data-stu-id="c3bcb-103">Get a member</span></span>

> <span data-ttu-id="c3bcb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c3bcb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c3bcb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c3bcb-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c3bcb-106">Utilice esta API para obtener a un miembro específico (usuario o grupo) en una unidad administrativa.</span><span class="sxs-lookup"><span data-stu-id="c3bcb-106">Use this API to get a specific member (user or group) in an administrative unit.</span></span>

## <a name="permissions"></a><span data-ttu-id="c3bcb-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c3bcb-107">Permissions</span></span>
<span data-ttu-id="c3bcb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c3bcb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="c3bcb-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c3bcb-110">Permission type</span></span>      | <span data-ttu-id="c3bcb-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c3bcb-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c3bcb-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c3bcb-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c3bcb-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="c3bcb-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="c3bcb-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c3bcb-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c3bcb-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c3bcb-115">Not supported.</span></span>    |
|<span data-ttu-id="c3bcb-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c3bcb-116">Application</span></span> | <span data-ttu-id="c3bcb-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c3bcb-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c3bcb-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c3bcb-118">HTTP request</span></span>

```http
GET /administrativeUnits/{id}/members/{id}
```
## <a name="request-headers"></a><span data-ttu-id="c3bcb-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c3bcb-119">Request headers</span></span>
| <span data-ttu-id="c3bcb-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="c3bcb-120">Name</span></span>      |<span data-ttu-id="c3bcb-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3bcb-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="c3bcb-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c3bcb-122">Authorization</span></span>  | <span data-ttu-id="c3bcb-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c3bcb-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c3bcb-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c3bcb-125">Request body</span></span>
<span data-ttu-id="c3bcb-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c3bcb-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c3bcb-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c3bcb-127">Response</span></span>

<span data-ttu-id="c3bcb-128">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto de [usuario](../resources/user.md) o [grupo](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c3bcb-128">If successful, this method returns a `200 OK` response code and a [user](../resources/user.md) or [group](../resources/group.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c3bcb-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c3bcb-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c3bcb-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c3bcb-130">Request</span></span>
<span data-ttu-id="c3bcb-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c3bcb-131">Here is an example of the request.</span></span>

```http
GET https://graph.microsoft.com/beta/administrativeUnits/{id}/members/{id}
```

##### <a name="response"></a><span data-ttu-id="c3bcb-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c3bcb-132">Response</span></span>
<span data-ttu-id="c3bcb-133">Este es un ejemplo de los ataques.</span><span class="sxs-lookup"><span data-stu-id="c3bcb-133">Here is an example of the respone.</span></span> <span data-ttu-id="c3bcb-134">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="c3bcb-134">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="c3bcb-135">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c3bcb-135">All of the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 100

{
  "@odata.type":"#microsoft.graph.user",
  "id":"492c5308-59fd-4740-9c83-4b3db07a6d70"
  "accountEnabled":true,
  "businessPhones":[],
  "companyName":null,
  "displayName":"Demo User"
}
```

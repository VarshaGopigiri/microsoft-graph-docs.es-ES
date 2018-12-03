---
title: Obtener administrativeUnit
description: Recuperar el directorio simple **administrativeUnit** que corresponde a esta **educationSchool**.
ms.openlocfilehash: 49ac05b44bc89f827091c3b846885a58cb7b8956
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087334"
---
# <a name="get-administrativeunit"></a><span data-ttu-id="ca60b-103">Obtener administrativeUnit</span><span class="sxs-lookup"><span data-stu-id="ca60b-103">Get administrativeUnit</span></span>

> <span data-ttu-id="ca60b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ca60b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ca60b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ca60b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ca60b-106">Recuperar el directorio simple **administrativeUnit** que corresponde a esta **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="ca60b-106">Retrieve the simple directory **administrativeUnit** that corresponds to this **educationSchool**.</span></span>

><span data-ttu-id="ca60b-107">**Nota:** Si se usa el token delegado, los miembros solo pueden ver información sobre sus propios centros educativos.</span><span class="sxs-lookup"><span data-stu-id="ca60b-107">**Note:** If the delegated token is used, members can only see information about their own schools.</span></span> <span data-ttu-id="ca60b-108">Use el recurso `...beta/education/me/schools` en este caso.</span><span class="sxs-lookup"><span data-stu-id="ca60b-108">Use the `...beta/education/me/schools` resource in this case.</span></span>

## <a name="permissions"></a><span data-ttu-id="ca60b-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="ca60b-109">Permissions</span></span>
<span data-ttu-id="ca60b-110">Se requiere una combinación de permisos para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="ca60b-110">A combination of permissions is required to call this API.</span></span> <span data-ttu-id="ca60b-111">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ca60b-111">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ca60b-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ca60b-112">Permission type</span></span>      | <span data-ttu-id="ca60b-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ca60b-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ca60b-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ca60b-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="ca60b-115">Uno de los permisos EduRoster.ReadBasic, EduRoster.Read, EduRoster.Write y Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="ca60b-115">One from EduRoster.ReadBasic, EduRoster.Read, EduRoster.Write plus Directory.Read.All</span></span>|
|<span data-ttu-id="ca60b-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ca60b-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="ca60b-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ca60b-117">Not supported.</span></span>  |
|<span data-ttu-id="ca60b-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ca60b-118">Application</span></span> | <span data-ttu-id="ca60b-119">EduRoster.Read.All, EduRoster.ReadWrite.All y Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="ca60b-119">EduRoster.Read.All, EduRoster.ReadWrite.All plus Directory.Read.All</span></span>| 

## <a name="http-request"></a><span data-ttu-id="ca60b-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ca60b-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/schools/{id}/administrativeUnit
```
## <a name="request-headers"></a><span data-ttu-id="ca60b-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ca60b-121">Request headers</span></span>
| <span data-ttu-id="ca60b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca60b-122">Header</span></span>       | <span data-ttu-id="ca60b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ca60b-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ca60b-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="ca60b-124">Authorization</span></span>  | <span data-ttu-id="ca60b-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ca60b-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ca60b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ca60b-127">Request body</span></span>
<span data-ttu-id="ca60b-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ca60b-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="ca60b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ca60b-129">Response</span></span>
<span data-ttu-id="ca60b-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [administrativeUnit](../resources/administrativeunit.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ca60b-130">If successful, this method returns a `200 OK` response code and an [administrativeUnit](../resources/administrativeunit.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ca60b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ca60b-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ca60b-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ca60b-132">Request</span></span>
<span data-ttu-id="ca60b-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ca60b-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_administrativeUnit"
}-->
```http
GET https://graph.microsoft.com/beta/education/schools/2961761D-8094-4183-A9F6-8E36E966C7D9/administrativeUnit
```
##### <a name="response"></a><span data-ttu-id="ca60b-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ca60b-134">Response</span></span>
<span data-ttu-id="ca60b-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ca60b-135">The following is an example of the response.</span></span> 

><span data-ttu-id="ca60b-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ca60b-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user",
  "isCollection": false
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 134

{
  "displayName": "displayName-value",
  "description": "description-value",
  "visibility": "visibility-value",
  "id": "id-value"
}
```

<!-- uuid: A681726F-B4A7-4BCF-9407-F87CB9A4771D
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get user",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
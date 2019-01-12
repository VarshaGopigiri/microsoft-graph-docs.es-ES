---
title: Obtener usuario
description: Recupere el directorio simple **user** correspondiente a este objeto **educationUser**.
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: 063b1297c2243f11b6eb1020703b7332390a4aa2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991927"
---
# <a name="get-user"></a><span data-ttu-id="16140-103">Obtener usuario</span><span class="sxs-lookup"><span data-stu-id="16140-103">Get user</span></span>

<span data-ttu-id="16140-104">Recupere el directorio simple **user** correspondiente a este objeto **educationUser**.</span><span class="sxs-lookup"><span data-stu-id="16140-104">Retrieve the simple directory **user** that corresponds to this **educationUser**.</span></span>

><span data-ttu-id="16140-105">**Nota:** Si se usa el token delegado, los miembros solo pueden ver información sobre sus propios centros educativos.</span><span class="sxs-lookup"><span data-stu-id="16140-105">**Note:** If the delegated token is used, members can only see information about their own schools.</span></span> <span data-ttu-id="16140-106">Use el recurso `...beta/education/me/schools` en este caso.</span><span class="sxs-lookup"><span data-stu-id="16140-106">Use the `...beta/education/me/schools` resource in this case.</span></span>

## <a name="permissions"></a><span data-ttu-id="16140-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="16140-107">Permissions</span></span>
<span data-ttu-id="16140-108">Se requiere una combinación de permisos para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="16140-108">A combination of permissions is required to call this API.</span></span> <span data-ttu-id="16140-109">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="16140-109">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="16140-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="16140-110">Permission type</span></span>      | <span data-ttu-id="16140-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="16140-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="16140-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="16140-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="16140-113">Uno de los permisos EduRoster.ReadBasic, EduRoster.Read, EduRoster.Write y Directory.Read.All o User.Read</span><span class="sxs-lookup"><span data-stu-id="16140-113">One from EduRoster.ReadBasic, EduRoster.Read, EduRoster.Write plus either Directory.Read.All or User.Read</span></span>|
|<span data-ttu-id="16140-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="16140-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="16140-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="16140-115">Not supported.</span></span>  |
|<span data-ttu-id="16140-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="16140-116">Application</span></span> | <span data-ttu-id="16140-117">EduRoster.Read.All, EduRoster.ReadWrite.All y Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="16140-117">EduRoster.Read.All, EduRoster.ReadWrite.All plus Directory.Read.All</span></span>| 

## <a name="http-request"></a><span data-ttu-id="16140-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="16140-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/me/user
GET /education/users/{id}/user
```
## <a name="request-headers"></a><span data-ttu-id="16140-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="16140-119">Request headers</span></span>
| <span data-ttu-id="16140-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16140-120">Header</span></span>       | <span data-ttu-id="16140-121">Valor</span><span class="sxs-lookup"><span data-stu-id="16140-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="16140-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="16140-122">Authorization</span></span>  | <span data-ttu-id="16140-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="16140-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="16140-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="16140-125">Request body</span></span>
<span data-ttu-id="16140-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="16140-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="16140-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16140-127">Response</span></span>
<span data-ttu-id="16140-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="16140-128">If successful, this method returns a `200 OK` response code and a [user](../resources/user.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="16140-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="16140-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="16140-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="16140-130">Request</span></span>
<span data-ttu-id="16140-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="16140-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_user"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/me/user
```
##### <a name="response"></a><span data-ttu-id="16140-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16140-132">Response</span></span>
<span data-ttu-id="16140-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="16140-133">The following is an example of the response.</span></span> 

><span data-ttu-id="16140-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="16140-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user",
  "isCollection": false
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 491

{
  "businessPhones": [
       "businessPhones-value"
   ],
   "displayName": "displayName-value",
   "givenName": "givenName-value",
   "jobTitle": "jobTitle-value",
   "mail": "mail-value",
   "mobilePhone": "mobilePhone-value",
   "officeLocation": "officeLocation-value",
   "preferredLanguage": "preferredLanguage-value",
   "surname": "surname-value",
   "userPrincipalName": "userPrincipalName-value",
   "id": "id-value"
}
```

<!-- uuid: FC4AAF57-A0ED-4899-B104-A8B89B72AD5A
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get user",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

---
title: Obtener usuario
description: Recupere el directorio simple **user** correspondiente a este objeto **educationUser**.
ms.openlocfilehash: e87fa333ab6a50be3f5222888693b0783dd9b22a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028772"
---
# <a name="get-user"></a><span data-ttu-id="25c47-103">Obtener usuario</span><span class="sxs-lookup"><span data-stu-id="25c47-103">Get user</span></span>

<span data-ttu-id="25c47-104">Recupere el directorio simple **user** correspondiente a este objeto **educationUser**.</span><span class="sxs-lookup"><span data-stu-id="25c47-104">Retrieve the simple directory **user** that corresponds to this **educationUser**.</span></span>

><span data-ttu-id="25c47-105">**Nota:** Si se usa el token delegado, los miembros solo pueden ver información sobre sus propios centros educativos.</span><span class="sxs-lookup"><span data-stu-id="25c47-105">**Note:** If the delegated token is used, members can only see information about their own schools.</span></span> <span data-ttu-id="25c47-106">Use el recurso `...beta/education/me/schools` en este caso.</span><span class="sxs-lookup"><span data-stu-id="25c47-106">Use the `...beta/education/me/schools` resource in this case.</span></span>

## <a name="permissions"></a><span data-ttu-id="25c47-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="25c47-107">Permissions</span></span>
<span data-ttu-id="25c47-108">Se requiere una combinación de permisos para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="25c47-108">A combination of permissions is required to call this API.</span></span> <span data-ttu-id="25c47-109">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="25c47-109">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="25c47-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="25c47-110">Permission type</span></span>      | <span data-ttu-id="25c47-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="25c47-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="25c47-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="25c47-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="25c47-113">Uno de los permisos EduRoster.ReadBasic, EduRoster.Read, EduRoster.Write y Directory.Read.All o User.Read</span><span class="sxs-lookup"><span data-stu-id="25c47-113">One from EduRoster.ReadBasic, EduRoster.Read, EduRoster.Write plus either Directory.Read.All or User.Read</span></span>|
|<span data-ttu-id="25c47-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="25c47-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="25c47-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="25c47-115">Not supported.</span></span>  |
|<span data-ttu-id="25c47-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="25c47-116">Application</span></span> | <span data-ttu-id="25c47-117">EduRoster.Read.All, EduRoster.ReadWrite.All y Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="25c47-117">EduRoster.Read.All, EduRoster.ReadWrite.All plus Directory.Read.All</span></span>| 

## <a name="http-request"></a><span data-ttu-id="25c47-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="25c47-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/me/user
GET /education/users/{id}/user
```
## <a name="request-headers"></a><span data-ttu-id="25c47-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="25c47-119">Request headers</span></span>
| <span data-ttu-id="25c47-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25c47-120">Header</span></span>       | <span data-ttu-id="25c47-121">Valor</span><span class="sxs-lookup"><span data-stu-id="25c47-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="25c47-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="25c47-122">Authorization</span></span>  | <span data-ttu-id="25c47-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="25c47-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="25c47-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="25c47-125">Request body</span></span>
<span data-ttu-id="25c47-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="25c47-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="25c47-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25c47-127">Response</span></span>
<span data-ttu-id="25c47-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="25c47-128">If successful, this method returns a `200 OK` response code and a [user](../resources/user.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="25c47-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="25c47-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="25c47-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="25c47-130">Request</span></span>
<span data-ttu-id="25c47-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="25c47-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_user"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/me/user
```
##### <a name="response"></a><span data-ttu-id="25c47-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25c47-132">Response</span></span>
<span data-ttu-id="25c47-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="25c47-133">The following is an example of the response.</span></span> 

><span data-ttu-id="25c47-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="25c47-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
---
title: Obtener usuario
description: Recupere el directorio simple **user** correspondiente a este objeto **educationUser**.
localization_priority: Normal
ms.openlocfilehash: 428d564231e3922c074d5dd783592e6a9560dc43
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27892251"
---
# <a name="get-user"></a><span data-ttu-id="7535f-103">Obtener usuario</span><span class="sxs-lookup"><span data-stu-id="7535f-103">Get user</span></span>

> <span data-ttu-id="7535f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7535f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7535f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7535f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7535f-106">Recupere el directorio simple **user** correspondiente a este objeto **educationUser**.</span><span class="sxs-lookup"><span data-stu-id="7535f-106">Retrieve the simple directory **user** that corresponds to this **educationUser**.</span></span>

><span data-ttu-id="7535f-107">**Nota:** Si se usa el token delegado, los miembros solo pueden ver información sobre sus propios centros educativos.</span><span class="sxs-lookup"><span data-stu-id="7535f-107">**Note:** If the delegated token is used, members can only see information about their own schools.</span></span> <span data-ttu-id="7535f-108">Use el recurso `...beta/education/me/schools` en este caso.</span><span class="sxs-lookup"><span data-stu-id="7535f-108">Use the `...beta/education/me/schools` resource in this case.</span></span>

## <a name="permissions"></a><span data-ttu-id="7535f-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="7535f-109">Permissions</span></span>
<span data-ttu-id="7535f-110">Se requiere una combinación de permisos para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="7535f-110">A combination of permissions is required to call this API.</span></span> <span data-ttu-id="7535f-111">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7535f-111">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7535f-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7535f-112">Permission type</span></span>      | <span data-ttu-id="7535f-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7535f-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7535f-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7535f-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="7535f-115">Uno de los permisos EduRoster.ReadBasic, EduRoster.Read, EduRoster.Write y Directory.Read.All o User.Read</span><span class="sxs-lookup"><span data-stu-id="7535f-115">One from EduRoster.ReadBasic, EduRoster.Read, EduRoster.Write plus either Directory.Read.All or User.Read</span></span>|
|<span data-ttu-id="7535f-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7535f-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="7535f-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7535f-117">Not supported.</span></span>  |
|<span data-ttu-id="7535f-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7535f-118">Application</span></span> | <span data-ttu-id="7535f-119">EduRoster.Read.All, EduRoster.ReadWrite.All y Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="7535f-119">EduRoster.Read.All, EduRoster.ReadWrite.All plus Directory.Read.All</span></span>| 

## <a name="http-request"></a><span data-ttu-id="7535f-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7535f-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/me/user
GET /education/users/{id}/user
```
## <a name="request-headers"></a><span data-ttu-id="7535f-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7535f-121">Request headers</span></span>
| <span data-ttu-id="7535f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7535f-122">Header</span></span>       | <span data-ttu-id="7535f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7535f-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="7535f-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="7535f-124">Authorization</span></span>  | <span data-ttu-id="7535f-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7535f-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="7535f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7535f-127">Request body</span></span>
<span data-ttu-id="7535f-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7535f-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="7535f-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7535f-129">Response</span></span>
<span data-ttu-id="7535f-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7535f-130">If successful, this method returns a `200 OK` response code and a [user](../resources/user.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7535f-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7535f-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7535f-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7535f-132">Request</span></span>
<span data-ttu-id="7535f-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7535f-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_user"
}-->
```http
GET https://graph.microsoft.com/beta/education/me/user
```
##### <a name="response"></a><span data-ttu-id="7535f-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7535f-134">Response</span></span>
<span data-ttu-id="7535f-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7535f-135">The following is an example of the response.</span></span> 

><span data-ttu-id="7535f-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7535f-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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

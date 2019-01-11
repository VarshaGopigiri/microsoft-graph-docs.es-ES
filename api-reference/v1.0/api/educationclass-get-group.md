---
title: Obtener grupo
description: Recupere el **group** de Office 365 correspondiente a este objeto **educationClass**.
localization_priority: Normal
ms.openlocfilehash: da7e179802739f39465cfb462c92c527ecac3d7c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825350"
---
# <a name="get-group"></a><span data-ttu-id="681f7-103">Obtener grupo</span><span class="sxs-lookup"><span data-stu-id="681f7-103">Get group</span></span>

<span data-ttu-id="681f7-104">Recupere el **group** de Office 365 correspondiente a este objeto **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="681f7-104">Retrieve the Office 365 **group** that corresponds to this **educationClass**.</span></span>

><span data-ttu-id="681f7-105">**Nota:** Si se usa el token delegado, los miembros solo pueden ver información sobre sus propios centros educativos.</span><span class="sxs-lookup"><span data-stu-id="681f7-105">**Note:** If the delegated token is used, members can only see information about their own schools.</span></span> <span data-ttu-id="681f7-106">Use el recurso `...beta/education/me/schools` en este caso.</span><span class="sxs-lookup"><span data-stu-id="681f7-106">Use the `...beta/education/me/schools` resource in this case.</span></span>

## <a name="permissions"></a><span data-ttu-id="681f7-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="681f7-107">Permissions</span></span>
<span data-ttu-id="681f7-108">Se requiere una combinación de permisos para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="681f7-108">A combination of permissions is required to call this API.</span></span> <span data-ttu-id="681f7-109">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="681f7-109">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="681f7-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="681f7-110">Permission type</span></span>      | <span data-ttu-id="681f7-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="681f7-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="681f7-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="681f7-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="681f7-113">Uno de los permisos EduRoster.ReadBasic, EduRoster.Read, EduRoster.Write y Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="681f7-113">One from EduRoster.ReadBasic, EduRoster.Read, EduRoster.Write plus Directory.Read.All</span></span>|
|<span data-ttu-id="681f7-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="681f7-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="681f7-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="681f7-115">Not supported.</span></span>  |
|<span data-ttu-id="681f7-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="681f7-116">Application</span></span> | <span data-ttu-id="681f7-117">EduRoster.Read.All, EduRoster.ReadWrite.All y Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="681f7-117">EduRoster.Read.All, EduRoster.ReadWrite.All plus Directory.Read.All</span></span>| 

## <a name="http-request"></a><span data-ttu-id="681f7-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="681f7-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/group
```
## <a name="request-headers"></a><span data-ttu-id="681f7-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="681f7-119">Request headers</span></span>
| <span data-ttu-id="681f7-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="681f7-120">Header</span></span>       | <span data-ttu-id="681f7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="681f7-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="681f7-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="681f7-122">Authorization</span></span>  | <span data-ttu-id="681f7-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="681f7-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="681f7-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="681f7-125">Request body</span></span>
<span data-ttu-id="681f7-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="681f7-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="681f7-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="681f7-127">Response</span></span>
<span data-ttu-id="681f7-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="681f7-128">If successful, this method returns a `200 OK` response code and a [group](../resources/group.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="681f7-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="681f7-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="681f7-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="681f7-130">Request</span></span>
<span data-ttu-id="681f7-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="681f7-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_group"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/classes/{class-id}/group
```
##### <a name="response"></a><span data-ttu-id="681f7-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="681f7-132">Response</span></span>
<span data-ttu-id="681f7-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="681f7-133">The following is an example of the response.</span></span> 

><span data-ttu-id="681f7-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="681f7-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user",
  "isCollection": false
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: xxx

{
  "id": "id-value",
  "description": "description-value",
  "displayName": "displayName-value",
  "groupTypes": [
    "groupTypes-value"
  ],
  "mail": "mail-value",
  "mailEnabled": true,
  "mailNickname": "mailNickname-value",
  "onPremisesLastSyncDateTime": "onPremisesLastSyncDateTime-value",
  "onPremisesSecurityIdentifier": "onPremisesSecurityIdentifier-value",
  "onPremisesSyncEnabled": true,
  "proxyAddresses": [
    "proxyAddresses-value"
   ],
   "securityEnabled": true,
   "visibility": "visibility-value"
}
```

<!-- uuid: 0087D9B3-1418-4C87-91C9-A18C6D93706B
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get user",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

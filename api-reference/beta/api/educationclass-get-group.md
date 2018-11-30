---
title: Obtener grupo
description: Recupere el **group** de Office 365 correspondiente a este objeto **educationClass**.
ms.openlocfilehash: 9a91f430f82ed4b5804958fa1045b76d5eff3c6f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085597"
---
# <a name="get-group"></a><span data-ttu-id="bbb85-103">Obtener grupo</span><span class="sxs-lookup"><span data-stu-id="bbb85-103">Get group</span></span>

> <span data-ttu-id="bbb85-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bbb85-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bbb85-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bbb85-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bbb85-106">Recupere el **group** de Office 365 correspondiente a este objeto **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="bbb85-106">Retrieve the Office 365 **group** that corresponds to this **educationClass**.</span></span>

><span data-ttu-id="bbb85-107">**Nota:** Si se usa el token delegado, los miembros solo pueden ver información sobre sus propios centros educativos.</span><span class="sxs-lookup"><span data-stu-id="bbb85-107">**Note:** If the delegated token is used, members can only see information about their own schools.</span></span> <span data-ttu-id="bbb85-108">Use el recurso `...beta/education/me/schools` en este caso.</span><span class="sxs-lookup"><span data-stu-id="bbb85-108">Use the `...beta/education/me/schools` resource in this case.</span></span>

## <a name="permissions"></a><span data-ttu-id="bbb85-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="bbb85-109">Permissions</span></span>
<span data-ttu-id="bbb85-110">Se requiere una combinación de permisos para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="bbb85-110">A combination of permissions is required to call this API.</span></span> <span data-ttu-id="bbb85-111">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bbb85-111">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bbb85-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bbb85-112">Permission type</span></span>      | <span data-ttu-id="bbb85-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bbb85-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bbb85-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bbb85-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="bbb85-115">Uno de los permisos EduRoster.ReadBasic, EduRoster.Read, EduRoster.Write y Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="bbb85-115">One from EduRoster.ReadBasic, EduRoster.Read, EduRoster.Write plus Directory.Read.All</span></span>|
|<span data-ttu-id="bbb85-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bbb85-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="bbb85-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bbb85-117">Not supported.</span></span>  |
|<span data-ttu-id="bbb85-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bbb85-118">Application</span></span> | <span data-ttu-id="bbb85-119">EduRoster.Read.All, EduRoster.ReadWrite.All y Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="bbb85-119">EduRoster.Read.All, EduRoster.ReadWrite.All plus Directory.Read.All</span></span>| 

## <a name="http-request"></a><span data-ttu-id="bbb85-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bbb85-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/group
```
## <a name="request-headers"></a><span data-ttu-id="bbb85-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bbb85-121">Request headers</span></span>
| <span data-ttu-id="bbb85-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bbb85-122">Header</span></span>       | <span data-ttu-id="bbb85-123">Valor</span><span class="sxs-lookup"><span data-stu-id="bbb85-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="bbb85-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="bbb85-124">Authorization</span></span>  | <span data-ttu-id="bbb85-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bbb85-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="bbb85-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bbb85-127">Request body</span></span>
<span data-ttu-id="bbb85-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bbb85-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="bbb85-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bbb85-129">Response</span></span>
<span data-ttu-id="bbb85-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bbb85-130">If successful, this method returns a `200 OK` response code and a [group](../resources/group.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bbb85-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bbb85-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bbb85-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bbb85-132">Request</span></span>
<span data-ttu-id="bbb85-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bbb85-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_group"
}-->
```http
GET https://graph.microsoft.com/beta/education/classes/2961761D-8094-4183-A9F6-8E36E966C7D9/group
```
##### <a name="response"></a><span data-ttu-id="bbb85-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bbb85-134">Response</span></span>
<span data-ttu-id="bbb85-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bbb85-135">The following is an example of the response.</span></span> 

><span data-ttu-id="bbb85-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bbb85-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
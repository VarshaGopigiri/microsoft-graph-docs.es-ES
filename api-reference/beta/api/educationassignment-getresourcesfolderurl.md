---
title: 'educationAssignment: getResourcesFolderUrl'
description: 'Esta función devuelve la dirección URL de OneDrive donde se deben cargar todos los recursos basados en archivos (Word, Excel y así sucesivamente).  '
localization_priority: Normal
ms.openlocfilehash: 4352fb051573f91ef93e781a1a06ba984b17a9ed
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887391"
---
# <a name="educationassignment-getresourcesfolderurl"></a><span data-ttu-id="5d7a3-103">educationAssignment: getResourcesFolderUrl</span><span class="sxs-lookup"><span data-stu-id="5d7a3-103">educationAssignment: getResourcesFolderUrl</span></span>

> <span data-ttu-id="5d7a3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5d7a3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5d7a3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5d7a3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5d7a3-106">Esta función devuelve la dirección URL de OneDrive donde se deben cargar todos los recursos basados en archivos (Word, Excel y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="5d7a3-106">This function returns the OneDrive URL where all file-based resources (Word, Excel, and so on) should be uploaded.</span></span>  
<span data-ttu-id="5d7a3-107">Tenga en cuenta que los archivos deben estar ubicados en esta carpeta con el fin de agregarse como recursos.</span><span class="sxs-lookup"><span data-stu-id="5d7a3-107">Note that files must be located in this folder in order to be added as resources.</span></span> <span data-ttu-id="5d7a3-108">Sólo un profesor en la clase puede determinar qué archivos para cargar.</span><span class="sxs-lookup"><span data-stu-id="5d7a3-108">Only a teacher in the class can determine what files to upload.</span></span> 

## <a name="permissions"></a><span data-ttu-id="5d7a3-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="5d7a3-109">Permissions</span></span>
<span data-ttu-id="5d7a3-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5d7a3-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5d7a3-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5d7a3-112">Permission type</span></span>      | <span data-ttu-id="5d7a3-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5d7a3-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5d7a3-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5d7a3-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="5d7a3-115">EduAssignments.ReadBasic, EduAssignments.Read</span><span class="sxs-lookup"><span data-stu-id="5d7a3-115">EduAssignments.ReadBasic, EduAssignments.Read</span></span>  |
|<span data-ttu-id="5d7a3-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5d7a3-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="5d7a3-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5d7a3-117">Not supported.</span></span>  |
|<span data-ttu-id="5d7a3-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5d7a3-118">Application</span></span> | <span data-ttu-id="5d7a3-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5d7a3-119">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="5d7a3-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5d7a3-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/assignments/{id}/getResourcesFolderUrl

```
## <a name="request-headers"></a><span data-ttu-id="5d7a3-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5d7a3-121">Request headers</span></span>
| <span data-ttu-id="5d7a3-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d7a3-122">Header</span></span>       | <span data-ttu-id="5d7a3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5d7a3-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="5d7a3-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="5d7a3-124">Authorization</span></span>  | <span data-ttu-id="5d7a3-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5d7a3-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="5d7a3-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5d7a3-127">Request body</span></span>
<span data-ttu-id="5d7a3-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5d7a3-128">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="5d7a3-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d7a3-129">Response</span></span>
<span data-ttu-id="5d7a3-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 Ok`.</span><span class="sxs-lookup"><span data-stu-id="5d7a3-130">If successful, this method returns a `200 Ok` response code.</span></span> <span data-ttu-id="5d7a3-131">El cuerpo contiene la dirección URL de OneDrive de una carpeta en la que se va a colocar todos los recursos basados en el archivo.</span><span class="sxs-lookup"><span data-stu-id="5d7a3-131">The body will contain the OneDrive URL of a folder in which to put all file-based resources.</span></span>

## <a name="example"></a><span data-ttu-id="5d7a3-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5d7a3-132">Example</span></span>
<span data-ttu-id="5d7a3-133">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="5d7a3-133">The following example shows how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="5d7a3-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5d7a3-134">Request</span></span>
<span data-ttu-id="5d7a3-135">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="5d7a3-135">The following is an example of a request.</span></span>
<!-- {
  "blockType": "request",
  "name": "educationassignment_publish"
}-->
```http
POST https://graph.microsoft.com/beta/education/classes/11012/assignments/19002/getResourcesFolderUrl
```

##### <a name="response"></a><span data-ttu-id="5d7a3-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d7a3-136">Response</span></span>
<span data-ttu-id="5d7a3-137">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="5d7a3-137">The following is an example of a response.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationAssignment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 279

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Edm.String",
    "value": "https://graph.microsoft.com/v1.0/drives/b!8-QjN2tsv0WyGnTv7vOvnQkmGHbbeMNLqYKONmHLVnvCVmBYIGpeT456457AdW9f/items/017NJZI25NOB5XZNLABF7646XAMDZTQQ6T"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationAssignment: publish",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

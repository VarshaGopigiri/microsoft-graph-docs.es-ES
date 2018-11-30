---
title: tipo de recurso signInStatus
description: Proporciona el inicio de sesión de estado (correcto o error) de inicio de sesión de
ms.openlocfilehash: cafa0dffe1b1d798d87225ac82901cf041d5e4fa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089989"
---
# <a name="signinstatus-resource-type"></a><span data-ttu-id="85dc8-103">tipo de recurso signInStatus</span><span class="sxs-lookup"><span data-stu-id="85dc8-103">signInStatus resource type</span></span>
<span data-ttu-id="85dc8-104">Proporciona el inicio de sesión de estado (correcto o error) de inicio de sesión de</span><span class="sxs-lookup"><span data-stu-id="85dc8-104">Provides the sign-in status (Success or Failure) of the sign-in</span></span>



## <a name="properties"></a><span data-ttu-id="85dc8-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="85dc8-105">Properties</span></span>
| <span data-ttu-id="85dc8-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="85dc8-106">Property</span></span>     | <span data-ttu-id="85dc8-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="85dc8-107">Type</span></span>   |<span data-ttu-id="85dc8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="85dc8-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="85dc8-109">additionalDetails</span><span class="sxs-lookup"><span data-stu-id="85dc8-109">additionalDetails</span></span>|<span data-ttu-id="85dc8-110">String</span><span class="sxs-lookup"><span data-stu-id="85dc8-110">String</span></span>|<span data-ttu-id="85dc8-111">Proporciona detalles adicionales acerca de la actividad de inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="85dc8-111">Provides additional details on the sign-in activity</span></span>|
|<span data-ttu-id="85dc8-112">errorCode</span><span class="sxs-lookup"><span data-stu-id="85dc8-112">errorCode</span></span>|<span data-ttu-id="85dc8-113">Int32</span><span class="sxs-lookup"><span data-stu-id="85dc8-113">Int32</span></span>|<span data-ttu-id="85dc8-114">Proporciona el código de error 5-6digit que se genera durante un error de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="85dc8-114">Provides the 5-6digit error code that's generated during a sign-in failure.</span></span> <span data-ttu-id="85dc8-115">Revise la [lista de códigos de error y los mensajes](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-activity-sign-ins-errors).</span><span class="sxs-lookup"><span data-stu-id="85dc8-115">Check out the [list of error codes and messages](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-activity-sign-ins-errors).</span></span>|
|<span data-ttu-id="85dc8-116">failureReason</span><span class="sxs-lookup"><span data-stu-id="85dc8-116">failureReason</span></span>|<span data-ttu-id="85dc8-117">String</span><span class="sxs-lookup"><span data-stu-id="85dc8-117">String</span></span>|<span data-ttu-id="85dc8-118">Proporciona el mensaje de error o el motivo del error para la actividad de inicio de sesión correspondiente.</span><span class="sxs-lookup"><span data-stu-id="85dc8-118">Provides the error message or the reason for failure for the corresponding sign-in activity.</span></span> <span data-ttu-id="85dc8-119">Revise la [lista de códigos de error y los mensajes](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-activity-sign-ins-errors).</span><span class="sxs-lookup"><span data-stu-id="85dc8-119">Check out the [list of error codes and messages](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-activity-sign-ins-errors).</span></span>|

## <a name="json-representation"></a><span data-ttu-id="85dc8-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="85dc8-120">JSON representation</span></span>

<span data-ttu-id="85dc8-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="85dc8-121">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.signInStatus"
}-->

```json
{
  "additionalDetails": "String",
  "errorCode": 1024,
  "failureReason": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "signInStatus resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
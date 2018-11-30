---
title: tipo de recurso deviceDetail
description: Indica los detalles del dispositivo asociados con un dispositivo utilizado para iniciar sesión. Incluye información como el explorador del dispositivo y la información del sistema operativo, si el dispositivo es Azure AD administrado.
ms.openlocfilehash: d7c1830ee5c99fc139a937fcee3896e2a9926592
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084141"
---
# <a name="devicedetail-resource-type"></a><span data-ttu-id="fa29d-104">tipo de recurso deviceDetail</span><span class="sxs-lookup"><span data-stu-id="fa29d-104">deviceDetail resource type</span></span>
<span data-ttu-id="fa29d-105">Indica los detalles del dispositivo asociados con un dispositivo utilizado para iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="fa29d-105">Indicates device details associated with a device used for signing in.</span></span> <span data-ttu-id="fa29d-106">Incluye información como el explorador del dispositivo y la información del sistema operativo, si el dispositivo es Azure AD administrado.</span><span class="sxs-lookup"><span data-stu-id="fa29d-106">Includes information like device browser and  OS info, if device is Azure AD managed.</span></span>



## <a name="properties"></a><span data-ttu-id="fa29d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fa29d-107">Properties</span></span>
| <span data-ttu-id="fa29d-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fa29d-108">Property</span></span>     | <span data-ttu-id="fa29d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="fa29d-109">Type</span></span>   |<span data-ttu-id="fa29d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa29d-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fa29d-111">Explorador</span><span class="sxs-lookup"><span data-stu-id="fa29d-111">browser</span></span>|<span data-ttu-id="fa29d-112">String</span><span class="sxs-lookup"><span data-stu-id="fa29d-112">String</span></span>|<span data-ttu-id="fa29d-113">Indica la información del explorador del que se usa para iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="fa29d-113">Indicates the browser information of the used for signing-in.</span></span>|
|<span data-ttu-id="fa29d-114">deviceId</span><span class="sxs-lookup"><span data-stu-id="fa29d-114">deviceId</span></span>|<span data-ttu-id="fa29d-115">String</span><span class="sxs-lookup"><span data-stu-id="fa29d-115">String</span></span>|<span data-ttu-id="fa29d-116">Hace referencia a la UniqueID del dispositivo usado para iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="fa29d-116">Refers to the UniqueID of the device used for signing-in.</span></span>|
|<span data-ttu-id="fa29d-117">displayName</span><span class="sxs-lookup"><span data-stu-id="fa29d-117">displayName</span></span>|<span data-ttu-id="fa29d-118">String</span><span class="sxs-lookup"><span data-stu-id="fa29d-118">String</span></span>|<span data-ttu-id="fa29d-119">Hace referencia al nombre del dispositivo usado para iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="fa29d-119">Refers to the name of the device used for signing-in.</span></span>|
|<span data-ttu-id="fa29d-120">isCompliant</span><span class="sxs-lookup"><span data-stu-id="fa29d-120">isCompliant</span></span>|<span data-ttu-id="fa29d-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="fa29d-121">Boolean</span></span>|<span data-ttu-id="fa29d-122">Indica si el dispositivo es compatible con o no.</span><span class="sxs-lookup"><span data-stu-id="fa29d-122">Indicates whether the device is compliant or not.</span></span>|
|<span data-ttu-id="fa29d-123">isManaged</span><span class="sxs-lookup"><span data-stu-id="fa29d-123">isManaged</span></span>|<span data-ttu-id="fa29d-124">Boolean</span><span class="sxs-lookup"><span data-stu-id="fa29d-124">Boolean</span></span>|<span data-ttu-id="fa29d-125">Indica si el dispositivo se administra o no.</span><span class="sxs-lookup"><span data-stu-id="fa29d-125">Indicates if the device is managed or not.</span></span>|
|<span data-ttu-id="fa29d-126">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="fa29d-126">operatingSystem</span></span>|<span data-ttu-id="fa29d-127">String</span><span class="sxs-lookup"><span data-stu-id="fa29d-127">String</span></span>|<span data-ttu-id="fa29d-128">Indica el nombre del sistema operativo y versión que usa para iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="fa29d-128">Indicates the OS name and version used for signing-in.</span></span>|
|<span data-ttu-id="fa29d-129">trustType</span><span class="sxs-lookup"><span data-stu-id="fa29d-129">trustType</span></span>|<span data-ttu-id="fa29d-130">String</span><span class="sxs-lookup"><span data-stu-id="fa29d-130">String</span></span>|<span data-ttu-id="fa29d-131">Indica información de si el dispositivo que ha iniciado sesión está unido a dominio de área de trabajo se unió a, se unió a AzureAD.</span><span class="sxs-lookup"><span data-stu-id="fa29d-131">Indicates information on whether the signed-in device is Workplace Joined, AzureAD Joined, Domain Joined.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="fa29d-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fa29d-132">JSON representation</span></span>

<span data-ttu-id="fa29d-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fa29d-133">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.deviceDetail"
}-->

```json
{
  "browser": "String",
  "deviceId": "String",
  "displayName": "String",
  "isCompliant": true,
  "isManaged": true,
  "operatingSystem": "String",
  "trustType": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "deviceDetail resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
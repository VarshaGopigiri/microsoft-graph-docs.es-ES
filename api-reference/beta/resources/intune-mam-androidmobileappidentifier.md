---
title: Tipo de recurso androidMobileAppIdentifier
description: El identificador de una aplicación móvil de Android.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 26c258dbf0091b44d2f7eea8fdf4066a5c8e6729
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27969775"
---
# <a name="androidmobileappidentifier-resource-type"></a><span data-ttu-id="3a9b4-103">Tipo de recurso androidMobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="3a9b4-103">androidMobileAppIdentifier resource type</span></span>

> <span data-ttu-id="3a9b4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3a9b4-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3a9b4-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3a9b4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3a9b4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3a9b4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3a9b4-107">El identificador de una aplicación móvil de Android.</span><span class="sxs-lookup"><span data-stu-id="3a9b4-107">The identifier for an Android app.</span></span>

<span data-ttu-id="3a9b4-108">Hereda de [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span><span class="sxs-lookup"><span data-stu-id="3a9b4-108">Inherits from [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span></span>

## <a name="properties"></a><span data-ttu-id="3a9b4-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3a9b4-109">Properties</span></span>
|<span data-ttu-id="3a9b4-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3a9b4-110">Property</span></span>|<span data-ttu-id="3a9b4-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a9b4-111">Type</span></span>|<span data-ttu-id="3a9b4-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a9b4-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3a9b4-113">packageId</span><span class="sxs-lookup"><span data-stu-id="3a9b4-113">packageId</span></span>|<span data-ttu-id="3a9b4-114">cadena</span><span class="sxs-lookup"><span data-stu-id="3a9b4-114">String</span></span>|<span data-ttu-id="3a9b4-115">El identificador de una aplicación, como se especifica en la Play Store.</span><span class="sxs-lookup"><span data-stu-id="3a9b4-115">The identifier for an app, as specified in the play store.</span></span>|

## <a name="relationships"></a><span data-ttu-id="3a9b4-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3a9b4-116">Relationships</span></span>
<span data-ttu-id="3a9b4-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3a9b4-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="3a9b4-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3a9b4-118">JSON Representation</span></span>
<span data-ttu-id="3a9b4-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3a9b4-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.androidMobileAppIdentifier"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidMobileAppIdentifier",
  "packageId": "String"
}
```






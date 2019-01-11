---
title: tipo de recurso iosBookmark
description: marcador de la dirección URL de iOS
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 37cdcc1b886914b4b42e0a97e8947a565c75f5b9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27841002"
---
# <a name="iosbookmark-resource-type"></a><span data-ttu-id="afd63-103">tipo de recurso iosBookmark</span><span class="sxs-lookup"><span data-stu-id="afd63-103">iosBookmark resource type</span></span>

> <span data-ttu-id="afd63-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="afd63-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="afd63-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="afd63-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="afd63-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="afd63-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="afd63-107">marcador de la dirección URL de iOS</span><span class="sxs-lookup"><span data-stu-id="afd63-107">iOS URL bookmark</span></span>
## <a name="properties"></a><span data-ttu-id="afd63-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="afd63-108">Properties</span></span>
|<span data-ttu-id="afd63-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="afd63-109">Property</span></span>|<span data-ttu-id="afd63-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="afd63-110">Type</span></span>|<span data-ttu-id="afd63-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="afd63-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="afd63-112">url</span><span class="sxs-lookup"><span data-stu-id="afd63-112">url</span></span>|<span data-ttu-id="afd63-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="afd63-113">String</span></span>|<span data-ttu-id="afd63-114">Dirección URL que permite acceder a</span><span class="sxs-lookup"><span data-stu-id="afd63-114">URL allowed to access</span></span>|
|<span data-ttu-id="afd63-115">bookmarkFolder</span><span class="sxs-lookup"><span data-stu-id="afd63-115">bookmarkFolder</span></span>|<span data-ttu-id="afd63-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="afd63-116">String</span></span>|<span data-ttu-id="afd63-117">La carpeta en la que se debe agregar el marcador en Safari</span><span class="sxs-lookup"><span data-stu-id="afd63-117">The folder into which the bookmark should be added in Safari</span></span>|
|<span data-ttu-id="afd63-118">displayName</span><span class="sxs-lookup"><span data-stu-id="afd63-118">displayName</span></span>|<span data-ttu-id="afd63-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="afd63-119">String</span></span>|<span data-ttu-id="afd63-120">El nombre para mostrar del marcador</span><span class="sxs-lookup"><span data-stu-id="afd63-120">The display name of the bookmark</span></span>|

## <a name="relationships"></a><span data-ttu-id="afd63-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="afd63-121">Relationships</span></span>
<span data-ttu-id="afd63-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="afd63-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="afd63-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="afd63-123">JSON Representation</span></span>
<span data-ttu-id="afd63-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="afd63-124">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosBookmark"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosBookmark",
  "url": "String",
  "bookmarkFolder": "String",
  "displayName": "String"
}
```






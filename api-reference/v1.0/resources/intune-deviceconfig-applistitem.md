---
title: Tipo de recurso appListItem
description: Representa una aplicación en la lista de aplicaciones administradas
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a70f68d291036a7a01823c1946aac655aee6e71c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27954431"
---
# <a name="applistitem-resource-type"></a><span data-ttu-id="3a89b-103">Tipo de recurso appListItem</span><span class="sxs-lookup"><span data-stu-id="3a89b-103">appListItem resource type</span></span>

> <span data-ttu-id="3a89b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3a89b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3a89b-105">Representa una aplicación en la lista de aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="3a89b-105">Represents an app in the list of managed applications</span></span>
## <a name="properties"></a><span data-ttu-id="3a89b-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3a89b-106">Properties</span></span>
|<span data-ttu-id="3a89b-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3a89b-107">Property</span></span>|<span data-ttu-id="3a89b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a89b-108">Type</span></span>|<span data-ttu-id="3a89b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a89b-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3a89b-110">name</span><span class="sxs-lookup"><span data-stu-id="3a89b-110">name</span></span>|<span data-ttu-id="3a89b-111">cadena</span><span class="sxs-lookup"><span data-stu-id="3a89b-111">String</span></span>|<span data-ttu-id="3a89b-112">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="3a89b-112">The application name</span></span>|
|<span data-ttu-id="3a89b-113">publicador</span><span class="sxs-lookup"><span data-stu-id="3a89b-113">publisher</span></span>|<span data-ttu-id="3a89b-114">cadena</span><span class="sxs-lookup"><span data-stu-id="3a89b-114">String</span></span>|<span data-ttu-id="3a89b-115">Publicador de la aplicación</span><span class="sxs-lookup"><span data-stu-id="3a89b-115">The publisher of the application</span></span>|
|<span data-ttu-id="3a89b-116">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="3a89b-116">appStoreUrl</span></span>|<span data-ttu-id="3a89b-117">cadena</span><span class="sxs-lookup"><span data-stu-id="3a89b-117">String</span></span>|<span data-ttu-id="3a89b-118">Dirección URL de la tienda de la aplicación</span><span class="sxs-lookup"><span data-stu-id="3a89b-118">The Store URL of the application</span></span>|
|<span data-ttu-id="3a89b-119">appId</span><span class="sxs-lookup"><span data-stu-id="3a89b-119">appId</span></span>|<span data-ttu-id="3a89b-120">cadena</span><span class="sxs-lookup"><span data-stu-id="3a89b-120">String</span></span>|<span data-ttu-id="3a89b-121">El identificador de la aplicación o de la agrupación de la aplicación</span><span class="sxs-lookup"><span data-stu-id="3a89b-121">The application or bundle identifier of the application</span></span>|

## <a name="relationships"></a><span data-ttu-id="3a89b-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3a89b-122">Relationships</span></span>
<span data-ttu-id="3a89b-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3a89b-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="3a89b-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3a89b-124">JSON Representation</span></span>
<span data-ttu-id="3a89b-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3a89b-125">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.appListItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.appListItem",
  "name": "String",
  "publisher": "String",
  "appStoreUrl": "String",
  "appId": "String"
}
```




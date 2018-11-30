---
title: Tipo de recurso appListItem
description: Representa una aplicación en la lista de aplicaciones administradas
ms.openlocfilehash: 16d191bb53f7546598b7869e8bc28be07cc4f604
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087561"
---
# <a name="applistitem-resource-type"></a><span data-ttu-id="d3d24-103">Tipo de recurso appListItem</span><span class="sxs-lookup"><span data-stu-id="d3d24-103">appListItem resource type</span></span>

> <span data-ttu-id="d3d24-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d3d24-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d3d24-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d3d24-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d3d24-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d3d24-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d3d24-107">Representa una aplicación en la lista de aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="d3d24-107">Represents an app in the list of managed applications</span></span>
## <a name="properties"></a><span data-ttu-id="d3d24-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d3d24-108">Properties</span></span>
|<span data-ttu-id="d3d24-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d3d24-109">Property</span></span>|<span data-ttu-id="d3d24-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="d3d24-110">Type</span></span>|<span data-ttu-id="d3d24-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3d24-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d3d24-112">name</span><span class="sxs-lookup"><span data-stu-id="d3d24-112">name</span></span>|<span data-ttu-id="d3d24-113">cadena</span><span class="sxs-lookup"><span data-stu-id="d3d24-113">String</span></span>|<span data-ttu-id="d3d24-114">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="d3d24-114">The application name</span></span>|
|<span data-ttu-id="d3d24-115">publicador</span><span class="sxs-lookup"><span data-stu-id="d3d24-115">publisher</span></span>|<span data-ttu-id="d3d24-116">cadena</span><span class="sxs-lookup"><span data-stu-id="d3d24-116">String</span></span>|<span data-ttu-id="d3d24-117">Publicador de la aplicación</span><span class="sxs-lookup"><span data-stu-id="d3d24-117">The publisher of the application</span></span>|
|<span data-ttu-id="d3d24-118">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="d3d24-118">appStoreUrl</span></span>|<span data-ttu-id="d3d24-119">cadena</span><span class="sxs-lookup"><span data-stu-id="d3d24-119">String</span></span>|<span data-ttu-id="d3d24-120">Dirección URL de la tienda de la aplicación</span><span class="sxs-lookup"><span data-stu-id="d3d24-120">The Store URL of the application</span></span>|
|<span data-ttu-id="d3d24-121">appId</span><span class="sxs-lookup"><span data-stu-id="d3d24-121">appId</span></span>|<span data-ttu-id="d3d24-122">cadena</span><span class="sxs-lookup"><span data-stu-id="d3d24-122">String</span></span>|<span data-ttu-id="d3d24-123">El identificador de la aplicación o de la agrupación de la aplicación</span><span class="sxs-lookup"><span data-stu-id="d3d24-123">The application or bundle identifier of the application</span></span>|

## <a name="relationships"></a><span data-ttu-id="d3d24-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d3d24-124">Relationships</span></span>
<span data-ttu-id="d3d24-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d3d24-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d3d24-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d3d24-126">JSON Representation</span></span>
<span data-ttu-id="d3d24-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d3d24-127">Here is a JSON representation of the resource.</span></span>
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






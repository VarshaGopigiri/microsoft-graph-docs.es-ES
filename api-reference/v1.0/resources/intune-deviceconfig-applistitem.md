---
title: Tipo de recurso appListItem
description: Representa una aplicación en la lista de aplicaciones administradas
ms.openlocfilehash: c9b39b5fdee8bb503ef66f729a6ee478581a6391
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029215"
---
# <a name="applistitem-resource-type"></a><span data-ttu-id="8bbe5-103">Tipo de recurso appListItem</span><span class="sxs-lookup"><span data-stu-id="8bbe5-103">appListItem resource type</span></span>

> <span data-ttu-id="8bbe5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8bbe5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8bbe5-105">Representa una aplicación en la lista de aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="8bbe5-105">Represents an app in the list of managed applications</span></span>
## <a name="properties"></a><span data-ttu-id="8bbe5-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8bbe5-106">Properties</span></span>
|<span data-ttu-id="8bbe5-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8bbe5-107">Property</span></span>|<span data-ttu-id="8bbe5-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8bbe5-108">Type</span></span>|<span data-ttu-id="8bbe5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bbe5-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8bbe5-110">name</span><span class="sxs-lookup"><span data-stu-id="8bbe5-110">name</span></span>|<span data-ttu-id="8bbe5-111">cadena</span><span class="sxs-lookup"><span data-stu-id="8bbe5-111">String</span></span>|<span data-ttu-id="8bbe5-112">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="8bbe5-112">The application name</span></span>|
|<span data-ttu-id="8bbe5-113">publicador</span><span class="sxs-lookup"><span data-stu-id="8bbe5-113">publisher</span></span>|<span data-ttu-id="8bbe5-114">cadena</span><span class="sxs-lookup"><span data-stu-id="8bbe5-114">String</span></span>|<span data-ttu-id="8bbe5-115">Publicador de la aplicación</span><span class="sxs-lookup"><span data-stu-id="8bbe5-115">The publisher of the application</span></span>|
|<span data-ttu-id="8bbe5-116">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="8bbe5-116">appStoreUrl</span></span>|<span data-ttu-id="8bbe5-117">cadena</span><span class="sxs-lookup"><span data-stu-id="8bbe5-117">String</span></span>|<span data-ttu-id="8bbe5-118">Dirección URL de la tienda de la aplicación</span><span class="sxs-lookup"><span data-stu-id="8bbe5-118">The Store URL of the application</span></span>|
|<span data-ttu-id="8bbe5-119">appId</span><span class="sxs-lookup"><span data-stu-id="8bbe5-119">appId</span></span>|<span data-ttu-id="8bbe5-120">cadena</span><span class="sxs-lookup"><span data-stu-id="8bbe5-120">String</span></span>|<span data-ttu-id="8bbe5-121">El identificador de la aplicación o de la agrupación de la aplicación</span><span class="sxs-lookup"><span data-stu-id="8bbe5-121">The application or bundle identifier of the application</span></span>|

## <a name="relationships"></a><span data-ttu-id="8bbe5-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8bbe5-122">Relationships</span></span>
<span data-ttu-id="8bbe5-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8bbe5-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8bbe5-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8bbe5-124">JSON Representation</span></span>
<span data-ttu-id="8bbe5-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8bbe5-125">Here is a JSON representation of the resource.</span></span>
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




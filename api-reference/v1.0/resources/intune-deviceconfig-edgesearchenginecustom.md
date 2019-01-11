---
title: Tipo de recurso edgeSearchEngineCustom
description: Permite a los administradores de TI configurar un motor de búsqueda predeterminado personalizado para dispositivos controlados por MDM.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 9797b311ae5c4741364a99da0c056c8fb3e18788
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845804"
---
# <a name="edgesearchenginecustom-resource-type"></a><span data-ttu-id="17033-103">Tipo de recurso edgeSearchEngineCustom</span><span class="sxs-lookup"><span data-stu-id="17033-103">edgeSearchEngineCustom resource type</span></span>

> <span data-ttu-id="17033-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="17033-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="17033-105">Permite a los administradores de TI configurar un motor de búsqueda predeterminado personalizado para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="17033-105">Allows IT admins to set a custom default search engine for MDM-Controlled devices.</span></span>

<span data-ttu-id="17033-106">Hereda de [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)</span><span class="sxs-lookup"><span data-stu-id="17033-106">Inherits from [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)</span></span>

## <a name="properties"></a><span data-ttu-id="17033-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17033-107">Properties</span></span>
|<span data-ttu-id="17033-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="17033-108">Property</span></span>|<span data-ttu-id="17033-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="17033-109">Type</span></span>|<span data-ttu-id="17033-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="17033-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="17033-111">edgeSearchEngineOpenSearchXmlUrl</span><span class="sxs-lookup"><span data-stu-id="17033-111">edgeSearchEngineOpenSearchXmlUrl</span></span>|<span data-ttu-id="17033-112">cadena</span><span class="sxs-lookup"><span data-stu-id="17033-112">String</span></span>|<span data-ttu-id="17033-113">Apunta a un vínculo HTTPS que contiene el archivo XML OpenSearch, que incluye, como mínimo, el nombre corto y la dirección URL del motor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="17033-113">Points to a https link containing the OpenSearch xml file that contains, at minimum, the short name and the URL to the search Engine.</span></span>|

## <a name="relationships"></a><span data-ttu-id="17033-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="17033-114">Relationships</span></span>
<span data-ttu-id="17033-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="17033-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="17033-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="17033-116">JSON Representation</span></span>
<span data-ttu-id="17033-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="17033-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.edgeSearchEngineCustom"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.edgeSearchEngineCustom",
  "edgeSearchEngineOpenSearchXmlUrl": "String"
}
```




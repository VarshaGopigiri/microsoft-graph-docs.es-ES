---
title: Tipo de recurso edgeSearchEngineCustom
description: Permite a los administradores de TI configurar un motor de búsqueda predeterminado personalizado para dispositivos controlados por MDM.
author: tfitzmac
ms.openlocfilehash: 1a9c1dc12226bf13764a155e804d379d20825103
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344236"
---
# <a name="edgesearchenginecustom-resource-type"></a><span data-ttu-id="f24bf-103">Tipo de recurso edgeSearchEngineCustom</span><span class="sxs-lookup"><span data-stu-id="f24bf-103">edgeSearchEngineCustom resource type</span></span>

> <span data-ttu-id="f24bf-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f24bf-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f24bf-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f24bf-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f24bf-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f24bf-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f24bf-107">Permite a los administradores de TI configurar un motor de búsqueda predeterminado personalizado para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="f24bf-107">Allows IT admins to set a custom default search engine for MDM-Controlled devices.</span></span>

<span data-ttu-id="f24bf-108">Hereda de [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)</span><span class="sxs-lookup"><span data-stu-id="f24bf-108">Inherits from [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)</span></span>

## <a name="properties"></a><span data-ttu-id="f24bf-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f24bf-109">Properties</span></span>
|<span data-ttu-id="f24bf-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f24bf-110">Property</span></span>|<span data-ttu-id="f24bf-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="f24bf-111">Type</span></span>|<span data-ttu-id="f24bf-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f24bf-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f24bf-113">edgeSearchEngineOpenSearchXmlUrl</span><span class="sxs-lookup"><span data-stu-id="f24bf-113">edgeSearchEngineOpenSearchXmlUrl</span></span>|<span data-ttu-id="f24bf-114">cadena</span><span class="sxs-lookup"><span data-stu-id="f24bf-114">String</span></span>|<span data-ttu-id="f24bf-115">Apunta a un vínculo HTTPS que contiene el archivo XML OpenSearch, que incluye, como mínimo, el nombre corto y la dirección URL del motor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f24bf-115">Points to a https link containing the OpenSearch xml file that contains, at minimum, the short name and the URL to the search Engine.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f24bf-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f24bf-116">Relationships</span></span>
<span data-ttu-id="f24bf-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f24bf-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f24bf-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f24bf-118">JSON Representation</span></span>
<span data-ttu-id="f24bf-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f24bf-119">Here is a JSON representation of the resource.</span></span>
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






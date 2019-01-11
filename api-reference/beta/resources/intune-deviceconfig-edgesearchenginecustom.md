---
title: Tipo de recurso edgeSearchEngineCustom
description: Permite a los administradores de TI configurar un motor de búsqueda predeterminado personalizado para dispositivos controlados por MDM.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: f5dbab3a3cc394df44d02dff1b79ffe5440f7a42
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27879796"
---
# <a name="edgesearchenginecustom-resource-type"></a><span data-ttu-id="8f9bd-103">Tipo de recurso edgeSearchEngineCustom</span><span class="sxs-lookup"><span data-stu-id="8f9bd-103">edgeSearchEngineCustom resource type</span></span>

> <span data-ttu-id="8f9bd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8f9bd-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8f9bd-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8f9bd-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8f9bd-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8f9bd-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8f9bd-107">Permite a los administradores de TI configurar un motor de búsqueda predeterminado personalizado para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="8f9bd-107">Allows IT admins to set a custom default search engine for MDM-Controlled devices.</span></span>

<span data-ttu-id="8f9bd-108">Hereda de [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)</span><span class="sxs-lookup"><span data-stu-id="8f9bd-108">Inherits from [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)</span></span>

## <a name="properties"></a><span data-ttu-id="8f9bd-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8f9bd-109">Properties</span></span>
|<span data-ttu-id="8f9bd-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8f9bd-110">Property</span></span>|<span data-ttu-id="8f9bd-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f9bd-111">Type</span></span>|<span data-ttu-id="8f9bd-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f9bd-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8f9bd-113">edgeSearchEngineOpenSearchXmlUrl</span><span class="sxs-lookup"><span data-stu-id="8f9bd-113">edgeSearchEngineOpenSearchXmlUrl</span></span>|<span data-ttu-id="8f9bd-114">cadena</span><span class="sxs-lookup"><span data-stu-id="8f9bd-114">String</span></span>|<span data-ttu-id="8f9bd-115">Apunta a un vínculo HTTPS que contiene el archivo XML OpenSearch, que incluye, como mínimo, el nombre corto y la dirección URL del motor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8f9bd-115">Points to a https link containing the OpenSearch xml file that contains, at minimum, the short name and the URL to the search Engine.</span></span>|

## <a name="relationships"></a><span data-ttu-id="8f9bd-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8f9bd-116">Relationships</span></span>
<span data-ttu-id="8f9bd-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8f9bd-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8f9bd-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8f9bd-118">JSON Representation</span></span>
<span data-ttu-id="8f9bd-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8f9bd-119">Here is a JSON representation of the resource.</span></span>
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






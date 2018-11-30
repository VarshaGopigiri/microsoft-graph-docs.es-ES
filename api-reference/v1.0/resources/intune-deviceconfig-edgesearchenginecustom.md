---
title: Tipo de recurso edgeSearchEngineCustom
description: Permite a los administradores de TI configurar un motor de búsqueda predeterminado personalizado para dispositivos controlados por MDM.
ms.openlocfilehash: 54617b01fc3082fc8c80b653e7df36e48c1de0d1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030414"
---
# <a name="edgesearchenginecustom-resource-type"></a><span data-ttu-id="d1820-103">Tipo de recurso edgeSearchEngineCustom</span><span class="sxs-lookup"><span data-stu-id="d1820-103">edgeSearchEngineCustom resource type</span></span>

> <span data-ttu-id="d1820-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d1820-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d1820-105">Permite a los administradores de TI configurar un motor de búsqueda predeterminado personalizado para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="d1820-105">Allows IT admins to set a custom default search engine for MDM-Controlled devices.</span></span>

<span data-ttu-id="d1820-106">Hereda de [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)</span><span class="sxs-lookup"><span data-stu-id="d1820-106">Inherits from [edgeSearchEngineBase](../resources/intune-deviceconfig-edgesearchenginebase.md)</span></span>

## <a name="properties"></a><span data-ttu-id="d1820-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1820-107">Properties</span></span>
|<span data-ttu-id="d1820-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d1820-108">Property</span></span>|<span data-ttu-id="d1820-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d1820-109">Type</span></span>|<span data-ttu-id="d1820-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1820-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d1820-111">edgeSearchEngineOpenSearchXmlUrl</span><span class="sxs-lookup"><span data-stu-id="d1820-111">edgeSearchEngineOpenSearchXmlUrl</span></span>|<span data-ttu-id="d1820-112">cadena</span><span class="sxs-lookup"><span data-stu-id="d1820-112">String</span></span>|<span data-ttu-id="d1820-113">Apunta a un vínculo HTTPS que contiene el archivo XML OpenSearch, que incluye, como mínimo, el nombre corto y la dirección URL del motor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d1820-113">Points to a https link containing the OpenSearch xml file that contains, at minimum, the short name and the URL to the search Engine.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d1820-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d1820-114">Relationships</span></span>
<span data-ttu-id="d1820-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d1820-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d1820-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d1820-116">JSON Representation</span></span>
<span data-ttu-id="d1820-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d1820-117">Here is a JSON representation of the resource.</span></span>
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




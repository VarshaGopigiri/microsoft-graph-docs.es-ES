---
title: tipo de recurso win32LobAppReturnCode
description: Contiene las propiedades de código de retorno para una aplicación de Win32
ms.openlocfilehash: 5f32e7e5953ade1036c49ac2fb45555fd353fa1d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084961"
---
# <a name="win32lobappreturncode-resource-type"></a><span data-ttu-id="57cee-103">tipo de recurso win32LobAppReturnCode</span><span class="sxs-lookup"><span data-stu-id="57cee-103">win32LobAppReturnCode resource type</span></span>

> <span data-ttu-id="57cee-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="57cee-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="57cee-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="57cee-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="57cee-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="57cee-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="57cee-107">Contiene las propiedades de código de retorno para una aplicación de Win32</span><span class="sxs-lookup"><span data-stu-id="57cee-107">Contains return code properties for a Win32 App</span></span>
## <a name="properties"></a><span data-ttu-id="57cee-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="57cee-108">Properties</span></span>
|<span data-ttu-id="57cee-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="57cee-109">Property</span></span>|<span data-ttu-id="57cee-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="57cee-110">Type</span></span>|<span data-ttu-id="57cee-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="57cee-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="57cee-112">returnCode</span><span class="sxs-lookup"><span data-stu-id="57cee-112">returnCode</span></span>|<span data-ttu-id="57cee-113">Int32</span><span class="sxs-lookup"><span data-stu-id="57cee-113">Int32</span></span>|<span data-ttu-id="57cee-114">Código de retorno.</span><span class="sxs-lookup"><span data-stu-id="57cee-114">Return code.</span></span>|
|<span data-ttu-id="57cee-115">type</span><span class="sxs-lookup"><span data-stu-id="57cee-115">type</span></span>|[<span data-ttu-id="57cee-116">win32LobAppReturnCodeType</span><span class="sxs-lookup"><span data-stu-id="57cee-116">win32LobAppReturnCodeType</span></span>](../resources/intune-apps-win32lobappreturncodetype.md)|<span data-ttu-id="57cee-117">El tipo de código de retorno.</span><span class="sxs-lookup"><span data-stu-id="57cee-117">The type of return code.</span></span> <span data-ttu-id="57cee-118">Los valores posibles son: `failed`, `success`, `softReboot`, `hardReboot` y `retry`.</span><span class="sxs-lookup"><span data-stu-id="57cee-118">Possible values are: `failed`, `success`, `softReboot`, `hardReboot`, `retry`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="57cee-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="57cee-119">Relationships</span></span>
<span data-ttu-id="57cee-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="57cee-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="57cee-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="57cee-121">JSON Representation</span></span>
<span data-ttu-id="57cee-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="57cee-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.win32LobAppReturnCode"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobAppReturnCode",
  "returnCode": 1024,
  "type": "String"
}
```






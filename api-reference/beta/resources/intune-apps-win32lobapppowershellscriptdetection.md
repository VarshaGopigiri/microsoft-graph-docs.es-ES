---
title: tipo de recurso win32LobAppPowerShellScriptDetection
description: Contiene las propiedades de la secuencia de comandos de PowerShell para detectar una aplicación de Win32
ms.openlocfilehash: e5d87d3d2a90c0ac7f8ce6db7e14b105583a76f9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086959"
---
# <a name="win32lobapppowershellscriptdetection-resource-type"></a><span data-ttu-id="24037-103">tipo de recurso win32LobAppPowerShellScriptDetection</span><span class="sxs-lookup"><span data-stu-id="24037-103">win32LobAppPowerShellScriptDetection resource type</span></span>

> <span data-ttu-id="24037-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="24037-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="24037-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="24037-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="24037-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="24037-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="24037-107">Contiene las propiedades de la secuencia de comandos de PowerShell para detectar una aplicación de Win32</span><span class="sxs-lookup"><span data-stu-id="24037-107">Contains PowerShell script properties to detect a Win32 App</span></span>

<span data-ttu-id="24037-108">Hereda de [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)</span><span class="sxs-lookup"><span data-stu-id="24037-108">Inherits from [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)</span></span>

## <a name="properties"></a><span data-ttu-id="24037-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="24037-109">Properties</span></span>
|<span data-ttu-id="24037-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="24037-110">Property</span></span>|<span data-ttu-id="24037-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="24037-111">Type</span></span>|<span data-ttu-id="24037-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="24037-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="24037-113">enforceSignatureCheck</span><span class="sxs-lookup"><span data-stu-id="24037-113">enforceSignatureCheck</span></span>|<span data-ttu-id="24037-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="24037-114">Boolean</span></span>|<span data-ttu-id="24037-115">Un valor que indica si se exige la comprobación de firma</span><span class="sxs-lookup"><span data-stu-id="24037-115">A value indicating whether signature check is enforced</span></span>|
|<span data-ttu-id="24037-116">runAs32Bit</span><span class="sxs-lookup"><span data-stu-id="24037-116">runAs32Bit</span></span>|<span data-ttu-id="24037-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="24037-117">Boolean</span></span>|<span data-ttu-id="24037-118">Un valor que indica si este script se debe ejecutar como de 32 bits</span><span class="sxs-lookup"><span data-stu-id="24037-118">A value indicating whether this script should run as 32-bit</span></span>|
|<span data-ttu-id="24037-119">scriptContent</span><span class="sxs-lookup"><span data-stu-id="24037-119">scriptContent</span></span>|<span data-ttu-id="24037-120">String</span><span class="sxs-lookup"><span data-stu-id="24037-120">String</span></span>|<span data-ttu-id="24037-121">La base64 codificado contenido de la secuencia de comandos para detectar la aplicación de línea de negocio (LoB) de Win32</span><span class="sxs-lookup"><span data-stu-id="24037-121">The base64 encoded script content to detect Win32 Line of Business (LoB) app</span></span>|

## <a name="relationships"></a><span data-ttu-id="24037-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="24037-122">Relationships</span></span>
<span data-ttu-id="24037-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="24037-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="24037-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="24037-124">JSON Representation</span></span>
<span data-ttu-id="24037-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="24037-125">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.win32LobAppPowerShellScriptDetection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobAppPowerShellScriptDetection",
  "enforceSignatureCheck": true,
  "runAs32Bit": true,
  "scriptContent": "String"
}
```





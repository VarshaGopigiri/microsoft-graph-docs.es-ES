---
title: tipo de recurso win32LobAppInstallExperience
description: Contiene las propiedades de la experiencia de instalación para una aplicación de Win32
ms.openlocfilehash: 04fed453125155073d75de417d13cfd81a5bcdd1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084284"
---
# <a name="win32lobappinstallexperience-resource-type"></a><span data-ttu-id="13c54-103">tipo de recurso win32LobAppInstallExperience</span><span class="sxs-lookup"><span data-stu-id="13c54-103">win32LobAppInstallExperience resource type</span></span>

> <span data-ttu-id="13c54-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="13c54-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="13c54-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="13c54-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="13c54-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="13c54-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="13c54-107">Contiene las propiedades de la experiencia de instalación para una aplicación de Win32</span><span class="sxs-lookup"><span data-stu-id="13c54-107">Contains installation experience properties for a Win32 App</span></span>
## <a name="properties"></a><span data-ttu-id="13c54-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="13c54-108">Properties</span></span>
|<span data-ttu-id="13c54-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="13c54-109">Property</span></span>|<span data-ttu-id="13c54-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="13c54-110">Type</span></span>|<span data-ttu-id="13c54-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="13c54-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="13c54-112">runAsAccount</span><span class="sxs-lookup"><span data-stu-id="13c54-112">runAsAccount</span></span>|[<span data-ttu-id="13c54-113">runAsAccountType</span><span class="sxs-lookup"><span data-stu-id="13c54-113">runAsAccountType</span></span>](../resources/intune-shared-runasaccounttype.md)|<span data-ttu-id="13c54-114">Indica el tipo de la aplicación se ejecuta en el contexto de ejecución.</span><span class="sxs-lookup"><span data-stu-id="13c54-114">Indicates the type of execution context the app runs in.</span></span> <span data-ttu-id="13c54-115">Los valores posibles son: `system` y `user`.</span><span class="sxs-lookup"><span data-stu-id="13c54-115">Possible values are: `system`, `user`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="13c54-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="13c54-116">Relationships</span></span>
<span data-ttu-id="13c54-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="13c54-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="13c54-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="13c54-118">JSON Representation</span></span>
<span data-ttu-id="13c54-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="13c54-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.win32LobAppInstallExperience"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobAppInstallExperience",
  "runAsAccount": "String"
}
```






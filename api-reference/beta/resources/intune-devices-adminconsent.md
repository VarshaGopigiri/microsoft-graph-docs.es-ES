---
title: tipo de recurso adminConsent
description: Información de consentimiento de administración.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 428729ff9a8a8ee5deb64c537922cb7a0417ba2e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962131"
---
# <a name="adminconsent-resource-type"></a><span data-ttu-id="41fb5-103">tipo de recurso adminConsent</span><span class="sxs-lookup"><span data-stu-id="41fb5-103">adminConsent resource type</span></span>

> <span data-ttu-id="41fb5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="41fb5-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="41fb5-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="41fb5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="41fb5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="41fb5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="41fb5-107">Información de consentimiento de administración.</span><span class="sxs-lookup"><span data-stu-id="41fb5-107">Admin consent information.</span></span>
## <a name="properties"></a><span data-ttu-id="41fb5-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="41fb5-108">Properties</span></span>
|<span data-ttu-id="41fb5-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="41fb5-109">Property</span></span>|<span data-ttu-id="41fb5-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="41fb5-110">Type</span></span>|<span data-ttu-id="41fb5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="41fb5-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="41fb5-112">shareAPNSData</span><span class="sxs-lookup"><span data-stu-id="41fb5-112">shareAPNSData</span></span>|[<span data-ttu-id="41fb5-113">adminConsentState</span><span class="sxs-lookup"><span data-stu-id="41fb5-113">adminConsentState</span></span>](../resources/intune-devices-adminconsentstate.md)|<span data-ttu-id="41fb5-114">El estado de consentimiento de administración de uso compartido de datos de usuarios y dispositivos para Apple.</span><span class="sxs-lookup"><span data-stu-id="41fb5-114">The admin consent state of sharing user and device data to Apple.</span></span> <span data-ttu-id="41fb5-115">Los valores posibles son: `notConfigured`, `granted` y `notGranted`.</span><span class="sxs-lookup"><span data-stu-id="41fb5-115">Possible values are: `notConfigured`, `granted`, `notGranted`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="41fb5-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="41fb5-116">Relationships</span></span>
<span data-ttu-id="41fb5-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="41fb5-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="41fb5-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="41fb5-118">JSON Representation</span></span>
<span data-ttu-id="41fb5-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="41fb5-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.adminConsent"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.adminConsent",
  "shareAPNSData": "String"
}
```






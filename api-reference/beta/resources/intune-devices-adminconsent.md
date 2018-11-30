---
title: tipo de recurso adminConsent
description: Información de consentimiento de administración.
ms.openlocfilehash: da7197c995d9c87ab69db11ae0c6c0804482877d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087964"
---
# <a name="adminconsent-resource-type"></a><span data-ttu-id="12e4a-103">tipo de recurso adminConsent</span><span class="sxs-lookup"><span data-stu-id="12e4a-103">adminConsent resource type</span></span>

> <span data-ttu-id="12e4a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="12e4a-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="12e4a-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="12e4a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="12e4a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="12e4a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="12e4a-107">Información de consentimiento de administración.</span><span class="sxs-lookup"><span data-stu-id="12e4a-107">Admin consent information.</span></span>
## <a name="properties"></a><span data-ttu-id="12e4a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="12e4a-108">Properties</span></span>
|<span data-ttu-id="12e4a-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="12e4a-109">Property</span></span>|<span data-ttu-id="12e4a-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="12e4a-110">Type</span></span>|<span data-ttu-id="12e4a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="12e4a-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="12e4a-112">shareAPNSData</span><span class="sxs-lookup"><span data-stu-id="12e4a-112">shareAPNSData</span></span>|[<span data-ttu-id="12e4a-113">adminConsentState</span><span class="sxs-lookup"><span data-stu-id="12e4a-113">adminConsentState</span></span>](../resources/intune-devices-adminconsentstate.md)|<span data-ttu-id="12e4a-114">El estado de consentimiento de administración de uso compartido de datos de usuarios y dispositivos para Apple.</span><span class="sxs-lookup"><span data-stu-id="12e4a-114">The admin consent state of sharing user and device data to Apple.</span></span> <span data-ttu-id="12e4a-115">Los valores posibles son: `notConfigured`, `granted` y `notGranted`.</span><span class="sxs-lookup"><span data-stu-id="12e4a-115">Possible values are: `notConfigured`, `granted`, `notGranted`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="12e4a-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="12e4a-116">Relationships</span></span>
<span data-ttu-id="12e4a-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="12e4a-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="12e4a-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="12e4a-118">JSON Representation</span></span>
<span data-ttu-id="12e4a-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="12e4a-119">Here is a JSON representation of the resource.</span></span>
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





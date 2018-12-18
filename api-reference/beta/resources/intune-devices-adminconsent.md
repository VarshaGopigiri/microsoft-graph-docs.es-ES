---
title: tipo de recurso adminConsent
description: Información de consentimiento de administración.
author: tfitzmac
ms.openlocfilehash: 7e535eb3475745c8c8aabb2701d9b9e24b8d3b02
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27354085"
---
# <a name="adminconsent-resource-type"></a><span data-ttu-id="6899f-103">tipo de recurso adminConsent</span><span class="sxs-lookup"><span data-stu-id="6899f-103">adminConsent resource type</span></span>

> <span data-ttu-id="6899f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6899f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6899f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6899f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6899f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6899f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6899f-107">Información de consentimiento de administración.</span><span class="sxs-lookup"><span data-stu-id="6899f-107">Admin consent information.</span></span>
## <a name="properties"></a><span data-ttu-id="6899f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6899f-108">Properties</span></span>
|<span data-ttu-id="6899f-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6899f-109">Property</span></span>|<span data-ttu-id="6899f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="6899f-110">Type</span></span>|<span data-ttu-id="6899f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6899f-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6899f-112">shareAPNSData</span><span class="sxs-lookup"><span data-stu-id="6899f-112">shareAPNSData</span></span>|[<span data-ttu-id="6899f-113">adminConsentState</span><span class="sxs-lookup"><span data-stu-id="6899f-113">adminConsentState</span></span>](../resources/intune-devices-adminconsentstate.md)|<span data-ttu-id="6899f-114">El estado de consentimiento de administración de uso compartido de datos de usuarios y dispositivos para Apple.</span><span class="sxs-lookup"><span data-stu-id="6899f-114">The admin consent state of sharing user and device data to Apple.</span></span> <span data-ttu-id="6899f-115">Los valores posibles son: `notConfigured`, `granted` y `notGranted`.</span><span class="sxs-lookup"><span data-stu-id="6899f-115">Possible values are: `notConfigured`, `granted`, `notGranted`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="6899f-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6899f-116">Relationships</span></span>
<span data-ttu-id="6899f-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="6899f-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="6899f-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6899f-118">JSON Representation</span></span>
<span data-ttu-id="6899f-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6899f-119">Here is a JSON representation of the resource.</span></span>
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






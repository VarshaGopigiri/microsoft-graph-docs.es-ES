---
title: tipo de recurso customSubjectAlternativeName
description: Definición de nombre alternativo del sujeto personalizada
ms.openlocfilehash: 14d6c24cd5e8c087b81fa51194301da522d169b5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086971"
---
# <a name="customsubjectalternativename-resource-type"></a><span data-ttu-id="5f77e-103">tipo de recurso customSubjectAlternativeName</span><span class="sxs-lookup"><span data-stu-id="5f77e-103">customSubjectAlternativeName resource type</span></span>

> <span data-ttu-id="5f77e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5f77e-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5f77e-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5f77e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5f77e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5f77e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5f77e-107">Definición de nombre alternativo del sujeto personalizada</span><span class="sxs-lookup"><span data-stu-id="5f77e-107">Custom Subject Alternative Name definition</span></span>
## <a name="properties"></a><span data-ttu-id="5f77e-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5f77e-108">Properties</span></span>
|<span data-ttu-id="5f77e-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5f77e-109">Property</span></span>|<span data-ttu-id="5f77e-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f77e-110">Type</span></span>|<span data-ttu-id="5f77e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f77e-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5f77e-112">sanType</span><span class="sxs-lookup"><span data-stu-id="5f77e-112">sanType</span></span>|[<span data-ttu-id="5f77e-113">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="5f77e-113">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="5f77e-114">Tipo de SAN personalizado.</span><span class="sxs-lookup"><span data-stu-id="5f77e-114">Custom SAN Type.</span></span> <span data-ttu-id="5f77e-115">Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="5f77e-115">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|
|<span data-ttu-id="5f77e-116">name</span><span class="sxs-lookup"><span data-stu-id="5f77e-116">name</span></span>|<span data-ttu-id="5f77e-117">String</span><span class="sxs-lookup"><span data-stu-id="5f77e-117">String</span></span>|<span data-ttu-id="5f77e-118">Nombre de SAN personalizado</span><span class="sxs-lookup"><span data-stu-id="5f77e-118">Custom SAN Name</span></span>|

## <a name="relationships"></a><span data-ttu-id="5f77e-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5f77e-119">Relationships</span></span>
<span data-ttu-id="5f77e-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5f77e-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5f77e-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5f77e-121">JSON Representation</span></span>
<span data-ttu-id="5f77e-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5f77e-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.customSubjectAlternativeName"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.customSubjectAlternativeName",
  "sanType": "String",
  "name": "String"
}
```






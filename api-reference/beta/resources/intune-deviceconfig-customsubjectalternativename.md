---
title: tipo de recurso customSubjectAlternativeName
description: Definición de nombre alternativo del sujeto personalizada
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 069cc1f6d93c785e4fc774d7988e0fc80febbb12
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27954123"
---
# <a name="customsubjectalternativename-resource-type"></a><span data-ttu-id="32ae1-103">tipo de recurso customSubjectAlternativeName</span><span class="sxs-lookup"><span data-stu-id="32ae1-103">customSubjectAlternativeName resource type</span></span>

> <span data-ttu-id="32ae1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="32ae1-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="32ae1-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="32ae1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="32ae1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="32ae1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="32ae1-107">Definición de nombre alternativo del sujeto personalizada</span><span class="sxs-lookup"><span data-stu-id="32ae1-107">Custom Subject Alternative Name definition</span></span>
## <a name="properties"></a><span data-ttu-id="32ae1-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32ae1-108">Properties</span></span>
|<span data-ttu-id="32ae1-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="32ae1-109">Property</span></span>|<span data-ttu-id="32ae1-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="32ae1-110">Type</span></span>|<span data-ttu-id="32ae1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="32ae1-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="32ae1-112">sanType</span><span class="sxs-lookup"><span data-stu-id="32ae1-112">sanType</span></span>|[<span data-ttu-id="32ae1-113">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="32ae1-113">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="32ae1-114">Tipo de SAN personalizado.</span><span class="sxs-lookup"><span data-stu-id="32ae1-114">Custom SAN Type.</span></span> <span data-ttu-id="32ae1-115">Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="32ae1-115">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|
|<span data-ttu-id="32ae1-116">name</span><span class="sxs-lookup"><span data-stu-id="32ae1-116">name</span></span>|<span data-ttu-id="32ae1-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="32ae1-117">String</span></span>|<span data-ttu-id="32ae1-118">Nombre de SAN personalizado</span><span class="sxs-lookup"><span data-stu-id="32ae1-118">Custom SAN Name</span></span>|

## <a name="relationships"></a><span data-ttu-id="32ae1-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="32ae1-119">Relationships</span></span>
<span data-ttu-id="32ae1-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="32ae1-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="32ae1-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="32ae1-121">JSON Representation</span></span>
<span data-ttu-id="32ae1-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="32ae1-122">Here is a JSON representation of the resource.</span></span>
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






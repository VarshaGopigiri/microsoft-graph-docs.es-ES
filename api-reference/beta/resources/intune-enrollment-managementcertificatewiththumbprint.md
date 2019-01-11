---
title: tipo de recurso managementCertificateWithThumbprint
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: d8f18e7fc117f00f99346267f544abc7d12db17e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27827219"
---
# <a name="managementcertificatewiththumbprint-resource-type"></a><span data-ttu-id="3a842-103">tipo de recurso managementCertificateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="3a842-103">managementCertificateWithThumbprint resource type</span></span>

> <span data-ttu-id="3a842-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3a842-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3a842-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3a842-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3a842-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3a842-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3a842-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3a842-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="3a842-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3a842-108">Properties</span></span>
|<span data-ttu-id="3a842-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3a842-109">Property</span></span>|<span data-ttu-id="3a842-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a842-110">Type</span></span>|<span data-ttu-id="3a842-111">Description</span><span class="sxs-lookup"><span data-stu-id="3a842-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3a842-112">huella digital</span><span class="sxs-lookup"><span data-stu-id="3a842-112">thumbprint</span></span>|<span data-ttu-id="3a842-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="3a842-113">String</span></span>|<span data-ttu-id="3a842-114">La huella digital del certificado de administración</span><span class="sxs-lookup"><span data-stu-id="3a842-114">The thumbprint of the management certificate</span></span>|
|<span data-ttu-id="3a842-115">certificado</span><span class="sxs-lookup"><span data-stu-id="3a842-115">certificate</span></span>|<span data-ttu-id="3a842-116">String</span><span class="sxs-lookup"><span data-stu-id="3a842-116">String</span></span>|<span data-ttu-id="3a842-117">El certificado de administración codificada en Base 64</span><span class="sxs-lookup"><span data-stu-id="3a842-117">The Base 64 encoded management certificate</span></span>|

## <a name="relationships"></a><span data-ttu-id="3a842-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3a842-118">Relationships</span></span>
<span data-ttu-id="3a842-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3a842-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="3a842-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3a842-120">JSON Representation</span></span>
<span data-ttu-id="3a842-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3a842-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managementCertificateWithThumbprint"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managementCertificateWithThumbprint",
  "thumbprint": "String",
  "certificate": "String"
}
```






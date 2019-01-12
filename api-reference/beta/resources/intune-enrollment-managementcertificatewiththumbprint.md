---
title: tipo de recurso managementCertificateWithThumbprint
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 6e6259c1f90547ff875fa31d3f383606749bc0dd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27983355"
---
# <a name="managementcertificatewiththumbprint-resource-type"></a><span data-ttu-id="a7d40-103">tipo de recurso managementCertificateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="a7d40-103">managementCertificateWithThumbprint resource type</span></span>

> <span data-ttu-id="a7d40-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a7d40-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a7d40-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a7d40-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a7d40-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a7d40-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a7d40-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a7d40-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="a7d40-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a7d40-108">Properties</span></span>
|<span data-ttu-id="a7d40-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a7d40-109">Property</span></span>|<span data-ttu-id="a7d40-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7d40-110">Type</span></span>|<span data-ttu-id="a7d40-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7d40-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a7d40-112">huella digital</span><span class="sxs-lookup"><span data-stu-id="a7d40-112">thumbprint</span></span>|<span data-ttu-id="a7d40-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="a7d40-113">String</span></span>|<span data-ttu-id="a7d40-114">La huella digital del certificado de administración</span><span class="sxs-lookup"><span data-stu-id="a7d40-114">The thumbprint of the management certificate</span></span>|
|<span data-ttu-id="a7d40-115">certificado</span><span class="sxs-lookup"><span data-stu-id="a7d40-115">certificate</span></span>|<span data-ttu-id="a7d40-116">String</span><span class="sxs-lookup"><span data-stu-id="a7d40-116">String</span></span>|<span data-ttu-id="a7d40-117">El certificado de administración codificada en Base 64</span><span class="sxs-lookup"><span data-stu-id="a7d40-117">The Base 64 encoded management certificate</span></span>|

## <a name="relationships"></a><span data-ttu-id="a7d40-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a7d40-118">Relationships</span></span>
<span data-ttu-id="a7d40-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a7d40-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a7d40-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a7d40-120">JSON Representation</span></span>
<span data-ttu-id="a7d40-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a7d40-121">Here is a JSON representation of the resource.</span></span>
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






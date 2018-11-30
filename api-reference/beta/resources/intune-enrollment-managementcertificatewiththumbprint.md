---
title: tipo de recurso managementCertificateWithThumbprint
description: Todavía no documentado
ms.openlocfilehash: 320b6241e1ac5a9078ccc32f99f87e9fd337335e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087978"
---
# <a name="managementcertificatewiththumbprint-resource-type"></a><span data-ttu-id="0ea8d-103">tipo de recurso managementCertificateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="0ea8d-103">managementCertificateWithThumbprint resource type</span></span>

> <span data-ttu-id="0ea8d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0ea8d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0ea8d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0ea8d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0ea8d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0ea8d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0ea8d-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="0ea8d-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="0ea8d-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0ea8d-108">Properties</span></span>
|<span data-ttu-id="0ea8d-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0ea8d-109">Property</span></span>|<span data-ttu-id="0ea8d-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ea8d-110">Type</span></span>|<span data-ttu-id="0ea8d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ea8d-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0ea8d-112">huella digital</span><span class="sxs-lookup"><span data-stu-id="0ea8d-112">thumbprint</span></span>|<span data-ttu-id="0ea8d-113">String</span><span class="sxs-lookup"><span data-stu-id="0ea8d-113">String</span></span>|<span data-ttu-id="0ea8d-114">La huella digital del certificado de administración</span><span class="sxs-lookup"><span data-stu-id="0ea8d-114">The thumbprint of the management certificate</span></span>|
|<span data-ttu-id="0ea8d-115">certificado</span><span class="sxs-lookup"><span data-stu-id="0ea8d-115">certificate</span></span>|<span data-ttu-id="0ea8d-116">String</span><span class="sxs-lookup"><span data-stu-id="0ea8d-116">String</span></span>|<span data-ttu-id="0ea8d-117">El certificado de administración codificada en Base 64</span><span class="sxs-lookup"><span data-stu-id="0ea8d-117">The Base 64 encoded management certificate</span></span>|

## <a name="relationships"></a><span data-ttu-id="0ea8d-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0ea8d-118">Relationships</span></span>
<span data-ttu-id="0ea8d-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0ea8d-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0ea8d-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0ea8d-120">JSON Representation</span></span>
<span data-ttu-id="0ea8d-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0ea8d-121">Here is a JSON representation of the resource.</span></span>
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






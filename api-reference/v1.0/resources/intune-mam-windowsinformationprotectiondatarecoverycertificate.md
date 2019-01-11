---
title: Tipo de recurso windowsInformationProtectionDataRecoveryCertificate
description: Certificado de recuperación de datos de Windows Information Protection
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 72edbdc16b2d84a2df6a4582bba12bab2feaa04c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27821066"
---
# <a name="windowsinformationprotectiondatarecoverycertificate-resource-type"></a><span data-ttu-id="59fd6-103">Tipo de recurso windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="59fd6-103">windowsInformationProtectionDataRecoveryCertificate resource type</span></span>

> <span data-ttu-id="59fd6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="59fd6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="59fd6-105">Certificado de recuperación de datos de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="59fd6-105">Windows Information Protection DataRecoveryCertificate</span></span>
## <a name="properties"></a><span data-ttu-id="59fd6-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="59fd6-106">Properties</span></span>
|<span data-ttu-id="59fd6-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="59fd6-107">Property</span></span>|<span data-ttu-id="59fd6-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="59fd6-108">Type</span></span>|<span data-ttu-id="59fd6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="59fd6-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="59fd6-110">subjectName</span><span class="sxs-lookup"><span data-stu-id="59fd6-110">subjectName</span></span>|<span data-ttu-id="59fd6-111">cadena</span><span class="sxs-lookup"><span data-stu-id="59fd6-111">String</span></span>|<span data-ttu-id="59fd6-112">Nombre de asunto del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="59fd6-112">Data recovery Certificate subject name</span></span>|
|<span data-ttu-id="59fd6-113">descripción</span><span class="sxs-lookup"><span data-stu-id="59fd6-113">description</span></span>|<span data-ttu-id="59fd6-114">cadena</span><span class="sxs-lookup"><span data-stu-id="59fd6-114">String</span></span>|<span data-ttu-id="59fd6-115">Descripción del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="59fd6-115">Data recovery Certificate description</span></span>|
|<span data-ttu-id="59fd6-116">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="59fd6-116">expirationDateTime</span></span>|<span data-ttu-id="59fd6-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="59fd6-117">DateTimeOffset</span></span>|<span data-ttu-id="59fd6-118">Fecha y hora de expiración del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="59fd6-118">Data recovery Certificate expiration datetime</span></span>|
|<span data-ttu-id="59fd6-119">certificado</span><span class="sxs-lookup"><span data-stu-id="59fd6-119">certificate</span></span>|<span data-ttu-id="59fd6-120">Binario</span><span class="sxs-lookup"><span data-stu-id="59fd6-120">Binary</span></span>|<span data-ttu-id="59fd6-121">Certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="59fd6-121">Data recovery Certificate</span></span>|

## <a name="relationships"></a><span data-ttu-id="59fd6-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="59fd6-122">Relationships</span></span>
<span data-ttu-id="59fd6-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="59fd6-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="59fd6-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="59fd6-124">JSON Representation</span></span>
<span data-ttu-id="59fd6-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="59fd6-125">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
  "subjectName": "String",
  "description": "String",
  "expirationDateTime": "String (timestamp)",
  "certificate": "binary"
}
```




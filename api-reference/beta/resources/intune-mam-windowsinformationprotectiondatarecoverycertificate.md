---
title: Tipo de recurso windowsInformationProtectionDataRecoveryCertificate
description: Certificado de recuperación de datos de Windows Information Protection
ms.openlocfilehash: bbc6ae8e4607e5992ac9dd23fa1eb67e51d1ecd4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084793"
---
# <a name="windowsinformationprotectiondatarecoverycertificate-resource-type"></a><span data-ttu-id="15800-103">Tipo de recurso windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="15800-103">windowsInformationProtectionDataRecoveryCertificate resource type</span></span>

> <span data-ttu-id="15800-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="15800-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="15800-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="15800-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="15800-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="15800-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="15800-107">Certificado de recuperación de datos de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="15800-107">Windows Information Protection DataRecoveryCertificate</span></span>
## <a name="properties"></a><span data-ttu-id="15800-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15800-108">Properties</span></span>
|<span data-ttu-id="15800-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="15800-109">Property</span></span>|<span data-ttu-id="15800-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="15800-110">Type</span></span>|<span data-ttu-id="15800-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="15800-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="15800-112">subjectName</span><span class="sxs-lookup"><span data-stu-id="15800-112">subjectName</span></span>|<span data-ttu-id="15800-113">cadena</span><span class="sxs-lookup"><span data-stu-id="15800-113">String</span></span>|<span data-ttu-id="15800-114">Nombre de asunto del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="15800-114">Data recovery Certificate subject name</span></span>|
|<span data-ttu-id="15800-115">descripción</span><span class="sxs-lookup"><span data-stu-id="15800-115">description</span></span>|<span data-ttu-id="15800-116">cadena</span><span class="sxs-lookup"><span data-stu-id="15800-116">String</span></span>|<span data-ttu-id="15800-117">Descripción del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="15800-117">Data recovery Certificate description</span></span>|
|<span data-ttu-id="15800-118">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="15800-118">expirationDateTime</span></span>|<span data-ttu-id="15800-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="15800-119">DateTimeOffset</span></span>|<span data-ttu-id="15800-120">Fecha y hora de expiración del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="15800-120">Data recovery Certificate expiration datetime</span></span>|
|<span data-ttu-id="15800-121">certificado</span><span class="sxs-lookup"><span data-stu-id="15800-121">certificate</span></span>|<span data-ttu-id="15800-122">Binario</span><span class="sxs-lookup"><span data-stu-id="15800-122">Binary</span></span>|<span data-ttu-id="15800-123">Certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="15800-123">Data recovery Certificate</span></span>|

## <a name="relationships"></a><span data-ttu-id="15800-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="15800-124">Relationships</span></span>
<span data-ttu-id="15800-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="15800-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="15800-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="15800-126">JSON Representation</span></span>
<span data-ttu-id="15800-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="15800-127">Here is a JSON representation of the resource.</span></span>
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





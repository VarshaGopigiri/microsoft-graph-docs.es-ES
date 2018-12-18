---
title: Tipo de recurso windowsInformationProtectionDataRecoveryCertificate
description: Certificado de recuperación de datos de Windows Information Protection
author: tfitzmac
ms.openlocfilehash: a66c1eeae6d405aa8d0546ac0143e2a8b3404231
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27361666"
---
# <a name="windowsinformationprotectiondatarecoverycertificate-resource-type"></a><span data-ttu-id="e5e02-103">Tipo de recurso windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="e5e02-103">windowsInformationProtectionDataRecoveryCertificate resource type</span></span>

> <span data-ttu-id="e5e02-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e5e02-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e5e02-105">Certificado de recuperación de datos de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="e5e02-105">Windows Information Protection DataRecoveryCertificate</span></span>
## <a name="properties"></a><span data-ttu-id="e5e02-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e5e02-106">Properties</span></span>
|<span data-ttu-id="e5e02-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e5e02-107">Property</span></span>|<span data-ttu-id="e5e02-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5e02-108">Type</span></span>|<span data-ttu-id="e5e02-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5e02-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e5e02-110">subjectName</span><span class="sxs-lookup"><span data-stu-id="e5e02-110">subjectName</span></span>|<span data-ttu-id="e5e02-111">cadena</span><span class="sxs-lookup"><span data-stu-id="e5e02-111">String</span></span>|<span data-ttu-id="e5e02-112">Nombre de asunto del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="e5e02-112">Data recovery Certificate subject name</span></span>|
|<span data-ttu-id="e5e02-113">descripción</span><span class="sxs-lookup"><span data-stu-id="e5e02-113">description</span></span>|<span data-ttu-id="e5e02-114">cadena</span><span class="sxs-lookup"><span data-stu-id="e5e02-114">String</span></span>|<span data-ttu-id="e5e02-115">Descripción del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="e5e02-115">Data recovery Certificate description</span></span>|
|<span data-ttu-id="e5e02-116">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="e5e02-116">expirationDateTime</span></span>|<span data-ttu-id="e5e02-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e5e02-117">DateTimeOffset</span></span>|<span data-ttu-id="e5e02-118">Fecha y hora de expiración del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="e5e02-118">Data recovery Certificate expiration datetime</span></span>|
|<span data-ttu-id="e5e02-119">certificado</span><span class="sxs-lookup"><span data-stu-id="e5e02-119">certificate</span></span>|<span data-ttu-id="e5e02-120">Binario</span><span class="sxs-lookup"><span data-stu-id="e5e02-120">Binary</span></span>|<span data-ttu-id="e5e02-121">Certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="e5e02-121">Data recovery Certificate</span></span>|

## <a name="relationships"></a><span data-ttu-id="e5e02-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e5e02-122">Relationships</span></span>
<span data-ttu-id="e5e02-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e5e02-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e5e02-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e5e02-124">JSON Representation</span></span>
<span data-ttu-id="e5e02-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e5e02-125">Here is a JSON representation of the resource.</span></span>
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




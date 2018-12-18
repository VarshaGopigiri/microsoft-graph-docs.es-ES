---
title: tipo de recurso bitLockerRecoveryOptions
description: Opciones de recuperación de BitLocker.
author: tfitzmac
ms.openlocfilehash: c85ce3111ed88ce8e8bf54c98d5fd3122571a0be
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27310608"
---
# <a name="bitlockerrecoveryoptions-resource-type"></a><span data-ttu-id="46d72-103">tipo de recurso bitLockerRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="46d72-103">bitLockerRecoveryOptions resource type</span></span>

> <span data-ttu-id="46d72-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="46d72-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="46d72-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="46d72-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="46d72-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="46d72-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="46d72-107">Opciones de recuperación de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="46d72-107">BitLocker Recovery Options.</span></span>
## <a name="properties"></a><span data-ttu-id="46d72-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="46d72-108">Properties</span></span>
|<span data-ttu-id="46d72-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="46d72-109">Property</span></span>|<span data-ttu-id="46d72-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="46d72-110">Type</span></span>|<span data-ttu-id="46d72-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="46d72-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="46d72-112">blockDataRecoveryAgent</span><span class="sxs-lookup"><span data-stu-id="46d72-112">blockDataRecoveryAgent</span></span>|<span data-ttu-id="46d72-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="46d72-113">Boolean</span></span>|<span data-ttu-id="46d72-114">Indica si se debe bloquear el agente de recuperación de datos basada en certificados.</span><span class="sxs-lookup"><span data-stu-id="46d72-114">Indicates whether to block certificate-based data recovery agent.</span></span>|
|<span data-ttu-id="46d72-115">recoveryPasswordUsage</span><span class="sxs-lookup"><span data-stu-id="46d72-115">recoveryPasswordUsage</span></span>|[<span data-ttu-id="46d72-116">configurationUsage</span><span class="sxs-lookup"><span data-stu-id="46d72-116">configurationUsage</span></span>](../resources/intune-deviceconfig-configurationusage.md)|<span data-ttu-id="46d72-117">Indica si los usuarios están permitidos o necesarios para generar una contraseña de recuperación de 48 dígitos para fijo o disco de sistema.</span><span class="sxs-lookup"><span data-stu-id="46d72-117">Indicates whether users are allowed or required to generate a 48-digit recovery password for fixed or system disk.</span></span> <span data-ttu-id="46d72-118">Los valores posibles son: `blocked`, `required` y `allowed`.</span><span class="sxs-lookup"><span data-stu-id="46d72-118">Possible values are: `blocked`, `required`, `allowed`.</span></span>|
|<span data-ttu-id="46d72-119">recoveryKeyUsage</span><span class="sxs-lookup"><span data-stu-id="46d72-119">recoveryKeyUsage</span></span>|[<span data-ttu-id="46d72-120">configurationUsage</span><span class="sxs-lookup"><span data-stu-id="46d72-120">configurationUsage</span></span>](../resources/intune-deviceconfig-configurationusage.md)|<span data-ttu-id="46d72-121">Indica si los usuarios están permitidos o necesarios para generar una clave de recuperación de 256 bits para fijo o disco de sistema.</span><span class="sxs-lookup"><span data-stu-id="46d72-121">Indicates whether users are allowed or required to generate a 256-bit recovery key for fixed or system disk.</span></span> <span data-ttu-id="46d72-122">Los valores posibles son: `blocked`, `required` y `allowed`.</span><span class="sxs-lookup"><span data-stu-id="46d72-122">Possible values are: `blocked`, `required`, `allowed`.</span></span>|
|<span data-ttu-id="46d72-123">hideRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="46d72-123">hideRecoveryOptions</span></span>|<span data-ttu-id="46d72-124">Boolean</span><span class="sxs-lookup"><span data-stu-id="46d72-124">Boolean</span></span>|<span data-ttu-id="46d72-125">Indica si se debe o no permitir que muestra las opciones de recuperación en el Asistente para la instalación de BitLocker para fijo o disco de sistema.</span><span class="sxs-lookup"><span data-stu-id="46d72-125">Indicates whether or not to allow showing recovery options in BitLocker Setup Wizard for fixed or system disk.</span></span>|
|<span data-ttu-id="46d72-126">enableRecoveryInformationSaveToStore</span><span class="sxs-lookup"><span data-stu-id="46d72-126">enableRecoveryInformationSaveToStore</span></span>|<span data-ttu-id="46d72-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="46d72-127">Boolean</span></span>|<span data-ttu-id="46d72-128">Indica si se debe o no permitir la información de recuperación de BitLocker almacenar en AD DS.</span><span class="sxs-lookup"><span data-stu-id="46d72-128">Indicates whether or not to allow BitLocker recovery information to store in AD DS.</span></span>|
|<span data-ttu-id="46d72-129">recoveryInformationToStore</span><span class="sxs-lookup"><span data-stu-id="46d72-129">recoveryInformationToStore</span></span>|[<span data-ttu-id="46d72-130">bitLockerRecoveryInformationType</span><span class="sxs-lookup"><span data-stu-id="46d72-130">bitLockerRecoveryInformationType</span></span>](../resources/intune-deviceconfig-bitlockerrecoveryinformationtype.md)|<span data-ttu-id="46d72-131">Configurar qué elementos de información de recuperación de BitLocker se almacenan en AD DS.</span><span class="sxs-lookup"><span data-stu-id="46d72-131">Configure what pieces of BitLocker recovery information are stored to AD DS.</span></span> <span data-ttu-id="46d72-132">Los valores posibles son: `passwordAndKey` y `passwordOnly`.</span><span class="sxs-lookup"><span data-stu-id="46d72-132">Possible values are: `passwordAndKey`, `passwordOnly`.</span></span>|
|<span data-ttu-id="46d72-133">enableBitLockerAfterRecoveryInformationToStore</span><span class="sxs-lookup"><span data-stu-id="46d72-133">enableBitLockerAfterRecoveryInformationToStore</span></span>|<span data-ttu-id="46d72-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="46d72-134">Boolean</span></span>|<span data-ttu-id="46d72-135">Indica si se va a habilitar BitLocker hasta que se almacena información de recuperación en AD DS o no.</span><span class="sxs-lookup"><span data-stu-id="46d72-135">Indicates whether or not to enable BitLocker until recovery information is stored in AD DS.</span></span>|

## <a name="relationships"></a><span data-ttu-id="46d72-136">Relaciones</span><span class="sxs-lookup"><span data-stu-id="46d72-136">Relationships</span></span>
<span data-ttu-id="46d72-137">Ninguna</span><span class="sxs-lookup"><span data-stu-id="46d72-137">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="46d72-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="46d72-138">JSON Representation</span></span>
<span data-ttu-id="46d72-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="46d72-139">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.bitLockerRecoveryOptions"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.bitLockerRecoveryOptions",
  "blockDataRecoveryAgent": true,
  "recoveryPasswordUsage": "String",
  "recoveryKeyUsage": "String",
  "hideRecoveryOptions": true,
  "enableRecoveryInformationSaveToStore": true,
  "recoveryInformationToStore": "String",
  "enableBitLockerAfterRecoveryInformationToStore": true
}
```






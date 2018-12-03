---
title: tipo de recurso bitLockerFixedDrivePolicy
description: Rol fijo de directivas de unidad BitLocker.
ms.openlocfilehash: c29f736515333fcdbeca8c18017b9403f845de9e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086978"
---
# <a name="bitlockerfixeddrivepolicy-resource-type"></a><span data-ttu-id="bc874-103">tipo de recurso bitLockerFixedDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="bc874-103">bitLockerFixedDrivePolicy resource type</span></span>

> <span data-ttu-id="bc874-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bc874-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bc874-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bc874-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bc874-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bc874-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bc874-107">Rol fijo de directivas de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="bc874-107">BitLocker Fixed Drive Policies.</span></span>
## <a name="properties"></a><span data-ttu-id="bc874-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bc874-108">Properties</span></span>
|<span data-ttu-id="bc874-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bc874-109">Property</span></span>|<span data-ttu-id="bc874-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc874-110">Type</span></span>|<span data-ttu-id="bc874-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc874-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bc874-112">encryptionMethod</span><span class="sxs-lookup"><span data-stu-id="bc874-112">encryptionMethod</span></span>|[<span data-ttu-id="bc874-113">bitLockerEncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="bc874-113">bitLockerEncryptionMethod</span></span>](../resources/intune-deviceconfig-bitlockerencryptionmethod.md)|<span data-ttu-id="bc874-114">Seleccione el método de cifrado para unidades de disco duro.</span><span class="sxs-lookup"><span data-stu-id="bc874-114">Select the encryption method for fixed drives.</span></span> <span data-ttu-id="bc874-115">Los valores posibles son: `aesCbc128`, `aesCbc256`, `xtsAes128` y `xtsAes256`.</span><span class="sxs-lookup"><span data-stu-id="bc874-115">Possible values are: `aesCbc128`, `aesCbc256`, `xtsAes128`, `xtsAes256`.</span></span>|
|<span data-ttu-id="bc874-116">requireEncryptionForWriteAccess</span><span class="sxs-lookup"><span data-stu-id="bc874-116">requireEncryptionForWriteAccess</span></span>|<span data-ttu-id="bc874-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="bc874-117">Boolean</span></span>|<span data-ttu-id="bc874-118">Esta configuración de directiva determina si la protección de BitLocker es necesaria para unidades de datos fijas que se puede escribir en un equipo.</span><span class="sxs-lookup"><span data-stu-id="bc874-118">This policy setting determines whether BitLocker protection is required for fixed data drives to be writable on a computer.</span></span>|
|<span data-ttu-id="bc874-119">recoveryOptions</span><span class="sxs-lookup"><span data-stu-id="bc874-119">recoveryOptions</span></span>|[<span data-ttu-id="bc874-120">bitLockerRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="bc874-120">bitLockerRecoveryOptions</span></span>](../resources/intune-deviceconfig-bitlockerrecoveryoptions.md)|<span data-ttu-id="bc874-121">Esta configuración de directiva permite controlar cómo protegida por BitLocker fijos datos se recuperan las unidades en ausencia de las credenciales necesarias.</span><span class="sxs-lookup"><span data-stu-id="bc874-121">This policy setting allows you to control how BitLocker-protected fixed data drives are recovered in the absence of the required credentials.</span></span> <span data-ttu-id="bc874-122">Esta configuración de directiva se aplica al activar BitLocker.</span><span class="sxs-lookup"><span data-stu-id="bc874-122">This policy setting is applied when you turn on BitLocker.</span></span>|

## <a name="relationships"></a><span data-ttu-id="bc874-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bc874-123">Relationships</span></span>
<span data-ttu-id="bc874-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="bc874-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="bc874-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bc874-125">JSON Representation</span></span>
<span data-ttu-id="bc874-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bc874-126">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.bitLockerFixedDrivePolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.bitLockerFixedDrivePolicy",
  "encryptionMethod": "String",
  "requireEncryptionForWriteAccess": true,
  "recoveryOptions": {
    "@odata.type": "microsoft.graph.bitLockerRecoveryOptions",
    "blockDataRecoveryAgent": true,
    "recoveryPasswordUsage": "String",
    "recoveryKeyUsage": "String",
    "hideRecoveryOptions": true,
    "enableRecoveryInformationSaveToStore": true,
    "recoveryInformationToStore": "String",
    "enableBitLockerAfterRecoveryInformationToStore": true
  }
}
```





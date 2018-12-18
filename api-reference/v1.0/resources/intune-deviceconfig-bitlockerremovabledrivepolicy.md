---
title: Tipo de recurso bitLockerRemovableDrivePolicy
description: Directivas de unidad extraíble de BitLocker
author: tfitzmac
ms.openlocfilehash: 77f4161f7cd7aef61ee257ba665ab19e03ff4dc8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27340015"
---
# <a name="bitlockerremovabledrivepolicy-resource-type"></a><span data-ttu-id="e2417-103">Tipo de recurso bitLockerRemovableDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="e2417-103">bitLockerRemovableDrivePolicy resource type</span></span>

> <span data-ttu-id="e2417-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e2417-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e2417-105">Directivas de unidad extraíble de BitLocker</span><span class="sxs-lookup"><span data-stu-id="e2417-105">BitLocker Removable Drive Policies.</span></span>
## <a name="properties"></a><span data-ttu-id="e2417-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e2417-106">Properties</span></span>
|<span data-ttu-id="e2417-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e2417-107">Property</span></span>|<span data-ttu-id="e2417-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2417-108">Type</span></span>|<span data-ttu-id="e2417-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2417-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e2417-110">encryptionMethod</span><span class="sxs-lookup"><span data-stu-id="e2417-110">encryptionMethod</span></span>|[<span data-ttu-id="e2417-111">bitLockerEncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="e2417-111">bitLockerEncryptionMethod</span></span>](../resources/intune-deviceconfig-bitlockerencryptionmethod.md)|<span data-ttu-id="e2417-112">Seleccione el método de cifrado para las unidades extraíbles.</span><span class="sxs-lookup"><span data-stu-id="e2417-112">Select the encryption method for removable  drives.</span></span> <span data-ttu-id="e2417-113">Los valores posibles son: `aesCbc128`, `aesCbc256`, `xtsAes128` y `xtsAes256`.</span><span class="sxs-lookup"><span data-stu-id="e2417-113">Possible values are: `aesCbc128`, `aesCbc256`, `xtsAes128`, `xtsAes256`.</span></span>|
|<span data-ttu-id="e2417-114">requireEncryptionForWriteAccess</span><span class="sxs-lookup"><span data-stu-id="e2417-114">requireEncryptionForWriteAccess</span></span>|<span data-ttu-id="e2417-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="e2417-115">Boolean</span></span>|<span data-ttu-id="e2417-116">Indica si se bloquea el acceso de escritura a dispositivos configurados en otra organización.</span><span class="sxs-lookup"><span data-stu-id="e2417-116">Indicates whether to block write access to devices configured in another organization.</span></span>  <span data-ttu-id="e2417-117">Si requireEncryptionForWriteAccess es false, este valor no se aplica.</span><span class="sxs-lookup"><span data-stu-id="e2417-117">If requireEncryptionForWriteAccess is false, this value does not affect.</span></span>|
|<span data-ttu-id="e2417-118">blockCrossOrganizationWriteAccess</span><span class="sxs-lookup"><span data-stu-id="e2417-118">blockCrossOrganizationWriteAccess</span></span>|<span data-ttu-id="e2417-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="e2417-119">Boolean</span></span>|<span data-ttu-id="e2417-120">Esta configuración de directiva determina si es necesaria la protección BitLocker para que se pueda escribir en las unidades de datos extraíbles en un equipo.</span><span class="sxs-lookup"><span data-stu-id="e2417-120">This policy setting determines whether BitLocker protection is required for removable data drives to be writable on a computer.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e2417-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e2417-121">Relationships</span></span>
<span data-ttu-id="e2417-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e2417-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e2417-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e2417-123">JSON Representation</span></span>
<span data-ttu-id="e2417-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e2417-124">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.bitLockerRemovableDrivePolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.bitLockerRemovableDrivePolicy",
  "encryptionMethod": "String",
  "requireEncryptionForWriteAccess": true,
  "blockCrossOrganizationWriteAccess": true
}
```




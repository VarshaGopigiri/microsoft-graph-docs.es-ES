---
title: Tipo de recurso bitLockerRemovableDrivePolicy
description: Directivas de unidad extraíble de BitLocker
author: tfitzmac
ms.openlocfilehash: 15de11384195350b455cd4696a260aedf1de7a26
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27354038"
---
# <a name="bitlockerremovabledrivepolicy-resource-type"></a><span data-ttu-id="e6ed8-103">Tipo de recurso bitLockerRemovableDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="e6ed8-103">bitLockerRemovableDrivePolicy resource type</span></span>

> <span data-ttu-id="e6ed8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e6ed8-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e6ed8-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e6ed8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e6ed8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e6ed8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e6ed8-107">Directivas de unidad extraíble de BitLocker</span><span class="sxs-lookup"><span data-stu-id="e6ed8-107">BitLocker Removable Drive Policies.</span></span>
## <a name="properties"></a><span data-ttu-id="e6ed8-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e6ed8-108">Properties</span></span>
|<span data-ttu-id="e6ed8-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e6ed8-109">Property</span></span>|<span data-ttu-id="e6ed8-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6ed8-110">Type</span></span>|<span data-ttu-id="e6ed8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6ed8-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e6ed8-112">encryptionMethod</span><span class="sxs-lookup"><span data-stu-id="e6ed8-112">encryptionMethod</span></span>|[<span data-ttu-id="e6ed8-113">bitLockerEncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="e6ed8-113">bitLockerEncryptionMethod</span></span>](../resources/intune-deviceconfig-bitlockerencryptionmethod.md)|<span data-ttu-id="e6ed8-114">Seleccione el método de cifrado para las unidades extraíbles.</span><span class="sxs-lookup"><span data-stu-id="e6ed8-114">Select the encryption method for removable  drives.</span></span> <span data-ttu-id="e6ed8-115">Los valores posibles son: `aesCbc128`, `aesCbc256`, `xtsAes128` y `xtsAes256`.</span><span class="sxs-lookup"><span data-stu-id="e6ed8-115">Possible values are: `aesCbc128`, `aesCbc256`, `xtsAes128`, `xtsAes256`.</span></span>|
|<span data-ttu-id="e6ed8-116">requireEncryptionForWriteAccess</span><span class="sxs-lookup"><span data-stu-id="e6ed8-116">requireEncryptionForWriteAccess</span></span>|<span data-ttu-id="e6ed8-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="e6ed8-117">Boolean</span></span>|<span data-ttu-id="e6ed8-118">Indica si se bloquea el acceso de escritura a dispositivos configurados en otra organización.</span><span class="sxs-lookup"><span data-stu-id="e6ed8-118">Indicates whether to block write access to devices configured in another organization.</span></span>  <span data-ttu-id="e6ed8-119">Si requireEncryptionForWriteAccess es false, este valor no se aplica.</span><span class="sxs-lookup"><span data-stu-id="e6ed8-119">If requireEncryptionForWriteAccess is false, this value does not affect.</span></span>|
|<span data-ttu-id="e6ed8-120">blockCrossOrganizationWriteAccess</span><span class="sxs-lookup"><span data-stu-id="e6ed8-120">blockCrossOrganizationWriteAccess</span></span>|<span data-ttu-id="e6ed8-121">Booleano</span><span class="sxs-lookup"><span data-stu-id="e6ed8-121">Boolean</span></span>|<span data-ttu-id="e6ed8-122">Esta configuración de directiva determina si es necesaria la protección BitLocker para que se pueda escribir en las unidades de datos extraíbles en un equipo.</span><span class="sxs-lookup"><span data-stu-id="e6ed8-122">This policy setting determines whether BitLocker protection is required for removable data drives to be writable on a computer.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e6ed8-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e6ed8-123">Relationships</span></span>
<span data-ttu-id="e6ed8-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e6ed8-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e6ed8-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e6ed8-125">JSON Representation</span></span>
<span data-ttu-id="e6ed8-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e6ed8-126">Here is a JSON representation of the resource.</span></span>
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






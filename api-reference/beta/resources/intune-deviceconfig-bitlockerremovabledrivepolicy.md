---
title: Tipo de recurso bitLockerRemovableDrivePolicy
description: Directivas de unidad extraíble de BitLocker
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b5c7d0d7fc188ee0c150bb7d0ac2143639ca32ae
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27873986"
---
# <a name="bitlockerremovabledrivepolicy-resource-type"></a><span data-ttu-id="5286f-103">Tipo de recurso bitLockerRemovableDrivePolicy</span><span class="sxs-lookup"><span data-stu-id="5286f-103">bitLockerRemovableDrivePolicy resource type</span></span>

> <span data-ttu-id="5286f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5286f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5286f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5286f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5286f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5286f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5286f-107">Directivas de unidad extraíble de BitLocker</span><span class="sxs-lookup"><span data-stu-id="5286f-107">BitLocker Removable Drive Policies.</span></span>
## <a name="properties"></a><span data-ttu-id="5286f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5286f-108">Properties</span></span>
|<span data-ttu-id="5286f-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5286f-109">Property</span></span>|<span data-ttu-id="5286f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="5286f-110">Type</span></span>|<span data-ttu-id="5286f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5286f-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5286f-112">encryptionMethod</span><span class="sxs-lookup"><span data-stu-id="5286f-112">encryptionMethod</span></span>|[<span data-ttu-id="5286f-113">bitLockerEncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="5286f-113">bitLockerEncryptionMethod</span></span>](../resources/intune-deviceconfig-bitlockerencryptionmethod.md)|<span data-ttu-id="5286f-114">Seleccione el método de cifrado para las unidades extraíbles.</span><span class="sxs-lookup"><span data-stu-id="5286f-114">Select the encryption method for removable  drives.</span></span> <span data-ttu-id="5286f-115">Los valores posibles son: `aesCbc128`, `aesCbc256`, `xtsAes128` y `xtsAes256`.</span><span class="sxs-lookup"><span data-stu-id="5286f-115">Possible values are: `aesCbc128`, `aesCbc256`, `xtsAes128`, `xtsAes256`.</span></span>|
|<span data-ttu-id="5286f-116">requireEncryptionForWriteAccess</span><span class="sxs-lookup"><span data-stu-id="5286f-116">requireEncryptionForWriteAccess</span></span>|<span data-ttu-id="5286f-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="5286f-117">Boolean</span></span>|<span data-ttu-id="5286f-118">Indica si se bloquea el acceso de escritura a dispositivos configurados en otra organización.</span><span class="sxs-lookup"><span data-stu-id="5286f-118">Indicates whether to block write access to devices configured in another organization.</span></span>  <span data-ttu-id="5286f-119">Si requireEncryptionForWriteAccess es false, este valor no se aplica.</span><span class="sxs-lookup"><span data-stu-id="5286f-119">If requireEncryptionForWriteAccess is false, this value does not affect.</span></span>|
|<span data-ttu-id="5286f-120">blockCrossOrganizationWriteAccess</span><span class="sxs-lookup"><span data-stu-id="5286f-120">blockCrossOrganizationWriteAccess</span></span>|<span data-ttu-id="5286f-121">Booleano</span><span class="sxs-lookup"><span data-stu-id="5286f-121">Boolean</span></span>|<span data-ttu-id="5286f-122">Esta configuración de directiva determina si es necesaria la protección BitLocker para que se pueda escribir en las unidades de datos extraíbles en un equipo.</span><span class="sxs-lookup"><span data-stu-id="5286f-122">This policy setting determines whether BitLocker protection is required for removable data drives to be writable on a computer.</span></span>|

## <a name="relationships"></a><span data-ttu-id="5286f-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5286f-123">Relationships</span></span>
<span data-ttu-id="5286f-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5286f-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5286f-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5286f-125">JSON Representation</span></span>
<span data-ttu-id="5286f-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5286f-126">Here is a JSON representation of the resource.</span></span>
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






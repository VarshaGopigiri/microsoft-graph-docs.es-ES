---
title: tipo de recurso sharedAppleDeviceUser
description: Todavía no documentado
ms.openlocfilehash: 79ebc5ae520c1c9b40bffb6a86e95693c52fa1e6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085099"
---
# <a name="sharedappledeviceuser-resource-type"></a><span data-ttu-id="90329-103">tipo de recurso sharedAppleDeviceUser</span><span class="sxs-lookup"><span data-stu-id="90329-103">sharedAppleDeviceUser resource type</span></span>

> <span data-ttu-id="90329-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="90329-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="90329-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="90329-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="90329-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="90329-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="90329-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="90329-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="90329-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="90329-108">Properties</span></span>
|<span data-ttu-id="90329-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="90329-109">Property</span></span>|<span data-ttu-id="90329-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="90329-110">Type</span></span>|<span data-ttu-id="90329-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="90329-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="90329-112">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="90329-112">userPrincipalName</span></span>|<span data-ttu-id="90329-113">String</span><span class="sxs-lookup"><span data-stu-id="90329-113">String</span></span>|<span data-ttu-id="90329-114">Nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="90329-114">User name</span></span>|
|<span data-ttu-id="90329-115">dataToSync</span><span class="sxs-lookup"><span data-stu-id="90329-115">dataToSync</span></span>|<span data-ttu-id="90329-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="90329-116">Boolean</span></span>|<span data-ttu-id="90329-117">Datos para la sincronización</span><span class="sxs-lookup"><span data-stu-id="90329-117">Data to sync</span></span>|
|<span data-ttu-id="90329-118">dataQuota</span><span class="sxs-lookup"><span data-stu-id="90329-118">dataQuota</span></span>|<span data-ttu-id="90329-119">Int64</span><span class="sxs-lookup"><span data-stu-id="90329-119">Int64</span></span>|<span data-ttu-id="90329-120">Cuota de datos</span><span class="sxs-lookup"><span data-stu-id="90329-120">Data quota</span></span>|
|<span data-ttu-id="90329-121">dataUsed</span><span class="sxs-lookup"><span data-stu-id="90329-121">dataUsed</span></span>|<span data-ttu-id="90329-122">Int64</span><span class="sxs-lookup"><span data-stu-id="90329-122">Int64</span></span>|<span data-ttu-id="90329-123">Cuota de datos</span><span class="sxs-lookup"><span data-stu-id="90329-123">Data quota</span></span>|

## <a name="relationships"></a><span data-ttu-id="90329-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="90329-124">Relationships</span></span>
<span data-ttu-id="90329-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="90329-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="90329-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="90329-126">JSON Representation</span></span>
<span data-ttu-id="90329-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="90329-127">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.sharedAppleDeviceUser"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.sharedAppleDeviceUser",
  "userPrincipalName": "String",
  "dataToSync": true,
  "dataQuota": 1024,
  "dataUsed": 1024
}
```






---
title: tipo de recurso sharedAppleDeviceUser
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 5ee74080b95328cf55813dc628ee7a517dff08e8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27806856"
---
# <a name="sharedappledeviceuser-resource-type"></a><span data-ttu-id="bf7e0-103">tipo de recurso sharedAppleDeviceUser</span><span class="sxs-lookup"><span data-stu-id="bf7e0-103">sharedAppleDeviceUser resource type</span></span>

> <span data-ttu-id="bf7e0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bf7e0-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bf7e0-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bf7e0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bf7e0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bf7e0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bf7e0-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="bf7e0-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="bf7e0-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf7e0-108">Properties</span></span>
|<span data-ttu-id="bf7e0-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bf7e0-109">Property</span></span>|<span data-ttu-id="bf7e0-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf7e0-110">Type</span></span>|<span data-ttu-id="bf7e0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf7e0-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bf7e0-112">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bf7e0-112">userPrincipalName</span></span>|<span data-ttu-id="bf7e0-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="bf7e0-113">String</span></span>|<span data-ttu-id="bf7e0-114">Nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="bf7e0-114">User name</span></span>|
|<span data-ttu-id="bf7e0-115">dataToSync</span><span class="sxs-lookup"><span data-stu-id="bf7e0-115">dataToSync</span></span>|<span data-ttu-id="bf7e0-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="bf7e0-116">Boolean</span></span>|<span data-ttu-id="bf7e0-117">Datos para la sincronización</span><span class="sxs-lookup"><span data-stu-id="bf7e0-117">Data to sync</span></span>|
|<span data-ttu-id="bf7e0-118">dataQuota</span><span class="sxs-lookup"><span data-stu-id="bf7e0-118">dataQuota</span></span>|<span data-ttu-id="bf7e0-119">Int64</span><span class="sxs-lookup"><span data-stu-id="bf7e0-119">Int64</span></span>|<span data-ttu-id="bf7e0-120">Cuota de datos</span><span class="sxs-lookup"><span data-stu-id="bf7e0-120">Data quota</span></span>|
|<span data-ttu-id="bf7e0-121">dataUsed</span><span class="sxs-lookup"><span data-stu-id="bf7e0-121">dataUsed</span></span>|<span data-ttu-id="bf7e0-122">Int64</span><span class="sxs-lookup"><span data-stu-id="bf7e0-122">Int64</span></span>|<span data-ttu-id="bf7e0-123">Cuota de datos</span><span class="sxs-lookup"><span data-stu-id="bf7e0-123">Data quota</span></span>|

## <a name="relationships"></a><span data-ttu-id="bf7e0-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bf7e0-124">Relationships</span></span>
<span data-ttu-id="bf7e0-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="bf7e0-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="bf7e0-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bf7e0-126">JSON Representation</span></span>
<span data-ttu-id="bf7e0-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bf7e0-127">Here is a JSON representation of the resource.</span></span>
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






---
title: tipo de recurso deviceManagementUserRightsLocalUserOrGroup
description: Representa información de un usuario local o el grupo que se utiliza para establecer los derechos de usuario.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: d795e2b259c71612b1d0720796b6ad76145bb36d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885746"
---
# <a name="devicemanagementuserrightslocaluserorgroup-resource-type"></a><span data-ttu-id="86022-103">tipo de recurso deviceManagementUserRightsLocalUserOrGroup</span><span class="sxs-lookup"><span data-stu-id="86022-103">deviceManagementUserRightsLocalUserOrGroup resource type</span></span>

> <span data-ttu-id="86022-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="86022-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="86022-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="86022-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="86022-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="86022-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="86022-107">Representa información de un usuario local o el grupo que se utiliza para establecer los derechos de usuario.</span><span class="sxs-lookup"><span data-stu-id="86022-107">Represents information for a local user or group used for user rights setting.</span></span>
## <a name="properties"></a><span data-ttu-id="86022-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="86022-108">Properties</span></span>
|<span data-ttu-id="86022-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="86022-109">Property</span></span>|<span data-ttu-id="86022-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="86022-110">Type</span></span>|<span data-ttu-id="86022-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="86022-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="86022-112">name</span><span class="sxs-lookup"><span data-stu-id="86022-112">name</span></span>|<span data-ttu-id="86022-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="86022-113">String</span></span>|<span data-ttu-id="86022-114">El nombre de este usuario o grupo local.</span><span class="sxs-lookup"><span data-stu-id="86022-114">The name of this local user or group.</span></span>|
|<span data-ttu-id="86022-115">descripción</span><span class="sxs-lookup"><span data-stu-id="86022-115">description</span></span>|<span data-ttu-id="86022-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="86022-116">String</span></span>|<span data-ttu-id="86022-117">Descripción del Administrador de este usuario o grupo local.</span><span class="sxs-lookup"><span data-stu-id="86022-117">Admin’s description of this local user or group.</span></span>|
|<span data-ttu-id="86022-118">securityIdentifier</span><span class="sxs-lookup"><span data-stu-id="86022-118">securityIdentifier</span></span>|<span data-ttu-id="86022-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="86022-119">String</span></span>|<span data-ttu-id="86022-120">El identificador de seguridad de este usuario o grupo local (por ejemplo, \* S-1-5-32-544).</span><span class="sxs-lookup"><span data-stu-id="86022-120">The security identifier of this local user or group (e.g. \*S-1-5-32-544).</span></span>|

## <a name="relationships"></a><span data-ttu-id="86022-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="86022-121">Relationships</span></span>
<span data-ttu-id="86022-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="86022-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="86022-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="86022-123">JSON Representation</span></span>
<span data-ttu-id="86022-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="86022-124">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
  "name": "String",
  "description": "String",
  "securityIdentifier": "String"
}
```






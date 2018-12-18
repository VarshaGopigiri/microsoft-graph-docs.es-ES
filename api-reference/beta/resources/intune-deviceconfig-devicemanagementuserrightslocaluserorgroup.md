---
title: tipo de recurso deviceManagementUserRightsLocalUserOrGroup
description: Representa información de un usuario local o el grupo que se utiliza para establecer los derechos de usuario.
author: tfitzmac
ms.openlocfilehash: baabd2f3bb9e3bce44d172cd83f61f57c5c2c98d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27303734"
---
# <a name="devicemanagementuserrightslocaluserorgroup-resource-type"></a><span data-ttu-id="9b88f-103">tipo de recurso deviceManagementUserRightsLocalUserOrGroup</span><span class="sxs-lookup"><span data-stu-id="9b88f-103">deviceManagementUserRightsLocalUserOrGroup resource type</span></span>

> <span data-ttu-id="9b88f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9b88f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9b88f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9b88f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9b88f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9b88f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9b88f-107">Representa información de un usuario local o el grupo que se utiliza para establecer los derechos de usuario.</span><span class="sxs-lookup"><span data-stu-id="9b88f-107">Represents information for a local user or group used for user rights setting.</span></span>
## <a name="properties"></a><span data-ttu-id="9b88f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b88f-108">Properties</span></span>
|<span data-ttu-id="9b88f-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9b88f-109">Property</span></span>|<span data-ttu-id="9b88f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b88f-110">Type</span></span>|<span data-ttu-id="9b88f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b88f-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9b88f-112">name</span><span class="sxs-lookup"><span data-stu-id="9b88f-112">name</span></span>|<span data-ttu-id="9b88f-113">String</span><span class="sxs-lookup"><span data-stu-id="9b88f-113">String</span></span>|<span data-ttu-id="9b88f-114">El nombre de este usuario o grupo local.</span><span class="sxs-lookup"><span data-stu-id="9b88f-114">The name of this local user or group.</span></span>|
|<span data-ttu-id="9b88f-115">descripción</span><span class="sxs-lookup"><span data-stu-id="9b88f-115">description</span></span>|<span data-ttu-id="9b88f-116">String</span><span class="sxs-lookup"><span data-stu-id="9b88f-116">String</span></span>|<span data-ttu-id="9b88f-117">Descripción del Administrador de este usuario o grupo local.</span><span class="sxs-lookup"><span data-stu-id="9b88f-117">Admin’s description of this local user or group.</span></span>|
|<span data-ttu-id="9b88f-118">securityIdentifier</span><span class="sxs-lookup"><span data-stu-id="9b88f-118">securityIdentifier</span></span>|<span data-ttu-id="9b88f-119">String</span><span class="sxs-lookup"><span data-stu-id="9b88f-119">String</span></span>|<span data-ttu-id="9b88f-120">El identificador de seguridad de este usuario o grupo local (por ejemplo, \* S-1-5-32-544).</span><span class="sxs-lookup"><span data-stu-id="9b88f-120">The security identifier of this local user or group (e.g. \*S-1-5-32-544).</span></span>|

## <a name="relationships"></a><span data-ttu-id="9b88f-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9b88f-121">Relationships</span></span>
<span data-ttu-id="9b88f-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9b88f-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="9b88f-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9b88f-123">JSON Representation</span></span>
<span data-ttu-id="9b88f-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9b88f-124">Here is a JSON representation of the resource.</span></span>
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






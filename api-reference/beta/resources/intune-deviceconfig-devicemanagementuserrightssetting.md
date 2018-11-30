---
title: tipo de recurso deviceManagementUserRightsSetting
description: Representa una configuración de permisos de usuario.
ms.openlocfilehash: e657c15a76700ef87283220254937ec685c57784
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088361"
---
# <a name="devicemanagementuserrightssetting-resource-type"></a><span data-ttu-id="dc2a8-103">tipo de recurso deviceManagementUserRightsSetting</span><span class="sxs-lookup"><span data-stu-id="dc2a8-103">deviceManagementUserRightsSetting resource type</span></span>

> <span data-ttu-id="dc2a8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dc2a8-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dc2a8-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dc2a8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="dc2a8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dc2a8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dc2a8-107">Representa una configuración de permisos de usuario.</span><span class="sxs-lookup"><span data-stu-id="dc2a8-107">Represents a user rights setting.</span></span>
## <a name="properties"></a><span data-ttu-id="dc2a8-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc2a8-108">Properties</span></span>
|<span data-ttu-id="dc2a8-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dc2a8-109">Property</span></span>|<span data-ttu-id="dc2a8-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc2a8-110">Type</span></span>|<span data-ttu-id="dc2a8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc2a8-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="dc2a8-112">state</span><span class="sxs-lookup"><span data-stu-id="dc2a8-112">state</span></span>|[<span data-ttu-id="dc2a8-113">stateManagementSetting</span><span class="sxs-lookup"><span data-stu-id="dc2a8-113">stateManagementSetting</span></span>](../resources/intune-deviceconfig-statemanagementsetting.md)|<span data-ttu-id="dc2a8-114">Configuración de los derechos que representa el estado actual de este usuario.</span><span class="sxs-lookup"><span data-stu-id="dc2a8-114">Representing the current state of this user rights setting.</span></span> <span data-ttu-id="dc2a8-115">Los valores posibles son: `notConfigured`, `blocked` y `allowed`.</span><span class="sxs-lookup"><span data-stu-id="dc2a8-115">Possible values are: `notConfigured`, `blocked`, `allowed`.</span></span>|
|<span data-ttu-id="dc2a8-116">localUsersOrGroups</span><span class="sxs-lookup"><span data-stu-id="dc2a8-116">localUsersOrGroups</span></span>|<span data-ttu-id="dc2a8-117">colección de [deviceManagementUserRightsLocalUserOrGroup](../resources/intune-deviceconfig-devicemanagementuserrightslocaluserorgroup.md)</span><span class="sxs-lookup"><span data-stu-id="dc2a8-117">[deviceManagementUserRightsLocalUserOrGroup](../resources/intune-deviceconfig-devicemanagementuserrightslocaluserorgroup.md) collection</span></span>|<span data-ttu-id="dc2a8-118">Que representa una colección de usuarios locales o grupos que se establecerá en el dispositivo si se permite el estado de esta configuración.</span><span class="sxs-lookup"><span data-stu-id="dc2a8-118">Representing a collection of local users or groups which will be set on device if the state of this setting is Allowed.</span></span> <span data-ttu-id="dc2a8-119">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="dc2a8-119">This collection can contain a maximum of 500 elements.</span></span>|

## <a name="relationships"></a><span data-ttu-id="dc2a8-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="dc2a8-120">Relationships</span></span>
<span data-ttu-id="dc2a8-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="dc2a8-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="dc2a8-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dc2a8-122">JSON Representation</span></span>
<span data-ttu-id="dc2a8-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="dc2a8-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementUserRightsSetting",
  "state": "String",
  "localUsersOrGroups": [
    {
      "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
      "name": "String",
      "description": "String",
      "securityIdentifier": "String"
    }
  ]
}
```






---
title: tipo de recurso windowsKioskActiveDirectoryGroup
description: La clase que se usa para identificar un grupo de Active Directory de Azure para la configuración de quiosco
ms.openlocfilehash: 18e876b50bdc8c8946bd511348d6ed3a6fc8fe5c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084927"
---
# <a name="windowskioskactivedirectorygroup-resource-type"></a><span data-ttu-id="e9d8b-103">tipo de recurso windowsKioskActiveDirectoryGroup</span><span class="sxs-lookup"><span data-stu-id="e9d8b-103">windowsKioskActiveDirectoryGroup resource type</span></span>

> <span data-ttu-id="e9d8b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e9d8b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e9d8b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e9d8b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e9d8b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e9d8b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e9d8b-107">La clase que se usa para identificar un grupo de Active Directory de Azure para la configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="e9d8b-107">The class used to identify an Azure Directory group for the kiosk configuration</span></span>

<span data-ttu-id="e9d8b-108">Hereda de [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span><span class="sxs-lookup"><span data-stu-id="e9d8b-108">Inherits from [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span></span>

## <a name="properties"></a><span data-ttu-id="e9d8b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e9d8b-109">Properties</span></span>
|<span data-ttu-id="e9d8b-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e9d8b-110">Property</span></span>|<span data-ttu-id="e9d8b-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9d8b-111">Type</span></span>|<span data-ttu-id="e9d8b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9d8b-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e9d8b-113">groupName</span><span class="sxs-lookup"><span data-stu-id="e9d8b-113">groupName</span></span>|<span data-ttu-id="e9d8b-114">String</span><span class="sxs-lookup"><span data-stu-id="e9d8b-114">String</span></span>|<span data-ttu-id="e9d8b-115">El nombre del grupo de AD que se bloqueará a esta configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="e9d8b-115">The name of the AD group that will be locked to this kiosk configuration</span></span>|

## <a name="relationships"></a><span data-ttu-id="e9d8b-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e9d8b-116">Relationships</span></span>
<span data-ttu-id="e9d8b-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e9d8b-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e9d8b-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e9d8b-118">JSON Representation</span></span>
<span data-ttu-id="e9d8b-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e9d8b-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskActiveDirectoryGroup"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskActiveDirectoryGroup",
  "groupName": "String"
}
```





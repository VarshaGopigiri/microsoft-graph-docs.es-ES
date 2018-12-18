---
title: tipo de recurso windowsKioskActiveDirectoryGroup
description: La clase que se usa para identificar un grupo de Active Directory de Azure para la configuración de quiosco
author: tfitzmac
ms.openlocfilehash: 618b93182d17d485a35d2567f45c218c6117658f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331780"
---
# <a name="windowskioskactivedirectorygroup-resource-type"></a><span data-ttu-id="1f75e-103">tipo de recurso windowsKioskActiveDirectoryGroup</span><span class="sxs-lookup"><span data-stu-id="1f75e-103">windowsKioskActiveDirectoryGroup resource type</span></span>

> <span data-ttu-id="1f75e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1f75e-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1f75e-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1f75e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1f75e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1f75e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1f75e-107">La clase que se usa para identificar un grupo de Active Directory de Azure para la configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="1f75e-107">The class used to identify an Azure Directory group for the kiosk configuration</span></span>

<span data-ttu-id="1f75e-108">Hereda de [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span><span class="sxs-lookup"><span data-stu-id="1f75e-108">Inherits from [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span></span>

## <a name="properties"></a><span data-ttu-id="1f75e-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1f75e-109">Properties</span></span>
|<span data-ttu-id="1f75e-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1f75e-110">Property</span></span>|<span data-ttu-id="1f75e-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="1f75e-111">Type</span></span>|<span data-ttu-id="1f75e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f75e-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1f75e-113">groupName</span><span class="sxs-lookup"><span data-stu-id="1f75e-113">groupName</span></span>|<span data-ttu-id="1f75e-114">String</span><span class="sxs-lookup"><span data-stu-id="1f75e-114">String</span></span>|<span data-ttu-id="1f75e-115">El nombre del grupo de AD que se bloqueará a esta configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="1f75e-115">The name of the AD group that will be locked to this kiosk configuration</span></span>|

## <a name="relationships"></a><span data-ttu-id="1f75e-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1f75e-116">Relationships</span></span>
<span data-ttu-id="1f75e-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="1f75e-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="1f75e-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1f75e-118">JSON Representation</span></span>
<span data-ttu-id="1f75e-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1f75e-119">Here is a JSON representation of the resource.</span></span>
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






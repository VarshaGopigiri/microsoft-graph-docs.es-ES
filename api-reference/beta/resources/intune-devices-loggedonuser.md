---
title: tipo de recurso loggedOnUser
description: Ha iniciado la sesión de usuario
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 056fae8051b70f2146930c8a2a1ae9505c0ec679
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962096"
---
# <a name="loggedonuser-resource-type"></a><span data-ttu-id="49cc7-103">tipo de recurso loggedOnUser</span><span class="sxs-lookup"><span data-stu-id="49cc7-103">loggedOnUser resource type</span></span>

> <span data-ttu-id="49cc7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="49cc7-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="49cc7-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="49cc7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="49cc7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="49cc7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="49cc7-107">Ha iniciado la sesión de usuario</span><span class="sxs-lookup"><span data-stu-id="49cc7-107">Logged On User</span></span>
## <a name="properties"></a><span data-ttu-id="49cc7-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="49cc7-108">Properties</span></span>
|<span data-ttu-id="49cc7-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="49cc7-109">Property</span></span>|<span data-ttu-id="49cc7-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="49cc7-110">Type</span></span>|<span data-ttu-id="49cc7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="49cc7-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="49cc7-112">userId</span><span class="sxs-lookup"><span data-stu-id="49cc7-112">userId</span></span>|<span data-ttu-id="49cc7-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="49cc7-113">String</span></span>|<span data-ttu-id="49cc7-114">Identificador de usuario</span><span class="sxs-lookup"><span data-stu-id="49cc7-114">User id</span></span>|
|<span data-ttu-id="49cc7-115">lastLogOnDateTime</span><span class="sxs-lookup"><span data-stu-id="49cc7-115">lastLogOnDateTime</span></span>|<span data-ttu-id="49cc7-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="49cc7-116">DateTimeOffset</span></span>|<span data-ttu-id="49cc7-117">Fecha hora cuando el usuario inicia sesión</span><span class="sxs-lookup"><span data-stu-id="49cc7-117">Date time when user logs on</span></span>|

## <a name="relationships"></a><span data-ttu-id="49cc7-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="49cc7-118">Relationships</span></span>
<span data-ttu-id="49cc7-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="49cc7-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="49cc7-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="49cc7-120">JSON Representation</span></span>
<span data-ttu-id="49cc7-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="49cc7-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.loggedOnUser"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.loggedOnUser",
  "userId": "String",
  "lastLogOnDateTime": "String (timestamp)"
}
```






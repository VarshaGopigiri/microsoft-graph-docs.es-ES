---
title: Tipo de recurso androidMobileAppIdentifier
description: El identificador de una aplicación móvil de Android.
ms.openlocfilehash: 976191384afb563a8243b92dfa9ddfcc98f0c4a2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085257"
---
# <a name="androidmobileappidentifier-resource-type"></a><span data-ttu-id="016ef-103">Tipo de recurso androidMobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="016ef-103">androidMobileAppIdentifier resource type</span></span>

> <span data-ttu-id="016ef-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="016ef-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="016ef-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="016ef-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="016ef-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="016ef-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="016ef-107">El identificador de una aplicación móvil de Android.</span><span class="sxs-lookup"><span data-stu-id="016ef-107">The identifier for an Android app.</span></span>

<span data-ttu-id="016ef-108">Hereda de [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span><span class="sxs-lookup"><span data-stu-id="016ef-108">Inherits from [mobileAppIdentifier](../resources/intune-mam-mobileappidentifier.md)</span></span>

## <a name="properties"></a><span data-ttu-id="016ef-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="016ef-109">Properties</span></span>
|<span data-ttu-id="016ef-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="016ef-110">Property</span></span>|<span data-ttu-id="016ef-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="016ef-111">Type</span></span>|<span data-ttu-id="016ef-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="016ef-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="016ef-113">packageId</span><span class="sxs-lookup"><span data-stu-id="016ef-113">packageId</span></span>|<span data-ttu-id="016ef-114">cadena</span><span class="sxs-lookup"><span data-stu-id="016ef-114">String</span></span>|<span data-ttu-id="016ef-115">El identificador de una aplicación, como se especifica en la Play Store.</span><span class="sxs-lookup"><span data-stu-id="016ef-115">The identifier for an app, as specified in the play store.</span></span>|

## <a name="relationships"></a><span data-ttu-id="016ef-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="016ef-116">Relationships</span></span>
<span data-ttu-id="016ef-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="016ef-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="016ef-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="016ef-118">JSON Representation</span></span>
<span data-ttu-id="016ef-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="016ef-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.androidMobileAppIdentifier"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidMobileAppIdentifier",
  "packageId": "String"
}
```






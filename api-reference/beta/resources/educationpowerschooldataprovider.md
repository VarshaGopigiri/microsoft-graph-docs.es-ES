---
title: recursos de educationPowerSchoolDataProvider
description: Se usa para configurar el perfil de sincronización de datos de school cuando PowerSchool se utiliza como el origen de entrada.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: 48a23a2e2a50e2e235b5722466c67094275236a1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27868785"
---
# <a name="educationpowerschooldataprovider-resource"></a><span data-ttu-id="a7188-103">recursos de educationPowerSchoolDataProvider</span><span class="sxs-lookup"><span data-stu-id="a7188-103">educationPowerSchoolDataProvider resource</span></span>

> <span data-ttu-id="a7188-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a7188-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a7188-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a7188-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a7188-106">Se usa para configurar el perfil de sincronización de datos de school cuando [PowerSchool](https://www.powerschool.com/solutions/student-information-system-sis/) se utiliza como el origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="a7188-106">Used to set up the school data synchronization profile when [PowerSchool](https://www.powerschool.com/solutions/student-information-system-sis/) is used as the input source.</span></span>

<span data-ttu-id="a7188-107">Deriva de [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).</span><span class="sxs-lookup"><span data-stu-id="a7188-107">Derived from [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).</span></span>

## <a name="properties"></a><span data-ttu-id="a7188-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a7188-108">Properties</span></span>

| <span data-ttu-id="a7188-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a7188-109">Property</span></span> | <span data-ttu-id="a7188-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7188-110">Type</span></span> | <span data-ttu-id="a7188-111">Description</span><span class="sxs-lookup"><span data-stu-id="a7188-111">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="a7188-112">**connectionUrl**</span><span class="sxs-lookup"><span data-stu-id="a7188-112">**connectionUrl**</span></span> | <span data-ttu-id="a7188-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="a7188-113">String</span></span> | <span data-ttu-id="a7188-114">La dirección URL de conexión a la instancia de PowerSchool.</span><span class="sxs-lookup"><span data-stu-id="a7188-114">The connection URL to the PowerSchool instance.</span></span> |
| <span data-ttu-id="a7188-115">**clientId**</span><span class="sxs-lookup"><span data-stu-id="a7188-115">**clientId**</span></span> | <span data-ttu-id="a7188-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="a7188-116">String</span></span> |  <span data-ttu-id="a7188-117">El identificador de cliente que se usa para conectarse a PowerSchool.</span><span class="sxs-lookup"><span data-stu-id="a7188-117">The client ID used to connect to PowerSchool.</span></span> |
| <span data-ttu-id="a7188-118">**clientSecret**</span><span class="sxs-lookup"><span data-stu-id="a7188-118">**clientSecret**</span></span> | <span data-ttu-id="a7188-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="a7188-119">String</span></span> |  <span data-ttu-id="a7188-120">El secreto de cliente para autenticar la conexión a la instancia de PowerSchool.</span><span class="sxs-lookup"><span data-stu-id="a7188-120">The client secret to authenticate the connection to the PowerSchool instance.</span></span> |
| <span data-ttu-id="a7188-121">**schoolsIds**</span><span class="sxs-lookup"><span data-stu-id="a7188-121">**schoolsIds**</span></span> | <span data-ttu-id="a7188-122">Colección String</span><span class="sxs-lookup"><span data-stu-id="a7188-122">String collection</span></span> |  <span data-ttu-id="a7188-123">La lista de escuelas para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="a7188-123">The list of schools to sync.</span></span> |
| <span data-ttu-id="a7188-124">**schoolYear**</span><span class="sxs-lookup"><span data-stu-id="a7188-124">**schoolYear**</span></span> | <span data-ttu-id="a7188-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="a7188-125">String</span></span> |  <span data-ttu-id="a7188-126">El año escolar para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="a7188-126">The school year to sync.</span></span> |
| <span data-ttu-id="a7188-127">**allowTeachersInMultipleSchools**</span><span class="sxs-lookup"><span data-stu-id="a7188-127">**allowTeachersInMultipleSchools**</span></span> | <span data-ttu-id="a7188-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="a7188-128">Boolean</span></span> |  <span data-ttu-id="a7188-129">Indica si el origen tiene varios identificadores para un solo alumno o profesor.</span><span class="sxs-lookup"><span data-stu-id="a7188-129">Indicates whether the source has multiple identifiers for a single student or teacher.</span></span> |
| <span data-ttu-id="a7188-130">**personalizaciones**</span><span class="sxs-lookup"><span data-stu-id="a7188-130">**customizations**</span></span> | [<span data-ttu-id="a7188-131">educationSynchronizationCustomizations</span><span class="sxs-lookup"><span data-stu-id="a7188-131">educationSynchronizationCustomizations</span></span>](educationsynchronizationcustomizations.md) | <span data-ttu-id="a7188-132">Personalización opcional que se aplicará a los perfiles de sincronización.</span><span class="sxs-lookup"><span data-stu-id="a7188-132">Optional customization to be applied to the synchronization profile.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a7188-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a7188-133">JSON representation</span></span>
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationPowerSchoolDataProvider"
}-->

```json
{
    "@odata.type": "#microsoft.graph.educationPowerSchoolDataProvider",
    "connectionUrl": "String",
    "clientId": "String",
    "clientSecret": "String",
    "schoolsids": ["String"],
    "schoolYear": "String",
    "allowTeachersInMultipleSchools": "Boolean",
    "customizations": { "@odata.type": "microsoft.graph.educationSynchronizationCustomizations" }
}
```

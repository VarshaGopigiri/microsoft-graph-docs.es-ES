---
title: tipo de recurso certificateConnectorSetting
description: Configuración de conector de certificados.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 56f12600b6aa78982dc51732d685dcd7c962d0b0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888602"
---
# <a name="certificateconnectorsetting-resource-type"></a><span data-ttu-id="296dc-103">tipo de recurso certificateConnectorSetting</span><span class="sxs-lookup"><span data-stu-id="296dc-103">certificateConnectorSetting resource type</span></span>

> <span data-ttu-id="296dc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="296dc-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="296dc-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="296dc-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="296dc-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="296dc-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="296dc-107">Configuración de conector de certificados.</span><span class="sxs-lookup"><span data-stu-id="296dc-107">Certificate connector settings.</span></span>
## <a name="properties"></a><span data-ttu-id="296dc-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="296dc-108">Properties</span></span>
|<span data-ttu-id="296dc-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="296dc-109">Property</span></span>|<span data-ttu-id="296dc-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="296dc-110">Type</span></span>|<span data-ttu-id="296dc-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="296dc-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="296dc-112">status</span><span class="sxs-lookup"><span data-stu-id="296dc-112">status</span></span>|<span data-ttu-id="296dc-113">Int32</span><span class="sxs-lookup"><span data-stu-id="296dc-113">Int32</span></span>|<span data-ttu-id="296dc-114">Estado del conector de certificado</span><span class="sxs-lookup"><span data-stu-id="296dc-114">Certificate connector status</span></span>|
|<span data-ttu-id="296dc-115">certExpiryTime</span><span class="sxs-lookup"><span data-stu-id="296dc-115">certExpiryTime</span></span>|<span data-ttu-id="296dc-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="296dc-116">DateTimeOffset</span></span>|<span data-ttu-id="296dc-117">Certificado caduque tiempo</span><span class="sxs-lookup"><span data-stu-id="296dc-117">Certificate expire time</span></span>|
|<span data-ttu-id="296dc-118">enrollmentError</span><span class="sxs-lookup"><span data-stu-id="296dc-118">enrollmentError</span></span>|<span data-ttu-id="296dc-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="296dc-119">String</span></span>|<span data-ttu-id="296dc-120">Error de inscripción de conector de certificado</span><span class="sxs-lookup"><span data-stu-id="296dc-120">Certificate connector enrollment error</span></span>|
|<span data-ttu-id="296dc-121">lastConnectorConnectionTime</span><span class="sxs-lookup"><span data-stu-id="296dc-121">lastConnectorConnectionTime</span></span>|<span data-ttu-id="296dc-122">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="296dc-122">DateTimeOffset</span></span>|<span data-ttu-id="296dc-123">Última vez certificado conector conectado</span><span class="sxs-lookup"><span data-stu-id="296dc-123">Last time certificate connector connected</span></span>|
|<span data-ttu-id="296dc-124">connectorVersion</span><span class="sxs-lookup"><span data-stu-id="296dc-124">connectorVersion</span></span>|<span data-ttu-id="296dc-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="296dc-125">String</span></span>|<span data-ttu-id="296dc-126">Versión del conector de certificado</span><span class="sxs-lookup"><span data-stu-id="296dc-126">Version of certificate connector</span></span>|
|<span data-ttu-id="296dc-127">lastUploadVersion</span><span class="sxs-lookup"><span data-stu-id="296dc-127">lastUploadVersion</span></span>|<span data-ttu-id="296dc-128">Int64</span><span class="sxs-lookup"><span data-stu-id="296dc-128">Int64</span></span>|<span data-ttu-id="296dc-129">Versión del conector de certificado que se cargan última</span><span class="sxs-lookup"><span data-stu-id="296dc-129">Version of last uploaded certificate connector</span></span>|

## <a name="relationships"></a><span data-ttu-id="296dc-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="296dc-130">Relationships</span></span>
<span data-ttu-id="296dc-131">Ninguna</span><span class="sxs-lookup"><span data-stu-id="296dc-131">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="296dc-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="296dc-132">JSON Representation</span></span>
<span data-ttu-id="296dc-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="296dc-133">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.certificateConnectorSetting"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.certificateConnectorSetting",
  "status": 1024,
  "certExpiryTime": "String (timestamp)",
  "enrollmentError": "String",
  "lastConnectorConnectionTime": "String (timestamp)",
  "connectorVersion": "String",
  "lastUploadVersion": 1024
}
```






---
title: tipo de recurso certificateConnectorSetting
description: Configuración de conector de certificados.
author: tfitzmac
ms.openlocfilehash: 8c993634eb4f41e16643ae3f40be74ecc3eb392f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326309"
---
# <a name="certificateconnectorsetting-resource-type"></a><span data-ttu-id="f6ab9-103">tipo de recurso certificateConnectorSetting</span><span class="sxs-lookup"><span data-stu-id="f6ab9-103">certificateConnectorSetting resource type</span></span>

> <span data-ttu-id="f6ab9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f6ab9-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f6ab9-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f6ab9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f6ab9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f6ab9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f6ab9-107">Configuración de conector de certificados.</span><span class="sxs-lookup"><span data-stu-id="f6ab9-107">Certificate connector settings.</span></span>
## <a name="properties"></a><span data-ttu-id="f6ab9-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6ab9-108">Properties</span></span>
|<span data-ttu-id="f6ab9-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f6ab9-109">Property</span></span>|<span data-ttu-id="f6ab9-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6ab9-110">Type</span></span>|<span data-ttu-id="f6ab9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6ab9-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f6ab9-112">status</span><span class="sxs-lookup"><span data-stu-id="f6ab9-112">status</span></span>|<span data-ttu-id="f6ab9-113">Int32</span><span class="sxs-lookup"><span data-stu-id="f6ab9-113">Int32</span></span>|<span data-ttu-id="f6ab9-114">Estado del conector de certificado</span><span class="sxs-lookup"><span data-stu-id="f6ab9-114">Certificate connector status</span></span>|
|<span data-ttu-id="f6ab9-115">certExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f6ab9-115">certExpiryTime</span></span>|<span data-ttu-id="f6ab9-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f6ab9-116">DateTimeOffset</span></span>|<span data-ttu-id="f6ab9-117">Certificado caduque tiempo</span><span class="sxs-lookup"><span data-stu-id="f6ab9-117">Certificate expire time</span></span>|
|<span data-ttu-id="f6ab9-118">enrollmentError</span><span class="sxs-lookup"><span data-stu-id="f6ab9-118">enrollmentError</span></span>|<span data-ttu-id="f6ab9-119">String</span><span class="sxs-lookup"><span data-stu-id="f6ab9-119">String</span></span>|<span data-ttu-id="f6ab9-120">Error de inscripción de conector de certificado</span><span class="sxs-lookup"><span data-stu-id="f6ab9-120">Certificate connector enrollment error</span></span>|
|<span data-ttu-id="f6ab9-121">lastConnectorConnectionTime</span><span class="sxs-lookup"><span data-stu-id="f6ab9-121">lastConnectorConnectionTime</span></span>|<span data-ttu-id="f6ab9-122">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f6ab9-122">DateTimeOffset</span></span>|<span data-ttu-id="f6ab9-123">Última vez certificado conector conectado</span><span class="sxs-lookup"><span data-stu-id="f6ab9-123">Last time certificate connector connected</span></span>|
|<span data-ttu-id="f6ab9-124">connectorVersion</span><span class="sxs-lookup"><span data-stu-id="f6ab9-124">connectorVersion</span></span>|<span data-ttu-id="f6ab9-125">String</span><span class="sxs-lookup"><span data-stu-id="f6ab9-125">String</span></span>|<span data-ttu-id="f6ab9-126">Versión del conector de certificado</span><span class="sxs-lookup"><span data-stu-id="f6ab9-126">Version of certificate connector</span></span>|
|<span data-ttu-id="f6ab9-127">lastUploadVersion</span><span class="sxs-lookup"><span data-stu-id="f6ab9-127">lastUploadVersion</span></span>|<span data-ttu-id="f6ab9-128">Int64</span><span class="sxs-lookup"><span data-stu-id="f6ab9-128">Int64</span></span>|<span data-ttu-id="f6ab9-129">Versión del conector de certificado que se cargan última</span><span class="sxs-lookup"><span data-stu-id="f6ab9-129">Version of last uploaded certificate connector</span></span>|

## <a name="relationships"></a><span data-ttu-id="f6ab9-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f6ab9-130">Relationships</span></span>
<span data-ttu-id="f6ab9-131">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f6ab9-131">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f6ab9-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f6ab9-132">JSON Representation</span></span>
<span data-ttu-id="f6ab9-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f6ab9-133">Here is a JSON representation of the resource.</span></span>
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






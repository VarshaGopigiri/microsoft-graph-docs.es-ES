---
title: tipo de recurso win32LobAppFileSystemDetection
description: Contiene la ruta de acceso de archivo o carpeta para detectar una aplicación de Win32
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: c901949295b1ff411dec5e9827b7991c922c2315
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27958211"
---
# <a name="win32lobappfilesystemdetection-resource-type"></a><span data-ttu-id="586e6-103">tipo de recurso win32LobAppFileSystemDetection</span><span class="sxs-lookup"><span data-stu-id="586e6-103">win32LobAppFileSystemDetection resource type</span></span>

> <span data-ttu-id="586e6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="586e6-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="586e6-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="586e6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="586e6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="586e6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="586e6-107">Contiene la ruta de acceso de archivo o carpeta para detectar una aplicación de Win32</span><span class="sxs-lookup"><span data-stu-id="586e6-107">Contains file or folder path to detect a Win32 App</span></span>

<span data-ttu-id="586e6-108">Hereda de [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)</span><span class="sxs-lookup"><span data-stu-id="586e6-108">Inherits from [win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)</span></span>

## <a name="properties"></a><span data-ttu-id="586e6-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="586e6-109">Properties</span></span>
|<span data-ttu-id="586e6-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="586e6-110">Property</span></span>|<span data-ttu-id="586e6-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="586e6-111">Type</span></span>|<span data-ttu-id="586e6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="586e6-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="586e6-113">ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="586e6-113">path</span></span>|<span data-ttu-id="586e6-114">String</span><span class="sxs-lookup"><span data-stu-id="586e6-114">String</span></span>|<span data-ttu-id="586e6-115">La ruta de acceso de archivo o carpeta para detectar la aplicación de línea de negocio (LoB) de Win32</span><span class="sxs-lookup"><span data-stu-id="586e6-115">The file or folder path to detect Win32 Line of Business (LoB) app</span></span>|
|<span data-ttu-id="586e6-116">fileOrFolderName</span><span class="sxs-lookup"><span data-stu-id="586e6-116">fileOrFolderName</span></span>|<span data-ttu-id="586e6-117">String</span><span class="sxs-lookup"><span data-stu-id="586e6-117">String</span></span>|<span data-ttu-id="586e6-118">El nombre de archivo o carpeta para detectar la aplicación de línea de negocio (LoB) de Win32</span><span class="sxs-lookup"><span data-stu-id="586e6-118">The file or folder name to detect Win32 Line of Business (LoB) app</span></span>|
|<span data-ttu-id="586e6-119">check32BitOn64System</span><span class="sxs-lookup"><span data-stu-id="586e6-119">check32BitOn64System</span></span>|<span data-ttu-id="586e6-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="586e6-120">Boolean</span></span>|<span data-ttu-id="586e6-121">Un valor que indica si este archivo o carpeta para comprobar la aplicación de 32 bits en el sistema de 64 bits</span><span class="sxs-lookup"><span data-stu-id="586e6-121">A value indicating whether this file or folder is for checking 32-bit app on 64-bit system</span></span>|
|<span data-ttu-id="586e6-122">tipo de detección</span><span class="sxs-lookup"><span data-stu-id="586e6-122">detectionType</span></span>|[<span data-ttu-id="586e6-123">win32LobAppFileSystemDetectionType</span><span class="sxs-lookup"><span data-stu-id="586e6-123">win32LobAppFileSystemDetectionType</span></span>](../resources/intune-apps-win32lobappfilesystemdetectiontype.md)|<span data-ttu-id="586e6-124">El tipo de detección del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="586e6-124">The file system detection type.</span></span> <span data-ttu-id="586e6-125">Los valores posibles son: `notConfigured`, `exists`, `modifiedDate`, `createdDate`, `version`, `sizeInMB`.</span><span class="sxs-lookup"><span data-stu-id="586e6-125">Possible values are: `notConfigured`, `exists`, `modifiedDate`, `createdDate`, `version`, `sizeInMB`.</span></span>|
|<span data-ttu-id="586e6-126">operator</span><span class="sxs-lookup"><span data-stu-id="586e6-126">operator</span></span>|[<span data-ttu-id="586e6-127">win32LobAppDetectionOperator</span><span class="sxs-lookup"><span data-stu-id="586e6-127">win32LobAppDetectionOperator</span></span>](../resources/intune-apps-win32lobappdetectionoperator.md)|<span data-ttu-id="586e6-128">El operador para la detección de archivos o carpetas.</span><span class="sxs-lookup"><span data-stu-id="586e6-128">The operator for file or fodler detection.</span></span> <span data-ttu-id="586e6-129">Los valores posibles son: `notConfigured`, `equal`, `notEqual`, `greaterThan`, `greaterThanOrEqual`, `lessThan` y `lessThanOrEqual`.</span><span class="sxs-lookup"><span data-stu-id="586e6-129">Possible values are: `notConfigured`, `equal`, `notEqual`, `greaterThan`, `greaterThanOrEqual`, `lessThan`, `lessThanOrEqual`.</span></span>|
|<span data-ttu-id="586e6-130">detectionValue</span><span class="sxs-lookup"><span data-stu-id="586e6-130">detectionValue</span></span>|<span data-ttu-id="586e6-131">String</span><span class="sxs-lookup"><span data-stu-id="586e6-131">String</span></span>|<span data-ttu-id="586e6-132">El valor de detección de archivo o carpeta</span><span class="sxs-lookup"><span data-stu-id="586e6-132">The file or folder detection value</span></span>|

## <a name="relationships"></a><span data-ttu-id="586e6-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="586e6-133">Relationships</span></span>
<span data-ttu-id="586e6-134">Ninguna</span><span class="sxs-lookup"><span data-stu-id="586e6-134">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="586e6-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="586e6-135">JSON Representation</span></span>
<span data-ttu-id="586e6-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="586e6-136">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.win32LobAppFileSystemDetection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobAppFileSystemDetection",
  "path": "String",
  "fileOrFolderName": "String",
  "check32BitOn64System": true,
  "detectionType": "String",
  "operator": "String",
  "detectionValue": "String"
}
```






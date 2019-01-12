---
title: Tipo de recurso eBookInstallSummary
description: Contiene las propiedades del resumen de la instalación de un libro para un dispositivo.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3d3a5d1ce5c05d0a8c20a79aea2fd3562ab2170c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27915945"
---
# <a name="ebookinstallsummary-resource-type"></a><span data-ttu-id="b9254-103">Tipo de recurso eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="b9254-103">eBookInstallSummary resource type</span></span>

> <span data-ttu-id="b9254-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b9254-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b9254-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b9254-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b9254-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b9254-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b9254-107">Contiene las propiedades del resumen de la instalación de un libro para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9254-107">Contains properties for the installation summary of a book for a device.</span></span>
## <a name="methods"></a><span data-ttu-id="b9254-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="b9254-108">Methods</span></span>
|<span data-ttu-id="b9254-109">Método</span><span class="sxs-lookup"><span data-stu-id="b9254-109">Method</span></span>|<span data-ttu-id="b9254-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9254-110">Return Type</span></span>|<span data-ttu-id="b9254-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9254-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="b9254-112">Obtener eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="b9254-112">Get eBookInstallSummary</span></span>](../api/intune-books-ebookinstallsummary-get.md)|[<span data-ttu-id="b9254-113">eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="b9254-113">eBookInstallSummary</span></span>](../resources/intune-books-ebookinstallsummary.md)|<span data-ttu-id="b9254-114">Lea las propiedades y las relaciones del objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="b9254-114">Read properties and relationships of the [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) object.</span></span>|
|[<span data-ttu-id="b9254-115">Actualizar eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="b9254-115">Update eBookInstallSummary</span></span>](../api/intune-books-ebookinstallsummary-update.md)|[<span data-ttu-id="b9254-116">eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="b9254-116">eBookInstallSummary</span></span>](../resources/intune-books-ebookinstallsummary.md)|<span data-ttu-id="b9254-117">Actualice las propiedades de un objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="b9254-117">Update the properties of a [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="b9254-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9254-118">Properties</span></span>
|<span data-ttu-id="b9254-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b9254-119">Property</span></span>|<span data-ttu-id="b9254-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9254-120">Type</span></span>|<span data-ttu-id="b9254-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9254-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b9254-122">id</span><span class="sxs-lookup"><span data-stu-id="b9254-122">id</span></span>|<span data-ttu-id="b9254-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="b9254-123">String</span></span>|<span data-ttu-id="b9254-124">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b9254-124">Key of the entity.</span></span>|
|<span data-ttu-id="b9254-125">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b9254-125">installedDeviceCount</span></span>|<span data-ttu-id="b9254-126">Int32</span><span class="sxs-lookup"><span data-stu-id="b9254-126">Int32</span></span>|<span data-ttu-id="b9254-127">Número de dispositivos que han instalado correctamente este libro.</span><span class="sxs-lookup"><span data-stu-id="b9254-127">Number of Devices that have successfully installed this book.</span></span>|
|<span data-ttu-id="b9254-128">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b9254-128">failedDeviceCount</span></span>|<span data-ttu-id="b9254-129">Int32</span><span class="sxs-lookup"><span data-stu-id="b9254-129">Int32</span></span>|<span data-ttu-id="b9254-130">Número de dispositivos que no han podido instalar este libro.</span><span class="sxs-lookup"><span data-stu-id="b9254-130">Number of Devices that have failed to install this book.</span></span>|
|<span data-ttu-id="b9254-131">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b9254-131">notInstalledDeviceCount</span></span>|<span data-ttu-id="b9254-132">Int32</span><span class="sxs-lookup"><span data-stu-id="b9254-132">Int32</span></span>|<span data-ttu-id="b9254-133">Número de dispositivos que no han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="b9254-133">Number of Devices that does not have this book installed.</span></span>|
|<span data-ttu-id="b9254-134">installedUserCount</span><span class="sxs-lookup"><span data-stu-id="b9254-134">installedUserCount</span></span>|<span data-ttu-id="b9254-135">Int32</span><span class="sxs-lookup"><span data-stu-id="b9254-135">Int32</span></span>|<span data-ttu-id="b9254-136">Número de usuarios cuyos dispositivos al completo han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="b9254-136">Number of Users whose devices have all succeeded to install this book.</span></span>|
|<span data-ttu-id="b9254-137">failedUserCount</span><span class="sxs-lookup"><span data-stu-id="b9254-137">failedUserCount</span></span>|<span data-ttu-id="b9254-138">Int32</span><span class="sxs-lookup"><span data-stu-id="b9254-138">Int32</span></span>|<span data-ttu-id="b9254-139">Número de usuarios que tienen 1 o más dispositivos que no han podido instalar este libro.</span><span class="sxs-lookup"><span data-stu-id="b9254-139">Number of Users that have 1 or more device that failed to install this book.</span></span>|
|<span data-ttu-id="b9254-140">notInstalledUserCount</span><span class="sxs-lookup"><span data-stu-id="b9254-140">notInstalledUserCount</span></span>|<span data-ttu-id="b9254-141">Int32</span><span class="sxs-lookup"><span data-stu-id="b9254-141">Int32</span></span>|<span data-ttu-id="b9254-142">Número de usuarios que no han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="b9254-142">Number of Users that did not install this book.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b9254-143">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b9254-143">Relationships</span></span>
<span data-ttu-id="b9254-144">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b9254-144">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="b9254-145">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b9254-145">JSON Representation</span></span>
<span data-ttu-id="b9254-146">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b9254-146">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.eBookInstallSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.eBookInstallSummary",
  "id": "String (identifier)",
  "installedDeviceCount": 1024,
  "failedDeviceCount": 1024,
  "notInstalledDeviceCount": 1024,
  "installedUserCount": 1024,
  "failedUserCount": 1024,
  "notInstalledUserCount": 1024
}
```






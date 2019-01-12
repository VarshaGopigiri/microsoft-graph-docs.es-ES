---
title: Tipo de recurso eBookInstallSummary
description: Contiene las propiedades del resumen de la instalación de un libro para un dispositivo.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a3d07dc2d1a1b7a117e001546cd5298765676bdd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27986155"
---
# <a name="ebookinstallsummary-resource-type"></a><span data-ttu-id="7714f-103">Tipo de recurso eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="7714f-103">eBookInstallSummary resource type</span></span>

> <span data-ttu-id="7714f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7714f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7714f-105">Contiene las propiedades del resumen de la instalación de un libro para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7714f-105">Contains properties for the installation summary of a book for a device.</span></span>
## <a name="methods"></a><span data-ttu-id="7714f-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="7714f-106">Methods</span></span>
|<span data-ttu-id="7714f-107">Método</span><span class="sxs-lookup"><span data-stu-id="7714f-107">Method</span></span>|<span data-ttu-id="7714f-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7714f-108">Return Type</span></span>|<span data-ttu-id="7714f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7714f-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="7714f-110">Obtener eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="7714f-110">Get eBookInstallSummary</span></span>](../api/intune-books-ebookinstallsummary-get.md)|[<span data-ttu-id="7714f-111">eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="7714f-111">eBookInstallSummary</span></span>](../resources/intune-books-ebookinstallsummary.md)|<span data-ttu-id="7714f-112">Lea las propiedades y las relaciones del objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="7714f-112">Read properties and relationships of the [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) object.</span></span>|
|[<span data-ttu-id="7714f-113">Actualizar eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="7714f-113">Update eBookInstallSummary</span></span>](../api/intune-books-ebookinstallsummary-update.md)|[<span data-ttu-id="7714f-114">eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="7714f-114">eBookInstallSummary</span></span>](../resources/intune-books-ebookinstallsummary.md)|<span data-ttu-id="7714f-115">Actualice las propiedades de un objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="7714f-115">Update the properties of a [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="7714f-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7714f-116">Properties</span></span>
|<span data-ttu-id="7714f-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7714f-117">Property</span></span>|<span data-ttu-id="7714f-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="7714f-118">Type</span></span>|<span data-ttu-id="7714f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="7714f-119">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7714f-120">id</span><span class="sxs-lookup"><span data-stu-id="7714f-120">id</span></span>|<span data-ttu-id="7714f-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="7714f-121">String</span></span>|<span data-ttu-id="7714f-122">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7714f-122">Key of the entity.</span></span>|
|<span data-ttu-id="7714f-123">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="7714f-123">installedDeviceCount</span></span>|<span data-ttu-id="7714f-124">Int32</span><span class="sxs-lookup"><span data-stu-id="7714f-124">Int32</span></span>|<span data-ttu-id="7714f-125">Número de dispositivos que han instalado correctamente este libro.</span><span class="sxs-lookup"><span data-stu-id="7714f-125">Number of Devices that have successfully installed this book.</span></span>|
|<span data-ttu-id="7714f-126">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="7714f-126">failedDeviceCount</span></span>|<span data-ttu-id="7714f-127">Int32</span><span class="sxs-lookup"><span data-stu-id="7714f-127">Int32</span></span>|<span data-ttu-id="7714f-128">Número de dispositivos que no han podido instalar este libro.</span><span class="sxs-lookup"><span data-stu-id="7714f-128">Number of Devices that have failed to install this book.</span></span>|
|<span data-ttu-id="7714f-129">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="7714f-129">notInstalledDeviceCount</span></span>|<span data-ttu-id="7714f-130">Int32</span><span class="sxs-lookup"><span data-stu-id="7714f-130">Int32</span></span>|<span data-ttu-id="7714f-131">Número de dispositivos que no han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="7714f-131">Number of Devices that does not have this book installed.</span></span>|
|<span data-ttu-id="7714f-132">installedUserCount</span><span class="sxs-lookup"><span data-stu-id="7714f-132">installedUserCount</span></span>|<span data-ttu-id="7714f-133">Int32</span><span class="sxs-lookup"><span data-stu-id="7714f-133">Int32</span></span>|<span data-ttu-id="7714f-134">Número de usuarios cuyos dispositivos al completo han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="7714f-134">Number of Users whose devices have all succeeded to install this book.</span></span>|
|<span data-ttu-id="7714f-135">failedUserCount</span><span class="sxs-lookup"><span data-stu-id="7714f-135">failedUserCount</span></span>|<span data-ttu-id="7714f-136">Int32</span><span class="sxs-lookup"><span data-stu-id="7714f-136">Int32</span></span>|<span data-ttu-id="7714f-137">Número de usuarios que tienen 1 o más dispositivos que no han podido instalar este libro.</span><span class="sxs-lookup"><span data-stu-id="7714f-137">Number of Users that have 1 or more device that failed to install this book.</span></span>|
|<span data-ttu-id="7714f-138">notInstalledUserCount</span><span class="sxs-lookup"><span data-stu-id="7714f-138">notInstalledUserCount</span></span>|<span data-ttu-id="7714f-139">Int32</span><span class="sxs-lookup"><span data-stu-id="7714f-139">Int32</span></span>|<span data-ttu-id="7714f-140">Número de usuarios que no han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="7714f-140">Number of Users that did not install this book.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7714f-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7714f-141">Relationships</span></span>
<span data-ttu-id="7714f-142">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7714f-142">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7714f-143">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7714f-143">JSON Representation</span></span>
<span data-ttu-id="7714f-144">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7714f-144">Here is a JSON representation of the resource.</span></span>
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




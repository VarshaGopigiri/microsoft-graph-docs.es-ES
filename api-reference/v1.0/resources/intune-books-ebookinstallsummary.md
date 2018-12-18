---
title: Tipo de recurso eBookInstallSummary
description: Contiene las propiedades del resumen de la instalación de un libro para un dispositivo.
author: tfitzmac
ms.openlocfilehash: 4f94c82a0d7cd234206586829981c62ba7d0a959
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344278"
---
# <a name="ebookinstallsummary-resource-type"></a><span data-ttu-id="bbbe7-103">Tipo de recurso eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="bbbe7-103">eBookInstallSummary resource type</span></span>

> <span data-ttu-id="bbbe7-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bbbe7-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bbbe7-105">Contiene las propiedades del resumen de la instalación de un libro para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bbbe7-105">Contains properties for the installation summary of a book for a device.</span></span>
## <a name="methods"></a><span data-ttu-id="bbbe7-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="bbbe7-106">Methods</span></span>
|<span data-ttu-id="bbbe7-107">Método</span><span class="sxs-lookup"><span data-stu-id="bbbe7-107">Method</span></span>|<span data-ttu-id="bbbe7-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bbbe7-108">Return Type</span></span>|<span data-ttu-id="bbbe7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbbe7-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="bbbe7-110">Obtener eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="bbbe7-110">Get eBookInstallSummary</span></span>](../api/intune-books-ebookinstallsummary-get.md)|[<span data-ttu-id="bbbe7-111">eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="bbbe7-111">eBookInstallSummary</span></span>](../resources/intune-books-ebookinstallsummary.md)|<span data-ttu-id="bbbe7-112">Lea las propiedades y las relaciones del objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="bbbe7-112">Read properties and relationships of the [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) object.</span></span>|
|[<span data-ttu-id="bbbe7-113">Actualizar eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="bbbe7-113">Update eBookInstallSummary</span></span>](../api/intune-books-ebookinstallsummary-update.md)|[<span data-ttu-id="bbbe7-114">eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="bbbe7-114">eBookInstallSummary</span></span>](../resources/intune-books-ebookinstallsummary.md)|<span data-ttu-id="bbbe7-115">Actualice las propiedades de un objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="bbbe7-115">Update the properties of a [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="bbbe7-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bbbe7-116">Properties</span></span>
|<span data-ttu-id="bbbe7-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bbbe7-117">Property</span></span>|<span data-ttu-id="bbbe7-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="bbbe7-118">Type</span></span>|<span data-ttu-id="bbbe7-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbbe7-119">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bbbe7-120">id</span><span class="sxs-lookup"><span data-stu-id="bbbe7-120">id</span></span>|<span data-ttu-id="bbbe7-121">String</span><span class="sxs-lookup"><span data-stu-id="bbbe7-121">String</span></span>|<span data-ttu-id="bbbe7-122">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bbbe7-122">Key of the entity.</span></span>|
|<span data-ttu-id="bbbe7-123">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bbbe7-123">installedDeviceCount</span></span>|<span data-ttu-id="bbbe7-124">Int32</span><span class="sxs-lookup"><span data-stu-id="bbbe7-124">Int32</span></span>|<span data-ttu-id="bbbe7-125">Número de dispositivos que han instalado correctamente este libro.</span><span class="sxs-lookup"><span data-stu-id="bbbe7-125">Number of Devices that have successfully installed this book.</span></span>|
|<span data-ttu-id="bbbe7-126">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bbbe7-126">failedDeviceCount</span></span>|<span data-ttu-id="bbbe7-127">Int32</span><span class="sxs-lookup"><span data-stu-id="bbbe7-127">Int32</span></span>|<span data-ttu-id="bbbe7-128">Número de dispositivos que no han podido instalar este libro.</span><span class="sxs-lookup"><span data-stu-id="bbbe7-128">Number of Devices that have failed to install this book.</span></span>|
|<span data-ttu-id="bbbe7-129">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bbbe7-129">notInstalledDeviceCount</span></span>|<span data-ttu-id="bbbe7-130">Int32</span><span class="sxs-lookup"><span data-stu-id="bbbe7-130">Int32</span></span>|<span data-ttu-id="bbbe7-131">Número de dispositivos que no han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="bbbe7-131">Number of Devices that does not have this book installed.</span></span>|
|<span data-ttu-id="bbbe7-132">installedUserCount</span><span class="sxs-lookup"><span data-stu-id="bbbe7-132">installedUserCount</span></span>|<span data-ttu-id="bbbe7-133">Int32</span><span class="sxs-lookup"><span data-stu-id="bbbe7-133">Int32</span></span>|<span data-ttu-id="bbbe7-134">Número de usuarios cuyos dispositivos al completo han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="bbbe7-134">Number of Users whose devices have all succeeded to install this book.</span></span>|
|<span data-ttu-id="bbbe7-135">failedUserCount</span><span class="sxs-lookup"><span data-stu-id="bbbe7-135">failedUserCount</span></span>|<span data-ttu-id="bbbe7-136">Int32</span><span class="sxs-lookup"><span data-stu-id="bbbe7-136">Int32</span></span>|<span data-ttu-id="bbbe7-137">Número de usuarios que tienen 1 o más dispositivos que no han podido instalar este libro.</span><span class="sxs-lookup"><span data-stu-id="bbbe7-137">Number of Users that have 1 or more device that failed to install this book.</span></span>|
|<span data-ttu-id="bbbe7-138">notInstalledUserCount</span><span class="sxs-lookup"><span data-stu-id="bbbe7-138">notInstalledUserCount</span></span>|<span data-ttu-id="bbbe7-139">Int32</span><span class="sxs-lookup"><span data-stu-id="bbbe7-139">Int32</span></span>|<span data-ttu-id="bbbe7-140">Número de usuarios que no han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="bbbe7-140">Number of Users that did not install this book.</span></span>|

## <a name="relationships"></a><span data-ttu-id="bbbe7-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bbbe7-141">Relationships</span></span>
<span data-ttu-id="bbbe7-142">Ninguna</span><span class="sxs-lookup"><span data-stu-id="bbbe7-142">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="bbbe7-143">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bbbe7-143">JSON Representation</span></span>
<span data-ttu-id="bbbe7-144">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bbbe7-144">Here is a JSON representation of the resource.</span></span>
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




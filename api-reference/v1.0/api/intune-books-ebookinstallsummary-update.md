---
title: Actualizar eBookInstallSummary
description: Actualice las propiedades de un objeto eBookInstallSummary.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: de522ea7a86c1bec192404870a2aa117a2fa1fe6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27986645"
---
# <a name="update-ebookinstallsummary"></a><span data-ttu-id="2fa1f-103">Actualizar eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="2fa1f-103">Update eBookInstallSummary</span></span>

> <span data-ttu-id="2fa1f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2fa1f-105">Actualice las propiedades de un objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="2fa1f-105">Update the properties of a [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2fa1f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2fa1f-106">Prerequisites</span></span>
<span data-ttu-id="2fa1f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2fa1f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2fa1f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2fa1f-109">Permission type</span></span>|<span data-ttu-id="2fa1f-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2fa1f-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2fa1f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2fa1f-111">Delegated (work or school account)</span></span>|<span data-ttu-id="2fa1f-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2fa1f-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="2fa1f-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2fa1f-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2fa1f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-114">Not supported.</span></span>|
|<span data-ttu-id="2fa1f-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2fa1f-115">Application</span></span>|<span data-ttu-id="2fa1f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2fa1f-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2fa1f-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/installSummary
```

## <a name="request-headers"></a><span data-ttu-id="2fa1f-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2fa1f-118">Request headers</span></span>
|<span data-ttu-id="2fa1f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2fa1f-119">Header</span></span>|<span data-ttu-id="2fa1f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2fa1f-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2fa1f-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="2fa1f-121">Authorization</span></span>|<span data-ttu-id="2fa1f-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2fa1f-123">Accept</span><span class="sxs-lookup"><span data-stu-id="2fa1f-123">Accept</span></span>|<span data-ttu-id="2fa1f-124">application/json</span><span class="sxs-lookup"><span data-stu-id="2fa1f-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2fa1f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2fa1f-125">Request body</span></span>
<span data-ttu-id="2fa1f-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="2fa1f-126">In the request body, supply a JSON representation for the [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) object.</span></span>

<span data-ttu-id="2fa1f-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="2fa1f-127">The following table shows the properties that are required when you create the [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span></span>

|<span data-ttu-id="2fa1f-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2fa1f-128">Property</span></span>|<span data-ttu-id="2fa1f-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fa1f-129">Type</span></span>|<span data-ttu-id="2fa1f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fa1f-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2fa1f-131">id</span><span class="sxs-lookup"><span data-stu-id="2fa1f-131">id</span></span>|<span data-ttu-id="2fa1f-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="2fa1f-132">String</span></span>|<span data-ttu-id="2fa1f-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-133">Key of the entity.</span></span>|
|<span data-ttu-id="2fa1f-134">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="2fa1f-134">installedDeviceCount</span></span>|<span data-ttu-id="2fa1f-135">Int32</span><span class="sxs-lookup"><span data-stu-id="2fa1f-135">Int32</span></span>|<span data-ttu-id="2fa1f-136">Número de dispositivos que han instalado correctamente este libro.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-136">Number of Devices that have successfully installed this book.</span></span>|
|<span data-ttu-id="2fa1f-137">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="2fa1f-137">failedDeviceCount</span></span>|<span data-ttu-id="2fa1f-138">Int32</span><span class="sxs-lookup"><span data-stu-id="2fa1f-138">Int32</span></span>|<span data-ttu-id="2fa1f-139">Número de dispositivos que no han podido instalar este libro.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-139">Number of Devices that have failed to install this book.</span></span>|
|<span data-ttu-id="2fa1f-140">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="2fa1f-140">notInstalledDeviceCount</span></span>|<span data-ttu-id="2fa1f-141">Int32</span><span class="sxs-lookup"><span data-stu-id="2fa1f-141">Int32</span></span>|<span data-ttu-id="2fa1f-142">Número de dispositivos que no han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-142">Number of Devices that does not have this book installed.</span></span>|
|<span data-ttu-id="2fa1f-143">installedUserCount</span><span class="sxs-lookup"><span data-stu-id="2fa1f-143">installedUserCount</span></span>|<span data-ttu-id="2fa1f-144">Int32</span><span class="sxs-lookup"><span data-stu-id="2fa1f-144">Int32</span></span>|<span data-ttu-id="2fa1f-145">Número de usuarios cuyos dispositivos al completo han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-145">Number of Users whose devices have all succeeded to install this book.</span></span>|
|<span data-ttu-id="2fa1f-146">failedUserCount</span><span class="sxs-lookup"><span data-stu-id="2fa1f-146">failedUserCount</span></span>|<span data-ttu-id="2fa1f-147">Int32</span><span class="sxs-lookup"><span data-stu-id="2fa1f-147">Int32</span></span>|<span data-ttu-id="2fa1f-148">Número de usuarios que tienen 1 o más dispositivos que no han podido instalar este libro.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-148">Number of Users that have 1 or more device that failed to install this book.</span></span>|
|<span data-ttu-id="2fa1f-149">notInstalledUserCount</span><span class="sxs-lookup"><span data-stu-id="2fa1f-149">notInstalledUserCount</span></span>|<span data-ttu-id="2fa1f-150">Int32</span><span class="sxs-lookup"><span data-stu-id="2fa1f-150">Int32</span></span>|<span data-ttu-id="2fa1f-151">Número de usuarios que no han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-151">Number of Users that did not install this book.</span></span>|



## <a name="response"></a><span data-ttu-id="2fa1f-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2fa1f-152">Response</span></span>
<span data-ttu-id="2fa1f-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-153">If successful, this method returns a `200 OK` response code and an updated [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2fa1f-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2fa1f-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="2fa1f-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2fa1f-155">Request</span></span>
<span data-ttu-id="2fa1f-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-156">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/installSummary
Content-type: application/json
Content-length: 236

{
  "@odata.type": "#microsoft.graph.eBookInstallSummary",
  "installedDeviceCount": 4,
  "failedDeviceCount": 1,
  "notInstalledDeviceCount": 7,
  "installedUserCount": 2,
  "failedUserCount": 15,
  "notInstalledUserCount": 5
}
```

### <a name="response"></a><span data-ttu-id="2fa1f-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2fa1f-157">Response</span></span>
<span data-ttu-id="2fa1f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 285

{
  "@odata.type": "#microsoft.graph.eBookInstallSummary",
  "id": "9708ad78-ad78-9708-78ad-089778ad0897",
  "installedDeviceCount": 4,
  "failedDeviceCount": 1,
  "notInstalledDeviceCount": 7,
  "installedUserCount": 2,
  "failedUserCount": 15,
  "notInstalledUserCount": 5
}
```




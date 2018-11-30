---
title: Actualizar eBookInstallSummary
description: Actualice las propiedades de un objeto eBookInstallSummary.
ms.openlocfilehash: 261dd70883992b2aa1b2d480407969c1c887c421
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028883"
---
# <a name="update-ebookinstallsummary"></a><span data-ttu-id="32891-103">Actualizar eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="32891-103">Update eBookInstallSummary</span></span>

> <span data-ttu-id="32891-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="32891-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="32891-105">Actualice las propiedades de un objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="32891-105">Update the properties of a [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="32891-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="32891-106">Prerequisites</span></span>
<span data-ttu-id="32891-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="32891-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="32891-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="32891-109">Permission type</span></span>|<span data-ttu-id="32891-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="32891-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="32891-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="32891-111">Delegated (work or school account)</span></span>|<span data-ttu-id="32891-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="32891-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="32891-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="32891-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="32891-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="32891-114">Not supported.</span></span>|
|<span data-ttu-id="32891-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="32891-115">Application</span></span>|<span data-ttu-id="32891-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="32891-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="32891-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="32891-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/installSummary
```

## <a name="request-headers"></a><span data-ttu-id="32891-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="32891-118">Request headers</span></span>
|<span data-ttu-id="32891-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32891-119">Header</span></span>|<span data-ttu-id="32891-120">Valor</span><span class="sxs-lookup"><span data-stu-id="32891-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="32891-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="32891-121">Authorization</span></span>|<span data-ttu-id="32891-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="32891-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="32891-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="32891-123">Accept</span></span>|<span data-ttu-id="32891-124">application/json</span><span class="sxs-lookup"><span data-stu-id="32891-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="32891-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="32891-125">Request body</span></span>
<span data-ttu-id="32891-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="32891-126">In the request body, supply a JSON representation for the [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) object.</span></span>

<span data-ttu-id="32891-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="32891-127">The following table shows the properties that are required when you create the [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span></span>

|<span data-ttu-id="32891-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="32891-128">Property</span></span>|<span data-ttu-id="32891-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="32891-129">Type</span></span>|<span data-ttu-id="32891-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="32891-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="32891-131">id</span><span class="sxs-lookup"><span data-stu-id="32891-131">id</span></span>|<span data-ttu-id="32891-132">String</span><span class="sxs-lookup"><span data-stu-id="32891-132">String</span></span>|<span data-ttu-id="32891-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="32891-133">Key of the entity.</span></span>|
|<span data-ttu-id="32891-134">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="32891-134">installedDeviceCount</span></span>|<span data-ttu-id="32891-135">Int32</span><span class="sxs-lookup"><span data-stu-id="32891-135">Int32</span></span>|<span data-ttu-id="32891-136">Número de dispositivos que han instalado correctamente este libro.</span><span class="sxs-lookup"><span data-stu-id="32891-136">Number of Devices that have successfully installed this book.</span></span>|
|<span data-ttu-id="32891-137">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="32891-137">failedDeviceCount</span></span>|<span data-ttu-id="32891-138">Int32</span><span class="sxs-lookup"><span data-stu-id="32891-138">Int32</span></span>|<span data-ttu-id="32891-139">Número de dispositivos que no han podido instalar este libro.</span><span class="sxs-lookup"><span data-stu-id="32891-139">Number of Devices that have failed to install this book.</span></span>|
|<span data-ttu-id="32891-140">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="32891-140">notInstalledDeviceCount</span></span>|<span data-ttu-id="32891-141">Int32</span><span class="sxs-lookup"><span data-stu-id="32891-141">Int32</span></span>|<span data-ttu-id="32891-142">Número de dispositivos que no han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="32891-142">Number of Devices that does not have this book installed.</span></span>|
|<span data-ttu-id="32891-143">installedUserCount</span><span class="sxs-lookup"><span data-stu-id="32891-143">installedUserCount</span></span>|<span data-ttu-id="32891-144">Int32</span><span class="sxs-lookup"><span data-stu-id="32891-144">Int32</span></span>|<span data-ttu-id="32891-145">Número de usuarios cuyos dispositivos al completo han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="32891-145">Number of Users whose devices have all succeeded to install this book.</span></span>|
|<span data-ttu-id="32891-146">failedUserCount</span><span class="sxs-lookup"><span data-stu-id="32891-146">failedUserCount</span></span>|<span data-ttu-id="32891-147">Int32</span><span class="sxs-lookup"><span data-stu-id="32891-147">Int32</span></span>|<span data-ttu-id="32891-148">Número de usuarios que tienen 1 o más dispositivos que no han podido instalar este libro.</span><span class="sxs-lookup"><span data-stu-id="32891-148">Number of Users that have 1 or more device that failed to install this book.</span></span>|
|<span data-ttu-id="32891-149">notInstalledUserCount</span><span class="sxs-lookup"><span data-stu-id="32891-149">notInstalledUserCount</span></span>|<span data-ttu-id="32891-150">Int32</span><span class="sxs-lookup"><span data-stu-id="32891-150">Int32</span></span>|<span data-ttu-id="32891-151">Número de usuarios que no han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="32891-151">Number of Users that did not install this book.</span></span>|



## <a name="response"></a><span data-ttu-id="32891-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32891-152">Response</span></span>
<span data-ttu-id="32891-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="32891-153">If successful, this method returns a `200 OK` response code and an updated [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="32891-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="32891-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="32891-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="32891-155">Request</span></span>
<span data-ttu-id="32891-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="32891-156">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="32891-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32891-157">Response</span></span>
<span data-ttu-id="32891-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="32891-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




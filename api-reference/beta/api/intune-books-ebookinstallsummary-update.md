---
title: Actualizar eBookInstallSummary
description: Actualice las propiedades de un objeto eBookInstallSummary.
author: tfitzmac
ms.openlocfilehash: b110646f51ce8c48e15bd8c5fbaa5e025952babc
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27350732"
---
# <a name="update-ebookinstallsummary"></a><span data-ttu-id="6884e-103">Actualizar eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="6884e-103">Update eBookInstallSummary</span></span>

> <span data-ttu-id="6884e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6884e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6884e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6884e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6884e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6884e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6884e-107">Actualice las propiedades de un objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="6884e-107">Update the properties of a [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6884e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6884e-108">Prerequisites</span></span>
<span data-ttu-id="6884e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6884e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6884e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6884e-111">Permission type</span></span>|<span data-ttu-id="6884e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6884e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6884e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6884e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="6884e-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6884e-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="6884e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6884e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6884e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6884e-116">Not supported.</span></span>|
|<span data-ttu-id="6884e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6884e-117">Application</span></span>|<span data-ttu-id="6884e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6884e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6884e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6884e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/installSummary
```

## <a name="request-headers"></a><span data-ttu-id="6884e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6884e-120">Request headers</span></span>
|<span data-ttu-id="6884e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6884e-121">Header</span></span>|<span data-ttu-id="6884e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6884e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6884e-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="6884e-123">Authorization</span></span>|<span data-ttu-id="6884e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6884e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6884e-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6884e-125">Accept</span></span>|<span data-ttu-id="6884e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6884e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6884e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6884e-127">Request body</span></span>
<span data-ttu-id="6884e-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="6884e-128">In the request body, supply a JSON representation for the [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) object.</span></span>

<span data-ttu-id="6884e-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="6884e-129">The following table shows the properties that are required when you create the [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).</span></span>

|<span data-ttu-id="6884e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6884e-130">Property</span></span>|<span data-ttu-id="6884e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6884e-131">Type</span></span>|<span data-ttu-id="6884e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6884e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6884e-133">id</span><span class="sxs-lookup"><span data-stu-id="6884e-133">id</span></span>|<span data-ttu-id="6884e-134">String</span><span class="sxs-lookup"><span data-stu-id="6884e-134">String</span></span>|<span data-ttu-id="6884e-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6884e-135">Key of the entity.</span></span>|
|<span data-ttu-id="6884e-136">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6884e-136">installedDeviceCount</span></span>|<span data-ttu-id="6884e-137">Int32</span><span class="sxs-lookup"><span data-stu-id="6884e-137">Int32</span></span>|<span data-ttu-id="6884e-138">Número de dispositivos que han instalado correctamente este libro.</span><span class="sxs-lookup"><span data-stu-id="6884e-138">Number of Devices that have successfully installed this book.</span></span>|
|<span data-ttu-id="6884e-139">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6884e-139">failedDeviceCount</span></span>|<span data-ttu-id="6884e-140">Int32</span><span class="sxs-lookup"><span data-stu-id="6884e-140">Int32</span></span>|<span data-ttu-id="6884e-141">Número de dispositivos que no han podido instalar este libro.</span><span class="sxs-lookup"><span data-stu-id="6884e-141">Number of Devices that have failed to install this book.</span></span>|
|<span data-ttu-id="6884e-142">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6884e-142">notInstalledDeviceCount</span></span>|<span data-ttu-id="6884e-143">Int32</span><span class="sxs-lookup"><span data-stu-id="6884e-143">Int32</span></span>|<span data-ttu-id="6884e-144">Número de dispositivos que no han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="6884e-144">Number of Devices that does not have this book installed.</span></span>|
|<span data-ttu-id="6884e-145">installedUserCount</span><span class="sxs-lookup"><span data-stu-id="6884e-145">installedUserCount</span></span>|<span data-ttu-id="6884e-146">Int32</span><span class="sxs-lookup"><span data-stu-id="6884e-146">Int32</span></span>|<span data-ttu-id="6884e-147">Número de usuarios cuyos dispositivos al completo han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="6884e-147">Number of Users whose devices have all succeeded to install this book.</span></span>|
|<span data-ttu-id="6884e-148">failedUserCount</span><span class="sxs-lookup"><span data-stu-id="6884e-148">failedUserCount</span></span>|<span data-ttu-id="6884e-149">Int32</span><span class="sxs-lookup"><span data-stu-id="6884e-149">Int32</span></span>|<span data-ttu-id="6884e-150">Número de usuarios que tienen 1 o más dispositivos que no han podido instalar este libro.</span><span class="sxs-lookup"><span data-stu-id="6884e-150">Number of Users that have 1 or more device that failed to install this book.</span></span>|
|<span data-ttu-id="6884e-151">notInstalledUserCount</span><span class="sxs-lookup"><span data-stu-id="6884e-151">notInstalledUserCount</span></span>|<span data-ttu-id="6884e-152">Int32</span><span class="sxs-lookup"><span data-stu-id="6884e-152">Int32</span></span>|<span data-ttu-id="6884e-153">Número de usuarios que no han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="6884e-153">Number of Users that did not install this book.</span></span>|



## <a name="response"></a><span data-ttu-id="6884e-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6884e-154">Response</span></span>
<span data-ttu-id="6884e-155">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6884e-155">If successful, this method returns a `200 OK` response code and an updated [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6884e-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6884e-156">Example</span></span>
### <a name="request"></a><span data-ttu-id="6884e-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6884e-157">Request</span></span>
<span data-ttu-id="6884e-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6884e-158">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/managedEBooks/{managedEBookId}/installSummary
Content-type: application/json
Content-length: 178

{
  "installedDeviceCount": 4,
  "failedDeviceCount": 1,
  "notInstalledDeviceCount": 7,
  "installedUserCount": 2,
  "failedUserCount": 15,
  "notInstalledUserCount": 5
}
```

### <a name="response"></a><span data-ttu-id="6884e-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6884e-159">Response</span></span>
<span data-ttu-id="6884e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6884e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






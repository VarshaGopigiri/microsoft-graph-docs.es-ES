---
title: Crear userInstallStateSummary
description: Cree un objeto userInstallStateSummary.
author: tfitzmac
ms.openlocfilehash: a1da2855896bae9d9c902ae978d3ce8c127f3bc4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27318420"
---
# <a name="create-userinstallstatesummary"></a><span data-ttu-id="fce0e-103">Crear userInstallStateSummary</span><span class="sxs-lookup"><span data-stu-id="fce0e-103">Create userInstallStateSummary</span></span>

> <span data-ttu-id="fce0e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fce0e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fce0e-105">Cree un objeto [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="fce0e-105">Create a new [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fce0e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fce0e-106">Prerequisites</span></span>
<span data-ttu-id="fce0e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fce0e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fce0e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fce0e-109">Permission type</span></span>|<span data-ttu-id="fce0e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fce0e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fce0e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fce0e-111">Delegated (work or school account)</span></span>|<span data-ttu-id="fce0e-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fce0e-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="fce0e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fce0e-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fce0e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fce0e-114">Not supported.</span></span>|
|<span data-ttu-id="fce0e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fce0e-115">Application</span></span>|<span data-ttu-id="fce0e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fce0e-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fce0e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fce0e-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary
```

## <a name="request-headers"></a><span data-ttu-id="fce0e-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fce0e-118">Request headers</span></span>
|<span data-ttu-id="fce0e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fce0e-119">Header</span></span>|<span data-ttu-id="fce0e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fce0e-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fce0e-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="fce0e-121">Authorization</span></span>|<span data-ttu-id="fce0e-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fce0e-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fce0e-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="fce0e-123">Accept</span></span>|<span data-ttu-id="fce0e-124">application/json</span><span class="sxs-lookup"><span data-stu-id="fce0e-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fce0e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fce0e-125">Request body</span></span>
<span data-ttu-id="fce0e-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto userInstallStateSummary.</span><span class="sxs-lookup"><span data-stu-id="fce0e-126">In the request body, supply a JSON representation for the userInstallStateSummary object.</span></span>

<span data-ttu-id="fce0e-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto userInstallStateSummary.</span><span class="sxs-lookup"><span data-stu-id="fce0e-127">The following table shows the properties that are required when you create the userInstallStateSummary.</span></span>

|<span data-ttu-id="fce0e-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fce0e-128">Property</span></span>|<span data-ttu-id="fce0e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="fce0e-129">Type</span></span>|<span data-ttu-id="fce0e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="fce0e-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fce0e-131">id</span><span class="sxs-lookup"><span data-stu-id="fce0e-131">id</span></span>|<span data-ttu-id="fce0e-132">String</span><span class="sxs-lookup"><span data-stu-id="fce0e-132">String</span></span>|<span data-ttu-id="fce0e-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="fce0e-133">Key of the entity.</span></span>|
|<span data-ttu-id="fce0e-134">userName</span><span class="sxs-lookup"><span data-stu-id="fce0e-134">userName</span></span>|<span data-ttu-id="fce0e-135">String</span><span class="sxs-lookup"><span data-stu-id="fce0e-135">String</span></span>|<span data-ttu-id="fce0e-136">Nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="fce0e-136">User name.</span></span>|
|<span data-ttu-id="fce0e-137">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="fce0e-137">installedDeviceCount</span></span>|<span data-ttu-id="fce0e-138">Int32</span><span class="sxs-lookup"><span data-stu-id="fce0e-138">Int32</span></span>|<span data-ttu-id="fce0e-139">Número de dispositivos instalados.</span><span class="sxs-lookup"><span data-stu-id="fce0e-139">Installed Device Count.</span></span>|
|<span data-ttu-id="fce0e-140">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="fce0e-140">failedDeviceCount</span></span>|<span data-ttu-id="fce0e-141">Int32</span><span class="sxs-lookup"><span data-stu-id="fce0e-141">Int32</span></span>|<span data-ttu-id="fce0e-142">Número de dispositivos erróneos.</span><span class="sxs-lookup"><span data-stu-id="fce0e-142">Failed Device Count.</span></span>|
|<span data-ttu-id="fce0e-143">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="fce0e-143">notInstalledDeviceCount</span></span>|<span data-ttu-id="fce0e-144">Int32</span><span class="sxs-lookup"><span data-stu-id="fce0e-144">Int32</span></span>|<span data-ttu-id="fce0e-145">Número de dispositivos no instalados.</span><span class="sxs-lookup"><span data-stu-id="fce0e-145">Not installed device count.</span></span>|



## <a name="response"></a><span data-ttu-id="fce0e-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fce0e-146">Response</span></span>
<span data-ttu-id="fce0e-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fce0e-147">If successful, this method returns a `201 Created` response code and a [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fce0e-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fce0e-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="fce0e-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fce0e-149">Request</span></span>
<span data-ttu-id="fce0e-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fce0e-150">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary
Content-type: application/json
Content-length: 189

{
  "@odata.type": "#microsoft.graph.userInstallStateSummary",
  "userName": "User Name value",
  "installedDeviceCount": 4,
  "failedDeviceCount": 1,
  "notInstalledDeviceCount": 7
}
```

### <a name="response"></a><span data-ttu-id="fce0e-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fce0e-151">Response</span></span>
<span data-ttu-id="fce0e-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fce0e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 238

{
  "@odata.type": "#microsoft.graph.userInstallStateSummary",
  "id": "1e5b41ba-41ba-1e5b-ba41-5b1eba415b1e",
  "userName": "User Name value",
  "installedDeviceCount": 4,
  "failedDeviceCount": 1,
  "notInstalledDeviceCount": 7
}
```




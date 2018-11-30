---
title: Actualizar userInstallStateSummary
description: Actualice las propiedades de un objeto userInstallStateSummary.
ms.openlocfilehash: b161cac0cc2d3ee0fd31662318ef2bb94232dc63
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089516"
---
# <a name="update-userinstallstatesummary"></a><span data-ttu-id="5bf45-103">Actualizar userInstallStateSummary</span><span class="sxs-lookup"><span data-stu-id="5bf45-103">Update userInstallStateSummary</span></span>

> <span data-ttu-id="5bf45-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5bf45-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5bf45-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5bf45-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5bf45-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5bf45-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5bf45-107">Actualice las propiedades de un objeto [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="5bf45-107">Update the properties of a [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5bf45-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5bf45-108">Prerequisites</span></span>
<span data-ttu-id="5bf45-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5bf45-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5bf45-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5bf45-111">Permission type</span></span>|<span data-ttu-id="5bf45-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5bf45-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5bf45-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5bf45-113">Delegated (work or school account)</span></span>|<span data-ttu-id="5bf45-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5bf45-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="5bf45-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5bf45-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5bf45-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5bf45-116">Not supported.</span></span>|
|<span data-ttu-id="5bf45-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5bf45-117">Application</span></span>|<span data-ttu-id="5bf45-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5bf45-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5bf45-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5bf45-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary/{userInstallStateSummaryId}
```

## <a name="request-headers"></a><span data-ttu-id="5bf45-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5bf45-120">Request headers</span></span>
|<span data-ttu-id="5bf45-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5bf45-121">Header</span></span>|<span data-ttu-id="5bf45-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5bf45-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5bf45-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="5bf45-123">Authorization</span></span>|<span data-ttu-id="5bf45-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5bf45-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5bf45-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5bf45-125">Accept</span></span>|<span data-ttu-id="5bf45-126">application/json</span><span class="sxs-lookup"><span data-stu-id="5bf45-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5bf45-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5bf45-127">Request body</span></span>
<span data-ttu-id="5bf45-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="5bf45-128">In the request body, supply a JSON representation for the [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) object.</span></span>

<span data-ttu-id="5bf45-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="5bf45-129">The following table shows the properties that are required when you create the [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md).</span></span>

|<span data-ttu-id="5bf45-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5bf45-130">Property</span></span>|<span data-ttu-id="5bf45-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="5bf45-131">Type</span></span>|<span data-ttu-id="5bf45-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="5bf45-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5bf45-133">id</span><span class="sxs-lookup"><span data-stu-id="5bf45-133">id</span></span>|<span data-ttu-id="5bf45-134">String</span><span class="sxs-lookup"><span data-stu-id="5bf45-134">String</span></span>|<span data-ttu-id="5bf45-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5bf45-135">Key of the entity.</span></span>|
|<span data-ttu-id="5bf45-136">userName</span><span class="sxs-lookup"><span data-stu-id="5bf45-136">userName</span></span>|<span data-ttu-id="5bf45-137">String</span><span class="sxs-lookup"><span data-stu-id="5bf45-137">String</span></span>|<span data-ttu-id="5bf45-138">Nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="5bf45-138">User name.</span></span>|
|<span data-ttu-id="5bf45-139">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="5bf45-139">installedDeviceCount</span></span>|<span data-ttu-id="5bf45-140">Int32</span><span class="sxs-lookup"><span data-stu-id="5bf45-140">Int32</span></span>|<span data-ttu-id="5bf45-141">Número de dispositivos instalados.</span><span class="sxs-lookup"><span data-stu-id="5bf45-141">Installed Device Count.</span></span>|
|<span data-ttu-id="5bf45-142">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="5bf45-142">failedDeviceCount</span></span>|<span data-ttu-id="5bf45-143">Int32</span><span class="sxs-lookup"><span data-stu-id="5bf45-143">Int32</span></span>|<span data-ttu-id="5bf45-144">Número de dispositivos erróneos.</span><span class="sxs-lookup"><span data-stu-id="5bf45-144">Failed Device Count.</span></span>|
|<span data-ttu-id="5bf45-145">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="5bf45-145">notInstalledDeviceCount</span></span>|<span data-ttu-id="5bf45-146">Int32</span><span class="sxs-lookup"><span data-stu-id="5bf45-146">Int32</span></span>|<span data-ttu-id="5bf45-147">Número de dispositivos no instalados.</span><span class="sxs-lookup"><span data-stu-id="5bf45-147">Not installed device count.</span></span>|



## <a name="response"></a><span data-ttu-id="5bf45-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5bf45-148">Response</span></span>
<span data-ttu-id="5bf45-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5bf45-149">If successful, this method returns a `200 OK` response code and an updated [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5bf45-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5bf45-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="5bf45-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5bf45-151">Request</span></span>
<span data-ttu-id="5bf45-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5bf45-152">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary/{userInstallStateSummaryId}
Content-type: application/json
Content-length: 127

{
  "userName": "User Name value",
  "installedDeviceCount": 4,
  "failedDeviceCount": 1,
  "notInstalledDeviceCount": 7
}
```

### <a name="response"></a><span data-ttu-id="5bf45-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5bf45-153">Response</span></span>
<span data-ttu-id="5bf45-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5bf45-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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






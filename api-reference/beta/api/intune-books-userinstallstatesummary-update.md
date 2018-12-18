---
title: Actualizar userInstallStateSummary
description: Actualice las propiedades de un objeto userInstallStateSummary.
author: tfitzmac
ms.openlocfilehash: 10129a9a18030498add1b8e3c0b664f2aa921de6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27316467"
---
# <a name="update-userinstallstatesummary"></a><span data-ttu-id="f27ad-103">Actualizar userInstallStateSummary</span><span class="sxs-lookup"><span data-stu-id="f27ad-103">Update userInstallStateSummary</span></span>

> <span data-ttu-id="f27ad-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f27ad-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f27ad-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f27ad-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f27ad-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f27ad-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f27ad-107">Actualice las propiedades de un objeto [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="f27ad-107">Update the properties of a [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f27ad-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f27ad-108">Prerequisites</span></span>
<span data-ttu-id="f27ad-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f27ad-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f27ad-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f27ad-111">Permission type</span></span>|<span data-ttu-id="f27ad-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f27ad-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f27ad-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f27ad-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f27ad-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f27ad-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f27ad-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f27ad-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f27ad-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f27ad-116">Not supported.</span></span>|
|<span data-ttu-id="f27ad-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f27ad-117">Application</span></span>|<span data-ttu-id="f27ad-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f27ad-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f27ad-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f27ad-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary/{userInstallStateSummaryId}
```

## <a name="request-headers"></a><span data-ttu-id="f27ad-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f27ad-120">Request headers</span></span>
|<span data-ttu-id="f27ad-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f27ad-121">Header</span></span>|<span data-ttu-id="f27ad-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f27ad-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f27ad-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f27ad-123">Authorization</span></span>|<span data-ttu-id="f27ad-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f27ad-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f27ad-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f27ad-125">Accept</span></span>|<span data-ttu-id="f27ad-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f27ad-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f27ad-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f27ad-127">Request body</span></span>
<span data-ttu-id="f27ad-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="f27ad-128">In the request body, supply a JSON representation for the [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) object.</span></span>

<span data-ttu-id="f27ad-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="f27ad-129">The following table shows the properties that are required when you create the [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md).</span></span>

|<span data-ttu-id="f27ad-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f27ad-130">Property</span></span>|<span data-ttu-id="f27ad-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f27ad-131">Type</span></span>|<span data-ttu-id="f27ad-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f27ad-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f27ad-133">id</span><span class="sxs-lookup"><span data-stu-id="f27ad-133">id</span></span>|<span data-ttu-id="f27ad-134">String</span><span class="sxs-lookup"><span data-stu-id="f27ad-134">String</span></span>|<span data-ttu-id="f27ad-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f27ad-135">Key of the entity.</span></span>|
|<span data-ttu-id="f27ad-136">userName</span><span class="sxs-lookup"><span data-stu-id="f27ad-136">userName</span></span>|<span data-ttu-id="f27ad-137">String</span><span class="sxs-lookup"><span data-stu-id="f27ad-137">String</span></span>|<span data-ttu-id="f27ad-138">Nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="f27ad-138">User name.</span></span>|
|<span data-ttu-id="f27ad-139">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="f27ad-139">installedDeviceCount</span></span>|<span data-ttu-id="f27ad-140">Int32</span><span class="sxs-lookup"><span data-stu-id="f27ad-140">Int32</span></span>|<span data-ttu-id="f27ad-141">Número de dispositivos instalados.</span><span class="sxs-lookup"><span data-stu-id="f27ad-141">Installed Device Count.</span></span>|
|<span data-ttu-id="f27ad-142">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="f27ad-142">failedDeviceCount</span></span>|<span data-ttu-id="f27ad-143">Int32</span><span class="sxs-lookup"><span data-stu-id="f27ad-143">Int32</span></span>|<span data-ttu-id="f27ad-144">Número de dispositivos erróneos.</span><span class="sxs-lookup"><span data-stu-id="f27ad-144">Failed Device Count.</span></span>|
|<span data-ttu-id="f27ad-145">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="f27ad-145">notInstalledDeviceCount</span></span>|<span data-ttu-id="f27ad-146">Int32</span><span class="sxs-lookup"><span data-stu-id="f27ad-146">Int32</span></span>|<span data-ttu-id="f27ad-147">Número de dispositivos no instalados.</span><span class="sxs-lookup"><span data-stu-id="f27ad-147">Not installed device count.</span></span>|



## <a name="response"></a><span data-ttu-id="f27ad-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f27ad-148">Response</span></span>
<span data-ttu-id="f27ad-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f27ad-149">If successful, this method returns a `200 OK` response code and an updated [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f27ad-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f27ad-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="f27ad-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f27ad-151">Request</span></span>
<span data-ttu-id="f27ad-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f27ad-152">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="f27ad-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f27ad-153">Response</span></span>
<span data-ttu-id="f27ad-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f27ad-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






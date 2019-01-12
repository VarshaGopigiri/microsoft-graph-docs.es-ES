---
title: Crear userInstallStateSummary
description: Cree un objeto userInstallStateSummary.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b738e79c832fbfde23bfa48a84573c6d5c8f3e98
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950259"
---
# <a name="create-userinstallstatesummary"></a><span data-ttu-id="deeca-103">Crear userInstallStateSummary</span><span class="sxs-lookup"><span data-stu-id="deeca-103">Create userInstallStateSummary</span></span>

> <span data-ttu-id="deeca-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="deeca-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="deeca-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="deeca-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="deeca-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="deeca-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="deeca-107">Cree un objeto [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="deeca-107">Create a new [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="deeca-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="deeca-108">Prerequisites</span></span>
<span data-ttu-id="deeca-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="deeca-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="deeca-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="deeca-111">Permission type</span></span>|<span data-ttu-id="deeca-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="deeca-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="deeca-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="deeca-113">Delegated (work or school account)</span></span>|<span data-ttu-id="deeca-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="deeca-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="deeca-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="deeca-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="deeca-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="deeca-116">Not supported.</span></span>|
|<span data-ttu-id="deeca-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="deeca-117">Application</span></span>|<span data-ttu-id="deeca-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="deeca-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="deeca-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="deeca-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary
```

## <a name="request-headers"></a><span data-ttu-id="deeca-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="deeca-120">Request headers</span></span>
|<span data-ttu-id="deeca-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="deeca-121">Header</span></span>|<span data-ttu-id="deeca-122">Valor</span><span class="sxs-lookup"><span data-stu-id="deeca-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="deeca-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="deeca-123">Authorization</span></span>|<span data-ttu-id="deeca-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="deeca-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="deeca-125">Accept</span><span class="sxs-lookup"><span data-stu-id="deeca-125">Accept</span></span>|<span data-ttu-id="deeca-126">application/json</span><span class="sxs-lookup"><span data-stu-id="deeca-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="deeca-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="deeca-127">Request body</span></span>
<span data-ttu-id="deeca-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto userInstallStateSummary.</span><span class="sxs-lookup"><span data-stu-id="deeca-128">In the request body, supply a JSON representation for the userInstallStateSummary object.</span></span>

<span data-ttu-id="deeca-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto userInstallStateSummary.</span><span class="sxs-lookup"><span data-stu-id="deeca-129">The following table shows the properties that are required when you create the userInstallStateSummary.</span></span>

|<span data-ttu-id="deeca-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="deeca-130">Property</span></span>|<span data-ttu-id="deeca-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="deeca-131">Type</span></span>|<span data-ttu-id="deeca-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="deeca-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="deeca-133">id</span><span class="sxs-lookup"><span data-stu-id="deeca-133">id</span></span>|<span data-ttu-id="deeca-134">String</span><span class="sxs-lookup"><span data-stu-id="deeca-134">String</span></span>|<span data-ttu-id="deeca-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="deeca-135">Key of the entity.</span></span>|
|<span data-ttu-id="deeca-136">userName</span><span class="sxs-lookup"><span data-stu-id="deeca-136">userName</span></span>|<span data-ttu-id="deeca-137">String</span><span class="sxs-lookup"><span data-stu-id="deeca-137">String</span></span>|<span data-ttu-id="deeca-138">Nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="deeca-138">User name.</span></span>|
|<span data-ttu-id="deeca-139">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="deeca-139">installedDeviceCount</span></span>|<span data-ttu-id="deeca-140">Int32</span><span class="sxs-lookup"><span data-stu-id="deeca-140">Int32</span></span>|<span data-ttu-id="deeca-141">Número de dispositivos instalados.</span><span class="sxs-lookup"><span data-stu-id="deeca-141">Installed Device Count.</span></span>|
|<span data-ttu-id="deeca-142">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="deeca-142">failedDeviceCount</span></span>|<span data-ttu-id="deeca-143">Int32</span><span class="sxs-lookup"><span data-stu-id="deeca-143">Int32</span></span>|<span data-ttu-id="deeca-144">Número de dispositivos erróneos.</span><span class="sxs-lookup"><span data-stu-id="deeca-144">Failed Device Count.</span></span>|
|<span data-ttu-id="deeca-145">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="deeca-145">notInstalledDeviceCount</span></span>|<span data-ttu-id="deeca-146">Int32</span><span class="sxs-lookup"><span data-stu-id="deeca-146">Int32</span></span>|<span data-ttu-id="deeca-147">Número de dispositivos no instalados.</span><span class="sxs-lookup"><span data-stu-id="deeca-147">Not installed device count.</span></span>|



## <a name="response"></a><span data-ttu-id="deeca-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="deeca-148">Response</span></span>
<span data-ttu-id="deeca-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="deeca-149">If successful, this method returns a `201 Created` response code and a [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="deeca-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="deeca-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="deeca-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="deeca-151">Request</span></span>
<span data-ttu-id="deeca-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="deeca-152">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary
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

### <a name="response"></a><span data-ttu-id="deeca-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="deeca-153">Response</span></span>
<span data-ttu-id="deeca-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="deeca-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






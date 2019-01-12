---
title: Crear windowsInformationProtectionAppLockerFile
description: Cree un objeto windowsInformationProtectionAppLockerFile.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a7b6bfb8271e6b462be1d18fd509da33aea836b3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27967598"
---
# <a name="create-windowsinformationprotectionapplockerfile"></a><span data-ttu-id="7e0d6-103">Crear windowsInformationProtectionAppLockerFile</span><span class="sxs-lookup"><span data-stu-id="7e0d6-103">Create windowsInformationProtectionAppLockerFile</span></span>

> <span data-ttu-id="7e0d6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7e0d6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7e0d6-105">Cree un objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).</span><span class="sxs-lookup"><span data-stu-id="7e0d6-105">Create a new [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7e0d6-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7e0d6-106">Prerequisites</span></span>
<span data-ttu-id="7e0d6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7e0d6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7e0d6-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7e0d6-109">Permission type</span></span>|<span data-ttu-id="7e0d6-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7e0d6-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7e0d6-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7e0d6-111">Delegated (work or school account)</span></span>|<span data-ttu-id="7e0d6-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7e0d6-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="7e0d6-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7e0d6-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7e0d6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7e0d6-114">Not supported.</span></span>|
|<span data-ttu-id="7e0d6-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7e0d6-115">Application</span></span>|<span data-ttu-id="7e0d6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7e0d6-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7e0d6-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7e0d6-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/exemptAppLockerFiles
POST /deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/protectedAppLockerFiles
POST /deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}/exemptAppLockerFiles
POST /deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}/protectedAppLockerFiles
```

## <a name="request-headers"></a><span data-ttu-id="7e0d6-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7e0d6-118">Request headers</span></span>
|<span data-ttu-id="7e0d6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e0d6-119">Header</span></span>|<span data-ttu-id="7e0d6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7e0d6-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7e0d6-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="7e0d6-121">Authorization</span></span>|<span data-ttu-id="7e0d6-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7e0d6-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7e0d6-123">Accept</span><span class="sxs-lookup"><span data-stu-id="7e0d6-123">Accept</span></span>|<span data-ttu-id="7e0d6-124">application/json</span><span class="sxs-lookup"><span data-stu-id="7e0d6-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7e0d6-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7e0d6-125">Request body</span></span>
<span data-ttu-id="7e0d6-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsInformationProtectionAppLockerFile.</span><span class="sxs-lookup"><span data-stu-id="7e0d6-126">In the request body, supply a JSON representation for the windowsInformationProtectionAppLockerFile object.</span></span>

<span data-ttu-id="7e0d6-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsInformationProtectionAppLockerFile.</span><span class="sxs-lookup"><span data-stu-id="7e0d6-127">The following table shows the properties that are required when you create the windowsInformationProtectionAppLockerFile.</span></span>

|<span data-ttu-id="7e0d6-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7e0d6-128">Property</span></span>|<span data-ttu-id="7e0d6-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e0d6-129">Type</span></span>|<span data-ttu-id="7e0d6-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e0d6-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7e0d6-131">displayName</span><span class="sxs-lookup"><span data-stu-id="7e0d6-131">displayName</span></span>|<span data-ttu-id="7e0d6-132">String</span><span class="sxs-lookup"><span data-stu-id="7e0d6-132">String</span></span>|<span data-ttu-id="7e0d6-133">El nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="7e0d6-133">The friendly name</span></span>|
|<span data-ttu-id="7e0d6-134">fileHash</span><span class="sxs-lookup"><span data-stu-id="7e0d6-134">fileHash</span></span>|<span data-ttu-id="7e0d6-135">String</span><span class="sxs-lookup"><span data-stu-id="7e0d6-135">String</span></span>|<span data-ttu-id="7e0d6-136">Hash del archivo SHA256</span><span class="sxs-lookup"><span data-stu-id="7e0d6-136">SHA256 hash of the file</span></span>|
|<span data-ttu-id="7e0d6-137">file</span><span class="sxs-lookup"><span data-stu-id="7e0d6-137">file</span></span>|<span data-ttu-id="7e0d6-138">Binario</span><span class="sxs-lookup"><span data-stu-id="7e0d6-138">Binary</span></span>|<span data-ttu-id="7e0d6-139">Archivo como una matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="7e0d6-139">File as a byte array</span></span>|
|<span data-ttu-id="7e0d6-140">id</span><span class="sxs-lookup"><span data-stu-id="7e0d6-140">id</span></span>|<span data-ttu-id="7e0d6-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="7e0d6-141">String</span></span>|<span data-ttu-id="7e0d6-142">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7e0d6-142">Key of the entity.</span></span>|
|<span data-ttu-id="7e0d6-143">version</span><span class="sxs-lookup"><span data-stu-id="7e0d6-143">version</span></span>|<span data-ttu-id="7e0d6-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="7e0d6-144">String</span></span>|<span data-ttu-id="7e0d6-145">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7e0d6-145">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="7e0d6-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e0d6-146">Response</span></span>
<span data-ttu-id="7e0d6-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e0d6-147">If successful, this method returns a `201 Created` response code and a [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7e0d6-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7e0d6-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="7e0d6-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7e0d6-149">Request</span></span>
<span data-ttu-id="7e0d6-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7e0d6-150">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/exemptAppLockerFiles
Content-type: application/json
Content-length: 211

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLockerFile",
  "displayName": "Display Name value",
  "fileHash": "File Hash value",
  "file": "ZmlsZQ==",
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="7e0d6-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e0d6-151">Response</span></span>
<span data-ttu-id="7e0d6-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7e0d6-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 260

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLockerFile",
  "displayName": "Display Name value",
  "fileHash": "File Hash value",
  "file": "ZmlsZQ==",
  "id": "d81f0e40-0e40-d81f-400e-1fd8400e1fd8",
  "version": "Version value"
}
```




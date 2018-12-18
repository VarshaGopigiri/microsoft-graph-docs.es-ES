---
title: Crear windowsInformationProtectionAppLockerFile
description: Cree un objeto windowsInformationProtectionAppLockerFile.
author: tfitzmac
ms.openlocfilehash: affd7838727ee79e4eef79a87b4dd4358cf4bb6a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334429"
---
# <a name="create-windowsinformationprotectionapplockerfile"></a><span data-ttu-id="62f20-103">Crear windowsInformationProtectionAppLockerFile</span><span class="sxs-lookup"><span data-stu-id="62f20-103">Create windowsInformationProtectionAppLockerFile</span></span>

> <span data-ttu-id="62f20-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="62f20-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="62f20-105">Cree un objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).</span><span class="sxs-lookup"><span data-stu-id="62f20-105">Create a new [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="62f20-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="62f20-106">Prerequisites</span></span>
<span data-ttu-id="62f20-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="62f20-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="62f20-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="62f20-109">Permission type</span></span>|<span data-ttu-id="62f20-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="62f20-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="62f20-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="62f20-111">Delegated (work or school account)</span></span>|<span data-ttu-id="62f20-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="62f20-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="62f20-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="62f20-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="62f20-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="62f20-114">Not supported.</span></span>|
|<span data-ttu-id="62f20-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="62f20-115">Application</span></span>|<span data-ttu-id="62f20-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="62f20-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="62f20-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="62f20-117">HTTP Request</span></span>
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

## <a name="request-headers"></a><span data-ttu-id="62f20-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="62f20-118">Request headers</span></span>
|<span data-ttu-id="62f20-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62f20-119">Header</span></span>|<span data-ttu-id="62f20-120">Valor</span><span class="sxs-lookup"><span data-stu-id="62f20-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="62f20-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="62f20-121">Authorization</span></span>|<span data-ttu-id="62f20-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="62f20-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="62f20-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="62f20-123">Accept</span></span>|<span data-ttu-id="62f20-124">application/json</span><span class="sxs-lookup"><span data-stu-id="62f20-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="62f20-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="62f20-125">Request body</span></span>
<span data-ttu-id="62f20-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsInformationProtectionAppLockerFile.</span><span class="sxs-lookup"><span data-stu-id="62f20-126">In the request body, supply a JSON representation for the windowsInformationProtectionAppLockerFile object.</span></span>

<span data-ttu-id="62f20-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsInformationProtectionAppLockerFile.</span><span class="sxs-lookup"><span data-stu-id="62f20-127">The following table shows the properties that are required when you create the windowsInformationProtectionAppLockerFile.</span></span>

|<span data-ttu-id="62f20-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="62f20-128">Property</span></span>|<span data-ttu-id="62f20-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="62f20-129">Type</span></span>|<span data-ttu-id="62f20-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="62f20-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="62f20-131">displayName</span><span class="sxs-lookup"><span data-stu-id="62f20-131">displayName</span></span>|<span data-ttu-id="62f20-132">String</span><span class="sxs-lookup"><span data-stu-id="62f20-132">String</span></span>|<span data-ttu-id="62f20-133">El nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="62f20-133">The friendly name</span></span>|
|<span data-ttu-id="62f20-134">fileHash</span><span class="sxs-lookup"><span data-stu-id="62f20-134">fileHash</span></span>|<span data-ttu-id="62f20-135">String</span><span class="sxs-lookup"><span data-stu-id="62f20-135">String</span></span>|<span data-ttu-id="62f20-136">Hash del archivo SHA256</span><span class="sxs-lookup"><span data-stu-id="62f20-136">SHA256 hash of the file</span></span>|
|<span data-ttu-id="62f20-137">file</span><span class="sxs-lookup"><span data-stu-id="62f20-137">file</span></span>|<span data-ttu-id="62f20-138">Binario</span><span class="sxs-lookup"><span data-stu-id="62f20-138">Binary</span></span>|<span data-ttu-id="62f20-139">Archivo como una matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="62f20-139">File as a byte array</span></span>|
|<span data-ttu-id="62f20-140">id</span><span class="sxs-lookup"><span data-stu-id="62f20-140">id</span></span>|<span data-ttu-id="62f20-141">String</span><span class="sxs-lookup"><span data-stu-id="62f20-141">String</span></span>|<span data-ttu-id="62f20-142">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="62f20-142">Key of the entity.</span></span>|
|<span data-ttu-id="62f20-143">version</span><span class="sxs-lookup"><span data-stu-id="62f20-143">version</span></span>|<span data-ttu-id="62f20-144">String</span><span class="sxs-lookup"><span data-stu-id="62f20-144">String</span></span>|<span data-ttu-id="62f20-145">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="62f20-145">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="62f20-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="62f20-146">Response</span></span>
<span data-ttu-id="62f20-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="62f20-147">If successful, this method returns a `201 Created` response code and a [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="62f20-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="62f20-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="62f20-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="62f20-149">Request</span></span>
<span data-ttu-id="62f20-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="62f20-150">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="62f20-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="62f20-151">Response</span></span>
<span data-ttu-id="62f20-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="62f20-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




---
title: Crear windowsInformationProtectionAppLockerFile
description: Cree un objeto windowsInformationProtectionAppLockerFile.
ms.openlocfilehash: a5496b599506e81e10e8a1f7d502796bdcb8d0f8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032151"
---
# <a name="create-windowsinformationprotectionapplockerfile"></a><span data-ttu-id="7126c-103">Crear windowsInformationProtectionAppLockerFile</span><span class="sxs-lookup"><span data-stu-id="7126c-103">Create windowsInformationProtectionAppLockerFile</span></span>

> <span data-ttu-id="7126c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7126c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7126c-105">Cree un objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).</span><span class="sxs-lookup"><span data-stu-id="7126c-105">Create a new [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7126c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7126c-106">Prerequisites</span></span>
<span data-ttu-id="7126c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7126c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7126c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7126c-109">Permission type</span></span>|<span data-ttu-id="7126c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7126c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7126c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7126c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="7126c-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7126c-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="7126c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7126c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7126c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7126c-114">Not supported.</span></span>|
|<span data-ttu-id="7126c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7126c-115">Application</span></span>|<span data-ttu-id="7126c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7126c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7126c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7126c-117">HTTP Request</span></span>
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

## <a name="request-headers"></a><span data-ttu-id="7126c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7126c-118">Request headers</span></span>
|<span data-ttu-id="7126c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7126c-119">Header</span></span>|<span data-ttu-id="7126c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7126c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7126c-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="7126c-121">Authorization</span></span>|<span data-ttu-id="7126c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7126c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7126c-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7126c-123">Accept</span></span>|<span data-ttu-id="7126c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="7126c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7126c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7126c-125">Request body</span></span>
<span data-ttu-id="7126c-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsInformationProtectionAppLockerFile.</span><span class="sxs-lookup"><span data-stu-id="7126c-126">In the request body, supply a JSON representation for the windowsInformationProtectionAppLockerFile object.</span></span>

<span data-ttu-id="7126c-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsInformationProtectionAppLockerFile.</span><span class="sxs-lookup"><span data-stu-id="7126c-127">The following table shows the properties that are required when you create the windowsInformationProtectionAppLockerFile.</span></span>

|<span data-ttu-id="7126c-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7126c-128">Property</span></span>|<span data-ttu-id="7126c-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="7126c-129">Type</span></span>|<span data-ttu-id="7126c-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="7126c-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7126c-131">displayName</span><span class="sxs-lookup"><span data-stu-id="7126c-131">displayName</span></span>|<span data-ttu-id="7126c-132">String</span><span class="sxs-lookup"><span data-stu-id="7126c-132">String</span></span>|<span data-ttu-id="7126c-133">El nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="7126c-133">The friendly name</span></span>|
|<span data-ttu-id="7126c-134">fileHash</span><span class="sxs-lookup"><span data-stu-id="7126c-134">fileHash</span></span>|<span data-ttu-id="7126c-135">String</span><span class="sxs-lookup"><span data-stu-id="7126c-135">String</span></span>|<span data-ttu-id="7126c-136">Hash del archivo SHA256</span><span class="sxs-lookup"><span data-stu-id="7126c-136">SHA256 hash of the file</span></span>|
|<span data-ttu-id="7126c-137">file</span><span class="sxs-lookup"><span data-stu-id="7126c-137">file</span></span>|<span data-ttu-id="7126c-138">Binario</span><span class="sxs-lookup"><span data-stu-id="7126c-138">Binary</span></span>|<span data-ttu-id="7126c-139">Archivo como una matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="7126c-139">File as a byte array</span></span>|
|<span data-ttu-id="7126c-140">id</span><span class="sxs-lookup"><span data-stu-id="7126c-140">id</span></span>|<span data-ttu-id="7126c-141">String</span><span class="sxs-lookup"><span data-stu-id="7126c-141">String</span></span>|<span data-ttu-id="7126c-142">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7126c-142">Key of the entity.</span></span>|
|<span data-ttu-id="7126c-143">version</span><span class="sxs-lookup"><span data-stu-id="7126c-143">version</span></span>|<span data-ttu-id="7126c-144">String</span><span class="sxs-lookup"><span data-stu-id="7126c-144">String</span></span>|<span data-ttu-id="7126c-145">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7126c-145">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="7126c-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7126c-146">Response</span></span>
<span data-ttu-id="7126c-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7126c-147">If successful, this method returns a `201 Created` response code and a [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7126c-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7126c-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="7126c-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7126c-149">Request</span></span>
<span data-ttu-id="7126c-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7126c-150">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="7126c-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7126c-151">Response</span></span>
<span data-ttu-id="7126c-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7126c-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




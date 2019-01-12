---
title: Actualizar windowsInformationProtectionAppLockerFile
description: Actualice las propiedades de un objeto windowsInformationProtectionAppLockerFile.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 6e6d81b953288e1c8c9435a9502616f3f9fbc1d4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923827"
---
# <a name="update-windowsinformationprotectionapplockerfile"></a><span data-ttu-id="c7d15-103">Actualizar windowsInformationProtectionAppLockerFile</span><span class="sxs-lookup"><span data-stu-id="c7d15-103">Update windowsInformationProtectionAppLockerFile</span></span>

> <span data-ttu-id="c7d15-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c7d15-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c7d15-105">Actualice las propiedades de un objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).</span><span class="sxs-lookup"><span data-stu-id="c7d15-105">Update the properties of a [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c7d15-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c7d15-106">Prerequisites</span></span>
<span data-ttu-id="c7d15-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c7d15-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c7d15-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c7d15-109">Permission type</span></span>|<span data-ttu-id="c7d15-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c7d15-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c7d15-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c7d15-111">Delegated (work or school account)</span></span>|<span data-ttu-id="c7d15-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c7d15-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="c7d15-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c7d15-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c7d15-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c7d15-114">Not supported.</span></span>|
|<span data-ttu-id="c7d15-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c7d15-115">Application</span></span>|<span data-ttu-id="c7d15-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c7d15-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c7d15-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c7d15-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/exemptAppLockerFiles/{windowsInformationProtectionAppLockerFileId}
PATCH /deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/protectedAppLockerFiles/{windowsInformationProtectionAppLockerFileId}
PATCH /deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}/exemptAppLockerFiles/{windowsInformationProtectionAppLockerFileId}
PATCH /deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}/protectedAppLockerFiles/{windowsInformationProtectionAppLockerFileId}
```

## <a name="request-headers"></a><span data-ttu-id="c7d15-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c7d15-118">Request headers</span></span>
|<span data-ttu-id="c7d15-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7d15-119">Header</span></span>|<span data-ttu-id="c7d15-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c7d15-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c7d15-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="c7d15-121">Authorization</span></span>|<span data-ttu-id="c7d15-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c7d15-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c7d15-123">Accept</span><span class="sxs-lookup"><span data-stu-id="c7d15-123">Accept</span></span>|<span data-ttu-id="c7d15-124">application/json</span><span class="sxs-lookup"><span data-stu-id="c7d15-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c7d15-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c7d15-125">Request body</span></span>
<span data-ttu-id="c7d15-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).</span><span class="sxs-lookup"><span data-stu-id="c7d15-126">In the request body, supply a JSON representation for the [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) object.</span></span>

<span data-ttu-id="c7d15-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).</span><span class="sxs-lookup"><span data-stu-id="c7d15-127">The following table shows the properties that are required when you create the [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).</span></span>

|<span data-ttu-id="c7d15-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c7d15-128">Property</span></span>|<span data-ttu-id="c7d15-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="c7d15-129">Type</span></span>|<span data-ttu-id="c7d15-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7d15-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c7d15-131">displayName</span><span class="sxs-lookup"><span data-stu-id="c7d15-131">displayName</span></span>|<span data-ttu-id="c7d15-132">String</span><span class="sxs-lookup"><span data-stu-id="c7d15-132">String</span></span>|<span data-ttu-id="c7d15-133">El nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="c7d15-133">The friendly name</span></span>|
|<span data-ttu-id="c7d15-134">fileHash</span><span class="sxs-lookup"><span data-stu-id="c7d15-134">fileHash</span></span>|<span data-ttu-id="c7d15-135">String</span><span class="sxs-lookup"><span data-stu-id="c7d15-135">String</span></span>|<span data-ttu-id="c7d15-136">Hash del archivo SHA256</span><span class="sxs-lookup"><span data-stu-id="c7d15-136">SHA256 hash of the file</span></span>|
|<span data-ttu-id="c7d15-137">file</span><span class="sxs-lookup"><span data-stu-id="c7d15-137">file</span></span>|<span data-ttu-id="c7d15-138">Binario</span><span class="sxs-lookup"><span data-stu-id="c7d15-138">Binary</span></span>|<span data-ttu-id="c7d15-139">Archivo como una matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="c7d15-139">File as a byte array</span></span>|
|<span data-ttu-id="c7d15-140">id</span><span class="sxs-lookup"><span data-stu-id="c7d15-140">id</span></span>|<span data-ttu-id="c7d15-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="c7d15-141">String</span></span>|<span data-ttu-id="c7d15-142">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c7d15-142">Key of the entity.</span></span>|
|<span data-ttu-id="c7d15-143">version</span><span class="sxs-lookup"><span data-stu-id="c7d15-143">version</span></span>|<span data-ttu-id="c7d15-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="c7d15-144">String</span></span>|<span data-ttu-id="c7d15-145">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c7d15-145">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="c7d15-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7d15-146">Response</span></span>
<span data-ttu-id="c7d15-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7d15-147">If successful, this method returns a `200 OK` response code and an updated [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c7d15-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7d15-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="c7d15-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c7d15-149">Request</span></span>
<span data-ttu-id="c7d15-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c7d15-150">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/exemptAppLockerFiles/{windowsInformationProtectionAppLockerFileId}
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

### <a name="response"></a><span data-ttu-id="c7d15-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7d15-151">Response</span></span>
<span data-ttu-id="c7d15-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c7d15-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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




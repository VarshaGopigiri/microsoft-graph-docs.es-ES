---
title: Actualizar windowsInformationProtectionAppLockerFile
description: Actualice las propiedades de un objeto windowsInformationProtectionAppLockerFile.
ms.openlocfilehash: bb19293b88c5956ee6836a207af728ae06c36364
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27082918"
---
# <a name="update-windowsinformationprotectionapplockerfile"></a><span data-ttu-id="f36e0-103">Actualizar windowsInformationProtectionAppLockerFile</span><span class="sxs-lookup"><span data-stu-id="f36e0-103">Update windowsInformationProtectionAppLockerFile</span></span>

> <span data-ttu-id="f36e0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f36e0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f36e0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f36e0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f36e0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f36e0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f36e0-107">Actualice las propiedades de un objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).</span><span class="sxs-lookup"><span data-stu-id="f36e0-107">Update the properties of a [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f36e0-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f36e0-108">Prerequisites</span></span>
<span data-ttu-id="f36e0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f36e0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f36e0-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f36e0-111">Permission type</span></span>|<span data-ttu-id="f36e0-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f36e0-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f36e0-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f36e0-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f36e0-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f36e0-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f36e0-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f36e0-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f36e0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f36e0-116">Not supported.</span></span>|
|<span data-ttu-id="f36e0-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f36e0-117">Application</span></span>|<span data-ttu-id="f36e0-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f36e0-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f36e0-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f36e0-119">HTTP Request</span></span>
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

## <a name="request-headers"></a><span data-ttu-id="f36e0-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f36e0-120">Request headers</span></span>
|<span data-ttu-id="f36e0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f36e0-121">Header</span></span>|<span data-ttu-id="f36e0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f36e0-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f36e0-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="f36e0-123">Authorization</span></span>|<span data-ttu-id="f36e0-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f36e0-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f36e0-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f36e0-125">Accept</span></span>|<span data-ttu-id="f36e0-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f36e0-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f36e0-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f36e0-127">Request body</span></span>
<span data-ttu-id="f36e0-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).</span><span class="sxs-lookup"><span data-stu-id="f36e0-128">In the request body, supply a JSON representation for the [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) object.</span></span>

<span data-ttu-id="f36e0-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).</span><span class="sxs-lookup"><span data-stu-id="f36e0-129">The following table shows the properties that are required when you create the [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).</span></span>

|<span data-ttu-id="f36e0-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f36e0-130">Property</span></span>|<span data-ttu-id="f36e0-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f36e0-131">Type</span></span>|<span data-ttu-id="f36e0-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f36e0-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f36e0-133">displayName</span><span class="sxs-lookup"><span data-stu-id="f36e0-133">displayName</span></span>|<span data-ttu-id="f36e0-134">String</span><span class="sxs-lookup"><span data-stu-id="f36e0-134">String</span></span>|<span data-ttu-id="f36e0-135">El nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="f36e0-135">The friendly name</span></span>|
|<span data-ttu-id="f36e0-136">fileHash</span><span class="sxs-lookup"><span data-stu-id="f36e0-136">fileHash</span></span>|<span data-ttu-id="f36e0-137">String</span><span class="sxs-lookup"><span data-stu-id="f36e0-137">String</span></span>|<span data-ttu-id="f36e0-138">Hash del archivo SHA256</span><span class="sxs-lookup"><span data-stu-id="f36e0-138">SHA256 hash of the file</span></span>|
|<span data-ttu-id="f36e0-139">file</span><span class="sxs-lookup"><span data-stu-id="f36e0-139">file</span></span>|<span data-ttu-id="f36e0-140">Binario</span><span class="sxs-lookup"><span data-stu-id="f36e0-140">Binary</span></span>|<span data-ttu-id="f36e0-141">Archivo como una matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="f36e0-141">File as a byte array</span></span>|
|<span data-ttu-id="f36e0-142">id</span><span class="sxs-lookup"><span data-stu-id="f36e0-142">id</span></span>|<span data-ttu-id="f36e0-143">String</span><span class="sxs-lookup"><span data-stu-id="f36e0-143">String</span></span>|<span data-ttu-id="f36e0-144">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f36e0-144">Key of the entity.</span></span>|
|<span data-ttu-id="f36e0-145">version</span><span class="sxs-lookup"><span data-stu-id="f36e0-145">version</span></span>|<span data-ttu-id="f36e0-146">String</span><span class="sxs-lookup"><span data-stu-id="f36e0-146">String</span></span>|<span data-ttu-id="f36e0-147">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f36e0-147">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="f36e0-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f36e0-148">Response</span></span>
<span data-ttu-id="f36e0-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f36e0-149">If successful, this method returns a `200 OK` response code and an updated [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f36e0-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f36e0-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="f36e0-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f36e0-151">Request</span></span>
<span data-ttu-id="f36e0-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f36e0-152">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/exemptAppLockerFiles/{windowsInformationProtectionAppLockerFileId}
Content-type: application/json
Content-length: 131

{
  "displayName": "Display Name value",
  "fileHash": "File Hash value",
  "file": "ZmlsZQ==",
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="f36e0-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f36e0-153">Response</span></span>
<span data-ttu-id="f36e0-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f36e0-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






---
title: Actualizar windowsInformationProtectionAppLockerFile
description: Actualice las propiedades de un objeto windowsInformationProtectionAppLockerFile.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a81a42b1245a8723935ac8497e69539b1e5c1df8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885684"
---
# <a name="update-windowsinformationprotectionapplockerfile"></a><span data-ttu-id="b3ecb-103">Actualizar windowsInformationProtectionAppLockerFile</span><span class="sxs-lookup"><span data-stu-id="b3ecb-103">Update windowsInformationProtectionAppLockerFile</span></span>

> <span data-ttu-id="b3ecb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b3ecb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b3ecb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b3ecb-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b3ecb-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b3ecb-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b3ecb-107">Actualice las propiedades de un objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).</span><span class="sxs-lookup"><span data-stu-id="b3ecb-107">Update the properties of a [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b3ecb-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b3ecb-108">Prerequisites</span></span>
<span data-ttu-id="b3ecb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b3ecb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b3ecb-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b3ecb-111">Permission type</span></span>|<span data-ttu-id="b3ecb-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b3ecb-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b3ecb-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b3ecb-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b3ecb-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b3ecb-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="b3ecb-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b3ecb-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b3ecb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b3ecb-116">Not supported.</span></span>|
|<span data-ttu-id="b3ecb-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b3ecb-117">Application</span></span>|<span data-ttu-id="b3ecb-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b3ecb-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b3ecb-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b3ecb-119">HTTP Request</span></span>
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

## <a name="request-headers"></a><span data-ttu-id="b3ecb-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b3ecb-120">Request headers</span></span>
|<span data-ttu-id="b3ecb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3ecb-121">Header</span></span>|<span data-ttu-id="b3ecb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b3ecb-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b3ecb-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="b3ecb-123">Authorization</span></span>|<span data-ttu-id="b3ecb-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b3ecb-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b3ecb-125">Accept</span><span class="sxs-lookup"><span data-stu-id="b3ecb-125">Accept</span></span>|<span data-ttu-id="b3ecb-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b3ecb-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b3ecb-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b3ecb-127">Request body</span></span>
<span data-ttu-id="b3ecb-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).</span><span class="sxs-lookup"><span data-stu-id="b3ecb-128">In the request body, supply a JSON representation for the [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) object.</span></span>

<span data-ttu-id="b3ecb-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).</span><span class="sxs-lookup"><span data-stu-id="b3ecb-129">The following table shows the properties that are required when you create the [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).</span></span>

|<span data-ttu-id="b3ecb-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b3ecb-130">Property</span></span>|<span data-ttu-id="b3ecb-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3ecb-131">Type</span></span>|<span data-ttu-id="b3ecb-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3ecb-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b3ecb-133">displayName</span><span class="sxs-lookup"><span data-stu-id="b3ecb-133">displayName</span></span>|<span data-ttu-id="b3ecb-134">String</span><span class="sxs-lookup"><span data-stu-id="b3ecb-134">String</span></span>|<span data-ttu-id="b3ecb-135">El nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="b3ecb-135">The friendly name</span></span>|
|<span data-ttu-id="b3ecb-136">fileHash</span><span class="sxs-lookup"><span data-stu-id="b3ecb-136">fileHash</span></span>|<span data-ttu-id="b3ecb-137">String</span><span class="sxs-lookup"><span data-stu-id="b3ecb-137">String</span></span>|<span data-ttu-id="b3ecb-138">Hash del archivo SHA256</span><span class="sxs-lookup"><span data-stu-id="b3ecb-138">SHA256 hash of the file</span></span>|
|<span data-ttu-id="b3ecb-139">file</span><span class="sxs-lookup"><span data-stu-id="b3ecb-139">file</span></span>|<span data-ttu-id="b3ecb-140">Binario</span><span class="sxs-lookup"><span data-stu-id="b3ecb-140">Binary</span></span>|<span data-ttu-id="b3ecb-141">Archivo como una matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="b3ecb-141">File as a byte array</span></span>|
|<span data-ttu-id="b3ecb-142">id</span><span class="sxs-lookup"><span data-stu-id="b3ecb-142">id</span></span>|<span data-ttu-id="b3ecb-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="b3ecb-143">String</span></span>|<span data-ttu-id="b3ecb-144">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b3ecb-144">Key of the entity.</span></span>|
|<span data-ttu-id="b3ecb-145">version</span><span class="sxs-lookup"><span data-stu-id="b3ecb-145">version</span></span>|<span data-ttu-id="b3ecb-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="b3ecb-146">String</span></span>|<span data-ttu-id="b3ecb-147">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b3ecb-147">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="b3ecb-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b3ecb-148">Response</span></span>
<span data-ttu-id="b3ecb-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b3ecb-149">If successful, this method returns a `200 OK` response code and an updated [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b3ecb-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b3ecb-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="b3ecb-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b3ecb-151">Request</span></span>
<span data-ttu-id="b3ecb-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b3ecb-152">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="b3ecb-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b3ecb-153">Response</span></span>
<span data-ttu-id="b3ecb-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b3ecb-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






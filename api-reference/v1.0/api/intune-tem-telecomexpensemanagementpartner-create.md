---
title: Crear telecomExpenseManagementPartner
description: Cree un objeto telecomExpenseManagementPartner.
ms.openlocfilehash: 327c2be4f84ea16d56a068db10c87e9d776b89c8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031195"
---
# <a name="create-telecomexpensemanagementpartner"></a><span data-ttu-id="2339d-103">Crear telecomExpenseManagementPartner</span><span class="sxs-lookup"><span data-stu-id="2339d-103">Create telecomExpenseManagementPartner</span></span>

> <span data-ttu-id="2339d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2339d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2339d-105">Cree un objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="2339d-105">Create a new [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2339d-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2339d-106">Prerequisites</span></span>
<span data-ttu-id="2339d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2339d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2339d-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2339d-109">Permission type</span></span>|<span data-ttu-id="2339d-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2339d-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2339d-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2339d-111">Delegated (work or school account)</span></span>|<span data-ttu-id="2339d-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2339d-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="2339d-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2339d-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2339d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2339d-114">Not supported.</span></span>|
|<span data-ttu-id="2339d-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2339d-115">Application</span></span>|<span data-ttu-id="2339d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2339d-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2339d-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2339d-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/telecomExpenseManagementPartners
```

## <a name="request-headers"></a><span data-ttu-id="2339d-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2339d-118">Request headers</span></span>
|<span data-ttu-id="2339d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2339d-119">Header</span></span>|<span data-ttu-id="2339d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2339d-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2339d-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="2339d-121">Authorization</span></span>|<span data-ttu-id="2339d-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2339d-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2339d-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2339d-123">Accept</span></span>|<span data-ttu-id="2339d-124">application/json</span><span class="sxs-lookup"><span data-stu-id="2339d-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2339d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2339d-125">Request body</span></span>
<span data-ttu-id="2339d-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto telecomExpenseManagementPartner.</span><span class="sxs-lookup"><span data-stu-id="2339d-126">In the request body, supply a JSON representation for the telecomExpenseManagementPartner object.</span></span>

<span data-ttu-id="2339d-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto telecomExpenseManagementPartner.</span><span class="sxs-lookup"><span data-stu-id="2339d-127">The following table shows the properties that are required when you create the telecomExpenseManagementPartner.</span></span>

|<span data-ttu-id="2339d-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2339d-128">Property</span></span>|<span data-ttu-id="2339d-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="2339d-129">Type</span></span>|<span data-ttu-id="2339d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="2339d-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2339d-131">id</span><span class="sxs-lookup"><span data-stu-id="2339d-131">id</span></span>|<span data-ttu-id="2339d-132">String</span><span class="sxs-lookup"><span data-stu-id="2339d-132">String</span></span>|<span data-ttu-id="2339d-133">Identificador único del partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="2339d-133">Unique identifier of the TEM partner.</span></span>|
|<span data-ttu-id="2339d-134">displayName</span><span class="sxs-lookup"><span data-stu-id="2339d-134">displayName</span></span>|<span data-ttu-id="2339d-135">String</span><span class="sxs-lookup"><span data-stu-id="2339d-135">String</span></span>|<span data-ttu-id="2339d-136">Nombre para mostrar del partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="2339d-136">Display name of the TEM partner.</span></span>|
|<span data-ttu-id="2339d-137">url</span><span class="sxs-lookup"><span data-stu-id="2339d-137">url</span></span>|<span data-ttu-id="2339d-138">String</span><span class="sxs-lookup"><span data-stu-id="2339d-138">String</span></span>|<span data-ttu-id="2339d-139">Dirección URL del panel de control administrativo del partner de TEM, donde un administrador puede configurar el servicio de su TEM.</span><span class="sxs-lookup"><span data-stu-id="2339d-139">URL of the TEM partner's administrative control panel, where an administrator can configure their TEM service.</span></span>|
|<span data-ttu-id="2339d-140">appAuthorized</span><span class="sxs-lookup"><span data-stu-id="2339d-140">appAuthorized</span></span>|<span data-ttu-id="2339d-141">Booleano</span><span class="sxs-lookup"><span data-stu-id="2339d-141">Boolean</span></span>|<span data-ttu-id="2339d-142">Si se ha autorizado a la aplicación de AAD del partner para que obtenga acceso a Intune.</span><span class="sxs-lookup"><span data-stu-id="2339d-142">Whether the partner's AAD app has been authorized to access Intune.</span></span>|
|<span data-ttu-id="2339d-143">enabled</span><span class="sxs-lookup"><span data-stu-id="2339d-143">enabled</span></span>|<span data-ttu-id="2339d-144">Booleano</span><span class="sxs-lookup"><span data-stu-id="2339d-144">Boolean</span></span>|<span data-ttu-id="2339d-145">Si la conexión de Intune al servicio de TEM está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="2339d-145">Whether Intune's connection to the TEM service is currently enabled or disabled.</span></span>|
|<span data-ttu-id="2339d-146">lastConnectionDateTime</span><span class="sxs-lookup"><span data-stu-id="2339d-146">lastConnectionDateTime</span></span>|<span data-ttu-id="2339d-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2339d-147">DateTimeOffset</span></span>|<span data-ttu-id="2339d-148">Marca de tiempo de la última solicitud enviada a Intune por el partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="2339d-148">Timestamp of the last request sent to Intune by the TEM partner.</span></span>|



## <a name="response"></a><span data-ttu-id="2339d-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2339d-149">Response</span></span>
<span data-ttu-id="2339d-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2339d-150">If successful, this method returns a `201 Created` response code and a [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2339d-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2339d-151">Example</span></span>
### <a name="request"></a><span data-ttu-id="2339d-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2339d-152">Request</span></span>
<span data-ttu-id="2339d-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2339d-153">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/telecomExpenseManagementPartners
Content-type: application/json
Content-length: 248

{
  "@odata.type": "#microsoft.graph.telecomExpenseManagementPartner",
  "displayName": "Display Name value",
  "url": "Url value",
  "appAuthorized": true,
  "enabled": true,
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```

### <a name="response"></a><span data-ttu-id="2339d-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2339d-154">Response</span></span>
<span data-ttu-id="2339d-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2339d-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 297

{
  "@odata.type": "#microsoft.graph.telecomExpenseManagementPartner",
  "id": "47a3b399-b399-47a3-99b3-a34799b3a347",
  "displayName": "Display Name value",
  "url": "Url value",
  "appAuthorized": true,
  "enabled": true,
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```




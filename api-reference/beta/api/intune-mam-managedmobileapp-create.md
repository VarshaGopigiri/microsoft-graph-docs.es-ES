---
title: Crear managedMobileApp
description: Cree un objeto managedMobileApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e94b95e4dfea69aafdd426fd4c9a5deca676ce42
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27881105"
---
# <a name="create-managedmobileapp"></a><span data-ttu-id="f2f09-103">Crear managedMobileApp</span><span class="sxs-lookup"><span data-stu-id="f2f09-103">Create managedMobileApp</span></span>

> <span data-ttu-id="f2f09-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f2f09-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f2f09-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f2f09-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f2f09-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f2f09-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f2f09-107">Cree un objeto [managedMobileApp](../resources/intune-mam-managedmobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f2f09-107">Create a new [managedMobileApp](../resources/intune-mam-managedmobileapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f2f09-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f2f09-108">Prerequisites</span></span>
<span data-ttu-id="f2f09-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f2f09-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f2f09-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f2f09-111">Permission type</span></span>|<span data-ttu-id="f2f09-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f2f09-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f2f09-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f2f09-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f2f09-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f2f09-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f2f09-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f2f09-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f2f09-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f2f09-116">Not supported.</span></span>|
|<span data-ttu-id="f2f09-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f2f09-117">Application</span></span>|<span data-ttu-id="f2f09-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f2f09-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f2f09-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f2f09-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/apps
POST /deviceAppManagement/androidManagedAppProtections/{androidManagedAppProtectionId}/apps
POST /deviceAppManagement/defaultManagedAppProtections/{defaultManagedAppProtectionId}/apps
POST /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/apps
```

## <a name="request-headers"></a><span data-ttu-id="f2f09-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f2f09-120">Request headers</span></span>
|<span data-ttu-id="f2f09-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2f09-121">Header</span></span>|<span data-ttu-id="f2f09-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f2f09-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f2f09-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f2f09-123">Authorization</span></span>|<span data-ttu-id="f2f09-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f2f09-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f2f09-125">Accept</span><span class="sxs-lookup"><span data-stu-id="f2f09-125">Accept</span></span>|<span data-ttu-id="f2f09-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f2f09-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f2f09-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f2f09-127">Request body</span></span>
<span data-ttu-id="f2f09-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedMobileApp.</span><span class="sxs-lookup"><span data-stu-id="f2f09-128">In the request body, supply a JSON representation for the managedMobileApp object.</span></span>

<span data-ttu-id="f2f09-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedMobileApp.</span><span class="sxs-lookup"><span data-stu-id="f2f09-129">The following table shows the properties that are required when you create the managedMobileApp.</span></span>

|<span data-ttu-id="f2f09-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f2f09-130">Property</span></span>|<span data-ttu-id="f2f09-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f2f09-131">Type</span></span>|<span data-ttu-id="f2f09-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2f09-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f2f09-133">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="f2f09-133">mobileAppIdentifier</span></span>|[<span data-ttu-id="f2f09-134">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="f2f09-134">mobileAppIdentifier</span></span>](../resources/intune-mam-mobileappidentifier.md)|<span data-ttu-id="f2f09-135">El identificador de una aplicación con el tipo de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f2f09-135">The identifier for an app with it's operating system type.</span></span>|
|<span data-ttu-id="f2f09-136">id</span><span class="sxs-lookup"><span data-stu-id="f2f09-136">id</span></span>|<span data-ttu-id="f2f09-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="f2f09-137">String</span></span>|<span data-ttu-id="f2f09-138">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f2f09-138">Key of the entity.</span></span>|
|<span data-ttu-id="f2f09-139">version</span><span class="sxs-lookup"><span data-stu-id="f2f09-139">version</span></span>|<span data-ttu-id="f2f09-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="f2f09-140">String</span></span>|<span data-ttu-id="f2f09-141">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f2f09-141">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="f2f09-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f2f09-142">Response</span></span>
<span data-ttu-id="f2f09-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedMobileApp](../resources/intune-mam-managedmobileapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f2f09-143">If successful, this method returns a `201 Created` response code and a [managedMobileApp](../resources/intune-mam-managedmobileapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f2f09-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f2f09-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="f2f09-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f2f09-145">Request</span></span>
<span data-ttu-id="f2f09-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f2f09-146">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/apps
Content-type: application/json
Content-length: 181

{
  "@odata.type": "#microsoft.graph.managedMobileApp",
  "mobileAppIdentifier": {
    "@odata.type": "microsoft.graph.mobileAppIdentifier"
  },
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="f2f09-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f2f09-147">Response</span></span>
<span data-ttu-id="f2f09-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f2f09-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 230

{
  "@odata.type": "#microsoft.graph.managedMobileApp",
  "mobileAppIdentifier": {
    "@odata.type": "microsoft.graph.mobileAppIdentifier"
  },
  "id": "0a129715-9715-0a12-1597-120a1597120a",
  "version": "Version value"
}
```






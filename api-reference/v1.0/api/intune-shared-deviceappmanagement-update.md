---
title: Actualizar deviceAppManagement
description: Actualice las propiedades de un objeto deviceAppManagement.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: f100e91f6943d24dd63be9c28ba0e96213cfc012
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991499"
---
# <a name="update-deviceappmanagement"></a><span data-ttu-id="23e48-103">Actualizar deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="23e48-103">Update deviceAppManagement</span></span>

> <span data-ttu-id="23e48-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="23e48-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="23e48-105">Actualice las propiedades de un objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="23e48-105">Update the properties of a [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="23e48-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="23e48-106">Prerequisites</span></span>
<span data-ttu-id="23e48-107">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="23e48-107">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="23e48-108">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="23e48-108">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>  <span data-ttu-id="23e48-109">Tenga en cuenta que el permiso adecuado varía según el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="23e48-109">Note that the appropriate permission varies according to the workflow.</span></span>

|<span data-ttu-id="23e48-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="23e48-110">Permission type</span></span>|<span data-ttu-id="23e48-111">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="23e48-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="23e48-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="23e48-112">Delegated (work or school account)</span></span>|<span data-ttu-id="23e48-113">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="23e48-113">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="23e48-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="23e48-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="23e48-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="23e48-115">Not supported.</span></span>|
|<span data-ttu-id="23e48-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="23e48-116">Application</span></span>|<span data-ttu-id="23e48-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="23e48-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="23e48-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="23e48-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement
```

## <a name="request-headers"></a><span data-ttu-id="23e48-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="23e48-119">Request headers</span></span>
|<span data-ttu-id="23e48-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23e48-120">Header</span></span>|<span data-ttu-id="23e48-121">Valor</span><span class="sxs-lookup"><span data-stu-id="23e48-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="23e48-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="23e48-122">Authorization</span></span>|<span data-ttu-id="23e48-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="23e48-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="23e48-124">Accept</span><span class="sxs-lookup"><span data-stu-id="23e48-124">Accept</span></span>|<span data-ttu-id="23e48-125">application/json</span><span class="sxs-lookup"><span data-stu-id="23e48-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="23e48-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="23e48-126">Request body</span></span>
<span data-ttu-id="23e48-127">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="23e48-127">In the request body, supply a JSON representation for the [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) object.</span></span>

<span data-ttu-id="23e48-128">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="23e48-128">The following table shows the properties that are required when you create the [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md).</span></span>

|<span data-ttu-id="23e48-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="23e48-129">Property</span></span>|<span data-ttu-id="23e48-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="23e48-130">Type</span></span>|<span data-ttu-id="23e48-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="23e48-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="23e48-132">id</span><span class="sxs-lookup"><span data-stu-id="23e48-132">id</span></span>|<span data-ttu-id="23e48-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="23e48-133">String</span></span>|<span data-ttu-id="23e48-134">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="23e48-134">Key of the entity.</span></span>|
|<span data-ttu-id="23e48-135">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="23e48-135">**Onboarding**</span></span>|
|<span data-ttu-id="23e48-136">isEnabledForMicrosoftStoreForBusiness</span><span class="sxs-lookup"><span data-stu-id="23e48-136">isEnabledForMicrosoftStoreForBusiness</span></span>|<span data-ttu-id="23e48-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="23e48-137">Boolean</span></span>|<span data-ttu-id="23e48-138">Indica si la cuenta está habilitada para la sincronización de aplicaciones de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="23e48-138">Whether the account is enabled for syncing applications from the Microsoft Store for Business.</span></span>|
|<span data-ttu-id="23e48-139">microsoftStoreForBusinessLanguage</span><span class="sxs-lookup"><span data-stu-id="23e48-139">microsoftStoreForBusinessLanguage</span></span>|<span data-ttu-id="23e48-140">String</span><span class="sxs-lookup"><span data-stu-id="23e48-140">String</span></span>|<span data-ttu-id="23e48-141">Información local que se usa para sincronizar las aplicaciones de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="23e48-141">The locale information used to sync applications from the Microsoft Store for Business.</span></span> <span data-ttu-id="23e48-142">Referencias culturales que son específicas de un país o región.</span><span class="sxs-lookup"><span data-stu-id="23e48-142">Cultures that are specific to a country/region.</span></span> <span data-ttu-id="23e48-143">Los nombres de dichas referencias culturales siguen RFC 4646 (Windows Vista y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="23e48-143">The names of these cultures follow RFC 4646 (Windows Vista and later).</span></span> <span data-ttu-id="23e48-144">El formato es <languagecode2>-<country/regioncode2>, donde <languagecode2> es un código de dos letras en minúsculas proveniente de ISO 639-1 y <country/regioncode2> es un código de dos letras en mayúsculas derivado de ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="23e48-144">The format is <languagecode2>-<country/regioncode2>, where <languagecode2> is a lowercase two-letter code derived from ISO 639-1 and <country/regioncode2> is an uppercase two-letter code derived from ISO 3166.</span></span> <span data-ttu-id="23e48-145">Por ejemplo, en-US para inglés (Estados Unidos) es una referencia cultural específica.</span><span class="sxs-lookup"><span data-stu-id="23e48-145">For example, en-US for English (United States) is a specific culture.</span></span>|
|<span data-ttu-id="23e48-146">microsoftStoreForBusinessLastCompletedApplicationSyncTime</span><span class="sxs-lookup"><span data-stu-id="23e48-146">microsoftStoreForBusinessLastCompletedApplicationSyncTime</span></span>|<span data-ttu-id="23e48-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="23e48-147">DateTimeOffset</span></span>|<span data-ttu-id="23e48-148">La última vez que se completó una sincronización de aplicaciones desde Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="23e48-148">The last time an application sync from the Microsoft Store for Business was completed.</span></span>|
|<span data-ttu-id="23e48-149">microsoftStoreForBusinessLastSuccessfulSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="23e48-149">microsoftStoreForBusinessLastSuccessfulSyncDateTime</span></span>|<span data-ttu-id="23e48-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="23e48-150">DateTimeOffset</span></span>|<span data-ttu-id="23e48-151">Última vez que se sincronizaron correctamente las aplicaciones de Microsoft Store para Empresas en la cuenta.</span><span class="sxs-lookup"><span data-stu-id="23e48-151">The last time the apps from the Microsoft Store for Business were synced successfully for the account.</span></span>|

## <a name="response"></a><span data-ttu-id="23e48-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="23e48-152">Response</span></span>
<span data-ttu-id="23e48-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="23e48-153">If successful, this method returns a `200 OK` response code and an updated [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) object in the response body.</span></span>

## <a name="example-request"></a><span data-ttu-id="23e48-154">Ejemplo de solicitud</span><span class="sxs-lookup"><span data-stu-id="23e48-154">Example request</span></span>

``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement
Content-type: application/json
Content-length: 2

{}
```

## <a name="example-response"></a><span data-ttu-id="23e48-155">Respuesta de ejemplo</span><span class="sxs-lookup"><span data-stu-id="23e48-155">Example response</span></span>

<span data-ttu-id="23e48-156">El objeto de respuesta que se muestra aquí es posible que esté truncado por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="23e48-156">The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="23e48-157">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="23e48-157">All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 110

{
  "@odata.type": "#microsoft.graph.deviceAppManagement",
  "id": "bbb801a3-01a3-bbb8-a301-b8bba301b8bb"
}
```




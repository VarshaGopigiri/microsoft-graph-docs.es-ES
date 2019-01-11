---
title: Crear windowsPrivacyDataAccessControlItem
description: Crear un nuevo objeto windowsPrivacyDataAccessControlItem.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 6881d6125e91f18eccfd93079c10dac672167f14
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811993"
---
# <a name="create-windowsprivacydataaccesscontrolitem"></a><span data-ttu-id="0db25-103">Crear windowsPrivacyDataAccessControlItem</span><span class="sxs-lookup"><span data-stu-id="0db25-103">Create windowsPrivacyDataAccessControlItem</span></span>

> <span data-ttu-id="0db25-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0db25-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0db25-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0db25-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0db25-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0db25-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0db25-107">Crear un nuevo objeto [windowsPrivacyDataAccessControlItem](../resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem.md) .</span><span class="sxs-lookup"><span data-stu-id="0db25-107">Create a new [windowsPrivacyDataAccessControlItem](../resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0db25-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0db25-108">Prerequisites</span></span>
<span data-ttu-id="0db25-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0db25-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0db25-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0db25-111">Permission type</span></span>|<span data-ttu-id="0db25-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0db25-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0db25-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0db25-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0db25-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0db25-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="0db25-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0db25-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0db25-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0db25-116">Not supported.</span></span>|
|<span data-ttu-id="0db25-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0db25-117">Application</span></span>|<span data-ttu-id="0db25-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0db25-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0db25-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0db25-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windows10GeneralConfiguration/privacyAccessControls
```

## <a name="request-headers"></a><span data-ttu-id="0db25-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0db25-120">Request headers</span></span>
|<span data-ttu-id="0db25-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0db25-121">Header</span></span>|<span data-ttu-id="0db25-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0db25-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0db25-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="0db25-123">Authorization</span></span>|<span data-ttu-id="0db25-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0db25-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0db25-125">Accept</span><span class="sxs-lookup"><span data-stu-id="0db25-125">Accept</span></span>|<span data-ttu-id="0db25-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0db25-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0db25-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0db25-127">Request body</span></span>
<span data-ttu-id="0db25-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windowsPrivacyDataAccessControlItem.</span><span class="sxs-lookup"><span data-stu-id="0db25-128">In the request body, supply a JSON representation for the windowsPrivacyDataAccessControlItem object.</span></span>

<span data-ttu-id="0db25-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windowsPrivacyDataAccessControlItem.</span><span class="sxs-lookup"><span data-stu-id="0db25-129">The following table shows the properties that are required when you create the windowsPrivacyDataAccessControlItem.</span></span>

|<span data-ttu-id="0db25-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0db25-130">Property</span></span>|<span data-ttu-id="0db25-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0db25-131">Type</span></span>|<span data-ttu-id="0db25-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="0db25-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0db25-133">id</span><span class="sxs-lookup"><span data-stu-id="0db25-133">id</span></span>|<span data-ttu-id="0db25-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="0db25-134">String</span></span>|<span data-ttu-id="0db25-135">La clave de WindowsPrivacyDataAccessControlItem.</span><span class="sxs-lookup"><span data-stu-id="0db25-135">The key of WindowsPrivacyDataAccessControlItem.</span></span>|
|<span data-ttu-id="0db25-136">accessLevel</span><span class="sxs-lookup"><span data-stu-id="0db25-136">accessLevel</span></span>|[<span data-ttu-id="0db25-137">windowsPrivacyDataAccessLevel</span><span class="sxs-lookup"><span data-stu-id="0db25-137">windowsPrivacyDataAccessLevel</span></span>](../resources/intune-deviceconfig-windowsprivacydataaccesslevel.md)|<span data-ttu-id="0db25-138">Esto indica un nivel de acceso para la categoría de datos de privacidad a la que se le dará la aplicación especificada a.</span><span class="sxs-lookup"><span data-stu-id="0db25-138">This indicates an access level for the privacy data category to which the specified application will be given to.</span></span> <span data-ttu-id="0db25-139">Los valores posibles son: `notConfigured`, `forceAllow`, `forceDeny` y `userInControl`.</span><span class="sxs-lookup"><span data-stu-id="0db25-139">Possible values are: `notConfigured`, `forceAllow`, `forceDeny`, `userInControl`.</span></span>|
|<span data-ttu-id="0db25-140">dataCategory</span><span class="sxs-lookup"><span data-stu-id="0db25-140">dataCategory</span></span>|[<span data-ttu-id="0db25-141">windowsPrivacyDataCategory</span><span class="sxs-lookup"><span data-stu-id="0db25-141">windowsPrivacyDataCategory</span></span>](../resources/intune-deviceconfig-windowsprivacydatacategory.md)|<span data-ttu-id="0db25-142">Esto indica una categoría de datos de privacidad al que se aplicará el control de acceso específico.</span><span class="sxs-lookup"><span data-stu-id="0db25-142">This indicates a privacy data category to which the specific access control will apply.</span></span> <span data-ttu-id="0db25-143">Los valores posibles son: `notConfigured`, `accountInfo`, `appsRunInBackground`, `calendar`, `callHistory`, `camera`, `contacts`, `diagnosticsInfo`, `email`, `location`, `messaging`, `microphone`, `motion`, `notifications`, `phone`, `radios`, `tasks`, `syncWithDevices`, `trustedDevices` .</span><span class="sxs-lookup"><span data-stu-id="0db25-143">Possible values are: `notConfigured`, `accountInfo`, `appsRunInBackground`, `calendar`, `callHistory`, `camera`, `contacts`, `diagnosticsInfo`, `email`, `location`, `messaging`, `microphone`, `motion`, `notifications`, `phone`, `radios`, `tasks`, `syncWithDevices`, `trustedDevices`.</span></span>|
|<span data-ttu-id="0db25-144">appPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="0db25-144">appPackageFamilyName</span></span>|<span data-ttu-id="0db25-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="0db25-145">String</span></span>|<span data-ttu-id="0db25-146">El nombre de la familia de paquete de una aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="0db25-146">The Package Family Name of a Windows app.</span></span> <span data-ttu-id="0db25-147">Cuando se establece, se aplica el nivel de acceso a la aplicación especificada.</span><span class="sxs-lookup"><span data-stu-id="0db25-147">When set, the access level applies to the specified application.</span></span>|
|<span data-ttu-id="0db25-148">appDisplayName</span><span class="sxs-lookup"><span data-stu-id="0db25-148">appDisplayName</span></span>|<span data-ttu-id="0db25-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="0db25-149">String</span></span>|<span data-ttu-id="0db25-150">El nombre de la familia de paquete de una aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="0db25-150">The Package Family Name of a Windows app.</span></span> <span data-ttu-id="0db25-151">Cuando se establece, se aplica el nivel de acceso a la aplicación especificada.</span><span class="sxs-lookup"><span data-stu-id="0db25-151">When set, the access level applies to the specified application.</span></span>|



## <a name="response"></a><span data-ttu-id="0db25-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0db25-152">Response</span></span>
<span data-ttu-id="0db25-153">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windowsPrivacyDataAccessControlItem](../resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0db25-153">If successful, this method returns a `201 Created` response code and a [windowsPrivacyDataAccessControlItem](../resources/intune-deviceconfig-windowsprivacydataaccesscontrolitem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0db25-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0db25-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="0db25-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0db25-155">Request</span></span>
<span data-ttu-id="0db25-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0db25-156">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windows10GeneralConfiguration/privacyAccessControls
Content-type: application/json
Content-length: 250

{
  "@odata.type": "#microsoft.graph.windowsPrivacyDataAccessControlItem",
  "accessLevel": "forceAllow",
  "dataCategory": "accountInfo",
  "appPackageFamilyName": "App Package Family Name value",
  "appDisplayName": "App Display Name value"
}
```

### <a name="response"></a><span data-ttu-id="0db25-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0db25-157">Response</span></span>
<span data-ttu-id="0db25-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0db25-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 299

{
  "@odata.type": "#microsoft.graph.windowsPrivacyDataAccessControlItem",
  "id": "03b15556-5556-03b1-5655-b1035655b103",
  "accessLevel": "forceAllow",
  "dataCategory": "accountInfo",
  "appPackageFamilyName": "App Package Family Name value",
  "appDisplayName": "App Display Name value"
}
```






---
title: Actualizar windowsAssignedAccessProfile
description: Actualizar las propiedades de un objeto windowsAssignedAccessProfile.
author: tfitzmac
ms.openlocfilehash: 84cbc1aaaebf9383c3d113d7f309c61de0cdeb67
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331363"
---
# <a name="update-windowsassignedaccessprofile"></a><span data-ttu-id="7feef-103">Actualizar windowsAssignedAccessProfile</span><span class="sxs-lookup"><span data-stu-id="7feef-103">Update windowsAssignedAccessProfile</span></span>

> <span data-ttu-id="7feef-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7feef-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7feef-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7feef-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7feef-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7feef-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7feef-107">Actualizar las propiedades de un objeto [windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="7feef-107">Update the properties of a [windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7feef-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7feef-108">Prerequisites</span></span>
<span data-ttu-id="7feef-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7feef-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7feef-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7feef-111">Permission type</span></span>|<span data-ttu-id="7feef-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7feef-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7feef-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7feef-113">Delegated (work or school account)</span></span>|<span data-ttu-id="7feef-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7feef-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="7feef-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7feef-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7feef-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7feef-116">Not supported.</span></span>|
|<span data-ttu-id="7feef-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7feef-117">Application</span></span>|<span data-ttu-id="7feef-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7feef-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7feef-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7feef-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windows10GeneralConfiguration/assignedAccessMultiModeProfiles/{windowsAssignedAccessProfileId}
```

## <a name="request-headers"></a><span data-ttu-id="7feef-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7feef-120">Request headers</span></span>
|<span data-ttu-id="7feef-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7feef-121">Header</span></span>|<span data-ttu-id="7feef-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7feef-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7feef-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="7feef-123">Authorization</span></span>|<span data-ttu-id="7feef-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7feef-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7feef-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7feef-125">Accept</span></span>|<span data-ttu-id="7feef-126">application/json</span><span class="sxs-lookup"><span data-stu-id="7feef-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7feef-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7feef-127">Request body</span></span>
<span data-ttu-id="7feef-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="7feef-128">In the request body, supply a JSON representation for the [windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md) object.</span></span>

<span data-ttu-id="7feef-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md).</span><span class="sxs-lookup"><span data-stu-id="7feef-129">The following table shows the properties that are required when you create the [windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md).</span></span>

|<span data-ttu-id="7feef-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7feef-130">Property</span></span>|<span data-ttu-id="7feef-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="7feef-131">Type</span></span>|<span data-ttu-id="7feef-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="7feef-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7feef-133">id</span><span class="sxs-lookup"><span data-stu-id="7feef-133">id</span></span>|<span data-ttu-id="7feef-134">String</span><span class="sxs-lookup"><span data-stu-id="7feef-134">String</span></span>|<span data-ttu-id="7feef-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7feef-135">Key of the entity.</span></span>|
|<span data-ttu-id="7feef-136">nombre del perfil</span><span class="sxs-lookup"><span data-stu-id="7feef-136">profileName</span></span>|<span data-ttu-id="7feef-137">String</span><span class="sxs-lookup"><span data-stu-id="7feef-137">String</span></span>|<span data-ttu-id="7feef-138">Esto es un nombre descriptivo usado para identificar un grupo de aplicaciones, el diseño de estas aplicaciones en el menú Inicio y los usuarios a quienes se asigna esta configuración de quiosco.</span><span class="sxs-lookup"><span data-stu-id="7feef-138">This is a friendly name used to identify a group of applications, the layout of these apps on the start menu and the users to whom this kiosk configuration is assigned.</span></span>|
|<span data-ttu-id="7feef-139">showTaskBar</span><span class="sxs-lookup"><span data-stu-id="7feef-139">showTaskBar</span></span>|<span data-ttu-id="7feef-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="7feef-140">Boolean</span></span>|<span data-ttu-id="7feef-141">Esta opción le permite al administrador especificar si se muestra la barra de tareas o no.</span><span class="sxs-lookup"><span data-stu-id="7feef-141">This setting allows the admin to specify whether the Task Bar is shown or not.</span></span>|
|<span data-ttu-id="7feef-142">appUserModelIds</span><span class="sxs-lookup"><span data-stu-id="7feef-142">appUserModelIds</span></span>|<span data-ttu-id="7feef-143">Colección String</span><span class="sxs-lookup"><span data-stu-id="7feef-143">String collection</span></span>|<span data-ttu-id="7feef-144">Estos son el único almacén de aplicaciones de Windows que estará disponible para iniciar desde el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="7feef-144">These are the only Windows Store Apps that will be available to launch from the Start menu.</span></span>|
|<span data-ttu-id="7feef-145">desktopAppPaths</span><span class="sxs-lookup"><span data-stu-id="7feef-145">desktopAppPaths</span></span>|<span data-ttu-id="7feef-146">Colección String</span><span class="sxs-lookup"><span data-stu-id="7feef-146">String collection</span></span>|<span data-ttu-id="7feef-147">Estas son las rutas de acceso de las aplicaciones de escritorio que estará disponible en el menú Inicio y las aplicaciones sólo el usuario podrá iniciar.</span><span class="sxs-lookup"><span data-stu-id="7feef-147">These are the paths of the Desktop Apps that will be available on the Start menu and the only apps the user will be able to launch.</span></span>|
|<span data-ttu-id="7feef-148">cuentas de usuario</span><span class="sxs-lookup"><span data-stu-id="7feef-148">userAccounts</span></span>|<span data-ttu-id="7feef-149">Colección String</span><span class="sxs-lookup"><span data-stu-id="7feef-149">String collection</span></span>|<span data-ttu-id="7feef-150">Las cuentas de usuario que se bloqueará a esta configuración de quiosco.</span><span class="sxs-lookup"><span data-stu-id="7feef-150">The user accounts that will be locked to this kiosk configuration.</span></span>|
|<span data-ttu-id="7feef-151">startMenuLayoutXml</span><span class="sxs-lookup"><span data-stu-id="7feef-151">startMenuLayoutXml</span></span>|<span data-ttu-id="7feef-152">Binario</span><span class="sxs-lookup"><span data-stu-id="7feef-152">Binary</span></span>|<span data-ttu-id="7feef-153">Permite a los administradores invalidar el diseño de inicio predeterminado y se evita que el usuario que lo modifique.</span><span class="sxs-lookup"><span data-stu-id="7feef-153">Allows admins to override the default Start layout and prevents the user from changing it.</span></span><span data-ttu-id="7feef-154">Para modificar el diseño, se especifica un archivo XML basado en el esquema de modificación del diseño.</span><span class="sxs-lookup"><span data-stu-id="7feef-154"> The layout is modified by specifying an XML file based on a layout modification schema.</span></span> <span data-ttu-id="7feef-155">XML debe estar en formato binario.</span><span class="sxs-lookup"><span data-stu-id="7feef-155">XML needs to be in Binary format.</span></span>|



## <a name="response"></a><span data-ttu-id="7feef-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7feef-156">Response</span></span>
<span data-ttu-id="7feef-157">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7feef-157">If successful, this method returns a `200 OK` response code and an updated [windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7feef-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7feef-158">Example</span></span>
### <a name="request"></a><span data-ttu-id="7feef-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7feef-159">Request</span></span>
<span data-ttu-id="7feef-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7feef-160">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windows10GeneralConfiguration/assignedAccessMultiModeProfiles/{windowsAssignedAccessProfileId}
Content-type: application/json
Content-length: 297

{
  "profileName": "Profile Name value",
  "showTaskBar": true,
  "appUserModelIds": [
    "App User Model Ids value"
  ],
  "desktopAppPaths": [
    "Desktop App Paths value"
  ],
  "userAccounts": [
    "User Accounts value"
  ],
  "startMenuLayoutXml": "c3RhcnRNZW51TGF5b3V0WG1s"
}
```

### <a name="response"></a><span data-ttu-id="7feef-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7feef-161">Response</span></span>
<span data-ttu-id="7feef-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7feef-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 413

{
  "@odata.type": "#microsoft.graph.windowsAssignedAccessProfile",
  "id": "cfa70299-0299-cfa7-9902-a7cf9902a7cf",
  "profileName": "Profile Name value",
  "showTaskBar": true,
  "appUserModelIds": [
    "App User Model Ids value"
  ],
  "desktopAppPaths": [
    "Desktop App Paths value"
  ],
  "userAccounts": [
    "User Accounts value"
  ],
  "startMenuLayoutXml": "c3RhcnRNZW51TGF5b3V0WG1s"
}
```






---
title: Eliminar usuario
description: Elimina un user.
ms.openlocfilehash: 94c9909ef64f5b358c7e14d4d201a081db584851
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084150"
---
# <a name="delete-user"></a><span data-ttu-id="7f55a-103">Eliminar usuario</span><span class="sxs-lookup"><span data-stu-id="7f55a-103">Delete user</span></span>

> <span data-ttu-id="7f55a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7f55a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7f55a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7f55a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7f55a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7f55a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7f55a-107">Elimina un [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="7f55a-107">Deletes a [user](../resources/intune-shared-user.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7f55a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7f55a-108">Prerequisites</span></span>
<span data-ttu-id="7f55a-109">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="7f55a-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="7f55a-110">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7f55a-110">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>  <span data-ttu-id="7f55a-111">Los permisos específicos necesarios depende de contexto.</span><span class="sxs-lookup"><span data-stu-id="7f55a-111">The specific permission required depends on context.</span></span>

|<span data-ttu-id="7f55a-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7f55a-112">Permission type</span></span>|<span data-ttu-id="7f55a-113">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7f55a-113">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7f55a-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7f55a-114">Delegated (work or school account)</span></span>||
| <span data-ttu-id="7f55a-115">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="7f55a-115">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="7f55a-116">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7f55a-116">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
| <span data-ttu-id="7f55a-117">&nbsp;&nbsp; **MAM**</span><span class="sxs-lookup"><span data-stu-id="7f55a-117">&nbsp; &nbsp; **MAM**</span></span> | <span data-ttu-id="7f55a-118">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7f55a-118">DeviceManagementApps.ReadWrite.All</span></span>|
| <span data-ttu-id="7f55a-119">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="7f55a-119">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="7f55a-120">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7f55a-120">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
| <span data-ttu-id="7f55a-121">&nbsp; &nbsp; **Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="7f55a-121">&nbsp; &nbsp; **Troubleshooting**</span></span> | <span data-ttu-id="7f55a-122">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7f55a-122">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="7f55a-123">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7f55a-123">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7f55a-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7f55a-124">Not supported.</span></span>|
|<span data-ttu-id="7f55a-125">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7f55a-125">Application</span></span>|<span data-ttu-id="7f55a-126">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7f55a-126">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7f55a-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7f55a-127">HTTP Request</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /users/{usersId}
```

## <a name="request-headers"></a><span data-ttu-id="7f55a-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7f55a-128">Request headers</span></span>

|<span data-ttu-id="7f55a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f55a-129">Header</span></span>|<span data-ttu-id="7f55a-130">Valor</span><span class="sxs-lookup"><span data-stu-id="7f55a-130">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7f55a-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="7f55a-131">Authorization</span></span>|<span data-ttu-id="7f55a-132">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7f55a-132">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7f55a-133">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7f55a-133">Accept</span></span>|<span data-ttu-id="7f55a-134">application/json</span><span class="sxs-lookup"><span data-stu-id="7f55a-134">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7f55a-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7f55a-135">Request body</span></span>

<span data-ttu-id="7f55a-136">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7f55a-136">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7f55a-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7f55a-137">Response</span></span>

<span data-ttu-id="7f55a-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="7f55a-138">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="7f55a-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7f55a-139">Example</span></span>

### <a name="request"></a><span data-ttu-id="7f55a-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7f55a-140">Request</span></span>

<span data-ttu-id="7f55a-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7f55a-141">Here is an example of the request.</span></span>

``` http
DELETE https://graph.microsoft.com/beta/users/{usersId}
```

### <a name="response"></a><span data-ttu-id="7f55a-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7f55a-142">Response</span></span>

<span data-ttu-id="7f55a-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7f55a-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 204 No Content
```



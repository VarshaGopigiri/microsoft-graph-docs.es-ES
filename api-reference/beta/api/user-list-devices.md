---
title: Lista los dispositivos de usuario
description: Obtener una lista de los dispositivos de usuario que admiten las capacidades de Roma de proyecto. Esto incluye la capacidad para iniciar una aplicación, o de mensajes o enviar datos a una aplicación. Una vez que se realice una llamada GET en Windows Millennium Edition / dispositivos, pase el identificador del dispositivo para enviar un comando al dispositivo.
localization_priority: Normal
ms.openlocfilehash: 455a134b2edcf64255a2818887c6ff68959a1202
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855926"
---
# <a name="list-user-devices"></a><span data-ttu-id="f7acd-105">Lista los dispositivos de usuario</span><span class="sxs-lookup"><span data-stu-id="f7acd-105">List user devices</span></span>

> <span data-ttu-id="f7acd-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f7acd-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f7acd-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f7acd-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f7acd-108">Obtener una lista de los dispositivos de usuario que admiten las capacidades de Roma de proyecto.</span><span class="sxs-lookup"><span data-stu-id="f7acd-108">Get a list of user devices that support Project Rome capabilities.</span></span> <span data-ttu-id="f7acd-109">Esto incluye la capacidad para iniciar una aplicación, o de mensajes o enviar datos a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="f7acd-109">This includes the ability to launch an app, or message or send data to an application.</span></span> <span data-ttu-id="f7acd-110">Una vez que se realice una llamada GET en Windows Millennium Edition / dispositivos, pase el identificador del dispositivo para [Enviar un comando](send-device-command.md) al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f7acd-110">After you do a GET call on me/devices, pass in the ID of the device to [send a command](send-device-command.md) to your device.</span></span>

## <a name="permissions"></a><span data-ttu-id="f7acd-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="f7acd-111">Permissions</span></span>

<span data-ttu-id="f7acd-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f7acd-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="f7acd-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f7acd-114">Permission type</span></span>      | <span data-ttu-id="f7acd-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f7acd-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f7acd-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f7acd-116">Delegated (work or school account)</span></span> | <span data-ttu-id="f7acd-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f7acd-117">Not supported.</span></span>    |
|<span data-ttu-id="f7acd-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f7acd-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f7acd-119">Device.Read</span><span class="sxs-lookup"><span data-stu-id="f7acd-119">Device.Read</span></span>    |
|<span data-ttu-id="f7acd-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f7acd-120">Application</span></span> | <span data-ttu-id="f7acd-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f7acd-121">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f7acd-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f7acd-122">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET me/devices
```

## <a name="request-headers"></a><span data-ttu-id="f7acd-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f7acd-123">Request headers</span></span>

| <span data-ttu-id="f7acd-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7acd-124">Header</span></span> |<span data-ttu-id="f7acd-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f7acd-125">Value</span></span>
|:----|:------|
|<span data-ttu-id="f7acd-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="f7acd-126">Authorization</span></span>| <span data-ttu-id="f7acd-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f7acd-p105">Bearer {token}. Required.</span></span> |
|<span data-ttu-id="f7acd-129">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f7acd-129">Accept</span></span> | <span data-ttu-id="f7acd-130">application/json</span><span class="sxs-lookup"><span data-stu-id="f7acd-130">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="f7acd-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f7acd-131">Request body</span></span>
<span data-ttu-id="f7acd-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f7acd-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f7acd-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7acd-133">Response</span></span>

<span data-ttu-id="f7acd-134">Si se realiza correctamente, este método devuelve un código de 200 respuesta y las propiedades de dispositivo de usuario en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f7acd-134">If successful, this method returns a 200 response code and the user device properties in the response body.</span></span>

<!-- { "blockType": "ignored" } -->

```http
HTTP/1.1 200 OK
```

<!-- { "blockType": "ignored" } -->

```json
{
  "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#devices",
  "value": [
    {
      "name": "name",
      "id": "id",
      "status": "status",
      "platform": "platform",
      "kind": "formFactor",
      "model": "model",
      "manufacturer": "manufacturer",
    }
  ]
}
```

## <a name="example"></a><span data-ttu-id="f7acd-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7acd-135">Example</span></span>
<span data-ttu-id="f7acd-136">En este ejemplo se devolverá la lista de dispositivos para un usuario.</span><span class="sxs-lookup"><span data-stu-id="f7acd-136">This example will return the list of devices for a user.</span></span> <span data-ttu-id="f7acd-137">Para el uso de un dispositivo de comando `me/devices/{id}/command`, deberá obtener el identificador del dispositivo que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="f7acd-137">To command a device using `me/devices/{id}/command`, you will need to get the ID of the device that is returned.</span></span>

#### <a name="request"></a><span data-ttu-id="f7acd-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f7acd-138">Request</span></span>

<span data-ttu-id="f7acd-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f7acd-139">The following is an example of the request.</span></span>

<!-- {
  "blockType": "ignored",
  "name": "list_devices"
}-->

```http
GET me/devices
Authorization: Bearer Eaeou....
Content-Type: application/json; charset=utf-8
```

#### <a name="response"></a><span data-ttu-id="f7acd-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7acd-140">Response</span></span>

<span data-ttu-id="f7acd-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f7acd-141">The following is an example of the response.</span></span> <span data-ttu-id="f7acd-142">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="f7acd-142">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="f7acd-143">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f7acd-143">All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.device",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 140

{
  "value": [
    {
      "Name": "JimSurface",
      "id": "6841b3db-2b55-467b-ad84-79a41a4ef665",
      "Manufacturer": "Microsoft Corporation",
      "Model": "Surface Book",
      "Kind": "Tablet",
      "Status": "Unknown",
      "Platform": "Windows"
    }
  ]
}
```

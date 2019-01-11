---
title: Obtener el estado del comando de dispositivo
description: Obtener el estado de un comando en un dispositivo. Para obtener la lista completa de códigos de estado, vea la lista de actionStatus.
localization_priority: Normal
ms.openlocfilehash: 9dca743a50f248abee76fb4d54352df3d400ada1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883135"
---
# <a name="get-device-command-status"></a><span data-ttu-id="a5e6f-104">Obtener el estado del comando de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a5e6f-104">Get device command status</span></span>

> <span data-ttu-id="a5e6f-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a5e6f-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a5e6f-107">Obtener el estado de un comando en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-107">Get the status of a command on a device.</span></span> <span data-ttu-id="a5e6f-108">Para obtener la lista completa de códigos de estado, vea la [lista de actionStatus](#list-of-actionstatus).</span><span class="sxs-lookup"><span data-stu-id="a5e6f-108">For the  full list of status codes, see [List of actionStatus](#list-of-actionstatus).</span></span>

## <a name="permissions"></a><span data-ttu-id="a5e6f-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="a5e6f-109">Permissions</span></span>

<span data-ttu-id="a5e6f-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a5e6f-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a5e6f-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a5e6f-112">Permission type</span></span>      | <span data-ttu-id="a5e6f-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a5e6f-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a5e6f-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a5e6f-114">Delegated (work or school account)</span></span> | <span data-ttu-id="a5e6f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-115">Not supported.</span></span>    |
|<span data-ttu-id="a5e6f-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a5e6f-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a5e6f-117">Device.Command</span><span class="sxs-lookup"><span data-stu-id="a5e6f-117">Device.Command</span></span>    |
|<span data-ttu-id="a5e6f-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a5e6f-118">Application</span></span> | <span data-ttu-id="a5e6f-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a5e6f-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a5e6f-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET me/devices/{id}/commands/{id}
```

## <a name="request-headers"></a><span data-ttu-id="a5e6f-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a5e6f-121">Request headers</span></span>

| <span data-ttu-id="a5e6f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5e6f-122">Header</span></span> |<span data-ttu-id="a5e6f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a5e6f-123">Value</span></span>
|:----|:------|
|<span data-ttu-id="a5e6f-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="a5e6f-124">Authorization</span></span>| <span data-ttu-id="a5e6f-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-p105">Bearer {token}. Required.</span></span> |
|<span data-ttu-id="a5e6f-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a5e6f-127">Accept</span></span> | <span data-ttu-id="a5e6f-128">application/json</span><span class="sxs-lookup"><span data-stu-id="a5e6f-128">application/json</span></span> |

## <a name="response"></a><span data-ttu-id="a5e6f-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5e6f-129">Response</span></span>
<!-- { "blockType": "ignored" } -->

```http
HTTP/1.1 200 OK
```
<!-- { "blockType": "ignored" } -->

```json
  {
    "id": "0",
    "status": "requesting",
    "type": "null",
    "appServiceName": "null",
    "packageFamilyName": "null",
    "error": "null",
    "responsepayload": "null",
    "payload": "null",
    "permissionTicket": "null",
    "postBackUri": "null"
  }
```

## <a name="list-of-actionstatus"></a><span data-ttu-id="a5e6f-130">Lista de actionStatus</span><span class="sxs-lookup"><span data-stu-id="a5e6f-130">List of actionStatus</span></span>

- <span data-ttu-id="a5e6f-131">solicitar, / / comando se ha creado y está esperando que va a procesar</span><span class="sxs-lookup"><span data-stu-id="a5e6f-131">requesting, // Command has been created and is waiting to be processed</span></span>
- <span data-ttu-id="a5e6f-132">sentToTarget, / / comando se ha enviado al dispositivo de destino</span><span class="sxs-lookup"><span data-stu-id="a5e6f-132">sentToTarget, // Command has been sent to the target device</span></span>
- <span data-ttu-id="a5e6f-133">ejecución, / / confirma la recepción del comando de dispositivo de destino y lo ejecute</span><span class="sxs-lookup"><span data-stu-id="a5e6f-133">executing, // Target device acknowledged receipt of the command and is executing it</span></span>
- <span data-ttu-id="a5e6f-134">completado, / / completada la ejecución de comandos</span><span class="sxs-lookup"><span data-stu-id="a5e6f-134">completed, // Command execution completed</span></span>
- <span data-ttu-id="a5e6f-135">failedToSend, / / el servicio no pudo enviar el comando al dispositivo de destino</span><span class="sxs-lookup"><span data-stu-id="a5e6f-135">failedToSend, // Service failed to send command to target device</span></span>
- <span data-ttu-id="a5e6f-136">executionFailed, / / error en la ejecución de comandos</span><span class="sxs-lookup"><span data-stu-id="a5e6f-136">executionFailed, // Command execution failed</span></span>
- <span data-ttu-id="a5e6f-137">commandDropped, / / comando colocada por cliente si el dispositivo se encuentra en estado de ConnectedStandby</span><span class="sxs-lookup"><span data-stu-id="a5e6f-137">commandDropped, // Command dropped by client if device is in ConnectedStandby state</span></span>
- <span data-ttu-id="a5e6f-138">Cancelar, / / cancelar el comando</span><span class="sxs-lookup"><span data-stu-id="a5e6f-138">cancel, // Cancel the command</span></span>
- <span data-ttu-id="a5e6f-139">Si cancela, / / cancelar el comando</span><span class="sxs-lookup"><span data-stu-id="a5e6f-139">cancelling, // Cancelling the command</span></span>
- <span data-ttu-id="a5e6f-140">Canceled, / / se ha cancelado el comando</span><span class="sxs-lookup"><span data-stu-id="a5e6f-140">canceled, // Command has been cancelled</span></span>
- <span data-ttu-id="a5e6f-141">Vuelva a intentar, / / servicio está reintentando para enviar comandos al destino</span><span class="sxs-lookup"><span data-stu-id="a5e6f-141">retry, // Service is retrying to send command to target</span></span>
- <span data-ttu-id="a5e6f-142">ha expirado, / / procesamiento de comandos se ha excedido el tiempo de caducidad</span><span class="sxs-lookup"><span data-stu-id="a5e6f-142">expired, // Command processing exceeded expiry time</span></span>
- <span data-ttu-id="a5e6f-143">error, / / interno error al procesar el comando</span><span class="sxs-lookup"><span data-stu-id="a5e6f-143">error, // Internal error while processing the command</span></span>
- <span data-ttu-id="a5e6f-144">personalizado / / personalizadas estado</span><span class="sxs-lookup"><span data-stu-id="a5e6f-144">custom // Custom status</span></span>

## <a name="example"></a><span data-ttu-id="a5e6f-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a5e6f-145">Example</span></span>

<span data-ttu-id="a5e6f-146">En este ejemplo, necesitará el identificador del dispositivo y el identificador del comando al que se ha emitido a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-146">In this example, you will need the ID of the device and the ID of the command that has been issued to a device.</span></span> <span data-ttu-id="a5e6f-147">El dispositivo identificador se devuelve cuando se emite un GET llamar a `/me/devices`, y el comando identificador se devuelve cuando se realiza una devolución de llamada en `/me/devices/{id}/command`.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-147">The device ID is returned when issuing a GET call to `/me/devices`, and the command ID is returned when doing a POST call on `/me/devices/{id}/command`.</span></span>

#### <a name="request"></a><span data-ttu-id="a5e6f-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a5e6f-148">Request</span></span>

<span data-ttu-id="a5e6f-149">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-149">The following example shows the request.</span></span>

<!-- {
  "blockType": "ignored",
  "name": "get_command"
} -->
```http
GET me/devices/{id}/commands/{id}
Authorization: Bearer Eaeou....
Content-Type: application/json; charset=utf-8
```

#### <a name="response"></a><span data-ttu-id="a5e6f-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5e6f-150">Response</span></span>

<span data-ttu-id="a5e6f-151">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-151">The following example shows the response.</span></span>
<!-- {
  "blockType": "ignored",
  "truncated": false,
  "@odata.type": "microsoft.graph.commandobject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK

{
  "value":
  {
    "id": "0158355AD4D680CC4E2994CC009EFFD7337D1335FCA6ED266…",
    "status": "completed",
    "type": null,
    "appServiceName": null,
    "packageFamilyName": null,
    "error": null,
    "permissionTicket": null,
    "postBackUri": null,
    "payload": null
  }
}
```


## <a name="get-command-payload"></a><span data-ttu-id="a5e6f-152">Obtener la carga de comando</span><span class="sxs-lookup"><span data-stu-id="a5e6f-152">Get command payload</span></span>

<span data-ttu-id="a5e6f-153">Obtenga una carga de respuesta para una acción específica en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-153">Get a response payload for a specific action on a device.</span></span> <span data-ttu-id="a5e6f-154">La carga de respuesta se usa al consultar un servicio de aplicación para transportar datos atrás.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-154">The response payload is used when querying an app service to carry data back.</span></span>


### <a name="permissions"></a><span data-ttu-id="a5e6f-155">Permisos</span><span class="sxs-lookup"><span data-stu-id="a5e6f-155">Permissions</span></span>

<span data-ttu-id="a5e6f-p108">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a5e6f-p108">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a5e6f-158">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a5e6f-158">Permission type</span></span>      | <span data-ttu-id="a5e6f-159">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a5e6f-159">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a5e6f-160">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a5e6f-160">Delegated (work or school account)</span></span> | <span data-ttu-id="a5e6f-161">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-161">Not supported.</span></span>    |
|<span data-ttu-id="a5e6f-162">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a5e6f-162">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a5e6f-163">Device.Command</span><span class="sxs-lookup"><span data-stu-id="a5e6f-163">Device.Command</span></span>    |
|<span data-ttu-id="a5e6f-164">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a5e6f-164">Application</span></span> | <span data-ttu-id="a5e6f-165">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-165">Not supported.</span></span> |

### <a name="http-request"></a><span data-ttu-id="a5e6f-166">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a5e6f-166">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET me/devices/{id}/command/{id}/responsePayload
```

### <a name="request-headers"></a><span data-ttu-id="a5e6f-167">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a5e6f-167">Request headers</span></span>

| <span data-ttu-id="a5e6f-168">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5e6f-168">Header</span></span> |<span data-ttu-id="a5e6f-169">Valor</span><span class="sxs-lookup"><span data-stu-id="a5e6f-169">Value</span></span>
|:----|:------|
|<span data-ttu-id="a5e6f-170">Authorization</span><span class="sxs-lookup"><span data-stu-id="a5e6f-170">Authorization</span></span>| <span data-ttu-id="a5e6f-p109">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-p109">Bearer {token}. Required.</span></span> |
|<span data-ttu-id="a5e6f-173">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a5e6f-173">Accept</span></span> | <span data-ttu-id="a5e6f-174">application/json</span><span class="sxs-lookup"><span data-stu-id="a5e6f-174">application/json</span></span> |

### <a name="response"></a><span data-ttu-id="a5e6f-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5e6f-175">Response</span></span>
<!-- { "blockType": "ignored" } -->

```http
HTTP/1.1 200 OK
```
<!-- { "blockType": "ignored" } -->

```json
{
  "@odata.context": "https://graph.microsoft.com/devices/$metadata#microsoft.graph.PayloadResponse",
  "MsIgnoredParameter":0,
  "CreationDate":"date-time",
  "Type":"Ok"
}
```

### <a name="example"></a><span data-ttu-id="a5e6f-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a5e6f-176">Example</span></span>

<span data-ttu-id="a5e6f-177">En este ejemplo, necesitará el identificador del dispositivo y el identificador del comando al que se ha emitido a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-177">In this example, you will need the ID of the device and the ID of the command that has been issued to a device.</span></span> <span data-ttu-id="a5e6f-178">El dispositivo identificador se devuelve cuando se emite un GET llamar en `/me/devices`, y el comando identificador se devuelve cuando se realiza una devolución de llamada en `/me/devices/{id}/command`.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-178">The device ID is returned when issuing a GET call on `/me/devices`, and the command ID is returned when doing a POST call on `/me/devices/{id}/command`.</span></span>

#### <a name="request"></a><span data-ttu-id="a5e6f-179">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a5e6f-179">Request</span></span>

<span data-ttu-id="a5e6f-180">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-180">The following example shows the request.</span></span>

<!-- { 
  "blockType": "ignored",
  "name": "get_command_payload"
} -->
```http
GET me/devices/{id}/commands/{id}
Authorization: Bearer Eaeou....
Content-Type: application/json; charset=utf-8
```

#### <a name="response"></a><span data-ttu-id="a5e6f-181">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5e6f-181">Response</span></span>

<span data-ttu-id="a5e6f-182">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5e6f-182">The following example shows the response.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": false,
  "@odata.type": "microsoft.graph.commandobject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK

{
  "@odata.context": "https://graph.microsoft.com/devices/$metadata#microsoft.graph.PayloadResponse",
  "MsIgnoredParameter":0,
  "CreationDate":"04/27/2017",
  "Type":"Ok"
}
```

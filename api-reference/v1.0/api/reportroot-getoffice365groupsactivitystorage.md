---
title: 'reportRoot: getOffice365GroupsActivityStorage'
description: Obtiene el total de almacenamiento usado en todos los buzones de grupo y sitios de grupo.
ms.openlocfilehash: 636a23e8bb094e31c648a701a59f55a8c7c6c73d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031875"
---
# <a name="reportroot-getoffice365groupsactivitystorage"></a><span data-ttu-id="e5a6c-103">reportRoot: getOffice365GroupsActivityStorage</span><span class="sxs-lookup"><span data-stu-id="e5a6c-103">reportRoot: getOffice365GroupsActivityStorage</span></span>

<span data-ttu-id="e5a6c-104">Obtiene el total de almacenamiento usado en todos los buzones de grupo y sitios de grupo.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-104">Get the total storage used across all group mailboxes and group sites.</span></span>

> <span data-ttu-id="e5a6c-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Grupos de Office 365](https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40).</span><span class="sxs-lookup"><span data-stu-id="e5a6c-105">**Note:** For details about different report views and names, see [Office 365 Reports - Office 365 groups](https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40).</span></span>

## <a name="permissions"></a><span data-ttu-id="e5a6c-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="e5a6c-106">Permissions</span></span>

<span data-ttu-id="e5a6c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e5a6c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="e5a6c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e5a6c-109">Permission type</span></span>                        | <span data-ttu-id="e5a6c-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e5a6c-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="e5a6c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e5a6c-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="e5a6c-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="e5a6c-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="e5a6c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e5a6c-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e5a6c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-114">Not supported.</span></span>                           |
| <span data-ttu-id="e5a6c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e5a6c-115">Application</span></span>                            | <span data-ttu-id="e5a6c-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="e5a6c-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="e5a6c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e5a6c-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365GroupsActivityStorage(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="e5a6c-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="e5a6c-118">Function parameters</span></span>

<span data-ttu-id="e5a6c-119">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-119">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="e5a6c-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e5a6c-120">Parameter</span></span> | <span data-ttu-id="e5a6c-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5a6c-121">Type</span></span>   | <span data-ttu-id="e5a6c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5a6c-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="e5a6c-123">period</span><span class="sxs-lookup"><span data-stu-id="e5a6c-123">period</span></span>    | <span data-ttu-id="e5a6c-124">cadena</span><span class="sxs-lookup"><span data-stu-id="e5a6c-124">string</span></span> | <span data-ttu-id="e5a6c-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="e5a6c-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="e5a6c-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="e5a6c-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-128">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="e5a6c-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e5a6c-129">Request headers</span></span>

| <span data-ttu-id="e5a6c-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="e5a6c-130">Name</span></span>          | <span data-ttu-id="e5a6c-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5a6c-131">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="e5a6c-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="e5a6c-132">Authorization</span></span> | <span data-ttu-id="e5a6c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="e5a6c-135">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="e5a6c-135">If-None-Match</span></span> | <span data-ttu-id="e5a6c-136">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-136">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="e5a6c-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-137">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="e5a6c-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5a6c-138">Response</span></span>

<span data-ttu-id="e5a6c-139">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-139">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="e5a6c-140">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-140">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="e5a6c-141">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-141">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="e5a6c-142">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-142">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="e5a6c-143">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="e5a6c-143">Report Refresh Date</span></span>
- <span data-ttu-id="e5a6c-144">Almacenamiento de buzón usado (bytes)</span><span class="sxs-lookup"><span data-stu-id="e5a6c-144">Mailbox Storage Used (Byte)</span></span>
- <span data-ttu-id="e5a6c-145">Almacenamiento de sitio usado (bytes)</span><span class="sxs-lookup"><span data-stu-id="e5a6c-145">Site Storage Used (Byte)</span></span>
- <span data-ttu-id="e5a6c-146">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="e5a6c-146">Report Date</span></span>
- <span data-ttu-id="e5a6c-147">Período del informe</span><span class="sxs-lookup"><span data-stu-id="e5a6c-147">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="e5a6c-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e5a6c-148">Example</span></span>

#### <a name="request"></a><span data-ttu-id="e5a6c-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e5a6c-149">Request</span></span>

<span data-ttu-id="e5a6c-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-150">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getoffice365groupsactivitystorage"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365GroupsActivityStorage(period='D7')
```

#### <a name="response"></a><span data-ttu-id="e5a6c-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5a6c-151">Response</span></span>

<span data-ttu-id="e5a6c-152">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-152">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.report"
} -->

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="e5a6c-153">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="e5a6c-153">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Mailbox Storage Used (Byte),Site Storage Used (Byte),Report Date,Report Period
```

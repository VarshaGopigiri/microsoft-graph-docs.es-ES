---
title: 'reportRoot: getOffice365ActiveUserCounts'
description: Obtiene el número de usuarios activos diarios en el período de informe por producto.
ms.openlocfilehash: 1abf72b50e7e6d6654d962757c0d28df967b8694
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032531"
---
# <a name="reportroot-getoffice365activeusercounts"></a><span data-ttu-id="7f9b2-103">reportRoot: getOffice365ActiveUserCounts</span><span class="sxs-lookup"><span data-stu-id="7f9b2-103">reportRoot: getOffice365ActiveUserCounts</span></span>

<span data-ttu-id="7f9b2-104">Obtiene el número de usuarios activos diarios en el período de informe por producto.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-104">Get the count of daily active users in the reporting period by product.</span></span>

> <span data-ttu-id="7f9b2-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Usuarios activos](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span><span class="sxs-lookup"><span data-stu-id="7f9b2-105">**Note:** For details about different report views and names, see [Office 365 Reports - Active Users](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span></span>

## <a name="permissions"></a><span data-ttu-id="7f9b2-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="7f9b2-106">Permissions</span></span>

<span data-ttu-id="7f9b2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7f9b2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="7f9b2-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7f9b2-109">Permission type</span></span>                        | <span data-ttu-id="7f9b2-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7f9b2-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="7f9b2-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7f9b2-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="7f9b2-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="7f9b2-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="7f9b2-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7f9b2-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7f9b2-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-114">Not supported.</span></span>                           |
| <span data-ttu-id="7f9b2-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7f9b2-115">Application</span></span>                            | <span data-ttu-id="7f9b2-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="7f9b2-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="7f9b2-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7f9b2-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365ActiveUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="7f9b2-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="7f9b2-118">Function parameters</span></span>

<span data-ttu-id="7f9b2-119">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-119">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="7f9b2-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7f9b2-120">Parameter</span></span> | <span data-ttu-id="7f9b2-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="7f9b2-121">Type</span></span>   | <span data-ttu-id="7f9b2-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="7f9b2-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="7f9b2-123">period</span><span class="sxs-lookup"><span data-stu-id="7f9b2-123">period</span></span>    | <span data-ttu-id="7f9b2-124">cadena</span><span class="sxs-lookup"><span data-stu-id="7f9b2-124">string</span></span> | <span data-ttu-id="7f9b2-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="7f9b2-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="7f9b2-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="7f9b2-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-128">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="7f9b2-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7f9b2-129">Request headers</span></span>

| <span data-ttu-id="7f9b2-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="7f9b2-130">Name</span></span>          | <span data-ttu-id="7f9b2-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="7f9b2-131">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="7f9b2-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="7f9b2-132">Authorization</span></span> | <span data-ttu-id="7f9b2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="7f9b2-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7f9b2-135">Response</span></span>

<span data-ttu-id="7f9b2-136">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-136">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="7f9b2-137">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-137">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="7f9b2-138">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-138">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="7f9b2-139">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-139">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="7f9b2-140">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="7f9b2-140">Report Refresh Date</span></span>
- <span data-ttu-id="7f9b2-141">Office 365</span><span class="sxs-lookup"><span data-stu-id="7f9b2-141">Office 365</span></span>
- <span data-ttu-id="7f9b2-142">Exchange</span><span class="sxs-lookup"><span data-stu-id="7f9b2-142">Exchange</span></span>
- <span data-ttu-id="7f9b2-143">OneDrive</span><span class="sxs-lookup"><span data-stu-id="7f9b2-143">OneDrive</span></span>
- <span data-ttu-id="7f9b2-144">SharePoint</span><span class="sxs-lookup"><span data-stu-id="7f9b2-144">SharePoint</span></span>
- <span data-ttu-id="7f9b2-145">Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="7f9b2-145">Skype For Business</span></span> 
- <span data-ttu-id="7f9b2-146">Yammer</span><span class="sxs-lookup"><span data-stu-id="7f9b2-146">Yammer</span></span>
- <span data-ttu-id="7f9b2-147">Teams</span><span class="sxs-lookup"><span data-stu-id="7f9b2-147">Teams</span></span>
- <span data-ttu-id="7f9b2-148">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="7f9b2-148">Report Date</span></span>
- <span data-ttu-id="7f9b2-149">Período del informe</span><span class="sxs-lookup"><span data-stu-id="7f9b2-149">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="7f9b2-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7f9b2-150">Example</span></span>

#### <a name="request"></a><span data-ttu-id="7f9b2-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7f9b2-151">Request</span></span>

<span data-ttu-id="7f9b2-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-152">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getoffice365activeusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365ActiveUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="7f9b2-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7f9b2-153">Response</span></span>

<span data-ttu-id="7f9b2-154">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-154">The following is an example of the response.</span></span>

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

<span data-ttu-id="7f9b2-155">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="7f9b2-155">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Office 365,Exchange,OneDrive,SharePoint,Skype For Business,Yammer,Teams,Report Date,Report Period
```

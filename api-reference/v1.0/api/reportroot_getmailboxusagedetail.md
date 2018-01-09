# <a name="reportroot-getmailboxusagedetail"></a><span data-ttu-id="bfdbb-101">reportRoot: getMailboxUsageDetail</span><span class="sxs-lookup"><span data-stu-id="bfdbb-101">reportRoot: getMailboxUsageDetail</span></span>

<span data-ttu-id="bfdbb-102">Obtiene información sobre el uso de buzones.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-102">Get details about mailbox usage.</span></span>

> <span data-ttu-id="bfdbb-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de buzones]((https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729)).</span><span class="sxs-lookup"><span data-stu-id="bfdbb-103">**Note:** For details about different report views and names, see [Office 365 Reports - Mailbox usage]((https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729)).</span></span>

## <a name="permissions"></a><span data-ttu-id="bfdbb-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="bfdbb-104">Permissions</span></span>

<span data-ttu-id="bfdbb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bfdbb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="bfdbb-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bfdbb-107">Permission type</span></span>                        | <span data-ttu-id="bfdbb-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bfdbb-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="bfdbb-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bfdbb-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="bfdbb-110">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-110">Not supported.</span></span>                           |
| <span data-ttu-id="bfdbb-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bfdbb-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bfdbb-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-112">Not supported.</span></span>                           |
| <span data-ttu-id="bfdbb-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bfdbb-113">Application</span></span>                            | <span data-ttu-id="bfdbb-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="bfdbb-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="bfdbb-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bfdbb-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getMailboxUsageDetail(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="bfdbb-116">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bfdbb-116">Request parameters</span></span>

<span data-ttu-id="bfdbb-117">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-117">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="bfdbb-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bfdbb-118">Parameter</span></span> | <span data-ttu-id="bfdbb-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="bfdbb-119">Type</span></span>   | <span data-ttu-id="bfdbb-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfdbb-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="bfdbb-121">period</span><span class="sxs-lookup"><span data-stu-id="bfdbb-121">Period</span></span>    | <span data-ttu-id="bfdbb-122">cadena</span><span class="sxs-lookup"><span data-stu-id="bfdbb-122">string</span></span> | <span data-ttu-id="bfdbb-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="bfdbb-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="bfdbb-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="bfdbb-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-126">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="bfdbb-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bfdbb-127">Request headers</span></span>

| <span data-ttu-id="bfdbb-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="bfdbb-128">Name</span></span>          | <span data-ttu-id="bfdbb-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfdbb-129">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="bfdbb-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="bfdbb-130">Authorization</span></span> | <span data-ttu-id="bfdbb-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="bfdbb-133">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="bfdbb-133">if-none-match</span></span> | <span data-ttu-id="bfdbb-134">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-134">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `304 Not Modified` response is returned.</span></span> <span data-ttu-id="bfdbb-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-135">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="bfdbb-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfdbb-136">Response</span></span>

<span data-ttu-id="bfdbb-137">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-137">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="bfdbb-138">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-138">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="bfdbb-139">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-139">Pre-authenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header to download.</span></span>

<span data-ttu-id="bfdbb-140">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-140">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="bfdbb-141">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="bfdbb-141">Report Refresh Date</span></span>
- <span data-ttu-id="bfdbb-142">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="bfdbb-142">User Principal Name</span></span>
- <span data-ttu-id="bfdbb-143">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="bfdbb-143">Display Name</span></span>
- <span data-ttu-id="bfdbb-144">Eliminado</span><span class="sxs-lookup"><span data-stu-id="bfdbb-144">Is Deleted</span></span>
- <span data-ttu-id="bfdbb-145">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="bfdbb-145">Deleted Date</span></span>
- <span data-ttu-id="bfdbb-146">Fecha de creación</span><span class="sxs-lookup"><span data-stu-id="bfdbb-146">Created Date</span></span>
- <span data-ttu-id="bfdbb-147">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="bfdbb-147">Last Activity Date</span></span>
- <span data-ttu-id="bfdbb-148">Número de elementos</span><span class="sxs-lookup"><span data-stu-id="bfdbb-148">Item Count</span></span>
- <span data-ttu-id="bfdbb-149">Almacenamiento usado (bytes)</span><span class="sxs-lookup"><span data-stu-id="bfdbb-149">Storage Used (Byte)</span></span>
- <span data-ttu-id="bfdbb-150">Cuota de advertencia de problema (bytes)</span><span class="sxs-lookup"><span data-stu-id="bfdbb-150">Issue Warning Quota (Byte)</span></span>
- <span data-ttu-id="bfdbb-151">Cuota de prohibición de envío (bytes)</span><span class="sxs-lookup"><span data-stu-id="bfdbb-151">Prohibit Send Quota (Byte)</span></span>
- <span data-ttu-id="bfdbb-152">Cuota de prohibición de envío o recepción (bytes)</span><span class="sxs-lookup"><span data-stu-id="bfdbb-152">Prohibit Send/Receive Quota (Byte)</span></span>
- <span data-ttu-id="bfdbb-153">Período del informe</span><span class="sxs-lookup"><span data-stu-id="bfdbb-153">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="bfdbb-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bfdbb-154">Example</span></span>

#### <a name="request"></a><span data-ttu-id="bfdbb-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bfdbb-155">Request</span></span>

<span data-ttu-id="bfdbb-156">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-156">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getmailboxusageuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getMailboxUsageDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="bfdbb-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfdbb-157">Response</span></span>

<span data-ttu-id="bfdbb-158">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-158">Here is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="bfdbb-159">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="bfdbb-159">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,Is Deleted,Deleted Date,Created Date,Last Activity Date,Item Count,Storage Used (Byte),Issue Warning Quota (Byte),Prohibit Send Quota (Byte),Prohibit Send/Receive Quota (Byte),Report Period
```

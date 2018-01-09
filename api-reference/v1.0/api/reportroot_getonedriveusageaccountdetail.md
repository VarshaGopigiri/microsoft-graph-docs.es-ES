# <a name="reportroot-getonedriveusageaccountdetail"></a><span data-ttu-id="1e848-101">reportRoot: getOneDriveUsageAccountDetail</span><span class="sxs-lookup"><span data-stu-id="1e848-101">reportRoot: getOneDriveUsageAccountDetail</span></span>

<span data-ttu-id="1e848-102">Obtiene información sobre el uso de OneDrive por cuenta.</span><span class="sxs-lookup"><span data-stu-id="1e848-102">Get details about OneDrive usage by account.</span></span>

> <span data-ttu-id="1e848-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de OneDrive para la Empresa]((https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)).</span><span class="sxs-lookup"><span data-stu-id="1e848-103">**Note:** For details about different report views and names, see [Office 365 Reports - OneDrive for Business usage]((https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)).</span></span>

## <a name="permissions"></a><span data-ttu-id="1e848-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="1e848-104">Permissions</span></span>

<span data-ttu-id="1e848-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1e848-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="1e848-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1e848-107">Permission type</span></span>                        | <span data-ttu-id="1e848-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1e848-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="1e848-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1e848-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="1e848-110">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1e848-110">Not supported.</span></span>                           |
| <span data-ttu-id="1e848-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1e848-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1e848-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1e848-112">Not supported.</span></span>                           |
| <span data-ttu-id="1e848-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1e848-113">Application</span></span>                            | <span data-ttu-id="1e848-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="1e848-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="1e848-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1e848-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOneDriveUsageAccountDetail(period='{period_value}')
GET /reports/getOneDriveUsageAccountDetail(date={date_value})
```

## <a name="request-parameters"></a><span data-ttu-id="1e848-116">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1e848-116">Request parameters</span></span>

<span data-ttu-id="1e848-117">En la URL de la solicitud, especifique el parámetro de consulta seleccionado con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="1e848-117">In the request URL, provide the chosen query parameter with a valid value.</span></span>

| <span data-ttu-id="1e848-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1e848-118">Parameter</span></span> | <span data-ttu-id="1e848-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="1e848-119">Type</span></span>   | <span data-ttu-id="1e848-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e848-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="1e848-121">period</span><span class="sxs-lookup"><span data-stu-id="1e848-121">Period</span></span>    | <span data-ttu-id="1e848-122">cadena</span><span class="sxs-lookup"><span data-stu-id="1e848-122">string</span></span> | <span data-ttu-id="1e848-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="1e848-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="1e848-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="1e848-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="1e848-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="1e848-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="1e848-126">date</span><span class="sxs-lookup"><span data-stu-id="1e848-126">date</span></span>      | <span data-ttu-id="1e848-127">Fecha</span><span class="sxs-lookup"><span data-stu-id="1e848-127">Date</span></span>   | <span data-ttu-id="1e848-128">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="1e848-128">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="1e848-129">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="1e848-129">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="1e848-130">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="1e848-130">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="1e848-131">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="1e848-131">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1e848-132">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1e848-132">Request headers</span></span>

| <span data-ttu-id="1e848-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="1e848-133">Name</span></span>          | <span data-ttu-id="1e848-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e848-134">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="1e848-135">Authorization</span><span class="sxs-lookup"><span data-stu-id="1e848-135">Authorization</span></span> | <span data-ttu-id="1e848-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1e848-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1e848-138">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="1e848-138">if-none-match</span></span> | <span data-ttu-id="1e848-139">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="1e848-139">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `304 Not Modified` response is returned.</span></span> <span data-ttu-id="1e848-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1e848-140">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="1e848-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1e848-141">Response</span></span>

<span data-ttu-id="1e848-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="1e848-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="1e848-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1e848-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="1e848-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="1e848-144">Pre-authenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header to download.</span></span>

<span data-ttu-id="1e848-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="1e848-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="1e848-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="1e848-146">Report Refresh Date</span></span>
- <span data-ttu-id="1e848-147">Dirección URL del sitio</span><span class="sxs-lookup"><span data-stu-id="1e848-147">Site URL</span></span>
- <span data-ttu-id="1e848-148">Nombre para mostrar del propietario</span><span class="sxs-lookup"><span data-stu-id="1e848-148">Owner Display Name</span></span>
- <span data-ttu-id="1e848-149">Eliminado</span><span class="sxs-lookup"><span data-stu-id="1e848-149">Is Deleted</span></span>
- <span data-ttu-id="1e848-150">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="1e848-150">Last Activity Date</span></span>
- <span data-ttu-id="1e848-151">Número de archivos</span><span class="sxs-lookup"><span data-stu-id="1e848-151">File Count</span></span>
- <span data-ttu-id="1e848-152">Número de archivos activos</span><span class="sxs-lookup"><span data-stu-id="1e848-152">Active File Count</span></span>
- <span data-ttu-id="1e848-153">Almacenamiento usado (bytes)</span><span class="sxs-lookup"><span data-stu-id="1e848-153">Storage Used (Byte)</span></span>
- <span data-ttu-id="1e848-154">Almacenamiento asignado (bytes)</span><span class="sxs-lookup"><span data-stu-id="1e848-154">Storage Allocated (Byte)</span></span>
- <span data-ttu-id="1e848-155">Período del informe</span><span class="sxs-lookup"><span data-stu-id="1e848-155">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="1e848-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1e848-156">Example</span></span>

#### <a name="request"></a><span data-ttu-id="1e848-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1e848-157">Request</span></span>

<span data-ttu-id="1e848-158">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1e848-158">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getonedriveusageuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOneDriveUsageAccountDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="1e848-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1e848-159">Response</span></span>

<span data-ttu-id="1e848-160">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1e848-160">Here is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="1e848-161">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="1e848-161">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Site URL,Owner Display Name,Is Deleted,Last Activity Date,File Count,Active File Count,Storage Used (Byte),Storage Allocated (Byte),Report Period
```

# <a name="reportroot-getskypeforbusinessactivityuserdetail"></a><span data-ttu-id="dbb20-101">reportRoot: getSkypeForBusinessActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="dbb20-101">reportRoot: getSkypeForBusinessActivityUserDetail</span></span>

<span data-ttu-id="dbb20-102">Obtiene información sobre la actividad de Skype Empresarial por usuario.</span><span class="sxs-lookup"><span data-stu-id="dbb20-102">Get details about Skype for Business activity by user.</span></span>

> <span data-ttu-id="dbb20-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-activity-8cbe2eb2-1194-4fd7-b1ee-9f9287c82424).</span><span class="sxs-lookup"><span data-stu-id="dbb20-103">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business activity](https://support.office.com/client/Skype-for-Business-Online-activity-8cbe2eb2-1194-4fd7-b1ee-9f9287c82424).</span></span>

## <a name="permissions"></a><span data-ttu-id="dbb20-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="dbb20-104">Permissions</span></span>

<span data-ttu-id="dbb20-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="dbb20-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="dbb20-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dbb20-107">Permission type</span></span>                        | <span data-ttu-id="dbb20-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dbb20-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="dbb20-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dbb20-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="dbb20-110">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="dbb20-110">Reports.Read.All</span></span>                         |
| <span data-ttu-id="dbb20-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dbb20-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dbb20-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dbb20-112">Not supported.</span></span>                           |
| <span data-ttu-id="dbb20-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dbb20-113">Application</span></span>                            | <span data-ttu-id="dbb20-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="dbb20-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="dbb20-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dbb20-115">HTTP request</span></span>

<!-- { "blockType": "samples" } --> 

```http
GET /reports/getSkypeForBusinessActivityUserDetail(period='{period_value}')
GET /reports/getSkypeForBusinessActivityUserDetail(date={date_value})
```

## <a name="request-parameters"></a><span data-ttu-id="dbb20-116">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dbb20-116">Request parameters</span></span>

<span data-ttu-id="dbb20-117">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="dbb20-117">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="dbb20-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dbb20-118">Parameter</span></span> | <span data-ttu-id="dbb20-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="dbb20-119">Type</span></span>   | <span data-ttu-id="dbb20-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbb20-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="dbb20-121">period</span><span class="sxs-lookup"><span data-stu-id="dbb20-121">period</span></span>    | <span data-ttu-id="dbb20-122">cadena</span><span class="sxs-lookup"><span data-stu-id="dbb20-122">string</span></span> | <span data-ttu-id="dbb20-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="dbb20-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="dbb20-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="dbb20-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="dbb20-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="dbb20-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="dbb20-126">date</span><span class="sxs-lookup"><span data-stu-id="dbb20-126">date</span></span>      | <span data-ttu-id="dbb20-127">Fecha</span><span class="sxs-lookup"><span data-stu-id="dbb20-127">Date</span></span>   | <span data-ttu-id="dbb20-128">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="dbb20-128">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="dbb20-129">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="dbb20-129">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="dbb20-130">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="dbb20-130">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="dbb20-131">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="dbb20-131">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="dbb20-132">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dbb20-132">Request headers</span></span>

| <span data-ttu-id="dbb20-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="dbb20-133">Name</span></span>          | <span data-ttu-id="dbb20-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbb20-134">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="dbb20-135">Authorization</span><span class="sxs-lookup"><span data-stu-id="dbb20-135">Authorization</span></span> | <span data-ttu-id="dbb20-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dbb20-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="dbb20-138">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="dbb20-138">If-None-Match</span></span> | <span data-ttu-id="dbb20-139">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="dbb20-139">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="dbb20-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="dbb20-140">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="dbb20-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dbb20-141">Response</span></span>

<span data-ttu-id="dbb20-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="dbb20-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="dbb20-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dbb20-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="dbb20-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="dbb20-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="dbb20-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="dbb20-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="dbb20-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="dbb20-146">Report Refresh Date</span></span>
- <span data-ttu-id="dbb20-147">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="dbb20-147">User Principal Name</span></span>
- <span data-ttu-id="dbb20-148">Eliminado</span><span class="sxs-lookup"><span data-stu-id="dbb20-148">Is Deleted</span></span>
- <span data-ttu-id="dbb20-149">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="dbb20-149">Deleted Date</span></span>
- <span data-ttu-id="dbb20-150">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="dbb20-150">Last Activity Date</span></span>
- <span data-ttu-id="dbb20-151">Número total de sesiones de punto a punto</span><span class="sxs-lookup"><span data-stu-id="dbb20-151">Total Peer-to-peer Session Count</span></span>
- <span data-ttu-id="dbb20-152">Número total de conferencias organizadas</span><span class="sxs-lookup"><span data-stu-id="dbb20-152">Total Organized Conference Count</span></span>
- <span data-ttu-id="dbb20-153">Número total de conferencias en las que participó</span><span class="sxs-lookup"><span data-stu-id="dbb20-153">Total Participated Conference Count</span></span>
- <span data-ttu-id="dbb20-154">Fecha de la última actividad de punto a punto</span><span class="sxs-lookup"><span data-stu-id="dbb20-154">Peer-to-peer Last Activity Date</span></span>
- <span data-ttu-id="dbb20-155">Fecha de la última actividad de una conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="dbb20-155">Organized Conference Last Activity Date</span></span>
- <span data-ttu-id="dbb20-156">Fecha de la última actividad de una conferencia en la que participó</span><span class="sxs-lookup"><span data-stu-id="dbb20-156">Participated Conference Last Activity Date</span></span>
- <span data-ttu-id="dbb20-157">Números de mensajes instantáneos de punto a punto</span><span class="sxs-lookup"><span data-stu-id="dbb20-157">Peer-to-peer IM Count</span></span>
- <span data-ttu-id="dbb20-158">Número de sesiones de audio de punto a punto</span><span class="sxs-lookup"><span data-stu-id="dbb20-158">Peer-to-peer Audio Count</span></span>
- <span data-ttu-id="dbb20-159">Minutos de audio de punto a punto</span><span class="sxs-lookup"><span data-stu-id="dbb20-159">Peer-to-peer Audio Minutes</span></span>
- <span data-ttu-id="dbb20-160">Número de sesiones de vídeo de punto a punto</span><span class="sxs-lookup"><span data-stu-id="dbb20-160">Peer-to-peer Video Count</span></span>
- <span data-ttu-id="dbb20-161">Minutos de vídeo de punto a punto</span><span class="sxs-lookup"><span data-stu-id="dbb20-161">Peer-to-peer Video Minutes</span></span>
- <span data-ttu-id="dbb20-162">Número de sesiones de uso compartido de aplicaciones de punto a punto</span><span class="sxs-lookup"><span data-stu-id="dbb20-162">Peer-to-peer App Sharing Count</span></span>
- <span data-ttu-id="dbb20-163">Número de transferencias de archivos de punto a punto</span><span class="sxs-lookup"><span data-stu-id="dbb20-163">Peer-to-peer File Transfer Count</span></span>
- <span data-ttu-id="dbb20-164">Número de mensajes instantáneos de conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="dbb20-164">Organized Conference IM Count</span></span>
- <span data-ttu-id="dbb20-165">Número de sesiones de audio o vídeo de conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="dbb20-165">Organized Conference Audio/Video Count</span></span>
- <span data-ttu-id="dbb20-166">Minutos de sesiones de audio o vídeo de conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="dbb20-166">Organized Conference Audio/Video Minutes</span></span>
- <span data-ttu-id="dbb20-167">Número de sesiones de uso compartido de aplicaciones se conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="dbb20-167">Organized Conference App Sharing Count</span></span>
- <span data-ttu-id="dbb20-168">Número de sesiones web de conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="dbb20-168">Organized Conference Web Count</span></span>
- <span data-ttu-id="dbb20-169">Número de conferencias de acceso telefónico local o aceptación de llamada organizadas por terceros</span><span class="sxs-lookup"><span data-stu-id="dbb20-169">Organized Conference Dial-in/out 3rd Party Count</span></span>
- <span data-ttu-id="dbb20-170">Número de conferencias de acceso telefónico local o aceptación de llamada organizadas por Microsoft</span><span class="sxs-lookup"><span data-stu-id="dbb20-170">Organized Conference Dial-in/out Microsoft Count</span></span>
- <span data-ttu-id="dbb20-171">Minutos de conferencias de acceso telefónico local organizadas por Microsoft</span><span class="sxs-lookup"><span data-stu-id="dbb20-171">Organized Conference Dial-in Microsoft Minutes</span></span>
- <span data-ttu-id="dbb20-172">Minutos de conferencias por aceptación de llamada organizadas por Microsoft</span><span class="sxs-lookup"><span data-stu-id="dbb20-172">Organized Conference Dial-out Microsoft Minutes</span></span>
- <span data-ttu-id="dbb20-173">Número de mensajes instantáneos de conferencias en la que participó</span><span class="sxs-lookup"><span data-stu-id="dbb20-173">Paricipated Conference IM Count</span></span>
- <span data-ttu-id="dbb20-174">Número de sesiones de audio o vídeo de conferencias en las que participó</span><span class="sxs-lookup"><span data-stu-id="dbb20-174">Participated Conference Audio/Video Count</span></span>
- <span data-ttu-id="dbb20-175">Minutos de audio o vídeo de conferencias en las que participó</span><span class="sxs-lookup"><span data-stu-id="dbb20-175">Participated Conference Audio/Video Minutes</span></span>
- <span data-ttu-id="dbb20-176">Número de sesiones de uso compartido de aplicaciones de conferencias en las que participó</span><span class="sxs-lookup"><span data-stu-id="dbb20-176">Participated Conference App Sharing Count</span></span>
- <span data-ttu-id="dbb20-177">Número de sesiones web de conferencias en las que participó</span><span class="sxs-lookup"><span data-stu-id="dbb20-177">Participated Conference Web Count</span></span>
- <span data-ttu-id="dbb20-178">Número de conferencias de acceso telefónico local o aceptación de llamada de terceros en las que participó</span><span class="sxs-lookup"><span data-stu-id="dbb20-178">Participated Conference Dial-in/out 3rd Party Count</span></span>
- <span data-ttu-id="dbb20-179">Productos asignados</span><span class="sxs-lookup"><span data-stu-id="dbb20-179">Assigned Products</span></span>
- <span data-ttu-id="dbb20-180">Período del informe</span><span class="sxs-lookup"><span data-stu-id="dbb20-180">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="dbb20-181">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dbb20-181">Example</span></span>

#### <a name="request"></a><span data-ttu-id="dbb20-182">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dbb20-182">Request</span></span>

<span data-ttu-id="dbb20-183">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dbb20-183">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getskypeforbusinessactivityuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessActivityUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="dbb20-184">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dbb20-184">Response</span></span>

<span data-ttu-id="dbb20-185">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dbb20-185">The following is an example of the response.</span></span>

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

<span data-ttu-id="dbb20-186">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="dbb20-186">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Is Deleted,Deleted Date,Last Activity Date,Total Peer-to-peer Session Count,Total Organized Conference Count,Total Participated Conference Count,Peer-to-peer Last Activity Date,Organized Conference Last Activity Date,Participated Conference Last Activity Date,Peer-to-peer IM Count,Peer-to-peer Audio Count,Peer-to-peer Audio Minutes,Peer-to-peer Video Count,Peer-to-peer Video Minutes,Peer-to-peer App Sharing Count,Peer-to-peer File Transfer Count,Organized Conference IM Count,Organized Conference Audio/Video Count,Organized Conference Audio/Video Minutes,Organized Conference App Sharing Count,Organized Conference Web Count,Organized Conference Dial-in/out 3rd Party Count,Organized Conference Dial-in/out Microsoft Count,Organized Conference Dial-in Microsoft Minutes,Organized Conference Dial-out Microsoft Minutes,Paricipated Conference IM Count,Participated Conference Audio/Video Count,Participated Conference Audio/Video Minutes,Participated Conference App Sharing Count,Participated Conference Web Count,Participated Conference Dial-in/out 3rd Party Count,Assigned Products,Report Period
```

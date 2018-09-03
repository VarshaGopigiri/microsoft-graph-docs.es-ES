# <a name="reportroot-getoffice365groupsactivitydetail"></a><span data-ttu-id="3444a-101">reportRoot: getOffice365GroupsActivityDetail</span><span class="sxs-lookup"><span data-stu-id="3444a-101">reportRoot: getOffice365GroupsActivityDetail</span></span>

<span data-ttu-id="3444a-102">Obtiene información sobre la actividad de Grupos de Office 365 por grupo.</span><span class="sxs-lookup"><span data-stu-id="3444a-102">Get details about Office 365 Groups activity by group.</span></span>

> <span data-ttu-id="3444a-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Grupos de Office 365](https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40).</span><span class="sxs-lookup"><span data-stu-id="3444a-103">**Note:** For details about different report views and names, see [Office 365 Reports - Office 365 groups](https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40).</span></span>

## <a name="permissions"></a><span data-ttu-id="3444a-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="3444a-104">Permissions</span></span>

<span data-ttu-id="3444a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3444a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="3444a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3444a-107">Permission type</span></span>                        | <span data-ttu-id="3444a-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3444a-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="3444a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3444a-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="3444a-110">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="3444a-110">Reports.Read.All</span></span>                         |
| <span data-ttu-id="3444a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3444a-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3444a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3444a-112">Not supported.</span></span>                           |
| <span data-ttu-id="3444a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3444a-113">Application</span></span>                            | <span data-ttu-id="3444a-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="3444a-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="3444a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3444a-115">HTTP request</span></span>

<!-- { "blockType": "samples" } --> 

```http
GET /reports/getOffice365GroupsActivityDetail(period='{period_value}')
GET /reports/getOffice365GroupsActivityDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="3444a-116">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="3444a-116">Function parameters</span></span>

<span data-ttu-id="3444a-117">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="3444a-117">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="3444a-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3444a-118">Parameter</span></span> | <span data-ttu-id="3444a-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="3444a-119">Type</span></span>   | <span data-ttu-id="3444a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="3444a-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="3444a-121">period</span><span class="sxs-lookup"><span data-stu-id="3444a-121">period</span></span>    | <span data-ttu-id="3444a-122">cadena</span><span class="sxs-lookup"><span data-stu-id="3444a-122">string</span></span> | <span data-ttu-id="3444a-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="3444a-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="3444a-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="3444a-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="3444a-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="3444a-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="3444a-126">date</span><span class="sxs-lookup"><span data-stu-id="3444a-126">date</span></span>      | <span data-ttu-id="3444a-127">Fecha</span><span class="sxs-lookup"><span data-stu-id="3444a-127">Date</span></span>   | <span data-ttu-id="3444a-128">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="3444a-128">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="3444a-129">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="3444a-129">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="3444a-130">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="3444a-130">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="3444a-131">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="3444a-131">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="3444a-132">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3444a-132">Request headers</span></span>

| <span data-ttu-id="3444a-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="3444a-133">Name</span></span>          | <span data-ttu-id="3444a-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="3444a-134">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="3444a-135">Autorización</span><span class="sxs-lookup"><span data-stu-id="3444a-135">Authorization</span></span> | <span data-ttu-id="3444a-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3444a-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="3444a-138">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="3444a-138">If-None-Match</span></span> | <span data-ttu-id="3444a-139">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="3444a-139">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="3444a-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3444a-140">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="3444a-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3444a-141">Response</span></span>

<span data-ttu-id="3444a-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="3444a-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="3444a-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3444a-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="3444a-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="3444a-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="3444a-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="3444a-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="3444a-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="3444a-146">Report Refresh Date</span></span>
- <span data-ttu-id="3444a-147">Nombre para mostrar del grupo</span><span class="sxs-lookup"><span data-stu-id="3444a-147">Group Display Name</span></span>
- <span data-ttu-id="3444a-148">Eliminado</span><span class="sxs-lookup"><span data-stu-id="3444a-148">Is Deleted</span></span>
- <span data-ttu-id="3444a-149">Nombre principal de propietario</span><span class="sxs-lookup"><span data-stu-id="3444a-149">Owner Principal Name</span></span>
- <span data-ttu-id="3444a-150">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="3444a-150">Last Activity Date</span></span>
- <span data-ttu-id="3444a-151">Tipo de grupo</span><span class="sxs-lookup"><span data-stu-id="3444a-151">Group Type</span></span>
- <span data-ttu-id="3444a-152">Número de miembros</span><span class="sxs-lookup"><span data-stu-id="3444a-152">Member Count</span></span>
- <span data-ttu-id="3444a-153">Número de miembros externos</span><span class="sxs-lookup"><span data-stu-id="3444a-153">External Member Count</span></span>
- <span data-ttu-id="3444a-154">Número de correos electrónicos recibidos de Exchange</span><span class="sxs-lookup"><span data-stu-id="3444a-154">Exchange Received Email Count</span></span>
- <span data-ttu-id="3444a-155">Número de archivos activos de SharePoint</span><span class="sxs-lookup"><span data-stu-id="3444a-155">SharePoint Active File Count</span></span>
- <span data-ttu-id="3444a-156">Número de mensajes publicados en Yammer</span><span class="sxs-lookup"><span data-stu-id="3444a-156">Yammer Posted Message Count</span></span>
- <span data-ttu-id="3444a-157">Número de mensajes leídos en Yammer</span><span class="sxs-lookup"><span data-stu-id="3444a-157">Yammer Read Message Count</span></span>
- <span data-ttu-id="3444a-158">Número de mensajes etiquetados como “Me gusta” en Yammer</span><span class="sxs-lookup"><span data-stu-id="3444a-158">Yammer Liked Message Count</span></span>
- <span data-ttu-id="3444a-159">Número total de elementos de buzones de Exchange</span><span class="sxs-lookup"><span data-stu-id="3444a-159">Exchange Mailbox Total Item Count</span></span>
- <span data-ttu-id="3444a-160">Almacenamiento usado de buzones de Exchange (bytes)</span><span class="sxs-lookup"><span data-stu-id="3444a-160">Exchange Mailbox Storage Used (Byte)</span></span>
- <span data-ttu-id="3444a-161">Número total de archivos de SharePoint</span><span class="sxs-lookup"><span data-stu-id="3444a-161">SharePoint Total File Count</span></span>
- <span data-ttu-id="3444a-162">Almacenamiento usado de sitios de SharePoint (bytes)</span><span class="sxs-lookup"><span data-stu-id="3444a-162">SharePoint Site Storage Used (Byte)</span></span>
- <span data-ttu-id="3444a-163">Período del informe</span><span class="sxs-lookup"><span data-stu-id="3444a-163">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="3444a-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3444a-164">Example</span></span>

#### <a name="request"></a><span data-ttu-id="3444a-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3444a-165">Request</span></span>

<span data-ttu-id="3444a-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3444a-166">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getoffice365groupsactivityuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365GroupsActivityDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="3444a-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3444a-167">Response</span></span>

<span data-ttu-id="3444a-168">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3444a-168">The following is an example of the response.</span></span>

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

<span data-ttu-id="3444a-169">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="3444a-169">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Group Display Name,Is Deleted,Owner Principal Name,Last Activity Date,Group Type,Member Count,Guest Count,Exchange Received Email Count,SharePoint Active File Count,Yammer Posted Message Count,Yammer Read Message Count,Yammer Liked Message Count,Exchange Mailbox Total Item Count,Exchange Mailbox Storage Used (Byte),SharePoint Total File Count,SharePoint Site Storage Used (Byte),Report Period
```

# <a name="reportroot-getemailappusageuserdetail"></a><span data-ttu-id="55caf-101">reportRoot: getEmailAppUsageUserDetail</span><span class="sxs-lookup"><span data-stu-id="55caf-101">reportRoot: getEmailAppUsageUserDetail</span></span>

<span data-ttu-id="55caf-102">Obtiene información sobre las actividades que realizaron los usuarios en las diferentes aplicaciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="55caf-102">Get details about which activities users performed on the various email apps.</span></span>

> <span data-ttu-id="55caf-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de aplicaciones de correo electrónico](https://support.office.com/client/Email-apps-usage-c2ce12a2-934f-4dd4-ba65-49b02be4703d).</span><span class="sxs-lookup"><span data-stu-id="55caf-103">**Note:** For details about different report views and names, see [Office 365 Reports - Email apps usage](https://support.office.com/client/Email-apps-usage-c2ce12a2-934f-4dd4-ba65-49b02be4703d).</span></span>

## <a name="permissions"></a><span data-ttu-id="55caf-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="55caf-104">Permissions</span></span>

<span data-ttu-id="55caf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="55caf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="55caf-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="55caf-107">Permission type</span></span>                        | <span data-ttu-id="55caf-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="55caf-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="55caf-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="55caf-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="55caf-110">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="55caf-110">Reports.Read.All</span></span>                         |
| <span data-ttu-id="55caf-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="55caf-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="55caf-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="55caf-112">Not supported.</span></span>                           |
| <span data-ttu-id="55caf-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="55caf-113">Application</span></span>                            | <span data-ttu-id="55caf-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="55caf-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="55caf-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="55caf-115">HTTP request</span></span>

<!-- { "blockType": "samples" } --> 

```http
GET /reports/getEmailAppUsageUserDetail(period='{period_value}')
GET /reports/getEmailAppUsageUserDetail(date={date_value})
```

## <a name="request-parameters"></a><span data-ttu-id="55caf-116">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="55caf-116">Request parameters</span></span>

<span data-ttu-id="55caf-117">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="55caf-117">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="55caf-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="55caf-118">Parameter</span></span> | <span data-ttu-id="55caf-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="55caf-119">Type</span></span>   | <span data-ttu-id="55caf-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="55caf-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="55caf-121">period</span><span class="sxs-lookup"><span data-stu-id="55caf-121">period</span></span>    | <span data-ttu-id="55caf-122">cadena</span><span class="sxs-lookup"><span data-stu-id="55caf-122">string</span></span> | <span data-ttu-id="55caf-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="55caf-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="55caf-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="55caf-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="55caf-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="55caf-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="55caf-126">date</span><span class="sxs-lookup"><span data-stu-id="55caf-126">date</span></span>      | <span data-ttu-id="55caf-127">Fecha</span><span class="sxs-lookup"><span data-stu-id="55caf-127">Date</span></span>   | <span data-ttu-id="55caf-128">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="55caf-128">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="55caf-129">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="55caf-129">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="55caf-130">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="55caf-130">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="55caf-131">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="55caf-131">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="55caf-132">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="55caf-132">Request headers</span></span>

| <span data-ttu-id="55caf-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="55caf-133">Name</span></span>          | <span data-ttu-id="55caf-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="55caf-134">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="55caf-135">Authorization</span><span class="sxs-lookup"><span data-stu-id="55caf-135">Authorization</span></span> | <span data-ttu-id="55caf-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="55caf-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="55caf-138">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="55caf-138">If-None-Match</span></span> | <span data-ttu-id="55caf-139">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="55caf-139">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="55caf-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="55caf-140">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="55caf-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55caf-141">Response</span></span>

<span data-ttu-id="55caf-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="55caf-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="55caf-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55caf-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="55caf-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="55caf-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="55caf-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="55caf-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="55caf-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="55caf-146">Report Refresh Date</span></span>
- <span data-ttu-id="55caf-147">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="55caf-147">User Principal Name</span></span>
- <span data-ttu-id="55caf-148">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="55caf-148">Display Name</span></span>
- <span data-ttu-id="55caf-149">Eliminado</span><span class="sxs-lookup"><span data-stu-id="55caf-149">Is Deleted</span></span>
- <span data-ttu-id="55caf-150">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="55caf-150">Deleted Date</span></span>
- <span data-ttu-id="55caf-151">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="55caf-151">Last Activity Date</span></span>
- <span data-ttu-id="55caf-152">Mail para Mac</span><span class="sxs-lookup"><span data-stu-id="55caf-152">Mail For Mac</span></span>
- <span data-ttu-id="55caf-153">Outlook para Mac</span><span class="sxs-lookup"><span data-stu-id="55caf-153">Outlook For Mac</span></span>
- <span data-ttu-id="55caf-154">Outlook para Windows</span><span class="sxs-lookup"><span data-stu-id="55caf-154">Outlook For Windows</span></span>
- <span data-ttu-id="55caf-155">Outlook para móviles</span><span class="sxs-lookup"><span data-stu-id="55caf-155">Outlook For Mobile</span></span>
- <span data-ttu-id="55caf-156">Otros para móviles</span><span class="sxs-lookup"><span data-stu-id="55caf-156">Other For Mobile</span></span>
- <span data-ttu-id="55caf-157">Outlook para web</span><span class="sxs-lookup"><span data-stu-id="55caf-157">Outlook For Web</span></span>
- <span data-ttu-id="55caf-158">Aplicación POP3</span><span class="sxs-lookup"><span data-stu-id="55caf-158">POP3 App</span></span>
- <span data-ttu-id="55caf-159">Aplicación IMAP4</span><span class="sxs-lookup"><span data-stu-id="55caf-159">IMAP4 App</span></span>
- <span data-ttu-id="55caf-160">Aplicación SMTP</span><span class="sxs-lookup"><span data-stu-id="55caf-160">SMTP App</span></span>
- <span data-ttu-id="55caf-161">Período del informe</span><span class="sxs-lookup"><span data-stu-id="55caf-161">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="55caf-162">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="55caf-162">Example</span></span>

#### <a name="request"></a><span data-ttu-id="55caf-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="55caf-163">Request</span></span>

<span data-ttu-id="55caf-164">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="55caf-164">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getemailappusageuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getEmailAppUsageUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="55caf-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55caf-165">Response</span></span>

<span data-ttu-id="55caf-166">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55caf-166">The following is an example of the response.</span></span>

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

<span data-ttu-id="55caf-167">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="55caf-167">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,Is Deleted,Deleted Date,Last Activity Date,Mail For Mac,Outlook For Mac,Outlook For Windows,Outlook For Mobile,Other For Mobile,Outlook For Web,POP3 App,IMAP4 App,SMTP App,Report Period
```

# <a name="reportroot-getemailappusageappsusercounts"></a><span data-ttu-id="956f0-101">reportRoot: getEmailAppUsageAppsUserCounts</span><span class="sxs-lookup"><span data-stu-id="956f0-101">reportRoot: getEmailAppUsageAppsUserCounts</span></span>

<span data-ttu-id="956f0-102">Obtiene el número de usuarios únicos por aplicación de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="956f0-102">Get the count of unique users per email app.</span></span>

> <span data-ttu-id="956f0-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de aplicaciones de correo electrónico](https://support.office.com/client/Email-apps-usage-c2ce12a2-934f-4dd4-ba65-49b02be4703d).</span><span class="sxs-lookup"><span data-stu-id="956f0-103">**Note:** For details about different report views and names, see [Office 365 Reports - Email apps usage](https://support.office.com/client/Email-apps-usage-c2ce12a2-934f-4dd4-ba65-49b02be4703d).</span></span>

## <a name="permissions"></a><span data-ttu-id="956f0-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="956f0-104">Permissions</span></span>

<span data-ttu-id="956f0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="956f0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="956f0-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="956f0-107">Permission type</span></span>                        | <span data-ttu-id="956f0-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="956f0-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="956f0-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="956f0-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="956f0-110">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="956f0-110">Reports.Read.All</span></span>                         |
| <span data-ttu-id="956f0-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="956f0-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="956f0-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="956f0-112">Not supported.</span></span>                           |
| <span data-ttu-id="956f0-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="956f0-113">Application</span></span>                            | <span data-ttu-id="956f0-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="956f0-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="956f0-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="956f0-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getEmailAppUsageAppsUserCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="956f0-116">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="956f0-116">Request parameters</span></span>

<span data-ttu-id="956f0-117">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="956f0-117">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="956f0-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="956f0-118">Parameter</span></span> | <span data-ttu-id="956f0-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="956f0-119">Type</span></span>   | <span data-ttu-id="956f0-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="956f0-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="956f0-121">period</span><span class="sxs-lookup"><span data-stu-id="956f0-121">period</span></span>    | <span data-ttu-id="956f0-122">cadena</span><span class="sxs-lookup"><span data-stu-id="956f0-122">string</span></span> | <span data-ttu-id="956f0-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="956f0-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="956f0-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="956f0-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="956f0-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="956f0-125">These values follow the format D   where    represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="956f0-126">Necesario.</span><span class="sxs-lookup"><span data-stu-id="956f0-126">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="956f0-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="956f0-127">Request headers</span></span>

| <span data-ttu-id="956f0-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="956f0-128">Name</span></span>          | <span data-ttu-id="956f0-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="956f0-129">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="956f0-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="956f0-130">Authorization</span></span> | <span data-ttu-id="956f0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="956f0-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="956f0-133">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="956f0-133">If-None-Match</span></span> | <span data-ttu-id="956f0-134">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="956f0-134">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="956f0-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="956f0-135">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="956f0-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="956f0-136">Response</span></span>

<span data-ttu-id="956f0-137">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="956f0-137">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="956f0-138">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="956f0-138">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="956f0-139">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="956f0-139">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="956f0-140">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="956f0-140">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="956f0-141">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="956f0-141">Report Refresh Date</span></span>
- <span data-ttu-id="956f0-142">Mail para Mac</span><span class="sxs-lookup"><span data-stu-id="956f0-142">Mail For Mac</span></span>
- <span data-ttu-id="956f0-143">Outlook para Mac</span><span class="sxs-lookup"><span data-stu-id="956f0-143">Outlook For Mac</span></span>
- <span data-ttu-id="956f0-144">Outlook para Windows</span><span class="sxs-lookup"><span data-stu-id="956f0-144">Outlook For Windows</span></span>
- <span data-ttu-id="956f0-145">Outlook para móviles</span><span class="sxs-lookup"><span data-stu-id="956f0-145">Outlook For Mobile</span></span>
- <span data-ttu-id="956f0-146">Otros para móviles</span><span class="sxs-lookup"><span data-stu-id="956f0-146">Other For Mobile</span></span>
- <span data-ttu-id="956f0-147">Outlook para web</span><span class="sxs-lookup"><span data-stu-id="956f0-147">Outlook For Web</span></span>
- <span data-ttu-id="956f0-148">Aplicación POP3</span><span class="sxs-lookup"><span data-stu-id="956f0-148">POP3 App</span></span>
- <span data-ttu-id="956f0-149">Aplicación IMAP4</span><span class="sxs-lookup"><span data-stu-id="956f0-149">IMAP4 App</span></span>
- <span data-ttu-id="956f0-150">Aplicación SMTP</span><span class="sxs-lookup"><span data-stu-id="956f0-150">SMTP App</span></span>
- <span data-ttu-id="956f0-151">Período del informe</span><span class="sxs-lookup"><span data-stu-id="956f0-151">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="956f0-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="956f0-152">Example</span></span>

#### <a name="request"></a><span data-ttu-id="956f0-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="956f0-153">Request</span></span>

<span data-ttu-id="956f0-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="956f0-154">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getemailappusageappsusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getEmailAppUsageAppsUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="956f0-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="956f0-155">Response</span></span>

<span data-ttu-id="956f0-156">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="956f0-156">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="956f0-157">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="956f0-157">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Mail For Mac,Outlook For Mac,Outlook For Windows,Outlook For Mobile,Other For Mobile,Outlook For Web,POP3 App,IMAP4 App,SMTP App,Report Period
```

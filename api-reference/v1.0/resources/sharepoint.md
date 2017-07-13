<span data-ttu-id="1493a-p102">La API de SharePoint de Microsoft Graph tiene algunas diferencias clave con las API de CSOM. El recurso del [sitio][] se asigna a `SPWeb`. El [sitio][] raíz (`SPWeb`) en un sitio de la colección tiene una faceta de [colecciónDeSitios](sitecollection.md), que contiene información acerca de `SPSite`. Debido a que los identificadores para los sitios solo son únicos dentro de su colección de sitios, el direccionamiento a un sitio a través del id. requiere proporcionar el identificador de la colección de sitios y el identificador del sitio.</span><span class="sxs-lookup"><span data-stu-id="1493a-p102">The Microsoft Graph SharePoint API has a few key differences with the CSOM APIs. The [site][] resource maps to `SPWeb`. The root [site][] (`SPWeb`) in a site collection has a [siteCollection](sitecollection.md) facet, which contains information about the `SPSite`. Because IDs for sites are only unique within their site collection, addressing a site by ID requires providing both the site collection identifier and the site identifier.</span></span>

La API de SharePoint de Microsoft Graph tiene algunas diferencias clave con las API de CSOM. El recurso del [sitio][] se asigna a `SPWeb`. El [sitio][] raíz (`SPWeb`) en un sitio de la colección tiene una faceta de [colecciónDeSitios](sitecollection.md), que contiene información acerca de `SPSite`. Debido a que los identificadores para los sitios solo son únicos dentro de su colección de sitios, el direccionamiento a un sitio a través del id. requiere proporcionar el identificador de la colección de sitios y el identificador del sitio.

```http
GET https://graph.microsoft.com/v1.0/sites/{hostname},{spsite-id},{spweb-id}/
```
<span data-ttu-id="1493a-136">Una dirección URL creada solo con el nombre de host apuntará al sitio raíz (`SPWeb`) en la colección de sitios predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1493a-136">A URL constructed with only the hostname will point to the root site (`SPWeb`) in the default site collection.</span></span>

```http
GET https://graph.microsoft.com/v1.0/sites/{hostname}
```

<span data-ttu-id="1493a-137">Una dirección URL creada solo con el nombre de host y el id. de siteCollection (`SPSite`) apuntará al sitio raíz (`SPWeb`) en la colección de sitios predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1493a-137">A URL constructed with only the hostname and siteCollection (`SPSite`) ID will point to the root site (`SPWeb`) in the given site collection.</span></span>

```http
GET https://graph.microsoft.com/v1.0/sites/{hostname},{spsite-id}
```

<span data-ttu-id="1493a-138">[sitio]: site.md</span><span class="sxs-lookup"><span data-stu-id="1493a-138">[Site]: site.md</span></span>
[drive]: drive.md
[siteCollection]: siteCollection.md

<!-- {
  "type": "#page.annotation",
  "description": "Getting started programming with the SharePoint API",
  "keywords": "getting started sharepoint rest api programming C# ios android rest http",
  "section": "documentation",
  "tocPath": "Getting Started",
  "tocIndex": -100
} -->

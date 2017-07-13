<span data-ttu-id="a353c-p117">Los criterios de búsqueda se expresan mediante la Sintaxis de consulta avanzada (AQS). Los resultados se ordenan por la fecha y la hora en que se ha enviado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="a353c-p117">Search criteria are expressed using Advanced Query Syntax (AQS). The results are sorted by the date and time that the message was sent.</span></span>

Los criterios de búsqueda se expresan mediante la Sintaxis de consulta avanzada (AQS). Los resultados se ordenan por la fecha y la hora en que se ha enviado el mensaje.

<span data-ttu-id="a353c-194">Puede especificar las siguientes propiedades en `message` en un criterio `$search`: `attachments`, `bccRecipients`, `body`, `category`, `ccRecipients`, `content`, `from`, `hasAttachments`, `participants`, `receivedDateTime`, `sender`, `subject`, `toRecipients`</span><span class="sxs-lookup"><span data-stu-id="a353c-194">You can specify the following properties on a `message` in a `$search` criterion: `attachments`, `bccRecipients`, `body`, `category`, `ccRecipients`, `content`, `from`, `hasAttachments`, `participants`, `receivedDateTime`, `sender`, `subject`, `toRecipients`</span></span>

<span data-ttu-id="a353c-195">Si realiza una búsqueda en mensajes y especifica un solo valor, la búsqueda se realiza con las propiedades de búsqueda predeterminadas de `from`, `subject` y `body`.</span><span class="sxs-lookup"><span data-stu-id="a353c-195">If you do a search on messages and specify only a value, the search is carried out on the default search properties of `from`, `subject` and `body`.</span></span>

<span data-ttu-id="a353c-196">En el ejemplo siguiente, se devuelven todos los mensajes del buzón del usuario que ha iniciado sesión que contienen la palabra "pizza" en cualquiera de las tres propiedades de búsqueda predeterminadas:</span><span class="sxs-lookup"><span data-stu-id="a353c-196">The following example returns all messages in the signed-in user's Inbox that contains "pizza" in any of the three default search properties:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$search="pizza"
```

<span data-ttu-id="a353c-197">En el ejemplo siguiente se buscan todos los mensajes en el buzón del usuario que se enviaron desde una dirección de correo específica:</span><span class="sxs-lookup"><span data-stu-id="a353c-197">The next example searches all messages in the user's Inbox that were sent from a specific email address:</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/messages?$search="from:help@contoso.com"
```

[graph-explorer]: https://graph.microsoft.io/en-us/graph-explorer
[odata-filter]: http://docs.oasis-open.org/odata/odata/v4.0/errata03/os/complete/part2-url-conventions/odata-v4.0-errata03-os-part2-url-conventions-complete.html#_Toc453752358
[odata-query]: http://docs.oasis-open.org/odata/odata/v4.0/errata03/os/complete/part2-url-conventions/odata-v4.0-errata03-os-part2-url-conventions-complete.html#_Toc453752356

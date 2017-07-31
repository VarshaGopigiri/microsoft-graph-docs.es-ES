<span data-ttu-id="95bfc-p119">Ahora que ha visto cómo realizar llamadas a Microsoft Graph, puede usar la referencia de la API para construir cualquier otro tipo de llamada que su aplicación necesite realizar. Sin embargo, tenga en cuenta que su aplicación debe tener los permisos adecuados configurados en el registro de aplicaciones para las llamadas que realice.</span><span class="sxs-lookup"><span data-stu-id="95bfc-p119">Now that you've seen how to make calls to Microsoft Graph, you can use the API reference to construct any other kinds of calls your app needs to make. However, bear in mind that your app needs to have the appropriate permissions configured on the app registration for the calls it makes.</span></span>

```
GET https://graph.microsoft.com/v1.0/me/messages?$select=subject,from,receivedDateTime&$top=25&$orderby=receivedDateTime%20DESC
Accept: application/json
Authorization: Bearer eyJ0eXAi...b66LoPVA
```

Ahora que ha visto cómo realizar llamadas a Microsoft Graph, puede usar la referencia de la API para construir cualquier otro tipo de llamada que su aplicación necesite realizar. Sin embargo, tenga en cuenta que su aplicación debe tener los permisos adecuados configurados en el registro de aplicaciones para las llamadas que realice.

## <a name="next-steps"></a><span data-ttu-id="95bfc-189">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="95bfc-189">Next steps</span></span>
- <span data-ttu-id="95bfc-190">Pruebe más características de la API de REST mediante el [Probador de Graph](https://graph.microsoft.io/graph-explorer).</span><span class="sxs-lookup"><span data-stu-id="95bfc-190">Try out more of the REST API using the [Graph explorer](https://graph.microsoft.io/graph-explorer).</span></span>

## <a name="see-also"></a><span data-ttu-id="95bfc-191">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="95bfc-191">See also</span></span>
- [<span data-ttu-id="95bfc-192">Protocolos de Azure AD v2.0</span><span class="sxs-lookup"><span data-stu-id="95bfc-192">Azure AD v2.0 protocols</span></span>](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-protocols/)
- [<span data-ttu-id="95bfc-193">Tokens de Azure AD v2.0</span><span class="sxs-lookup"><span data-stu-id="95bfc-193">Azure AD v2.0 tokens</span></span>](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-tokens/)

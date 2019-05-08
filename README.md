# IDP integration with REST-API

This sample shows how to enable IDP integration in REST-API.

See demo: `modules/web/web/VAADIN/demo/idp-login-demo.html`

Demo URL: http://localhost:8080/app/VAADIN/demo/idp-login-demo.html

## Authentication flow:

1. Users click on login link `/app/rest/v2/idp/login`
2. SP controller sends redirect to IDP form
3. After authentication IDP sends IDP ticket back to web page using parameter in URL
4. Web page extracts IDP ticket from URL and sends it to REST authentication controller: `/app/rest/v2/idp/token`
5. REST responds with actual REST-API token

Finally, web page can use REST-API token for data access.
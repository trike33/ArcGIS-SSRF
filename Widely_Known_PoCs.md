## Portal Sharing endpoints

Please note these endpoints, unfortunately are undocumented.

The `<portal>` part of the endpoints would typically be `arcgis` or similar, yet it is fully customizable for each organization. (Quick tip, you can typically discover it because when accessing the webroot, `/`, the server will redirect you to either `/<portal>/home` or `/<portal>/sharing/oauth/login` or similar).
Under `/<portal>/sharing/portals/self` you can find services URLs for the application, this endpoint is typically public.

Some websites might filter out the HTML format but allow other output formats, fortunately, Arcgis offers a `?f=` parameter(on almost all endpoints) which allows you to specify the output format, try to tamper it with for example `pjson` format.

All these endpoints suffer from the same parameter named `url`(except for the `proxy` which it does not take the `url` parameter).

`/<portal>/sharing/rss`

`/<portal>/sharing/kml`

`/<portal>/sharing/proxy`

`/<portal>/sharing/checkUrl.jsp`

`/<portal>/sharing/tools/legend`

`/<portal>/sharing/tools/print/newPrint/execute`

## Services directory

Once you have a couple of rest services routes, try to enum them, based on what you have review the docs from the application("API Reference"). The most common services available for unauthenticated users are `MapServer` or `FeatureServer`.

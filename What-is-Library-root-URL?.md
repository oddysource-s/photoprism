**Library root URL** is the address of your PhotoPrism server (API), including the `http`/`https` scheme. 
On the following example, it is highlighted in yellow:

<img src="https://user-images.githubusercontent.com/5675681/230467450-2a82dfcd-e83b-409a-adfd-050723c2ccf1.png" width=500 alt="Example"/>

If your instance is served at a non-root path, like `https://myserver.io/photoprism/`, then include the path as well.

## Examples of valid URLs:
- `http://10.0.0.125:2342`
- `http://photoprism.local`
- `https://myserver.io/photoprism`
- `https://prism.myserver.io`
- `https://username:password@myserver.io/photoprism` – if your server requires HTTP basic auth

## Examples of invalid URLs:
- `10.0.0.125:2342` – missing the scheme, must be `http://10.0.0.125:2342`
- `https://admin@prism.local/originals/` – WebDAV URL, must be `https://prism.local`
- `https://prism.myserver.io/library/browse` – Web app "Search" page, must be `https://prism.myserver.io`
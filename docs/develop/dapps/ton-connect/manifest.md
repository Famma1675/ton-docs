<script src="https://unpkg.com/@tonconnect/ui@latest/dist/tonconnect-ui.min.js"></script>![Screenshot_20240825-222016](https://github.com/user-attachments/assets/f8f101a8-abd4-4079-a289-35ab2425ef41)
![Screenshot_20240825-222016](https://github.com/user-attachments/assets/fb2c1a4a-71a1-4e9e-9631-5c941d0314e7)
![Screenshot_20240825-225854](https://github.com/user-attachments/assets/7d58fcab-262f-42e8-a44d-3bb4a21b554f)

# Creating manifest.json

Every app needs to have its manifest to pass meta information to the wallet. Manifest is a JSON file named as `tonconnect-manifest.json` following format:

```json
{
    "url": "<app-url>",                        // required
    "name": "<app-name>",                      // required
    "iconUrl": "<app-icon-url>",               // required
    "termsOfUseUrl": "<terms-of-use-url>",     // optional
    "privacyPolicyUrl": "<privacy-policy-url>" // optional
}
```

## Example

You can find an example of the manifest below:

```json
{
    "url": "https://ton.vote",
    "name": "TON Vote",
    "iconUrl": "https://ton.vote/logo.png"
}
```
## Best practices

- Best practice is to place the manifest in the root of your app and repository, e.g. `https://myapp.com/tonconnect-manifest.json`. It allows the wallet to handle your app better and improve the UX connected to your app.
- Make sure that `manifest.json` file is available to GET by its URL.

## Fields description
|Field|Requirement|Description|
|---|---|---|
|`url` |required| app URL. Will be used as the DAppidentifier. Will be used to open the DAppafter click to its icon in the wallet. It is recommended to pass url without closing slash, e.g. 'https://mydapp.com' instead of 'https://mydapp.com/'.|
| `name`|required| app name. Might be simple, will not be used as identifier.|
| `iconUrl`| required | Url to the app icon. Must be PNG, ICO, ... format. SVG icons are not supported. Perfectly pass url to a 180x180px PNG icon.|
| `termsOfUseUrl` |optional| url to the Terms Of Use document. Optional for usual apps, but required for the apps which is placed in the Tonkeeper recommended apps list.|
| `privacyPolicyUrl` | optional | url to the Privacy Policy document. Optional for usual apps, but required for the apps which is placed in the Tonkeeper recommended apps list.|

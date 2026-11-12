# Website page map

The frontend has **3 standalone HTML pages**. Collection browsing, chat, tracking
and the assistant cart are interactions on the home page, not separate pages.
The backend API is not a browser page, and its generated API documentation is
disabled.

| Page | Purpose | Links to |
|---|---|---|
| [`frontend/index.html`](./frontend/index.html) (`/` or `/index.html`) | Shopping assistant, product results and assistant cart | Kiaasa’s external home page (`https://kiaasa.com/`); the store finder (`stores.html`) from both “Our Stores” and “Find a Store”; the privacy notice (`privacy.html`, opens in a new tab). Product cards link to the catalogue-provided product page in a new tab. Cart checkout continues to the corresponding Kiaasa product page; it does not submit to the website cart. A valid Shiprocket tracking card can link to live tracking in a new tab. |
| [`frontend/stores.html`](./frontend/stores.html) (`/stores.html`) | Search, sort and view Kiaasa store locations | Home page (`index.html`) from the logo, “Back to shopping” and breadcrumb; Google Maps directions for each store; telephone links when a store phone number is available; Kiaasa’s official store directory (`https://stores.kiaasaretail.com/`) in the footer and if store data cannot load. The map attributes OpenStreetMap. |
| [`frontend/privacy.html`](./frontend/privacy.html) (`/privacy.html`) | Assistant privacy and data-use notice | Home page (`index.html`) through “Back to shopping”; Kiaasa customer support (`https://www.kiaasa.in/contact-us`); Kiaasa’s official website (`https://www.kiaasa.in/`). |

## Page-to-page links

```text
Home (/) ── Our Stores / Find a Store ──> Store finder (/stores.html)
Home (/) ── Privacy ────────────────────> Privacy notice (/privacy.html)
Store finder ── logo / Back / Home ─────> Home (/)
Privacy notice ── Back to shopping ─────> Home (/)
```

The home page’s product, cart and tracking destinations are generated from
catalogue or tracking data; they are external destinations rather than extra
frontend pages. The store finder also builds Google Maps directions from the
selected store and, when available, the visitor’s location.

## Counting scope

The count is based on the standalone `.html` files in `frontend/`. It excludes
backend API endpoints, collection filters and other in-page assistant states,
third-party destinations, and the static HTML files used as catalogue data.

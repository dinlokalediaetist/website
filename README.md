# Din lokale diætist

A responsive Danish website for Julie Spanggaard Zielke, an udkørende klinisk diætist near Viborg. Built with plain HTML and CSS for GitHub Pages. No build step, JavaScript, or package installation is required. The site remains under construction and is not indexed by search engines.

- `index.html`: main page with home visits, consultations, services, biography, prices, and contact information.
- `tilskud-og-forsikring.html`: general subsidy and insurance information with a link to Sygeforsikringen “danmark”.
- `handelsbetingelser.html`: preliminary cancellation and travel information; complete business terms are still pending.
- `styles.css`: responsive layout and styling.
- `images/`: two generated food photographs, the user-supplied `diaetist-portraet.png` used in “Om mig”, and a retained, unused SVG map. The active map uses OpenStreetMap tiles. The ingredients photograph is retained as an unused asset.

Open `index.html` in a browser to preview. GitHub Pages can publish this repository directly from the root of `main`.

Before launch, add the remaining business information, finalize trading terms and subsidy reporting details, and review the supplied prices. The name, telephone number and email address are user-supplied. Keep the construction notices and `noindex, nofollow` on all three pages until launch is explicitly requested.

Navigation, telephone links and the map work without JavaScript. The OpenStreetMap tiles require an internet connection and an HTTP(S) preview so browsers send the required Referer header. All internal paths are relative for GitHub Pages subpath support. Review all three pages at desktop and mobile sizes after shared CSS changes.

## Privacy

The home address is private. Do not publish it, label the circle center as a home or clinic, add address pins or coordinate links, or describe identifying details about the home. The map represents a general service area only. Do not send location data to external map services without explicit authorization.

## Map and content sources

- The active map is a static, responsive grid of OpenStreetMap tiles in `index.html`, with an overlaid circle and visible copyright attribution. Only tiles intersecting the displayed viewport are included; native lazy loading and browser caching are used. The user explicitly requested OpenStreetMap for the general service area. No private address, home marker, geolocation or personal data is sent.
- `images/jylland-kort.svg` is retained as an unused earlier map.
- The map shows a roughly 42 km-wide general service area near Viborg using Web Mercator tiles at zoom 11, exposing more small-town labels. The 15 km circle has a diameter of approximately 71.43% of the image width. The distance scale uses the latitude of the original public village center; local projection distortion across the circle is less than 0.3%. No home-address marker is shown.
- The map circle is 15 km, as most recently requested. The travel surcharge starts beyond 15 km at 10 kr. per km beyond that threshold. Keep the travel pricing explicit. The user requested removal of the visible map caption; preserve radius information in the accessible description only.
- Prices and preliminary cancellation wording come from the supplied handwritten reference; consultation duration, package contents, contact name, phone and travel radius include the user's corrections. The first consultation is 75 minutes and follow-ups are 35 minutes.
- Subsidy information links to the [official provider](https://www.sygeforsikring.dk/tilskud-til-diaetist), checked 15 September 2026. No clinic registration, reimbursement handling or guaranteed insurance coverage is claimed.

## Image prompts

`images/frokost.png`

Generated with the built-in image generation tool.

Use case: photorealistic-natural. Asset type: Danish dietitian website hero photograph. Primary request: Photorealistic editorial food photograph of appealing everyday Scandinavian lunch: a white ceramic bowl of pearl barley, peas, radishes, cucumber ribbons and leafy herbs, with rye bread at the edge. Scene/backdrop: Light natural linen and pale wood. Style/medium: Candid premium food magazine photography, tactile real food textures. Composition/framing: Landscape 3:2, close overhead-to-45-degree view, main bowl centered to allow a portrait crop. Lighting/mood: Soft sunny window light; joyful, welcoming everyday eating, no diet-culture styling. Constraints: No text, no people, no logos, no watermark.

`images/raavarer.png`

Use case: photorealistic-natural. Asset type: Danish dietitian website supporting photograph. Primary request: Photorealistic close editorial still life of seasonal fresh carrots with green tops, tomatoes, leafy greens and a halved lemon loosely arranged on pale neutral linen. Scene/backdrop: Scandinavian kitchen daylight, pale neutral linen. Style/medium: Natural premium editorial food photography, tactile real vegetable and linen textures. Composition/framing: Landscape 3:2, close still life, loose natural arrangement. Lighting/mood: Soft natural daylight, fresh and warm. Constraints: No text, no people, no logos, no watermark.

The map supplements the native labels with readable town names in transparent HTML text, without white boxes or an overlaid header. Keep the copyright attribution visible. Smaller-town positions use public geographic coordinates projected into the same Web Mercator viewport; recompute their percentages if the center or extent changes. Sources: [Rødkærsbro](https://mapcarta.com/17574882), [Ans](https://mapcarta.com/17595036), [Kjellerup](https://mapcarta.com/17583306), [Bruunshåb](https://sunrise-sunset.org/dk/bruunshab), [Løgstrup](https://www.geonames.org/search.html?country=DK&q=Danmark&startRow=300).

Additional town-label sources: [Frederiks](https://mapcarta.com/17589572), [Karup](https://geloky.com/geocoding/place/Karup%2BDenmark), [Ravnstrup in Viborg Municipality](https://commons.wikimedia.org/wiki/Category:Ravnstrup_(Viborg_Kommune)), [Rødding near Viborg](https://mapcarta.com/17574920), [Stoholm](https://mapcarta.com/17570736), [Vammen](https://mapcarta.com/17567194). The map spans 42 km to show settlements both inside and outside the 15 km circle. Edge labels use left/right alignment to stay readable on mobile.

Further town-label sources: [Ørum near Viborg](https://mapcarta.com/17576966), [Vinkel near Viborg](https://mapcarta.com/17566032), [Ulstrup](https://mapcarta.com/17567494), [Fårvang](https://mapcarta.com/17590260). The map viewport spans 42 km to include Ulstrup at the eastern edge; the circle remains 15 km in radius. Vinkel and Ulstrup labels have small text offsets for readability.

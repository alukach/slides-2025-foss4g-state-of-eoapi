---
title: FOSS4G - State of eoAPI
info: |
  What's changed in eoAPI in 2025, what's on the horizon for 2026?
class: text-center
highlighter: shiki
drawings:
  persist: false
  enable: false
transition: slide-left
mdc: true
addons:
    - slidev-addon-qrcode

theme: './theme'
layout: title
image: /images/theme/lena-delta.jpg
---


# State of the eoAPI

::subtitle::
What's changed in 2025?

What's coming in 2026?

<DecorativeRectangle
  width="50%"
  height="40%"
  :zIndex="20"
  :position="{
    bottom: '2%',
    right: '0%',
  }"
  :customStyle="{ mixBlendMode: 'multiply', borderTopRightRadius: 0, borderBottomRightRadius: 0 }"
>
  <!-- You can place content _inside_ of rectangles! -->
  <div w-full h-full relative items-end justify-end p-4 text-white text-right>
    <h4>
      ⚡️ Lightning Talk
    </h4>
    <h3 text-5xl>
      FOSS4G
    </h3>
    <h4 text-md font-mono>
      2025-11-19
    </h4>
    <h5 text-sm>
      <code text-primary>@alukach</code>
    </h5>
  </div>
</DecorativeRectangle>
<LogoHorPos position="top-left" height="24px" />

---
layout: iframe-right
url: https://eoapi.dev
---

# eoAPI

**eoAPI** is an open-source toolkit for building scalable Earth Observation applications.

<div class="absolute bottom-4 left-4 flex flex-row items-center gap-2">
  <CurrentUrlQRCode
    url="https://eoapi.dev"
    :dotsOptions="{ type: 'classy-rounded' }"
    :width="100"
    :height="100"
  />
  <code text-xs>eoapi.dev</code>
</div>

<LogoHorNegMono position="bottom-right" />

<!-- Also supports notes that are displayed in the presenter view. Just make sure that the comment is places at the END of the slide (after logo/rectangles) -->
---
layout: iframe-right
url: https://stac-utils.github.io/pgstac/pgstac/
---

# pgstac

> A set of SQL functions and schema to build highly performant databases for Spatio-Temporal Asset Catalogs (STAC).

<v-clicks>

- collection search
- improved data loading with queryables
- maintenance: improved stability via miscellanious fixes
- maintenance: improved scalability via low-level optimizations

</v-clicks>

<div class="absolute bottom-4 left-4 flex flex-row items-center gap-2">
  <CurrentUrlQRCode
    url="https://github.com/stac-utils/pgstac"
    :dotsOptions="{ type: 'classy-rounded' }"
    :width="100"
    :height="100"
  />
  <code text-xs>github.com/stac-utils/pgstac</code>
</div>

---
layout: iframe-right
url: https://developmentseed.org/tipg/
---

# tipg

> Simple and Fast Geospatial OGC Features and Tiles API for PostGIS.

<v-clicks>

- maintenance: improved stability via miscellanious fixes
- looking at expanding backends to duckdb / datafusion / gdal

</v-clicks>

<div class="absolute bottom-4 left-4 flex flex-row items-center gap-2">
  <CurrentUrlQRCode
    url="https://github.com/developmentseed/tipg"
    :dotsOptions="{ type: 'classy-rounded' }"
    :width="100"
    :height="100"
  />
  <code text-xs>github.com/developmentseed/tipg</code>
</div>

---
layout: iframe-right
url: https://stac-utils.github.io/stac-fastapi-pgstac/
---

# stac-fastapi-pgstac

> An HTTP interface built in FastAPI to validate requests, sends data to a PgSTAC backend, and adds links to the returned data

<v-clicks >

- Collection Search extension!
  - free-text search
  - query (stacql)
  - filter (cql)
  - sorting
  - fields
- improved pagination

</v-clicks>

<div class="absolute bottom-4 left-4 flex flex-row items-center gap-2">
  <CurrentUrlQRCode
    url="https://github.com/stac-utils/stac-fastapi-pgstac"
    :dotsOptions="{ type: 'classy-rounded' }"
    :width="100"
    :height="100"
  />
  <code text-xs>github.com/stac-utils/stac-fastapi-pgstac</code>
</div>

---
layout: iframe-right
url: https://developmentseed.org/titiler
---

# titiler

> A modern dynamic tile server built on top of FastAPI and Rasterio/GDAL.

<v-clicks>

- OGC Maps API (`/map`) and `/preview/{width}x{height}.{format}` endpoints
- HTML responses for tilesets, tilematrixsets, algorithms, colormaps, and landing page
- Zarr support in `titiler.xarray` with Obstore
- OpenTelemetry integration

</v-clicks>

<div class="absolute bottom-4 left-4 flex flex-row items-center gap-2">
  <CurrentUrlQRCode
    url="https://github.com/developmentseed/titiler"
    :dotsOptions="{ type: 'classy-rounded' }"
    :width="100"
    :height="100"
  />
  <code text-xs>github.com/developmentseed/titiler</code>
</div>

---
layout: iframe-right
url: https://developmentseed.org/eoapi-cdk
---

# eoapi-cdk

> A package of AWS CDK constructs designed to encapsulate eoAPI services and best practices as simple reusable components.

<v-clicks>

- New constructs:
  - `stac-auth-proxy`
  - `PrivateLambdaApiGateway`
  - `stactools-item-generator` & `stac-item-loader`
- Lambda **SnapStart** option to reduce cold starts

</v-clicks>

<div class="absolute bottom-4 left-4 flex flex-row items-center gap-2">
  <CurrentUrlQRCode
    url="https://github.com/developmentseed/eoapi-cdk"
    :dotsOptions="{ type: 'classy-rounded' }"
    :width="100"
    :height="100"
  />
  <code text-xs>github.com/developmentseed/eoapi-cdk</code>
</div>

---
layout: iframe-right
url: https://developmentseed.org/eoapi-k8s
---

# eoapi-k8s

> Production-ready Kubernetes deployment with flexible database options, unified ingress configuration, and built-in monitoring.

<v-clicks>

- Improved pgSTAC via exposing deep configuration to helm charts
- Optional pgSTAC queue processor and extent updater CronJobs wired into those settings
- STAC Browser integration

</v-clicks>

<div class="absolute bottom-4 left-4 flex flex-row items-center gap-2">
  <CurrentUrlQRCode
    url="https://github.com/developmentseed/eoapi-k8s"
    :dotsOptions="{ type: 'classy-rounded' }"
    :width="100"
    :height="100"
  />
  <code text-xs>github.com/developmentseed/eoapi-k8s</code>
</div>

---
layout: iframe-right
url: https://developmentseed.org/stac-auth-proxy/
---

# stac-auth-proxy

<span text-xs uppercase tracking-wide px-2 py-1 rounded bg-green-500 text-white>New</span>

> An application gateway to impose advanced authorization policies on STAC APIs.

**Key Features:**

- Fine-grained access control for STAC endpoints
- Policy-based authorization
- Transparent proxy for existing STAC APIs

<div class="absolute bottom-4 left-4 flex flex-row items-center gap-2">
  <CurrentUrlQRCode
    url="https://github.com/developmentseed/stac-auth-proxy/"
    :dotsOptions="{ type: 'classy-rounded' }"
    :width="100"
    :height="100"
  />
  <code text-xs>github.com/developmentseed/stac-auth-proxy</code>
</div>

---

# eoapi-notifier

<span text-xs uppercase tracking-wide px-2 py-1 rounded bg-green-500 text-white>New</span>

> Tooling to listen to changes to pgSTAC database and broadcast messages to consumers.

**Key Features:**
- Real-time change detection from pgSTAC
- MQTT message broadcasting
- Event-driven architecture for STAC workflows

<div class="absolute bottom-4 left-4 flex flex-row items-center gap-2">
  <CurrentUrlQRCode
    url="https://github.com/developmentseed/eoapi-notifier/"
    :dotsOptions="{ type: 'classy-rounded' }"
    :width="100"
    :height="100"
  />
  <code text-xs>github.com/developmentseed/eoapi-notifier</code>
</div>

---
layout: image-right
image: /images/stac-manager.png
backgroundSize: contain
---

# stac-manager

<span text-xs uppercase tracking-wide px-2 py-1 rounded bg-green-500 text-white>New</span>
<span text-xs uppercase tracking-wide px-2 py-1 rounded bg-amber-500 text-white>Experimental</span>

> Web application for detail-oriented curation of STAC collections by subject matter experts.

- Uses STAC API Transaction Extension
- Extensible plugin system for STAC extensions
- Modular React packages for customization:
  - `@stac-manager/client`, `data-core`, `data-widgets`, `data-plugins`

<div class="absolute bottom-4 left-4 flex flex-row items-center gap-2">
  <CurrentUrlQRCode
    url="https://github.com/developmentseed/stac-manager/"
    :dotsOptions="{ type: 'classy-rounded' }"
    :width="100"
    :height="100"
  />
  <code text-xs>github.com/developmentseed/stac-manager</code>
</div>

---
layout: iframe-right
url: https://radiantearth.github.io/stac-browser/#/external/stac-geoparquet.labs.eoapi.dev
scale: 0.5
---

# stac-fastapi-geoparquet

<span text-xs uppercase tracking-wide px-2 py-1 rounded bg-green-500 text-white>New</span>
<span text-xs uppercase tracking-wide px-2 py-1 rounded bg-amber-500 text-white>Experimental</span>

Serve a full-featured STAC API from stac-geoparquet files — no database required.

**Key Features:**
- Serves from blob storage (S3, GCS, etc.)
- No database infrastructure needed
- Compatible with stac-geoparquet format

<div class="absolute bottom-4 left-4 flex flex-row items-center gap-2">
  <CurrentUrlQRCode
    url="https://github.com/stac-utils/stac-fastapi-geoparquet"
    :dotsOptions="{ type: 'classy-rounded' }"
    :width="100"
    :height="100"
  />
  <code text-xs>github.com/stac-utils/stac-fastapi-geoparquet</code>
</div>

---
layout: iframe-right
url: https://developmentseed.org/stac-map/?href=https://raw.githubusercontent.com/developmentseed/labs-375-stac-geoparquet-backend/refs/heads/main/data/naip.parquet
scale: 0.5
---

# stac-map

<span text-xs uppercase tracking-wide px-2 py-1 rounded bg-green-500 text-white>New</span>
<span text-xs uppercase tracking-wide px-2 py-1 rounded bg-amber-500 text-white>Experimental</span>

Interactive map viewer for STAC data.

**Features:**
- Visualize STAC items on a map
- Support for geoparquet sources
- Lightweight exploration interface

<div class="absolute bottom-4 left-4 flex flex-row items-center gap-2">
  <CurrentUrlQRCode
    url="https://github.com/developmentseed/stac-map/"
    :dotsOptions="{ type: 'classy-rounded' }"
    :width="100"
    :height="100"
  />
  <code text-xs>github.com/developmentseed/stac-map</code>
</div>

---
layout: image-right
image: /images/theme/Tanezrouft_Basin.jpg
---

# We would ❤️ to hear from you!


<div class="flex flex-col items-center gap-2 mt-2">
 <CurrentUrlQRCode
    url="https://github.com/developmentseed/eoAPI/discussions/209"
    :dotsOptions="{ type: 'classy-rounded' }"
    :width="200"
    :height="200"
  />
  <code text-xs>github.com/developmentseed/eoAPI/discussions/209</code>
</div>


---
layout: title
# Landsat 9 image of Apostle Islands, Lake Superior
# https://unsplash.com/photos/j7HqdQqn7Jo
image: https://images.unsplash.com/photo-1722080767251-aad7fa1796d3
---

# Thank you!

<br mt-4 />

### Authors

<div mt-2 flex flex-wrap items-center gap-2>
  <a href="https://github.com/bitner" target="_blank" title="@bitner">
    <img src="https://github.com/bitner.png" alt="@bitnerd" w-10 h-10 rounded-full />
  </a>
  <a href="https://github.com/gadomski" target="_blank" title="@gadomski">
    <img src="https://github.com/gadomski.png" alt="@gadomski" w-10 h-10 rounded-full />
  </a>
  <a href="https://github.com/alukach" target="_blank" title="@alukach">
    <img src="https://github.com/alukach.png" alt="@alukach" w-10 h-10 rounded-full />
  </a>
  <a href="https://github.com/pantierra" target="_blank" title="@pantierra">
    <img src="https://github.com/pantierra.png" alt="@pantierra" w-10 h-10 rounded-full />
  </a>
  <a href="https://github.com/ividito" target="_blank" title="@ividito">
    <img src="https://github.com/ividito.png" alt="@ividito" w-10 h-10 rounded-full />
  </a>
  <a href="https://github.com/vincentsarago" target="_blank" title="@vincentsarago">
    <img src="https://github.com/vincentsarago.png" alt="@vincentsarago" w-10 h-10 rounded-full />
  </a>
  <a href="https://github.com/danielfdsilva" target="_blank" title="@danielfdsilva">
    <img src="https://github.com/danielfdsilva.png" alt="@danielfdsilva" w-10 h-10 rounded-full />
  </a>
  <a href="https://github.com/hrodmn" target="_blank" title="@hrodmn">
    <img src="https://github.com/hrodmn.png" alt="@hrodmn" w-10 h-10 rounded-full />
  </a>
</div>


<DecorativeRectangle
  width="30%"
  height="96%"
  zIndex=11
  :position="{
    bottom: '2%',
    right: '2%',
  }"
  :customStyle="{ mixBlendMode: 'multiply' }"
>
  <div w-full h-full relative items-start justify-between p-4 text-white text-left class="[&_a]:no-underline [&_a]:text-white [&_a:hover]:text-gray-200">
    <div mb-4 gap-5 items-start justify-start text-sm font-mono class="[&_a]:flex [&_a]:items-center [&_a]:gap-1">
      <Logo src="/images/logos/hor--neg-mono@2x.png" height="24px" alt="DevelopmentSeed" class="!relative !top-0 !left-0" />
      <a href="mailto:anthony@developmentseed.org" title="Email">
        <EmailIcon size="20" pr-1 />
        <span>anthony@developmentseed.org</span>
      </a>
      <a href="https://github.com/alukach" target="_blank" title="GitHub">
        <GitHubIcon size="20" pr-1 />
        <span>@alukach</span>
      </a>
      <a href="https://www.linkedin.com/in/alukach" target="_blank" title="LinkedIn">
        <LinkedInIcon size="20" pr-1 />
        <span>in/alukach</span>
      </a>
      <!-- <a href="https://developmentseed.org/careers" target="_blank" class="font-sans" text-xs text-strong text-italics>
        <span pr-1>🚀</span>
        We're hiring!
      </a> -->
      <CurrentUrlQRCode
        fullWidth
        image='/images/logos/symbol--neg-mono@2x.png'
        :dotsOptions="{ type: 'classy-rounded', color: 'white' }"
      />
    </div>
    <div opacity-70 w-100 class="text-[10px]">
      <div>Attributions:</div>
      <div>
        Slide images from <a href="https://unsplash.com/@usgs?utm_source=ds-slides&utm_medium=referral" target="_blank" class="text-white hover:text-gray-200">USGS</a> on <a href="https://unsplash.com/?utm_source=ds-slides&utm_medium=referral">Unsplash</a>
      </div>
    </div>
  </div>
</DecorativeRectangle>

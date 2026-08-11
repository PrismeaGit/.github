<p align="center"> <img src="assets/logo.png" alt="Prismea" width="96" /> </p> <h1 align="center">Prismea</h1> <p align="center"> <strong>Swiss trading-card retail, built in-house.</strong><br /> Boutique TCG suisse — Pokémon, One Piece, scellé, singles et cartes gradées. </p> <p align="center"> <a href="https://prismea.ch">prismea.ch</a> · <a href="https://discord.gg/k9jXt7UW4C">Discord</a> · <a href="https://www.instagram.com/prismea_">Instagram</a> · <a href="https://www.tiktok.com/@prismea_">TikTok</a> </p>
Who we are
Prismea is a trading-card shop based in Yverdon-les-Bains, Switzerland. We sell sealed product, singles and graded slabs, we buy collections back from customers, and we handle grading submissions on their behalf.

We build and run our own storefront rather than renting one. That is a deliberate choice: the parts of this business that are worth getting right — pricing against live market data, reserving stock honestly during checkout, valuing a collection someone is about to part with — are exactly the parts an off-the-shelf platform treats as generic.

What we build
Storefront	Full catalogue with faceted search, product galleries, price-trend history and graded-card detail
Checkout	Guest and account checkout, card / TWINT / PayPal, stock reserved atomically so nothing oversells
Rachat (buyback)	Customers submit collections card by card or as a bulk lot, with live valuations and a tracked offer workflow
Grading	Submission intake and status tracking through to the returned grade
Loyalty	Points earned per order and spendable at checkout, at admin-configurable rates
Back office	Catalogue management, scan and CSV import from collection-tracking exports, orders, customers, buyback and grading queues
The storefront is in French, for a French-speaking Swiss market.

How we build it
A TypeScript-adjacent JavaScript monorepo — Next.js on the front, Express and Prisma over PostgreSQL on the back, sharing schema and business-rule packages so the two cannot disagree about what an order is.

<p> <img alt="Next.js" src="https://img.shields.io/badge/Next.js-black?logo=next.js&logoColor=white" /> <img alt="React" src="https://img.shields.io/badge/React-20232a?logo=react&logoColor=61dafb" /> <img alt="Express" src="https://img.shields.io/badge/Express-404d59?logo=express&logoColor=white" /> <img alt="Prisma" src="https://img.shields.io/badge/Prisma-2d3748?logo=prisma&logoColor=white" /> <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-336791?logo=postgresql&logoColor=white" /> <img alt="Stripe" src="https://img.shields.io/badge/Stripe-635bff?logo=stripe&logoColor=white" /> <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ed?logo=docker&logoColor=white" /> </p>
A few things we hold ourselves to:

Money is never trusted from the client. Totals, discounts and shipping are recomputed server-side at checkout from the product table; the request body is an intent, not a price.
Tests run against the real thing. The API suites mount the real application over HTTP against a real database, with no mocking — a guard that gets removed or reordered fails the build instead of passing a test built on a stub.
Every change goes through the same gate. Linting, type checking, dependency licences, secret scanning, dead-code and architecture-boundary analysis, schema-drift detection and the full test suite, before anything ships.
Documentation is part of the work. The reasoning behind a decision lives with the code, because the expensive thing to lose is not the implementation — it's why it is that way.
Repositories
Our application code is private: it runs a live shop, with customer orders and payment integrations in it. This organisation is here for the public face of that work.

Get in touch
Customers — support@prismea.ch, or find us on Discord
Everything else — support@prismea.ch
<p align="center"><sub>Yverdon-les-Bains, Switzerland</sub></p>

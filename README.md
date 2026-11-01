# Hong Kong Land Lots & Leases MCP

Connect your AI assistant to [BumiAtlas](https://bumiatlas.com) for Hong Kong land research through the Model Context Protocol.

This listing is a focused entry point for:

- Every land lot in Hong Kong (~375k) from the Lands Department's Lot dataset on CSDI/data.gov.hk: name, series, number, class, Land Registry PRN, register description, area and boundary
- Lot lookup as LandsD writes it ("IL 2782", "Lot 155 in DD 9", "DD9-155"), by PRN ("C4800223"), or by coordinates
- Lease terms where a grant document is loaded (~75k lots): grant type, term, expiry, permitted uses and building restrictions (height, storeys, site coverage, plot ratio, building covenant)
- Satellite and street map images of a lot and its neighbours, labelled by lot name

New Territories leases dated 1997-06-27 are shown extended to 2047-06-30 under the New Territories Leases (Extension) Ordinance. Lots have no owner, title or price information.

## Connect

```
https://bumiatlas.com/mcp/hongkong
```

Add it as a custom connector in any MCP client and sign in with Google. Tools, examples and data notes: [bumiatlas.com/mcp-docs/hongkong](https://bumiatlas.com/mcp-docs/hongkong).

## Tools

| Tool | Description |
|---|---|
| `HK_lot_search` | Find lots by name (IL 2782, DD 9 Lot 155), PRN, lot number, LotCSUID, or `latitude, longitude` |
| `HK_lot_get` | One lot: series, number, class, PRN, register description and lease terms; boundary as GeoJSON |
| `HK_lot_image` | Satellite or street map image of a lot or point, with every lot in view outlined and labelled with its lot name |

## Example prompts

- *"Which lot is at 22.2818, 114.1581 in Central? How big is it?"*
- *"Look up lot IL 2782: what does its lease allow, and when does it expire?"*
- *"What is the lot with PRN C4800223?"*
- *"How many lots are in DD 9?"*

## Data sources

Lots and lease terms © Lands Department, HKSAR Government (Land Parcel dataset, [data.gov.hk](https://data.gov.hk)), updated quarterly. Lots have no owner, title or price information.

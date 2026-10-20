---
name: xylem-mes-order-lookup
description: Look up a manufacturing order in Xylem's Apis Manager MES v2 surface, then its BOM and routing.
api: Xylem Apis Manager
generated: '2026-10-19'
method: generated
source: openapi/xylem-apis-manager-openapi.yml
operations:
  - MES_v2_GetOrderByOrderNumber
  - MES_v2_GetOrderBOMByOrderNumber
  - MES_v2_GetRoutingByPartNumber
---
# MES order lookup

1. Obtain a bearer token via the OAuth 2.0 password flow at `/token` (credentials are issued by Xylem; no self-serve signup).
2. Call `MES_v2_GetOrderByOrderNumber` with the order number.
3. Call `MES_v2_GetOrderBOMByOrderNumber` for the order's bill of materials.
4. For a part on the BOM, call `MES_v2_GetRoutingByPartNumber`.

Only the apis-dev and apis-test environments are publicly reachable; no rate limits, idempotency or error reference are published.

# Global Party Process API

API Process qui agit comme proxy/pass-through vers Global Party System API.

## Description

Cette API fournit un point d'entrée Process API pour accéder aux parties dans Global Data. Elle fait essentiellement un pass-through vers Global Party System API, permettant d'ajouter de la logique d'orchestration future si nécessaire.

## Endpoints

Identiques à Global Party System API:
- GET /api/process/global/parties
- POST /api/process/global/parties
- GET /api/process/global/parties/{partyGlobalId}
- POST /api/process/global/parties/lookup

## Configuration

### Connexions HTTP Requises

- **Global Party System API** (port 8081)

Configurer dans `global.xml`:
- `Global_Party_System_API_Config`

### Port

- **Port HTTP**: 8082

## Architecture Technique

### Flows Business-Logic

- `get-parties-business-logic`: Pass-through vers System API
- `upsert-party-business-logic`: Pass-through vers System API
- `get-party-by-global-id-business-logic`: Pass-through vers System API
- `lookup-party-business-logic`: Pass-through vers System API


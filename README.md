# 🚗 Vehicle Telematics Platform

Fleet management system for tracking vehicles, collecting telemetry, and analyzing performance.

## Features

- Real-time GPS vehicle tracking (Leaflet.js)
- Telemetry collection (speed, fuel, temperature, RPM, tire pressure, battery)
- Analytics & charts (Chart.js)
- REST API (Express.js) + MongoDB
- Docker Compose setup

## Tech Stack

Node.js, Express, MongoDB (Mongoose), HTML/CSS/JS, Leaflet, Chart.js, Docker

## Quick Start

### Docker
```bash
git clone https://github.com/prakash-kumar592/vehicle-telematics-platform.git
cd vehicle-telematics-platform
docker-compose up -d
```
- Frontend: http://localhost:3000
- Backend API: http://localhost:5000/api/health
- MongoDB: localhost:27017

### Local
```bash
cd backend
cp .env.example .env
npm install
npm run dev
```
Then open `frontend/index.html` in a browser (needs MongoDB running on localhost:27017).

## API Endpoints

**Vehicles**
- `POST /api/vehicles` · `GET /api/vehicles` · `GET|PUT|DELETE /api/vehicles/:id`

**Locations**
- `POST /api/locations` · `GET /api/locations/:vehicleId` · `GET /api/locations/:vehicleId/latest`

**Telemetry**
- `POST /api/telemetry` · `GET /api/telemetry/:vehicleId` · `GET /api/telemetry/:vehicleId/latest`

**Analytics**
- `GET /api/analytics/fuel|distance|speed|summary/:vehicleId`

## Project Structure

```
vehicle-telematics-platform/
├── backend/   (config, models, controllers, routes, middleware, server.js)
├── frontend/  (css, js, index.html)
├── docker/Dockerfile
├── docker-compose.yml
└── README.md
```

## License

MIT — Prakash Kumar

# Strategic Public Procurement Desk

## One-sentence benefit

Help public buyers turn procurement cases into transparent, resilient and sustainable purchasing decisions.

## Live demo

[Watch the workflow](docs/demo.webm).

## Screenshots

![Strategic public procurement dashboard](docs/screenshot.png)

## Main features

- Search and sort procurement cases across tenders and buying teams.
- Create a strategic sourcing case through the Java service.
- Advance draft and review cases toward approval.
- View buying guidance on a separate route.
- Handle loading, empty, error and success states responsively.

## Technology used

Vue 3, TypeScript, Pinia, Vue Router, Vite, Spring Boot and Java 21.

## Installation instructions

Install Node.js 22 and Java 21. Run `npm install`, then start the backend with `cd backend && mvn spring-boot:run`. In another terminal run `npm run dev`.

## Commercial licensing/contact

Commercial licensing and integration support are available. Use the repository contact options to discuss deployment.

## Business problem and users

Public buyers, procurement advisers, sustainability teams and suppliers need to coordinate strategic criteria, proportional evidence and lifecycle value.

## Key workflows

Find a tender case, add a procurement need, review its owner and priority, advance the decision state and consult the buying guidance.

## Vue framework highlights

Pinia provides reactive API state and computed metrics, Vue Router separates operational and guidance views, and Vue templates expose accessible live updates.

## Java backend highlights

Spring Boot supplies validated list, search, create and update APIs, consistent error responses, a health endpoint and tested service rules.

## Architecture and state flow

Vue actions call `/api/items` through the development proxy. The Java controller validates requests, the service owns workflow state and responses update the Pinia store.

## Accessibility and responsive behaviour

The interface uses labelled search, semantic navigation, keyboard controls, readable status text and layouts that collapse cleanly on small screens.

## Verification commands

Run `npm test`, `npm run build`, `cd backend && mvn test` and `cd backend && mvn package`.

## Structure

`src` holds the Vue routes and store, `backend` holds the Java API, and `docs` holds inspected media.

## Tradeoffs

The sample uses in-memory records for a fast local setup. A production service should add identity, persistence and partner data exchange.

## Roadmap

Add criterion libraries, supplier evidence, joint purchasing, conflict checks and award analytics.

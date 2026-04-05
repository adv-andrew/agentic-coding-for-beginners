# Web Dev Final Project

React app for my Web Development class.

## Rules
- React 18 with functional components only (no class components)
- Use CSS modules for styling (no Tailwind or Bootstrap)
- State management with useState and useContext only (no Redux)
- Must be responsive (mobile + desktop)
- Must be accessible (alt text, aria labels, semantic HTML)

## Project Structure
- src/components/ -- React components
- src/pages/ -- page-level components
- src/context/ -- React context providers
- src/assets/ -- images and static files
- public/ -- index.html and favicon

## How to Run
- npm install
- npm start (runs on localhost:3000)
- npm test (runs Jest tests)
- npm run build (creates production build)

## API
- We use a mock API at http://localhost:3001
- Start it with: npm run api
- Endpoints: GET /tasks, POST /tasks, DELETE /tasks/:id

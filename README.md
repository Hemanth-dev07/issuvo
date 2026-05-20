# Issuvo

Issuvo is a support ticket management web app built with Next.js, React, Tailwind CSS, MongoDB, and Mongoose. It lets users create, view, update, and delete support tickets while tracking useful ticket details such as category, priority, progress, and status.

## Features

- Dashboard view for browsing support tickets by category
- Create new support tickets
- Edit existing ticket details
- Delete tickets that are no longer needed
- Track ticket priority from 1 to 5
- Track ticket progress from 0% to 100%
- Track ticket status such as Not Started, Started, and Done
- MongoDB-backed persistence using Mongoose
- API routes for creating, reading, updating, and deleting tickets
- Dark themed UI styled with Tailwind CSS

## Tech Stack

- Next.js
- React
- Tailwind CSS
- MongoDB
- Mongoose
- Font Awesome

## Project Structure

```txt
issuvo/
├── app/
│   ├── (components)/
│   │   ├── DeleteBlock.jsx
│   │   ├── Nav.jsx
│   │   ├── PriorityDisplay.jsx
│   │   ├── ProgressDisplay.jsx
│   │   ├── StatusDisplay.jsx
│   │   ├── TicketCard.jsx
│   │   └── TicketForm.jsx
│   ├── (models)/
│   │   └── Ticket.js
│   ├── TicketPage/
│   │   └── [id]/
│   │       └── page.jsx
│   ├── api/
│   │   └── Tickets/
│   │       ├── route.js
│   │       └── [id]/
│   │           └── route.js
│   ├── globals.css
│   ├── layout.js
│   └── page.jsx
├── public/
├── package.json
├── postcss.config.js
└── tailwind.config.js
```

## Getting Started

### Prerequisites

Make sure you have the following installed:

- Node.js
- npm
- A MongoDB database connection string

### Installation

Clone the repository:

```bash
git clone https://github.com/Hemanth-dev07/issuvo.git
cd issuvo
```

Install dependencies:

```bash
npm install
```

Create a `.env.local` file in the project root and add your MongoDB connection string:

```env
MONGODB_URI=your_mongodb_connection_string
```

Start the development server:

```bash
npm run dev
```

Open the app in your browser:

```txt
http://localhost:3000
```

## Available Scripts

```bash
npm run dev
```

Runs the app in development mode.

```bash
npm run build
```

Builds the app for production.

```bash
npm run start
```

Starts the production server after building the app.

```bash
npm run lint
```

Runs the Next.js lint command.

## Environment Variables

| Variable      | Description                                |
| ------------- | ------------------------------------------ |
| `MONGODB_URI` | MongoDB connection string used by Mongoose |

## API Routes

| Method   | Route              | Description                 |
| -------- | ------------------ | --------------------------- |
| `GET`    | `/api/Tickets`     | Fetch all tickets           |
| `POST`   | `/api/Tickets`     | Create a new ticket         |
| `GET`    | `/api/Tickets/:id` | Fetch a single ticket by ID |
| `PUT`    | `/api/Tickets/:id` | Update a ticket by ID       |
| `DELETE` | `/api/Tickets/:id` | Delete a ticket by ID       |

## Ticket Fields

Each ticket stores the following information:

- Title
- Description
- Category
- Priority
- Progress
- Status
- Active state
- Created and updated timestamps

## Deployment Notes

Before deploying, make sure the production environment has `MONGODB_URI` configured.

Also review any hardcoded `localhost:3000` API fetch URLs and convert them to relative URLs or an environment-based base URL before hosting the app outside your local machine.

## Author

Built by Hemanth.

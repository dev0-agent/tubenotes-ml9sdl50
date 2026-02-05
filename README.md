# TubeNotes

> Your personal knowledge base for YouTube content.

TubeNotes is a full-stack bookmarking application designed to help you learn from YouTube videos more effectively. Instead of just watching, TubeNotes allows you to save videos to a personal library, add timestamped annotations, and organize content with tags. Never lose track of a key insight again.

## Tech Stack

*   **Framework:** TanStack Start (React with SSR)
*   **Database:** Drizzle ORM
*   **Styling:** Tailwind CSS & shadcn/ui
*   **Video Integration:** YouTube IFrame Player API

## Features

*   **Video Library:** Save and organize YouTube videos.
*   **Smart Player:** Watch videos directly within the app.
*   **Timestamped Notes:** Add notes that are linked to specific video times.
*   **Instant Seek:** Click a note's timestamp to jump the player to that moment.
*   **Tagging:** Organize your library by topic.
*   **Search:** Quickly find videos by title or tag.

## Getting Started

1.  **Clone the repository:**
    ```bash
    git clone <repo-url>
    cd tubenotes
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    ```

3.  **Setup Environment:**
    Create a `.env` file based on `.env.example` and add your database credentials.

4.  **Run Database Migrations:**
    ```bash
    npx drizzle-kit push
    ```

5.  **Start the Development Server:**
    ```bash
    npm run dev
    ```

## Documentation

*   See [TASKLIST.md](./TASKLIST.md) for the development roadmap.
*   See [LEARNINGS.md](./LEARNINGS.md) for technical insights gathered during development.
*   See [.dev0/RULES.md](./.dev0/RULES.md) for coding standards.
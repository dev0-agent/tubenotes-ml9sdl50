# Task List

This file shows the current progress of all tasks in this project.
It is automatically updated by dev0 as tasks are completed.

---

## Phase 1

- [x] ✅ **Setup Environment and Database Configuration**
  Create an `env.ts` file to handle environment variables (DATABASE_URL). Configure Drizzle ORM with a basic connection client. Ensure the project can connect to the database.

- [ ] ⏳ **Design Database Schema**
  Define the Drizzle schema. We need tables for `videos` (id, youtubeId, title, url, createdAt), `notes` (id, videoId, timestamp, content, createdAt), and `tags` (id, name, videoId). Run the initial migration to create the tables.

- [ ] ⏳ **Create Global Layout and Navigation**
  Implement the root layout using TanStack Start. Add a responsive navigation bar with links to 'Home' and 'Add Video'. Include a placeholder for the main content area.

## Phase 2

- [ ] ⏳ **Implement Video Addition Server Function**
  Create a server function to handle adding a new video. It should accept a YouTube URL, extract the Video ID using regex, and insert the record into the `videos` table using Drizzle. Return the new video object.

- [ ] ⏳ **Build Video Library Dashboard**
  Create the index route to display saved videos. Use a loader to fetch videos from Drizzle. Render them in a responsive grid using shadcn/ui Cards. Each card should link to the individual video page.

- [ ] ⏳ **Create Video Detail Route & Player Component**
  Create a dynamic route `$videoId`. Build a `YouTubePlayer` component that wraps the IFrame API. It needs to expose a ref or context to control playback (seekTo). Ensure the player loads the correct video ID from the route params.

- [ ] ⏳ **Implement Timestamped Notes System**
  Build the notes interface next to the player. 1. Create a server action to save a note. 2. In the UI, add a text area and a 'Add Note at [Current Time]' button. 3. When clicked, capture the player's current time and save it to the DB.

- [ ] ⏳ **Implement Seek-to-Note Functionality**
  List existing notes for the video below/beside the player. Make the timestamp in each note clickable. When clicked, use the player ref to seek the video to that specific second.

## Phase 3

- [ ] ⏳ **Add Tagging Functionality**
  Update the 'Add Video' and 'Video Detail' views to support tags. Allow users to add tags to a video. Update the schema if necessary (if not done in task-2) and add UI badges to display them.

- [ ] ⏳ **Implement Search and Filter**
  Add a search bar to the dashboard. Implement filtering logic in the loader or via a server function to filter videos by title or selected tag.

## Phase 4

- [ ] ⏳ **UI Polish and Empty States**
  Improve the visual design. Add empty states for when no videos or notes exist. Improve the styling of the note timestamps (e.g., format seconds as MM:SS). Ensure mobile responsiveness.

- [ ] ⏳ **Error Handling and Validation**
  Add Zod validation for inputs (valid YouTube URLs). specific error messages if the YouTube API fails to load or if the database is unreachable.

---

_Last updated by dev0 automation_

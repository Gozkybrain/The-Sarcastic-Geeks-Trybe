# Sarcastic Geeks Trybe

The **`Sarcastic Geeks Trybe`** is an Online Community aimed at connecting even the lowest echelon of developers and techies in general, and creating a link with seniors and intermediates alike. Community extra mural activities like [X Spaces](https://x.com/sarcasticgeek4u) and [#100DaysOfCodeAndDesign](https://x.com/gozkybrain4u/status/1913151187777388680) have been pivoting this collaborative and creative insight, and now the community's official web program.

## The Trybe's Activities

Members of the Trybe connect online authenticating with their X account (for dp purposes), and participate in community games to earn in-app points which would eventually be used for in-app community activity like purchase of accessories and voting rights, etc.

## Development Requirements
- [React JS](https://reactjs.org/): **Web App Interface**
- [Animate.css](https://animate.style/) and [GSAP (GreenSock)](https://greensock.com/gsap/): **Animation Flow**
- [Firebase Console](https://console.firebase.google.com/): **Authentication and Database**


## Expected Mini Apps and Games

- [Obstacle Course](./obstacle-course.md)
- [Snake Game](./snake-game.md)
- [Hangman Game](./hangman-game.md)
- Bez AI Course Builder
- FindMe App (Coming Soon)


.. and more exciting browser games to foster community activity, and even a featured store to spend community in-app points before they actually become in-app token on web3.

### Peer-to-Peer Transfers

Users can now **send Cowries 🐚 directly to other users** within the platform!  
This enables seamless **P2P transactions** and supports **in-app purchases**, empowering users to transfer balances across accounts safely and instantly.  

✅ Select a recipient from the community.  
✅ Enter the amount to transfer.  
✅ System automatically deducts from your accounts in order of available balance.  
✅ Recipient receives Cowries 🐚 instantly, with balances updated in real-time.


# Bez AI — AI-Powered Personalized Course Builder

## Features

- AI-driven interactive chatbot that gathers user goals and preferences.
- Dynamic question flow limited to 5 questions before generating course.
- Validates user access via a secret code.
- Generates detailed, JSON-based course structure:
  - Modules with titles, descriptions.
  - Embedded YouTube videos fetched via search API.
- Stores courses in Firestore under a `courses` collection.
- Saves user's full name and course creation timestamp for sorting.
- Auto-focuses input field for quick typing.
- Replaces input & send button with a "Start Course" button after generation.
- Clean UI with scrolling chat messages and distinct user/AI styling.
- Uses Next.js App Router for navigation (`/course/:course-id`).

### 1. AI Prompt Flow

Bez AI uses a structured prompt system to create a personalized learning experience through conversation:

- **System Intro Prompt:** This sets the initial context and tone for the chatbot, welcoming the user and framing the interaction around learning tech skills.
- **Follow-up System Prompt:** After each user input, a dynamic follow-up prompt guides the AI to ask relevant questions, gradually gathering detailed info about the user's learning goals. The bot collects up to 5 key inputs (`questionsAsked`).
- **Course Generation Prompt:** Once the user has answered enough questions and provided an access code, a special prompt instructs the AI to generate a full course outline in JSON format, tailored to the user's age, name, and stated goals.

This layered prompt approach ensures the conversation feels natural while collecting necessary data for course creation.

---

### 2. Course JSON Generation & Parsing

The AI's response is expected to contain a **JSON** object describing the course:

- `courseTitle`
- `courseDescription`
- An array of `modules`, each with:
  - `title`
  - `description`
  - Placeholders for video metadata

Bez AI extracts this JSON even if it’s wrapped inside code blocks using regex parsing, and then parses it to a JavaScript object for further use.

---

### 3. YouTube Video Enrichment

To enhance each module, Bez AI connects with the **YouTube Data API** and performs the following steps:

- Constructs a search query combining the module title and the user's learning goal.
- Fetches the top YouTube tutorial video matching the query.
- Extracts video details including URL, title, description, thumbnail, and duration.
- Injects this data back into the corresponding course module.

This ensures every module is enriched with relevant video tutorials, making the course interactive and visually engaging.

---

### 4. Saving Course Data

Once the course JSON is fully populated with YouTube video info, the entire course object is saved in **Firebase Firestore** under the `courses` collection. The saved data includes:

- The user's `fullName` — to associate the course with the creator for easy retrieval or filtering.
- A `createdAt` timestamp — to record when the course was generated.

This persistence enables future retrieval, user-specific course management, and analytics.

---

### 5. User Interface & Navigation

- After the course is generated, the chatbot displays the course content formatted in HTML with images and clickable links to YouTube tutorials.
- The chat input field and send button are hidden.
- A **“Start Course”** button appears, which, when clicked, navigates the user to the course page at `/course/:course-id`.
- This page displays the full course experience, allowing users to learn with the curated content and videos seamlessly.
- Certificate of completion is awarded at the end of the course, you are responsible for learning progress.
- Users can only learn from their own courses.

---

## What to expect?

The project is part of the Community's [#90DaysLab]() Challenge, which aims to create and scale a startup to funding in 90 days.

- First the project will provide a seamless Twitter Authentication system for Trybe members to welcome them online and give them a Profile.
- Games will be announced and released gradually and regularly and the Trybe will of course be involved in testing the Games and giving honest reviews.
- Games will be updated based on relevant reviews for best Trybe experience.
- Trybe members will earn points to help participate in activities.
- When the community gets integrated into the web3 platform, web3 activities will also be incorporated.

## COMING SOON - FindMe API and APP
An experimental **AI-assisted job discovery platform** focused on startup jobs.  
The platform aggregates **startup jobs + funding data** from multiple APIs, enriches them with metadata (founders, socials, funding info), stores them in a database, and allows job seekers to search, filter, and apply — either directly via job links or by networking with startup founders.

---


# Contributions

This project is an official community project for the Sarcastic Geeks Trybe, and with special contributions from Trybe leads, among other outsourced resources.


# TODO
- Plan Admin route
  - Overview Statistics: All Admin Users, Top Earning Users, Graph of gender and graph of rank, search for users
  - All Users Page with search and special filtering, admin can edit user data completely and add funds
  - Extract user data from collection, migrate user data to a new db collection, etc.
  - Courses: Moderate, Create, Delete available courses
  - Jobs: Pending because the feature is not yet ready
  - Update Project with Beta Testing Review badge and score. ie view all completed projects.

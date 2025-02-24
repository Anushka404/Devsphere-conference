# DevSphere Conference

A fictional tech conference website built with **SvelteKit** and **Tailwind CSS**.

## 🚀 Features

- **Home Page:** Hero section, keynote speakers.
- **Speakers Page:** Grid layout showcasing speakers with images, names, and bios.
- **Schedule Page:** Structured timetable of sessions.
- **Sponsors Page:** List of sponsors with logos and tiers.
- **About Page:** Introduction to the conference.
- **Contact Page:** Contact form and social media links.
- **Bonus Features:**  countdown timer, session filtering, sponsor tiers, Google Map integration.

## 🛠 Tech Stack

- **SvelteKit**
- **Tailwind CSS**
- **JavaScript**

## 📦 Installation & Setup

1. **Clone the Repository**
   ```bash
   git clone [https://github.com/yourusername/devsphere-conference.git]
   cd devsphere-conference
   ```

2. **Install Dependencies**
   ```bash
   npm install
   ```

3. **Run Development Server**
   ```bash
   npm run dev
   ```

## 📂 Project Structure

```
/src
 ├── lib
 │   ├── components  # Reusable components
 │   │   ├── CountdownTimer.svelte
 │   │   ├── DarkModeToggle.svelte
 │   │   ├── Footer.svelte
 │   │   ├── Header.svelte
 │   │   ├── LocationCard.svelte
 │   │   ├── Main.svelte
 │   │   ├── ScheduleCard.svelte
 │   │   ├── SpeakerCard.svelte
 │   │   ├── Sponsor.svelte
 │   ├── data  # Data files
 │   │   ├── schedule.js
 │   │   ├── speakers.js
 │   │   ├── index.js
 ├── routes
 │   ├── about
 │   ├── contact
 │   ├── schedule
 │   ├── speakers
 │   ├── sponsors
 │   ├── +layout.svelte  # Main layout
 │   ├── +page.svelte  # Root page
 ├── static
 │   ├── assets
 │   ├── images
 │   │   ├── favicon.png
 ├── app.css  # Global styles
 ├── app.html  # Main HTML template
 ├── .gitignore  # Git ignore file
 ├── .npmrc  # NPM config
 ├── jsconfig.json  # JS config
 ├── package-lock.json  # Lock file
 ├── package.json  # Dependencies
 ├── README.md  # Project documentation
 ├── svelte.config.js  # Svelte config
 ├── vite.config.js  # Vite config
```

## 📜 Code Quality & Guidelines

- **Clean and modular code structure.**
- **Responsive and visually appealing UI.**
- **Reusable components for consistency.**
- **Follow best practices in Svelte and Tailwind CSS.**

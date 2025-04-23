this requiments files first make. then supabase use for backend and expo api file based use full project compelete

## 📌 Project Title: Habit Tracker + Leaderboard App

A mobile app that helps users build and track daily habits while competing with others through a global leaderboard based on streaks and XP.

---

## 🚀 Features

### ✅ Habit Management

- Create, edit, and delete daily habits
- Customize habits with:
  - Title
  - Color or emoji/icon
  - Scheduled days (e.g. Mon/Wed/Fri)
- Mark habits as done/not done daily
- Habit streak tracking
- XP rewards for consistency

### 📅 Daily Tracker View

- Calendar or list view of today’s habits
- Toggle/check-off habits
- Visual feedback (e.g. confetti or animations)

### 📈 Progress & Analytics

- Weekly streak charts
- Completion history (calendar heatmap)
- XP earned by week/month
- Longest streaks

### 🧑‍🤝‍🧑 Leaderboard

- Global leaderboard based on XP
- Option to follow friends
- Top 10/Top 100 list
- Show username, avatar, XP, current streak

### 👤 User Profile

- Avatar & username
- Stats summary: XP, longest streak, current streak
- Editable bio
- Level/Rank (gamified)

### 🔐 Authentication

- Sign up & sign in (email/password)
- Supabase Auth integration
- Optional social login (Google, Apple)

### 🛠️ Settings

- Dark mode toggle
- Habit reminder notifications (Expo push)
- Clear all data / reset progress

---

## 🗃️ Database Structure (Supabase)

### Tables

#### `users`

- `id` (UUID)
- `email`
- `username`
- `avatar_url`
- `xp`
- `current_streak`
- `longest_streak`
- `created_at`

#### `habits`

- `id` (UUID)
- `user_id` (FK)
- `title`
- `icon`
- `color`
- `frequency` (e.g., Mon, Tue, Fri)
- `created_at`

#### `habit_logs`

- `id` (UUID)
- `habit_id` (FK)
- `date` (YYYY-MM-DD)
- `completed` (boolean)

# SpotMe

SpotMe is a training, nutrition and body-tracking platform. It brings together a mobile app for everyday logging, a web platform for members and health professionals, and an AI service that helps each member understand their progress from their own data.

## Repositories

| Repository | Description | Stack | Visibility |
|---|---|---|---|
| [mobile](https://github.com/SpotMe-Gym/mobile) | Offline-first mobile app for iOS and Android, with an Apple Watch companion. Workouts, nutrition, body measurements and heart rate. | TypeScript, Expo, React Native | Private |
| [website](https://github.com/SpotMe-Gym/website) | Web platform: product site, member area, professional area and admin verification. | TypeScript, Next.js, Supabase | Private |
| [ai](https://github.com/SpotMe-Gym/ai) | AI service that analyses a member's training, nutrition and body data and answers with evidence. | Python, LangGraph | Private |
| [SpotMe-Workspace](https://github.com/SpotMe-Gym/SpotMe-Workspace) | Shared documentation, decisions and proposals for the whole project. | Markdown | Private |

Private repositories are visible to organization members only.

## The platform

**Mobile app.** Workout planning and a guided workout player with timers, food logging with search and barcode scanning, weight and body measurements with a 3D body view, heart rate from Bluetooth straps and Apple Watch, and a home screen built from configurable widgets. The app works offline and syncs when a connection is available.

**Member area.** A desktop counterpart to the app: dashboard, weight and body history, nutrition, targets, care team, data export and account deletion.

**Professional area.** Personal trainers, nutritionists, dietitians and doctors apply with their credentials and are verified before they can invite clients. Each client decides which of their data a professional may see. Professionals can keep private notes and suggest calorie and macronutrient targets.

**AI service.** Analysis and coaching grounded in the member's own records and in published research, with rules that adapt to the member's jurisdiction.

## Architecture

- The mobile app and the website share one Supabase backend, with row-level security on every table.
- Profile, weight, body measurements, meals and workouts sync in both directions between the app and the website.
- The AI service reads member data under the same access rules and runs as a separate service.
- The product is available in English and Italian.

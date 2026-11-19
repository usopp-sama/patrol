# Patrol

Fly a twin-engine fighter through autumn lake country at sunset. Take on enemy jets, find a landing strip, or switch to the cockpit and watch your six in the mirrors.

## Play locally

Open [public/index.html](public/index.html) in a WebGL2-capable browser. All game code, graphics, and synthesized sound live in that file. The game also works offline.

Use the mouse or arrow keys to steer. **G** fires the gun, **F** fires a missile, **Space** cycles cameras, **C** looks behind while held, and **L** requests landing or takeoff. Open **Controls** to change bindings and sensitivity or configure a gamepad.

## Host on Vercel

1. Import this GitHub repository as a new Vercel project. Keep the repository root as the project root. The included configuration serves the `public` directory as a static site.
2. Deploy the project. Then open **Analytics** in the project sidebar and enable **Web Analytics**.
3. Redeploy once after enabling analytics so Vercel serves the analytics script and collection endpoints. Open the production site and start a flight to generate the first measurements. [Vercel setup guide](https://vercel.com/docs/analytics/quickstart)

## Read traffic and play stats

Open **Vercel → your Patrol project → Analytics**. Choose **Production** and a date range, then read the **Pages** breakdown.

| Dashboard metric | Page | What it measures |
| --- | --- | --- |
| Visitors | `/` | Estimated distinct visitors who opened the game |
| Visitors | `/play` | Estimated distinct visitors who started at least one flight |
| Page Views | `/` | Game page loads, including reloads |
| Page Views | `/play` | Flights started, including replays |

The two paths label the title and flight screens in analytics. Patrol records the title once per document load and the flight screen when a sortie actually starts. Opening settings, switching cameras, landing, and taking off again during the same sortie do not start another count. Local files opened directly skip analytics. The game keeps running when analytics is blocked.

For the share of visitors who played, divide the `/play` visitor count by the `/` visitor count for the same period. Vercel estimates visitors anonymously, so these figures are approximate. [Dashboard guide](https://vercel.com/docs/analytics/using-web-analytics) · [How visitors are counted](https://vercel.com/docs/analytics)

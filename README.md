# Sales & Revenue Analysis Dashboard

A React + Vite dashboard for analyzing business sales data, with CSV/Excel import,
interactive filters, KPI cards, charts, and auto-generated business insights.

## Run it in VS Code

1. Open this folder (`sales-dashboard`) in VS Code: `File > Open Folder...`
2. Open a terminal in VS Code: `Terminal > New Terminal`
3. Install dependencies:
   ```
   npm install
   ```
4. Start the dev server:
   ```
   npm run dev
   ```
5. It will open automatically at `http://localhost:5173`. If not, click the link
   shown in the terminal.

## Requirements

- Node.js 18 or newer (check with `node -v`). Download from https://nodejs.org if needed.

## Project structure

```
sales-dashboard/
├── index.html            entry HTML page
├── package.json          dependencies and scripts
├── vite.config.js        Vite dev server config
└── src/
    ├── main.jsx           React app entry point
    └── SalesDashboard.jsx the dashboard component (all logic + UI)
```

## Using your own data

The dashboard loads with generated sample data by default. Go to the
"Data Import" tab in the sidebar and drag in a `.csv` or `.xlsx` file with
columns like Order Date, Order ID, Product, Category, Quantity, Unit Price,
Sales, Revenue, Region, Customer, Salesperson. Columns are matched automatically
regardless of exact naming — only Order Date, Product, and Quantity are required.

## Build for production

```
npm run build
```

Output goes to the `dist/` folder, which you can deploy to any static host
(Vercel, Netlify, GitHub Pages, etc.).

## Note on database connections

The "Database Connection" panel in Data Import is a visual placeholder.
Connecting to a live database (Postgres, MySQL, etc.) requires a backend
service to hold credentials and run queries — this is a frontend-only project.

## Push this to GitHub

From inside this folder:

```
git init
git add .
git commit -m "Initial commit: Sales & Revenue Analysis Dashboard"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo-name>.git
git push -u origin main
```

Create the empty repo on GitHub first (github.com → New repository), without
a README or .gitignore, then copy its URL for the `git remote add` step above.

`node_modules/` and `dist/` are already excluded via `.gitignore`, so the
repo stays small. Anyone cloning it just needs to run `npm install` and
`npm run dev` to get going, per the steps above.

### Deploy the live dashboard (optional)

Once on GitHub, you can deploy it for free in a couple of clicks:
- **Vercel**: vercel.com → Import Project → pick the repo → deploys automatically (it detects Vite)
- **Netlify**: netlify.com → Add new site → Import from GitHub → build command `npm run build`, publish directory `dist`
- **GitHub Pages**: needs `vite.config.js` updated with a `base` path matching your repo name, then `npm run build` and publish the `dist/` folder

# AeroScope - Global Air Quality Tracker

A premium, highly interactive global air quality visualization dashboard featuring a full-screen map, real-time localized pollution analytics, and predictive health recommendations. Built using Leaflet.js map layer integrations and the World Air Quality Index (WAQI / aqicn.org) API.

---

## 🌟 Key Features

*   **Global Visual Mapping**: Full-screen interactive map utilizing premium CartoDB Dark Matter tiles layered with real-time global WAQI station markings.
*   **Multi-Pollutant Layers**: Switch dynamically between composite AQI and standalone fine particles ($PM_{2.5}$, $PM_{10}$), Ozone ($O_3$), Nitrogen Dioxide ($NO_2$), Sulfur Dioxide ($SO_2$), and Carbon Monoxide ($CO$).
*   **Geolocalized Analytical Drawer**: Click anywhere on the map to query the nearest station and slide out a clean, minimalist slate sidebar featuring:
    *   Large, color-coded AQI badge matching standard health levels.
    *   An interactive slider pointer representing AQI values.
    *   Dynamic, custom-rendered pollutant progress indicators.
    *   Comprehensive weather reports (temperature, humidity, wind, and barometric pressure).
    *   Actionable localized health advisories.
*   **Autocomplete Search**: Built-in station autocomplete search. Simply type a city name (e.g. "Tokyo", "London") to fly there instantly.
*   **API Token Safe Store**: An elegant, local token manager that stores your WAQI token securely in `localStorage` inside your browser, combined with a built-in Shanghai Demo Mode for rapid offline previewing.

---

## 🚀 Quickstart

AeroScope is a pure front-end web application with zero server-side dependencies. You can run it instantly:

### Method 1: Direct Execution
Simply open [index.html](file:///Users/uuuu/Desktop/GenTools/anti/AQmap/index.html) in any modern web browser (Double-click the file in macOS Finder or drag it into Chrome/Safari).

### Method 2: Local Development Server
To serve it from a local server, run one of the following commands in the project directory:

```bash
# Using python
python3 -m http.server 8080

# Using Node.js
npx http-server -p 8080
```
Then navigate to `http://localhost:8080` in your browser.

---

## 🔑 Getting Your Free WAQI API Token

To fetch real-time global data from stations, you will need a personal API token (takes less than 10 seconds to generate):

1. Go to the WAQI API Platform token creation page: **[aqicn.org/data-platform/token/](https://aqicn.org/data-platform/token/)**
2. Enter your Name and Email address, then click **Submit**.
3. Check your email inbox. You will receive an activation mail containing your unique API Token string immediately.
4. Open AeroScope, click the **Settings** gear icon in the top right, paste your token, and click **Save & Apply**!

> [!NOTE]
> **Demo Mode**
> If you choose to click "Enable Shanghai Demo Mode" in the settings, the app will run using a public fallback token that returns live measurements for Shanghai, China. This lets you explore the dashboard's features immediately without an email sign-up.

---

## 🛠️ Technology Stack

*   **Structure**: Semantic HTML5 (incorporating native `<dialog>` and responsive structure).
*   **Styling**: Pure CSS3 utilizing:
    *   **Flat Slate SaaS Aesthetics**: Clean dark surfaces, neat solid borders, tailored HSL color indicators, and highly structured typography.
    *   **Dynamic UI**: Customized CSS custom properties (`--brand-color`, etc.) styled dynamically by JavaScript inputs.
    *   **Native Transitions**: `@starting-style` transitions for native top-layer `<dialog>` modals.
    *   **Fully Responsive**: Grid & flexbox fluid layouts transforming sidebar drawers into mobile bottom sheets seamlessly.
*   **Logic**: Modern Vanilla JavaScript utilizing native standard APIs (navigator geolocation, standard Fetch client, local storage caching).
*   **Map Engine**: Leaflet.js v1.9.4 CDN.

---

## 🌐 Deploying to GitHub & GitHub Pages

Since AeroScope is built as a single, fully-contained static HTML file, it is exceptionally easy to host and share using **GitHub Pages** for free!

### How to Push to GitHub

1. Create a new, empty repository on your GitHub account (do not add a README, license, or `.gitignore` yet).
2. Copy your GitHub repository URL (e.g., `https://github.com/your-username/aeroscope.git`).
3. Run the following commands in your local project folder to initialize git, link the remote repository, and push:

```bash
# 1. Initialize local Git repository (if not done already)
git init

# 2. Add files
git add index.html README.md

# 3. Create initial commit
git commit -m "feat: initial commit with unified standalone dashboard"

# 4. Rename main branch
git branch -M main

# 5. Add your remote repository origin (replace with your URL)
git remote add origin https://github.com/your-username/aeroscope.git

# 6. Push to GitHub
git push -u origin main
```

### How to Enable GitHub Pages (Free Hosting!)

Once the code is pushed to GitHub, you can publish it as a live website in 10 seconds:

1. Go to your repository on **GitHub.com**.
2. Click on the ⚙️ **Settings** tab in the top navigation bar.
3. Under the **Code and automation** sidebar section, click on **Pages**.
4. In the **Build and deployment** section, under **Branch**:
   * Change "None" to **`main`**.
   * Leave the folder select as **`/ (root)`**.
   * Click **Save**.
5. Wait about 30 seconds, and refresh the page. You will see a banner at the top of the Pages settings showing your live URL (e.g., `https://your-username.github.io/aeroscope/`).

Now anyone in the world can open your premium real-time map with a single click!

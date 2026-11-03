# Simple-Calculator
A simple, clean calculator that runs in your browser. It is a single `index.html` file with no build step and nothing to install.

## Features

- Add, subtract, multiply and divide, with chained calculations (for example `12 + 8 × 2`, evaluated one step at a time as you press each operator)
- Percent, plus/minus sign change, backspace and all-clear
- Full keyboard support
- Light and dark themes that follow your device setting
- Indian-style digit grouping (for example `12,34,567`)
- A history line above the result that shows the last calculation
- Clear message on division by zero
- Responsive layout that works on phones and desktops

## Download

Pick whichever option suits you.

**Option 1: Download the file**

1. Open the repository page on GitHub.
2. Click `index.html`.
3. Click the download icon (Download raw file) at the top right of the file view.

**Option 2: Clone the repository**

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
```

Replace `<your-username>` and `<your-repo>` with the actual values.

**Option 3: Download as ZIP**

On the repository page, click **Code**, then **Download ZIP**, and extract it.

## How to run

Double-click `index.html`, or drag it into any modern browser (Chrome, Edge, Firefox, Safari). That is all.

Optionally, serve it locally:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000` in your browser.

## How to use

Click or tap the keys, or type on your keyboard.

| Key on screen | Keyboard | What it does |
| --- | --- | --- |
| `0`–`9` | `0`–`9` | Enter digits |
| `.` | `.` or `,` | Decimal point |
| `+` `−` `×` `÷` | `+` `-` `*` or `x` `/` | Choose an operation |
| `=` | `Enter` or `=` | Show the result |
| `%` | `%` | Turn the number into a percentage |
| `±` | none | Switch between positive and negative |
| `⌫` | `Backspace` | Delete the last digit |
| `AC` | `Esc` or `Delete` | Clear everything |

### Notes on behavior

- **Chaining:** pressing a second operator calculates the pending operation first. `2 + 3 ×` shows `5` and waits for the next number.
- **Percent:** on its own, `50 %` gives `0.5`. After `+` or `−`, it takes that percentage of the first number, so `200 + 10 %` becomes `200 + 20` and equals `220`.
- **Precision:** results are rounded to 12 significant digits to avoid floating point noise like `0.1 + 0.2 = 0.30000000000000004`.
- **Length limit:** you can type up to 15 digits in one number.

## Publish on GitHub Pages

1. Push `index.html` to your repository.
2. Go to **Settings**, then **Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select your branch (usually `main`) and the `/ (root)` folder, then click **Save**.
5. After a minute, your calculator is live at `https://<your-username>.github.io/<your-repo>/`.

## Customize

All styling lives in the `<style>` block at the top of `index.html`. The colors and fonts are defined as variables in the `:root` section, so you can change the whole look by editing a few values (for example `--accent` for the equals key and `--op` for the operator keys).

Fonts (DM Mono and DM Sans) load from Google Fonts. If you are offline, the calculator falls back to your system fonts and works the same.

## Project structure

```
.
├── index.html   # the entire app: markup, styles and logic
└── README.md    # this file
```

## Browser support

Any current version of Chrome, Edge, Firefox or Safari.

## License

Add a license of your choice (for example MIT) before publishing. If you are unsure, GitHub can add one for you from **Add file**, then **Create new file**, then name it `LICENSE`.

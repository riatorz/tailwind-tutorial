# Tailwind Tutorial
This is a tutorial for Tailwind CSS.

## Installation
After download [Nodejs](https://nodejs.org/en/download/) and npm, run the following command to install Tailwind CSS:

```bash
npm install -D tailwindcss
```
Initialize Tailwind CSS:
```
npx tailwindcss init
```
After that, you will see a file named `tailwind.config.js` in your project directory.
For configure template paths and purge unused styles, you can edit the file `tailwind.config.js` as follows:
```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
Add the Tailwind directives to your CSS file:
If you don't have a CSS file, you can create a new file named `styles.css` in your **src** folder.
```css
/*./src/styles.css*/
@tailwind base;
@tailwind components;
@tailwind utilities;
```
Start the Tailwind CLI build process:
```bash
npx tailwindcss -i ./src/styles.css -o ./dist/output.css
```
After all the steps above, you will see a file named `output.css` in your **dist** folder. And folder structure is as follows:
```
.
├── dist
│   ├── output.css
├── src                    # Source folder
│   ├── examples            # different example pages
│   │  ├── header.html          # Header example
│   │  ├── navbar-header.html   # Navbar example
│   │  ├── navbar-page.html     # Navbar1 example
│   │  ├── page1.html           # Page
│   ├── index.html  # Basic Html file
│   ├── styles.css  # Css Input file
└── 
```
### All done! You can now use Tailwind CSS in your project. Start open index.html in your browser to see the result!
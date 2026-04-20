#  Mystery Shop Roulette

A chaotic, single-page web application that embraces the mystery of online shopping algorithms. No recommendations, no curated lists — just random search queries thrown into the void.

**[Try it →](https://kanrog.github.io/shop-roulette/)**

##  What's New in v1.1
The project has evolved from generating random product IDs (which often resulted in dead links) to generating **randomized search queries**.

* **Customizable Word List:** Searches are pulled dynamically from a `words.txt` file.
* **Multi-Store Support:** You can now choose to search on **AliExpress**, **Amazon**, or let the app pick **Randomly** between the two.
* **1-Word & 2-Word Modes:** Press "1-Word Search" for broad chaos, or "2-Word Search" to combine two random concepts for highly specific, weird results.
* **Persistent Stats:** The site remembers your roll count and last generated search across sessions using cookies.

##  How it Works

The page reads from an external text file (`words.txt`) using the JavaScript `fetch()` API. When you click a button, it grabs random words from the list, constructs a search URL for the selected marketplace, and redirects your current tab.

### Running Locally
Because the app uses `fetch()` to read the `words.txt` file, opening `index.html` directly from your hard drive (`file:///`) might be blocked by your browser's CORS/security policies.

**To test locally:**
1. Use a local server (e.g., VS Code Live Server, or run `python -m http.server` in your terminal).
2. Or simply host it on **GitHub Pages** — it works perfectly out of the box!

*(Note: There is a small fallback array of words hardcoded into `index.html` just in case the text file fails to load).*

##  Customization

You can easily customize the pool of random words!
1. Open `words.txt`.
2. Add, remove, or change the words.
3. Keep it to **one word or short phrase per line**.
4. Save and deploy. The app will automatically read the updated list.

##  Aesthetics
The UI features a stylized, cyber/synthwave aesthetic with CSS grid noise, ambient background glows, and a simulated terminal ticker to give it that "hacking the mainframe" feel before tossing you into a storefront.

##  Disclaimer
I am an AliExpress affiliate, but this specific site and the links it generates **do not append any affiliate tracking codes**. I receive no financial incentive from the randomized redirects. 

The site and tool is not affiliated with, endorsed by, or related to AliExpress, Amazon, or Alibaba Group in any way. Pure fun, no warranty, just vibes.

# Hack Nerd Font for ChromeOS hterm

## How to use

1. Open hterm and press Ctrl+Shift+J to open the developer console for your terminal
2. Paste the following JavaScript into the console
3. Profit

```javascript
term_.prefs_.set(
  "user-css",
  "https://cdn.jsdelivr.net/gh/Lillecarl/fontastic@main/style.css",
);
term_.prefs_.set("font-family", '"hack", monospace');
```

## How to make this yourself

1. Create a GitHub repo and clone it to your developer environment
2. Install woff2 tools in your developer environment (`nix shell nixpkgs#woff2` works)
3. Go to [NerdFonts.com](https://nerdfonts.com) and copy the download URL for your favorite font.
4. Download the font into your repository
5. Run woff2_compress on the font variant you want to use (probably regular)
6. Create a css file like the one in this repo
7. Commit your woff2 file and your css file, push
8. Browse to your stylesheet on github.com, copy the link into https://www.jsdelivr.com/GitHub
9. Use the jsdelivr link in `term_.prefs_.set("user-css", "url");`

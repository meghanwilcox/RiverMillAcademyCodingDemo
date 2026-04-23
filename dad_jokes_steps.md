# 🎤 Dad Joke Generator — Step-by-Step Guide
### For students following along in the workshop!

---

## 🗂️ What You Have
- **`dad_jokes_worksheet.html`** — Open this file. This is YOUR file to work in.
- **`dad_jokes_complete.html`** — The finished version. Peek if you get stuck!

Open `dad_jokes_worksheet.html` in:
1. A **text editor** (VS Code, Notepad, TextEdit) to edit the code
2. A **browser** (Chrome, Firefox) to see it working

Every time you make a change and save the file, refresh the browser to see it!

---

## ✏️ The Blanks — What to Type Where

There are **6 blanks** (BLANK A through BLANK F) in the `<script>` section of your file.
Find each comment like `// BLANK A` and replace the `"_________"` with the correct answer below.

---

### BLANK A — `"joke-text"`

**Find this line:**
```js
const jokeText = document.getElementById("_________");  // BLANK A
```
**Replace with:**
```js
const jokeText = document.getElementById("joke-text");
```
**Why?** We're telling JavaScript to find the `<p>` tag in the HTML that has `id="joke-text"`. That's where the joke will appear.

---

### BLANK B — `"joke-btn"`

**Find this line:**
```js
const jokeBtn = document.getElementById("_________");  // BLANK B
```
**Replace with:**
```js
const jokeBtn = document.getElementById("joke-btn");
```
**Why?** Same idea — we're grabbing the button so we can listen for when it gets clicked.

---

### BLANK C — `"Loading..."`

**Find this line:**
```js
jokeText.textContent = "_________";  // BLANK C
```
**Replace with:**
```js
jokeText.textContent = "Loading...";
```
**Why?** Fetching from the internet takes a tiny bit of time. We swap the text to "Loading..." so the user knows something is happening. You can actually write whatever you want here — try something funny!

---

### BLANK D — `json`

**Find this line:**
```js
const data = await response._________();  // BLANK D
```
**Replace with:**
```js
const data = await response.json();
```
**Why?** The API sends us back raw text. `.json()` converts it into a real JavaScript object so we can use `data.joke`. JSON stands for JavaScript Object Notation — it's how apps share data on the internet.

---

### BLANK E — `joke`

**Find this line:**
```js
jokeText.textContent = data._________;  // BLANK E
```
**Replace with:**
```js
jokeText.textContent = data.joke;
```
**Why?** The API sends back an object that looks like this:
```json
{
  "id": "abc123",
  "joke": "Why don't scientists trust atoms? Because they make up everything!",
  "status": 200
}
```
So `data.joke` is how we grab just the joke text out of that object.

---

### BLANK F — `"click"`

**Find this line:**
```js
jokeBtn.addEventListener("_________", getDadJoke);  // BLANK F
```
**Replace with:**
```js
jokeBtn.addEventListener("click", getDadJoke);
```
**Why?** `addEventListener` watches for something to happen. We tell it to watch for a `"click"` event, and when it happens, call our `getDadJoke` function. Other events exist too — like `"mouseover"` (hovering) or `"keydown"` (pressing a key).

---

## ✅ Check Your Work

Once all 6 blanks are filled in:
1. **Save** the file
2. **Refresh** the browser
3. Click the **"Get a Joke!"** button
4. A dad joke should appear! 🎉

If it doesn't work, open **DevTools** in Chrome:
- Press `F12` or right-click the page → "Inspect"
- Click the **Console** tab
- Red text = an error with a clue about what's wrong

---

## 🚀 Bonus Challenges (if you finish early!)

Try these on your own — there's no single right answer!

1. **Change the loading message** (BLANK C) to something funnier, like `"Finding the world's worst joke... 🥁"`
2. **Add a joke counter** — display how many jokes you've fetched so far
3. **Add a second button** that copies the joke to your clipboard using `navigator.clipboard.writeText()`
4. **Change the button color** in the CSS when a joke is loading so users know to wait
5. **Try a different free API** — `https://official-joke-api.appspot.com/random_joke` works the same way!

---

## 💡 Key Concepts You Just Used

| Concept | What it does |
|---|---|
| `document.getElementById()` | Finds an HTML element by its `id` |
| `.textContent` | Gets or sets the text inside an element |
| `async` / `await` | Lets JavaScript wait for slow things (like the internet) |
| `fetch()` | Makes a request to a URL, like a browser loading a webpage |
| `.json()` | Converts raw API response into a usable JS object |
| `addEventListener("click", fn)` | Runs a function when something is clicked |
| `try / catch` | Handles errors gracefully instead of crashing |

---

*Great work! You just used JavaScript to talk to the internet. That's literally how every app you use every day works. 🌐*
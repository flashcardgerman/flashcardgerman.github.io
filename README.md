# DeutschLern — German Flashcards (HTML, CSS, JavaScript)

A browser-based flashcard app for learning German vocabulary with Ukrainian translations. It uses spaced repetition to schedule reviews. Built entirely with HTML, CSS, and vanilla JavaScript. It includes 250 words across CEFR levels A1–C1, and you can create your own decks, track your learning streak, and monitor progress per level. No frameworks or build tools required!

## 📊 Features

  * 250 built-in German words across 5 levels: **A1, A2, B1, B2, C1** (50 words each) 📚
  * Ukrainian translations with German example sentences for every word 🇺🇦🇩🇪
  * Spaced repetition based on an adapted **SM-2 algorithm** 🧠
  * Four-level answer rating: Again, Hard, Good, Easy 🎯
  * Smart study queue: due cards first, then up to 20 new cards per session ✨
  * Failed cards are re-inserted later in the same session for extra practice 🔁
  * 3D card-flip animation 🃏
  * Create custom decks with bulk card import (`German | translation | example`) ➕
  * Delete custom decks along with their progress 🗑️
  * Word list with filtering by level and mastery indicators (0–5 dots) 📝
  * Statistics dashboard: total cards, learned, reviewed, accuracy, study days 📊
  * Daily streak tracking with a 30-day activity calendar 🔥
  * Per-level progress bars 🏆
  * Keyboard shortcuts for fast studying ⌨️
  * Swipe gestures on touch devices 👆
  * Auto-save progress to local storage 💾
  * Responsive dark-themed design for desktop, mobile, and landscape mode 📱
  * Custom favicon and SEO meta description 🌐

## 🚀 Getting Started

### Run Locally

1.  Clone this repository:

    ```bash
    git clone https://github.com/deutschlern/deutschlern.github.io
    ```

2.  Navigate to the project folder:

    ```bash
    cd deutschlern.github.io
    ```

3.  Open `index.html` in your browser.

That's it! No build tools or server required.

## Online Demo

You can also use the application directly via GitHub Pages:
[https://deutschlern.github.io](https://deutschlern.github.io)

> Replace the repository URL and demo link with your own GitHub username/repository if different.

## 📁 Project Structure

```
index.html        # Main application (HTML, CSS & JS)
```

## 📖 How It Works

1.  **Choose a deck** on the **Колоди** (Decks) tab. Select a built-in A1–C1 deck or create your own.
2.  **Study cards** on the **Навчання** (Study) tab. Each card shows a German word; tap or click it to see the translation and an example sentence.
3.  **Rate your answer**:
    * 😟 **Знову** (Again): you didn't remember. The card resets and comes back later in this session.
    * 😐 **Важко** (Hard): you remembered with difficulty. The card gets a shorter interval.
    * 😊 **Добре** (Good): you remembered correctly. The card gets the normal interval.
    * 🤩 **Легко** (Easy): you remembered effortlessly. The card gets a longer interval.
4.  **Browse all words** on the **Слова** (Words) tab and filter them by level.
5.  **Track progress** on the **Статистика** (Statistics) tab, including your streak calendar and per-level mastery.

### Creating a Custom Deck

Click **➕ Нова колода** and enter one card per line in this format:

```
Hallo | привіт
Welt | світ | Die Welt ist schön.
Buch | книга
```

The third part (example sentence) is optional.

### Spaced Repetition Logic

  * **First successful review** → next review in 1 day
  * **Second successful review** → next review in 6 days
  * **Subsequent reviews** → previous interval × ease factor (starting at 2.5, minimum 1.3)
  * **Easy** multiplies the interval by 1.3; **Hard** multiplies it by 0.6
  * **Again** or **Hard** resets the repetition count
  * A word counts as **learned** after 3 or more successful repetitions

### ⌨️ Keyboard Shortcuts

| Key               | Action      |
| ----------------- | ----------- |
| `Space` / `Enter` | Flip card   |
| `1`               | Again       |
| `2`               | Hard        |
| `3`               | Good        |
| `4`               | Easy        |

### 👆 Touch Gestures

Swipes work after the card has been flipped:

  * **Swipe right** → Good
  * **Swipe left** → Again

## 💻 Technologies Used

  * **HTML5** for structure
  * **CSS3** for layout, 3D flip animations, and the dark theme
  * **JavaScript (ES6)** for the spaced repetition logic and UI
  * **[Inter](https://fonts.google.com/specimen/Inter)** font via Google Fonts
  * **LocalStorage API** for saving progress

## 📄 License

This project is released under the MIT License. Feel free to use, modify, and distribute.

## 🙏 Acknowledgments

Built to help Ukrainian speakers learn German vocabulary through daily practice and scientifically proven spaced repetition techniques. Viel Erfolg beim Deutschlernen! 🇩🇪

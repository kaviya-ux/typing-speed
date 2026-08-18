# ⌨️ Typing Speed Test

A single-file typing speed test built with HTML, Tailwind CSS, and vanilla JavaScript. Type the given sentence within 60 seconds and see your live WPM (words per minute) and accuracy.

## Features

- 60-second countdown timer
- Random sentence picked from a small text pool each time you start/restart
- Live WPM (words per minute) calculation
- Live accuracy percentage as you type
- Character-by-character feedback: correct characters turn green, incorrect ones are highlighted red, and the current character is underlined
- Auto-finishes the test early if you type the full sentence before time runs out
- Restart button to reset everything and get a new sentence

## Tech Stack

- HTML5
- [Tailwind CSS](https://tailwindcss.com/) (via CDN)

## How It Works

- A random sentence is split into individual `<span>` characters and rendered in the text box.
- As the user types in the `<textarea>`, each typed character is compared against the corresponding character in the sentence, and Tailwind classes (`text-green-600`, `text-red-600 bg-red-100`, `border-b-2 border-blue-600`) are toggled with `classList` to show correct, incorrect, and current-position feedback.
- WPM is calculated as `(correct characters / 5) / (elapsed minutes)`, the standard "5 characters = 1 word" approximation.
- Accuracy is `(correct characters / total typed characters) * 100`.
- The test ends either when the 60-second timer hits zero or when the user finishes typing the full sentence.

## Possible Improvements

- Add difficulty levels (short/medium/long paragraphs)
- Add a "best score" tracker using localStorage
- Support custom typing duration (30s / 60s / 120s)
- Add sound effects for correct/incorrect keystrokes

## License

Free to use for learning or personal projects.

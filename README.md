# Replit-Sight-Words-Reading-Practice-App
 kid-friendly web app called "Sight Words Practice" to help my elementary-age child (grades K-5)
Sight Words Practice
A hands-free reading practice app for elementary-age kids (grades K–5). The child reads a sight word out loud, the browser's built-in speech recognition automatically checks whether she said it correctly, and she gets a score with color-coded feedback at the end of each round — no manual grading, no accounts, no saved data.
What it does
Grade selector (K–5): Pick a grade level before starting a round. Word banks are sourced from the standard, publicly published Dolch word lists (Pre-Primer, Primer, 1st, 2nd, 3rd grade, plus the Dolch noun list) for grades K–3, and Fry's Instant Words (4th–5th hundred and beyond) for grades 4–5.
5-word rounds: Each round presents 5 words, one at a time, in large kid-friendly text.
Microphone-based scoring: Tap the mic button, read the word aloud, and the app uses the Web Speech API (SpeechRecognition / webkitSpeechRecognition) to automatically compare what was said to the target word — no parent needs to click a confirm button.
Hidden scoring until the round ends: Individual results aren't revealed word-by-word; the score and color-coded review (green = correct, orange/red = needs practice) only appear after all 5 words in the round are attempted.
Nothing is saved: No localStorage, cookies, database, or login. Each round's score is shown only for that round — refreshing or starting a new round doesn't carry anything over.
Read-aloud hint: A speaker button next to each word uses SpeechSynthesis to read the word aloud as a pronunciation hint.
Celebration feedback: Light animation/sound on correct answers and on a perfect round, to keep it encouraging.
Tech stack
Single-page app — HTML/CSS/JavaScript (or React, depending on what Replit generated)
Browser-native Web Speech API for both speech recognition and text-to-speech
No backend, no database — fully stateless, client-side only
Browser support
Speech recognition works best in Chrome-based browsers. Safari's support for SpeechRecognition is limited/inconsistent, so Chrome is recommended for the smoothest experience. The app should show a friendly fallback message if the browser doesn't support it.
Running it
This app was generated on Replit from a detailed build prompt. To run it:

Open the project on Replit and click Run.
Grant microphone access when prompted by the browser.
Pick a grade level and start practicing.
Word list sources
Dolch Sight Words — a classic, widely used list of high-frequency words for early readers (Pre-Primer through 3rd Grade, plus a noun list), first published by Edward William Dolch. Public domain.
Fry's Instant Words — Dr. Edward Fry's list of the most frequently occurring words in English texts, commonly used through upper elementary grades. Public domain.
Possible future enhancements
Optional progress tracking across sessions (which words need more practice over time)
A manual override in case speech recognition mishears a word
Ability to add custom word lists (e.g., words sent home by a teacher)
Adjustable round size (currently 5 words)
Project background
This app was scoped and its build prompt drafted collaboratively, then built on Replit. See PROMPT.md in this repo (or the original prompt document) for the exact specification used to generate the app.

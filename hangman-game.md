# 🕹️ Hangman Riddle — Sarcastic Geeks Trybe

A simple yet engaging Hangman-style word guessing game with hints and scoring, challenges players to guess a hidden word based on a given hint. If the player makes too many incorrect guesses, the game is lost.

A letter... a guess... a life on the line.  
Can you outwit the riddle and survive the noose?

**Hangman Riddle** is a daily word-guessing game where you test your vocabulary, logic, and luck — one letter at a time.

---

This version includes:

- Trybe Authentication (users must be logged in to play).
- Daily score tracking.
- One score submission per user per day.
- Clean responsive UI with keyboard interaction.

---

## 🚀 How to Play

1. **Login or Sign Up**
   - You must be authenticated to play.
   - The auth overlay appears if you're not signed in.

2. **Gameplay**
   - You are shown a hint for a hidden word.
   - Click on letters from the on-screen keyboard to guess.
   - Correct guesses reveal letters in the word.
   - Wrong guesses count towards game over (max 7 tries).

3. **Scoring**
   - If you guess the word, you win and your score is the number of letters in the word (e.g. "Rainbow" = 7 points).
   - You can claim this score once per day by clicking **Claim Score**.
   - After claiming, you won’t be able to submit again for that day.

4. **Daily Limits**
   - You can only play and claim one Hangman score per calendar day.
   - If you already submitted a score today, you’ll see a notice and the Claim button will be hidden.

---


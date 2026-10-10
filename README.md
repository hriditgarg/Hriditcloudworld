# HriditSnake

A browser-based Snake game. Create an account or log in before starting a game.
Completed scores, the best score, and games played are saved per account in this
browser and remain available after reload.

## Account and score storage

This project is a static site with no server or database. Account records and
scores are stored in the browser's `localStorage`; passwords are stored only as
salted PBKDF2-SHA-256 hashes. Use the same browser and device to access saved
accounts. Clearing site data removes them. These local accounts are not
server-backed authentication and do not sync across devices; anyone with access
to this browser profile can alter the saved data. Do not use a sensitive or
reused password. Serve the site over HTTPS (or localhost) for Web Crypto
password hashing.

## Terms and conditions

Players must agree to the terms shown when opening the game. Agreement is
remembered in this browser; choosing "I disagree" keeps the game locked. The
terms explain that locally stored accounts and scores cannot be recovered or
secured by the game owner if the browser profile is compromised. This local
agreement prompt is not a security mechanism or a substitute for legal advice.

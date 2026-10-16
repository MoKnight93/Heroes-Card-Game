# Choose Your Squad | Card Battle

An interactive, browser-based hero card battle game. Build a squad of up to 3 heroes from **Marvel**, **DC** and **Mortal Kombat**, discover hidden team bonuses, and fight turn by turn using a rock-paper-scissors move system.

Everything is one `index.html` file (HTML, CSS and vanilla JavaScript). No build step, no frameworks, no backend.

- Interactive and entertaining
- 100% ad-free
- No tracking, no accounts, no payments
- **Made for fun. Not commercial. No money is made from this project.**

---

## Run it

1. Put `index.html` and the `Assets/` folder together (portraits are loaded from `./Assets/Images/Model Portraits/`).
2. Open `index.html` in any modern browser.

If a portrait is missing, the game shows the hero's initials instead, so it still works.

Progress (best run and discovered teams) is saved in your browser's `localStorage`. Nothing is sent anywhere.

---

## How the card game works

### Game modes

| Mode | What it is |
|---|---|
| **Single Match** | You are P1, the computer is P2. Pick 1 to 3 heroes for each side, then fight one match. |
| **Dual Mode** | Build a team of 1 to 3 and survive a **run of 10 matches** against random enemy teams that get harder as you win. Lose once and the run ends. After match 10 you can keep going in **Endless** mode. |

### Building a squad

- Choose 1 to 3 heroes per side. You can filter the roster by Marvel, DC or Mortal Kombat.
- Each hero card has four stats:
  - **STR**: offensive power
  - **ABL**: skills and powers
  - **DEF**: durability (reduces damage taken)
  - **HP**: stamina and total health
- Attack power is calculated as `STR × 0.55 + ABL × 0.45`.

### Fighting: one hero duel at a time

Heroes fight in order, one against one. When a hero is knocked out (K.O.), the next card on that side steps in. The side that runs out of heroes loses.

### Moves: rock, paper, scissors

Every round you choose a move, and the enemy secretly chooses one too.

- **Strike** beats **Power Move**
- **Power Move** beats **Guard**
- **Guard** beats **Strike**

Damage multipliers (your damage / damage you take):

| You ↓ / Enemy → | Strike | Power Move | Guard |
|---|---|---|---|
| **Strike** | ×1 / ×1 | ×1.25 / ×0.6 | ×0.4 / ×0.8 |
| **Power Move** | ×0.6 / ×1.25 | ×1.7 / ×1.7 | ×1.4 / ×0.35 |
| **Guard** | ×0.8 / ×0.4 | ×0.35 / ×1.4 | ×0.3 / ×0.3 |

Extra rules:

- **Power Move** hits hard but **misses 35%** of the time. Strike and Guard miss 10%.
- **Guard** heals **4% of max HP** each round (if the hero is still alive).
- Any hit can be a **critical hit**: 15% chance, ×1.8 damage.
- Damage also has a random spread (about ±30%) and is reduced by the target's DEF.
- The enemy picks moves based on its stats: strong hitters lean toward Power Move, tough heroes lean toward Guard. This is not shown to the player.

### Team bonuses (Team Dex)

Put the right heroes together to discover **hidden teams**. A team gives a power and HP bonus to every hero on your side. A team needs 2 or more members, and **only the strongest bonus counts**. Discovered teams are saved in the in-game **Team Dex**; undiscovered ones show as locked.

Teams in the game: Fantastic Four, Avengers, West Coast Avengers, X-Men, X-Force, Guardians of the Galaxy, Asgardians, Cap & Bucky, Justice League, Teen Titans, Bat Family, Earthrealm Defenders and Shaolin Monks.

### The 10-match run (Dual Mode)

| Matches | Level | Enemy stat boost | Enemy team size |
|---|---|---|---|
| 1 to 4 | Normal | none | 1 to 2 |
| 5 to 6 | Hard | +4% | 2 to 3 |
| 7 to 8 | Harder | +8% | 3 |
| 9 | Legendary | +14% | 3 |
| 10 | **Final Boss** | +14% | the 3 strongest heroes |
| 11+ | Endless | +14%, then +3% more every match | 3 |

Your best run (matches cleared) is saved in your browser.

### Controls

- **Autoplay**: the game picks Strike for you every round.
- **1× / 2× / 4×**: animation speed.
- **Skip**: instantly finish the current fight.
- **Auto next** (Dual Mode): automatically start the next match after a win.

---

## Legal notice, licenses and credits

**This is a free, non-commercial fan project made only for fun and entertainment.**

- It is not affiliated with, endorsed by, sponsored by, or approved by Marvel, Disney, DC, Warner Bros. Entertainment, Warner Bros. Games, NetherRealm Studios, or any other rights holder.
- The project contains **no ads**, takes **no donations**, sells nothing, and earns **no income** of any kind.

### Third-party characters and artwork

All characters, names, likenesses, portraits and related imagery shown in this game belong to their respective owners. They are **not** covered by any license I could give, and nothing in this repository grants you rights to them.

| Franchise | Owner / rights holder |
|---|---|
| Marvel characters (Spider-Man, Thor, Hulk, Iron Man, Wolverine, Deadpool, etc.) | © Marvel / The Walt Disney Company. Marvel and its characters are trademarks of Marvel Characters, Inc. |
| DC characters (Batman, Superman, The Flash, Joker, Green Lantern, etc.) | © DC Comics / Warner Bros. Discovery. DC and its characters are trademarks of DC Comics. |
| Mortal Kombat characters (Scorpion, Sub-Zero, Raiden, Liu Kang, etc.) | © Warner Bros. Games / NetherRealm Studios. Mortal Kombat is a trademark of Warner Bros. Entertainment Inc. |
| Character portraits from *Injustice 2* and other game or film sources | © their respective studios and publishers |

Hero stats in the game (STR, ABL, DEF, HP) and team bonuses are my own fan-made, unofficial numbers, loosely inspired by how strong each character is in the comics, films and games.

### Fair-use / fan-work statement

This project is a non-profit, transformative fan work. Using characters and images this way **does not give me ownership of them**, and a disclaimer does not replace permission from the rights holders. If you are a rights holder and want any asset removed, please open an issue or contact me and I will take it down promptly.

### My code

The game code (HTML, CSS, JavaScript) is original work. Please do not redistribute the third-party artwork, and do not use this project commercially.

### Fonts

[Bangers](https://fonts.google.com/specimen/Bangers) and [Barlow Condensed](https://fonts.google.com/specimen/Barlow+Condensed) are loaded from Google Fonts under the SIL Open Font License.


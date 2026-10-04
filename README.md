# Panelka

[Русская версия](README.ru.md)

A one-button browser game about reaction. A tower crane carries the floors of a panel apartment block, and you drop each one onto the stack with a single tap. The straighter you build, the taller the building gets.

A panelka is the everyday Russian word for a prefabricated panel apartment block.

**[Play in the browser](https://posoxai.github.io/PanelHouseBuildGame/)**

<p>
  <img src="screenshots/day.png" width="300" alt="Panelka by day with the Russian interface: a ten-floor building and the crane bringing the next floor">
  <img src="screenshots/night.png" width="300" alt="The same site in the dark theme with the English interface: night, with lit windows">
</p>

Left: the light theme with the Russian interface. Right: the dark theme with the English one.

## How to play

Tap the site or press Space (Enter works too) when the floor is over the building.

- Anything that overhangs the building is cut off, and the next floor is that much narrower.
- A floor dropped beside the building ends the game.
- A floor counts as straight when it lands almost exactly on the one below.

## Speed and width

- The crane speeds up one step for every three floors placed. The current step is shown under the floor counter.
- Three straight floors in a row win back some width. Each further straight floor in the run wins back a little more, until the building is back to its starting width.
- If a piece was cut off before that run, the third straight floor also takes the speed down one step. This happens once per cut.
- When that drop falls on a scheduled speed-up, the two cancel out and the speed stays the same.

## Ranks

A finished building gets a rank by its number of floors.

| Floors | Rank |
| --- | --- |
| 0 | Foundation pit |
| 1–4 | Unfinished |
| 5–8 | Khrushchyovka |
| 9–11 | Nine-storey block |
| 12–15 | Twelve-storey block |
| 16–24 | Sixteen-storey block |
| 25–39 | High-rise |
| 40 and more | Skyscraper |

The ranks are the everyday Russian names for standard apartment blocks. A khrushchyovka is the low-rise type built in the Khrushchev years, usually five storeys.

A floor in the game is 2.7 m tall, so the building's height in metres is shown next to the score.

## Language

The interface is in English and Russian. It opens in Russian when Russian is among the browser's languages and in English otherwise. The RU/EN switch remembers your choice.

## How to run

The whole game is one file, `index.html`. There is no build step and there are no dependencies.

- Locally: open `index.html` in a browser.
- Online: the game is published with GitHub Pages at https://posoxai.github.io/PanelHouseBuildGame/. Every commit to `main` updates it automatically.

Fonts load from Google Fonts. Without a network the game falls back to system fonts.

The best score and the sound setting are kept in the player's browser. The light theme draws the building by day and the dark theme by night, with lit windows.

## Credits

The game was designed, drawn and written by Claude, the AI assistant made by Anthropic: the mechanics, the canvas graphics, the sound and the page design.

The idea of making a browser game and the speed rules (a step every three floors, and the drop after three straight floors) came from posoxAI.

## License

MIT. The full text is in [LICENSE](LICENSE).

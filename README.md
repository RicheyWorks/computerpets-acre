# Acre

**Pet Farm Tycoon** — Farming simulator growing specialized crops and pet treats for the care loop.

Part of the [ComputerPets](https://github.com/RicheyWorks/computerpets) universe. Map: [computerpets-ecosystem](https://github.com/RicheyWorks/computerpets-ecosystem).

> Status: **design scaffold**. Gameplay contract is frozen. Engine choice is the one in the brief. Implementation comes next.

## Loop

Treats have to come from somewhere. Acre is the field: bamboo, brine-weed, pond cress. Crops buff species that canonically eat them.

## Genre & engine

- Genre: **Farming sim**
- Engine: **Unity**
- Stack: Unity 6 · C# · crop tables per biome · treats feed Kettle and overlay
- Default surface: `Unity editor`

## How you play

1. Plot grid. Plant biome-legal seeds.
2. Pets assigned as farmhands (idle).
3. Harvest → inventory → Kettle or feed.
4. Drought day from Quests seed.

## Talks to

- computerpets-kettle
- computerpets-lure
- computerpets-hearth
- computerpets-ledger
- computerpets-quests

## Failure doctrine

Wrong crop for species → wither, explain. Server down → local day continues, sync later. No microtransactions for rain.

Canon rules that never yield:

- 210 living kinds. No illegal hybrids.
- Overlay pets can get tired, sick, or hide. Tokens are not burned by a minigame.
- Desktop walk stays the main quest. Closing Acre must leave Rui walking.

## Layout

```
computerpets-acre/
  README.md
  LICENSE
  docs/DESIGN.md
  src/                implementation lands here
```

## Run (Windows)

```powershell
Unity Hub > Acre/; play mode.
```

Meet Rui first via the [flagship start-here](https://github.com/RicheyWorks/computerpets/blob/main/docs/START-HERE.md). This game is optional.

## License

MIT. See [LICENSE](LICENSE).

---

*Two hundred ten living kinds. Keep them so a line does not go quiet.*

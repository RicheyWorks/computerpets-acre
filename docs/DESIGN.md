# Acre design

Implement against this file, not folklore.

## Identity

- Product: **Acre**
- Repo: `computerpets-acre`
- Idea: Pet Farm Tycoon
- Genre: Farming sim
- Engine: Unity
- Surface: `Unity editor`

## Loop

Treats have to come from somewhere. Acre is the field: bamboo, brine-weed, pond cress. Crops buff species that canonically eat them.

## Play beats

- Plot grid. Plant biome-legal seeds.
- Pets assigned as farmhands (idle).
- Harvest → inventory → Kettle or feed.
- Drought day from Quests seed.

## Neighbors

- computerpets-kettle
- computerpets-lure
- computerpets-hearth
- computerpets-ledger
- computerpets-quests

## Failure doctrine

Wrong crop for species → wither, explain. Server down → local day continues, sync later. No microtransactions for rain.

## Hard rules

1. Minigames cannot mint or burn NFTs by themselves (Minter is the write path).
2. Stats come from lived overlay care + Dojo caps, not cash shop.
3. Species kits stay inside Lore. Illegal hybrids never spawn.
4. Fail soft: the desktop overlay process is not this process.

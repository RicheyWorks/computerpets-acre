# Acre

**Species-aware farming for ComputerPets.**

A planned farming game where biome-appropriate crops become treats for the pet care loop.

**Stage: design scaffold.** This checkout contains a design document and a source placeholder. The experience below is planned; there is no runnable app or integrated service yet.

[Status](#status) · [Planned experience](#planned-experience) · [Contributor quickstart](#contributor-quickstart) · [Game design](docs/DESIGN.md) · [Ecosystem map](https://github.com/RicheyWorks/computerpets-ecosystem)

## Status

| Available today | What you can inspect |
| --- | --- |
| [Game design](docs/DESIGN.md) | Intended behavior, boundaries, and planned dependencies. |
| [Source placeholder](src/Game.cs) | Empty C# class; no Unity project or scene is checked in. |
| [MIT license](LICENSE) | Licensing terms for the repository. |

Gameplay, endpoints, integration arrows, and failure handling on this page describe implementation targets. No build/test harness, CI workflow, or product screenshots are included in this scaffold.

## Planned experience

- Plot grid. Plant biome-legal seeds.
- Pets assigned as farmhands (idle).
- Harvest → inventory → Kettle or feed.
- Drought day from Quests seed.

### Planned technology

- Genre: **Farming sim**
- Engine: **Unity**
- Stack: Unity 6 · C# · crop tables per biome · treats feed Kettle and overlay
- Default surface: `Unity editor`

### Planned connections

These arrows show intended dependencies, rather than working integrations.

```mermaid
flowchart LR
  acre -->|crops| kettle
  acre -->|treats| overlay
  quests -->|drought| acre
```

## Contributor quickstart

With access to this private repository, Git and PowerShell are enough to review the scaffold:

```powershell
git clone https://github.com/RicheyWorks/computerpets-acre.git
Set-Location computerpets-acre
Get-Content docs/DESIGN.md
Get-Content src/Game.cs
```

Read [Game design](docs/DESIGN.md) before choosing implementation details. The commands above inspect the checked-in files; app installation, editor launch, and server startup become possible after a buildable project and entry point are added.

### First implementation target

**Bamboo plot, one harvest into feed inventory.**

You know it works when: Wrong crop withers with an explanation. Server down: local day continues.

Treat this as an acceptance target for a future implementation. Start with the documented slice, add the required project setup and focused tests, and update these instructions with commands that work from a fresh clone.

## Design boundaries

1. Minigames cannot mint or burn NFTs by themselves (Minter is the write path).
2. Stats come from lived overlay care + Dojo caps, not cash shop.
3. Species kits stay inside Lore. Illegal hybrids never spawn.
4. Fail soft: the desktop overlay process is not this process.

**Required failure behavior:**

Wrong crop for species → wither, explain. Server down → local day continues, sync later. No microtransactions for rain.

## Ecosystem

- [computerpets-kettle](https://github.com/RicheyWorks/computerpets-kettle)
- [computerpets-lure](https://github.com/RicheyWorks/computerpets-lure)
- [computerpets-hearth](https://github.com/RicheyWorks/computerpets-hearth)
- [computerpets-ledger](https://github.com/RicheyWorks/computerpets-ledger)
- [computerpets-quests](https://github.com/RicheyWorks/computerpets-quests)

Start with the [ComputerPets flagship](https://github.com/RicheyWorks/computerpets) for the desktop pet. This repository describes an optional extension; the [ecosystem map](https://github.com/RicheyWorks/computerpets-ecosystem) explains the broader plan.

## License

MIT. See [LICENSE](LICENSE).

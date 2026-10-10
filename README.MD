# The Dumpster Fire — Dhog Plugins

Dalamud plugins for FINAL FANTASY XIV: party coordination, duty and treasure-map runs, daily tasks, chocobo care, chat translation, local appearance changes, and gameplay utilities.

[Plugins and guides](https://aethertek.io/) · [Documentation](https://wiki.aethertek.io/) · [The Dumpster Fire community](https://discord.gg/ac6gjDvR8R) · [Support the plugins](https://ko-fi.com/mcvaxius)

## Installation

1. Install [XIVLauncher](https://github.com/goatcorp/FFXIVQuickLauncher), enable Dalamud in its settings, and launch the game through it.
2. Type `/xlsettings` in game chat, open **Experimental**, and find **Custom Plugin Repositories**.
3. Add **one** of the repository URLs below, click **+**, then **Save and Close**.
4. Type `/xlplugins`, find the plugin by its name below, and install it. Follow that plugin's setup guide before starting automation.

**Recommended: Aethertek's main repository**

```text
https://aethertek.io/x.json
```

**Alternative: this repository's plugin feed**

```text
https://raw.githubusercontent.com/McVaxius/TheDumpsterFire/master/pluginmaster.json
```

Use only one feed to avoid duplicate repository entries. The shared feed also carries XA and community plugins; [the XA collection has its own feature guide](https://github.com/xa-io/MyDalamudPlugins).

MOM, DhogNav, and Deep Ducking have free public hosts with separately granted functionality. Installing a host or supporting the project does not grant private access. Footballer's availability is also arranged through the community.

## Find a plugin

| Plugin | What it does |
| --- | --- |
| [Fren Rider](#fren-rider) | Follow a configured party member and coordinate mounts, combat, and duty automation. |
| [Loot Goblin](#loot-goblin) | Manage treasure-map queues, coffers, portals, and treasure-dungeon runs. |
| [M.O.G.T.O.M.E.](#mogtome) | Farm supported duties and manage Moogle Treasure Trove and Blunderville shopping. |
| [VERMAXION](#vermaxion) | Schedule daily and weekly tasks with settings for each character. |
| [AI Duty Solver](#ai-duty-solver) | Run supported duties and manage loot, desynthesis, and vendor shopping. |
| [DAD](#dad) | Prepare crews, form parties, queue duties, and run ordered schedules. |
| [HealBot / Coppelia](#healbot--coppelia) | Heal watched targets, combine healing with damage, or pair a helper with another character. |
| [BFE](#bfe) | Farm Eureka Pyros bunny FATEs and treasure coffers. |
| [Choke-abo](#choke-abo) | Buy and feed racing-chocobo training food and execute breeding progression. |
| [Chocobo Colourized](#chocobo-colourized) | Plan and automate fruit feeding for a companion chocobo's colour. |
| [Hello Fellow Human](#hello-fellow-human) | Create proximity and emote-triggered reactions. |
| [DhogGPT](#dhoggpt) | Translate incoming chat and compose translated outgoing messages. |
| [Dheacon](#dheacon) | Play alerts and locally generated spoken commentary. |
| [Krangler](#krangler) | Change supported name displays and appearances locally. |
| [Thick Thighs Save Lives](#thick-thighs-save-lives) | Keep essential character and party state visible in a local or web HUD. |
| [Dhog Potato System](#dhog-potato-system) | Reduce crowd visibility and control game rendering on weaker machines. |
| [Botology](#botology) | Review plugin compatibility, overlap warnings, and installed-plugin controls. |
| [Footballer](#footballer) | Display privacy-aware party foot showcases from character previews. |
| [MOM](#mom) | Configure supported PvP sessions with separately granted access. |
| [DhogNav](#dhognav) | Browse and manage a private location address book. |
| [Deep Ducking](#deep-ducking) | Manage supported deep-dungeon runs, saves, and item strategies with private access. |

## [Fren Rider](https://github.com/McVaxius/FrenRider)

Keep another character with a configured party member and coordinate the supporting automation. Open `/frenrider` or `/fr`.

- **Follow choices** — Use NavMesh, Visland, BossMod, or the game's normal follow, with separate overworld and duty preferences.
- **Spacing and formations** — Adjust follow distances, combat following, social spacing, and positions based on party slots.
- **Mount support** — Coordinate mounting, flying, passenger following, and catching up when the party spreads out.
- **Combat providers** — Integrate with BossMod Reborn, VBM, Rotation Solver Reborn, Wrath, or Daedalus, with per-character choices.
- **Everyday helpers** — Configure food, companion summoning and stance, FATE sync, job stones, repair, and post-duty desynthesis.
- **Duty coordination** — Hand supported duties to ADS under configurable conditions and delays, with party, run, and duty-owner status visible.

Select your party member and movement/combat providers in `/fr settings`. Install the providers you select; ADS is needed for delegated duties and its repair/desynthesis utilities. `/fr on` and `/fr off` control the active character's automation.

## [Loot Goblin](https://github.com/McVaxius/LootGoblin)

Organize and automate treasure-map runs from map selection through coffers and treasure dungeons. Open `/lootgoblin` or `/lg`.

- **Map queue** — Enable map types, choose run counts, and see the current map and remaining work.
- **Map sources** — Use inventory first, with optional saddlebag and retainer retrieval; XA Database supplies retainer information.
- **Coffers and portals** — Decipher maps, resolve treasure locations, open coffers, wait through combat, and handle portal entry.
- **Party coordination** — Wait for required party members, mount readiness, nearby players, and underwater readiness where applicable.
- **Treasure dungeons** — Delegate supported runs to ADS, including final-coffer collection before applying the selected exit behavior.
- **Optional map purchases** — Use Emptor after configured stock sources are exhausted, with a gil ceiling for each map and manually applied price suggestions.

Use `/lg settings` to select maps, party rules, and dependencies before `/lg on`. vnavmesh supports movement; ADS, XA Database, and Emptor are required for their respective optional features. Main provides Start, Pause/Resume, and Stop.

## [M.O.G.T.O.M.E.](https://github.com/McVaxius/MOGTOME)

**Management Of Grand Tome Operations & Management Engine** handles repeated duty farming and reward shopping. Open `/mogtome` or `/mog`.

- **Duty farming** — Queue and repeat The Praetorium and The Porta Decumana with saved run counters and reset handling.
- **Party setup** — Configure leader/member behavior and separate settings for each character through the setup wizard.
- **Combat and upkeep** — Select a combat provider and configure repairs, food, potions, mitigation, and limit breaks.
- **Run statistics** — Review completed runs and saved summaries, and choose to stop after the next successful run.
- **Moogle shopping** — Set desired inventory quantities for current event rewards, view costs and ownership, and buy outstanding quantities explicitly.
- **Blunderville** — Configure run or MGF limits, leader/member participation, and a separate reward shopping list with optional shopping after farming.

Start with `/mogtome config` and its Setup Wizard. ADS is the primary duty backend; AutoDuty is an alternative. Follow the project's required vnavmesh, combat-provider, XA Slave, YesAlready, and game-control setup. Blunderville must be unlocked before it can run.

## [VERMAXION](https://github.com/McVaxius/VERMAXION)

Run recurring tasks after AutoRetainer processing, manually, or through the saved task timer. Open `/vermaxion` or `/vmx`; settings belong to each account and character.

- **Gold Saucer tasks** — Configure Lord of Verminion, Mini Cactpot, Jumbo Cactpot, and chocobo racing on their own schedules.
- **Racing progression** — Choose ordinary racing or Choke-abo target-pedigree progression, with breeding mode, feed grade, gil/MGP reserves, feeding policy, and a saved daily racing allowance.
- **FC supplies** — Reconcile Seal Sweetener II stock, replenish the configured target, and separately opt in to activation.
- **Retainer equipment** — Upgrade eligible combat retainers by item level and gatherers by Perception.
- **Fishing** — Configure Ocean Fishing, AutoHook integration, bait stock, participating characters, and optional inventory cleanup.
- **Task control** — Order tasks before or after AutoRetainer, inspect due/blocked work, save favorites, run eligible tasks, cancel current work, or use FULL STOP.

Use `/vmx config` for character settings and task ordering. Each task shows its required plugins and setup state. AutoRetainer is needed for its processing hooks; Target Pedigree requires Choke-abo. `/vmx chocobo settings` opens the racing settings.

## [AI Duty Solver](https://github.com/McVaxius/ADS)

ADS executes supported instanced-duty routes while showing the current phase, objective, ownership, and blockers. Open `/ads`; entering a duty alone does not start ADS.

- **Duty controls** — Start outside or inside a duty, resume an interrupted run, and release ADS ownership with Stop.
- **Coverage overview** — Review the current duty and its supported behavior before choosing to run it.
- **Guided setup** — Configure duty behavior, interaction rules, utilities, and treasure/follow preferences through replayable setup flows.
- **Loot choices** — Configure loot handling, including an optional XA Database check for already-owned glamour equipment.
- **Inventory utilities** — Use desynthesis presets, skill-up filtering, and materia extraction controls.
- **Shop lists** — Preview vendor offers and saved item targets, choose refill or spending policies, and start supported purchases explicitly.

Main and `/ads mini` keep Start, Resume, and Stop accessible. Follow the project's operator guide for the dependencies and coverage of your chosen duty. `/ads loot` and `/ads desynth` open their respective utility controls.

## [DAD](https://github.com/McVaxius/dad)

Plan repeatable solo or multibox duty runs and coordinate the characters that should participate. Open `/dad`. [Player guide](https://github.com/McVaxius/dad/blob/main/DAD_AETHERTEK.md).

- **Reusable crews** — Save exact characters, requested jobs, roles, substitutes, and stop conditions, or instantiate a role-based template.
- **Preparation and readiness** — Check characters and required plugins, prepare requested gearsets, and wait for busy clients to become available.
- **Party formation** — Assemble and verify regular parties or supported alliance crews; Crew Tools can form a group without queueing.
- **Supported queues** — Run Duty Support, Trust, local or premade duties, eligible roulettes, and supported MOGTOME handoffs.
- **Ordered schedules** — Chain saved presets, set repeat counts, and run manually or at the daily reset; resume eligible failed schedules from their failed entry.
- **Visible control** — See readiness, queue state, reconnect progress, and blockers, with scoped cancellation and Stop All.

Multibox use needs one Coordinator and connected Client Dads using matching builds. Required plugins include Fren Rider, ADS, vnavmesh, XA Database, XA Slave, and a supported BossMod. Optional AutoParty provides separately arranged Discord-based registration and peer pairing; local DAD use remains available without it.

## [HealBot / Coppelia](https://github.com/McVaxius/Coppelia)

Heal explicitly watched targets, combine healing with damage, or assign a helper to another character. The installer name is **HealBot**; the project remains **Coppelia**. Open `/healbot` or `/hb` and use Quick Setup.

- **Watched-target healing** — Configure WHM, SCH, AST, or SGE healing for up to 20 friendly targets, including supported targets outside your party.
- **Raises and buffs** — Apply job-specific healing, raise, buff, and pre-buff rules from the same watched-target list.
- **Healer-first JOAT** — Jacqueline of All Trades gives healing priority, then uses Rotation Solver Reborn for eligible damage with DoTs-only or full-rotation choices.
- **Powerlevel support** — Use equipped BRD/MCH instant attacks against eligible damaged enemies already fighting the configured Fren or local character.
- **Helper/Newb roles** — Pair one authenticated helper with one connecting character; the Newb performs no local healing or attacking.
- **Questing assistance** — Integrate with Questionable Companion's helper assignment, watched-target healing, following, and optional passenger support.

Stand-alone healing needs Fren Rider, vnavmesh, and BossMod Reborn or VBM; JOAT additionally needs Rotation Solver Reborn. Direct pairing requires a matching pair-specific secret and a trusted network: its traffic is authenticated but not encrypted. The setup wizard explains the extra requirements for the chosen role.

## [BFE](https://github.com/McVaxius/BFE)

**Bunny Farm Eureka** automates the Pyros bunny-FATE and coffer loop. Open `/bfe` and configure the run before starting.

- **Pyros loop** — Run the supported bunny FATE workflow in Eureka Pyros.
- **Coffer hunting** — Follow the bunny treasure search and move toward the resulting coffer.
- **Session limits** — Choose continuous operation or a configured hours/minutes duration.
- **Repair options** — Enable repair support and choose the durability threshold and self-repair preference.
- **Retainer coordination** — Configure optional retainer, submarine, and AutoRetainer Multi Mode support.
- **Statistics** — Review session and saved totals for gil, coffer tiers, and tracked rare rewards.

The dependency panel identifies vnavmesh, Rotation Solver Reborn, and BossMod Reborn readiness. Pyros is the available run selection; the other displayed Eureka zones are not enabled. `/bfe settings` opens settings and `/bfe stop` stops the workflow.

## [Choke-abo](https://github.com/McVaxius/ChokeAbo)

Train and breed **racing chocobos**, with manual feeding controls and progression coordinated by VERMAXION. Open `/chokeabo`.

- **Training food** — Choose Grade 1, 2, or 3 feed for racing-chocobo training sessions.
- **Stock and bulk buying** — Use existing food first and purchase missing training supplies through the multi-buy workflow.
- **Breeding stock** — Review fledglings, retired parents, pedigree, sex, and remaining breeding capacity.
- **Parent choices** — Execute owned-parent breeding or use an opposite-sex NPC covering permit of the required pedigree.
- **Progression actions** — Coordinate retirement, covering, the 24-hour covering wait, collection, and registration with VERMAXION's target-pedigree settings.
- **Spending and feeding policy** — Respect gil/MGP reserves and choose Fall back, Skip, or Stop when feeding cannot proceed, with Pause/Resume/Stop for progression.

VERMAXION owns progression settings and the daily racing allowance; Choke-abo executes feeding and breeding. Pedigree and racing rank are separate values. Companion feather-colour changes use Chocobo Colourized instead.

## [Chocobo Colourized](https://github.com/McVaxius/ChocoboColourized)

Plan a fruit-feeding sequence for your **companion chocobo's feather colour**. This is separate from racing-chocobo training. Open `/chococolor`.

- **Colour selection** — Choose current and target colours from the available palette and inspect their swatches.
- **Feeding calculation** — Calculate the fruit sequence needed to move toward the selected colour.
- **Supply list** — See required fruit quantities and inventory requirements before feeding.
- **Save and copy** — Save the calculated plan for the current character or copy the results to the clipboard.
- **Feeding automation** — Feed the saved sequence from the stable's Feed inventory screen, retaining progress for a later continuation.
- **Colour timers** — Track the six-hour colour-change wait separately for each saved character and chocobo.

Stable the companion and have the required fruit available before starting. Follow the project's inventory-window setup instructions, including **Open All** and **Expanded**, so the feed items remain accessible.

## [Hello Fellow Human](https://github.com/McVaxius/HelloFellowHuman)

Build automatic social and roleplay reactions for nearby players using the game's normal commands and emotes. Open `/hfh`, or start Guided Setup with `/hfh wizard`.

- **Proximity reactions** — Respond when a specific player or any nearby player enters the configured range.
- **Emote reactions** — Trigger a response to a selected incoming emote with its own detection range.
- **COPYCAT** — Mirror incoming emotes and optionally provide a fallback command when mirroring is unavailable.
- **Rule timing** — Set delays, cooldowns, distance, weather requirements, and whether to target the triggering player.
- **Presets** — Keep multiple rule sets, switch between them, and import/export presets; guided edits stay in a draft until Finish.
- **Optional effects** — Apply temporary nameplate glow or launch configured local audio/video files from advanced rules.

`/hfh on` and `/hfh off` control reactions for the current account. The DTR entry can show the active preset and toggle reactions. Use trusted local media files and preset imports.

## [DhogGPT](https://github.com/McVaxius/DhogGPT)

Translate incoming chat and compose translated messages for the channel you choose. Open `/dhoggpt`, `/dgpt`, or `/dog`.

- **Incoming translation** — Translate selected chat channels in real time and print their translations to Echo.
- **Outgoing composer** — Translate and send to say, party, FC, linkshells, cross-world linkshells, shout, yell, and tells.
- **Language choices** — Select source/destination languages or use source-language autodetection.
- **Channel control** — Choose which incoming channels participate without translating all chat.
- **Providers** — Use the default translation service or configure LibreTranslate-compatible endpoints.
- **Reading tools** — Review recent history, use a compact chat view, and avoid repeated requests through duplicate suppression and a short-term cache.

The first-use guide helps select channels and languages. UI language is separate from translation language. Selected messages are sent to the configured translation provider.

## [Dheacon](https://github.com/McVaxius/dheacon)

Add classic sound alerts or preset-driven spoken commentary to supported game events. Open `/dheacon` and use Quick Setup.

- **Two modes** — Choose packaged sound alerts or spoken commentary.
- **Event selection** — Configure supported login, combat, idle, music, nearby-player, duty, crafting, and gathering events.
- **Local speech** — Use Piper or installed Windows voices; generated speech and playback stay on your computer.
- **Preset management** — Choose, duplicate, import, or export commentary presets and optional line packs.
- **Trigger tuning** — Adjust event toggles, trigger chance, cooldowns, voice choices, and reusable audio-cache limits.
- **Optional follower** — Request a local Imaginary Fren through Krangler while alerts and speech remain usable without that integration.

Piper requires a one-time runtime and chosen-voice download; Windows speech uses installed voices. `/dheacon on`, `/dheacon off`, and the DTR control enablement; `/dheacon say <text>` queues a manual line in spoken mode.

## [Krangler](https://github.com/McVaxius/Krangler)

Change supported names, chat, and appearances locally for screenshots and personal display. Open `/krangler` or `/kr`; `/kr wizard` opens guided setup.

- **Name and chat options** — Apply deterministic pseudonyms to supported name displays and independently enable chat garbling.
- **Appearance choices** — Randomize supported race, clan, gender, hair, face, eye, and other appearance fields.
- **Exact replacement rules** — Hide or replace selected race/clan/gender combinations, with an optional self exemption.
- **Presets** — Choose saved appearance presets and exact NPC replacement rules, or import compatible appearance data.
- **Soul Thief** — Capture supported looks from locally loaded players, NPCs, and chocobos as reusable presets.
- **Imaginary Fren** — Spawn an optional local follower with a selected name and preset.

Changes are local and are not synchronized to other players. Player Search, Friends List, and other unsupported surfaces can still show original names. Glamourer is not required. `/kr on` and `/kr off` control the master state.

## [Thick Thighs Save Lives](https://github.com/McVaxius/TTSL)

Keep essential character and party information visible when the normal game view is reduced. Open `/ttsl`; `/ttsl setup` starts guided setup.

- **Character snapshot** — See the current zone, coordinates, and character state.
- **Health and mana** — Keep HP/MP bars visible independently of the normal game HUD.
- **Conditions and equipment** — Monitor combat/duty flags and a repair summary.
- **Party overview** — Review party HP, mana, positions, and distance in one place.
- **Radar and labels** — Show party positions on a radar and optionally use krangled display names.
- **Local or web HUD** — Choose Local HUD, Local + Web, or Web only, with explicit settings for publication and permissions.

The web HUD uses a separately installed server. The [latest release](https://github.com/McVaxius/TTSL/releases/latest) provides `latestServer.zip` with the standalone Windows server; its setup guide covers the connection and permission choices.

## [Dhog Potato System](https://github.com/McVaxius/DPS)

Reduce crowd visibility and control rendering on weaker machines. Open its configuration from the Dalamud plugin installer; results depend on the system and selected options.

- **Crowd visibility** — Hide non-party players while retaining party members.
- **Companion visibility** — Hide pets, chocobos, and minions to reduce the visible crowd further.
- **Target exception** — Optionally keep the current target visible.
- **Rendering modes** — Choose foreground or background no-render modes.
- **Window and hotkeys** — Bind safety/mode hotkeys and save or restore the game window's position and size.
- **Restore controls** — Use **All Off** to return to normal rendering and visibility.

Choose visibility and rendering options in its settings before enabling them. Keep its restore controls accessible when using reduced rendering.

## [Botology](https://github.com/McVaxius/botology)

Review plugins that may overlap or interfere with one another, alongside their installed state and controls. Open `/botology`, `/bottist`, or `/botologist`.

- **Compatibility grid** — See tracked plugins, installed state, captured versions, and compatibility assessments together.
- **Overlap warnings** — Review conflicts and rule explanations, with configurable toast, popup, or window alerts.
- **Filtering and sorting** — Filter by category, plugin, or author, sort table columns, and choose optional columns.
- **Installed controls** — Enable or disable selected installed plugins and use best-effort DTR visibility switches.
- **Catalog links and notes** — Open repository links, inspect update availability, and read cached catalog patch notes.
- **Per-plugin exceptions** — Set ignore flags and inspect detail popups; the AI column is an attribution signal rather than proof of authorship.

Botology's Enabled switch controls assessment alerts. The grid's plugin-enable and DTR actions operate separately on the selected plugin.

## [Footballer](https://github.com/McVaxius/footballer)

Display a privacy-aware party-foot showcase using character preview captures. Access availability is arranged through the community. Open `/footballer` or `/foot`.

- **Party cards** — Browse the current party in character cards with a saved feet capture and capture status.
- **Lodestone privacy** — Hide feet when the character's face is unavailable on Lodestone.
- **Inspect captures** — Open character inspection and capture the available preview through explicit actions.
- **Pose and footwear** — Apply the preset inspect pose or choose preview-only **Without footwear**.
- **Preview scaling** — Save the CharacterInspect preview scale so captures match the window's actual size.
- **Refresh and labels** — Refresh party captures or Lodestone information and choose real or krangled display labels.

Preview-only footwear changes affect the local preview. The main window shows privacy and capture readiness before displaying the saved result.

## [MOM](https://github.com/McVaxius/mom-public)

Configure supported PvP sessions through separately granted MOM access. `/mom` opens the free public introduction or the installed authorized functionality.

- **Session routes** — Choose supported Casual Crystalline Conflict, Frontline, or Rival Wings routes.
- **Job and run setup** — Select the job and run count in the session controls.
- **Target preferences** — Configure MOM's priority-targeting choices.
- **Combat policy** — Tune burst and limit-break preferences.
- **Survival policy** — Configure Guard and Recuperate preferences.
- **Session status** — Monitor readiness in Main or Mini and use Start or Cancel Active Run.

All session features require separately granted access. Keep the public host installed and enabled, and follow the publisher's access instructions using Aethertek Plugin Manager. The authorized interface shows Rotation Solver and vnavmesh requirements.

## [DhogNav](https://github.com/McVaxius/dhognav-public)

Browse and organize a location address book through separately granted DhogNav access. `/dnav` opens the free public introduction or the installed authorized interface.

- **Two browsing views** — Use Compact browsing or Expanded mode for additional controls.
- **Area browsing** — Browse saved entries by their area.
- **Search** — Find entries in the expanded address book.
- **Editing and sharing** — Edit locations and import/export saved entries.
- **Filters and limits** — Configure duty, player, and territory filters, cooldowns, and timeouts.
- **Access and appearance** — Check installed access and save language, colour, spacing, and window-opacity preferences.

Address-book functionality requires separately granted access. Keep the public host enabled and follow the publisher's installation instructions through Aethertek Plugin Manager; **Check installed access** refreshes an installed package.

## [Deep Ducking](https://github.com/McVaxius/dduck-public)

Manage supported Palace of the Dead, Heaven-on-High, Eureka Orthos, and Pilgrim's Traverse workflows through separately granted DDuck access. Open `/dduck` or `/dd`.

- **Run setup** — Select a save, starting floor, finish condition, farming goal, and repeat behavior.
- **Save management** — Inspect current save slots, continue the selected save, and explicitly delete a selected slot while protecting the other slot.
- **Floor progression** — Coordinate room exploration, pulls, revealed-trap avoidance, and passage interactions.
- **Loot strategy** — Select chest types and collection timing, with party-leader coffer handling and personal final rewards.
- **Item strategy** — Configure pomander, potion, reserve, and boss-use preferences.
- **Run control** — Use Main or Mini for Hold, Resume, FULL STOP, or an exit after the next boss that retains the save.

Dungeon automation requires separately granted access and the required combat/navigation setup, including BossMod Reborn. The free host supplies access information and community links. FULL STOP persists across reloads; `/dd resume` is an explicit request to resume an eligible retained run.

## Support

- Join [The Dumpster Fire community](https://discord.gg/ac6gjDvR8R) and use its plugin discussion channels for setup help, access availability, and suggestions.
- Report bugs on the relevant public plugin repository, including the plugin version, the action you took, and the result you expected.
- Find the wider collection and guides at [aethertek.io](https://aethertek.io/), or [support the plugins on Ko-fi](https://ko-fi.com/mcvaxius).

Please enjoy the growing dumpster fire. 🔥

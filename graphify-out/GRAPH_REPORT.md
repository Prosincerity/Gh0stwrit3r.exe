# Graph Report - Gh0stwrit3r  (2026-09-09)

## Corpus Check
- 44 files · ~50,027 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 357 nodes · 520 edges · 30 communities (18 shown, 8 thin omitted)
- Extraction: 92% EXTRACTED · 8% INFERRED · 0% AMBIGUOUS · INFERRED: 44 edges (avg confidence: 0.85)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `ffa75abd`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- BeatPlayer
- ProjectStorage
- MainActivity.kt
- ProjectMetadata
- ProjectStorageTest
- WaveformViewport
- ProjectStorageBeatTest
- EditorScreen.kt
- WaveformExtractor
- Settings
- WaveformExtractorTest
- gradlew
- ExampleInstrumentedTest
- What You Must Do When Invoked
- Ghostwriter
- Task: DAW-style waveform view for BeatPlayer (replaces slider)
- Project handoff: Ghostwriter
- graphify reference: extra exports and benchmark
- Ghostwriter agent instructions
- graphify reference: query, path, explain
- graphify reference: add a URL and watch a folder
- graphify reference: commit hook and native CLAUDE.md integration
- graphify reference: incremental update and cluster-only
- graphify reference: GitHub clone and cross-repo merge
- graphify reference: transcribe video and audio
- extraction-spec.md

## God Nodes (most connected - your core abstractions)
1. `BeatPlayer` - 34 edges
2. `ProjectStorage` - 32 edges
3. `ProjectStorageTest` - 25 edges
4. `WaveformViewport` - 23 edges
5. `ProjectStorageBeatTest` - 21 edges
6. `BeatPlayerTest` - 21 edges
7. `ProjectMetadata` - 17 edges
8. `WaveformMarker` - 12 edges
9. `WaveformExtractor` - 12 edges
10. `EditorScreen()` - 12 edges

## Surprising Connections (you probably didn't know these)
- `EditorScreen()` --calls--> `ProjectInfoDialog()`  [INFERRED]
  app/src/main/java/com/prosincerity/ghostwriter/ui/screens/EditorScreen.kt → app/src/main/java/com/prosincerity/ghostwriter/ui/screens/ProjectInfoDialog.kt
- `GhostwriterApp()` --calls--> `EditorScreen()`  [EXTRACTED]
  app/src/main/java/com/prosincerity/ghostwriter/MainActivity.kt → app/src/main/java/com/prosincerity/ghostwriter/ui/screens/EditorScreen.kt
- `WaveformView()` --references--> `WaveformMarker`  [EXTRACTED]
  app/src/main/java/com/prosincerity/ghostwriter/ui/components/WaveformView.kt → app/src/main/java/com/prosincerity/ghostwriter/data/ProjectMetadata.kt
- `BeatPlayerPanel()` --references--> `WaveformMarker`  [EXTRACTED]
  app/src/main/java/com/prosincerity/ghostwriter/ui/screens/EditorScreen.kt → app/src/main/java/com/prosincerity/ghostwriter/data/ProjectMetadata.kt
- `EditorScreen()` --calls--> `WaveformMarker`  [EXTRACTED]
  app/src/main/java/com/prosincerity/ghostwriter/ui/screens/EditorScreen.kt → app/src/main/java/com/prosincerity/ghostwriter/data/ProjectMetadata.kt

## Import Cycles
- None detected.

## Communities (30 total, 8 thin omitted)

### Community 0 - "BeatPlayer"
Cohesion: 0.10
Nodes (3): BeatPlayer, BeatPlayerTest, MediaPlayer

### Community 1 - "ProjectStorage"
Cohesion: 0.15
Nodes (3): Context, IntArray, ProjectStorage

### Community 2 - "MainActivity.kt"
Cohesion: 0.17
Nodes (14): Editor, GhostwriterApp(), Home, MainActivity, Screen, Settings, HomeScreen(), NewProjectDialog() (+6 more)

### Community 3 - "ProjectMetadata"
Cohesion: 0.14
Nodes (5): ProjectMetadata, WaveformMarker, ProjectInfoDialog(), ProjectMetadataTest, JSONObject

### Community 7 - "EditorScreen.kt"
Cohesion: 0.23
Nodes (13): android, IntArray, Modifier, WaveformView(), BeatPlayerPanel(), displayNameFor(), EditorScreen(), formatPlaybackTime() (+5 more)

### Community 8 - "WaveformExtractor"
Cohesion: 0.29
Nodes (5): IntArray, WaveformExtractor, ByteBuffer, MediaCodec, MediaFormat

### Community 9 - "Settings"
Cohesion: 0.24
Nodes (4): Context, Settings, formatInterval(), SettingsFormatTest

### Community 11 - "gradlew"
Cohesion: 0.83
Nodes (3): gradlew script, die(), warn()

### Community 17 - "What You Must Do When Invoked"
Cohesion: 0.08
Nodes (24): For /graphify add and --watch, For /graphify query, For the commit hook and native CLAUDE.md integration, For --update and --cluster-only, /graphify, Honesty Rules, Interpreter guard for subcommands, Part A - Structural extraction for code files (+16 more)

### Community 18 - "Ghostwriter"
Cohesion: 0.09
Nodes (19): Feature Roadmap, Guiding rules, Non-goals, Phase 1 — Barebones notepad (MVP), Phase 2 — Songwriting environment, Documentation Index, Ghostwriter — Documentation, How to combine the two (+11 more)

### Community 19 - "Task: DAW-style waveform view for BeatPlayer (replaces slider)"
Cohesion: 0.13
Nodes (14): 0. Branch setup (do this first), 1. What this feature is, 2. Non-negotiables carried over from project rules, 3.1 `logic/WaveformExtractor.kt` (new, pure logic module), 3.2 Waveform data caching (`ProjectStorage.kt`), 3.3 `logic/WaveformViewport.kt` (new, pure logic module), 3.4 `ui/components/WaveformView.kt` (new Composable), 3.5 Marker persistence (`ProjectMetadata.kt`) (+6 more)

### Community 20 - "Project handoff: Ghostwriter"
Cohesion: 0.17
Nodes (12): 10. Before you start making changes, 1. What this project is, 2. Non-negotiable philosophy — read this before suggesting anything, 3. Tech stack (as of last verified state), 4. Repository structure (current), 5. What's actually built right now, 6. Deliberate architectural decisions — please don't silently reverse these, 7. Known technical debt (not yet addressed, tracked, but not urgent) (+4 more)

### Community 21 - "graphify reference: extra exports and benchmark"
Cohesion: 0.22
Nodes (8): graphify reference: extra exports and benchmark, Step 6b - Wiki (only if --wiki flag), Step 7 - Neo4j export (only if --neo4j or --neo4j-push flag), Step 7a - FalkorDB export (only if --falkordb or --falkordb-push flag), Step 7b - SVG export (only if --svg flag), Step 7c - GraphML export (only if --graphml flag), Step 7d - MCP server (only if --mcp flag), Step 8 - Token reduction benchmark (only if total_words > 5000)

### Community 22 - "Ghostwriter agent instructions"
Cohesion: 0.33
Nodes (5): Current architecture, Development workflow, Ghostwriter agent instructions, graphify, Non-negotiable project constraints

### Community 23 - "graphify reference: query, path, explain"
Cohesion: 0.33
Nodes (5): For /graphify explain, For /graphify path, graphify reference: query, path, explain, Step 0 — Constrained query expansion (REQUIRED before traversal), Step 1 — Traversal

### Community 24 - "graphify reference: add a URL and watch a folder"
Cohesion: 0.50
Nodes (3): For /graphify add, For --watch, graphify reference: add a URL and watch a folder

### Community 25 - "graphify reference: commit hook and native CLAUDE.md integration"
Cohesion: 0.50
Nodes (3): For git commit hook, For native CLAUDE.md integration, graphify reference: commit hook and native CLAUDE.md integration

### Community 26 - "graphify reference: incremental update and cluster-only"
Cohesion: 0.50
Nodes (3): For --cluster-only, For --update (incremental re-extraction), graphify reference: incremental update and cluster-only

## Knowledge Gaps
- **83 isolated node(s):** `Home`, `Usage`, `What graphify is for`, `Step 0 - GitHub repos and multi-path merge (only if a URL or several paths)`, `Step 1 - Ensure graphify is installed` (+78 more)
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 163 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)
- **8 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `ProjectMetadata` connect `ProjectMetadata` to `ProjectStorage`?**
  _High betweenness centrality (0.108) - this node is a cross-community bridge._
- **Why does `ProjectStorage` connect `ProjectStorage` to `MainActivity.kt`, `EditorScreen.kt`?**
  _High betweenness centrality (0.105) - this node is a cross-community bridge._
- **Why does `BeatPlayer` connect `BeatPlayer` to `EditorScreen.kt`?**
  _High betweenness centrality (0.104) - this node is a cross-community bridge._
- **Are the 20 inferred relationships involving `BeatPlayer` (e.g. with `.freshPlayer_currentPositionIsZero()` and `.freshPlayer_defaultsLoopingToTrue()`) actually correct?**
  _`BeatPlayer` has 20 INFERRED edges - model-reasoned connections that need verification._
- **Are the 11 inferred relationships involving `WaveformViewport` (e.g. with `.clamped_shrinkingViewportKeepsScrollWithinTheNewEnd()` and `.panBy_clampsAtTheStartAndEndOfTheTimeline()`) actually correct?**
  _`WaveformViewport` has 11 INFERRED edges - model-reasoned connections that need verification._
- **What connects `Home`, `Usage`, `What graphify is for` to the rest of the system?**
  _83 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `BeatPlayer` be split into smaller, more focused modules?**
  _Cohesion score 0.10338680926916222 - nodes in this community are weakly interconnected._

# Banned Antipatterns (Compose UI subset) — AI Hallucination Lookup

_Subset of `references/00-banned-antipatterns.md` from haidrrrry/compose-kotlin-agent-skills (MIT). Original row numbers kept; non-UI rows (coroutine scope, MVI `_state.update`, Room, Hilt, Ktor, DataStore, Paging, build) omitted._

Load this file before reviewing any agent-generated Kotlin. Every row is a production bug waiting to ship.

| # | Banned (WRONG) | Correct (RIGHT) | Why it breaks |
|---|----------------|-----------------|---------------|
| 3 | `Text("Hello")` in UI | `stringResource(R.string.hello)` | No localization |
| 4 | `collectAsState()` Android | `collectAsStateWithLifecycle()` | Background battery drain |
| 7 | `items(list)` no key | `items(list, key = { it.id })` | Lost item state |
| 8 | Pass `ViewModel` to child | Pass lambdas / state | Broken previews + tight coupling |
| 9 | `remember { mutableStateOf }` for screen state | ViewModel `StateFlow` | Dies on rotation |
| 14 | `Modifier.clickable` before `clip` wrong order | padding→clip→bg→clickable | Wrong hit target |
| 15 | Sort inside `LazyColumn` items | `remember` or VM sort | Recompose every frame |
| 16 | `derivedStateOf` without `remember` | `remember { derivedStateOf { } }` | Recreated each frame |
| 17 | Backwards write in `@Composable` | Write in event handlers only | Infinite recompose |
| 23 | Coil `AsyncImage` without network dep | `coil-compose` + `coil-network-okhttp` | Images never load |
| 24 | `contentDescription = null` on icons | Meaningful description or `null` only if decorative | TalkBack failure |

## How to use in review mode

When auditing a file, grep for each WRONG column pattern. If found, cite row number and apply RIGHT fix before approving.

Compose audit checklist: [`../SKILL.md`](../SKILL.md)

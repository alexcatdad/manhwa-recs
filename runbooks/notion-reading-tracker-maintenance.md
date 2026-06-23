# Notion Reading Tracker Maintenance Runbook

Use this when maintaining the Notion database `Story Analysis & Reading Tracker`.

## Source Of Truth

- Notion database: `Story Analysis & Reading Tracker`
- Database ID: `4d26fd44-d54d-42d5-bf16-784e1d47ef58`
- Data source ID: `ae90c30c-b8fb-413e-a5b2-9c463365afaa`
- Local audit log: `decisions.jsonl`

## Workflow

1. Read the incoming handoff or user notes fully before updating Notion.
2. Fetch the Notion database schema before editing properties.
3. If new story-analysis categories are requested, add them as options on `Story Tool Tags` unless the user asks for a different model.
4. Search exact titles in the Notion data source before creating rows.
5. Update existing rows in place when the title exists.
6. Create a new row only when exact-title searches do not find a reliable match.
7. Preserve existing grades unless the handoff explicitly changes them.
8. Put interpretive story-analysis details in `Notes`; put reusable labels in `Story Tool Tags`.
9. After multi-step maintenance, append important process/schema decisions to `decisions.jsonl`.
10. Verify representative rows by fetching or searching Notion after edits.

## Current Tag Semantics

- `Genre Saturation`: Good story becomes harder to enjoy because recently consumed stories share too much narrative grammar.
- `Emotional Repetition`: Story revisits the same emotional conflict without meaningful advancement.
- `Narrative Weight Mismatch`: Story assigns heavy emotional weight to a character or issue with limited active plot participation.
- `Emotional Continuity Violation`: Emotional state contradicts or ignores the current established plot state.

## Known Tool Constraint

The Notion `query_data_sources` SQL path may be blocked by the workspace plan. If that happens, use workspace/data-source search plus direct page fetch/update calls.

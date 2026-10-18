---
name: happyhorse-video
description: Create or edit HappyHorse video through Ace Data Cloud in Gemini CLI, or retrieve an original task result. Use the installed HappyHorse MCP tools and current service schema, not model-provider configuration.
---

# HappyHorse with Ace Data Cloud

## Choose only the requested service operation

Use MCP server `happyhorse-by-ace-data-cloud` and the actual prefixed tool names discovered by Gemini CLI. The package allowlist is: `happyhorse_list_models`, `happyhorse_generate_video`, `happyhorse_generate_video_from_image`, `happyhorse_generate_video_from_references`, `happyhorse_edit_video`, `happyhorse_get_task`, `happyhorse_get_tasks_batch`.

Call only `happyhorse_list_models` for a reference-only first check. It returns documentation, not a generation or balance result.

Choose text-to-video, image-to-video, reference-image video, or video edit explicitly. Image-to-video requires image_url; references require image_urls as an actual array; video editing requires video_url plus prompt. Read supported model/resolution/ratio/duration from the current tool schema; do not map Seedance fields into this service.

## Authentication and paid actions

Token setup belongs in Gemini CLI native extension settings, not the conversation. Direct setup questions to `gemini extensions config happyhorse-by-ace-data-cloud` and the repository's illustrated README. Do not read credential stores, print tokens, bypass Allowed APIs or infer balance from a reference tool result.

Inspect current tool schemas and current price before a paid operation. Ask only for missing task-relevant choices; preserve the user's requested model, input and budget. Do not silently add fallback models or chargeable operations. For user-supplied reference media, confirm the user is authorized to use it. Main-model inference and Ace video tools have separate costs.

## Submit once, retrieve the original task

1. Submit the chosen authorized generation/edit once and retain its task ID and any original trace ID.
2. Query `happyhorse_get_task` with **`task_id`**, using the original ID. Never use a generation tool for polling. Honor the server's pacing and state fields.
3. Keep pending/processing distinct from terminal complete/failed. If a bounded wait or network call times out, retain the same ID for a later lookup; do not resubmit automatically.
4. On terminal success, show the actual video URLs and metadata. On failure, preserve the returned error/ID. A task ID or successful CLI turn is not a completed artifact or proof of unique billing.
5. When the user supplies an old task ID, only retrieve that task. If no ID is supplied, ask for it; do not create or invent one.

401: check the native password setting and Key expiry. 403: inspect actual permission/moderation details. For balance issues, review current account information. For 429/5xx/timeouts, keep original IDs and avoid a second paid submission. Never include the Token in error output.

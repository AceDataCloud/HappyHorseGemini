# HappyHorse by Ace Data Cloud

This independent HappyHorse extension loads service-specific tools and a `happyhorse-video` workflow skill. It is not endorsed by the service owner or Google and does not change Gemini CLI's main model/login.

Call only `happyhorse_list_models` for a reference-only first check. It returns documentation, not a generation or balance result.

Use the native password setting `Ace Data Cloud HappyHorse API Token` for credentials; never ask for a Key in chat or expose it. For the requested paid operation, check current price, model and parameters and stay within the user's authorized budget. Submit once, retain the task ID, query the same ID with `happyhorse_get_task` using parameter `task_id`, and do not regenerate to poll or retry. Task-query permission does not grant generation permission. Return only actual terminal media URLs; pending, connection and green CLI status are not final output or unique-billing evidence.

Choose text-to-video, image-to-video, reference-image video, or video edit explicitly. Image-to-video requires image_url; references require image_urls as an actual array; video editing requires video_url plus prompt. Read supported model/resolution/ratio/duration from the current tool schema; do not map Seedance fields into this service.

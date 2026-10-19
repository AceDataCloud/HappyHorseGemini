# HappyHorseGemini

This repository owns the HappyHorse Gemini CLI manifest, native sensitive Token setting, workflow skill, commands and bilingual onboarding. The existing HappyHorseMCP owns the server; reuse its hosted endpoint without duplicating/changing shared code. Do not add hooks, trust bypass, hidden fallbacks or automatic paid generation.

Run `python3 -m unittest discover -s tests`, `python3 scripts/package_extension.py --output /tmp/happyhorse-by-ace-data-cloud.tar.gz`, the official `gemini extensions validate` and isolated lifecycle smoke checks. Ordinary CI must use test discovery. Keep English/Chinese guidance aligned, preserve real screenshot sources and license, do not commit .env, keys or private user transcripts. Publish changes through the bot PR; do not merge automatically.

Choose text-to-video, image-to-video, reference-image video, or video edit explicitly. Image-to-video requires image_url; references require image_urls as an actual array; video editing requires video_url plus prompt. Read supported model/resolution/ratio/duration from the current tool schema; do not map Seedance fields into this service.

**Task:**

You are an expert in Telugu cinema and languages. I am building a trivia game where players guess the Telugu movie based on a literal or funny English translation of its title.

I need you to generate a new level for my game containing 15 popular Telugu movies and automatically write the files to my project.

**Rules for the English Translations:**
- Translate the Telugu movie title literally into English. It can be funny or extremely literal (e.g., "The Golden Egg-Laying Duck" for Ponmuttayidunna Tharavu, or "The Boy with a Hump" for Kunjikoonan).
- Write the translations in English.
- Do NOT mention the original Telugu movie name or actor names.
- Make sure the movies are very famous and recognizable to a Telugu audience.

**Execution Steps (Follow exactly in order):**

1. **Determine the next album name:** Look at `telugu_triv_data/allLevelDetails_v3.json`. Find the last "English Translations" album (e.g., "English Translations 1") and increment the number to create the new album name (e.g., "English Translations 2"). If it doesn't exist yet, start with "English Translations 1".
2. **Update `allLevelDetails_v3.json`:** Append a new JSON object for this new album to the end of the array. Use this exact structure:
```json
{
    "name": "[New Album Name]",
    "lvls": [Number of levels],
    "cost": 150,
    "star": null,
    "is_text": true,
    "cover": 0,
    "type": "English Translations"
}
```
3. **Create the Folder:** Create a new directory at `telugu_triv_data/[New Album Name]/`.
4. **Write `units.json`:** Generate an array of 15 movie names (ALL CAPS) and write it to `telugu_triv_data/[New Album Name]/units.json`.
5. **Write `questions.json`:** Generate an array of 15 English translations matching the exact order of `units.json`, and write it to `telugu_triv_data/[New Album Name]/questions.json`.

Please proceed with generating and writing the files!

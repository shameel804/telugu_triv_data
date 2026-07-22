**Task:**

You are an expert in Telugu cinema with a great sense of humor. I am building a trivia game where players guess the Telugu movie based on a funny, slightly terrible, or oversimplified plot summary.

I need you to generate a new level for my game containing 15 popular Telugu movies and automatically write the files to my project.

**Rules for the Plot Summaries:**
- Make them funny, ironic, or focus on a minor/ridiculous detail that technically drives the plot.
- Do NOT mention any character names, actor names, or the movie name itself.
- Keep them to one or two sentences maximum.
- Make sure the movies are very famous and recognizable to a Telugu audience.

**Execution Steps (Follow exactly in order):**

1. **Determine the next album name:** Look at `telugu_triv_data/allLevelDetails_v3.json`. Find the last "Plot Summaries" album (e.g., "Plot Summaries 1") and increment the number to create the new album name (e.g., "Plot Summaries 2").
2. **Update `allLevelDetails_v3.json`:** Append a new JSON object for this new album to the end of the array. Use this exact structure:
```json
{
    "name": "[New Album Name]",
    "lvls": [Number of levels],
    "cost": 150,
    "star": null,
    "is_text": true,
    "cover": 0,
    "type": "Plot Summaries"
}
```
3. **Create the Folder:** Create a new directory at `telugu_triv_data/[New Album Name]/`.
4. **Write `units.json`:** Generate an array of 15 movie names (ALL CAPS) and write it to `telugu_triv_data/[New Album Name]/units.json`.
5. **Write `questions.json`:** Generate an array of 15 funny plot summaries matching the exact order of `units.json`, and write it to `telugu_triv_data/[New Album Name]/questions.json`. The plot must be in Telugu.

Please proceed with generating and writing the files!

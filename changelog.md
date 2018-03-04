# Changelog

| Date | Module | Change |
|---|---|---|
| 19.11.17 | (None) | Started changelog for Cube Science project|
| 19.11.17 | Seeding Engine | Added Adam's Algorithm for round generation|
| 19.11.17 | Seeding Engine | Added Graph Model for this module as se_model.svg|
| 19.11.17 | Seeding Engine | Description of seeding engine data flow|
| 07.01.18 | Score Calculator | Added frequency and average place for each player|
| 07.01.18 | Score Calculator | Added processing of multiple input files|
| 07.01.18 | Statistics_2017 |Added player win rate for all matches in the year|
| 07.01.18 | Statistics_2017 |Added class 'Deck' and loading data from matches and decklists to one list of 'Decks'|
| 07.01.18 | Statistics_2017 |Added win rates for colors and main archetypes|
| 07.01.18 | Statistics_2017 |Added games and matches win rates for cards|
| 07.01.18 | Score Calculator |Added graph generation for players from all games and matches (one year)|
| 20.01.18 | Statistics_2017|Added color-matches and archetype-matches, also with graphs for statistics and score calculations|
| 4.03.18 | Data Manager | New module to take care of loading and saving data about decks, card and matches |
| 4.03.18 | Data Manager | Moved data loading functions to Loader() class, added loading AllCards.json from the website|
| 4.03.18 | Data Manager | Added loading draft-player-archetype data|
| 4.03.18 | Data Manager | Added method that finds incorrect names in the decklists data|
| 4.03.18 | Data Manager | Added method that correct incorrect names in all decklists data and methd for the same with cube list|


Next: build sub-library with relevant card data and store it in another json file
      improve entering matches data with some good input pattern (p1 s1 p2 s2 .txt file --> matches.json)
      possibly stop using nodejs input scripting and go full python (but keep it in json anyway)
      move data_manager from notebook to an imported library module
      graph_module
      score_calculator
      
      a lot of refactorization incoming, less code, more re-use
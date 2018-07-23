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
| 10.03.18 | Data Manager | Added Converter() and Saver() classes, added conversion of matches from .txt to .json format|
| 10.03.18 | Data Manager | Added method to prepare matches for draft coverage to the Converter class|
| 11.03.18 | Data Manager | Added method to load draft decklists from .txt file in more convenient format to Loader class|
| 11.03.18 | Data Manager | Added method that converts decklists from .txt to .json and also changes numbers to cardnames |
| 14.03.18 | Score Calculator | Added method that takes .json file with matches and saves score table in .md format for coverage|
| 14.03.18 | Data Manager | Added method to convert draft data from .json to prepared decklists for coverage in .txt format |
| 18.03.18 | Task Order | Some task management stuff to decide what is the next move and why |
| 31.05.18 | Data Manager | Generated some funny aliases for players|
| 31.05.18 | Data Manager | Added method to Converter that replaces all player names with generated aliases|
| 31.05.18 | Data Manager | Converted all matches to use player aliases and saved as aliases_matches to be committed to repo|
| 20.07.18 | Reconstruction | Added new module for reconstruction of cube lists, along with visual representation of changes|
| 21.07.18 | Reconstruction | Added method to visually show known card growth after each iteration of aggregation.|
| 23.07.18 | Data | Added last known decks from 2012-2015 period|
| 23.07.18 | Data Manager | Converted all decks from .txt to .json format|
| 23.07.18 | Data Manager | Added extension for correcting the cardnames in past decklists, refreshed the allcards.json to newest version available|

Next tasks:
2. Build sub-library with relevant card data and store it in another json file
 and re-run the reconstruction module

So all necessary data will be available in the system (probably also with the draft 4/2018). Next step would be to divide current jupyter notebooks into modules that are just imported to one notebook for various purposes, so there is more order. 
3. Move data loader to exterior module
4. Move analytics / statistics to exterior module
5. Move score calaculator to exterior module
6. Move seeding engine to exterior module
7. Move coverage to exterior module

After that, there will be time to finally go with currently blocked tasks, like:
10. Build win ratio matrix based on all known matches for players and for archetypes
11. Build swiss round builder
12. Build seeding engine

Next:
      add coverage module that will take new draft data and convert them to convenient .txt formatted as .md

      
      a lot of refactorization incoming, less code, more code re-use
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
| 24.07.18 | Archetype Workshop |Added method to load only signifficant card data - used|
| 28.07.18 | Data Manager | Added method that updates the numbered_X_Y file by using changes_X_Y.txt file and latest cube list|
| 18.09.18 | Archetype Workshop | Removed 'min CMC' as not relevant, added creature density, power to toughness, power to cmc and toughness to cmc parameters, also added deck ID (player name plus draft number)|
| 18.09.18 | Archetype Workshop | Pre-analysis step one - converting data to data frame and generating histograms for all numeric variables |
| 18.09.18 | Archetype Workshop | Pre-analysis step two - find minimal and maximal values for each parameter, needed for normalizaction |
| 20.09.18 | Task Order | Updated changelog file along with planned tasks and order fo them. Prioritised Archetype Workshop for time being |
| 25.09.18 | Archetype Workshop | Histograms moved to new method |
| 25.09.18 | Archetype Workshop | Added scatter plots for each pair of numerical parameters, with archetype coloring |
| 26.09.18 | Archetype Workshop | Remove MedianCMC parameter and add normalization for data frame |
| 26.09.18 | Archetype Workshop | Normalized data to normalized data frame which will be used to calculate distance |
| 27.09.18 | Archetype Workshop | Added method that converts data from normalized_pre_df to dict with coordinates |
| 27.09.18 | Archetype Workshop | Added method that calculates distance between two sets of deck coordinates |
| 27.09.18 | Archetype Workshop | Added method that finds the closest deck for each deck and shows the distance |
| 1.11.18 | Cube Science Modules Visual | Added graph representing current progress on Archetype Workshop module |
| 1.11.18 | Archetype Workshop | Added Card Vote method as second method for the classification, defined next steps |
| 18.11.18 | Archetype Workshop | Added Center Point method as third method for classification, seems that it has low accurancy|
| 28.02.19 | Archetype Workshop | Added Parameter Vote method as fourth method. Unfortunately it doesn't seem to be very effective, only like 41 percent|
| 4.08.19 | Archetype Workshop | Added gathering information about the classification process for further investigation|
| 4.08.19 | Archetype Workshop | Saving, loading and analysis of the classification done by all methods. Updating decks|
| 2.11.19 | Archetype Workshop | Added unweighted kNN method as a fifth classification method. Tried weighted without good results|

Next tasks:

(--> Archetype Workshop track)
DONE 1. Generate scatterplots for each numerical parameters pair to look for some corelation
DONE 2. Normalize data present in data frame to make it from 0.0 to 1.0 (standard formula: (value - min(values))/(max(values) - min(values))
DONE 3. Define function that calculates the distance between two decks, in n-dimensional space (n = number of parameters)
NOT NECESSARY 4. Calculate all distances between all known decks (220 at this point) and keep it as distance matrice 
DONE 5. For each deck find a deck that is closest to this specific deck when using these metrics
6. Generate graphviz visualisation where every deck has edge / arrow to closest deck and see what happens (look for some groups)
DONE 7. Experiment with some radiuses to try classify the decks (find center of each archetype - CenterPoint Method)
DONE 7a. Try classification with kNN method without and with weighted votes
DONE 7b. Try classification with parameter vote
DONE 7c. Try classification with card vote (each card votes for some archetype)
7d. Add TaggedVote method of classification
7e. Add MethodVote method for classifcation (or even weighted method vote - later)
7f. Examine methods accuracy for different volume of data

(--> Seeding Engine track) ? LOW PRIORITY
8.  Build win ratio matrix based on all known matches for players and for archetypes
9.  Build swiss round builder
10. Build seeding engine

(--> Code refactoring work)
11.  Move data loader to exterior module
12. Move analytics / statistics to exterior module
13. Move seeding engine to exterior module
14. Move coverage to exterior module

Divide current jupyter notebooks into modules that are just imported to one notebook for various purposes, so there is more order. 

(--> Coverage Module track)
15. Add coverage module that will take new draft data and convert them to convenient .txt formatted as .md
16. Add coverage module that makes a .html with visual decklists
17. Automated coverage so only comments for matches, introduction and summary need to be added, nothing more.
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
| 25.04.20 | Coverage Module | Loading decklists, converting to img list, html template, header, basics, background, all decks, convert to .pdf file |
| 29.04.20 | Coverage Module | Add missing images, convert card image names, move to linux version|
| 30.04.20 | Coverage Module | Add missing images, convert all decks, update log, committ coverageModule|
| 23.05.20 | Tag Analytics | New sub-module to clean all tagging done for relevant cards (PC)|
| 24.05.20 | Tag Analytics | Tag cleaning finished, most likely not all of them will be used |
| 24.05.20 | Reconstruction Module | Added method that saves all reconstructed cube lists to new 'reconstructed' directory|
| 25.05.20 | General | Updated changelog and task lists for future enhancements |
| 19.07.20 |Synergy Checker | Added PoC of new module synergyChecker (not to be added soon)|
| 22.07.20 | Tag Analytics | tagAnalytics module initial commit (before re-factorization|
| 24.07.20 | Archetype Worksop | Updated table to more readable, swapped rows with columns (each columns represents score from one method | 
| 30.07.20 | Coverage Module | Changed filename, added scoreCalculator as class, added score table to the html file |
| 31.07.20 | Coverage Module | Add match table to the html file, now full coverage (decks, matches, scores) is generated for draft |
| 26.09.20 | Coverage Module | Moved prepareDecklistsForCoverage (text) from Data Manager to Coverage Module |
| 27.09.20 | Card Analytics | Added calculating expected and actula card popularity, saving results as .csv file |
| 11.10.20 | Card Analytics | Added plot generating for accumulated average and saving these plots to 'popularity' directory |
| 25.10.20 | Card Analytics | Added HTML generation and conversion to .pdf |
| 31.10.20 | Archetype Detector | Added Tag kNN11 method (first method based on tags)|
| 1.11.20 | Archetype Detector | Added Tag Center Point method (last supervised method)| 
| 2.11.20 | Archetype Detector | Added unsupervised classification for parameters and tags |
| 5.11.20 | Archetype Detector | Added generation of graph and edges for parameters based clustering |
| 7.11.20 | Archetype Detector | Added graph creation based on generated nodes and edges (ranks is not working)|

Next tasks:

(--> Coverage Module track )
C1. Fix basics names in files from lower to capitalized case (data issue)
DONE C2. Add formatted table with matches to the coverage
DONE C3. Integrate score calculator and make it create formatted table
DONE C4. Integrate with old coverage module (? add .txt decklists)
C5. Build entire pipeline: IN (decklists, matches) OUT (visual coverage, text decklists)
C6. Add optional introduction, comment for draft and for matches
DONE Add coverage module that makes a .html with visual decklists

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
DONE 7da. Add Tagged KNN11 method
DONE 7db. Add Tagged Center Point Method
NOT RELEVANT 7dc. Add TagVote method (each tags votes fo archetype (similar to prameterVote)
7e. Add MethodVote method for classifcation (or even weighted method vote - later)
7f. Examine methods accuracy for different volumes of data (from 100 to 300 decks) -- use random subsets for data (generate data subsets first for each data point, use same data sets for each method -- from average
8. Add cardCloud method (calculate 1-2-3 step neighborhood for each deck)?
DONE 9. Open classification = find deck groups but don't give them archetype name
10. Refactor tagAnalytics module
11. Create graphviz input to show steps in unsupervised hierarchical classification

(--> Synergy Checker ) new module idea
DONE S1. Design algorithm for synergy checking
DONE S2. Prepare 'proof of concept' with small ammount of cards to see if it works

(--> Card Analytics ) 
DONE 1. Visualise expected and actual card popularity over time (matplot lib, save images)
DONE 2. Add template and generate .pdf file
3. Card win %

(--> Database Module ) 
D1. Create script to generate SQL inserts for matches
D2. Create script to generate SQL inserts for decks
D3. Create script to generate SQL inserts for cubes
D4. Create script to generate SQL inserts for relevant cards
D5. Create script to generate SQL inserts for tags
D6. Create script to generate SQL inserts for decklists

(--> Seeding Engine track) ? LOW PRIORITY? Possibly not relevant anymore
8.  Build win ratio matrix based on all known matches for players and for archetypes
9.  Build swiss round builder
10. Build seeding engine

(--> Code refactoring work)
11. Move data loader to exterior module
12. Move analytics / statistics to exterior module
13. Move seeding engine to exterior module
14. Move coverage to exterior module
15. Create file with all relevant paths to be loaded by any module

Divide current jupyter notebooks into modules that are just imported to one notebook for various purposes, so there is more order. 
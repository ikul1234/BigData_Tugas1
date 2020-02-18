# Tugas 1 Big Data
- [Tugas 1 Big Data](#tugas-1-big-data)
  - [## Business Understanding](#h2-id%22business-understanding-2489%22business-understandingh2)
  - [## Data Understanding](#h2-id%22data-understanding-2147%22data-understandingh2)
    - [Column Detail](#column-detail)
      - [Dataset 1(Match)](#dataset-1match)
      - [Dataset 2(hero_names)](#dataset-2heronames)
  - [## Data Preparation](#h2-id%22data-preparation-688%22data-preparationh2)
  - [## Modeling](#h2-id%22modeling-684%22modelingh2)
    - [Join Dataset From 2 Different .csv Files](#join-dataset-from-2-different-csv-files)
  - [## Evaluation](#h2-id%22evaluation-680%22evaluationh2)
    - [Joiner](#joiner)
  - [## Deployment](#h2-id%22deployment-676%22deploymenth2)
    - [Connect MySQL](#connect-mysql)
    - [Write to Database in MySQL](#write-to-database-in-mysql)
    - [Write to XLS File](#write-to-xls-file)
  - [## Final Workflow](#h2-id%22final-workflow-674%22final-workflowh2)
## Business Understanding
---
In this project, I use Dota game dataset to know what hero player use in the game. Process that could be applied to this data is join from 2 data set then Write it to XLS file and MySQL.
## Data Understanding
---
* Number of Dataset: 2
* Number of Rows: 5000 and 112
* Number Columns: 13 and 3
  
### Column Detail
#### Dataset 1(Match)
* match_id : Identifier Match
* start_time: Player start time
* duration: Duration of the game
* tower_status_radiant: Status of Tower on Radiant Side
* tower_status_dire: Status of Tower on Dire Side
* barracks_status_dire: Status of Barracks on Dire Side
* barracks_status_radiant: Status of Barracks on Radiant Side
* first_blood_time: First Blood Time on The Game
* game_mode: Mode of The Game
* radiant_win: Status Win (either yes or no)
* negative_votes: Number of Negative Votes on The Game
* positive_votes: Number of Positive Votes on The Game
* cluster: Cluster on The Game
#### Dataset 2(hero_names)
* name: Name of the Heroes
* hero_id: Indentifier Hero
* localized_name: Simplified Name of the Heroes
  
## Data Preparation
---
Download Dataset on Kaggle (https://www.kaggle.com/devinanzelmo/dota-2-matches)
1. Pick the dataset (On my case, I use match.csv and hero_names.csv)
2. Find same column name so We can join it (On my case, both of the .csv file have hero_id column)
## Modeling
---
### Join Dataset From 2 Different .csv Files
1. Csv files:
* Add 2 file reader
* Set input location for the file
* Check read column header
* Set the column delimiter
* Check ignore spaces and tabs
* Check if the preview is right then click apply
* Click OK
* Execute

## Evaluation
---
### Joiner
1. Add joiner
2. Set 2 File Reader's Output to joiner
3. Set 2 column that you will join (In my case, hero_id on Match and hero_id on hero_names)
4. Apply then Click OK
5. Execute
## Deployment
---
### Connect MySQL
1. Add MySQL Connector
2. Choose your Database Dialect (In my case, I use MySQL)
3. Choose your Driver Name (In my case, MySQL 5)
4. Set your Database hostname and Database name according to your MySQL
5. Click Apply then OK
6. Execute
### Write to Database in MySQL
1. Add DB Writer
2. Set Joiner's Output to DB Writer
3. Set MySQL Connector to DB Writer
4. Set Schema that you want to write it
5. Set Table name that you want to write it
6. Click Apply then Click OK
7. Execute
### Write to XLS File
1. Add Excel Writer(XLS)
2. Set Joiner's Output to Excel Writer(XLS)
3. Set File Location that you want
4. Click Apply then Click OK
5. Execute
## Final Workflow
---

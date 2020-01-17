# Cooking Show Challenge!

The challenge is to build an application that creates equally matched kitchen teams from a collection of chefs. 

Craft a solution that: 
* you would consider to be representative of your level of professionalism
* you would be comfortable handing off to someone else to maintain
* uses a technology that you are comfortable with
* notes any assumptions that you make

## Problem Description

Your company will be hosting a cooking competition. A number of chefs have registered online for the competition and each one has been assigned a skill rating based on their ability to make the following four dishes they will need to make:

* Risotto
* Pizza
* Cake
* Baked Potato

The organizer has tasked you with creating the kitchen teams for the tournament. You are free to do this however you like, but you have been asked to keep the following points in mind:

* The organizer doesn't know how many teams there will be yet
* Each team must have the same number of chefs
  * Any chefs that cannot be assigned to a kitchen team will be placed on a waiting list (ex. if there are 40 chefs and the organizer wants 6 teams, there will be 4 chefs on the waiting list)
* Each kitchen team must be closely balanced in each of the four dishes, such that the competition remains close. 

### Chef Data

The chef data will be made available via a REST API from the registration team. Unfortunately, their API is not yet availabe. For now, the registration team has offered you sample chef data in the [chefs.json](./chefs.json) file. The format of the data in the file will match the format of the REST response when it is available, at which point you will need to be able to quickly integrate it.

To generate additional random data for the JSON reponse, use the content from the file [chefGenerator.txt](./chefGenerator.txt) and run in through the JSON generator at the following website https://www.json-generator.com

You can change the value in `repeat(40)` to generate data for any number of chefs.

### UI Features

You have decided to build a small web application for this task. The organizer likes this approach and you discuss the following features:

* By default, the home page will show all chefs as being on the waiting list
* There will be a control that allows the user to enter the number of desired kitchen teams
* There will be a button that, when clicked, will generate the desired number of kitchen teams and put the remainder in the waiting list
* There will be a button that, when clicked, will reset the application and put all of the chefs back on the waiting list
* The generated kitchen will display the following:
  * Details For Each Chef
    * Full Chef Name
    * Risotto Rating
    * Pizza Rating
    * Cake Rating
    * Baked Potato Rating
  * Team Risotto Rating Average
  * Team Pizza Rating Average
  * Team Cake Rating Average
  * Team Baked Potato Rating Average
* The waiting list will display the following:

  * Details For Each Player
    * Full Chef Name
    * Risotto Rating
    * Pizza Rating
    * Cake Rating
    * Baked Potato Rating

The organizer has left the look and feel of the application and the technologies/languages to use in your capable hands.

## Example Output

The API returns the following chef data, which is then displayed on the home page.

_This is example output to help you understand the problem only. Make yours look pretty!_

**Waiting List**

| Chef          | Risotto |  Pizza   |   Cake   | Baked Potato |
| ------------- | :-----: | :------: | :------: | :----------: |
| Gordon Ramsay |   90    |    98    |    92    |      65      |
| Jamie Oliver  |   80    |    60    |    50    |      50      |
| Guy Fieri     |   60    |    85    |    20    |      60      |
| Rachael Ray   |   70    |    90    |    60    |      75      |
| Julia Child   |   94    |    55    |   100    |      50      |

The user selects 2 kitchen teams and clicks the button to generate the teams. The following teams and a waiting list is formed from your algorithm: 

**Waiting List**

| Chef          | Risotto |  Pizza   |   Cake   | Baked Potato |
| ------------- | :-----: | :------: | :------: | :----------: |
| Gordon Ramsay |   90    |    98    |    92    |      65      |

**Kitchen Team 1**

| Chef          | Risotto |  Pizza   |   Cake   | Baked Potato |
| ------------- | :-----: | :------: | :------: | :----------: |
| Jamie Oliver  |   80    |    60    |    50    |      50      |
| Rachael Ray   |   70    |    90    |    60    |      75      |
| **Average**   |   75    |    75    |    55    |     62.5     |

**Kitchen Team 2**

| Chef          | Risotto |  Pizza   |   Cake   | Baked Potato |
| ------------- | :-----: | :------: | :------: | :----------: |
| Guy Fieri     |   60    |    85    |    20    |      60      |
| Julia Child   |   94    |    55    |   100    |      50      |
| **Average**   |   77    |    70    |    60    |      55      |

## Submission

Submissions are to be made via a public git repository. Please include proof that demonstrates how the program works. A publicly accessible deployed application would be awesome, though not required.

## Final Thoughts

_We are not specifically looking to see if you are able to write an algorithm to find the most optimal solution. We are looking for a thoughtful approach at solving the problem and that you write a reasonable algorithm that implements the approach._

_Good luck and have fun!_

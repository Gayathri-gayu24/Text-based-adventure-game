Structure:

1. Imports and Global Variables:
    - import time: Used for creating delays to enhance user experience.
    - import json: Used for saving and loading game data.
    - inventory = []: List to store collected items.
    - clues = 0: Counter for collected clues.
    - suspicions = 0: Counter for suspicion level.

2. Function Definitions:
    - show_intro(): Introduces the game to the player.
    - choose_location(): Prompts the player to choose an investigation location.
    - crime_scene(): Handles events and choices at the crime scene.
    - house(): Handles events and choices at the suspect's house.
    - warehouse(): Handles events and choices at the old warehouse.
    - apartment(): Handles events and choices at the victim's apartment.
    - solve_mystery(): Determines if the player has enough clues to solve the mystery.
    - choose_next_location(): Redirects the player to choose a new location to investigate.
    - save_game(): Saves the current game state to a file.
    - load_game(): Loads a saved game state from a file.
    - main(): The main game loop that handles the main menu and user choices.

3. Main Game Loop:
    - The game runs in an infinite loop offering the main menu options to start a new game, load a game, or exit.

 Detailed Description:

1. Introduction (show_intro()):
    - Welcomes the player to the game and sets the scene. Introduces the player as a detective in a noir-style city.

2. Location Selection (choose_location()):
    - Prompts the player to choose from one of four locations: crime scene, suspect's house, old warehouse, or victim's apartment. Ensures valid input.

3. Investigate Locations:
    - Crime Scene (crime_scene()):
        - The player can choose to take or leave items found at the scene. Updates inventory, clues, and suspicions based on choices.
    - Suspect's House (house()):
        - Similar choice mechanism as the crime scene. Players can read a letter or ignore it and break a box or leave it.
    - Old Warehouse (warehouse()):
        - Players find money and a key, with similar choices to take or leave them.
    - Victim's Apartment (apartment()):
        - Choices include reading a diary or ignoring it and taking a photo or leaving it.

4. Mystery Solving (solve_mystery()):
    - Checks if the player has gathered enough clues and managed suspicions to solve the mystery. Offers feedback and next steps.

5. Save and Load Functions:
    - Save Game (save_game()):
        - Saves current game data to a JSON file.
    - Load Game (load_game()):
        - Loads game data from a JSON file if it exists.

6. Main Function (main()):
    - Offers the main menu options. Based on user choice, starts a new game, loads a game, or exits. Contains the game loop.

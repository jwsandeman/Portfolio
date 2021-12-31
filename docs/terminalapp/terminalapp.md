# JasonSandeman_T1A3 - Terminal Application

A recipe suggestion app written using ruby.

## 🔗 Links

View the source code on GitHub [here](https://github.com/jwsandeman/JasonSandeman_T1A3)

View my Notion Project Management Dashboard [here](https://jwsandeman.notion.site/T1A3-Terminal-Application-efe7f174b7fa4dd69b60a83e1c0847ab)

[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://festive-aryabhata-690f3c.netlify.app/index.html)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jason-sandeman-33268496/)
[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/jwsandeman)

## Installation

Clone the project:

```bash
  git clone https://github.com/jwsandeman/JasonSandeman_T1A3.git
```

Go to the project directory:

```bash
  cd JasonSandeman_T1A3/src
```

Installs ruby gem dependencies:

```bash
  ./install.sh
```

Runs the application:

```bash
  ruby main.rb
```

Alternatively you can give the app a head start by passing in your name with the run command for example(make sure to use ""):

```bash
   ruby main.rb "John Connor"
```

## Troubleshooting/Help

To run this application on your computer you will need access to your terminal with the correct permissions enabled so that you run bash commands from the terminal.

You will also need ruby installed which be done following these [instructions](https://www.ruby-lang.org/en/downloads/). There are instructions for Linux, Mac and Windows users.

If you get a permission error when trying to run the install command you can use the following command to change your permissions. After that you should be able to run the install command above.

```bash
   chmod +x ./install.sh
```

If you are having trouble getting the app to run make sure you have the following dependencies and their correct versions. Check the gemfile to make sure the your gems are using a similar version (if the last and second last decimal place in the version numbers are different that should still be fine.) and update them in the Gemfile in the './src' directory if necessary.

```bash
   gem 'colorize', '~> 0.8.1'
```

```bash
   gem 'tty-prompt', '~> 0.23.1'
```

```bash
   gem 'rspec', '~> 3.10'
```

```bash
   gem 'artii', '~> 2.1', '>= 2.1.2'
```

```bash
   gem 'rubocop', '~> 1.23'
```

```bash
   gem 'tty-progressbar', '~> 0.18.2'
```

```bash
   gem 'faker', '~> 2.19'
```

## 1. Purpose & Scope

I will be building a recipe suggestion app based on the selections that a user makes. The app will ask the user what ingredients they currently have at home and then suggest relevant recipes based on matching ingredients. These matching recipes will be displayed in a list with how many matching ingredients each recipe has. Any ingredients that the user is missing from the recipe is automatically added to a shopping list to make it easier to reference when shopping. They will also be able to view the cooking instructions for each of their chosen recipes.

### Why Build It

This app helps users quickly find recipes based on what ingredients they already have at home and reduces the number of ingredients they have to go out and buy. This prevents users from wasting time finding recipes that involve ingredients they don't have at home which is a very common and very frustrating problem. It also helps prevent them from doubling up on ingredients or not buying enough when shopping for multiple recipes as it tells the user exactly how much of each ingredient they need for each recipe.

### Target Audience

The target audience is anyone looking for ideas of what to cook based on the ingredients they already have at home and any ingredients that they need will be added to a handy shopping list for quick reference.

### How To Use It

Following the installation instructions above, and once all the dependencies have been installed, the application will run. Once the application is running users will be able to navigate through the menus using the directional arrows and the enter key. The app will also prompt the user to answer questions as necessary. Once the user has finished using the application they will be able to select "Exit" from the main menu to close the application.

## 2. Features

When a user first runs the app they will be presented with an interactive TTY-Prompt menu of options displaying the following features:

   1. Select Ingredients - This is where you select ingredients you currently have at home. You can add or remove as many ingredients as you want.
   2. Matching Recipes - This shows a list of recipes that match your ingredients. You can select as many recipes as you want. You can also remove recipes if you change your mind.
   3. My Recipes - Here you can view your recipes and then select a recipe to view the cooking instructions for that recipe.
   4. Shoppig List - This is a list of all of the ingredients that are missing from your selected recipes.
   5. Exit - This will close the application.

### Select Ingredients

- The next menu gives the user the option to choose "add ingredients" or "remove ingredients".
- Users can view a list of ingredients that is populated from all available recipes. This will be done using a recipe class that I will seed with around 5-10 recipes.
- They will be able to select the ingredients that they currently have in their pantry/fridge. Once they select an ingredient that ingredient will be used to access the "ingredient_selected" attribute in the individual_recipe class and set it to "true".
- Users will also be able to remove ingredients if they make a mistake or change their minds. This will be done in a similar method except it will set "ingredient_selected" to "false".
- If a user tries to add the same ingredient twice they will receive an error message stating that they have already added that ingredient.

### Matching Recipes

- Once Users have selected their ingredients they will be able to view a list of recipes with the number of matching ingredients next to the recipe which will be displayed based on a class method that sums up the total "true" values for each recipe and returns a to_s string interpolation of the recipe name.
- Users will be able to select as many recipes as they want and add them to their selected recipes (My Recipes). This will be done by changing the "selected_recipe" attribute in the individual_recipe class object to "true".
- Users will be able to remove recipes if they made a mistake or change their minds. This will be done by setting the "selected_recipe" attribute in the individual_recipe class object to "false".

### My Recipes

- Users will then be able to view the list of the recipes that they have selected. These recipes will be populated based on returning the recipes that have the "recipe_selected" attribute set to "true".
- They will have the option to select an individual recipe and view the instructions on how to prepare and cook it. TTY-Prompt will open the selected recipe and the cooking instructions will be displayed using a method from the individual_recipe class called print_full_recipe.

### Shopping List

- Once users have added recipes they will be able to view all of the missing ingredients that are required to make the recipes they have selected.
- The missing ingredients will be populated by iterating through each recipe and returning the recipes that have selected_recipe set to true to a new array. Then all of the ingredients with a value of "false" from that new array will be printed to the screen.

## 3. User Interaction and Experience

### Welcome Screen

- The user will be greeted by a welcome screen and prompted to enter their name.
- If they dont enter a string, they will be prompted to enter their name again until a string is entered.
- Once they do this they will be given a greeting prompt explaining how to interact with the menu options. This will form the basis for all user interactions in the app.
- The reason I am using TTY-Prompt for most of my user input is to simplify the user experience but also it comes with the added benefit of error handling as users are limited in what they can actually input/select. If they dont select the correct option or input an in invalid option they will receive a prompt on the screen indicatng that they have made an error and that they should try again. Errors will be displayed in red using colorize.

### Main Menu

- After the user is greeted by the app, they will be shown a list of menu items that they can interact with using the arrow "keys" and options can be selected using the "enter" key.
- I will be using the same navigation system when users are selecting ingredients, selecting recipes, viewing recipes and viewing the shopping list.

### Select Ingredients

Users will be shown a sub-menu with 2 options:

1. Add Ingredients

   - This takes them to the ingredients screen where they can start adding ingredients that they have at home.
   - Every time they add an ingredient it will be added to a new list above the available ingredients. This list will be a quick reference and a confirmation that they have successfully added their ingredient.
   - If they try to add the same ingredient twice they will be told that they have already added that ingredient.
   - Once they have finished adding ingredients they will be able to select "Finished adding ingredients" which will take them back to the main menu.

2. Remove Ingredients
   - This will only be available once they have already added some ingredients
   - If they try to remove ingredients before adding any ingredients they will be given an error message and taken back to the sub-menu

### Matching Recipes

1. Add recipes
   - Users will be shown a list of the matching recipes and how many ingredients are matching for each recipe. They will be able to arrow down through the list of recipes and press enter to add a recipe to their list called "My Recipes".
   - If they try to add the same recipe twice they will be told that they have already added that recipe.
   - Every time they add a recipe it will be displayed above the available recipes. This will be so they have a quick reference for what they have already added.
   - Once they are finished adding recipe's they will be able to select "finished adding recipes" which will take them back to the submenu.
2. Remove Recipes
   - They will be able to arrow down through the list of recipes and press enter to remove a recipe from their list "My Recipes".
   - Once they are finished removing recipe's they will be able to select "finished removing recipes" which will take them back to the submenu.

### My Recipes

- Users will be shown a list of the recipes that they have selected.
- They will be able to arrow down through the list of recipes and press enter to view a recipe's cooking instructions.
- Once they are finished viewing recipe's they will be able to select "finished viewing recipes" which will take them back to the main menu.

### Shopping List

- Users will be shown a list of ingredients that they are missing from the recipe's that they have selected
- They can press "enter" to go back to the main menu

## 4. Control Flow Diagram

![Terminal Application Control Flow Diagram](./docs/Terminal%20App%20Control%20Flow.png)

Here is a [Link](https://whimsical.com/terminal-app-control-flow-XJLcP7uFDbPyKQayBbWVLs@7YNFXnKbYeumqm8HZNhB9) to my Control Flow Diagram on Whimsical.

## 5. Implementation Plan

To help me organise this project and stick to my goals I have used a Notion project management dashboard. Here is the [Link](https://jwsandeman.notion.site/T1A3-Terminal-Application-efe7f174b7fa4dd69b60a83e1c0847ab) to the dashboard where you will find my "Tasks" board and my "Project Deliverables" timeline which i used to manage my time.

I used the Tasks board to keep track of any ideas, questions, bugs or general once-off taks that came to mind, whilst the Deliverables timeline was used to manage the project implementation plan and keep me accountable to my plan.

### Tasks

![Tasks](./docs/tasks_board.png)

### Deliverables

![Deliverables](./docs/notion_deliverables.png)

### Implement Features

![Implement Features](./docs/notion_implement_features.png)

### Initialise Project

![Initialise Project](./docs/notion_initialise_project.png)

### Select Ingredients Feature

![Select Ingredients](./docs/notion_select_ingredients.png)

### Matching Recipes Feature

![Matching Recipes](./docs/notion_matching_recipes.png)

### My Recipes Feature

![My Recipes](./docs/notion_my_recipes.png)

### Shopping List Feature

![Shopping List](./docs/notion_shopping_list.png)

### Testing

Most of my tests were carried out using RSpec which can be found in the src code, but i also carried out a couple of manual tests to confirm the app was working as intended.

![Testing](./docs/notion_manual_tests.png)

## 6. Attribution

- Recipes [Website](https://www.4ingredients.com.au/recipes)
- Ruby Gem [RSpec](https://github.com/rspec/rspec-metagem)
- Ruby Gem [Bundler](https://bundler.io/)
- Ruby Gem [TTY-Prompt](https://github.com/piotrmurach/tty-prompt)
- Ruby Gem [Colorize](https://github.com/fazibear/colorize)
- Ruby Gem [Artii](https://github.com/miketierney/artii)
- Ruby Gem [Rubocop](https://github.com/rubocop/rubocop)
- Ruby Gem [Faker](https://github.com/faker-ruby/faker)
- Ruby Gem [Tty-progressbar](https://github.com/piotrmurach/tty-progressbar)
- Awesome Readme [Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)

## Contact

To get in touch, email jw.sandeman@gmail.com or find me on [twitter](https://twitter.com/jwsandeman).

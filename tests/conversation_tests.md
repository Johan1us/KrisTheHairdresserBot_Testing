#### This file contains tests to evaluate that your bot behaves as expected.
#### If you want to learn more, please see the docs: https://rasa.com/docs/rasa/user-guide/testing-your-assistant/

## greet happy path
* greet: hallo
  - utter_greet
  - utter_i_can_help_with

## greet unhappy path
* greet: hoi
  - utter_greet
  - utter_i_can_help_with
* deny: nee
  - utter_no_problem
  - utter_future_help
  - utter_goodbye
* goodbye: tot ziens
  - action_listen

## goodbye happy path
* goodbye: dag
  - utter_glad_to_help
  - utter_future_help
  - utter_goodbye

## goodbye unhappy path
* goodbye: Later
  - utter_glad_to_help
  - utter_future_help
  - utter_goodbye
* deny: nee man
  - utter_my_excuses
  - utter_something_else_i_can_help_with

## bot challenge
* bot_challenge: ben je een mens
  - utter_iamabot

## give demo
* give_demo: kun je een demo geven
  - utter_demo
  - utter_demo1

## give demo 1
* greet: hi
    - utter_greet
    - utter_i_can_help_with
* give_demo: geef demo
    - utter_demo
    - utter_demo1
* affirm: ja
    - utter_glad_to_help
    - utter_something_else_i_can_help_with

## opening hours happy path
* opening_hours: vanaf hoelaat zijn jullie open?
  - utter_opening_hours
  - utter_something_else_i_can_help_with

## greet + opening hours
* greet: hoi
    - utter_greet
    - utter_i_can_help_with
* opening_hours: wanneer gaan de deuren open
    - utter_opening_hours
    - utter_something_else_i_can_help_with
* deny: nee, dank je
    - utter_glad_to_help
    - utter_future_help
    - utter_goodbye
    
## greet + opening hours
* greet: ola
    - utter_greet
    - utter_i_can_help_with
* opening_hours: wanneer gaan jullie dicht
    - utter_opening_hours
    - utter_something_else_i_can_help_with
* deny: nee, dank je
    - utter_glad_to_help
    - utter_future_help
    - utter_goodbye
## say goodbye
* goodbye
  - utter_goodbye

## bot challenge
* bot_challenge
  - utter_iamabot

## survey happy path
* greet
    - utter_greet
* affirm
    - health_form
    - form{"name": "health_form"}
    - form{"name": null}
    - utter_slots_values
* thankyou
    - utter_no_worries
    - utter_goodbye

## survey stop
* greet
    - utter_greet
* affirm
    - health_form
    - form{"name": "health_form"}
* out_of_scope
    - utter_ask_continue
* deny
    - action_deactivate_form
    - form{"name": null}
    - utter_goodbye

## survey continue
* greet
    - utter_greet
* affirm
    - health_form
    - form{"name": "health_form"}
* out_of_scope
    - utter_ask_continue
* affirm
    - health_form
    - form{"name": null}
    - utter_slots_values

## no survey
* greet
    - utter_greet
* deny
    - utter_goodbye

## ask health questions form
* greet
    - utter_greet
* affirm
    - health_form
    - form{"name": "health_form"}
* ask_exercise
    - utter_exercise_info
    - health_form
    - form{"name": null}
    - utter_goodbye

## ask diet questions
* ask_eat_healthy
    - utter_diet_info

## ask stress questions
* ask_lower_stress
    - utter_stress_info

## ask exercise
* ask_exercise
    - utter_exercise_info
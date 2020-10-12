# Rasa for Beginners wellness-check-bot
This assistant is a project for the Rasa for Beginners course. 

It uses a form to collect a user's daily health information and saves it to an Airtable.

![wellness-bot-conversation](https://github.com/RasaHQ/rasa-for-beginners/blob/master/images/bot_conversation.png?raw=true)

![wellness-bot-conversation](https://github.com/RasaHQ/rasa-for-beginners/blob/master/images/airtable.png?raw=true)

## Running the assistant
1. Download the Airtable template and generate an [Airtable API token](https://support.airtable.com/hc/en-us/articles/219046777-How-do-I-get-my-API-key-). You'll also need to locate your Table Name and Base ID, which can be found in the [Airtable API docs](https://airtable.com/api).

2. Make a copy of the `.example-env` and rename it `.env`. Add your Airtable API token, Base ID, and Table Name to the file.

3. Install Rasa Open Source: https://rasa.com/docs/rasa/user-guide/installation/
(note - this project is compatible with Rasa Open Source version 1.10.x. We plan to update this tutorial for the 2.0 release soon)

4. Install the action server dependencies

``pip install -r requirements-actions.txt``

5. Train the model:

``rasa train``

6. Open a second terminal window and start the action server:

``rasa run actions``

7. Return to the first terminal window and start the assistant on the command line:

``rasa shell``

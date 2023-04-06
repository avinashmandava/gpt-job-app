# gpt-job-app
flask app that uses OpenAI's gpt api to help you write documents to help you get a job like resumes, cover letters, stories to tell in interviews.

# How to run

## Install dependencies
First install dependencies by running
```
pip install -r requirements.txt
```

## Set up .env file in root directory
You have to create a .env file in the root directory. It should look like this, with the data filled out replacing the <> placeholders.

```
OPENAI_API_KEY=<your openai API key. This project uses gpt-3.5-turbo so it should be very cheap to run and test.>
DB_OUTPUT_DIR=<path of the folder where you will store user data, like "db">
```

## Run the code
Once you have set the above up you can run
```
python main.py
```

Then follow the prompts to get a resume generated for you. The resume output is currently JSON stored in {DB_OUTPUT_DIR}/user_data.json.

To test out the interactive chat functionality, try uncommenting lines 137 and 154 and commenting out lines 138 and 155. This will create a back and forth to gather more data from the user about activities, skills, and impact that the bot can use to extract key points.

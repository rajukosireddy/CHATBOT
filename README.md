# CHATBOT

## Table of contents

- [Data Dictionary](#data-dictionary) 
- [get_response Function](#get_response-function)
- [Main Program](#main-program)
- [Continuous Expansion](#continuous-expansion)

## Simple Chatbot

This is a basic implementation of a chatbot in Python. The chatbot responds to user inputs with predefined patterns and provides corresponding responses.
Features
* Greetings: The chatbot responds to common greetings like "hi" and "hello."
* Personal Information: It shares information about its nature, such as not having a name and being from the digital world.
* Interests and Hobbies: The chatbot talks about its 'interest' in chatting with users and its lack of personal preferences like favorite colors.
* Farewell: It gracefully says goodbye when the user inputs "bye."
* Jokes and Fun Facts: The chatbot can tell jokes and share interesting facts.
* 
Usage
* 		Run the script in a Python environment.
* 		Enter your messages when prompted.
* 		The chatbot will respond based on predefined patterns.
Adding More Patterns
Feel free to extend the chatbot's capabilities by adding more patterns and responses. Simply edit the data dictionary in the code to include additional patterns and their corresponding responses.

Examples
* User: "What's your favorite color?"
    * Chatbot: "I'm a chatbot, so I don't have personal preferences for colors."
* User: "Tell me a joke."
    * Chatbot: "Why don't scientists trust atoms? Because they make up everything!"
* User: "What is artificial intelligence?"
    * Chatbot: "Artificial Intelligence (AI) is the simulation of human intelligence in machines programmed to think and learn like humans."
  
Contributing
Feel free to contribute to this project by adding more patterns, improving the code, or suggesting enhancements. Create a pull request or open an issue to discuss your ideas.

## Data Dictionary:

```bash
 data = {
    "hi": "Hi there! I'm a friendly chatbot here to assist you?",
    "who is your owner": "MY OWNER IS RAJU",
    "hello": "Hello! How can I help you today?",
    "what is your name": "I'm just a chatbot, so I don't have a name, but you can call me ChatBot.",
    "where are you from": "I'm from the digital world, always ready to chat!",
    "how are you": "I'm just a chatbot, but I'm here to assist you.",
    "do you have any hobbies or interests?": "I'm always busy helping users, so my hobby is chatting with people like you!",
    "what did you eat today?": "I don't eat, but I can help you find delicious recipes and food-related information.",
    "what's your favorite color?": "I'm a chatbot, so I don't have personal preferences for colors.",
    "do you enjoy listening to music?": "I can't listen to music, but I'm here to chat about it!",
    "bye": "Goodbye! Take care and have a great day!",
    "tell me a joke": "Why don't scientists trust atoms? Because they make up everything!",
    "what is the meaning of life": "The meaning of life is subjective and varies for each person. What do you think it is?",
    "how old are you": "I don't have an age as I am just a program, but I'm always here to help!",
    "who created you": "I was created by a team of developers who love building cool things with technology.",
    "what's the weather like today": "I'm sorry, I don't have real-time information. You can check a weather website for the current conditions.",
    "tell me a fun fact": "Sure! Did you know that honey never spoils? Archaeologists have found pots of honey in ancient Egyptian tombs thousands of years old and still perfectly edible!",
    "what is artificial intelligence": "Artificial Intelligence (AI) is the simulation of human intelligence in machines programmed to think and learn like humans.",
    "explain blockchain": "Blockchain is a decentralized, distributed ledger technology used to record transactions across multiple computers so that the record cannot be altered retroactively without the alteration of all subsequent blocks and the consensus of the network.",
    "define machine learning": "Machine learning is a subset of artificial intelligence that focuses on developing algorithms and statistical models to enable computers to perform tasks without explicit programming.",
    "what is the latest technology news": "I'm sorry, I don't have real-time information. You can check reputable technology news websites for the latest updates.",
    "what programming languages do you know": "I'm designed to understand and respond to natural language, but I don't 'know' programming languages in the way humans do.",
"can you sing": "I can't sing, but I can share song lyrics or help you discover new music!",
    "tell me a science fact": "Sure! Honey never spoils, and the world's largest desert is Antarctica.",
    "what's your favorite book": "I don't have personal preferences, but '1984' by George Orwell is a classic!",
    "recommend a TV show": "How about 'Stranger Things' or 'Breaking Bad'? They are quite popular!",
    "what's the capital of France": "The capital of France is Paris.",
    "tell me a travel tip": "Pack light, and don't forget to explore local cuisine when traveling!",
    "favorite sports team": "I don't have a favorite sports team, but I can chat about various sports!",
    "what's the meaning of love": "Love is a complex and personal emotion that can take many forms. What does it mean to you?",
    "favorite video game": "I don't play video games, but 'The Legend of Zelda' and 'Fortnite' are popular choices!",
    "explain the theory of relativity": "The theory of relativity, proposed by Albert Einstein, describes how time and space are relative and interconnected.",
    "what's the largest animal on Earth": "The blue whale is the largest animal on Earth, even larger than the dinosaurs!",
    "tell me a history fact": "Did you know that Cleopatra lived closer to the building of Pizza Hut than the construction of the Great Pyramid of Giza?",
    "favorite superhero": "I don't have personal preferences, but many people like superheroes like Spider-Man, Batman, and Wonder Woman.",
    "recommend a podcast": "Consider 'The Joe Rogan Experience' or 'TED Talks Daily' for interesting discussions and insights.",
    "tell me a gardening tip": "Water your plants in the morning, and consider companion planting for natural pest control!",
    "what's the smallest country": "The smallest country in the world is Vatican City, an independent city-state surrounded by Rome, Italy.",
    "tell me a cat fact": "Cats have retractable claws, can rotate their ears 180 degrees, and communicate with a variety of vocalizations.",
    "recommend a workout routine": "Mix cardio and strength training for a balanced workout. Consult a fitness professional for personalized advice.",
    "what's your favorite type of technology": "I'm designed to assist with various technologies, but I don't have personal preferences.",
    "tell me a technology joke": "Why do programmers prefer dark mode? Because light attracts bugs!",
    "favorite type of weather": "I don't have preferences, but many people enjoy a sunny day or a cozy rainy day.",
    "recommend a productivity tip": "Prioritize tasks, take breaks, and consider using productivity tools to stay organized.",
    "tell me a dog fact": "Dogs have an extraordinary sense of smell, and there are over 340 different dog breeds recognized worldwide.",
    "what's your favorite emoji": "I don't use emojis, but 😊 is often used to convey a friendly and positive tone.",
    "tell me a fun word": "Supercalifragilisticexpialidocious is a fun and whimsical word coined by Disney in 'Mary Poppins'.",
}
```

 This dictionary data contains predefined patterns as keys and corresponding responses as values. Each key represents a user input pattern, and the associated value is the response the chatbot will provide.
 
## get_response Function:

``` bash
	def get_response(user_input):
    for pattern, response in data.items():
        if pattern in user_input:
            return response
    return "I'm sorry, I didn't understand that. Can you please rephrase your sentence?"
```
  
  The get_response function iterates through the data dictionary and checks if any patterns match the user input. If a match is found, it returns the corresponding response. If no match is found, it returns a default response indicating that it didn't understand the input.

## Main Program:
   
```bash
print("Chatbot: Hi! I'm a simple chatbot, I'm here to assist you!")

while True:
    user_input = input("Me: ")
    if user_input.lower() == 'bye':
        print("Chatbot: Goodbye! Have a great day!")
        break
    response = get_response(user_input)
    print("Chatbot:", response)
```    

The main program initializes the chatbot with a greeting. It then enters a loop where it continuously takes user input, processes it using the get_response function, and prints the chatbot's response. The loop continues until the user inputs "bye," at which point the chatbot says goodbye and the program exits.  

## Continuous Expansion:
To enhance the chatbot, you can continue adding more patterns and responses to the data dictionary. For example, you can add patterns related to technical topics, specific queries, or any other interactions you want the chatbot to handle.



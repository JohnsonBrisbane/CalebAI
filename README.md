# CalebAI
My first AI project to chat with my son

import random

responses = {
    "hello": ["Hello dad!", "Hi Dad!", "Greetings dad!"],
    "how are you?": ["I'm good dad, thanks dad!", "I'm doing great dad!", "All is well! dad"],
    "bye": ["Goodbye Dad!", "Farewell dad!", "Take care dad!"],
    "default": ["I'm sorry, I didn't understand.", "Could you please rephrase that?", "I'm still learning."]
}
def get_response(input_text):
    input_text = input_text.lower()
    
    # Check for predefined responses
    for key in responses:
        if key in input_text:
            return random.choice(responses[key])
    
    # Return a default response if no predefined response is found
    return random.choice(responses["default"])

while True:
    user_input = input("You: ")
    response = get_response(user_input)
    print("Chat AI:", response)

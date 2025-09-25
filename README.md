# AI-test1
First ai test
simple_ai.py
# simple_ai.py
# A basic AI chatbot for students

import random

# Some responses the AI knows
responses = {
    "hello": ["Hi there!", "Hello!", "Hey! How’s it going?"],
    "how are you": ["I’m doing great, thanks!", "I’m just a script, but I’m fine!", "All good here.
    "bye": ["Goodbye!", "See you later!", "Bye! Have a great day!"],
    "who are you": ["I’m your simple AI chatbot.", "I’m just some Python code, but I can chat with you!"],
}

def ai_reply(user_input):
    user_input = user_input.lower()
    for key in responses:
        if key in user_input:
            return random.choice(responses[key])
    return "Sorry, I don’t understand that yet."

print("🤖 Simple AI Chatbot (type 'bye' to exit)")
while True:
    user = input("You: ")
    if "bye" in user.lower():
        print("AI:", random.choice(responses["bye"]))
        break
    reply = ai_reply(user)
    print("AI:", reply)
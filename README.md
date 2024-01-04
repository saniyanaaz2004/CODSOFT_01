def simple_chatbot(user_input):
    # Convert user input to lowercase for case-insensitive matching
    user_input = user_input.lower()

    # Define predefined rules and responses
    rules = {
        'hello': 'Hi there! How can I help you?',
        'how are you': 'I am a chatbot, so I don\'t have feelings, but thanks for asking!',
        'goodbye': 'Goodbye! Have a great day!',
        'default': 'I m sorry, I don t understand that. Can you please ask something else?',
    }

    # Check if the user input matches any predefined rule
    response = rules.get(user_input, rules['default'])

    return response

# Simple loop for interaction with the chatbot
while True:
    user_input = input("You: ")
    
    # Exit the loop if the user types 'exit'
    if user_input.lower() == 'exit':
        print("Chatbot: Goodbye!")
        break

    # Get the chatbot's response based on the user input
    bot_response = simple_chatbot(user_input)
    
    print("Chatbot:", bot_response)

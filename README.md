# Amazon Lex Chatbot - BankerBot

## Overview

Welcome to the README for BankerBot, a chatbot designed using Amazon Lex to help imaginary bank customers check their account balances and transfer money between accounts. This project demonstrates how to implement context carryover to enhance user experience by remembering information across interactions.

## Project Structure

This project is divided into five parts:
1. **Introduction to Amazon Lex and Initial Setup**: Creating the base chatbot with basic intents.
2. **Adding Functionality**: Implementing the CheckBalance intent.
3. **Connecting AWS Lambda**: Integrating the chatbot with AWS Lambda to handle backend logic.
4. **Context Carryover**: Setting up context carryover to remember user information.
5. **Advanced Features**: Implementing fund transfer intents (to be completed).

## Part 4: Context Carryover

### Objectives
- Implement context carryover to avoid repeated user prompts.
- Enhance user experience by remembering user details across interactions.

### Steps

1. **Set Up a New Lex Chatbot and Intents**
   - Create a new `BankerBot`.
   - Set up `WelcomeIntent` and `FallbackIntent`.
   - Create `CheckBalance` intent with a custom slot type `accountType`.
   - Connect the chatbot with AWS Lambda.

2. **Create an Output Context for CheckBalance**
   - In the `CheckBalance` intent page, add a new output context tag `contextCheckBalance`.
   - Set the timeout for 5 turns (90 seconds).

3. **Create FollowupCheckBalance Intent**
   - Create a new intent `FollowupCheckBalance`.
   - Add `contextCheckBalance` as an input context.
   - Define sample utterances and slots (`accountType` and `dateOfBirth`).

4. **Implement Context Carryover in FollowupCheckBalance Intent**
   - Set up default values for slots using `contextCheckBalance`.
   - Ensure the Lambda function is connected to this intent.


## Key Learnings

- **Context Tags**: Used to store and retrieve information across conversations, improving user experience by reducing repeated prompts.
- **Session Management**: Essential for creating more interactive and user-friendly chatbots.
- **AWS Integration**: Combining Amazon Lex with AWS Lambda for dynamic backend processing.

## Final Thoughts

This project has been a valuable learning experience, providing insights into chatbot development with Amazon Lex, context management, and AWS integration. In the next phase, I aim to further enhance BankerBot by adding a fund transfer feature and utilizing AWS CloudFormation for quick setup.

## Connect with Me

- Author: Kanika Mathur
- GitHub: [Kanika Mathur](https://github.com/KanikaGenesis)
- LinkedIn: [Kanika Mathur](https://www.linkedin.com/in/kanika-mathur-083080121/)


# Chat Analyzer

## Description

This program analyzes the gives chat file for:
- How active a given user is in the chat
- Who has started a conversation in the chat how many times
- Has a user's (or the whole chat's) interaction increased in the given period (or the whole chat)

It also allows the user to add some date constraints and genrate graphs for some actions.

The program currently works for Telegram and Whatsapp chat exports

#Limitations
1. Whatsapp chats need to be in following format: 22/08/20, 18:04 - Friend Name : Message Text
2. For Timing change time system time format to 24 Hrs and restart whatsapp before exporting the chats.

## How to Run

First install the required dependencies using the command:
`pip install -r requirements.txt`

Then you can run the program with the following command:
`python chat_analyzer <options> <path_to_chatfile>`

e.g. python chat_analyzer.py -p -cS -ml 5 -a -sG -iC _chat.txt

To know about the options run the command:
`python chat_analyzer --help`

Usage: chat_analyzer.py [OPTIONS] PATH_TO_CHATFILE

Options:
  -p, --percentage          Show percentage contribution to the chat
  -cS, --conv-starters      Get the frequecy at which each person has started
                            the conversation

  -u, --username TEXT       Show results for a particular User only (Provide
                            the username)

  -ml, --minlength INTEGER  Minumin Msg length
  -c, --constraint TEXT...  Add date Constraints (format - mm/dd/yy)
  -a, --activity            Show hourwise activity of users
  -iC, --interaction-curve  Tell whether the interaction of the user has
                            increased or decreased

  -sG, --show-graph         Show graph(s) for the selected options if
                            available

  --help                    Show this message and exit.

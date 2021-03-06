# morning-text-bot

The morning-text-bot is a simple telegram bot that sends a collection of telegram messages to start the day. Details
 follow Installation and Configuration.

## Installation

Use git to clone.

```bash
git clone https://github.com/coldbrewdev/morning-text-bot
```
A sample-config.py file is provided.

## Configuration

The code is currently configured such that in addition to the repo you will need (1) to create your own telegram bot (2) to host the script and have the script run daily at your set time (3) a config file.

### Telegram Bot

Creating a telegram bot is a [straightforward process](https://core.telegram.org/bots). This bot currently uses the
 http protocol for the telegram API directly, i.e. you don't need supplemental modules. Just get your bot's ID and the
  chat ID
  of the person you want to message.

### Hosting

PythonAnywhere and AWS Lightsail are fine options. On PythonAnywhere you can schedule a daily task. On AWS Lightsail (Ubuntu) you can add it as a cron task.

## Usage Details

Running the script currently sends four consecutive messages. Here we detail their contents and some thoughts on how you might modify them.

### Good Morning
Sends the current date and the ages (in days) of you and one other person.

### Weather
Currently provides a brief description of the weather forecast for Chicago today. Can change to your city by changing lat/lon in the API call (and change the message to say your city).

### Headlines
Currently provides top headlines from CNN Lite, Business Insider, and MarketWatch, along with SPX and DJI futures.

You could use BeautifulSoup or your favorite parser to get headlines from other sites.

### COVID Data
Currently provides updates on COVID cases and COVID vaccinations for the City of Chicago via their API. You could configure to whatever region you could find data for.

## License
MIT License found in LICENSE.txt
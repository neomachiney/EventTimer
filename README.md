# Event Timer
![EventTimer](https://github.com/neomachiney/EventTimer/blob/master/pics/EventTimer.png)
![EventTimer2](https://github.com/neomachiney/EventTimer/blob/master/pics/EventTimer2.png)
[![Code Grade](https://www.code-inspector.com/project/15088/status/svg)](https://frontend.code-inspector.com/public/project/15088/EventTimer/dashboard)
[![Code Quality](https://www.code-inspector.com/project/15088/score/svg)](https://frontend.code-inspector.com/public/project/15088/EventTimer/dashboard)
![Travis Build](https://api.travis-ci.com/neomachiney/EventTimer.svg?branch=master)
[![PyPI version](https://badge.fury.io/py/event-timer.svg)](https://badge.fury.io/py/event-timer)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

- :warning: Before diving into my tools, read this: [NUKED](https://github.com/machineydv/machineydv/blob/master/NUKED.md)

## Description
A simple and light event countdown manager. Here, event is anything that you need countdown on. You can almost fill anything as event such as movie release dates or appointments.

## Features
* Ability to run countdown of multiple events and printing of countdown is in different time format (GMT, Nepali, Indian)
* Event creation is as easy as adding a few lines. It find the config files in different locations and even from argument
* Output is colorful and oddly satisfying

## Installation
Use either of any options:
* `pip install event-timer`
* `python3 setup.py install`

## Usage
Before running this tool, create or edit config files which can be found in different locations. The order in which looks for config file is:
1. --config filename.cfg
2. {CURRENT_WORKING_DIRECTORY}/{DEFAULT_FILES}
3. ~/{DEFAULT_FILES}
4. EventTimer/{DEFAULT_FILES} if you use it without installation.  

Here,
* {DEFAULT_FILES}: `("event.cfg", ".event.cfg", "event_config.cfg", ".event_config.cfg")`. 
* {CURRENT_WORKING_DIRECTORY}: The directory in which you are when running the program

The default_file list may change and is found in src/EventTimer/lib/Globals.py

Finally, `EventTimer` or `python3 EventTimer.py` to run.

## Examples
See examples folder for event.cfg examples

## Limitations
* Providing wrong data will cause wrong time to be displayed especially when choosing timezones. Some timezones maybe 1hr forward or backward so
caution is advised on important events.
* Unhidden logical bugs or faults in modules

## Todo
* Send notification libnotifysend and slack notification when timer is reached.

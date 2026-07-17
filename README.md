# Quantifying Sleep Positions With Body Weight

![Photo of various electronic components.](https://hosting.photobucket.com/bbcfb0d4-be20-44a0-94dc-65bff8947cf2/5b93a2c3-8297-4a47-996c-a428c35c57b8.jpg)

Quantifying sleep behavior by capturing and analyzing how body weight is distributed across a sleeping surface over extended periods of time.

## Application Overview

The system uses eight force-sensitive resistor (FSR) pads connected to a Raspberry Pi 5 for capturing pressure data throughout the night. By continuously recording these signals, it can infer sleeping positions and detect patterns in how the body shifts during rest. The data workflow is designed around Python and Flask for collection and storage as JSON, forming a flexible foundation for long-term tracking.

Currently the project is focused on research, hardware assembly and validating the feasibility of this approach. The broader goal is to analyze trends over a 30 to 90 day period and translate raw pressure data into meaningful insights about physical behavior during sleep. Visualization will play a key role, with D3.js and JavaScript tools transforming the collected data into interactive graphics.

This project originally relied on an AMG8833 IR thermal sensor to measure body heat while sleeping. Due to technical difficulties, I chose to go another route; using numerous FSR pads to quantify my body weight over a prolonged period of time instead. The `app.py` script in this repository reflects this first approach, connecting to an AMG8833 over I2C and printing its 8x8 grid of temperature readings once per second.

## Basic Setup Instructions

Below are the required software programs and instructions for running the current sensor script on a Raspberry Pi.

### Programs Needed

- [Git](https://git-scm.com/downloads)

- [Python](https://www.python.org/downloads/)

### Steps For Use

1. Install the above programs

2. Enable I2C on the Raspberry Pi: `sudo raspi-config`

3. Select `Interface Options` and `I2C` from the RPi config UI

4. Wire the AMG8833 sensor to the RPi's SCL and SDA pins

5. Open a terminal

6. Clone this repository: `git clone git@github.com:devbret/sleeping-positions-project.git`

7. Navigate to the repo's directory: `cd sleeping-positions-project`

8. Create a virtual environment: `python3 -m venv venv`

9. Activate your virtual environment: `source venv/bin/activate`

10. Install the needed dependencies: `pip install adafruit-circuitpython-amg88xx`

11. Run the sensor script: `python3 app.py`

## Development Roadmap

The planned FSR system follows development pipeline outlined below:

- **Sense:** Eight FSR pads positioned across the sleeping surface, each registering pressure applied by body weight

- **Collect:** Raspberry Pi 5 continuously reads the FSR signals throughout the night using Python

- **Store:** Workflow records the readings as JSON so as to keep the data flexible for long-term accumulation

- **Analyze:** Over 30 to 90 days, the accumulated pressure data is mined for trends in sleeping positions

- **Visualize:** Interactive graphics built with D3.js and other JavaScript tools translate the raw data into meaningful insights

Progress updates, build logs and photos are documented at the associated [Hackaday.io project page](https://hackaday.io/project/203728-quantifying-sleep-positions-with-body-weight).

## Other Considerations

This project repo is intended to demonstrate an ability to do the following:

- Capture continuous pressure data with eight FSR pads and a Raspberry Pi 5

- Infer sleeping positions and detect patterns in how the body shifts during rest

- Build a flexible Python and Flask workflow which stores long-term readings as JSON

- Translate 30 to 90 days of raw pressure data into interactive D3.js visualizations

If you have any questions or would like to collaborate, please reach out either on GitHub or via [my website](https://bretbernhoft.com/).

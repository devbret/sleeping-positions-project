# Quantifying Sleep Positions With Body Weight

![Photo of various electronic components.](https://hosting.photobucket.com/bbcfb0d4-be20-44a0-94dc-65bff8947cf2/5b93a2c3-8297-4a47-996c-a428c35c57b8.jpg)

Systematically quantifying sleep behavior by capturing and analyzing how body weight is distributed across a sleeping surface over extended periods of time.

## Overview

The project uses eight force-sensitive resistor (FSR) pads connected to a Raspberry Pi 5 to capture pressure data throughout the night. By continuously recording these signals, the system can infer sleeping positions and detect patterns in how the body shifts during rest. The data workflow is being designed around Python and Flask for collection and storage as JSON, forming a flexible foundation for long-term tracking.

Currently the project is focused on research, hardware assembly and validating the feasibility of this approach. The broader goal is to analyze trends over a 30 to 90 day period and translate raw pressure data into meaningful insights about physical behavior during sleep. Visualization will play a key role, with D3.js and JavaScript tools planned to transform the collected data into interactive graphics. This iterative process reflects a hands-on approach to self-quantification and pattern discovery.

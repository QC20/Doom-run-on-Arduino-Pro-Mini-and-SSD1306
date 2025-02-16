# Run the Classic Doom Game with SSD1306 and Arduino Pro Mini (16 mHz/5V)

Witness the magic where the legendary Doom meets the compact power of Arduino Pro Mini and the versatile SSD1306 display.

Delve into the rich history of Doom, a game that revolutionized the gaming industry with its immersive gameplay and iconic graphics. Thanks to its efficient design, Doom is playable on almost any device, from powerful computers to humble microcontrollers like Arduino Pro Mini.

Discover how this repository enables you to experience the thrill of Doom on your Arduino setup, leveraging the capabilities of SSD1306 for an engaging visual experience. Explore the possibilities as we bridge the gap between retro gaming and modern microcontroller technology. Let's embark on a journey where the past meets the future, all within the palm of your hand!

### Current Wiring
For your convinience I have listed my current wiring underneath. You can fit it differently depending on your setup. However, please note that the Arduino Pro Mini has dedicated SDA on A4 and SCL on A5. On many models these pins are inconviently placed not-to-grid on the PCB board. Besides these video pins you are free to choose any other pins for your setup. 

Arduino —– OLED
5v ——–––––––—–— VCC (pay attention to your OLED voltage requirements)

GND ——–––––––—– GND

A4 ————–––––––– SDA

A5 ————–––––––– SCL
q

Arduino - Buttons
UP button ––––– 8 Pin
Down button ––– 7 Pin
Left button ––– 9 Pin
Right button –– 6 Pin


## Doom 

Doom run on Arduino Uno:
https://wokwi.com/projects/397445939459713025

The Wokwi simulator does not have a Arduino Pro Mini option, which is why I have recreated the setup with an Arduino Uno. The basic premise is the same though. The choice of making it with the Pro Mini is due to its smaller design. However, you can also do it with the Arduino Uno if this is the only microcontroller you have available. 

<video width="320" height="240" controls>
  <source src="img/vid/IMG_6066.mov" type="video/mp4">
  Your browser does not support the video tag.
</video>

## Game Map
To make this project possible, I had to make some compromises, allowing us to see a functioning prototype of Doom running on one of the smallest Arduino products available. The current version is operating with 92% of the available memory, meaning that we are rapidly approaching the limit of what is achievable. One adjustment I made was to include only one level (based on E1M1 from Wolfenstein 3D). So, when you clear a level and advance to the next, you are essentially replaying the same level repeatedly. Fun, right?

```
  ################################################################
  #############################...........########################
  ######....###################........E..########################
  ######....########..........#...........#...####################
  ######.....#######..........L.....E.......M.####################
  ######.....#######..........#...........#...####################
  ##################...########...........########################
  ######.........###...########...........########################
  ######.........###...#############D#############################
  ######.........#......E##########...############################
  ######....E....D...E...##########...############################
  ######.........#.......##########...############################
  ######....E....##################...############################
  #...##.........##################...############################
  #.K.######D######################...############################
  #...#####...###############...#E.....K##########################
  ##D######...###############..####...############################
  #...#####...###############..####...############################
  #...#...#...###############..####...############################
  #...D...#...#####################...############################
  #...#...#...#####################...############################
  #...######D#######################L#############################
  #.E.##.........#################.....#################........##
  #...##.........############...............############........##
  #...##...E.....############...............############........##
  #....#.........############...E.......E....#.........#........##
  #....L....K....############................D....E....D....E...##
  #....#.........############................#.........#........##
  #...##.....E...############...............####....####........##
  #...##.........############...............#####..#####.....M..##
  #...##.........#################.....##########..#####........##
  #...######L#######################D############..###############
  #...#####...#####################...###########..###############
  #E.E#####...#####################...###########..###############
  #...#...#...#####################.E.###########..###############
  #...D.M.#...#####################...###########..###############
  #...#...#...#####################...###########..###.#.#.#.#####
  #...#####...#####################...###########...#.........####
  #...#####...#####################...###########...D....E..K.####
  #................##......########...###########...#.........####
  #....E........E...L...E...X######...################.#.#.#.#####
  #................##......########...############################
  #################################...############################
  #############..#..#..#############L#############################
  ###########....#..#.########....#...#....#######################
  #############.....##########.P..D...D....#######################
  ############################....#...#....#######################
  ##############..#################...############################
  ##############..############....#...#....#######################
  ############################....D...D....#######################
  ############################....#...#....#######################
  #################################...############################
  ############################.............#######################
  ############################..........EK.#######################
  ############################.............#######################
  ################################################################
```


## SSD1306 OLED Display

The SSD1306 OLED (Organic Light-Emitting Diode) display is based on light-emitting diode (LED) technology, where the emissive electroluminescent layer is a film of organic compound that emits light in response to an electric current. This layer of organic semiconductor is situated between two electrodes, typically with at least one electrode being transparent.

OLEDs are extensively used to create digital displays in various devices such as television screens, computer monitors, portable systems like mobile phones, handheld game consoles, and PDAs. Notably, OLED displays do not require a backlight as they emit visible light themselves. This characteristic enables OLED displays to achieve deep black levels, making them thinner, lighter, and capable of offering a high contrast ratio compared to traditional liquid crystal displays (LCDs).

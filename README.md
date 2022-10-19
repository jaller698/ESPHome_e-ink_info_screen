# ESPHome_e-ink_info_screen

I wanted a simple dashboard to show the current weather, and a forecast. Plus the time it takes me to take public transport to the four most visited destinations. Inspired by [esphome-weatherman-dashboard](https://github.com/Madelena/esphome-weatherman-dashboard) & [esphome-waveshare-e-paper-dashboard](https://github.com/DeastinY/esphome-waveshare-e-paper-dashboard) I set out to create my own take.  

No soldering needed. 

## Hardware

- The screen itself is a 7.5 inch waveshare E-ink display. Which can be found at Amazon: [Link](https://www.amazon.de/-/en/gp/product/B075R4QY3L/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1) 
- Additionally I used a driver board for the display. [Link]( https://www.amazon.de/-/en/gp/product/B07RM1BBVF/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1 )
- To frame it in a nice and neat way, I used a generic picture frame from [Ikea](https://www.ikea.com/dk/da/p/ribba-ramme-sort-50378448/).
- A micro USB cable to power the board, and a mobile phone powerbrick to said cable. 

## Setting up
1. Connect the driver board with the display, there should be  an inclouded ribbon cable.
2. Install the ESPhome integration in your homeassistant configuration. 
3. Copy the files from this directory to your configuration. 
4. Modify the ./config/esphome/secrets.yaml to include your own secrets.
5. Connect either the board directly to the computer running HaOS via USB-cable, or another way. 
6. Flash the "Weatherman.yaml" file to your driver board, using ESPHome. 


## Data sources

If you followed the guide, you should now have a functioning E-ink display. But you'll need to modify the template sensor in the inclouded configuartion field, to incloude your own sensors. Furthermore, if you wish to make use of the Rejseplan API (Danish public transport), you'll need to contact Rejseplanen [Labs](https://help.rejseplanen.dk/hc/da/requests/new). Alternatively you can make use of the [Goodservice API](https://www.goodservice.io/api/stops/<stop_id>). Some further tinkering might be needed then. 

## Todo
1. Configure the second page to include price data from the local powergrid. 
2. Add Energy consumption data. 


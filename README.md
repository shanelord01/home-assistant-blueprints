This is an edge use case - but I wanted to be able to make my Actron Que air conditioner change from heat to fan if my upstairs rooms became too hot, 
in order to circulate the hot air around the house. It should then revert to previous state when the temperatures stabilise (so it heats again
at night time).

I have my air conditioner running thanks to this amazing add-on https://github.com/MikeJMcGuire/hass-actronque - Thanks Mike!

Two helpers need to be created:

1. Input Boolean (Override Flag)
- Go to Settings → Devices & Services → Helpers.
- Click + Create Helper (bottom right).
- Select Toggle.
- Set:
  Name: Actron Temp Override Active
- Click Create.

2. Input Text (Active Zones Storage)
- Still in Helpers, click + Create Helper again.
- Select Text.
- Set:
  Name: Actron Active Zones
  Maximum Length: 255
- Click Create.

Then when you import the blueprint, select all of your upstairs zones you want to include, and then all of your zones (not including the main controller), 
then season sensor and the helpers. You can then adjust the acceptable temp difference.

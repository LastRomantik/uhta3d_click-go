### How do you like the possibility to make the usual navigation more comfortable? )
I wrote a little plugin that gives you a bit more freedom to navigate the virtual tour.

### I'll tell you the gist:
There are often virtual tours where the hotspots are very small and it is not always convenient to click on them or just tap them with a mouse or finger on the phone. So why not remove the hard link to the hotspot click event?

Now, with the Click&Go plugin, you don't have to worry about whether or not it's convenient to hit the hotspot with your mouse. You can just click in the direction you want to go and the plugin will find the closest hotspot and click on it if it is within the allowed field of view.

P.S. In my opinion, this kind of navigation should be standard for all virtual tours. But that's just me :)

### Plug-in connection (example):
```
<plugin name="uhta3d_clickandgo" url="plugins/uhta3d_clickandgo.js" keep="true"
	angle="40" 
	offset="10" 
	onover="set(alpha, 0.5)"
	onout="set(alpha, 1)"
	onclick="onclick()"
/>
```

### Parameters:
* _**angle**_ - finding angle of the nearest hotspot from mouse click (default 40)
```
    Krpano XML:
        uhta3d_clickandgo.angle         - get value
        uhta3d_clickandgo.angle = 40    - set value
    JavaScript:
        uhta3d_clickandgo.angle()       - get value
        uhta3d_clickandgo.angle(40)     - set value
```

* _**offset**_ - offset force when hotspot is not found (default 10)
```
    Krpano XML:
        uhta3d_clickandgo.offset        - get value
        uhta3d_clickandgo.offset = 10   - set value
    JavaScript:
        uhta3d_clickandgo.offset()      - get value
        uhta3d_clickandgo.offset(10)    - set value
```

* _**onover**_ - applies to the new found hotspot
```
    onover = "set(alpha, 0.5)"
```

* _**onout**_ - applies to the past hotspot that lost mouse focus
```
    onout = "set(alpha, 1)"
```

* _**onclick**_ - applies to the current hotspot
```
    onclick="onclick()"
```
_p.s. callwith() does not need to be used, it is already written inside the plugin. Works with the hotspot.onclick attribute by executing its code._

> [!NOTE]
> And as usual:
> Have fun testing and waiting for feedback to fix bugs and errors in the work. And maybe some interesting suggestions for modernisation)

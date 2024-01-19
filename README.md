<div align='center'><h2>Usage</h2></div>

Event:
  - TriggerEvent('notifications:sendNotification', 2, 'Hello world!', 5000)

For QB Replace:

Go to qb-core\client\functions.lua & search for
```lua
function QBCore.Functions.Notify
```
Delete whole function and replace this

```lua
function QBCore.Functions.Notify(text, texttype, length)
    local color = 0
    if texttype == 'success' then color = 3 elseif texttype == 'error' then color = 2 else color = 1 end
    TriggerEvent('notifications:sendNotification', color, text, length or 5000)
end
```

Colors:
  - Normal: 1
  - Error: 2
  - Warning: 3
    
<div align='center'></div>
<div align='center'><h2>Preview</h2></div>


![image](https://github.com/thesevenq/notifications/assets/59538879/7a399947-6ccd-4edf-89e3-2e2f7ec502c7)


<p>Visitor count</p>
  <img src="https://profile-counter.glitch.me/notifications_NP-4.O-Style-replace/count.svg" />

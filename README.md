# Cron
Cron System for RedM Extended

## How to install
* Download the lastest version of cron
* Copy and paste ```cron``` folder to ```resources/cron```
* Insert the .sql file into your database.
* Add ```ensure cron``` to your ```server.cfg``` file
* Now you are ready!

## Usage
```lua

-- Execute task 5:10, every day
function CronTask(d, h, m)
  print('Task done')
end

TriggerEvent('cron:runAt', 5, 10, CronTask)

-- Execute task every monday at 18:30
function CronTask(d, h, m)
  if d == 1 then
    print('Task done')
  end
end

TriggerEvent('cron:runAt', 18, 30, CronTask)

```
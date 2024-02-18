# 0x19. Postmortem - Api blacked out our service

- DevOps
- SysAdmin

> ## Postmortem

## Issue Summary
- **Duration**: 6 hours, from 10:00 AM to 04:00 PM (GMT)
- **Impact**: the api shutdown unexpectedly and to users have a blackout from our service
- **Root Cause**: after investigations it turn that there is a problem was that a cdn that we relay on changes some configurations in there api.

## Timeline
- **11:00 AM**: The first sign of trouble was a sudden influx of error logs in the api.
- **Actions Taken**: We delved into the database connection and scanned through the logs.
- **Misleading Investigation**: Our quest began with a wild goose chase for network connectivity issues. It felt like we were trying to catch shadows.
- **Escalation**: By 12:00 PM, the api  drama had reached its peak, and we had to call in the senior backend engineers.
- **Resolution**: At the stroke of 3:00 PM, after an intense battle with the misconfiguration beast, we finally exorcised integrating the new configuration .

## Root Cause and Resolution
- **Root Cause**: The api, in the form of a misconfiguration, disrupted the database connection, pushing our authentication service into a full-blown crisis mode.
- **Resolution**: With our holy rollback spell and a dash of optimized database connection parameters, we managed to restore peace in the kingdom, ensuring the api wouldn't dare show their faces again.

## Corrective and Preventative Measures
- **Improvements**: We're reinforcing our fortress by fortifying the monitoring system to catch any mischievous misconfigurations and database connection dramas. We're also conjuring automated rollback spells for those critical services.
- **Tasks to Address the Issue**:
    1. Putting misconfigurations on a strict diet by implementing rigorous code review processes.
    2. Training our crystal ball to proactively monitor critical service parameters, including database connections and error logs.
    3. Crafting automated rollback spells to swiftly banish any mischievous api that dare disturb our service peace.
    4. Hosting a " seminar with the engineering team to ensure we all know how to spot and tackle these shenanigans in the future.


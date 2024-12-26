tzdata: Python package providing IANA time zone data (now with Ramat HaSharon support!)
====================================================

Being born in Ramat HaSharon is a real struggle, apart from being a general condescending a**hole and a burden to society, growing up with ALSES (Always Late to Social Events Syndrome) is really tough.

But now, worries be gone!

Are you always late to social events but you don't really care and just want your friends to get off your back? we got you covered, with our newest addition to tzdata `Asia/Ramat_HaSharon`!

Just use the ultimate excuse of **"I'm not *actually* late, I'm from Ramat HaSharon"**

They don't believe you? Prove em wrong.



`pip install git+https://github.com/omribromberg/tzdata.git`

```python
from zoneinfo import ZoneInfo
from datetime import datetime

normal_people_arrival_time =  datetime.strptime("2024-01-01 13:30", "%Y-%m-%d  %H:%M").astimezone(ZoneInfo("Asia/Tel_Aviv"))
print(f"normal people are arriving at: {normal_people_arrival_time.strftime("%H:%M:%S")}")
# normal people are arriving at: 13:30:00


# Doing stupid stuff being late


disturbed_people_arrival_time = datetime.strptime("2024-01-01 14:10", "%Y-%m-%d  %H:%M").astimezone(ZoneInfo("Asia/Tel_Aviv"))
print(f"other people think you arrive late at: {disturbed_people_arrival_time.strftime("%H:%M:%S")}")
# other people think you arrive late at: 14:10:00

reality_arrival_time = disturbed_people_arrival_time.astimezone("Asia/Ramat_HaSharon")
print(f"but in reality you are an early bird arriving at: {reality_arrival_time.strftime("%H:%M:%S")}")
# but in reality you are an early bird arriving at: 13:27:18

print("GREAT SUCCESS, friends.STFU() == FriendshipStatus.OFF_MY_BACK # True")
# GREAT SUCCESS, friends.STFU() == FriendshipStatus.OFF_MY_BACK # True
```





We are now working to get this PR official, please star this project to get us going and finally make ALSES reality.



This is a Python package containing ``zic``-compiled binaries for the IANA time
zone database. It is intended to be a fallback for systems that do not have
system time zone data installed (or don't have it installed in a standard
location), as a part of `PEP 615 <https://www.python.org/dev/peps/pep-0615/>`_

This repository generates a ``pip``-installable package, published on PyPI as
`tzdata <https://pypi.org/project/tzdata>`_.

For more information, see `the documentation <https://tzdata.readthedocs.io>`_.



# mobility_analytics
Analysis of location data platform. The platform has location data which it uses in order to calculate insights. Within the location data we look for high-quality devices. Qualified devices (QMAU = Qualified Monthly Active Users) represent normal human behavior throughout the day.(go to work > go back home, go out to buy groceries, travel etc.)
with a good location signals coverage and stable signals collection. In other words, the device activity should be well covered with location signals, without data anomalies, so Placer can produce accurate insights which represent the reality.

Analysis
● How does the device's activity look like in terms of time?
Food for thought:
○ Active Hour for a device is defined as an hour with at least 1 registered signal
○ We can than define an ‘active-day'?
○ We can also have active-days in a specific month that we can consider “good enough” (i.e. decent activity)

● How does the device's activity look like in terms of movement?
We want to ensure that devices are not static and move normally (go to work, go shopping etc.). 
We can describe the movement activity during the sample period with a metric we create.

○ We Convert the signal coordinates to geohash (level 7 recommended) in order to simplify the movement analysis and base the new metric on that.
○ We than define a minimal/normal movement activity on a given day/month.
○ We than can define an abnormal activity of too low/high geo distribution
(i.e. devices which are not moving enough/devices vs those which move all over the US in a single day)

● We Set thresholds to define a Qualified User - based on the metrics we have already generated so far.
Than we select the metrics and the corresponding thresholds you think best represent the definition of a qualified user.

○ We can find also some relationships between the “conditions” (metrics) you selected - a device
should be disqualified if it fails to meet any of the criteria.

○ Visualizations and Explanations and supportive info for our decisions comes later on here.

Qualified Users Summary - based on the thresholds and the QMAU definition you set in the previous step, we present here many QMAU we have in the sample.

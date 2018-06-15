# Vehicles
Data description:
Dataset: obd2.csv
Variables:
1. 'vehicle_id' - car's identifier
2. 'ride_id' - travel ID. Observations for a given vehicle with a common ride_id are for one journey by one car.

3. 'timestamp' - the time at which the measurement was made

4. 'type' - information whether it is a measurement of rotations ("rmp") or speed ("speed")

5. 'result' - the value of the measurement

Task: Determine on which gear the car is going at the moment. So the idea is to develop an algorithm that for a given observation will assign the gear the car was on at the moment.
Of course the task wouldn't demand machine learning, if we were provided with following data for each car: number of gears, wheel circumference and gear ratio for each gear.
Problem type: 1-dimensional clustering
Variable clustered: rpm/speed
Data preprocessing: special treatment of abnormal observations, taking the logarithm of the main variable
Method applied: for each vehicle several KMeans models where created for different numbers of clusters (gears). The best number of clusters was established by comparing inertias.
Visualisation: a separated plot was created for each vehicle indicating the gear assigned to each point (observation) using different colors


Aknowledgment: the dataset is from "MyWheels - yor drive assistant", mywheels.pl/en/

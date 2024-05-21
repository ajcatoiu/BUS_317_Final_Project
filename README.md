# Facial Recognition for User Authentication
Authors: Andrew Catoiu, RJ Livelo

## About This Project
<strong>Goal</strong><br>
In this project, we gathered images of faces. Some were of our own, and the rest were of random faces on the internet. Our goal is to authenticate device users my detecting their face on the computer webcam.<br><br>

<strong>Process</strong><br>
xyz use a model trained on Roboflow, using the images as our dataset, to detect 

## Necessary dependencies/libraries
Before compiling, you must clone the cJSON parser from GitHub using this command:
```
git clone git@github.com:DaveGamble/cJSON.git
```

## How To Use
To test Part 1 of this project, run these commands <strong>in order</strong>.

1) On server VM:
```bash
make server
```

2) On client VM:
```bash
make client
```
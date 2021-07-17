# AI_TASK2_SMART_METHODS-
This work is for my second task in the AI route at [Smart Methods'](https://s-m.com.sa/c12_in.php) training program.

## Task description 
Using [Turtlebot3](https://emanual.robotis.com/docs/en/platform/turtlebot3/overview/) with [SLAM approach](https://en.wikipedia.org/wiki/Simultaneous_localization_and_mapping) to create and save a map.

## Task Steps

1- After installing ROS melodic with proper Gazebo version in the [pervious task](https://github.com/Khaled-Dahhasi/AI_task1_smart_methods), we will install the dependencies that this task will need for Turtlebot3 and SLAM simulations. We will use this [tutorial](https://emanual.robotis.com/docs/en/platform/turtlebot3/quick-start/#pc-setup)

2- Now we will install the simulation package to launch the simulation using this [tutorial](https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/). this package offer a variety of bots and simulation worlds.
It also offers a node that lets you operate the bot in real time in the simulation world.

Here is an example of the bot in turtlebot3 world simulation (red circle drawn to show the bot): ![turtlebot3world](https://user-images.githubusercontent.com/85564881/126042708-af0255b9-0d73-4aa8-b002-cc979e067a86.png)

3- Now we will use SLAM simulation to Create a map of the simulated World and save it for future use in navigation. this is done via the lidar sensor mounted on the bot. 
the burger bot and the Tutrlebot3 world are gonna be used for this test. We will use [this tutorial](https://emanual.robotis.com/docs/en/platform/turtlebot3/slam_simulation/) for the commands.

after Launching the simulation's world and bot with SLAM we now have to use the operating node to move the bot around to "explore" the area with it's lidar sensor. Doing this we will see how the map is getting complete in the SLAM simulation.

![Completing Map](https://user-images.githubusercontent.com/85564881/126044143-fe208300-9346-4eec-a6e0-e52d4a10e452.gif)

4- After moving around enough to complete the full map we will save it for future use using the command 

`rosrun map_server map_saver -f ~/map`
![Saving Map](https://user-images.githubusercontent.com/85564881/126044340-5a7544df-2f26-48de-82b6-63136df3ecac.gif)
![Saved Map](https://user-images.githubusercontent.com/85564881/126044392-56732a24-f840-45a7-a284-cee75dc2f4a7.png)

with this the task is done and in future tasks this map will be used for navigation purposes.

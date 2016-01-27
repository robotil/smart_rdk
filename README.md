# smart_rdk
ATTENTION, starting Jenuary 27, 2016, the parameter scen should be given without "work_space"...
***********************************************************************************************
This repository keeps scenarios generated by SmART. They can be reproduced.

Install:

1. git clone the repository
2. cd smart_rdk/src/smart_rdk
3. mkdir include
4. cd ../../; catkin_make
5. mkdir smart_rdk/devel/lib/smart_rdk/; 
6. cp smart_rdk/ReplayPlayer smart_rdk/devel/lib/smart_rdk/
7. source smart_rdk/devel/setup.bash


Running:


In order to run a scenario, copy from the directory of the sample you want to run, for example: 8Sept_sampl_8, the files:
     scen.SFV, scenarioEnv.world,  scenarioMission.bag to:
             smart_rdk/src/smart_rdk/work_space/scenario_1/ and then:

          bobcat:  roslaunch smart_rdk runScenario_robil2.launch
          bobtank: roslaunch smart_rdk runScenario_robil2_bobtank.launch
    or:
          bobcat: roslaunch smart_rdk runScenario_robil2.launch scen:=<dirofsampl>
          bobtank: roslaunch smart_rdk runScenario_robil2_bobtank.launch scen:=<dirofsampl>
              
In order to replicate a scenario, get from ftp or drive site the bag files and then:

          bobcat: roslaunch smart_rdk repScenario_robil2.launch scen:=<dirofsampl>
          bobtank: roslaunch smart_rdk repScenario_robil2_bobtank.launch scen:=<dirofsampl>
          Additional Parameters: st - start time in seconds
                                 dt - duration in seconds
                                FORMAT st:=xx for ex. st:=30

More on bobtank:

When launching the repScenario version, don't hit the "play" button on the Gazebo client. Hit the run on the terminal.


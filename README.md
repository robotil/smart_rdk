# smart_rdk
This repository keeps scenarios generated by SmART. They can be reproduced.

Install:

1. git clone the repository
2. cd smart_rdk/src/smart_rdk
3. mkdir include
4. catkin_make
5. cp smart_rdk/ReplayPlayer smart_rdk/devel/lib/smart_rdk/
6. source smart_rdk/devel/setup.bash


In order to run a scenario, copy:
     scen.SFV, scenarioEnv.world,  scenarioMission.bag to:
             smart_rdk/src/smart_rdk/work_space/scenario_1/ and then:

          roslaunch smart_rdk runScenario_robil2.launch
                        
In order to replicate a scenario, get from ftp site bag files and then:

          roslaunch smart_rdk repScenario_robil2.launch scen:=work_space/<dirofsampl>



# ROS Move Base

This repository demonstrates the usage of setting up move_base with and without map.  

## Package Structure
```
.
├── CMakeLists.txt
├── config
│   ├── base_global_planner_params.yaml
│   ├── base_local_planner_params.yaml
│   ├── costmap_common_params.yaml
│   ├── global_costmap_params.yaml
│   ├── local_costmap_params.yaml
│   └── move_base_params.yaml
├── launch
│   ├── amcl.launch
│   ├── map_server.launch
│   ├── move_base.launch
│   └── start_navigation.launch
├── LICENSE
├── maps
│   ├── playpen.pgm
│   └── playpen.yaml
├── package.xml
└── README.md

3 directories, 16 files
```

## Installation

I would recommend clone the entire [navigation stack](https://github.com/ros-planning/navigation) to local computer as well as [navigation messages](https://github.com/ros-planning/navigation_msgs). However, if you would prefer to install through apt you may do as you wish.  

## Obstacle Layer

By setting the `combination_method = 0` it allows whatever in the obstacle layer to overwrite the master costmap. Most of the time you will be using `combination_method = 1`. [ref1](https://answers.ros.org/question/316191/static_layer-gets-deleted-by-obstacle_layer-in-global_costmap/) [ref2](http://wiki.ros.org/costmap_2d/hydro/obstacles)  

This parameter can be changed under `config/costmap_common_params.yaml`.

To again register static map obstacle into the master costmap you may run this command.  
```bash
rosservice call /move_base/clear_costmaps "{}"
```

## References  

- https://answers.ros.org/question/155091/move_base-without-map/
- For more detail references on config files please look at each individual file for references.  
- https://answers.ros.org/question/316191/static_layer-gets-deleted-by-obstacle_layer-in-global_costmap/

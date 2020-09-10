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

## References  

- https://answers.ros.org/question/155091/move_base-without-map/
For details references on config files please look at each individual files for references.  

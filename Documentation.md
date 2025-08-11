# Documentation

## Running a problem

As shown within the examples section, to run a problem both the executable and input file are required as command line arguments, as can be seen below. 

```
./CabanaPD/build/install/bin/ElasticWave CabanaPD/examples/mechanics/inputs/elastic_wave.json
```

Each line in the input file defines a parameter or setting of the simulation, with the following available options:

    "dx"                       : {"value": [0.001, 0.001, 0.001], "unit": "m"},
        Sets the distance between particles. If provided, this is used to calculate m (neighbors defining interaction zone)
    "system_size"              : {"value": [0.2, 0.2, 0.3], "unit": "m"},
        Defines the dimension in the x, y, and z planes
    "density"                  : {"value": 7800, "unit": "kg/m^3"},

    "bulk_modulus"             : {"value": 130e+9, "unit": "Pa"},
    "shear_modulus"            : {"value": 78e+9, "unit": "Pa"},
    "critical_stretch"         : {"value": 0.02},
    "horizon"                  : {"value": 0.00417462, "unit": "m"},  
    "use_contact"              : {"value": true},
    "contact_horizon_factor"   : {"value": 0.9},
    "contact_horizon_extend_factor"   : {"value": 0.01},  
    "cylinder_outer_radius"    : {"value": 0.025, "unit": "m"},
    "cylinder_inner_radius"    : {"value": 0.02, "unit": "m"},
    "cylinder_height"          : {"value": 0.1, "unit": "m"},
    "max_radial_velocity"      : {"value": 200, "unit": "m/s"}, 
    "min_radial_velocity"      : {"value": 50, "unit": "m/s"},
    "max_vertical_velocity"    : {"value": 100, "unit": "m/s"}, 
    "final_time"               : {"value": 2.5e-4, "unit": "s"},
    "timestep"                 : {"value": 1.7e-07, "unit": "s"},
    "timestep_safety_factor"   : {"value": 0.70},
    "output_frequency"         : {"value": 50},
    "output_reference"         : {"value": false}

how to format input file
    options for inputs
        like different input file examples show different things
        m or horizon (not for dem)
        low particle counts
        ^ should i say how it can also be calculated within the cpp file
        maybe go line by line to say what the different settings could do? like changing the time step output frequency

how to set up particles and randomizing them

how to select between BPM, LPS, or Contact models

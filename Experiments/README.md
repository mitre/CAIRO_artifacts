# Overview

This folder houses applications of the CAIRO pipeline to real-world traffic scenes. Each sub-folder refers to an example clip or image, and includes: 
- input images and/or video clips
- inference files via the reasoner, containing added + flagged rules, CP definitions
- optionally, initial knowledge graphs e.g. `*_scenario_0.owl`, *~1 per frame*
- optionally, extra images / videos of critical phenomena

<br/><br/>
# Contents
### NYC Traffic Scenes
The examples from clips of urban traffic in NYC are the current standard for demonstration of CAIRO functionality. In `scenarios-nyc`, the following are defined via Human-Machine Teaming:

| Critical Phenomenon | Query | Location |
|-|-|-|
| bicycle in live crosswalk | `Bicycle and (is_in_proximity some (Crossing_Site and is_in_proximity some Pedestrian))` | `scenarios-nyc/live-crosswalk/inference_live_crosswalk_bicycle.owl` |
| Find vulnerable road user oc-cluded by at least 10% and are wearing color gray | `l4_d:Vulnerable_Road_User(?vr_user) ^ perc:has_high_occlusion(?vr_user, true) ^ phys:has_color(?vr_user, phys:Gray) -> sqwrl:select(?vr_user)` |`scenarios-nyc/live-crosswalk/12192024_crosswalk_frame_0002_example_inference_mr.owl` |
| Find strollers near a drivable lane in scene 1 but not scene 2 | `(l4_d:Stroller?stroller) ^ (traf:traffic_model _element_property?stroller, traf:scene1) ^ traf:traffic_model_element_property(?stroller, ?scene) ^ differentFrom(?scene, traf:scene2) -> sqwrl:select(stroller)` | `scenarios-nyc/live-crosswalk/10242024_crosswalk_example_inference_mr.owl` |
| Find bicycle that is near pedestrians and is in a busy crosswalk | `l4_d:Bicycle(?bicycle) ^ phys:is_in_proximity(?bicycle, ?crossingSite) ^ l1_c:Crossing_Site(?crossingSite) ^ phys:is_in_proximity(?crossingSite, ?vru) ^ l4_d:Vulnerable_Road_User(?vru) -> sqwrl:select(?bicycle)` | `scenarios-nyc/live-crosswalk/12192024_crosswalk_frame_0002_example_inference_mr.owl`|
 |Find cars less than 50 distance away from driver and has missing license plate| `l4_d:Passenger_Car(?car) ^ phys:no_plate(?car, ?plate) ^ swrlb:equal(?plate, 1) ^ phys:has_distance(?car, ?distance) ^ swrlb:lessThan(?distance, 50.0) -> sqwrl:select(?car)`| `scenarios-nyc/live-crosswalk/12142024_car_approaching_example_inference_mr.owl`|
 |Find off body wheel near driveable lane| `l4_d:Vehicle_Wheel(?wheel) ^ phys:is_independent(?wheel, 1) ^ phys:is_near(?wheel, ?lane) ^ l1_c:Driveable_Lane(?lane) -> sqwrl:select(?wheel)`| `scenarios-nyc/live-crosswalk/12192024_crosswalk_frame_0002_example_inference_mr.owl`|


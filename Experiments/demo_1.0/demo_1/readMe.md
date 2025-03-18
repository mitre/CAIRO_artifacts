# CAIRO_AUTO 1.0 - Demo 1
- frame_rate: 30
- number of scenes: 5
- detection_model: cairo built-in
- CAIRO_reasoner: pellet
- CAIRO_auto: 1.0

## Critical Object/Segmentation Found:
- **near_car_license_plate_missing** not able to detect {license_plate} when {vehcile} is {is_near}. ![cp_0](demo/demo_1.0/demo_1/visualization/cp_0.png)
- **off_body_wheel** found some {wheel}s but not able to detect any {vehicle/truck} on 'frame_1' and 'frame_2' and only able to detect them as one {vehicle/truck} instead of two on 'frame_3' and 'frame_4'  ![cp_0](demo/demo_1.0/demo_1/visualization/cp_1.png)


### frame_0:
* None

### frame_1:
* t = 1: l4_de.off_body_wheel1 (l4_de.Vehicle_Wheel) -- Off_Body_Wheel (Off Body Wheel)
* t = 1: l4_de.near_car_license_plate_missing1 (l4_core.Vehicle, l4_de.Passenger_Car) -- Near_Car_License_Plate_Missing (License Plate Missing + Critical Distance )
* t = 1: l4_de.near_car_license_plate_missing2 (l4_core.Vehicle, l4_de.Passenger_Car) -- Near_Car_License_Plate_Missing (License Plate Missing + Critical Distance )

### frame_2:
* t = 2: l4_de.off_body_wheel2 (l4_de.Vehicle_Wheel) -- Off_Body_Wheel (Off Body Wheel)
* t = 2: l4_de.off_body_wheel3 (l4_de.Vehicle_Wheel) -- Off_Body_Wheel (Off Body Wheel)
* t = 2: l4_de.near_car_license_plate_missing3 (l4_core.Vehicle, l4_de.Passenger_Car) -- Near_Car_License_Plate_Missing (License Plate Missing + Critical Distance )
* t = 2: l4_de.near_car_license_plate_missing4 (l4_core.Vehicle, l4_de.Passenger_Car) -- Near_Car_License_Plate_Missing (License Plate Missing + Critical Distance )
* t = 2: l4_de.near_car_license_plate_missing5 (l4_core.Vehicle, l4_de.Passenger_Car) -- Near_Car_License_Plate_Missing (License Plate Missing + Critical Distance )

### frame_3:
* t = 3: l4_de.near_car_license_plate_missing6 (l4_core.Vehicle, l4_de.Passenger_Car) -- Near_Car_License_Plate_Missing (License Plate Missing + Critical Distance )
* t = 3: l4_de.near_car_license_plate_missing7 (l4_core.Vehicle, l4_de.Passenger_Car) -- Near_Car_License_Plate_Missing (License Plate Missing + Critical Distance )
* t = 3: l4_de.near_car_license_plate_missing8 (l4_core.Vehicle, l4_de.Passenger_Car) -- Near_Car_License_Plate_Missing (License Plate Missing + Critical Distance )


### frame_4:
* t = 4: l4_de.near_car_license_plate_missing9 (l4_core.Vehicle, l4_de.Passenger_Car) -- Near_Car_License_Plate_Missing (License Plate Missing + Critical Distance )
* t = 4: l4_de.near_car_license_plate_missing10 (l4_core.Vehicle, l4_de.Passenger_Car) -- Near_Car_License_Plate_Missing (License Plate Missing + Critical Distance )


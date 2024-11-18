# Data Collected by Vehicle

<img src="./img/overpass/Vehicular_urban_overpass.png" alt="Description of your image" width="500" height="">

## Description

The vehicular urban overpass scenario contains 52 roadside facilities (RSFs) and a complex multi-lane overpass. The vehicle is equipped with communication devices and multi-modal sensors, including three cameras, two types of depth cameras (three each), and a LiDAR. The time interval between adjacent snapshots is 50 ms and the frame rate of the multi-modal sensory data at the vehicle is 20 Hz. The frame rate of the communication data is also 20 Hz. The snapshots corresponding to all data are reflected in the filenames, such as "snapshot91_pointcloud.txt" for LiDAR point cloud data at snapshot 91 and "csi_95.mat" for the chanenl matrix at snapshot 95. The total duration of all three scenarios is 75 s with snapshots ranging from 1 to 1500.
Special case: in the txt files, we set the Z-values of all ground vehicular trajectories to 0.

## Coordinate System Description

### **[World Coordinate System]:**

The world coordinate system is a North-East-Down (NED) coordinate system with the X-axis pointing north, the Y-axis pointing east, and the Z-axis pointing downward. It is a right-handed coordinate system, with the origin at the same height as the ground.

### **[Vehicle Coordinate System]:**

This system includes both vehicles. The X-axis points forward, the Y-axis points to the right, and the Z-axis points downward relative to the vehicle. It is a right-handed coordinate system, with the origin at the center of the vehicle and a certain height relative to the ground.

The position coordinates and heading angles given in the vehicle trajectory txt files represent the position of the vehicle coordinate system's origin in the world coordinate system, as well as the orientation of the vehicle coordinate system relative to the world coordinate system. 
(Special case: in the txt files, we set the z-values of all ground vehicles' trajectories to 0. Before use, it is necessary to subtract the height of the vehicle center relative to the ground to obtain the actual coordinates of the vehicle coordinate system's origin in the world coordinate system.) Additionally, note that pitch, roll, and yaw in the vehicle trajectory txt files are given in radians.

### **[LiDAR Coordinate System]:**

The coordinate axes align with those of the vehicle system, with the origin offset by a fixed amount relative to the vehicle coordinate system's origin.

### **[Camera Coordinate System]:**

The coordinate axes by default align with those of the vehicle system. If multiple cameras are mounted on a device, each camera's orientation will be specified. The camera origin is offset by a fixed amount relative to the vehicle coordinate system's origin.

### **[mmWave Radar Coordinate System]:**

The coordinate axes align with those of the vehicle system, with the origin offset by a fixed amount relative to the vehicle coordinate system's origin.

### **[Communication Antenna Coordinate System]:**

The coordinate axes align with those of the vehicle system, with the origin offset by a fixed amount relative to the vehicle coordinate system's origin.

## Sensor Position

The vehicular urban wide lane scenario includes vehicles of the **"Blue SUV"**, **"Mini Cooper"**, **"Sedan"**, **"Pickup"**, **"Box truck"**, **"Concrete"**, **"Refuse truck"**, **"School bus"** and **"Tank"** types. The relative coordinate positions and parameter information of the sensors are given as follows:

<table>
    <thead>
        <tr>
        <th rowspan="2">Side View</th>
        <th rowspan="2">Name</th>
        <th colspan="8" style="text-align: center;">Camera</th>
        <th colspan="5" style="text-align: center;">LiDAR</th>
        <th colspan="5" style="text-align: center;">mmWave Radar</th>
        </tr>
        <tr>
        <th>Direction</th>
        <th>X(m)</th>
        <th>Y(m)</th>
        <th>Z(m)</th>
        <th>Pitch</th>
        <th>Roll</th>
        <th>Yaw</th>
        <th>FoV Degrees(°)</th>
        <th>X(m)</th>
        <th>Y(m)</th>
        <th>Z(m)</th>
        <th>Vertical FoV(°)</th>
        <th>Horizontal FoV(°)</th>
        <th>X(m)</th>
        <th>Y(m)</th>
        <th>Z(m)</th>
        <th>Vertical FoV(°)</th>
        <th>Horizontal FoV(°)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
        <td><img src="./img/overpass/car1_blue_suv.png" alt="Side view of car1" width="100"></td>
        <td>Blue SUV</td>
        <td>+x</td>
        <td>2</td>
        <td>0</td>
        <td>-1</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>100</td>
        <td>0</td>
        <td>0</td>
        <td>-1.9</td>
        <td>-25~15</td>
        <td>-180~180</td>
        <td>0</td>
        <td>0</td>
        <td>0.8</td>
        <td>-10~10</td>
        <td>-90~90</td>
        </tr>
        <tr>
        <td><img src="./img/overpass/car2_mini_white_car_suv.png" alt="Side view of car1" width="100"></td>
        <td>Mini Cooper</td>
        <td>+x</td>
        <td>1.8</td>
        <td>0</td>
        <td>-1</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>100</td>
        <td>0</td>
        <td>0</td>
        <td>-1.8</td>
        <td>-25~15</td>
        <td>-180~180</td>
        <td>0</td>
        <td>0</td>
        <td>0.8</td>
        <td>-10~10</td>
        <td>-90~90</td>
        </tr>
        <tr>
        <td><img src="./img/overpass/car3_white_car.png" alt="Side view of car1" width="100"></td>
        <td>Sedan</td>
        <td>+x</td>
        <td>2.3</td>
        <td>0</td>
        <td>-1</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>100</td>
        <td>0</td>
        <td>0</td>
        <td>-1.9</td>
        <td>-25~15</td>
        <td>-180~180</td>
        <td>0</td>
        <td>0</td>
        <td>0.8</td>
        <td>-10~10</td>
        <td>-90~90</td>
        </tr>
        <tr>
        <td><img src="./img/overpass/car4_pika.png" alt="Side view of car1" width="100"></td>
        <td>Pickup</td>
        <td>+x</td>
        <td>3.5</td>
        <td>0</td>
        <td>-1.2</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>100</td>
        <td>0</td>
        <td>0</td>
        <td>-2.4</td>
        <td>-25~15</td>
        <td>-180~180</td>
        <td>0</td>
        <td>0</td>
        <td>0.8</td>
        <td>-10~10</td>
        <td>-90~90</td>
        </tr>
        <tr>
        <td><img src="./img/overpass/car5_xianxing_car.png" alt="Side view of car1" width="100"></td>
        <td>Box truck</td>
        <td>+x</td>
        <td>3.2</td>
        <td>0</td>
        <td>-1.4</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>100</td>
        <td>0</td>
        <td>0</td>
        <td>-2.8</td>
        <td>-25~15</td>
        <td>-180~180</td>
        <td>0</td>
        <td>0</td>
        <td>0.8</td>
        <td>-10~10</td>
        <td>-90~90</td>
        </tr>
        <tr>
        <td><img src="./img/overpass/car6_hu_ni_tu_car.png" alt="Side view of car1" width="100"></td>
        <td>Concrete</td>
        <td>+x</td>
        <td>1</td>
        <td>0</td>
        <td>-4.1</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>100</td>
        <td>0</td>
        <td>0</td>
        <td>-4.1</td>
        <td>-25~15</td>
        <td>-180~180</td>
        <td>0</td>
        <td>0</td>
        <td>0.8</td>
        <td>-10~10</td>
        <td>-90~90</td>
        </tr>
        <tr>
        <td><img src="./img/overpass/car7_rush_car.png" alt="Side view of car1" width="100"></td>
        <td>Refuse truck</td>
        <td>+x</td>
        <td>2.5</td>
        <td>0</td>
        <td>-4.1</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>100</td>
        <td>0</td>
        <td>0</td>
        <td>-4.1</td>
        <td>-25~15</td>
        <td>-180~180</td>
        <td>0</td>
        <td>0</td>
        <td>0.8</td>
        <td>-10~10</td>
        <td>-90~90</td>
        </tr>
        <tr>
        <td><img src="./img/overpass/car8_school_lolar_car.png" alt="Side view of car1" width="100"></td>
        <td>School bus</td>
        <td>+x</td>
        <td>1.2</td>
        <td>0</td>
        <td>-2.8</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>100</td>
        <td>0</td>
        <td>0</td>
        <td>-2.8</td>
        <td>-25~15</td>
        <td>-180~180</td>
        <td>0</td>
        <td>0</td>
        <td>0.8</td>
        <td>-10~10</td>
        <td>-90~90</td>
        </tr>
        <tr>
        <td><img src="./img/overpass/car9_statci_mesh .png" alt="Side view of car1" width="100"></td>
        <td>Tank</td>
        <td>+x</td>
        <td>0</td>
        <td>0</td>
        <td>-4</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>100</td>
        <td>0</td>
        <td>0</td>
        <td>-4</td>
        <td>-25~15</td>
        <td>-180~180</td>
        <td>0</td>
        <td>0</td>
        <td>0.8</td>
        <td>-10~10</td>
        <td>-90~90</td>
        </tr>
    </tbody>
</table>



<table>
    <thead>
        <tr>
        <th rowspan="2">Side View</th>
        <th rowspan="2">Name</th>
        <th colspan="3" style="text-align: center;">Communication Equipment</th>
        </tr>
        <tr>
        <th>X(m)</th>
        <th>Y(m)</th>
        <th>Z(m)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
        <td><img src="./img/overpass/car1_blue_SUV.png" alt="Side view of car1" width="100"></td>
        <td>Blue SUV</td>
        <td>0.3</td>
        <td>0</td>
        <td>-1.1</td>
        </tr>
        <tr>
        <td><img src="./img/overpass/car2_mini_white_car_SUV.png" alt="Side view of car1" width="100"></td>
        <td>Mini Cooper</td>
        <td>0.5</td>
        <td>-0.1</td>
        <td>-1.3</td>
        </tr>
        <tr>
        <td><img src="./img/overpass/car3_white_car.png" alt="Side view of car1" width="100"></td>
        <td>Sedan</td>
        <td>0.3</td>
        <td>0</td>
        <td>-1.7</td>
        </tr>
        <tr>
        <td><img src="./img/overpass/car4_pika.png" alt="Side view of car1" width="100"></td>
        <td>Pickup</td>
        <td>3.5</td>
        <td>0</td>
        <td>1.2</td>
        </tr>
        <tr>
        <td><img src="./img/overpass/car5_xianxing_car.png" alt="Side view of car1" width="100"></td>
        <td>Box truck</td>
        <td>0</td>
        <td>0</td>
        <td>-2.1</td>
        </tr>
        <tr>
        <td><img src="./img/overpass/car6_hu_ni_tu_car.png" alt="Side view of car1" width="100"></td>
        <td>Concrete</td>
        <td>0.5</td>
        <td>-0.1</td>
        <td>-1.3</td>
        </tr>
        <tr>
        <td><img src="./img/overpass/car7_rush_car.png" alt="Side view of car1" width="100"></td>
        <td>Refuse truck</td>
        <td>0.8</td>
        <td>0</td>
        <td>-2.6</td>
        </tr>
        <tr>
        <td><img src="./img/overpass/car8_school_lolar_car.png" alt="Side view of car1" width="100"></td>
        <td>School bus</td>
        <td>0.3</td>
        <td>-0.3</td>
        <td>-1.7</td>
        </tr>
        <tr>
        <td><img src="./img/overpass/car9_statci_mesh .png" alt="Side view of car1" width="100"></td>
        <td>Tank</td>
        <td>1.3</td>
        <td>0</td>
        <td>-1.4</td>
        </tr>
    </tbody>
</table>


<table>
  <thead>
    <tr> 
      <th rowspan="3">Name</th>
      <th rowspan="3">Direction</th>
      <th colspan="7" style="text-align: center;">Camera</th>
      <th colspan="5" style="text-align: center;">LiDAR</th>
      <th colspan="5" style="text-align: center;">mmWave Radar</th>
    </tr>
    <tr>
      <th>X(m)</th>
      <th>Y(m)</th>
      <th>Z(m)</th>
      <th>Pitch</th>
      <th>Roll</th>
      <th>Yaw</th>
      <th>FoV Degrees(°)</th>
      <th>X(m)</th>
      <th>Y(m)</th>
      <th>Z(m)</th>
      <th>Vertical FoV(°)</th>
      <th>Horizontal FoV(°)</th>
      <th>X(m)</th>
      <th>Y(m)</th>
      <th>Z(m)</th>
      <th>Vertical FoV(°)</th>
      <th>Horizontal FoV(°)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">RSF</td> <!-- This cell now spans three rows -->
      <td>Left</td>
      <td>4.9</td>
      <td>0</td>
      <td>-7.2</td>
      <td>-25</td>
      <td>0</td>
      <td>90</td>
      <td>100</td>
      <td rowspan="3">-0.2</td>
      <td rowspan="3">0</td>
      <td rowspan="3">4.3</td>
      <td rowspan="3">-40~0</td>
      <td rowspan="3">-180~180</td>
      <td rowspan="3">-0.2</td>
      <td rowspan="3">0</td>
      <td rowspan="3">-0.8</td>
      <td rowspan="3">-10~10</td>
      <td rowspan="3">-90~90</td>
    </tr>
    <tr>
      <td>Middle</td>
      <td>5</td>
      <td>0</td>
      <td>-7.2</td>
      <td>-25</td>
      <td>0</td>
      <td>0</td>
      <td>100</td>
    </tr>
    <tr>
      <td>Right</td>
      <td>4.8</td>
      <td>0</td>
      <td>-7.2</td>
      <td>-25</td>
      <td>0</td>
      <td>-90</td>
      <td>100</td>
    </tr>
    <!-- Additional rows for other data as needed -->
  </tbody>
</table>



<table>
  <thead>
    <tr>
      <th rowspan="3">Name</th>
      <th colspan="3" style="text-align: center;">Communication Equipment</th>
    </tr>
    <tr>
      <th>X(m)</th>
      <th>Y(m)</th>
      <th>Z(m)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="1">RSF</td> <!-- This cell now spans three rows -->
      <td>0.8</td>
      <td>0</td>
      <td>-3.4</td>
    </tr>
    <!-- Additional rows for other data as needed -->
  </tbody>
</table>



**Direction:** This parameter represents the installation orientation of the sensor in the vehicle coordinate system, which can be one of the six directions: +x, -x, +y, -y, +z, -z. It describes the installation location and direction of the sensor relative to the vehicle body.

**X, Y, Z:** These three parameters collectively describe the three-dimensional spatial position of the sensor in the vehicle coordinate system, with the unit in meters. They provide the spatial coordinates of the sensor relative to the vehicle origin.

**Pitch, Roll, Yaw:** These three parameters describe the three rotational angles of the sensor in the vehicle coordinate system, with the unit in degrees. Pitch represents the pitch angle, Roll represents the roll angle, and Yaw represents the yaw angle. They define the spatial attitude of the sensor.

**Field of View(FoV) Degrees(°):** This parameter gives the total field of view angle of the sensor, with the unit in degrees. It reflects the range of the scene that the sensor can perceive.

**Vertical FoV(°):** This parameter gives the vertical field of view angle of the sensor, with the unit in degrees. It defines the sensor's perception range in the vertical direction.

**Horizontal FoV(°):** This parameter gives the horizontal field of view angle of the sensor, with the unit in degrees. It defines the sensor's perception range in the horizontal direction.


## Sensor Parameters

The camera and LiDAR sensors deployed on the vehicles in this scenario are of the same type. The specific sensor parameters are as follows:

| **Camera RGB Sensor Parameters**    | **Value** |
|-------------------------------------|-----------|
| **Width**                           | 1920      |
| **Height**                          | 1080      |
| **FOV**                             | 100。      |
| **AutoExpcosureSpeed**              | 100       |
| **AutoExposureBias**                | 0         |
| **AutoExposureMaxBrightness**       | 0.64      |
| **AutoExposureMinBrightness**       | 0.03      |
| **MotionBlurAmount**                | 0         |
| **TargetGamma**                     | 1.0       |

 | **Camera Depth Sensor Parameters** | **Value**                     |
|------------------------------------|-------------------------------|
| **Width**                          | 1920                          |
| **Height**                         | 1080                          |
| **FOV**                            | 100。                          |
| **MotionBlurAmount**               | 0                             |
| **Image Type**                     | DepthPlanner/DepthPerspective |
| **TargetGamma**                    | 1.0                           |
| **OrthoWidth**                     | 5.12                          |

| **LiDAR Sensor Parameters** |  **Value**  |
|-----------------------------|-------|
| **NumberOfChannels**        | 16    |
| **HorizontalFOVStart**      | -180  |
| **HorizontalFOVEnd**        | 180   |
| **VerticalFOVUpper**        | 15    |
| **VerticalFOVLower**        | -25   |


The camera and LiDAR sensors deployed on the RSFs in this scenario are also of the same type. The specific sensor parameters are as follows:

| **Camera RGB Sensor Parameters**    | **Value** |
|-------------------------------------|-----------|
| **Width**                           | 1920      |
| **Height**                          | 1080      |
| **FOV**                             | 100。      |
| **AutoExpcosureSpeed**              | 100       |
| **AutoExposureBias**                | 0         |
| **AutoExposureMaxBrightness**       | 0.64      |
| **AutoExposureMinBrightness**       | 0.03      |
| **MotionBlurAmount**                | 0         |
| **TargetGamma**                     | 1.0       |

 | **Camera Depth Sensor Parameters** | **Value**                     |
|------------------------------------|-------------------------------|
| **Width**                          | 1920                          |
| **Height**                         | 1080                          |
| **FOV**                            | 100。                          |
| **MotionBlurAmount**               | 0                             |
| **Image Type**                     | DepthPlanner/DepthPerspective |
| **TargetGamma**                    | 1.0                           |
| **OrthoWidth**                     | 5.12                          |

| **LiDAR Sensor Parameters** | **Value** |
|-----------------------------|-----------|
| **NumberOfChannels**        | 64        |
| **HorizontalFOVStart**      | -180      |
| **HorizontalFOVEnd**        | 180       |
| **VerticalFOVUpper**        | 0         |
| **VerticalFOVLower**        | -40       |


## RSF Position

The deployment of RSFs is the same across different traffic density scenarios, and the table below describes the positions of RSFs in each scenario.



<table>
  <thead>
    <tr>
      <th>ID</th>
      <th>X(m)</th>
      <th>Y(m)</th>
      <th>Z(m)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
  <td>RSF1</td>
  <td>19.1</td>
  <td>-128.5</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF2</td>
  <td>484.3</td>
  <td>-397.5</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF3</td>
  <td>375.1</td>
  <td>-396.5</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF4</td>
  <td>269.9</td>
  <td>-393.5</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF5</td>
  <td>163</td>
  <td>-391.7</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF6</td>
  <td>103</td>
  <td>-392.9</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF7</td>
  <td>58.216</td>
  <td>-438.73</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF8</td>
  <td>5.721</td>
  <td>-499.073</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF9</td>
  <td>-1.394</td>
  <td>-559.2</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF10</td>
  <td>-7.8</td>
  <td>-650.9</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF11</td>
  <td>-14.3</td>
  <td>-759.5</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF12</td>
  <td>-23.45</td>
  <td>-910.44</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF13</td>
  <td>-104.62</td>
  <td>-901.46</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF14</td>
  <td>-95.94</td>
  <td>-747.2</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF15</td>
  <td>-90.65</td>
  <td>-641.5</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF16</td>
  <td>-83.385</td>
  <td>-533.24</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF17</td>
  <td>-104.36</td>
  <td>-460.4</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF18</td>
  <td>-151.4</td>
  <td>-391.76</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF19</td>
  <td>-271.71</td>
  <td>-379.87</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF20</td>
  <td>-423.8</td>
  <td>-375</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF21</td>
  <td>-410.66</td>
  <td>-299.7</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF22</td>
  <td>-272.5</td>
  <td>-305.56</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF23</td>
  <td>-142.5</td>
  <td>-290.95</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF24</td>
  <td>-81.954</td>
  <td>-226.4</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF25</td>
  <td>-60.437</td>
  <td>-125.927</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF26</td>
  <td>-52.39</td>
  <td>9.62</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF27</td>
  <td>-44.05</td>
  <td>145.166</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF28</td>
  <td>33.35</td>
  <td>144.626</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF29</td>
  <td>25.65</td>
  <td>5.826</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF30</td>
  <td>35.36</td>
  <td>-223.61</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF31</td>
  <td>97.01</td>
  <td>-292.33</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF32</td>
  <td>177.64</td>
  <td>-315.52</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF33</td>
  <td>282.34</td>
  <td>-318.02</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF34</td>
  <td>417.14</td>
  <td>-319.62</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF35</td>
  <td>567.54</td>
  <td>-322.92</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF36</td>
  <td>-64.81</td>
  <td>-292.02</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF37</td>
  <td>4.68</td>
  <td>-403.63</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF38</td>
  <td>333.53976562</td>
  <td>-312.62234375</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF39</td>
  <td>200.95230469</td>
  <td>-307.12267578</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF40</td>
  <td>85.89654297</td>
  <td>-304.39339844</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF41</td>
  <td>-37.51589844</td>
  <td>-355.05207031</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF42</td>
  <td>-90.07994141</td>
  <td>-447.82425781</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF43</td>
  <td>-100.34967773</td>
  <td>-616.76746094</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF44</td>
  <td>-99.05029297</td>
  <td>-719.7675</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF45</td>
  <td>-26.15138672</td>
  <td>-752.38867188</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF46</td>
  <td>-22.02945801</td>
  <td>-635.67933594</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF47</td>
  <td>14.21632568</td>
  <td>-465.55484375</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF48</td>
  <td>77.63334473</td>
  <td>-361.11335938</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF49</td>
  <td>23.05393066</td>
  <td>-245.75470703</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF50</td>
  <td>-90.62886719</td>
  <td>-265.92591797</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF51</td>
  <td>-217.20259766</td>
  <td>-303.57550781</td>
  <td>0</td>
</tr>
<tr>
  <td>RSF52</td>
  <td>-334.31332031</td>
  <td>-309.71257812</td>
  <td>0</td>
</tr>
  </tbody>
</table>

**X, Y, Z:** These three parameters collectively describe the three-dimensional spatial position of the RSF in the scenario, with the unit in meters.

**Pitch, Roll, Yaw:** These three parameters describe the three rotational angles of the RSF in the scenario, with the unit in degrees. Pitch represents the pitch angle, Roll represents the roll angle, and Yaw represents the yaw angle. They define the spatial attitude of the RSF.



<img src="./img/overpass/overpass_OverLook.png" alt="Description of your image" width="600" height="400">

## Correspondence between vehicle types and Car ID under different intelligent agent densities

<table>
  <tr>
    <th rowspan="2">Type</th>
    <th colspan="3" style="text-align: center;">Car ID under different intelligent agent densities</th>
  </tr>
  <tr>
    <th>Low</th>
    <th>Medium</th>
    <th>High</th>
  </tr>
  <tr>
    <td>Blue SUV</td>
    <td>2 3 4 8 10 11 13 14 17 20 24 27 28 42 43 44 45 46 47 48</td>
    <td>2 3 4 8 10 11 13 14 17 20 24 27 28 42 43 44 45 46 47 48 52 53 57 59 67 68 70</td>
    <td>2 3 4 8 10 11 13 14 17 20 24 27 28 42 43 44 45 46 47 48 52 53 57 59 67 68 70 71 79 80 82 86 89 90 91 95</td>
  </tr>
  <tr>
    <td>Mini Cooper</td>
  <td>9 12 16 18 23 26 33 35 36 40</td>
  <td>9 12 16 18 23 26 33 35 36 40 50 51 60 63 69</td>
  <td>9 12 16 18 23 26 33 35 36 40 50 51 60 63 69 74 76 78 81 83 85 88 94 96 98</td>
  </tr>
  <tr>
    <td>Sedan</td>
  <td>1 5 6 15 22 30 32 38 41 49</td>
  <td>1 5 6 15 22 30 32 38 41 49 55 56 58 62 64 66</td>
  <td>1 5 6 15 22 30 32 38 41 49 55 56 58 62 64 66 75 92 93</td>
  </tr>
  <tr>
    <td>Pickup</td>
  <td>19 21 29 31 37</td>
  <td>19 21 29 31 37 65</td>
  <td>19 21 29 31 37 65</td>
  </tr>
  <tr>
    <td>Box truck</td>
  <td>7 39</td>
  <td>7 39</td>
  <td>7 39 73 84</td>
  </tr>
  <tr>
    <td>Concrete</td>
    <td>NaN</td>
    <td>NaN</td>
    <td>77</td>
  </tr>
  <tr>
    <td>Refuse truck</td>
    <td>NaN</td>
    <td>54</td>
    <td>54 72</td>
  </tr>
  <tr>
    <td>School bus</td>
  <td>25 34</td>
  <td>25 34</td>
  <td>25 34 99</td>
  </tr>
  <tr>
    <td>Tank</td>
    <td>NaN</td>
    <td>61</td>
    <td>61 87 97</td>
  </tr>
</table>
<p><strong>Note:</strong> In the table below, "NaN" indicates that the type is not applicable.</p>


## Intelligent Agent Trajectory

The vehicle pose information for each frame is represented as follows:

- The first 3 columns represent the x, y, and z coordinates of the vehicle in that frame, in meters.
- The next 3 columns represent the roll, pitch, and yaw angles of the vehicle in that frame, in radians.
- The last column represents the frame number.

| Traffic Density | Folder Link                                                  |
| --------------- | ------------------------------------------------------------ |
| Low             | [Low Traffic Density Folder](link/to/low/traffic/density/folder) |
| Medium          | [Medium Traffic Density Folder](link/to/medium/traffic/density/folder) |
| High            | [High Traffic Density Folder](link/to/medium/traffic/density/folder) |


It should be noted that the frame interval of each car in the simulation scene is a subset of the 1st frame to the 1500th frame. For example, Car1 enters the scene at the 1st frame and leaves the scene at the 828th frame. The valid frame interval is from the 1st frame to the 827th frame, and the 828th frame to the 1500th frame is an invalid frame interval, which does not provide perception and communication data.
We sort out the valid simulation intervals of each car in this scene as follows.

<table>
  <tr>
    <th rowspan="2">Car id</th>
    <th colspan="2" style="text-align: center;">Sunnyday_Morning_Low intelligent agent density</th>
</tr>
  <tr>
            <th>Start Frame</th>
            <th>Stop Frame</th>
  </tr>
        <tr><td>Car2</td><td>75</td><td>903</td></tr>
 
</table>
<p><strong>Note:</strong> In the table below, "NaN" indicates that The vehicle is not involved in the simulation.</p>

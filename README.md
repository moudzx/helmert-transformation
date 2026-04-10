# helmert-transformation

The Earth's actual shape is complex. <br>
The Earth is lumpy and irregular due to uneven mass distribution (mountains, ocean trenches, dense rock underground).

We use an ellipsoid as a reference shape to provide a smooth, mathematically manageable surface for calculating coordinates, distances and maps.

However, a single ellipsoid model cannot fit the entire planet perfectly at the same time; so we have multiple local/global datums that uses different ellipsoid models.

<img width="754" height="384" alt="gcs" src="https://github.com/user-attachments/assets/fb4e9311-b712-479a-9537-3c8001eb5511" /><br>

GPS uses a global datum (called WGS84), which uses an ellipsoid that is the "best fit" for the entire planet.
Different countries and organizations optimize their own local datums; so when the GPS satalleits produces a raw position in WGS84, this position is transformed into the correct local datums to match the map we use.

<h3>Transform coordinates</h3>
<img width="819" height="540" alt="transformation" src="https://github.com/user-attachments/assets/97514ac1-c334-4b10-beff-0444570691e3" /><br><br>


To transform from datum A to datum B<br>
This tool implement a three-stage datum transformation pipeline:<br>

1) Geographic A (lat/lon/h) -> Geocentric A (X/Y/Z) <br>
 <img width="554" height="346" alt="1" src="https://github.com/user-attachments/assets/20e04cd6-b6d8-491e-aced-a84aed5bdacf" /><br><br>
  
2) Geocentric A (X/Y/Z) -> Geocentric B (X/Y/Z) <br>
  <img width="1015" height="532" alt="2" src="https://github.com/user-attachments/assets/ddf104ab-5d62-4f83-b267-28bba4f96ea6" /><br><br>

 
3) Geocentric B (X/Y/Z) -> Geographic A (lat/lon/h) <br>
<img width="801" height="407" alt="3" src="https://github.com/user-attachments/assets/5daf17f5-7e37-4c45-82a6-5d31a43cf0bb" />
<img width="272" height="169" alt="4" src="https://github.com/user-attachments/assets/39a4b1f9-01d7-4033-96f0-a8496546db23" />





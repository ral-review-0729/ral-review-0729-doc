# Teleoperation Handle Installation and Testing

中文版本：

[遥操作手柄的安装与测试](https://www.notion.so/1bc33900bc8780569f76ff2b5a09b771?pvs=21)

Back to Table of Contents:

[Getting Started](https://www.notion.so/Getting-Started-1b433900bc8780c4a503e3490ce3e718?pvs=21)

## **Creating the Handle**

Download the PDF file, print the Markers using duplex printing with 100% scaling (no scaling)

[https://yaag.w5.cx/U2FsdGVkX18JWLtxzQSCU4InDpNB2fLr2vgDtLm-O_c6cfO3YwLUr62NVYAb4qclbq4g9Wy-3Zd2CEuDtzGGJ6HDWuJOhYf9vzKpqtEG2QqO6VteSwiTWs64P-3_8iVL748-uxiquYXUYx9g0anTqLcIUMvnPbz5va4snC_AxNJluMtnTQSIiYSAdX889XqneSYBclCPMF0OTVij74bEdOhPNRgE43P0nXax1TfdESs/code/astra_teleop/raw/refs/heads/main/src/astra_teleop/marker_array.pdf](https://yaag.w5.cx/U2FsdGVkX18JWLtxzQSCU4InDpNB2fLr2vgDtLm-O_c6cfO3YwLUr62NVYAb4qclbq4g9Wy-3Zd2CEuDtzGGJ6HDWuJOhYf9vzKpqtEG2QqO6VteSwiTWs64P-3_8iVL748-uxiquYXUYx9g0anTqLcIUMvnPbz5va4snC_AxNJluMtnTQSIiYSAdX889XqneSYBclCPMF0OTVij74bEdOhPNRgE43P0nXax1TfdESs/code/astra_teleop/raw/refs/heads/main/src/astra_teleop/marker_array.pdf)

![image.png](Teleoperation%20Handle%20Installation%20and%20Testing%201c033900bc8780008c97cf65191f4bf2/image.png)

![image.png](Teleoperation%20Handle%20Installation%20and%20Testing%201c033900bc8780008c97cf65191f4bf2/image%201.png)

Cut along the dotted lines. Marker IDs and orientation dots are marked on the back. Note: The right handle uses Markers ID 0-16. The left handle uses Markers ID 18-30. Marker ID 17 should be ignored. Apply Markers counterclockwise from the top using double-sided tape for best results

**Right Handle**

![image.png](Teleoperation%20Handle%20Installation%20and%20Testing%201c033900bc8780008c97cf65191f4bf2/image%202.png)

Top View

![image.png](Teleoperation%20Handle%20Installation%20and%20Testing%201c033900bc8780008c97cf65191f4bf2/image%203.png)

Front View

![image.png](Teleoperation%20Handle%20Installation%20and%20Testing%201c033900bc8780008c97cf65191f4bf2/image%204.png)

Left View

![image.png](Teleoperation%20Handle%20Installation%20and%20Testing%201c033900bc8780008c97cf65191f4bf2/image%205.png)

Back View

![image.png](Teleoperation%20Handle%20Installation%20and%20Testing%201c033900bc8780008c97cf65191f4bf2/image%206.png)

Right View

**Left Handle**

![image.png](Teleoperation%20Handle%20Installation%20and%20Testing%201c033900bc8780008c97cf65191f4bf2/image%207.png)

Top View

![image.png](Teleoperation%20Handle%20Installation%20and%20Testing%201c033900bc8780008c97cf65191f4bf2/image%208.png)

Front View

![image.png](Teleoperation%20Handle%20Installation%20and%20Testing%201c033900bc8780008c97cf65191f4bf2/image%209.png)

Left View

![image.png](Teleoperation%20Handle%20Installation%20and%20Testing%201c033900bc8780008c97cf65191f4bf2/image%2010.png)

Back View

![image.png](Teleoperation%20Handle%20Installation%20and%20Testing%201c033900bc8780008c97cf65191f4bf2/image%2011.png)

Right View

## **Creating Calibration Board**

Download the calibration board file and attach it to a flat surface:

[https://yaag.w5.cx/U2FsdGVkX18JWLtxzQSCU4InDpNB2fLr2vgDtLm-O_c6cfO3YwLUr62NVYAb4qclbq4g9Wy-3Zd2CEuDtzGGJ6HDWuJOhYf9vzKpqtEG2QqO6VteSwiTWs64P-3_8iVL748-uxiquYXUYx9g0anTqLcIUMvnPbz5va4snC_AxNJluMtnTQSIiYSAdX889XqneSYBclCPMF0OTVij74bEdOhPNRgE43P0nXax1TfdESs/code/astra_teleop/raw/refs/heads/main/src/astra_teleop/calibration_board.png](https://yaag.w5.cx/U2FsdGVkX18JWLtxzQSCU4InDpNB2fLr2vgDtLm-O_c6cfO3YwLUr62NVYAb4qclbq4g9Wy-3Zd2CEuDtzGGJ6HDWuJOhYf9vzKpqtEG2QqO6VteSwiTWs64P-3_8iVL748-uxiquYXUYx9g0anTqLcIUMvnPbz5va4snC_AxNJluMtnTQSIiYSAdX889XqneSYBclCPMF0OTVij74bEdOhPNRgE43P0nXax1TfdESs/code/astra_teleop/raw/refs/heads/main/src/astra_teleop/calibration_board.png)

## Camera Intrinsic Calibration (Test)

Install dependencies:

```bash
# Install Dependance First
git clone https://yaag.w5.cx/U2FsdGVkX18JWLtxzQSCU4InDpNB2fLr2vgDtLm-O_c6cfO3YwLUr62NVYAb4qclbq4g9Wy-3Zd2CEuDtzGGJ6HDWuJOhYf9vzKpqtEG2QqO6VteSwiTWs64P-3_8iVL748-uxiquYXUYx9g0anTqLcIUMvnPbz5va4snC_AxNJluMtnTQSIiYSAdX889XqneSYBclCPMF0OTVij74bEdOhPNRgE43P0nXax1TfdESs/code/astra_teleop.git
cd astra_teleop
pip install -e .
```

Collect calibration images:

```bash
python -m astra_teleop.calibration_collect -d /dev/video0 -c ./calibration_images
```

Move the calibration board in front of the camera:

![image.png](Teleoperation%20Handle%20Installation%20and%20Testing%201c033900bc8780008c97cf65191f4bf2/image%2012.png)

Process calibration images:

```bash
python -m astra_teleop.calibration_process -c ./calibration_images
```

Sample output (results saved to `calibration_images/calibration_results_{%Y%m%d%H%M%S}.yaml`):

```prolog
...
filename = calibration_images/0054.png
len(charuco_ids) = 24
len(object_points) = 24
len(image_points) = 24
filename = calibration_images/0040.png
len(charuco_ids) = 24
len(object_points) = 24
len(image_points) = 24

POINTS USED FOR CALIBRATION
number of images with suitable points = 55
len(all_object_points) = 55
len(all_image_points) = 55

calibration_results =
{'calibration_date': datetime.datetime(2025, 3, 20, 16, 9, 15, 858170),
 'camera_matrix': array([[1.39009897e+03, 0.00000000e+00, 9.91544788e+02],
       [0.00000000e+00, 1.39313263e+03, 5.51069328e+02],
       [0.00000000e+00, 0.00000000e+00, 1.00000000e+00]]),
 'distortion_coefficients': array([[ 0.01798524,  0.12828308, -0.00238978,  0.00725993, -0.27386293]]),
 'image_size': [1080, 1920, 3],
 'number_of_corresponding_points_used': 1255,
 'number_of_images_processed': 60,
 'number_of_images_used': 55,
 'projection_error': 0.880561854112254}

saved calibration results to calibration_images/calibration_results_20250320160915.yaml
```

## Handle Detection (Test)

Detect markers:

```bash
python -m astra_teleop.calibration_process -c ./calibration_images
```

Displays detected markers and transformation matrix relative to camera coordinate system (Fc):

![image.png](Teleoperation%20Handle%20Installation%20and%20Testing%201c033900bc8780008c97cf65191f4bf2/image%2013.png)

![image.png](Teleoperation%20Handle%20Installation%20and%20Testing%201c033900bc8780008c97cf65191f4bf2/image%2014.png)

## Improving Detection Accuracy

Higher camera resolution improves accuracy but reduces speed. CORNER_REFINE_APRILTAG improves precision but increases processing time. Web client uses 720p resolution and disables CORNER_REFINE_APRILTAG for real-time performance.
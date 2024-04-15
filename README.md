<div align="center">

# Smart Traffic Detection using YOLO-5 and Deep-Sort

</div>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()

</div>

<div align="center">
<img src="assets/output.gif" width="1000px" height="600px">
</div>

### On CPU - `12 to 15 FPS`

### Python version - `Python 3.8.8 - Python 3.10.10`

## Pre-requisites :

1. Clone the Repository [vehicle-counting-yolov5](https://github.com/VishalJx/VishalJx-Smart-Traffic-Detection-Using-YOLO-v5.git)

```bash
mkdir LaneSense
cd LaneSense
git clone https://github.com/VishalJx/VishalJx-Smart-Traffic-Detection-Using-YOLO-v5.git
```

2. Clone the legacy Yolo-v5 Repository

```bash
git clone https://github.com/ultralytics/yolov5.git
```

3. Install the libraries

```bash
pip install -r requirements.txt
```

## Directory Structure :

After completing the above steps your directory should look like somewhat as of below structure

- `vehicle-counting-yolov5`
  - deep_sort
  - yolov5
  - input.mp4
  - yolov5s.pt
  - tracker.py
  - requirements.txt

## Run the algorithm

```bash
python tracker.py
# This will download model weight - yolov5s.pt to base folder on first execution.
```

## Working Idea

[Graphical Demo](https://github.com/VishalJx/VishalJx-Smart-Traffic-Detection-Using-YOLO-v5/blob/main/stimulation.mp4)

- The main idea is to examine live video feeds of traffic intersections using YOLO(You Only Look Once) algorithm.
- The system determines the **lane-specific car density** by detecting and tracking vehicles.
- Afterwards, lanes with a higher vehicle density receive green signals, which maximizes traffic flow and reduces wait times.

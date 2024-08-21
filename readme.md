
# RedLightGuardian - Traffic Signal Violation Detection System

## Overview
This project leverages Computer Vision and YOLOv8 to identify vehicles violating traffic signals with high precision. By using a custom-trained YOLOv8 model, the system accurately detects red light violations. Once a violation is detected, the system captures the vehicle's number plate, retrieves the registration number, and generates an automated challan based on the database of vehicle registrations. TensorFlow and Convolutional Neural Networks (CNN) are used to process and analyze traffic footage, aiding law enforcement and traffic management.

## Project Goals
- Enhance traffic management.
- Support law enforcement by accurately identifying vehicles that violate traffic signals.
- Automatically generate and issue challans for offending vehicles.

## Process
1. **Detection of Traffic Violations**:
   - Utilize a YOLOv8 model trained on a custom vehicle dataset to detect red light violations.
   - Detect when a vehicle crosses predetermined virtual lines at a traffic signal.
   
2. **Number Plate Recognition**:
   - Capture the number plate of the violating vehicle.
   - Use Convolutional Neural Networks (CNN) within TensorFlow to process and recognize the registration number from the captured images.
   
3. **Challan Generation**:
   - Retrieve the vehicle's registration details from a database.
   - Automatically generate and issue a challan (traffic ticket) to the vehicle owner.

## Features
- **High Precision Detection**: Custom-trained YOLOv8 model for accurate detection of red light violations.
- **Automated Number Plate Recognition**: CNNs in TensorFlow enable reliable reading of number plates from traffic footage.
- **Seamless Integration**: Efficient processing of traffic footage through the integration of TensorFlow with detection and recognition modules.
- **Automated Challan Issuance**: Streamlined enforcement process by automatically generating and issuing challans based on retrieved registration data.

## ANPR System

In addition to detecting traffic violations, an Automatic Number Plate Recognition (ANPR) system is used for real-time vehicle license plate detection. This system can be used in a variety of settings, including toll tax collection and parking systems. 

The ANPR system leverages YOLOv5 for number plate detection and PaddleOCR for recognizing characters on the detected plates. NorFair is utilized for object tracking to ensure the most accurate OCR results.

**TechStack:**
- OpenCV
- PyTorch
- YOLOv5
- PaddleOCR
- NorFair

### Usage Instructions for ANPR:
To detect number plates in a video feed:

```bash
python3 anpr-system.py \
    --weights yolo_weights.pt \
    --input input_video.mp4 \
    --output output_video.mp4 \
    --csv all_number_plates.csv
```

For more information and access to the repository, check out [ANPR-System Repo](https://github.com/Tkvmaster/ANPR-System.git).

## Installation

1. Clone the repository:

   ```bash
   https://github.com/Jasmit7/RedLightGuardian
   ```

2. Navigate to the project directory:

   ```bash
   cd RedLightGuardian
   ```

## Usage
The system will automatically process the traffic footage, detect red light violations, capture number plates, and issue challans.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements
- Special thanks to the contributors of YOLOv8, TensorFlow, and the ANPR System.
- Acknowledgment to any other libraries or resources used in the project.
```


# Computer-Vision-Icon-Matching
The **Computer Vision Icon Matching** project processes PDFs (Schedule and Room Plan) to identify and count matching icons using computer vision techniques. It leverages OpenCV for contour detection, preprocessing, and template matching, ensuring efficient and accurate visual component identification and analysis for document automation tasks.

## Features
- PDF-to-image conversion using `pdf2image`.
- Grayscale conversion and contour detection to extract icons from the PDFs.
- Image preprocessing with histogram equalization and adaptive thresholding.
- Template matching using OpenCV’s `cv2.matchTemplate` to identify and count matching components.
- Visualization of icon extraction and processing steps.


## Code Overview

The code follows these steps:

1. **PDF Conversion**: The `extract_icons_from_pdf` function converts PDF pages into images and extracts grayscale icons using contour detection.
2. **Preprocessing**: The `preprocess_special_icon` function applies thresholding, edge detection, and morphological operations to enhance icon clarity.
3. **Icon Matching**: The `count_matching_icons` function matches icons from the Schedule to those in the Room Plan using template matching (`cv2.matchTemplate`) and records occurrences.
4. **Visualization**: The `visualize_icon_processing` function visualizes the various processing stages for specific icons to debug and refine the matching process.

## Output

The program outputs a count of each icon from the Schedule found in the Room Plan, with visualizations for icons that need further inspection.

## Assumptions

- The PDFs contain icons in image form. If they are vector graphics, they must be rasterized before processing.
- The icons in both PDFs are similar in size and appearance; otherwise, additional preprocessing (like resizing or rotation) may be required.

## Troubleshooting

- Ensure that all dependencies are installed from the `requirements.txt`.
- If icon matching is inconsistent, try adjusting the threshold value in `cv2.matchTemplate` or modifying preprocessing parameters.

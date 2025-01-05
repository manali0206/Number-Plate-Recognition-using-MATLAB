# Number-Plate-Recognition-using-MATLAB
The License Plate Detection System is a MATLAB-based project designed to identify and extract the license plate region from a vehicle image. It begins by allowing the user to select an image file using uigetfile, after which the image is converted to grayscale for simplified processing. The code then crops the lower third of the image, assuming the license plate is positioned in this region. This cropped area is thresholded to create a binary image, where pixel intensities above a certain value (150) are set to white (1), and others to black (0). To improve the binary image, morphological operations such as hole filling and median filtering are applied multiple times, removing noise and enhancing the plate region.

Next, connected component analysis is performed to label distinct regions in the processed image. Region properties such as area and orientation are analyzed to filter out irrelevant regions, keeping only those with characteristics matching a license plate (e.g., appropriate size and orientation). The remaining region, corresponding to the license plate, is extracted using bounding box coordinates. This bounding box is adjusted slightly to ensure accurate cropping of the license plate, which is then displayed as the final output. This system lays the groundwork for license plate recognition by isolating the plate region, enabling further steps like Optical Character Recognition (OCR) for extracting alphanumeric characters.

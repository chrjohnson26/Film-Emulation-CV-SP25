# Film-Emulation-CV-SP25

This repository contains a High Dynamic Range (HDR) image processing pipeline, implementing the Debevec algorithm for HDR reconstruction and the Reinhard operator for tone mapping. Check out [our HDR dataset on Google Drive](https://drive.google.com/drive/folders/1f8BAv3cZWv1MtfIDVDXO2MoX68-QR-a4?usp=sharing) and [the processed HDR images on Google Drive](https://drive.google.com/drive/folders/1Jsv7LVcdsvOUPuSliDZ4YODO_5oRG9gu?usp=share_link)

## Description

Our HDR pipeline takes multiple exposures of the same scene and combines them to create an image with extended dynamic range. This allows for the preservation of details in both bright and dark regions of a scene that would be lost in a single exposure.

The pipeline consists of three main components:
1. **Debevec Algorithm** - Recovers the camera response function and creates a radiance map
2. **Reinhard Tone Mapping** - Maps the high dynamic range image to a displayable range
3. **Bloom Effect** - Adds a subtle glow to bright areas

## Demo

To run a demonstration of our HDR pipeline:

1. Download [our HDR dataset from Google Drive](https://drive.google.com/drive/folders/1f8BAv3cZWv1MtfIDVDXO2MoX68-QR-a4?usp=share_link)
2. From the Google Drive, download the folder titled "8" which contains a sample exposure stack
3. Clone this repository: `git clone https://github.com/yourusername/hdr-pipeline.git`
4. Install the required dependencies: `pip install -r requirements.txt`
5. Run each cell of the `main.ipynb` Jupyter notebook

The demo will process the exposure stack from scene 8, displaying:
- The recovered camera response function
- The resulting HDR radiance map
- The final tone-mapped image with bloom effects

This demonstration provides a complete walkthrough of our pipeline's capabilities using a representative scene from our dataset.

## Requirements

The primary dependencies are listed in `requirements.txt`:

```bash
pip install -r requirements.txt
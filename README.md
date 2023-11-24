# Virtual histological staining of unlabeled autopsy tissue

This repository contains codes and images necessary for reproducing the deep learning-based virtual staining of unstained autopsy tissue slides.

## Network Training Testing Codes

You can find the codes for network testing in this folder, due to the size restriction, the model file can be downloaded at xx:

1. **Training procedure**: To perform the training of autopsy virtual staining network used the RegiStain framework proposed in our work, simply run `train_stage2_seperate_train_by_iters.py`. Before executing the codes, please make sure to update the paths of the training and validation images within the code. And this RegiStain framework is not restricted in the virtual staining tasks. It is friendly to be adapted to other supervised image-to-image translation tasks which require the pixel-level registration of the paired data. 

2. **Testing Procedure**: To perform the testing and generate virtually stained H&E images using the autofluorescence channels of the unlabeled autopsy tissue section as the input, simply run `test_G.py`. Before executing the codes, please make sure to update the paths of the testing images within the code.

3. **Dependencies**: The required Python packages to run the codes are listed in `dependencies.yml`.

4. **Execution Time**: Running the testing codes for a set of 10 example images takes approximately 26 seconds using an Nvidia GeForce RTX 3090 GPU.

## Example Images

Example images can be found at xx. Here's what you will find:


- **Input**: Autofluorescence images of unstained autopsy tissue sections; each FOV corresponds to a `.mat` file, with the 1st channel representing the DAPI channel and the 2nd channel representing the TxRed channel.
- **Output**: Virtually stained H&E images generated by the network model.
- **Ground Truth**: Histochemically stained H&E images for reference/comparison.


10 individual FOVs are provided as example images. Each FOV measures 2048 x 2048 pixels, corresponding to roughly 333 x 333 µm².
The 10 FOVs are labeled from "001" to "010".
  - "001"-"005": These correspond to tissue regions suffering from severe autolysis, rendering staining artifacts in the histochemically stained images (ground truth).
  - "006"-"010": These correspond to well-preserved tissue regions with high histochemical staining quality.


## Support

Should you encounter any problems while running the codes, please feel free to contact [liyuzhu@ucla.edu](mailto:liyuzhu@ucla.edu) or [jxlli@ucla.edu](mailto:jxlli@ucla.edu).


## License

This project is open-sourced under the Apache License 2.0. See the [LICENSE](LICENSE) file for details.

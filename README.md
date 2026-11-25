[![Abcdspec-compliant](https://img.shields.io/badge/ABCD_Spec-v1.1-green.svg)](https://github.com/brain-life/abcd-spec)
[![Run on Brainlife.io](https://img.shields.io/badge/Brainlife-bl.app.313-blue.svg)](https://doi.org/10.25663/brainlife.app.313)

### Author
- Sophia Vinci-Booher (svincibo@indiana.edu)

### Contributor
- Soichi Hayashi (hayashis@iu.edu)

### Project director
- Franco Pestilli (franpest@indiana.edu)

# app-combineROI

<!-- brainlife-app:begin (generated from the App manifest; edit the manifest, not this block) -->

> **Combines two ROI datasets into one by copying all ROI NIfTI files from both inputs into a single ROI folder, renaming duplicates.**

This app will combine two ROI datatype datasets into one ROI datatype dataset. If, for example, there are 3 rois in the first ROI dataset and 2 rois in the second ROI dataset, the output ROI data set will contain 5 rois. NOTE: This app can be used to extract one roi from an ROI dataset. If you enter the same roi in the roi1 and roi2 fields, the resulting ROI will simply be that roi.

| | |
|---|---|
| 📥 **Inputs** | `neuro/rois` ×2 |
| 📤 **Outputs** | `neuro/rois` |
| ⚙️ **Resources** | 1 CPUs |
| 🔗 **Run it** | [doi.org/10.25663/brainlife.app.313](https://doi.org/10.25663/brainlife.app.313) |

#### 📥 Inputs

| Input | Datatype | Required | Description |
|---|---|---|---|
| `roi1` | `neuro/rois` | yes | First ROI dataset (folder of roi NIfTI files). Must be in the same space as roi2; the App does not check alignment. |
| `roi2` | `neuro/rois` | yes | Second ROI dataset; files whose names already exist in roi1 are copied with a -2 suffix. Must be in the same space as roi1. |

#### 📤 Outputs

| Output | Datatype | Description |
|---|---|---|
| `output` | `neuro/rois` | ROI dataset whose rois folder contains every ROI of both inputs. |

📚 **References used by this App:**
- Avesani P. et al. The open diffusion data derivatives, brain data upcycling via integrated publishing of derivatives and reproducible open cloud services. Sci Data 6, 69 (2019). [doi:10.1038/s41597-019-0073-y](https://doi.org/10.1038/s41597-019-0073-y)

<!-- brainlife-app:end -->

This app will combine multiple ROI datatypes into one ROI file. The input data are ROI brainlife datatypes (two or more) and the output data is one ROI brainlife datatype. The output ROI will contain all of the roi.nii.gz files that were contained within each of the input ROI brainlife datatypes.

NOTE: The rois supplied MUST BE IN ALIGNMENT with one another -- they must
be in the same space. If the rois to be combined are not in alignment with
one another, then the output of this app will be UNUSABLE
(even though the app will not fail to complete).

If, for example, the the first input ROI has 2 rois inside of it and the second input ROI has 3 rois 
inside of it, then the output will be an ROI dataset with 5 rois inside of it. 

### Funding 
[![NSF-BCS-1734853](https://img.shields.io/badge/NSF_BCS-1734853-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1734853)
[![NSF-BCS-1636893](https://img.shields.io/badge/NSF_BCS-1636893-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1636893)
[![NSF-ACI-1916518](https://img.shields.io/badge/NSF_ACI-1916518-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1916518)
[![NSF-IIS-1912270](https://img.shields.io/badge/NSF_IIS-1912270-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1912270)
[![NSF-SMA-2004877](https://img.shields.io/badge/NSF_SMA-2004877-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=2004877)
[![NIH-NIBIB-R01EB029272](https://img.shields.io/badge/NIH_NIBIB-R01EB029272-green.svg)](https://grantome.com/grant/NIH/R01-EB029272-01)
[![NIH-T32-HD007475](https://img.shields.io/badge/NIH_T32-HD007475-green.svg)](https://www.nichd.nih.gov/grants-contracts/training-careers/extramural/institutional)

### Citations

We kindly ask that you cite the following articles when publishing papers and code using this code.

Avesani, P., McPherson, B., Hayashi, S. et al. The open diffusion data derivatives, brain data upcycling via integrated publishing of derivatives and reproducible open cloud services. Sci Data 6, 69 (2019). https://doi.org/10.1038/s41597-019-0073-y

MIT Copyright (c) 2020 brainlife.io The University of Texas at Austin and Indiana University### On Brainlife.io

You can submit this App online at [https://doi.org/10.25663/brainlife.app.313](https://doi.org/10.25663/brainlife.app.313) via the "Execute" tab.

### Running Locally (on your machine)

1. git clone this repo.
2. Inside the cloned directory, create `config.json` with something like the following content with paths to your input files.

```json
{
"rois1": "testdata/roi1/",
"rois2": "testdata/roi2/"
}
```

3. Launch the App by executing `main`

```bash
./main
```

### Sample Datasets

If you don't have your own input file, you can download sample datasets from Brainlife.io, or you can use [Brainlife CLI](https://github.com/brain-life/cli).

## Output

All output files will be generated under the current working directory (pwd). The main output of this App is the ROI folder that contains .nii.gz files for each ROI in the input folders. This file contains following object.

### Dependencies

None.

# The-Table-Cell-Recognition-TCR

The Table Cell Recognition (TCR) dataset is designed to address the limitations of existing table structure recognition datasets, specifically by providing fine-grained cell-scale annotations that include table footers—a component often overlooked in prior work. This section details the data acquisition, annotation process, quality assurance mechanisms, and distribution of the dataset, ensuring a comprehensive understanding of its construction and utility in enhancing table recognition models.

## 📂 Dataset Contents

The "data" folder includes:

- **TABLE_IMG**: 
  -  5,826 table images. The tables are cropped from [**TableBank**](https://github.com/doc-analysis/TableBank).
- **TABLE_LABEL**:
  - Each annotation file is a plain **TXT** file corresponding to a table image, following the **YOLO format**:
    [class index] [x_center] [y_center] [width] [height]
  - All coordinates are **normalized** to the range `[0,1]`, relative to the image dimensions.
### **Class Index Mapping**
| Class Index | Description   |
|-------------|---------------|
| **0**       | Single Cell   |
| **1**       | Merged Cell   |
| **2**       | Header        |
| **3**       | Footer        |

## 🔎 Use Cases
- Table detection and structure recognition
- Table-to-structured-data extraction
- Fine-tuning deep learning models for document layout analysis

## 📖 Citation
If you use this dataset in your research, please cite:
```bibtex
@dataset{TCR2025
}
```

## 📜 License
This dataset is released under the [Apache License 2.0](LICENSE).

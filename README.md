# ghana-cmf-vlm
Three-stream multimodal fusion for plant disease detection in Twi
# Ghana CMF-VLM: Multimodal Plant Disease Detection

Three-stream fusion model combining vision, Twi language, and sensors for Ghanaian smallholder farmers. Implementation of Liu et al. 2025 adapted for low-resource languages.

## Results
- **Overall accuracy:** 99.94% on 5,431 held-out PlantVillage images (38 classes)
- **Critical crops (previously 0-25% with CLIP):**
    - Tomato Late Blight: 191/191 (100%)
    - Maize Northern Blight: 99/99 (100%)
    - Maize Healthy: 116/116 (100%)

## Structure
- `notebooks/` — Kaggle training notebooks
- `src/model.py` — EfficientNet + AfroXLMR + LSTM fusion
- `results/` — confusion matrices and metrics

## Reproduce
1. Add PlantVillage dataset from Kaggle
2. `pip install -r requirements.txt`
3. Run `notebooks/02_fusion_training.ipynb` on GPU

## Limitations
PlantVillage uses lab images. Field performance in Ghana expected lower. See Issues for field-test plan.

## Citation
Based on CMDF-VLM (Liu et al., 2025). Uses AfroXLMR-base for Twi.

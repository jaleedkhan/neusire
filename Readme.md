# NeuSyRE: A Neuro-Symbolic Visual Understanding and Reasoning Framework based on Scene Graph Enrichment

![SWJ-BlockDiagram](https://user-images.githubusercontent.com/71158275/226135008-08114a1d-da4d-4e24-bd00-a0583d8eaab9.jpg)

## Requirements
- Ubuntu 18.04
- CUDA 10.1
- Python 3.7
- PyTorch 1.4
- KGTK 0.5

## Downloads
- [VG dataset](https://visualgenome.org/api/v0/api_home.html)
- [CSKG embeddings](https://drive.google.com/drive/u/1/folders/16347KHSloJJZIbgC9V5gH7_pRx0CzjPQ)
- [COCO dataset](https://cocodataset.org/#captions-2015)
- [Faster RCNN pretrained network](https://1drv.ms/u/s!AmRLLNf6bzcir8xemVHbqPBrvjjtQg?e=hAhYCw)
- [SGG pretrained network](https://1drv.ms/u/s!AmRLLNf6bzcir9x7OYb6sKBlzoXuYA?e=s3Y602)
- [Image Captioning Pretrained Network and Preprocessed Dataset](https://drive.google.com/drive/folders/1mCx8R8d36ZpUSoVZKExs0FDA_IXiAiZA?usp=sharing)
- [Image Generation Pretrained Network](https://github.com/google/sg2im)

## Code
### Scene Graph Generation and Enrichment
- [Scene Graph Generation evaluation on VG/COCO dataset](SGG/SGG_Evaluation.ipynb)
- [Scene Graph Enrichment using CSKG with evaluation](CSKG/j_SG_CSKG.ipynb)
### Downstream Tasks
- [Image Captioning using COCO dataset](SubGC/SubGC.ipynb) 
- [Image Captioning evaluation](SubGC/SubGC_evaluation.ipynb)
- [Image Generation using VG dataset](SG2IM/SG2IM.ipynb)

## Important Directories
### VG dataset
- Generated scene graphs of all images (in Eval_IO/vg/0_images) in the dataset are saved to Eval_IO/vg/1_pred_scene_graphs
- Enriched scene graphs are saved to Eval_IO/vg/2_enriched_scene_graphs
- Generated images are saved to Eval_IO/vg/3_generated_images
### COCO dataset
- Generated scene graphs of all images (in Eval_IO/coco/0_images) in the dataset are saved to Eval_IO/coco/1_pred_scene_graphs
- Enriched scene graphs are saved to Eval_IO/coco/2_enriched_scene_graphs
- Generated captions are saved to Eval_IO/coco/3_captions

## Steps to run the code
- Download the datasets and place them in the given directories, and follow the following sequence to run the code in the notebooks. 
- Run all cells step-by-step in [SGG/SGG.ipynb](SGG/SGG.ipynb) to install required packages, set up the SGG module, train the SGG deep learning pipeline, and test it on sample image(s).
- Run all cells step-by-step in [SGG/SGG_Evaluation.ipynb](SGG/SGG_Evaluation.ipynb) to run the trained SGG pipeline on all images in the dataset and generate scene graphs. (This step needs to be repeated for each dataset)
  - The variables 'eval_inp_img' and 'eval_outp_sg' in the first cell should point to the directory containing input images and the directory where the generated scene graphs should be placed, respectively.
  - The evaluation (calculation of recall metrics) is done along with the scene graph enrichment step in the next part. 
- Run all cells step-by-step in [CSKG/j_SG_CSKG.ipynb](CSKG/j_SG_CSKG.ipynb) to set up the knowledge enrichment module, enrich all scene graphs generated in the previous step with common sense knowledge, and to evaluate the recall measures for scene graphs and enriched scene graphs.
  - Once the enriched scene graphs have been created and saved for all images in the dataset, the code in the following cell will calculate the recall scores (R@K and mR@K for K = 20, 50, 100 for each dataset)
- Run all cells step-by-step in [SubGC/SubGC.ipynb](SubGC/SubGC.ipynb) to set up the image captioning module and test it on sample image(s). 
- Run all cells step-by-step in [SubGC/SubGC_Evaluation.ipynb](SubGC/SubGC_Evaluation.ipynb) to run the trained image captioning module on scene graphs and enriched scene graphs generated in the previous steps, and calculate the evaluation metrics.
- Change the paths to datasets and other resources in the code to your local paths where needed.

## Citations
```
@article{khan2023neusyre,
  title={NeuSyRE: Neuro-Symbolic Visual Understanding and Reasoning Framework based on Scene Graph Enrichment},
  author={Khan, Muhammad Jaleed and Breslin, John G and Curry, Edward},
  journal={Semantic Web},
  year={2022}
}

@inproceedings{khan2022expressive,
  title={Expressive Scene Graph Generation Using Commonsense Knowledge Infusion for Visual Understanding and Reasoning},
  author={Khan, Muhammad Jaleed and Breslin, John G and Curry, Edward},
  booktitle={The Semantic Web: 19th International Conference, ESWC 2022, Hersonissos, Crete, Greece, May 29--June 2, 2022, Proceedings},
  pages={93--112},
  year={2022},
  organization={Springer}
}

@article{khan2022common,
  title={Common Sense Knowledge Infusion for Visual Understanding and Reasoning: Approaches, Challenges, and Applications},
  author={Khan, Muhammad Jaleed and Breslin, John G and Curry, Edward},
  journal={IEEE Internet Computing},
  volume={26},
  number={4},
  pages={21--27},
  year={2022},
  publisher={IEEE}
}

```

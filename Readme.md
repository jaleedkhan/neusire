# NeuSyRE: A Neuro-Symbolic Visual Understanding and Reasoning Framework based on Scene Graph Enrichment

![SWJ-BlockDiagram](https://user-images.githubusercontent.com/71158275/226135008-08114a1d-da4d-4e24-bd00-a0583d8eaab9.jpg)

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

<!---
## Citations
```
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
--->

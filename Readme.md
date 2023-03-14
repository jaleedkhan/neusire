# NeuSyRE: A Neuro-Symbolic Visual Understanding and Reasoning Framework based on Scene Graph Enrichment
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
Image Captioning:
- [Image Captioning using COCO dataset](SubGC/SubGC.ipynb) 
- [Image Captioning evaluation](SubGC/SubGC_evaluation.ipynb)
Image Generation:
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

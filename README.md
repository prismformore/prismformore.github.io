# SegGen: Supercharging Segmentation Models with Text2Mask and Mask2Img Synthesis
Hanrong Ye, Jason Kuen, Qing Liu, Zhe Lin, Brian Price, Dan Xu 

[Paper](https://arxiv.org/abs/2311.03355) | [Project Page](https://seggenerator.github.io/)


![teaser_coco_website](https://github.com/prismformore/seggen/assets/14089338/e9160e82-72d2-4319-8334-7f3255994b86) \
**SegGen** not only significantly improves the performance of state-of-the-art segmentation models on standard benchmarks (COCO and ADE20K), but also boosts the generalization ability towards challenging images from unseen domains. The three columns on the left are from PASCAL dataset and the three on the right are synthesized by generative model Kandinsky 2.


![image](https://github.com/prismformore/seggen/assets/14089338/de916a15-702f-4afe-a508-8f8726132216)\
**Workflow of SegGen**: We introduce two generative models: a text-to-mask (Text2Mask) generation model and a mask-to-image( Mask2Img) generation model, based on which we design two approaches for generating new segmentation training samples: MaskSyn and ImgSyn. (a) MaskSyn focuses on generating new segmentation masks. It first extracts the caption of the real image as a text prompt and uses it to generate new masks with the Text2Mask model. Then, the new masks and text prompt are fed into the Mask2Img model to produce the corresponding new images. (b) ImgSyn focuses on the synthesis of new images. It directly inputs human-labeled masks and text prompts into the Mask2Img model to generate new images.


![masksyn_0](https://github.com/prismformore/seggen/assets/14089338/57008a5a-065b-4882-aea7-b418e9229bf3)\
**MaskSyn** synthesizes new mask-image pairs. It first generates synthetic segmentation masks with a Text2Mask model, and then synthesizes new images with a Mask2Image model.


![imgsyn_0](https://github.com/prismformore/seggen/assets/14089338/2b852f1e-4546-4034-a7a2-dde1b3fc2124)\
**ImgSyn** synthesizes new images. It generates new images conditioned on human-annotated segmentation masks with a Mask2Image model.


# BibTeX
```
@article{ye2023seggen,
  title={SegGen: Supercharging Segmentation Models with Text2Mask and Mask2Img Synthesis},
  author={Ye, Hanrong and Kuen, Jason and Liu, Qing and Lin, Zhe and Price, Brian and Xu, Dan},
  journal={arXiv preprint arXiv:2311.03355},
  year={2023}
}
```

# Video Generation from Single Semantic Label Map
|  ![CVPR 2019 logo][logo-cvpr] | Paper accepted at [2019 IEEE Conference on Computer Vision and Pattern Recognition (CVPR)](http://cvpr2019.thecvf.com/)   |
|:-:|---|

[logo-cvpr]: https://github.com/junting/seg2vid/blob/junting/figs/cvpr2019.png "CVPR 2019 logo"

| ![Junting Pan][JuntingPan-photo]  | ![Chengyu Wang][ChengyuWang-photo]  |  ![Xu Jia][XuJia-photo] | ![Jing Shao][JingShao-photo] | ![Lu Sheng][LuSheng-photo] |![Junjie Yan][JunjieYan-photo]  | ![Xiaogang Wang][XiaogangWang-photo]  |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| [Junting Pan][JuntingPan-web]  | [Chengyu Wang][ChengyuWang-web] | [Xu Jia][XuJia-web] | [Jing Shao][JingShao-web] |  [Lu Sheng][LuSheng-web] | [Junjie Yan][JunjieYan-web]  | [Xiaogang Wang][XiaogangWang-web]   |

[JuntingPan-web]: https://junting.github.io/
[ChengyuWang-web]: https://www.linkedin.com/in/chengyu-wang/
[XuJia-web]: https://stephenjia.github.io/
[JingShao-web]: https://amandajshao.github.io/
[LuSheng-web]: https://scholar.google.com.hk/citations?user=_8lB7xcAAAAJ&hl=en
[JunjieYan-web]: http://www.cbsr.ia.ac.cn/users/jjyan/main.htm
[XiaogangWang-web]: http://www.ee.cuhk.edu.hk/~xgwang/

[JuntingPan-photo]: https://github.com/junting/seg2vid/blob/junting/authors/juntingpan.png "Junting Pan"
[ChengyuWang-photo]: https://github.com/junting/seg2vid/blob/junting/authors/ChengyuWang.png "Chengyu Wang"
[XuJia-photo]: https://github.com/junting/seg2vid/blob/junting/authors/XuJia.png "Xu Jia"
[JingShao-photo]: https://github.com/junting/seg2vid/blob/junting/authors/JingShao.png "JingShao"
[LuSheng-photo]: https://github.com/junting/seg2vid/blob/junting/authors/lusheng.png "Lu Sheng"
[JunjieYan-photo]: https://github.com/junting/seg2vid/blob/junting/authors/JunjieYan.png "Junjie Yan"
[XiaogangWang-photo]: https://github.com/junting/seg2vid/blob/junting/authors/XiaogangWang.png "Xiaogang Wang"


## Abstract

This paper proposes the novel task of video generation conditioned on a SINGLE semantic label map, which provides a good balance between flexibility and quality in the generation process. Different from typical end-to-end approaches, which model both scene content and dynamics in a single step, we propose to decompose this difficult task into two sub-problems. As current image generation methods do better than video generation in terms of detail, we synthesize high quality content by only generating the first frame. Then we animate the scene based on its semantic meaning to obtain the temporally coherent video, giving us excellent results overall. We employ a cVAE for predicting optical flow as a beneficial intermediate step to generate a video sequence conditioned on the initial single frame. A semantic label map is integrated into the flow prediction module to achieve major improvements in the image-to-video generation process. Extensive experiments on the Cityscapes dataset show that our method outperforms all competing methods.


## Publication

Find our work on [arXiv](https://arxiv.org/abs/1903.04480). 

![Image of the paper](https://github.com/junting/seg2vid/blob/junting/figs/paper_thumbnail.jpg)

Please cite with the following Bibtex code:

```
@article{pan2019video,
  title={Video Generation from Single Semantic Label Map},
  author={Pan, Junting and Wang, Chengyu and Jia, Xu and Shao, Jing and Sheng, Lu and Yan, Junjie and Wang, Xiaogang},
  journal={arXiv preprint arXiv:1903.04480},
  year={2019}
}
```

You may also want to refer to our publication with the more human-friendly Chicago style:

*Junting Pan, Chengyu Wang, Xu Jia, Jing Shao, Lu Sheng, Junjie Yan and Xiaogang Wang. "Video Generation from Single Semantic Label Map." CVPR 2019.*


## Models

The Seg2Vid presented in our work can be downloaded from the links provided below the figure:

Seg2Vid Architecture
![architecture-fig]

Img2Vid Architecture
![img2vid-fig]

* [[Img2Img pretrained models]](https://github.com/NVIDIA/pix2pixHD)
* [[Img2vid pretrained models]](https://drive.google.com/drive/folders/1-EuWjU2-UOFDBCoD5JRHn0F5xbevIZZg)

[architecture-fig]: https://github.com/junting/seg2vid/blob/junting/figs/two_stage.png "seg2vid architecture"
[Img2vid-fig]: https://github.com/junting/seg2vid/blob/junting/figs/full_architecture.png "img2vid architecture"


## Visual Results
### Cityscapes (Generation)
| ![Generated Video 1]  | ![Generated Video 2]  |
|:-:|:-:|

[Generated Video 1]:https://github.com/junting/seg2vid/blob/junting/gifs/generation/gcity_1.gif
[Generated Video 2]:https://github.com/junting/seg2vid/blob/junting/gifs/generation/gcity_2.gif

### Cityscapes (Prediction given the 1st frame and its segmetation mask)
| ![Predicted Video 1]  | ![Predicted Video 2]  |
|:-:|:-:|
| ![Predicted Flow 1]  | ![Predicted Flow 2]  |

[Predicted Video 1]:https://github.com/junting/seg2vid/blob/junting/gifs/flow/pcity_1.gif
[Predicted Video 2]:https://github.com/junting/seg2vid/blob/junting/gifs/flow/pcity_2.gif
[Predicted Flow 1]:https://github.com/junting/seg2vid/blob/junting/gifs/flow/flow_1.gif
[Predicted Flow 2]:https://github.com/junting/seg2vid/blob/junting/gifs/flow/flow_2.gif

### Cityscapes 24 frames (Prediction given the 1st frame and its segmetation mask)
| ![Long Video 1]  | ![Long Video 2]  | ![Long Video 3]  |
|:-:|:-:|:-:|

[Long Video 1]:https://github.com/junting/seg2vid/blob/junting/gifs/length/lcity_1.gif
[Long Video 2]:https://github.com/junting/seg2vid/blob/junting/gifs/length/lctiy_2.gif
[Long Video 3]:https://github.com/junting/seg2vid/blob/junting/gifs/length/lcity_3.gif

### UCF-101 (Prediction given the 1st frame)
| ![UCF Video 1]  | ![UCF Video 2]  | ![UCF Video 3] | ![UCF Video 4]  | ![UCF Video 5]  | ![UCF Video 6]  |
|:-:|:-:|:-:|:-:|:-:|:-:|

[UCF Video 1]:https://github.com/junting/seg2vid/blob/junting/gifs/ucf101/ice_01.gif
[UCF Video 2]:https://github.com/junting/seg2vid/blob/junting/gifs/ucf101/ice_02.gif
[UCF Video 3]:https://github.com/junting/seg2vid/blob/junting/gifs/ucf101/ice_03.gif
[UCF Video 4]:https://github.com/junting/seg2vid/blob/junting/gifs/ucf101/violin_01.gif
[UCF Video 5]:https://github.com/junting/seg2vid/blob/junting/gifs/ucf101/violin_02.gif
[UCF Video 6]:https://github.com/junting/seg2vid/blob/junting/gifs/ucf101/violin_03.gif

### KTH (Prediction given the 1st frame)
| ![KTH Video 1]  | ![KTH Video 2]  | ![KTH Video 3] | ![KTH Video 4]  | ![KTH Video 5]  | 
|:-:|:-:|:-:|:-:|:-:|

[KTH Video 1]:https://github.com/junting/seg2vid/blob/junting/gifs/kth/kth_1.gif
[KTH Video 2]:https://github.com/junting/seg2vid/blob/junting/gifs/kth/kth_2.gif
[KTH Video 3]:https://github.com/junting/seg2vid/blob/junting/gifs/kth/kth_3.gif
[KTH Video 4]:https://github.com/junting/seg2vid/blob/junting/gifs/kth/kth_4.gif
[KTh Video 5]:https://github.com/junting/seg2vid/blob/junting/gifs/kth/kth_5.gif

## Getting Started

### Dataset
- Cityscapes
  - Cityscapes dataset can be downloaded from the [official website](https://www.cityscapes-dataset.com/) (registration required).
  - We apply Deeplab-V3 [github-repo](https://github.com/tensorflow/models/tree/master/research/deeplab) to get the corresponding semantic maps.
  - We organize the dataset following as below:
  ```
  seg2vid
  ├── authors 
  ├── figs
  ├── gifs
  ├── logos
  ├── pretrained_models
  ├── src
  ├── data
  │   ├── cityscapes
  │   │   ├── leftImg8bit_sequence
  │   │   │   ├── train_256x128
  │   │   │   │   ├── aachen
  │   │   │   │   │   ├── aachen_000003_000019_leftImg8bit.png
  │   │   │   ├── val_256x2128
  │   │   │   ├── val_pix2pixHD
  │   │   │   │   ├── frankfurt
  │   │   │   │   │   ├── frankfurt_000000_000294_pix2pixHD.png
  │   │   │   ├── train_semantic_segmask
  │   │   │   ├── val_semantic_segmask
  │   │   │   │   ├── frankfurt
  │   │   │   │   │   ├── frankfurt_000000_000275_ssmask.png
  │   │   ├── gtFine
  │   │   │   ├── train
  │   │   │   ├── val
  │   │   │   │   ├── frankfurt
  │   │   │   │   │   ├── frankfurt_000000_000294_gtFine_instanceIds.png
  ```

- KTH
  - We use the [KTH human action dataset](http://www.nada.kth.se/cvap/actions/) dataset, and we follow the data processing in [svg](https://github.com/edenton/svg).
- UCF-101
  - UCF-101 dataset can be downloader from the [official website](https://www.crcv.ucf.edu/research/data-sets/human-actions/ucf101/)

### Testing
```
  python -u test_refine_w_mask_two_path.py --suffix refine_w_mask_two_path --dataset cityscapes_two_path
```
### Training
```
  python -u train_refine_multigpu_w_mask_two_path.py --batch_size 8 --dataset cityscapes_two_path
```

### Seg2Vid on Pytorch

Seg2Vid is implemented in [Pytorch](https://pytorch.org/).

## Contact

If you have any general doubt about our work or code which may be of interest for other researchers, please use the [public issues section](https://github.com/junting/seg2vid/issues) on this github repo. Alternatively, drop us an e-mail at <mailto:junting.pa@gmail.com>.

<!---
Javascript code to enable Google Analytics
-->

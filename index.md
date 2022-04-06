---
# title: "Dual-AI: Dual Actor Interaction Learning for Group Activity Recognition"
# feature_image: "https://picsum.photos/1300/400?image=989"
feature_text: |
  # Dual-AI: Dual Actor Interaction Learning for Group Activity Recognition
  ###### [Mingfei Han](https://youthHan.github.io)\*, [David Junhao Zhang](https://junhaozhang98.github.io/)\*, Yali Wang\*, [Rui Yan](https://ruiyan1995.github.io/), [Lina Yao](https://www.linayao.com/), [Xiaojun Chang](https://www.xiaojun.ai/), [Yu Qiao](http://mmlab.siat.ac.cn/yuqiao/) :email:
  \* means equal contribution
  
---

### Abstract
Learning spatial-temporal relation among multiple actors is crucial for group activity recognition. 
Different group activities often show the diversified interactions between actors in the video. 
Hence, 
it is often difficult to model complex group activities from a single view of spatial-temporal actor evolution. 
To tackle this problem, 
we propose a distinct Dual-path Actor Interaction (Dual-AI) framework, 
which flexibly arranges spatial and temporal transformers in two complementary orders, 
enhancing actor relations by integrating merits from different spatio-temporal paths. 
Moreover, 
we introduce a novel Multi-scale Actor Contrastive Loss (MAC-Loss) between two interactive paths of Dual-AI. 
Via self-supervised actor consistency in both frame and video levels, 
MAC-Loss can effectively distinguish individual actor representations to reduce action confusion among different actors.
Consequently, 
our Dual-AI can boost group activity recognition by fusing such discriminative features of different actors. 
To evaluate the proposed approach, 
we conduct extensive experiments on the widely used benchmarks, 
including Volleyball, 
Collective Activity, 
and NBA datasets. 
The proposed Dual-AI achieves state-of-the-art performance on all these datasets. 
It is worth noting the proposed Dual-AI with 50\% training data outperforms a number of recent approaches with 100\% training data.
This confirms the generalization power of Dual-AI for group activity recognition, 
even under the challenging scenarios of limited supervision.

### Motivation

{% include figure.html image="/assets/motivation.png" position="center" %}
Accuracy per Category and Example of *left spike* and *right set* group activity. 
Red dashed line and Violet dashed line below show spatial and temporal actor interaction respectively. With spatial and temporal modeling applied in different orders, ST path and TS path learn different spatiotemporal patterns and thereby are skilled at different classes, supported by the accuracy plot.

### Remarkable Finding

{% include figure.html image="/assets/acc_plot.png" position="center" %}
*Accuracy comparison with data in different percentage on Volleyball dataset*

Our method achieves SOTA performance, and achieves 94.2% with 50% data, which is competitive to a number of recent approaches trained with 100% data. Solid point means result with additional optical flow input.
          
### Pipeline

{% include figure.html image="/assets/pipeline.png" position="center" %}
Our Dual-path Actor Interaction (Dual-AI) learning framework, where S-Trans and T-Trans denote Spatial-Transformer and Temporal-transformer respectively. It effectively explores actor evolution in two complementary spatiotemporal views, *i.e.*, ST path and TS path. Moreover, a Multi-scale Actor Contrastive loss is designed to enable interaction and cooperation of the two paths.

### Experiments
Our methods achieves SOTA results on multiple datasets, including the Volleyball Dataset, the Collective Dataset and the NBA Dataset under different kinds of supervision.


### Citation
If you use our method or code in your research, please consider citing the paper as follows:
```
@inproceedings{han2022dualai,
  title={Dual-AI: Dual-path Actor Interaction Learning for Group Activity Recognition},
  author={Han, Mingfei and Zhang, David Junhao and Wang, Yali and Yan, Rui and Yao, Lina and Chang, Xiaojun and Qiao, Yu},
  booktitle={Conference on Computer Vision and Pattern Recognition},
  year={2022},
  organization={IEEE}
}
```
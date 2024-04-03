

### Train: 
train train_nervcp.py -e
300
--lower-width
96
--num-blocks
1
--dataset
bunny
--frame_gap
1
--outf
bunny_ab
--embed
1.25_80
--stem_dim_num
512_1
--reduction
2
--fc_hw_dim
9_16_26
--expansion
1
--single_res
--loss
Fusion6
--warmup
0.05
--lr_type
cosine
--strides
5
2
2
2
2
--conv_type
conv
-b
1
--lr
0.0005
--norm
none
--act
gelu
--PE
kcPE

### Evalute: 
train train_nervcp.py -e
300
--lower-width
96
--num-blocks
1
--dataset
bunny
--frame_gap
1
--outf
bunny_ab
--embed
1.25_80
--stem_dim_num
512_1
--reduction
2
--fc_hw_dim
9_16_26
--expansion
1
--single_res
--loss
Fusion6
--warmup
0.05
--lr_type
cosine
--strides
5
2
2
2
2
--conv_type
conv
-b
1
--lr
0.0005
--norm
none
--act
gelu
--PE
kcPE
--eval_only
--weight
checkpoint/NeR_1.25_80/model_val_best.pth
## 🤗 *Acknowledgements*
This code is built on # NeRV: Neural Representations for Videos  (NeurIPS 2021)
### [Project Page](https://haochen-rye.github.io/NeRV). We thank the authors for sharing their codes of NeRV.

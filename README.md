## 该文件夹是用来存模式识别作业——convnext模型文件的目录
### 下面将针对子文件夹及模型文件进行简单的介绍： 
* （1）文件夹
```
├── conv_kernel_weight_results（analyze_kernel_weight.py脚本生成的部分权重、偏置等直方图）
├── convnext_no_transfer_learning（不使用迁移学习训练convnext模型的文件夹）
├── plot_img（传入TensorBoard进行可视化的图片，以及predict.py脚本单次预测的图片路径）
├── Post_experimental_processing（存放生成混淆矩阵及模型指标的脚本及图片）
├── runs（传入TensorBoard进行可视化的参数文件，通过train.py脚本生成）
├── tensorboard_results（TensorBoard可视化得到的结果图）
└── weights（保存了训练epochs为10次过程中验证集的val_accuracy最高的权重文件best_model.pth）
```
* （2）文件夹 -- 不使用迁移学习训练的文件夹convnext_no_transfer_learning
```
├── ntl_plot_img（传入TensorBoard进行可视化的图片）
├── ntl_runs（传入TensorBoard进行可视化的参数文件，通过ntl_train.py脚本生成）
├── ntl_tensorboard_results（TensorBoard可视化得到的结果图）
├── Post_experimental_processing_ntl（存放生成混淆矩阵及模型指标的脚本及图片）
└── weights（保存了训练epochs为50次过程中验证集的val_accuracy最高的权重文件ntl_best_model.pth）
```
* （3）文件 -- 不使用迁移学习训练的文件夹下的文件
```
├── class_indices.json（生成的json文件用于TensorBoard）
├── ntl_model.py（不使用迁移学习的convnext模型文件）
├── ntl_my_dataset.py（不使用迁移学习的自定义数据集的方法脚本）
├── ntl_predict.py（不使用迁移学习的模型预测脚本）
├── ntl_train.py（不使用迁移学习的convnext模型训练脚本）
└── ntl_utils.py（划分数据集，多GPU并行训练，构建TensorBoard可视化，动态学习率等功能的脚本）
```
* （4）文件 -- 使用迁移学习训练
```   
├── analyze_kernel_weight.py（生成直方图所应用的脚本）
├── class_indices.json（生成的json文件用于TensorBoard和predict.py中类别可视化索引）
├── convnext_base_22k_224.pth（官方下载的预训练模型权重文件）
├── model.py（convnext模型文件）
├── my_dataset.py（自定义数据集的方法脚本）
├── predict.py（模型的预测脚本）
├── README.md（文件类型解释）
├── train.py（模型训练脚本）
└── utils.py（划分数据集，多GPU并行训练，构建TensorBoard可视化，动态学习率等功能的脚本）
```
### 权重文件获取链接：
* （1）convnext网络不使用迁移学习训练得到的权重文件：[ntl_best_model.pth](https://drive.google.com/file/d/1k9z3dhlL6wWEECMrW37ZQxsTJTEKxz7j/view?usp=sharing)
* （2）convnext网络使用迁移学习所用的预训练权重文件：[convnext_base_22k_224.pth](https://drive.google.com/file/d/1hsDAW80OdbJCjzRnCl258QQwjxiWrDJR/view?usp=sharing)
* （3）convnext网络使用迁移学习训练得到的权重文件：[best_model.pth](https://drive.google.com/file/d/1jqrwSbBj3Lg24IzzsAd2pYRARkrg8Y7v/view?usp=sharing)
### 信息及维护时间：
```
作者：林飞
创建：2022-05-17
更新：2022-05-22
目的：使用convnext网络对Masked-Face-Dataset数据集进行训练，完成图像分类任务（是否带帽子）。
```

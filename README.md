# 项目一：基于NumPy实现OpenCLIP ViT-B-32图像编码器复现
深圳大学 Python程序设计大作业
仅使用NumPy实现ViT图像编码器前向传播，完成图像特征提取，不使用PyTorch、不训练模型。

## 目录结构
- image_encoder.py：核心代码，完成全部 6 处 TODO
- helpers.py：课程提供辅助函数
- check.py：分阶段数值校验脚本
- run.py：运行编码器输出特征
- requirements.txt：Python 依赖列表
- assets/images/：课程提供的10张测试图片
- report/main.tex：实验报告LaTeX源码
- report/figs/：报告配图
- weights/：【不上传GitHub】课程下发模型权重，仅本地运行使用

## 环境与依赖
Python >= 3.11
pip install -r requirements.txt

## 运行校验
python check.py --stage all
所有 stage 输出 PASS 代表实现正确，本项目全部校验通过。

## 运行推理
python run.py --output output_tokens.npz

## 实验结果
输出特征维度为 [B, 512]，特征经过 L2 归一化；数值误差在课程给定容差范围内。

## 本人贡献说明
helpers.py、预处理脚本、校验脚本由课程提供；本人独立完成 image_encoder.py 内 6 处 TODO 代码编写、调试。
参考输出仅用于 check.py 比对，不作为模型输入。

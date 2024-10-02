# WoundSegUnet
## Reference the following datasets for training, testing, and validaiton
-> https://www.kaggle.com/datasets/laithjj/diabetic-foot-ulcer-dfu
-> https://www.kaggle.com/datasets/leoscode/wound-segmentation-images

## Wound Image Segmentation using Deep CNN Architectures
Researcher: Daniel Doyon
Advisor: Drs. Edward H. Currie, Yimin Zhao

Wound closure is a tedious process that depends on the skill of the individual surgeon, and is prone to non-precision. Robotic Process Automation (RPA) has the potential to overcome inherent limitations of humans and offer to automate and streamline this process faster and more precisely  than humans. The segmentation of wound regions from patient images is critical for quickly marking the region of interest (the wound area), which can play a significant role in wound closure, and is the objective of this research. We implemented a wound image segmentation model of high accuracy via Deep Convolutional Neural Networks (CNN), which can be integrated into a gantry robotic wound system that can segment wounds on foreign data. Using this information, a PC controller can then automatically detect the edges of the wound using gray-scale processing, and guide the gantry system apply polymignytes fixtures to close the wound.

	The U-Net architecture was used as the main framework of the model, which is the gold standard for medical image segmentation with over 71,000 citations as of august 2024 [1]. The problem is that the base U-net architecture is limited in its accuracy. Tweaks must be made to achieve a high-performance model, especially for specific use cases like wound image segmentation.

The goal of this research was to maximize the dice score output by the model. The dice score is a measure of the overlap between the predicted segmentation mask and the ground truth mask. Several methods, such as data pre-processing, hyperparameter tuning, architecture tweaks, and model ensembling, can be the difference between a model that performs subpar, and groundbreaking.

So far, we have been able to achieve a dice score of accuracy .937, or 93.7%. With the implementation of better pre-processing and post processing methods, we may be able to increase the accuracy by a wider margin. Even with such high accuracy, the precision of the model is of the utmost importance in use cases like medical imaging. A 100% accurate model is nigh impossible at the risk of overfitting.  So, getting close to .95 - .98 is the objective we should strive for in the future.

References

Liu et al., “Ore image segmentation method using U-Net and Res_Unet convolutional networks”, RSC, Issue 16, 2024.

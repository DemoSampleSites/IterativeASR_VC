## Abstract
Many existing works on voice conversion (VC) tasks use automatic speech recognition (ASR) models for ensuring linguistic consistency between source and converted samples. However, for the low-data resource domains, training a high-quality ASR remains to be a challenging task. In this work, we propose a novel iterative way of improving both the ASR and VC models. We first train an ASR model which is used to ensure content preservation while training a VC model. In the next iteration, the VC model is used as a data augmentation method to further fine-tune and generalize the ASR model to diverse speakers. By iteratively fine-tuning and training the ASR and VC models, respectively, we experimentally show the improvement in the both the models. Our proposed method outperforms the one-shot English singing and Hindi speech VC baseline models in subjective and objective evaluations in low-data resource settings.

---
## One-shot Hindi Speech Voice Conversion
In this section, we showcase some samples from our proposed model and also provide samples from the baseline model for comparision on the Hindi speech domain.<br>
**All singers are unseen during the model training.** 

|              | Sample 1 (Female → Male) | Sample 2 (Male → Female) |
|:------------:|:-------:|:-------:|
|    **Source**    |    <audio controls="controls">  <source type="audio/wav" src="Samples/Hindi/0/0SPK_1-1_1526.wav"></source> </audio>   |    <audio controls="controls">  <source type="audio/wav" src="Samples/Hindi/1/0SPK_2-1_1001.wav"></source> </audio>  |
|    **Target**    |     <audio controls="controls">  <source type="audio/wav" src="Samples/Hindi/0/0SPK_2-1_1023.wav"></source> </audio>   |     <audio controls="controls">  <source type="audio/wav" src="Samples/Hindi/1/0SPK_1-1_1646.wav"></source> </audio> |
|    **Baseline**   |     <audio controls="controls">  <source type="audio/wav" src="Samples/Hindi/0/Iter_0_SRC_0SPK_1-1_1526_TRG_0SPK_2-1_1023.wav"></source> </audio>    |     <audio controls="controls">  <source type="audio/wav" src="Samples/Hindi/1/Iter_0_SRC_0SPK_2-1_1001_TRG_0SPK_1-1_1646.wav"></source> </audio>     |
| **Proposed Method** |    <audio controls="controls">  <source type="audio/wav" src="Samples/Hindi/0/Iter_3_SRC_0SPK_1-1_1526_TRG_0SPK_2-1_1023.wav"></source> </audio>     |    <audio controls="controls">  <source type="audio/wav" src="Samples/Hindi/1/Iter_3_SRC_0SPK_2-1_1001_TRG_0SPK_1-1_1646.wav"></source> </audio>      |

---

## One-shot English Singing Voice Conversion
In this section, we showcase some samples from our proposed model and also provide samples from the baseline model for comparision on the English singing domain.<br>
**All singers are unseen during the model training.**  

### Male to Male

|              | Sample 1 (PMAR(NUS48E) → M05(NHSS)) | Sample 2 (ZHIY(NUS48E) → PMAR(NUS48E)) |
|:------------:|:-------:|:-------:|
|    **Source**    |    <audio controls="controls">  <source type="audio/wav" src="Samples/Singing/0/PMAR-11-034.wav"></source> </audio>   |    <audio controls="controls">  <source type="audio/wav" src="Samples/Singing/1/ZHIY-14-006.wav"></source> </audio>  |
|    **Target**    |     <audio controls="controls">  <source type="audio/wav" src="Samples/Singing/0/M05-0S11_24-210.wav"></source> </audio>   |     <audio controls="controls">  <source type="audio/wav" src="Samples/Singing/1/PMAR-05-024.wav"></source> </audio> |
|    **Baseline**   |     <audio controls="controls">  <source type="audio/wav" src="Samples/Singing/0/Iter_0_SRC_PMAR-11-034_TRG_M05-0S11_24-210.wav"></source> </audio>    |     <audio controls="controls">  <source type="audio/wav" src="Samples/Singing/1/Iter_0_SRC_ZHIY-14-006_TRG_PMAR-05-024.wav"></source> </audio>     |
| **Proposed Method** |    <audio controls="controls">  <source type="audio/wav" src="Samples/Singing/0/Iter_2_SRC_PMAR-11-034_TRG_M05-0S11_24-210.wav"></source> </audio>     |    <audio controls="controls">  <source type="audio/wav" src="Samples/Singing/1/Iter_2_SRC_ZHIY-14-006_TRG_PMAR-05-024.wav"></source> </audio>      |

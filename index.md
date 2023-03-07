## Abstract
Many existing works on voice conversion (VC) tasks use automatic speech recognition (ASR) models for ensuring linguistic consistency between source and converted samples. However, for the low-data resource domains, training a high-quality ASR remains to be a challenging task. In this work, we propose a novel iterative way of improving both the ASR and VC models. We first train an ASR model which is used to ensure content preservation while training a VC model. In the next iteration, the VC model is used as a data augmentation method to further fine-tune and generalize the ASR model to diverse speakers. By iteratively fine-tuning and training the ASR and VC models, respectively, we experimentally show the improvement in the both the models. Our proposed method outperforms the one-shot English singing and Hindi speech VC baseline models in subjective and objective evaluations in low-data resource settings.

---
## One-shot Hindi Speech Voice Conversion
In this section, we showcase some samples from our proposed model and also provide samples from the baseline model for comparision on the Hindi speech domain.<br>
**All singers are unseen during the model training.** 

---

|              | Sample 1 (F05(NHSS) → PMAR(NUS48E)) | Sample 2 (PMAR(NUS48E) → F05(NHSS)) |
|:------------:|:-------:|:-------:|
|    **Source**    |    <audio controls="controls">  <source type="audio/wav" src="CroppedSources/F05_48.wav"></source> </audio>   |    <audio controls="controls">  <source type="audio/wav" src="CroppedSources/PMAR_43.wav"></source> </audio>  |
|    **Target**    |     <audio controls="controls">  <source type="audio/wav" src="CroppedSources/PMAR_1.wav"></source> </audio>   |     <audio controls="controls">  <source type="audio/wav" src="CroppedSources/F05_118.wav"></source> </audio> |
|    **Baseline**   |     <audio controls="controls">  <source type="audio/wav" src="Samples/Comparision/Singing_V_0/F2F/SRC_F05_48_TRG_PMAR_1.wav"></source> </audio>    |     <audio controls="controls">  <source type="audio/wav" src="Samples/Comparision/Singing_V_0/F2F/SRC_PMAR_43_TRG_F05_118.wav"></source> </audio>     |
| **Proposed Method** |    <audio controls="controls">  <source type="audio/wav" src="Samples/Comparision/Singing_V_2/F2F/SRC_F05_48_TRG_PMAR_1.wav"></source> </audio>     |    <audio controls="controls">  <source type="audio/wav" src="Samples/Comparision/Singing_V_2/F2F/SRC_PMAR_43_TRG_F05_118.wav"></source> </audio>      |

|              | Sample 1 (F05(NHSS) → ZHIY(NUS48E)) | Sample 2 (PMAR(NUS48E) → M05(NHSS)) |
|:------------:|:-------:|:-------:|
|    **Source**    |    <audio controls="controls">  <source type="audio/wav" src="CroppedSources/F05_48.wav"></source> </audio>   |    <audio controls="controls">  <source type="audio/wav" src="CroppedSources/PMAR_1.wav"></source> </audio>  |
|    **Target**    |     <audio controls="controls">  <source type="audio/wav" src="CroppedSources/ZHIY_14.wav"></source> </audio>   |     <audio controls="controls">  <source type="audio/wav" src="CroppedSources/M05_98.wav"></source> </audio> |
|    **Baseline**   |     <audio controls="controls">  <source type="audio/wav" src="Samples/Comparision/Singing_V_0/F2M/SRC_F05_48_TRG_ZHIY_14.wav"></source> </audio>    |     <audio controls="controls">  <source type="audio/wav" src="Samples/Comparision/Singing_V_0/F2M/SRC_PMAR_1_TRG_M05_98.wav"></source> </audio>     |
| **Proposed Method** |    <audio controls="controls">  <source type="audio/wav" src="Samples/Comparision/Singing_V_2/F2M/SRC_F05_48_TRG_ZHIY_14.wav"></source> </audio>     |    <audio controls="controls">  <source type="audio/wav" src="Samples/Comparision/Singing_V_2/F2M/SRC_PMAR_1_TRG_M05_98.wav"></source> </audio>      |

---

## One-shot English Singing Voice Conversion
In this section, we showcase some samples from our proposed model and also provide samples from the baseline model for comparision on the English singing domain.<br>
**All singers are unseen during the model training.**  

|              | Sample 1 (M05(NHSS) → F05(NHSS)) | Sample 2 (ZHIY(NUS48E) → PMAR(NUS48E)) |
|:------------:|:-------:|:-------:|
|    **Source**    |    <audio controls="controls">  <source type="audio/wav" src="CroppedSources/M05_118.wav"></source> </audio>   |    <audio controls="controls">  <source type="audio/wav" src="CroppedSources/ZHIY_14.wav"></source> </audio>  |
|    **Target**    |     <audio controls="controls">  <source type="audio/wav" src="CroppedSources/F05_48.wav"></source> </audio>   |     <audio controls="controls">  <source type="audio/wav" src="CroppedSources/PMAR_1.wav"></source> </audio> |
|    **Baseline**   |     <audio controls="controls">  <source type="audio/wav" src="Samples/Comparision/Hindi_V_0/M2F/SRC_M05_118_TRG_F05_48.wav"></source> </audio>    |     <audio controls="controls">  <source type="audio/wav" src="Samples/Comparision/Hindi_V_0/M2F/SRC_ZHIY_14_TRG_PMAR_1.wav"></source> </audio>     |
| **Proposed Method** |    <audio controls="controls">  <source type="audio/wav" src="Samples/Comparision/Hindi_V_3/M2F/SRC_M05_118_TRG_F05_48.wav"></source> </audio>     |    <audio controls="controls">  <source type="audio/wav" src="Samples/Comparision/Hindi_V_3/M2F/SRC_ZHIY_14_TRG_PMAR_1.wav"></source> </audio>      |

### Male to Male

|              | Sample 1 (M05(NHSS) → ZHIY(NUS48E)) | Sample 2 (ZHIY(NUS48E) → M05(NHSS)) |
|:------------:|:-------:|:-------:|
|    **Source**    |    <audio controls="controls">  <source type="audio/wav" src="CroppedSources/M05_98.wav"></source> </audio>   |    <audio controls="controls">  <source type="audio/wav" src="CroppedSources/ZHIY_14.wav"></source> </audio>  |
|    **Target**    |     <audio controls="controls">  <source type="audio/wav" src="CroppedSources/ZHIY_14.wav"></source> </audio>   |     <audio controls="controls">  <source type="audio/wav" src="CroppedSources/M05_98.wav"></source> </audio> |
|    **Baseline**   |     <audio controls="controls">  <source type="audio/wav" src="Samples/Comparision/Hindi_V_0/M2M/SRC_M05_98_TRG_ZHIY_14.wav"></source> </audio>    |     <audio controls="controls">  <source type="audio/wav" src="Samples/Comparision/Hindi_V_0/M2M/SRC_ZHIY_14_TRG_M05_98.wav"></source> </audio>     |
| **Proposed Method** |    <audio controls="controls">  <source type="audio/wav" src="Samples/Comparision/Hindi_V_3/M2M/SRC_M05_98_TRG_ZHIY_14.wav"></source> </audio>     |    <audio controls="controls">  <source type="audio/wav" src="Samples/Comparision/Hindi_V_3/M2M/SRC_ZHIY_14_TRG_M05_98.wav"></source> </audio>      |
